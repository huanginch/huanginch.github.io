title: 'CSS: word-break'
author: int
tags:
  - css
categories: []
date: 2022-09-09 20:19:00
---
word-break是用來對內文做自動換行的語法，除了英文的斷行，也有針對中日韓語系的斷行設定。

* normal: 依照各語言的預設方法斷行(單字太長會超出)。
* break-all: 超過邊界就會自動斷行(包含中日韓)
* keep-all: 自動斷行，但在中日韓語系不適用，所以有使用到中日韓的網站不要使用。
* break-word: 即使單字太長也會自動斷行，和使用 ```word-break: normal``` + ```overflow-wrap: anywher```的效果相同。

## 範例

<iframe height="300" style="width: 100%;" scrolling="no" title="word-break" src="https://codepen.io/intHuang/embed/zYjqNpW?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/zYjqNpW">
  word-break</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>