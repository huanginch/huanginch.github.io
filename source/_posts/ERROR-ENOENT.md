title: 'HEXO ERROR: spawn ENOENT'
author: int
tags:
  - hexo
  - hexo error
categories: []
date: 2022-05-23 11:14:00
---
前幾天在更新文章到github時出現了一個錯誤碼:
```
Error: spawn ENOENT
```
<p>ENOENT是Error NO ENTry 或 Error No ENTity的縮寫，意思等同於常見的no such file or directory，中文意思就是檔案不存在或找不到路徑。</p>
<p>本以為是deploy需要的hexo-publish.bat沒寫好或_config.yml中哪裡沒設定好，但後來發現是文章我使用了中文命名才導致他無法辨識。</p>
<p>所以說<strong>不要用中文幫文章命名，標題可以建好檔案之後改</strong>。</p>
<p>也算是學了一課，不然當初找半天找不要哪裡錯。</p>