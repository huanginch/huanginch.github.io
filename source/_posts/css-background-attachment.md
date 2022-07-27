title: 'CSS: background-attachment'
author: int
tags:
  - css
categories:
  - css background
date: 2022-07-27 15:23:00
---
background-attachment可以設定背景圖片、文字與viewport的關係，有三個屬性。

## fixed

```css
.box{
	background-attachment: fixed;
}
```

背景會被固定在viewport上，意及不管怎麼滾動網頁，背景圖都不會改變。

## local

```css
.box{
	background-attachment: local;
}
```

外層網頁在滾動的時候內層背景與內文會跟著滾動，滾動內層元素的時候背景與內文也會跟著移動(背景被固定在內文的位置)。

## scroll

```css
.box{
	background-attachment: scroll
}
```
滾動外層網頁時的效果和local相同，但滾動內層的時候只有內文會滾動，背景圖會被固定在viewport上(背景被固定在元素上)。

## 範例

* 建議使用0.5x觀看

<iframe height="300" style="width: 100%;" scrolling="no" title="background-attachment" src="https://codepen.io/intHuang/embed/OJvxxGO?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/OJvxxGO">
  background-attachment</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

從上到下分別是fixed、local、scroll，最後一個則是因為有兩張背景圖，所以分別設定了scroll和local兩個屬性，這理想示範的是可以同時為不同背景設定不同屬性。