title: 'CSS: background-repeat'
author: int
tags:
  - css
categories:
  - css background
date: 2022-07-22 10:47:00
---
當用圖片當作背景圖案填滿元素時，除非刻意事先裁切圖片大小，不然不可能圖片會和元素大小一樣，更何況會有RWD的需求，在不同裝置上元素大小都可能會不同，那這時候圖片無法填滿的地方會怎麼呈現？ CSS會有一個屬性叫做background-repeat，並且預設值為repeat，所以就會出現下面的情況。

<iframe height="300" style="width: 100%;" scrolling="no" title="background-repeat" src="https://codepen.io/intHuang/embed/KKoqpPx?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/KKoqpPx">
  background-repeat</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

可以看到圖片用重複出現的方式填滿整個box，那如果不想要重複怎麼辦？ 這時候我們就可以利用background-repeat來做調整。

## repeat

```css
.box {
	background-repeat: repeat;
}
```

這是預設值，會沿著x軸與y軸重複(意即橫的跟直的方向都會用重複圖片的方式填滿)

## repeat-x

```css
.box {
	background-repeat: repeat-x;
}
```

只會沿著x軸(橫向)重複圖片，直的方向不會，直的填不滿會留白。

## repeat-y

```css
.box {
	background-repeat: repeat-y;
}
```

只會沿著y軸(直向)重複圖片，橫的方向不會，橫的填不滿會留白。

## no-repeat

```css
.box {
	background-repeat: no-repeat;
}
```

不重複任何圖片，填不滿的地方會留白。

## 結語

一般來說都會使用no-repeat並搭配background-position和background-size來調整圖片，通常不太會用repeat，又或者只會用到repeat-x來做出色塊重複的效果，單純的repeat或repeat-y很少使用。