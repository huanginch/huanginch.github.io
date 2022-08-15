title: 'CSS: em 與 rem'
author: int
tags:
  - css
categories: []
date: 2022-08-15 23:16:00
---
我們平常寫網頁使用的單位是px，不過px是絕對單位，如果使用者改變預設字體大小，使用px單位的元素將不會跟著改變，這時候就會使用em或者rem這兩個相對單位。

## em

em的計算方式是看父層元素的大小再乘上給予的係數，比如我將某個p段落的font-size設定成1.5em，如果父層元素的font-size是16px，那這個p段落的font-size就會是32px。

## rem

rem的r代表的是root，所以會根據root的大小改變，一般瀏覽器預設字體大小都是16px，所以我任何文字的font-size設定成1.5rem都會是32px。

## 總結

em與rem不只會用於文字上，margin、padding等等有時也會使用em與rem，不過border、shadow、border-radius並不會使用em或rem，還是會使用px。

一般來說會使用的都是rem，因為rem是根據root來設定，em在計算上面較不方便。