title: 'CSS:float'
author: int
tags:
  - css
categories: []
date: 2022-07-07 11:09:00
---
float是一種可以讓元素漂移的屬性，用法很像word中常用的文繞圖，所以float也比較常應用在文字與圖片的排版，元素與元素間還是比較常使用flex box。

## 語法

1. none:
```css
.box{
	float: none:
}
```
	不使用float，預設也是這個。
    
2. right
<iframe height="300" style="width: 100%;" scrolling="no" title="float practice" src="https://codepen.io/intHuang/embed/MWVKBRj?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/MWVKBRj">
  float practice</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>
(推薦使用0.5x觀看)
可以看到圖片會飄到右邊，文字則是繞著圖片下來。

3. left
<iframe height="300" style="width: 100%;" scrolling="no" title="float right" src="https://codepen.io/intHuang/embed/LYdGJYm?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/LYdGJYm">
  float right</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>
(推薦使用0.5x觀看)
可以看到圖片會飄到左邊，文字和right一樣繞著圖片下來。

4. inline-start
<iframe height="300" style="width: 100%;" scrolling="no" title="float left" src="https://codepen.io/intHuang/embed/mdxVGyo?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/mdxVGyo">
  float left</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

元素會從容器的開頭，也就是上一個元素的最左邊開始延伸。

5. inline-end
<iframe height="300" style="width: 100%;" scrolling="no" title="float inline-start" src="https://codepen.io/intHuang/embed/KKoVxNN?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/KKoVxNN">
  float inline-start</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

元素會從容器的結尾，也就是上一個元素的最右邊開始延伸。

## 小結
其實inline-start跟inline-end看起來根本一樣，我還是有點搞不清楚它們差在哪裡，試了不同的排版方式他們看起來還是一樣，如果有人知道他們到底差在哪裡希望可以告訴我。
