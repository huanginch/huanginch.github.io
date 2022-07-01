title: 'Javascript: 條件運算子(三元運算子)'
author: int
tags:
  - javascript
categories:
  - js-operator
date: 2022-06-16 13:58:00
---
上一篇有提到一元運算子以及二元運算子，這篇會來介紹三元運算子。
三元運算子，又稱作條件運算子，顧名思義就是針對三個運算元做運算。

## 語法

condition ? 值a : 值b;

```js
let a = 3;
let msg = a >= 0 ? "a is positive" : "a is negtive" ;
console.log(msg); //執行結果: "a is positive"
```

簡單來說問號前面是判斷式，根據你給的式子，成立的話會回傳值a，不成立就值b，所以才會又稱為條件運算子。


一開始看到這個的時候會覺得是什麼XD 可能是因為這個東西其實不常使用，多數時候我們還是會使用if-else，主要是閱讀上比較直觀，但偶爾會不想寫那麼長的程式碼就會用這個代替。