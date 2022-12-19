title: 使用AOS套件後出現X軸
author: int
tags:
  - javascript
  - frontend
  - aos
categories: []
date: 2022-12-19 19:48:00
---
[AOS (Animation-on-Scroll)](https://michalsnik.github.io/aos/)套件是一個在網頁開發上很常使用的動畫套件，不過在使用到「**fade-left**」與「**fade-right**」時很常會發生網頁出現x軸的情形。


<iframe height="300" style="width: 100%;" scrolling="no" title="aos-overflow" src="https://codepen.io/intHuang/embed/rNrNyXW?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/rNrNyXW">
  aos-overflow</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

以上面的例子來說，在我頁面滾動到灰色區塊前都會有一個x軸存在，而造成這個原因正是「**fade-left**」與「**fade-right**」這兩個效果並用所導致；因為這兩個效果是利區塊位置改變(從負軸到正軸的位移)，所以就會產生x軸。(此情況也會發生在自己寫的animation-on-scroll上，道理是相同的。)

## 解決方法
知道原因之後要解決這件事其實很簡單，產生x軸的原因是元素超出畫面，那個幫他上個overflow-hidden把超出去的元素藏起來就好了。

為了一勞永逸，直接在body上面加上`overflow-x: hidden;`的style就可以了。

## 地雷
但這邊還有個小小地雷，在做RWD時你會發現手機版的`overflow-x: hidden;`上不去，這是因為手機版瀏覽器會自己加上`overflow: auto;`還是加在inline-style上，根本概不掉，所以這時候要用一個div把你的整個網頁包起來，`overflow-x: hidden`就寫在上面。

## 總結
這個問題困擾我好久了，害我一直沒辦法做左右淡入的動畫，還好有找到解決方法，希望這篇文章可以幫助跟我遇到相同問題的人。