title: 'Javascript: 陣列函式(上)'
author: int
tags:
  - javascript
categories: []
date: 2022-06-09 11:49:00
---
我們在[這篇文](https://huanginch.github.io/2022/06/07/Javascipt-array/)有提到陣列的基本性質介紹與簡單的賦值取值操作，這篇會來介紹可以用在陣列上的一些常用函式。

* forEach():
	* forEach有點像for迴圈，他會遍歷每個元素，用法如下。
    ```js
    let arr = [1, 2, 3];
    arr.forEach(function(item, index, arr){
    	console.log(item);
    })
    /*執行結果為:
    1
    2
    3
    */
    ```
    有幾個特別的地方要注意，首先，括弧內要放入一個函式，再來，函式傳入的參數至少要有一個item，但後面的index，array可以視情況加，而他們分別代表當前元素的值、索引值與陣列本身，值得提醒的一點，item、index、array這三個參數名稱不是固定的，你可以改成a、b、c也沒差，但還是建議用方便辨識的方法來命名。
    
* filter():
 	* 可以根據給的條件，回傳符合條件的元素陣列。
    ```js
    let arr = [1, 2, 3];
    
    let newArr = arr.filter(function(item){
    	return item > 1;
    })
    
    console.log(newArr); //執行結果: [2, 3]
    ```
    以這段程式碼來說，return後就是我所設的條件，其中傳入的function與item就和forEach一樣。與forEach不同的是，filter不會修改到原本的arr，而是會建一個新的array，所以我才會又宣告一個newArr來接。
    
* find():
	* find跟filter很像，都會去尋找符合條件的元素並回傳，但find只會找**第一個**符合條件的，所以他回傳的是元素不是陣列。
    ```js
    let arr = [1, 2, 3];
    
    let a = arr.find(function(item){
    	return item > 1;
    })
    
    console.log(a); //執行結果: 2
    
    ```
    
* findIndex():
 	* 從名稱可以看出來，這是用來找索引值的，而跟find相同，只會找符合的第一個元素。
    ```js
    let arr = [1, 2, 3];
    
    let aIndex = arr.find(function(item){
    	return item > 1;
    })
    
    console.log(aIndex); //執行結果: 1
    
    ```
    第一筆符合的是2，而2的index為1，所以結果為1。
    
* map():
	* map和forEach很像，唯一不同的是他會回傳新陣列。
    ```js
    let arr = [1, 2, 3];
    
    let newArr = arr.map(function(item){
    	return item > 1;
    })
    
    console.log(newArr); //執行結果: [false, true, true]
    ```
    map遍歷了arr中每個元素，並根據條件做出判斷，1沒有小於1所以是false，2、3都大於1所以是true。
    
* 除了forEahc之外，其他三個都會回傳一個新的陣列，所以要記得加上return才不會出錯，下篇我會來介紹slice、splice等等。