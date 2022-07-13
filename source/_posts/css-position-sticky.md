title: 'CSS: position:sticky'
author: int
tags:
  - css
categories:
  - css position
date: 2022-07-13 19:08:00
---
sticky像是結合了fixed和relative，有position: sticky的元素會像fixed一樣被固定在畫面上，但並不會超出父元素，一旦父元素超出畫面，sticky元素也會跟著消失在畫面上。

## 語法
```css
.box{
	position: sticky
}
```

## 範例

<iframe height="300" style="width: 100%;" scrolling="no" title="position: sticky" src="https://codepen.io/intHuang/embed/LYdRqXa?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/LYdRqXa">
  position: sticky</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

從範例中可以看到第二個sticky-box一旦碰到橘色的部分(另一個div)就不會固定在畫面上，而是會消失，至於sticky-box的位置，一樣可以透過top、bottom、left、right來控制，這部分在position: fixed有介紹過，用法是相同的。([傳送門](https://huanginch.github.io/2022/07/09/css-position-fixed/))

## 結語
sticky雖然好用，但要注意他是比較新的語法，部分瀏覽器可能無法支援(特別是IE)，可以透過[caniuse](https://caniuse.com/?search=sticky)來查詢是否支援。