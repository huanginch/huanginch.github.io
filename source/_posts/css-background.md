title: 'CSS: background'
author: int
tags:
  - css
categories:
  - css background
date: 2022-07-20 11:37:00
---
background是用來設定元素背景的屬性，除了常見的直接給予背景一個顏色，也可以給予一張圖片來做為背景，接著就會來介紹背景的各種屬性。

## 語法

### background
```css
.box{
	background: #fff, url(...), ...;
}
```

background所有屬性的縮寫，關於background的值都可以寫在這裡。
在寫的時候可以用 , 分開，用逗號隔開的一段會視為一次設定，後面的會蓋在前面的上面。

### background-color
```css
.box{
	background-color: #fff;
}
```

為背景設定單一顏色。

### background-image

```css
background-image: url(...);
```

為背景設定圖片，圖片會使用url語法來載入外部的圖片，可以同時載入兩張以上的url，也可以使用linear-gradient和linear-radius。

* [文章傳送門](https://huanginch.github.io/2022/07/21/css-background-image/)

### background-repeat

```css
background-repeat: no-repeat;
```

background-reapet會出現在當背景圖片無法填滿整個元素時，會依照設定的值以重複出現圖片的方式來填滿元素

* [文章傳送門](https://huanginch.github.io/2022/07/22/css-background-repeat/)

### background-position

```css
background-position: top;
```

可以設定背景圖的位置，可以使用top、bottom、left、right、center、數字、百分比、與各種單位來設定

* [文章傳送門](https://huanginch.github.io/2022/07/23/background-position/)

### background-size

```css
background-size: contain;
```

一般來說背景圖片不可能剛好符合元素大小，用size可以調整背景圖片的大小與圖片會從哪裡開始延伸。

* [文章傳送門](https://huanginch.github.io/2022/07/24/css-background-size/)

### background-origin

```css
background-origin: border-box;
```

可以設定背景圖的起始位置，是從邊界開始算，還是從邊界裡面開始算都可以用這個設定

* [文章傳送門](https://huanginch.github.io/2022/07/25/css-background-origin/)

### background-clip

```css
background-clip: border-box;
```
可以設定背景會延伸到哪裡，延伸到邊界停止、到邊界底下、或是留白，與origin有點相似

* [文章傳送門](https://huanginch.github.io/2022/07/26/css-background-clip/)

### background-attachment

```css
background-attachment: scroll;
```

設定背景與viewport(滾動畫面時所能看見的範圍)的關係

* [文章傳送門](https://huanginch.github.io/2022/07/27/css-background-attachment/)