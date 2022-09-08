title: 'CSS: word-wrap'
author: int
tags:
  - css
categories: []
date: 2022-09-08 20:14:00
---
word-wrap，又或者可以寫成overflow-wrap，是css中文字用來換行的語法。

* normal: 只在單字結束時換行，所以可能會導致文字超出div(overflow)。
* anywhere: 在單字結束時換行，如果沒有適合的斷點會強制換行，但會考慮soft wrap。
* break-word: 在單字結束時換行，如果沒有適合的斷點會強制換行，不考慮soft wrap。

## 範例

<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/intHuang/embed/JjvGOmz?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/JjvGOmz">
  Untitled</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

在範例中我設定box最大寬度是150px，最小寬度是最大字母的大小(這裡會顯示出anywhere和break-word的差異)。

在normal情況下，如果文字本身太長是不會換行的，即使這樣文字會超出容器。在anywhere時會換行，但是換行的基準是最小寬度。break-word則是會把依照normal的方式，但超出的字母會換行。

## 總結

一般情況都是使用break-word，並且word-wrap都會搭配word-break使用，下一篇我就會來介紹word-break。