title: 'CSS: Position: Absolute and Relative'
author: int
tags:
  - css
categories:
  - css position
date: 2022-07-14 11:40:00
---
這兩個屬性通常會一起出現，所以這邊把他們放在一起介紹，讓我們先從absolute開始看起。

## absolute

```css
.box{
	position: absolute;
}
```

absolute屬性會讓元素從document flow上移除，講的白話一點，就是網頁上的其他元素會無視這個元素，所以就會出現元素重疊，而這個absolute元素的位置可以透過top、bottom、left、right屬性來設定，這四個屬性的相關介紹可以看[這裡](https://huanginch.github.io/2022/07/09/css-position-fixed/)

可是他的位置是從哪裡算起的呢？答案是上一層並且有設定position的元素(除了position: static)，如果沒有那就會默認為起始的容器(通常都是body)

以下面這個例子來看(建議以0.25x觀看)，黃色方塊會跑到最底下，因為我將bottom設置為0，同時他上面的父元素並沒有設置position，所以默認會用body來做計算。

<iframe height="300" style="width: 100%;" scrolling="no" title="position: absolute " src="https://codepen.io/intHuang/embed/rNdWVRv?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/rNdWVRv">
  position: absolute </a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## relative

這時候如果想讓黃色方塊留在藍色方塊中，又不希望藍色方塊的位置跑掉，就可以使用position: relative

```css
.parent-box{
	position: relative;
}

.child-box{
	position: absolute;
}
```

設置了relative屬性的元素也可以透過top、bottom、right、left四個屬性來設定位置，基本上就與static相同，所以relative可以說是為了absolute而存在的。

從下面的例子就可以看到，我在藍色方塊設置了position: relative; 所以黃色方塊就被固定在藍色方塊的底部。

<iframe height="300" style="width: 100%;" scrolling="no" title="position: absolute " src="https://codepen.io/intHuang/embed/BarQNez?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/BarQNez">
  position: absolute </a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## 結語

absolute與relative算是很常用在元素內的排版，特別是有圖文的樣式，之前寫作業的時候也有用到，不過一開始我沒想到可以用absolute和relative，還在那邊用background image XD ，下次我就會記得了。