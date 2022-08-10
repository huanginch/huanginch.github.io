title: 'JQuery: $(document).ready()'
author: int
tags:
  - jquery
categories: []
date: 2022-08-10 13:30:00
---
在撰寫jquery時要特別注意，一般來說所有的程式都要寫在 $(document).ready()裡，這個函式代表網頁載入完成後該執行什麼，所以將一些動畫程式碼寫在這個外面會沒有作用。

## 語法

```js
$(document).ready(function(){
	//your code here
});
```

document指的是整個網頁，透過$()可以監聽，而ready()是確認監聽的元素是否完全載入好。

關於jquery基本介紹可以看[這篇](https://huanginch.github.io/2022/07/29/JQuery-intro/)