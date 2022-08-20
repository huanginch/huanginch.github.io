title: 'bs5: stretched-link'
author: int
tags:
  - css
  - bs5
categories: []
date: 2022-08-20 11:11:00
---
在設計網頁時我們很常將一個區塊作為可點擊的連結，例如可點擊的卡片、可點擊的文章等等，平常的情況下我們都會使用`a` tag來做出這樣的效果，不過bs5提供了一個更簡單的方法來實作。

## 使用方法

只要在對應區塊的a連結內加入`stretched-link` class就可以讓整個父層元素變得
可點擊。

* 以卡片為例

<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/intHuang/embed/dymaJwJ?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/dymaJwJ">
  Untitled</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## 原理

他是透過偽元素`::after`並用`position:absolute`讓a連結覆蓋整個元素，因為bs5的卡片元件本身就有`position:relative`的特性，所以可以直接使用，其他元件或自己寫的元素沒有的話要記得在最外層加上`position: relative`才會作用。

## 可能會讓連結無法延伸的原因

剛剛也提到`stretched-link`是透過position:absolute實作，所以只要有以下情況都可能讓他無法使用:

* static 以外的 position 值。
* none 以外的 transform 或 perspective 值。
* 在 transform 或 perspective 使用 will-change 作為值。
* none 以外的 filter 值，或是在 filter 使用 will-change 作為值 (只會在 Firefox 作用)。

在使用時要特別注意。