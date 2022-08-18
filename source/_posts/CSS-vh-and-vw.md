title: 'CSS: vh、vw'
author: int
tags:
  - css
categories: []
date: 2022-08-18 16:00:00
---
在CSS中有兩個單位可以做到稱滿整個版面，一個是vh(view height)，一個是vw(view width)。

這兩個單位代表的是螢幕可視範圍高度與寬度的百分比，所以100vh與100vw分別代表100%
整個螢幕可視高度與100%螢幕可視寬度。

與%單位不同，%是以父層來計算，vw與vh是整個視窗，所以經常會用在banner上。

## 範例

<iframe height="300" style="width: 100%;" scrolling="no" title="vh and vw" src="https://codepen.io/intHuang/embed/mdxaXEZ?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/mdxaXEZ">
  vh and vw</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

這裡的example使用了vw與vh這兩個單位，所以會撐滿整個視窗。