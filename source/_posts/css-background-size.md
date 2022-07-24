title: 'CSS: background-size'
author: int
tags:
  - css
categories:
  - css background
date: 2022-07-24 11:06:00
---
background-size顧名思義，可以調整圖片的大小，除了可以用數字來調整外，還包含以下幾個值:

## contain

```css
.box{
	background-size: contain;
}
```

讓圖片盡可能填滿整個元素，並且用不裁切或擠壓到的方式，如果填不滿就會用repeat的方式填滿(除非你把repeat設為no-repeat，關於repeat可以看[這篇](https://huanginch.github.io/2022/07/22/css-background-repeat/))


## cover

```css
.box{
	background-size: cover;
}
```

把圖片盡量縮小成可以完全塞進去元素的大小，如果圖片會超出去元素，多的部分就會被裁掉。


## auto

```css
.box{
	background-size: auto;
}
```

在不改變圖片的任何屬性的情況下用圖片填滿背景。


## 範例

<iframe height="300" style="width: 100%;" scrolling="no" title="background-size" src="https://codepen.io/intHuang/embed/MWVoRBV?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/MWVoRBV">
  background-size</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>


除了以上三個屬性，還可以使用px、%、em等等單位，之後再配合background-position來調整位置，比較常見的作法是使用cover搭配background-posiiotn: center，如此就可以把圖片居中，並顯示出正中間的圖案。