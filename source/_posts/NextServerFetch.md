---
title: Send Cookie in Next.js Server Component
date: 2023-10-23 12:54:08
tags:
---
## 前言
好久沒更新了，這次在工作上遇到一點問題，也採了不少的坑，所以來記錄一下。

## 問題
為了追求 Performance，如果有使用到 SSR 框架(例如 Next 或 Nuxt)，有時會把獲取資料這個步驟放在 Server Componet 來做，如此一來資料會在 Client 端請求頁面當下就發送，而不是等到開始渲染頁面時才發送(可以參考[這篇文章](https://www.bugsnag.com/blog/server-side-rendering-and-authenticated-content/))。

不過這樣會有個問題，如果我們今天發送的請求是需要做身分驗證的，不論是透過 Session 還是 Token，我們都需要把 Cookie 帶上，但是在 Server Component 中，我們沒辦法直接使用 `document.cookie`[註] 來取得 Cookie，因為這是在 Server 端執行的，所以我們需要找到一個方法來取得 Cookie。

[註] 有時候會看到沒有設定 cookie 還是可以直接發送請求，那是因為瀏覽器自動幫我們在發送請求時也把 cookie 帶上，同樣 server 端也沒有這個功能。

## 解法
在 next 中，可能會看到某些文章表示可以使用 `getServerSideProps` 來取得 cookie，但是這個方法只適用12以下的版本，從13開始的版本已經不支援了，所以我們需要找到其他方法。

根據[官方文件](https://nextjs.org/docs/app/building-your-application/data-fetching/fetching-caching-and-revalidating#fetching-data-on-the-server-with-fetch)，他們已經把原生的 fetch 做擴充，所以不再需要 `getServerSideProps` 來取得資料，而是直接使用 `fetch` 就可以了。同時官方也提供了 [`cookie`](https://nextjs.org/docs/app/api-reference/functions/cookies) 以及 [`header`](https://nextjs.org/docs/app/api-reference/functions/headers) 可以讓我們在 server component 也能自定義 cookie 以及 header。

但是具體到底要怎麼攜帶 cookie ? 使用 TS 你就會發現 cookie() 給的資料根本不是字串而是 `ReadonlyRequestCookies` 這個型別，我參考了 stackoverflow 上的[這篇文章](https://stackoverflow.com/questions/76274546/next-js-does-not-send-cookies-with-fetch-request-even-though-credentials-are-inc)才知道要怎麼使用。cookie() 可以直接使用 toString()，所以在 header 中設定 cookie 時，可以直接使用 cookie().toString()。

## 例外處理
這邊也有一個小小的坑，就是 response 的錯誤處理，如果 server 掛了或是使用者給的資料不對導致 response 是 4xx 或 5xx 怎麼辦?

官方的範例:
```ts
async function getData() {
  const res = await fetch('https://api.example.com/...')
  // The return value is *not* serialized
  // You can return Date, Map, Set, etc.
 
  if (!res.ok) {
    // This will activate the closest `error.js` Error Boundary
    throw new Error('Failed to fetch data')
  }
 
  return res.json()
}
 
export default async function Page() {
  const data = await getData()
 
  return <main></main>
}
```

我們要另外設定一個 `error.tsx` 來處理，官方文件把他放在 [Error handling](https://nextjs.org/docs/app/building-your-application/routing/error-handling)的章節 (小抱怨: Fetch Data 章節沒有提供超連結也沒有額外說明和 error.ts 的關係，甚至在 ts 範例中的註解也沒有將 error.js 改成 error.ts 或 error.tsx。像我這種有問題才會翻文件的人很難去注意 Error handling 章節會和這裡有關。)

範例程式碼中的 `throw new Error('Failed to fetch data')` 會去觸發最靠近當前頁面的 error 文件，並且去渲染

```tsx
'use client' // Error components must be Client Components
 
import { useEffect } from 'react'
 
export default function Error({
  error,
  reset,
}: {
  error: Error & { digest?: string }
  reset: () => void
}) {
  useEffect(() => {
    // Log the error to an error reporting service
    console.error(error)
  }, [error])
 
  return (
    <div>
      <h2>Something went wrong!</h2>
      <button
        onClick={
          // Attempt to recover by trying to re-render the segment
          () => reset()
        }
      >
        Try again
      </button>
    </div>
  )
}
```

## 額外補充
這裡補充一個和前面比較無關，但同樣也是我在解決這個問題的過程中有遇到的狀況。

在使用 `fetch` 時，如果你的網址是使用相對路徑，例如 `/api/...`，那麼在 server component 中就會變成 `http://localhost:3000/api/...`，這樣就會導致跨域的問題，所以要改成使用絕對路徑，例如 `https://inthuang.tw/api/...`。當然在開發種比較常用到的是把網域設定成環境變數，例如 `process.env.NEXT_PUBLIC_DOMAIN`，這樣就可以在不同環境中使用不同的網域。

## 小結
這次的問題其實不算很大，但是在解決的過程中還是花了不少時間，也遇到了各種狀況糾纏在一起，所以就來記錄一下。