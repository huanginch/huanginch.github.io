title: 'CSS: background-attachment:fixed on safari'
author: int
tags:
  - css
categories: []
date: 2022-08-07 20:56:00
---
CSS有一個屬性叫background-attachment:fixed，詳細可以參考[這篇](https://huanginch.github.io/2022/07/27/css-background-attachment/)。

不過他有一個很大的問題，就是safari以及一些安卓瀏覽器上不支援。

我原本設計了一個網站，在body上下了一個背景並使用了background-attachment:fixed這個屬性，但卻因為這個理由我沒辦法完整呈現我的背景。

不支援的理由主要是過於耗能，可以參考[這篇](https://stackoverflow.com/questions/23236158/how-to-replicate-background-attachment-fixed-on-ios)。

那我能解決的辦法有兩個，一個是不要使用(沒錯，很像廢話，但查到的都是叫我改用scroll)，一個是改成用div以及position:fixed。

我當然是選擇後者，因為我還是希望我的網頁背景有fixed的效果，所以我在我的網頁最上面加上一個div並給他background-image

```html
<body>
  <div class="background"></div>
  ...
</body>
```

```css
.background {
    background: url("../images/background-lg.png") no-repeat, $secondary;
    background-size: cover;
    -webkit-background-size: cover;
    background-position: center;
    background-position-x: 50%;
    background-position-y: 50%;
    position: fixed;
    height: 100%;
    width: 100%;

    @include pad {
        background-image: url("../images/background-md.png");
        background-position: 80%;
        background-position-x: 80%;
    }
}
```