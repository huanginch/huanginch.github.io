title: 'CSS: animation and @keyframe'
author: int
tags:
  - css
categories: []
date: 2022-08-24 17:54:00
---
CSS提供了許多語法來做動畫，這裡要介紹的是@keyframe這個關鍵字，可以針對元素來做一連串的動畫。

## 語法

首先要在@keyframe關鍵字後面為自己的動畫做命名，到時候套用到元素上時會使用。@keyframe的語法有幾種，可以針對秒數來切割動畫效果，或是直接一次到底。

* from、to

```css
@keyframe myAnimation {
	from {top: 0px;}
    to {top: 200px;}
}
```

這個寫法元素就可以直接最左邊移動到最右邊

* 針對秒數細分

```css
@keyframes myAnimation {
  0%   {top: 0px;}
  25%  {top: 200px;}
  50%  {top: 100px;}
  75%  {top: 200px;}
  100% {top: 0px;}
}
```

這個寫法會將動畫持續時間切割成100等分，到達指定%數時會執行對應的動畫。假設動畫持續時間設定為4秒，那第0秒時會在top: 0px的位置，第一秒時(4*0.25)會移動到top: 200px的地方，依此類推

## 套用到元素上

要讓元素使用我們用@keyframe設定的動畫就要使用`animation`語法

```css
@keyframes myAnimation {
  0%   {top: 0px;}
  25%  {top: 200px;}
  50%  {top: 100px;}
  75%  {top: 200px;}
  100% {top: 0px;}
}

div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation: myAnimation 5s;
}
```

## animation

aniamtion也如同background、border等等，有多種屬性，並且可以合併成一個屬性。

* animation-name: 欲套用的@keyframe動畫名稱。
* aniamtion-duration: 動畫持續時間。
* aniamtion-duration-function: 動畫函式，css有寫好一些動畫函式，或是可以自己撰寫，可以參考[轉場動畫](https://huanginch.github.io/2022/08/17/CSS-transition/)。
* animation-delay: 動畫延遲時間。
* animation-iteration-count: 動畫重複次數，也可以使用infinite讓他永遠持續下去。
* animation-direction: 動畫的方向。
* animation-fill-mode: 動畫最後會停在哪格。
* animation-play-state: 動畫的播放狀態，有paused和running兩個屬性。

## 範例
<iframe height="300" style="width: 100%;" scrolling="no" title="Day 42-練習 keyframes" src="https://codepen.io/intHuang/embed/qBovwdE?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/qBovwdE">
  Day 42-練習 keyframes</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>