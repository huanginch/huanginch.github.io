title: CSS介紹
author: int
tags:
  - css
categories: []
date: 2022-06-28 13:33:00
---
## 介紹
CSS，全名 Cascading Style Sheet，中文叫做階層式樣式表，是用來為網頁增加各種樣式，包括顏色、字體、排版等等，至於所謂的階層式代表著對同一個html元素可以增加不同的樣式規則，最後會顯示在網頁上的樣式則是由css的權重來決定。


## 歷史
css目前為止有三個版本，第一版出現於1996年，1998年推出第二版，同時也開始了css3的開發，也是我們目前正在使用的版本，時至今日css3依舊在開發中。至於未來會不會有css4，答案是否定的，因為有別於前兩版，css3的概念整個被翻新，他將各項功能模組化，所以未來只會有各種模組功能的更新，這也使得css的開發更加有彈性。

## 使用方法
想在html中使用css有三種方法

### inline
第一種是直接寫在html tag裡面，但就開發和維護上並不推薦這種做法
```html
<div style="background: red"><p>123</p></div>
```

### style tag
第二種一樣是寫在html裡面，但是會包在style tag裡
```html
<style>
  p{
  	background: red;
  }
</style>

<div><p>123</p></div>
```

### 另外寫一個檔案
就開發上來說，這個方法是最推薦的，因為方便維護，基本上除非用vue之類的框架，不然都會選擇這種方式
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>uHost</title>
    <link rel="shortcut icon" href="favicon.png">
    <link rel="stylesheet" href="main.css"> <!--加上自己寫的css file的link-->
</head>

<body>
    <main>
        <section id="product-overview">
            <h1>Get the freedom you deserve.</h1>
        </section>
        <section id="plans">
            <h1 class="section-title">Choose Your Plan</h1>
            <p>Make sure you get the most for your money!</p>
        </section>
    </main>
</body>

</html>
```
用codepen來示範會長這樣，html和css是不同檔案

<iframe height="300" style="width: 100%;" scrolling="no" title="Day2 - 移除圖片空隙" src="https://codepen.io/intHuang/embed/ZExEzPJ?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/ZExEzPJ">
  Day2 - 移除圖片空隙</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## 總結
之前寫了很多篇css的用法，但好像都沒有從頭開始介紹，才會有這篇，之後也會寫其他的用法，像是權重的比較之類。