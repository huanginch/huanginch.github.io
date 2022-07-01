title: 如何使用HEXO建立個人部落格
tags:
  - hexo
categories:
  - hexo introduce
author: int
date: 2022-05-19 21:26:00
---
## 前言
**一些廢話，不想看可以直接看步驟**
<p>許多工程師都擁有自己的技術部落格，剛好在六角學院上課的時候有一小節就是在介紹寫部落格這件事，剛好趁這次機會開始養成寫部落格的習慣。</p>

一開始我跟著HEXO的 [官方文件](https://hexo.io/zh-tw/) 操作，不過中間的步驟可能是我誤解文件的意思還是怎樣，總之我按照首頁的步驟做是錯的，所以想說順便用這個主題來當作我的第一篇文章。

## 步驟:
1. 打開cmd(不會的可以按 window +R 輸入後 cmd 或直接在工具列的搜尋欄搜尋cmd)
2. 切到自己希望網站放置的資料夾，我是選D槽根目錄，當然你也可以選別的槽，又或者是在槽中建個資料夾來放之類的，不過他等等會自己產生一個叫blog的資料夾我就沒特別創資料夾了
3. 依序輸入下列指令
```bash
    $ npm install hexo-cli -g
    $ cd blog
    $ npm install
    $ hexo init blog
    $ hexo server
```
4. 依照指令執行完就建置好環境了，你的cmd應該會跳出一行字: **Hexo is running at http://localhost:4000/(如圖)**![](https://i.imgur.com/UKZ1SWm.png)

5. 在瀏覽器上輸入剛剛出現在cmd上的網址就可以成功打開Hexo部落格了

## 結語:
第一次寫部落格，挺有趣的，之後應該會記錄一些Hexo的使用方法跟程式課程的筆記
如果有任何問題歡迎和我聯繫