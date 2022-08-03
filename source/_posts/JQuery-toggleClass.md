title: 'JQuery: toggleClass'
author: int
tags:
  - Jquery
  - ''
categories: []
date: 2022-08-03 17:18:00
---
我上次在[這篇](https://huanginch.github.io/2022/07/29/JQuery-intro/)簡單介紹了jQuery，這篇要來介紹其中一個常見的function: toggleClass。

這個函式是我在學如何製作漢堡選單時學習到的，之後也會寫一篇關於如何製作漢堡選單的文章。

## 用途

toggleClass可以改變class的有無，比如說我對一個按鈕點擊後想要對某個元素做出樣式改變就可以使用。以下面這個例子來說，我設定成點擊.menu-btn後會修改.navbar-list的show class狀態，如果.navbar-list有show class會移除，沒有就會新增。

```js
$('.menu-btn').click(function (e) {
    e.preventDefault();
    $('.navbar-list').toggleClass('show');
  });
```