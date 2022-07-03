title: 'CSS: 標籤、類別、ID選擇器'
author: int
tags:
  - css
categories: []
date: 2022-07-03 11:28:00
---
CSS中要對html元素做操作就會需要用到所謂的選擇器來選取DOM元素，這裡會介紹幾個基礎且常見的選擇器。

## 標籤選擇器(Type Selector)
html中有許多的標籤，之前[這篇](https://huanginch.github.io/2022/06/27/html-tag/)也有介紹一些常見的標籤，想當然可以直接選取標籤並為他們制定規則[註1]。

<iframe height="300" style="width: 100%;" scrolling="no" title="tag selector" src="https://codepen.io/intHuang/embed/QWmbmzG?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/QWmbmzG">
  tag selector</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

標籤選擇器不需要多寫什麼，直接寫上標籤名稱即可，像我這裡就幫h1加了背景。

## 類別選擇器(Class Selector)
因為標籤選擇器只能選取所有相同類別的標籤而不能單獨對某個特定標籤做出處理，所以就有了類別選擇器，可以在標籤上加上屬性class，選擇時可以針對class name做選取

<iframe height="300" style="width: 100%;" scrolling="no" title="class selector" src="https://codepen.io/intHuang/embed/YzaXadM?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/YzaXadM">
  class selector</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

類別選擇器的寫法是在要選取的class name前面加上一個 **.**

## ID選擇器(ID Selector)
和類別選擇器很類似，ID選擇器也可以針對特定元素做出處理

<iframe height="300" style="width: 100%;" scrolling="no" title="ID Selector" src="https://codepen.io/intHuang/embed/poLJLYw?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/poLJLYw">
  ID Selector</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

和class寫法不同，ID是在ID前面加上 **#**

[註1]所謂的規則(Rule)指的就是選擇器加上css屬性，例如:
```css
h1{
	color: white;
}
```
## 總結

我自己比較常用到標籤與類別選擇器，至於類別和ID選擇器的差異會留到新文章來做比較。