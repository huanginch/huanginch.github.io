title: 'CSS: text-align'
author: int
tags:
  - css
categories: []
date: 2022-07-30 16:50:00
---
text-align是css中用來對齊文字的屬性，可以將文字設定為靠左、靠右、置中等等。

## left

靠左對齊。

```css
h1 {
	text-align: left;
}
```

## right

靠右對齊。

```css
h1 {
	text-align: right;
}
```

## center

置中。

```css
h1 {
	text-align: center;
}
```

## justify

將文字用不同空格隔開以達到整個文字區塊寬度相等(除了最後一行)。

```css
h1 {
	text-align: justify;
}
```

## justify-all

與jutify基本相同，但最後一行也會包括在內。

```css
h1 {
	text-align: justify-all;
}
```

## start

靠元素開頭對齊。

```css
h1 {
	text-align: start;
}
```

## end

靠元素結尾對齊。

```css
h1 {
	text-align: end;
}
```

## match-parent

與父元素相同的對齊方式，但如果父元素的元素方向和子元素不同會以父元素的為準。

```css
h1 {
	text-align: match-parent;
}
```

* 上述提到的元素方向比較常見於因為float或flexbox所導致的軸線方向變換。