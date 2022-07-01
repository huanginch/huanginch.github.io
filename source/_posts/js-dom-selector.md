title: 'Javascript: 選取DOM元素'
author: int
tags:
  - javascript
categories: []
date: 2022-05-31 11:16:00
---
在javascipt中，如果想操作Html的元素要先使用document.querySelector()等語法來選取，這篇會來介紹有哪些語法以及如何選取。

## 語法

* document.querySelector(): 最常見的語法，這個語法可以選取html中**第一個符合條件的元素**。
* document.querySelectorAll(): 與querySelector()用法相同，但會選取**所有符合條件的元素**，並回傳一個nodelist。
* document.getElementById(): 根據指定的id選取相對應元素。
* document.getElementByClassName(): 根據指定的class名稱選取相對應元素。
* document.getElementByTagName():根據指定的標籤名稱選取相對應元素。

## 選取元素
在qeuerySelector()與querySelectorAll()中，根據選取不同類型元素，條件寫法也不同。<br/>
* 選取html tag: 在單引號或雙引號中直接寫上標籤名稱即可
```js
document.querySelector('h1');
```
* 選取class name: 在在單引號或雙引號中寫上classname，但前面必須加.
```js
document.querySelector('.header');
```
* 選取id: 在單引號或雙引號中寫上id，但前面必須加#
```js
document.querySelector('#email');
```

其實選取方式就跟css的選取方式相同，所以說querySelector的部分也可以寫成這樣:
```js
document.querySelector('.header h1'); // 選取header class中的h1
```
在剩下的getElementBy...中，只需要在單引號或雙引號中寫下相對應的名字即可
```js
document.getElementById('email');
document.getElementByClassName('header');
document.getElementByTagName('h1');
```

這篇算是簡單整理，幫助自己記憶，平常的話我都使用querySelector()或querySelectorAll()而已，其他幾個視情況使用，分享給大家。