title: 'Javascript: if判斷式'
author: int
tags:
  - javascript
categories: []
date: 2022-06-06 11:11:00
---
在javascript中，可以透過if判斷式來進行條件判斷，比如說判斷一個人年紀是否超過18，超過18才能買菸買酒。

## 語法
```js
if(statement){
	/*your code...*/
}
```

以前面的例子來說就可以寫成:
```js
if(age >= 18){
	console.log('可以買菸買酒');
}
```

## else 判斷式
如果想對if以外的條件也做出處理，可以使用else

### 語法
```js
if(statement){
	/*your code..*/
}
else{
	/*your code...*/
}
```

當條件符合if中的判斷式時，會執行if大括弧中的code，不符合會跳過if大括弧，執行else大括弧中的code。

以前面的例子來說:
```js
if(age > 18){
	console.log('可以買菸買酒');
}
else{
	console.log('你未成年，不能買菸買酒');
}
```

## if-else 判斷式
如果想要同時判斷多個條件，可以用if-else

### 語法
```js
if(statement){
	/*your code...*/
}
else if(statement){
	/*your code...*/
}
else{
	/*your code...*/
}
```
我們用上面的例子，但這次多個條件判斷是否大於20歲來看看
```js
if(age > 20){
	console.log('民法成年')
}
else if(age > 18){
	console.log('刑法成年')
    
}
else{
	console.log('未成年')
}
```

* 注意! if-else可以有很多個，但if跟else只能有一個，if只能在最前，else只能在最後，if-else 和 else 可以沒有。


if判斷式算是非常基本但是卻非常常被使用到的語法，紀錄下來和大家分享。