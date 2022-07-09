title: 'CSS: position'
author: int
tags:
  - css
categories:
  - css position
date: 2022-07-08 11:44:00
---
position可以用來安排元素的位置，包含讓他們重疊或固定於網頁某個地方都能用position來實現，這篇會來介紹position的各種值以及和position相關的其他屬性。

不過因為有些屬性內容比較多我會改成用連結文章的方式，並且之後這幾天都會寫和positon相關的主題，之後再彙整過來。

## position屬性
1. static: 
	* 預設值，在static上不會有任何元素重疊。
    ```css
    h2{
    	position: static;
    }
    ```
2. absolute、relative:
	* 這兩個雖然分別是不同屬性但基本上都會一起使用。
    * [介紹文章傳送門]() (待補)
    ```css
    .parent-box{
    	position:relative;
    }
    
    .child-box{
    	position:absolute;
    }
    ```

3. fixed:
	* 可以將元素固定在網頁上，不論如何滑動頁面元素都不會消失。
	* [介紹文章傳送門](https://huanginch.github.io/2022/07/09/css-position-fixed/)
    ```css
    h2{
    	position: fixed;
    }
    ```
5. sticky
	* sticky比較像fixed + relative，可以讓子元素固定在畫面上，滾動時又不會超出父元素。
	* [介紹文章傳送門]() (待補)
    ```css
    h2{
    	position: sticky;
    }
    ```
  
## 其他元素定位相關屬性

## float

* 常用於文字與圖片，可做出文繞圖的樣式。
* [介紹文章傳送門](https://huanginch.github.io/2022/07/07/css-float/)

## z-index

* 可調整網頁z軸(也就是圖片與元素的重疊和上下關係)
* [介紹文章傳送門]() (待補)