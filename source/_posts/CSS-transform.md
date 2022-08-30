title: 'CSS: transform'
author: int
tags:
  - css
categories: []
date: 2022-08-30 21:42:00
---
transform提供開發者可以對元素旋轉、位移、縮放等等，只要使用對應的函式就能達到效果。

## 函式

* translate: 位移
```css
transform: translate(x, y);
```
* matrix: 向量變換
```css
transform: matrix(a, b, c, d, tx, ty);
```
* scale: 縮放
```css
transform: scale(sx);
transform: scale(sx, sy);
```
* rotate: 旋轉
```css
transform: rotate(a);
```
* skew: 傾斜
```css
transform: skew(ax);
transform: skew(ax, ay);
```