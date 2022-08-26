title: 'CSS: animation on scroll plugin'
author: int
tags:
  - css
categories: []
date: 2022-08-26 18:31:00
---
為了讓網頁看起來更豐富，很常會讓頁面在滾動時套用動畫，這篇會介紹最簡單達成這個目的的插件-[animation on scroll library](https://michalsnik.github.io/aos/)。

AOS插件提供了非常多樣的簡易載入動畫，如果只是要讓網頁呈現簡單的動畫，aos肯定是首選。

## 載入方法

1. npm、yarn

2. CDN

css: 
```html
<link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
```
js: 
```html
<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
```

## 使用

1. 在網頁中加入初始化js語法(可以寫在script中或寫在外部的js檔案)。
```js
AOS.init();
```
2. 在欲套用動畫的元素上加入對應的動畫函式。
```html
<div data-aos="fade-up"></div>
```

兩步驟結束，是不是超簡單XD<br/>當然也可以自訂動畫時間、動畫函式與滾動次數等等

```html
<div data-aos="fade-up"
     data-aos-duration="3000">
</div>
```

```html
<div data-aos="fade-down"
     data-aos-easing="linear"
     data-aos-duration="1500">
</div>
```

套用方式也是只要複製貼上就好，相當簡單。

## 結語

之前不知道有這個套件我都手寫jQuery還達不到自己想要的效果，自從知道這個套件後簡單的載入動畫我都改用這個了。