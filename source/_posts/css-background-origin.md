title: 'CSS: background-origin'
author: int
tags:
  - css
categories:
  - css background
date: 2022-07-25 13:07:00
---
background-origin可以設定背景圖片的起點位置，分為以下三種:

## border-box

border-box會讓圖片從border正下方開始延伸，意即border會覆蓋在圖片上。
## padding-box

padding-box會讓圖片從padding開始延伸，所以border底下會留白，這個也是background-origin的預設值。

## content-box

content-box會讓圖片從content開始延伸，所以border和padding的部分會留白。

## 範例

<iframe height="300" style="width: 100%;" scrolling="no" title="background-origin" src="https://codepen.io/intHuang/embed/abYymLa?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/abYymLa">
  background-origin</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## 結語
要注意的是如果沒有下no-repeat，看起來會沒有差別，不過一般來說都會設定no-repeat就是。