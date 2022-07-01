title: 'Javascript: 讀取JSON'
author: int
tags:
  - json
  - javascript
categories: []
date: 2022-06-25 11:12:00
---
在[這篇](https://huanginch.github.io/2022/06/24/JSON%E6%A0%BC%E5%BC%8F/)有介紹過json格式，這篇會來介紹如何用js讀取json。

假設我們有一個json檔:
```json
[{
  "id": 1,
  "first_name": "Frannie",
  "last_name": "Sandeland",
  "email": "fsandeland0@sogou.com",
  "gender": "Female",
  "ip_address": "227.100.11.35"
}, {
  "id": 2,
  "first_name": "Batsheva",
  "last_name": "Biswell",
  "email": "bbiswell1@miitbeian.gov.cn",
  "gender": "Female",
  "ip_address": "214.81.196.38"
}, {
  "id": 3,
  "first_name": "Priscilla",
  "last_name": "Mapletoft",
  "email": "pmapletoft2@reference.com",
  "gender": "Genderfluid",
  "ip_address": "37.45.100.248"
}]
```

假設我想要讀取第二筆的email，那這邊就要先觀察這個格式最外層，上一篇也說過通常最外層是陣列，這裡也是，那我就要寫成:
```js
let data = `這裡貼上剛剛的data`;

let target = data[1];
```

這邊就會得到第二筆資料全部內容，可是我要怎麼單獨取出email欄位? 很簡單，因為這層是物件，用物件取值的方法就行了，寫法有兩種:

```js
let target = data[1].email;

let target = data[1]['email'];
```

這樣就可以拿到第二筆資料的email了，把上面的code整理一下:
```js
let data = `這裡貼上剛剛的data`;

let target = data[1].email //或是 data[1]['email'];

console.log(target); //執行結果: bbiswell1@miitbeian.gov.cn
```

是不是很簡單? 這篇裡有提到物件的讀取方法，但我還沒有寫文章介紹過，下次會整理一篇物件相關的文章，謝謝觀看。