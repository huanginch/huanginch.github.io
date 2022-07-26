title: 'CSS: background-clip'
author: int
tags:
  - css
categories:
  - css background
date: 2022-07-26 12:30:00
---
background-clip可以設定背景圖片會延伸到哪裡，和origin不同，origin是設定起點，從上次的範例就可以看出來，圖片下方還是會延伸到border底下。

* 上次的範例

<iframe height="300" style="width: 100%;" scrolling="no" title="background-origin" src="https://codepen.io/intHuang/embed/abYymLa?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/abYymLa">
  background-origin</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

background-clip有四種屬性:

## border-box

```css
.box {
	background-clip: border-box;
}
```
border-box會讓圖片延伸到border底下。

## padding-box

```css
.box {
	background-clip: padding-box;
}
```

padding-box會讓圖片延伸到padding底下，但border底下不會有圖片，會留白。

## content-box

```css
.box {
	background-clip: content-box;
}
```

content不會讓圖片超出content box的範圍，所以如果你的元素有padding和border，這兩個地方都會留白。

## text

```css
.box {
	background-clip: text;
	-webkit-background-clip: text;
  	color: transparent;
}
```

text不會讓圖片超出文字的部分，比較像是幫文字填色，但填的是圖片，要特別注意使用時要加上後面兩行，color的用意是避免圖片載入失敗，此時會導致text沒有顏色，加上color以避免這個情況，至於webkit是chrome的寫法，其他瀏覽器要稍微注意語法的支援。

## 範例
* 建議使用0.5x觀看

<iframe height="300" style="width: 100%;" scrolling="no" title="background-clip" src="https://codepen.io/intHuang/embed/xxWLMbe?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/xxWLMbe">
  background-clip</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>