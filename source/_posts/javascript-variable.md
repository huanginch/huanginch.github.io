title: 'javascript: 變數宣告'
author: int
tags:
  - javascript
categories: []
date: 2022-06-02 11:02:00
---
javascript的變數宣告相對其他語言簡單容易的許多，這篇會簡單介紹怎麼宣告。

* var
	* 最早在javascript中只有這個語法可以用來宣告變數
    ```js
    var a;
    ```
* let 
	* 現在都使用這個語法來宣告變數
    ```js
    let a;
    ```
* const
	* 一旦被初始化就很難再被重新賦值
    ```js
    const a;
    ```
* 什麼都不寫
	* 沒錯，只寫變數名稱也能夠宣告，因為沒有寫的話會被當作是在window下的變數
    ```js
    a = 0;
    ```
    
相對於其他語言，javascript宣告變數真的簡單很多，也可能和他是弱型別語言有關，這部分我不是很了解，等有機會研究之後再來寫文。