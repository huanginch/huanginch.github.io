title: 'Javascript: 陣列函式(下)'
author: int
tags:
  - javascript
categories: []
date: 2022-06-10 10:38:00
---
我們在[上篇](https://huanginch.github.io/2022/06/09/Javascript-array-function/)介紹了forEach、filter、find、findIndex和map，這篇會來介紹其他常用的陣列函式。

* slice():
	* slice可以從給定的範圍複製一份新的array。
    ```js
    let arr = [1, 2, 3, 4, 5];
    let newArr1 = arr.slice(2);
    let newArr2 = arr.slice(2, 4);
    
    console.log(newArr1);//執行結果:[3, 4, 5]
    console.log(newArr2);//執行結果:[3, 4]
    ```
    帶入slice中的第一個參數代表要從哪個索引值開始複製，第二個代表結束的索引值，不代第二個預設會是複製到array結束，如果帶入負數會從最後一個元素開始往前推，比如說-3就是倒數第三個。這裡要注意，複製範圍是含頭不含尾，所以可以看到newArr2只複製到索引值3的元素。
* splice():
	* 這個函式跟slice只差了一個字，導致我常常記錯。與slice不同，splice是用來插入或刪除元素，比較像是push跟pop的用法。
    ```js
    let arr = [1, 2, 3];
    arr.splice(0, 1);
    console.log(arr);//執行結果:[2, 3];
    
    arr.splice(0, 0, 5);
    console.log(arr);//執行結果:[5, 2, 3];
    
    arr.splice(0, 1, 1);
    console.log(arr);//執行結果:[1, 2, 3];
    ```
    splice第一個參數代表開始的索引值，這裡跟slice一樣，第二個代表要移動幾步，比如說以執行結果1來說，我從索引值0移動了一步，移到了索引值1，接著用第三個參數的值取代掉移動到的前一個元素(一樣含頭不含尾的概念)，而結果1沒有第三個參數，所以執行出來後arr只剩下[2, 3]。雖然說可以做到刪除插入元素的結果，但我個人感覺整體邏輯是取代就是，拿執行結果2來說，不移動所以沒東西可以取代，就直接插入5這樣。最後，跟slice一樣，參數可以代負數，負數就代表從最後面開始算。
    
* sort():
	* 這個從名字就可以看出來是排序用的。
    ```js
    let arr = [1, 5, 6, 8, 4, 3];
    arr.sort();
    console.log(arr);//執行結果:[1, 3, 4, 5, 6, 8]
    ```
    直接使用的話是由小排到大，如果是字串就按照ascii code來排，比較特別的是sort可以寫compare function來自訂排序方式。
    ```js    
    let arr = [2, 5, 1, 0];
    arr.sort(compare(b, a) {
      if ( a < b) {
        return -1;
      }
      if ( a > b) {
        return 1;
      }
      // a 必須等於 b
      return 0;
  	});
    
    console.log(arr); //執行結果:[5, 2, 1, 0]

    ```
    a, b代表了陣列中的元素，他會依序去比較你帶入的參數，小於回傳-1，大於回傳+1，等於回傳0。像這裡我就把它改成由大排到小。
    
本次陣列函式介紹就差不多到這邊，雖然沒有列出所有的函式，但我認為我列出的已經是相對常用的了，希望大家會喜歡。