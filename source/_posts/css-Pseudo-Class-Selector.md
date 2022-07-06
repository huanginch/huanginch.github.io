title: 'CSS: 擬態選擇器'
author: int
tags:
  - css
categories:
  - css selector
date: 2022-06-22 14:05:00
---
在css中有種被稱作pesudo class的類別，可以用來做一些互動效果，最常見的就是a link上會用到的hover。而css中要選取pesudo class就要用到pesudo class selector，中文翻作擬態選擇器。

## 語法

```css
a:hover{
	color: #000;
}
```
使用分號後接上pesudo class的名稱就是pesudo class selector，常見的pesudov class除了hover還有 active、link等等。因為很多就不一一列出，有興趣可以參閱[MDN網站](https://developer.mozilla.org/zh-TW/docs/Web/CSS/Pseudo-classes)


這篇只是介紹最簡單的用法，因為深入的原理等等我還沒學會，如果有機會我會再寫文章來詳細介紹的。