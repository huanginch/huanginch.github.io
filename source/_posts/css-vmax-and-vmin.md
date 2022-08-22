title: 'CSS: vmax、vmin'
author: int
tags:
  - css
categories: []
date: 2022-08-22 23:11:00
---
vmax與vmin是css中的單位，與vh、vw很相似，都是依據viewport來改變大小的單位，與vh、vw相同，範圍是0~100。

## VMAX

vmax會找到viewport中較大的那邊，元素的長度或寬度會與那個邊相同長度，比如現在螢幕大小是1920*1080，假設我使用了一個元素他的寬度是100vmax，那麼這個元素的寬度會和螢幕寬度相同(1920 > 1080)。

## VMIN

和vamx相反，vmin會找較短的邊，該元素長度或寬度會與短邊相同。

## 範例

* 可以試著改變螢幕大小來觀看效果

<iframe height="300" style="width: 100%;" scrolling="no" title="vmax、vmin" src="https://codepen.io/intHuang/embed/XWEGVaW?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/XWEGVaW">
  vmax、vmin</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>