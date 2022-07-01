title: 'CSS: border-box'
author: int
tags:
  - css
categories: []
date: 2022-06-23 11:55:00
---
在css中常常要自己去計算padding、margin等等的推擠造成的盒模型大小不同，所以css有提供一個叫border-box的方法讓你不用去計算。

## box-sizing

這個就是用來選擇是否使用border-box，不修改的話預設會是content-box。
```css
.box{
	box-sizing: content-box;
}
```

## border-box

想要使用border-box只需要把content-box做修改即可

```css
.box{
	box-sizing: border-box;
}
```

## 套用到所有元素

因為border-box很方便，所以開發者通常會希望一次都套用到所有元素上，這時候就可以這樣寫

```
*, *:before, *:after{
	box-sizing: border-box;
}
```

這樣所有元素都會吃到border-box，* 代表全部，至於before和after就是擬態選擇器中有稍微提到的pesudo class，這部分以後會一起介紹。

其實我之前切版都沒有使用到，下次應該會來試試，這樣我就不用自己計算推擠了。

