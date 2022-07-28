title: 'CSS: font'
author: int
tags:
  - css
categories: []
date: 2022-07-28 13:46:00
---
字型在網頁設計中是必不可少的一部份，這篇會來簡單介紹字型的屬性以及一些注意事項。

## 預設字體

每種作業系統與瀏覽器都有自己的預設字體，這裡主要介紹Windows和Mac，因為這兩種作業系統在PC上的市佔率最高。

* Windows: 常用中文字體有三種:新細明體(預設)、微軟正黑體、標楷體。英文有一種: Segoe UI。要特別注意雖然windows預設是新細明體，但在網頁設計上都會改成使用較好閱讀的微軟正黑，新細明體字體太細不適合閱讀，算是windows小雷的地方。


* Mac: 中文: 蘋方(預設)

其他系統預設英文字體可以參考[這篇](https://css-tricks.com/snippets/css/system-font-stack/)

在讀設計稿時常常會遇到一個問題: 設計師用Mac/Windows內建字體設計，我的電腦沒有那個字體怎麼辦，這時候只要使用你的系統的預設字體即可，比如windows就用微軟正黑，Mac就用蘋方。

## 在css中載入字型

```css
.body {
	font-family: 第一種字形, 第二種字形, "第三 種字形" 
}
```

想要在css中載入內建字體可以使用font-family，瀏覽器會從第一種字形開始套用，找不到就會套用第二種，以此類推，一般來說直接把字形名稱寫上去就好了，但如果遇到字體名稱有空格或無法載入就要加上單引號或雙引號。

## 載入外部字體

除了作業系統內建的字體我們也可以載入外部字體，最常用的就是Google Fonts，因為這樣就沒有跨作業系統而缺字體的問題。

一般來說中文會使用Noto Sans TC，這是Google與Adobe共同開發的開源字體，英文則會使用Roboto。<br>載入詳細步驟可以參考[這篇](https://hackmd.io/@YmcMgo-NSKOqgTGAjl_5tg/HJpJk8ABU/https%3A%2F%2Fhackmd.io%2F2nenMilfR7WSJSDI4WzcWA%3Fview)

## 字重

font還有一個屬性叫做font-weight，可以調整字體的粗細，可以細分為100、200...到900這幾種，不過要注意有些字體只有支援少數幾種字重，比如說微軟正黑只有Light(100)、Normal(400)、Bold(900)三種，所以大家才會選擇使用Google Fonts的Noto Sans TC，因為他支援100~900的字重。

在觀看設計稿時也要特別注意設計師設計的字重，常見的有Medium、Regular(Normal)、Bold，Normal是預設，Medium與Bold轉換成數字分別對應到500與900。

更多關於字重的介紹可以看[這篇](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight)

## css懶人包

這個懶人包包含了所有常見預設字體，依序為Mac->Windows->Android->IOS->通用字體，其中Arial與sans-serif為最常見也最多瀏覽器支援的字體，如果不想特別設計字體可以使用這個懶人包。

```css
body {
	font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Microsoft JhengHei", Roboto, "Helvetica Neue", Arial, sans-serif;
}
```