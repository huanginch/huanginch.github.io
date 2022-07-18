title: 'CSS: Max-width and min-width'
author: int
tags:
  - css
categories: []
date: 2022-07-18 19:13:00
---
max-width和min-width可以為元素設定最大寬度與最小寬度，讓元素的寬度不會被width的值所限制。

## 語法
```css
.box1{
	max-width: 50px;
}

.box2{
	min-width: 10px;
}
```

## max-width

元素的寬度不會超過max-width所設定的值

## min-width

元素的寬度不會小於min-width所設定的值

## 結語
這幾次寫作業為了讓寬度達到跟設計稿相同高度很常使用到max-width，一來是寬度最大就是那樣，二來會有簡易的RWD，相當好用。