title: 'CSS: z-index'
author: int
tags:
  - css
categories:
  - css position
date: 2022-07-12 20:30:00
---
一般排版的時候都是調整元素在網頁上的位置，也就是x、y軸，那如果想做出元素重疊時，要調整上下層就要調整z-index。

z-index的數值可以自己自訂(你想寫10000也沒人阻止你，但不見一這樣做，程式碼很難維護)，但都遵循一個原則，數字越大越上面。

## 語法
z-index的值分成兩種，一個是數字另一個是auto，如果設成auto就會自動安排z-index，莫認為越下面z-index越大，元素也越上層；如果不寫z-index預設值為0。

```css
.box1{
	z-index: 0;
}

.box2{
	z-index: auto;
}
```

## 範例

<iframe height="300" style="width: 100%;" scrolling="no" title="z-index" src="https://codepen.io/intHuang/embed/WNzGwPE?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/WNzGwPE">
  z-index</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

可以看到除了auto，z-index的數字是越大越上層，auto的部分則是按照順序安排權重。

## 結語
當然，你會看到我都有用到position，因為有使用到position才會出現元素重疊的情形，這時候z-index就是個好用的東西，好好運用就可以排出好看的排版。
