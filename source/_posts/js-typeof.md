title: 'Javascript: typeof、void'
author: int
tags:
  - javascript
categories:
  - js-operator
date: 2022-06-20 12:19:00
---
這篇也繼續把剩下的運算子補齊。

## typeof

typeof有兩種寫法:

```js
typeof 運算元

typeof(運算元)
```

這兩種意思都一樣，使用typeof回傳運算元的資料型態，非常方便，所以這個運算子也是相當常見。

## void

void也有兩種寫法:

```
void 運算式

void(運算式)
```

void會解析運算式然後回傳undefined，白話一點就是不回傳任何東西但可以執行後面的運算式。可以被使用在a連結中:
```html
<a href="javascript:void(0)">點擊這裡，甚麼都不會發生</a>
```
當使用者點擊連結時， void(0)會被解析為undefined， 而甚麼都不會發生。這個算是比較少見，但偶爾會看到有人使用來增加程式的可讀性。

寫了這麼多篇運算子也結束了，這篇就是運算子介紹完結篇，下次會出一篇總整理方便大家找。