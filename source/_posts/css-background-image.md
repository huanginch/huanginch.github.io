title: 'CSS: background-image'
author: int
tags:
  - css
categories:
  - css background
date: 2022-07-21 10:55:00
---
background-image可以為元素的背景設定圖像，通常是放上外部的圖片，不過除了圖片也能用其他的顏色函式(例如rgba、linear-gradient等)為背景上色，並且可以疊加。

## linear-gradient

linear-gradient函式可以做出顏色漸層，搭配background-image就可以做出以下效果:

<iframe height="300" style="width: 100%;" scrolling="no" title="background-image: linear-gradient" src="https://codepen.io/intHuang/embed/bGvWajY?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/bGvWajY">
  background-image: linear-gradient</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>


設定幾個顏色就會有幾個顏色由上到下依序等分漸層，如果你設定了to left、to right或是to bottom(如box2)，就會從指定的方向漸層(範例中為向左漸層)，如果設定數字，就會在指定的位置才開始出現漸層，以box2為例，紅色我設定為75%，所以從右邊向左邊漸層，到75%的地方才會開始出現漸層，同時也能使用角度來設定方向(如box3)。

## 圖層疊加

背景圖片也能疊加，可以圖片與圖片疊，也可以圖片與顏色疊加

<iframe height="300" style="width: 100%;" scrolling="no" title="background-image" src="https://codepen.io/intHuang/embed/jOzmZWX?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/jOzmZWX">
  background-image</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

他會從最後一個開始，一層一層疊上去。

## 結語
通常使用了background-image都還會配合background-position和background-size來調整位置，可以看考上一篇[background](https://huanginch.github.io/2022/07/20/css-background/)


