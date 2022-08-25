title: 'CSS: opacity'
author: int
tags:
  - css
categories: []
date: 2022-08-25 17:27:00
---
opacity顧名思義就是拿來調整透明度的，可以針對目標元素改變透明度，數值為0~1之間，0為完全透明，1為完全不透明。

## 語法

```css
div {
	opacity: 0.5;
}
```

## 範例

<iframe height="300" style="width: 100%;" scrolling="no" title="opacity" src="https://codepen.io/intHuang/embed/VwXOvyR?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/VwXOvyR">
  opacity</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

範例中的box1與box2正是使用了opacity的區別，一般來說opacity會應用在hover的效果，我通常會用在圖片上，讓圖片產生hover效果，而一般開發者常見的用法會是overlay，讓他產生一個有透明度的背景(overlay)覆蓋整個元素，範例中的box3就是應用了opacity與overlay來達到效果的。