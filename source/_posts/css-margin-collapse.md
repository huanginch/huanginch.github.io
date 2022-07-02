title: 'CSS: 邊界重疊(Margin Collapse)'
author: int
tags:
  - css
categories: []
date: 2022-07-02 11:55:00
---
在[盒模型篇](https://huanginch.github.io/2022/06/30/css-box-model/)有介紹了margin，這篇會來介紹在使用margin時會遇到的問題:邊界重疊

## 介紹
所謂邊界重疊，是發生在相連的元素之間如果都有寫上margin推擠，可能會導致重疊，舉個例子:
<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/intHuang/embed/abYOmqg?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/abYOmqg">
  Untitled</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

可以看到我用了top: 25px, bottom: 15px，照理來說兩個box之間的距離應該要是25+15 = 40px，但這裡看起來的距離只有25px，這就是所謂的邊界重疊(margin collapse)，上下邊界會重疊，並由較大的覆蓋較小的，這並不是什麼bug，當初設計時就是這樣設計的。

## 解決方法
如果你不希望發生邊界重疊，試著使用padding達到相同視覺效果，當然還有其他方法，可以參考[這篇](https://ithelp.ithome.com.tw/articles/10219975)，不過最推薦的方法還是使用padding。

## 總結
會發生margin collapse的似乎不只是兄弟元素，父子之間也會，但我目前還沒有研究過，之後等我了解了會再來編輯文章。