title: 'Javascipt: 陣列'
author: int
tags:
  - javascript
categories: []
date: 2022-06-07 13:14:00
---
在[資料型態](https://huanginch.github.io/2022/06/03/javascript-datatype/)那篇有介紹到array這個型別，這篇就會詳細介紹array的基本使用方法與概念。

## 宣告
陣列宣告會用中括號來表示，而陣列的值會放在中括號中，陣列的值可以是其他資料型態，但是每個值都必須是相同型態。
```js
// 空陣列
let arr1 = [];

// 數字陣列
let arr2 = [1, 2 ,3, 10];

//字串陣列
let arr3 = ["aaa", "bbb", "ccc"];
```
* 陣列的縮寫常會使用arr

## 取值

陣列有所謂的索引值，可以透過索引值取得對應的值，而索引值是從0開始，寫法如下

```js
let arr = [100, 520, 891];

console.log(arr[0]); //執行結果: 100
console.log(arr[1]); //執行結果: 520
console.log(arr[2]); //執行結果: 891
```

## 賦值

如果想要更改arr中的內容，寫法也跟取值一樣，並使用賦值運算子。
```js
let arr = [800, 900, 1000];

arr[0] = 1;
console.log(arr[0]); //執行結果: 1
console.log(arr); //執行結果: [1, 900, 1000]
```
可以看到arr第一個值(索引值0)變成了1。

## 新增

前面都只有針對已經有的值做處理，那如果我們想要增加一個元素進去該怎麼做?

* push():
	* 使用push可以在陣列最後面新增元素
    ```js
    let arr = [720, 800, 100];
    arr.push(500);
    console.log(arr); //執行結果: [720, 800, 100, 500]
    ```
* unshift()"
	* 使用unshift可以在陣列最前面新增元素
    ```js
    let arr = [720, 800 ,100];
    arr.unshift(500);
    console.log(arr); //執行結果: [500, 720, 800, 100]
    ```

## 刪除
 有了新增，自然也會有刪除
 
* pop():
 	* 與push相對，pop可以從陣列最後面刪除元素
    ```js
    let arr = [720, 800, 100];
    arr.pop();
    console.log(arr); //執行結果: [720, 800]
    ```
* shift():
	* 與unshift()相對，shift可以從最前面刪除元素
    ```js
    let arr = [720, 800, 100];
    arr.shift();
    console.log(arr); //執行結果: [800, 100]
    ```

## 取得長度
想取得當前陣列長度(意即有幾個元素)可以使用array.length。

```js
let arr = [1, 2, 3];

console.log(arr.length) //執行結果: 3
```

以上述程式碼來看，我宣告的arr使有三個元素的陣列，所以arr.length的值就會是3。

<br/>
    
基本操作就介紹到這邊，其他進階的array function會留到下一篇做講解。