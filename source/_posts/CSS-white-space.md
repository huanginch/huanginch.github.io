title: 'CSS: white-space'
author: int
tags:
  - css
categories: []
date: 2022-09-10 20:47:00
---
white-space是針對空格做換行的設定，有以下幾個選擇

* normal: 連續的空白字元會被合併(collapse)，換行字元被視為空白字元。換行只在被文字空間限制時發生。
* nowrap: 對待空白和換行字元的方式和normal一樣，但不會發生任何換行。
* pre: 連續的空白字元都會被保留。換行在有換行字元以及```<br>```時發生。
* pre-wrap: 連續的空白字元都會被保留。換行會在換行字元、有```<br>```元素以及被文字空間限制時發生。
* pre-line: 連續的空白字元會被合併(collapse)。換行在換行字元、 ```<br>```以及被文字空間限制時發生。

## 範例

<iframe height="300" style="width: 100%;" scrolling="no" title="white-spacec" src="https://codepen.io/intHuang/embed/VwxaOXM?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/VwxaOXM">
  white-spacec</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>