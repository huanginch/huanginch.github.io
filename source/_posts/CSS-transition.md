title: 'CSS: 轉場動畫(transition)'
author: int
tags:
  - css
categories: []
date: 2022-08-17 13:01:00
---
transition可以為樣式在改變時添加動畫，比如hover時可能會改變字體顏色、多條border等等，加入transition可以讓這個改變更加流暢。

## transition-property

要轉換的目標css屬性，比如color、border等等，也可以用all針對所有改變的屬性作出動畫。

```css
a {
	transition-property: all;
}
```

## transition-duration

設定動畫要持續多久

```css
a {
	transition-duration: 0.5s
}
```

## transition-timing-function
動畫呈現函式，可以自訂動畫呈現的效果，但這方面比較複雜，所以CSS也有提供幾個事先寫好的函式，更多可以參考[官方文件](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-timing-function)

* linear

* ease

* ease-in

* ease-out

* ease-in-out

* step-start

* step-end

關於動畫呈現效果我之後會補上文章

## transition-delay

設定延遲幾秒才出現動畫

```css
a {
	transition-delay:250ms;
}
```

## transition

上述的語法都可以簡寫成transition一個屬性

```css
a {
	transition: <property> <duration> <timing-function> <delay>;
}
```

## 範例

<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/intHuang/embed/oNqQmRg?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/oNqQmRg">
  Untitled</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

[註] transition要放在a上，不能放在hover上，否則滑鼠游標離開a時會沒有動畫。