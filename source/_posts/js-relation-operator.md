title: 'Javascript: 關係運算子'
author: int
tags:
  - javascript
categories:
  - js-operator
date: 2022-06-17 11:31:00
---
可以比較兩者的關係(子集與宇集的概念)

## 語法

### in

```js
a in b
```

如果a在b裡面，回傳true，否則回傳false。

ex:
```js
let arr = ['a', 'b', 'c'];

console.log(a in arr);//執行結果: true
console.log('length' in arr);//執行結果: true
```

可以比較的不只是元素與陣列，還有函式與物件，屬性與物件都可以比較，所以'length' in arr才會回傳true，因為arr的屬性有length。


### instanceof

```js
物件名稱 instanceof 物件類型
```

跟in比較不一樣，instanceof只是用來比較這個物件是不是某個物件類型，是的話一樣回傳true。用英文來看就是這個object是不是這個class的instance，這裡如果對物件導向有了解應該就看得懂，不了解也沒關係，可以看看以下例子:

```js
var theDay = new Date(1995, 12, 17);
console.log(theDay instanceof Date);//執行結果: true
```

這樣應該就比較清楚了，關係運算式我自己比較少用到，但可能是我做的專案還不夠多不夠大，不過我自己覺得他用起來很方便，那這篇就差不多到這邊。