title: JSON格式
author: int
tags:
  - json
  - javascript
categories: []
date: 2022-06-24 22:55:00
---
JSON是一種資料儲存的格式，全名為JavaScript Object Notation，但json格式不只可以在js中使用，其他語言也可以，其中在做網路請求時也很常使用json格式來傳遞資料。

## 格式
```json
[
 {
   "name": "Ming",
   "age": 18,
   "sex": "male"
 },
 {
  "name": "Amy',
  "age": 20,
  "sex", "female"
 }
]
```
其實跟js的物件格式很像，你可以用陣列包裹物件，或是用物件包裹陣列，不同的是key會包在雙引號裡面。比較常見的用法是如同範例程式中用陣列包裹。

json格式算是我最喜歡的資料格式，可能是因為我當初在學校學java第一個學怎麼處理的資料格式就是json。

下篇會來介紹如何用js讀取json的值。