title: 'Bootstrap5: 格線系統'
author: int
tags:
  - css
  - bs5
categories: []
date: 2022-08-01 14:31:00
---
在Bootstrap中有一個很重要的東西稱作格線系統，BS5將網頁切分成row與column，一個row裡面會有12個column，所以在撰寫時會產生以下結構:

**container > row > column**

可以將網頁想成一個excel，container就是工作表，row與column就是欄位。

在常用的設計稿軟體中有些也支援格線系統(如Adobe XD、figma)，工程師可以依照設計師劃的格線為網頁原宿設定統一的寬度，不用去撰寫一些奇怪的寬高(我們稱為magic number，乍看之下沒辦法得到什麼語意化的資訊)

## 規則

row與column有個特別的規定，row裡面一定要接column，就像ul或ol裡面一定要接li，但container就沒有此限制。

### 正確例子

* ex1:
```html
<div class="container">
	<div class="row">
  		<div class="col-6"></div><div class="col-6"></div>
  	</div>
</div>
```
這是最標準的寫法，container接row再接column。

* ex2:
```html
<div class="container">
  	<h1>Title</h1>
	<div class="row">
  		<div class="col-6"></div><div class="col-6"></div>
  	</div>
</div>
```
container底下可以接其他標籤

### 錯誤例子
* ex1:
```html
<div class="container">
	<div class="row">
      	<h3>sub title</h3>
  	<div class="col-6"></div><div class="col-6"></div>
  	</div>
</div>
```
row後面一定要接col，所以這樣寫是錯的。


## 格線系統的RWD

格線系統也支援RWD，寫法為 ```col-size-number```，在col後面加上對應螢幕尺寸的代號(sm、md、lg、xl、xxl...)就可以達成RWD的效果。

## 結語
要特別注意，並不是網頁所有的元素都必須使用到格線系統，必須視情況使用，有時候我會在網頁中同時用到flex的排版與格線系統。

特別是文字的部分，因為設計師或客戶可能會更改設計稿的文字，所以就算一開始設計稿的某些文字部分是符合格線系統，也不要寫得剛剛好，又或者是就不要使用格線系統，避免之後修改或維護的困難。
