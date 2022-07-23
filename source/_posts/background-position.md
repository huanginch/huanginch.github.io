title: 'CSS: background-position'
author: int
tags:
  - css
categories:
  - css background
date: 2022-07-23 10:57:00
---
關於其他background的屬性都有提到，想要調整background的位置就要利用background-position這個屬性，除了各種數字單位外還可以使用top、bottom、left、right、center。

<iframe height="300" style="width: 100%;" scrolling="no" title="background-position" src="https://codepen.io/intHuang/embed/dymRddN?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/dymRddN">
  background-position</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

可以看到在box1我使用了center，所以背景圖片會居中，如果使用了top、bottom、left、right就會分別靠上、靠下、靠左、靠右。


也可以像box2那樣，寫了bottom和right之後分別寫上數字，此時圖片就會位於從右數來35%的位置，從下數來45%的位置。