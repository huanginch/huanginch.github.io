title: JQuery介紹
author: int
tags:
  - jquery
  - javascript
categories: []
date: 2022-07-29 15:19:00
---
此文章為觀看六角學院「[jQuery基礎教學](https://youtu.be/GVWOIP-HX70)」影片之筆記。

## 什麼是JQuery

JQuery是一個Javascript的函式庫，通常被用於網頁動畫呈現，優點是小、輕量、內容豐富且支援多個瀏覽器，所以很常被使用在網頁設計上。

## 載入方式

要把JQuery加入到自己的作品內有幾個方法:

1. [官網下載](https://jquery.com/)

2. CDN
```
https://cdnjs.cloudflare.com/ajax/libs/jquery/3.5.1/jquery.min.js
```
	* [其他版本CDN](https://cdnjs.com/libraries/jquery)
    
3. npm或yarn
```bash
npm install jquery
```
```bash
yarn install jquery
```


* 當然還有其他下載方法，詳細可以參考[官網](https://jquery.com/download/)

## 範例程式

```js
$(document).ready(function(){
	$('h1').hide();
})
```
在JQuery中使用了$()來代替listener，所以裡面會放置選擇器，再使用.functionname()來觸發目標函式以達到想要的效果。


## 常見函式

動態載入、改變屬性等等都是JQuery常見的用法，所以有時候觀看原始碼時會發現有些部分在HTML中工程師並沒有寫任何東西，那他可能是透過JQuery進行動態載入。例如常見的[Nivo Slider](https://themeisle.com/)都是使用JQuery作呈現。

## APIS

關於JQuery的所有函式都可以在官網文件找到:[傳送門](https://api.jquery.com/)
