title: 'html: 錨點'
author: int
tags:
  - html
categories: []
date: 2022-08-02 18:03:00
---
按下一個按鈕，可以往下滾動到頁面中相對應的區塊，這是網頁設計中很常使用到的技巧，要達成這個效果就要使用到Html中的錨點(anchor)。

## id

說到錨點就要提到html的一個屬性: id，id就像是當前區塊或元素的身分證，它代表了當前元素，所以整個頁面中id只會出現一次，而id就是所謂的錨點，透過找到這個獨一無二的id來達成。

```html
<div id="section1">
  ...
</div>
```
常見於html中的id。

## a標籤

那有了錨點，我們要怎麼讓使用者能使用這個功能？這時候就會用到a連結，我們一般預設a連結會寫成如下:

```html
<a href="#">link</a>
```
那個href所指向的#指的就是首頁，如果改成id的名稱就可以跳轉到那個區塊。
但是，所有id名稱前面都要加上#，否則他會認為是外部連結。

## 範例

<iframe height="300" style="width: 100%;" scrolling="no" title="Day 27-錨點練習" src="https://codepen.io/intHuang/embed/RwMQVPq?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/RwMQVPq">
  Day 27-錨點練習</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>