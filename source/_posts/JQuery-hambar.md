title: 使用JQuery製作漢堡選單
author: int
tags:
  - jquery
  - css
categories: []
date: 2022-08-09 20:19:00
---
漢堡選單是一個很常使用在手機版網頁的菜單呈現方式，因為按鈕是三條線，很像一個漢堡所以稱為漢堡選單。

![hambar](../images/pasted-99.png)

## 原理

漢堡選單的原理是利用jquery的toggleClass來為navbar新增或移除css class，所以分成兩個部分，一個是css，一個是jquery。

## CSS

```css
.navbar{
	width: 100%;
	max-height: 0%;
    position: absolute;
    bottom: 0;
    left: 0;
    z-index: 10;
    transform: translateY(100%);        
    overflow: hidden;
    transition: max-height 0.7s;
    background: $navbar__color;
}
.navbar.show{
	max-height: 500px;
}
```

首先是navbar的樣式，將navbar的高度設為0讓它消失，並用position和transform將navbar固定在自己想要的位置，transition設定展開動畫，overflow將多餘的內容隱藏，背景色設定成和原本的navbar相同。

.show將navbar的高度變成500px(這裡可以自訂)，因為transition的緣故會產生動畫。

## JQuery

```js
$('.menu-btn').click(function (e) {
    e.preventDefault();
    $('.navbar').toggleClass('show');
  });
```
按下漢堡選單後(我這裡的class叫menu-btn)，對navbar新增show class，所以高度會變成500，這時菜單就會出現了。而e.preventDefault()單純是用來取消a的預設動作。

## 範例

<iframe height="300" style="width: 100%;" scrolling="no" title="hambar" src="https://codepen.io/intHuang/embed/KKoBpwG?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/KKoBpwG">
  hambar</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

