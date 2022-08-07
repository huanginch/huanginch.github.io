title: owl-carousel drag bug
author: int
tags:
  - jquery
  - owl-carousel
categories: []
date: 2022-08-06 21:58:00
---
owl-carsouel是一個jquery插件，提供滾動式卡片樣式與動畫，[官網](https://owlcarousel2.github.io/OwlCarousel2/)，但是我卻發現他有一個bug，在手機版上如果左右滑動後點擊事件會失效。

查了查後發現是owl-carsouel一直以來的bug，按著[這篇](https://github.com/OwlCarousel2/OwlCarousel2/issues/1864)試著解決這個bug，簡單來說要把owl.carousel.js或owl.carousel.min.js中的`(Math.abs(d.x)>3||(new Date).getTime()-this._drag.time>300)`改成`((Math.abs(delta.x) > 3 || new Date().getTime() - this._drag.time > 300) && event.type === 'mouseup')`，我這著做之後在電腦上即使使用開發人員工具換成手機模式也不會產生bug了可喜可賀。

但是，沒錯，但是我用手機開網頁這個bug還是在，真的尷尬，現在我查不到任何解決方法了，值得慶幸的是再點一次同樣可以觸發，如果有人知道如何解決歡迎告訴我。