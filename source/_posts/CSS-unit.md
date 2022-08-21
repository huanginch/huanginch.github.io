title: 'CSS: 單位(unit)'
author: int
tags:
  - css
categories: []
date: 2022-08-21 17:34:00
---
在CSS中有許多的單位提供開發者使用，不同情況下適合的單位都不同，這篇將會彙整所有CSS可以使用的單位。

## 絕對單位

不會隨著root大小或螢幕大小改變的單位。

|Unit|Description|
|----|----|
|cm|公分|
|mm|毫米|
|in|英吋|
|px|像素|
|pt|points(1pt = 1/72 of 1in)|
|pc|picas (1pc = 12 pt)|

## 相對單位

會自適應的單位，為了因應RWD的需求，現在大多使用這些單位來做開發。

|Unit|Description|
|----|----|
|em|[介紹文章](https://huanginch.github.io/2022/08/15/css-em-and-rem/)|
|ex|根據x軸的高度改變(很少使用)|
|ch|根據字元'0'的大小改變|
|rem|[介紹文章](https://huanginch.github.io/2022/08/15/css-em-and-rem/)|
|vw|[介紹文章](https://huanginch.github.io/2022/08/18/CSS-vh-and-vw/)|
|vh|[介紹文章](https://huanginch.github.io/2022/08/18/CSS-vh-and-vw/)|
|vmax|根據viewport最小邊改變|
|vmin|根據viewport最大邊改變|
|%|百分比|

## 結語

最常使用的單位是px、rem、vw、vh、%這幾個，如果可以的話盡量使用px以外的其他幾種單位，因為px是絕對單位。不過並不是所有元素都要更改成相對單位，如果是border或shadow之類的寬度還是會習慣使用px，因為我們通常不會希望這些樣式改變。