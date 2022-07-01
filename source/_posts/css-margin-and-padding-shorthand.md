title: 'CSS: Margin 、 Padding與Border 的寫法與縮寫'
author: int
tags:
  - css
categories: []
date: 2022-07-01 11:40:00
---
在[上一篇盒模型](https://huanginch.github.io/2022/06/30/css-box-model/)介紹了margin、padding和border，所以這篇會來介紹在css中的寫法。

## Marign
在上一篇中有提到margin有分上下左右，所以寫法也有分上下左右。

### 全部相同寬度
```css
h2{
	margin: 5px;
}
```
### 個別設定
```css
h2{
	margin-top: 5px;
    margin-bottom: 10px;
    margin-left: 12px;
    margin-right: 8px;
}
```

### 縮寫
你可能會想說，這樣我要設定只有一邊不同不就很麻煩嗎？所以css有提供縮寫寫法:

```css
h2{
	margin: 5px 8px 10px 12px;
}
```
以上從左到右分別為上、右、下、左

```css
h2{
	margin: 5px 12px;
}
```
以上從左到右為上和下、左和右

## Padding
padding的寫法跟margin很像

### 全部相同寬度
```css
h2{
	padding: 5px;
}
```
### 個別設定
```css
h2{
	padding-top: 5px;
    padding-bottom: 10px;
    padding-left: 12px;
    padding-right: 8px;
}
```
### 縮寫
和margin一樣，padding也有縮寫寫法
```css
h2{
	padding: 5px 8px 10px 12px;
}
```
以上依序為上、右、下、左

```css
h2{
	padding: 5px 10px;
}
```
以上依序為上和下、左和右

## Border
border的位置設定也和margin、padding一樣，不同的是border可以設定樣式、顏色、寬度等等

### 個別設定
```css
h2{
	border-top-width: 5px;
    border-top-color: #000;
    border-top-style: solid;
    ...
}
```

### 縮寫

#### 全部相同
```css
h2{
	border: 5px solid #000;
}
```
以上順序可以調換
#### 個別設定
```css
h2{
	border-top: 5px solid #000;
    border-bottom: 1px dashed #fff;
    border-left: 3px dotted #000;
    border-right: 10px solid #000;
}
```
以上順序可以調換


個人覺得有縮寫真的很方便，之前不知道有縮寫的時候還笨笨的一個一個寫，code變有夠長的，自從學會了縮寫整個世界都不一樣了呢XD