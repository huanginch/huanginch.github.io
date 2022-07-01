title: 'Javascript: delete、逗號運算子、字串運算子'
author: int
tags:
  - javascript
categories:
  - js-operator
date: 2022-06-19 12:28:00
---
前面幾篇幾乎把所有的運算子都介紹過一遍了，這篇會介紹幾個寫起來篇幅比較少的運算子。

## 一元運算子: delete

之前在[算術運算子篇](https://huanginch.github.io/2022/06/15/js-arthimetic-operator/)中也有介紹其他的一元運算子，這篇會把最後的一元運算子介紹給大家。

delete可以刪除物件、物件屬性、陣列元素等等。刪除後物件會變成undefined
```
delete 物件名稱;

delete 物件名稱.屬性;

delete 物件名稱[index];

delete 屬性; //只有在with中才能使用
```

## 逗點運算子

常用於迴圈內，可以同時進行兩種條件式判斷

```
for(i = 0, j = 0; i < n, j <= n, i++, j++){
	.....
}
```

## 字串運算子

其實就是 '+'，只是他也可以用來連接字串
```
let str1 = 'this';
let str2 = 'is';

let str3 = str1 + str2;

console.log(str3);//執行結果: thisis
```



