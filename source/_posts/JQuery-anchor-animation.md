title: 'JQuery: Html錨點動畫'
author: int
tags:
  - jquery
  - html
categories: []
date: 2022-08-05 20:44:00
---
我在[這篇](https://huanginch.github.io/2022/08/02/html-anchor/)有介紹到html中的錨點，而本篇會來介紹如何用JQuery來讓跳轉的動畫變得流暢。

## 載入JQuery

首先第一步當然是載入JQuery，載入的方法在[JQuery介紹](https://huanginch.github.io/2022/07/29/JQuery-intro/)有說明。

## 撰寫JQuery

```js
//回頂部
$('h1').on('click', function () {
    $("html,body").animate(
      {
        scrollTop: 0 //回到第一個區塊
      },
      800
    );
  })
  
  //其它連到對應區塊
  $(".navbar-list a").on("click", function () {
    var hrefLink = $(this).attr("href");
    console.log(hrefLink);
    $("html,body").animate(
      {
        scrollTop: $(hrefLink).offset().top//直接到相對位置
      },
      800
    );
  });
```

* 首先我們來一步一步拆解，回頂部區塊就是會滾動回網頁最頂部，用在href="#"的link中，所以當相對應得標籤被點擊(在我這裡是h1)，html和body就會用animate function滾回頂部，用800毫秒的時間，而這裡最重要的就是scrollTop()，scrollTop代表目前viewport最頂端的元素在網頁中的位置，所以將scrollTop設為0就會回到頂部。

* 接著是其他按鈕會滾動到對應區塊的動畫，同樣按了對應的按鈕(我這裡叫navbar-list裡的a)就會產生滾動動畫，透過hrefLink取得id，再透過.offset().top，取得那個元素的頂部座標，就會產生滾動動畫了。