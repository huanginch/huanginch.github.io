title: 'CSS: 後代選擇器'
author: int
tags:
  - css
categories: []
date: 2022-06-11 19:29:00
---
在CSS中，如果要選取DOM元素、class name、tag name等等來做選取，然而HTML可能會有一層包一層的情況，如果不想要設定很多classname來做選取就可以使用後代選擇器。

## 語法
<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/intHuang/embed/RwQqYLV?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/RwQqYLV">
  Untitled</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

可以看到我在.header後面加上li，並用空格隔開，這種寫法就是後代選擇器，可以針對選到的DOM元素的後代再進行選取，這個算是非常常用也非常實用的一種做法。

到這裡就差不多了，雖然這篇的篇幅很短，後代選擇器也很簡單，但不代表他不重要，基本上每個網頁都一定會使用到後代選擇器，他就是如此方便。