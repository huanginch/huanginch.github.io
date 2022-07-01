title: 'javascript: 常見資料型態'
author: int
tags:
  - javascript
categories: []
date: 2022-06-03 14:49:00
---
這篇會簡單整理常見的javascript資料型態

* number
	* 數字型別，不管整數小數都是number type
* string
	* 字串型別，用單引號或雙引號包起來都行
* boolean
	* 布林值，只有true和false兩種值
* array
	* 用 [ ] 表示，可以存數字、字串、陣列、物件等等，但每筆資料型態必須相同，表示方式為
    ```js
    let arr = ["a", "b", "c"]
    ```
* object
	* 用 { } 表示，包含屬性與值，可以是數字、字串、陣列、物件等等，每筆資料都可以是不同型態，表示方式為
    ```js
    let obj = {
    	name: "Andy",
        age: 5
    }
    ```
* null
	* 空值
* Undefined
	* 未定義，任何變數在被初始化前都是未定義
    
當然這只是列出常見的，還有其他我比較不了解的我沒有列出來，就只是記錄比較常用的這樣。