title: 'CSS: Overflow'
author: int
tags:
  - css
categories: []
date: 2022-07-19 12:11:00
---
有時候會有元素太大導致超出父元素的問題，這就叫做overflow(特別容易發生在有設定高度的元素中)，以下面為例:

<iframe height="300" style="width: 100%;" scrolling="no" title="css:overflow" src="https://codepen.io/intHuang/embed/qBormgx?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/qBormgx">
  css:overflow</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

可以看到文字超出了parent

通常的作法是不設定高度，讓元素按照內容去伸展高度，但如果說我今天就是希望這個元素這麼高，這時候就可以使用overflow這個屬性

## Overflow

* visible

```css
.box{
	overflow: visibile;
}
```

預設值，呈現效果等同上面的例子。

* hidden

將overflow的元素藏起來

```css
box{
	overflow: hidden;
}
```

<iframe height="300" style="width: 100%;" scrolling="no" title="css:overflow" src="https://codepen.io/intHuang/embed/mdxWmov?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/mdxWmov">
  css:overflow</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

可以看到多餘的部分都消失在元素內了。

* scroll

```css
.box{
	overflow: scroll;
}
```
<iframe height="300" style="width: 100%;" scrolling="no" title="css:overflow: hidden" src="https://codepen.io/intHuang/embed/rNdymbm?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/rNdymbm">
  css:overflow: hidden</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

讓子元素保持在父元素內，可以用上下左右滾動的方式看到超過的部分。

* auto、overlay
```css
.box{
	overflow: auto;
}
```

<iframe height="300" style="width: 100%;" scrolling="no" title="css:overflow: auto" src="https://codepen.io/intHuang/embed/LYdWyvm?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/LYdWyvm">
  css:overflow: auto</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

讓子元素保持在父元素內，和scroll不同，只能用上下滾動的方式看到超過的部分。
而overlay和auto相同，只是不同瀏覽器支援不同語法。
