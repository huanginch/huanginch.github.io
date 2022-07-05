title: 'CSS: !important'
author: int
tags:
  - css
categories: []
date: 2022-07-05 11:12:00
---
css中有一個特別的語法叫做 !important，他可以無視任何權重，任何規則都無法覆蓋加上!important的條件。

## 語法
在某個條件最後方加上!important即可。
```css
h2{
	color: white !important;
}
```

## 不推薦使用
但開發中並不推薦使用!important，因為他會讓你的程式碼無視權重，變得更難維護，你可能要在千萬行程式碼中找到!important才知道為什麼你新下的規則蓋不掉，當然在某些特定情況下還是可以用，比如說你不希望任何一條規則覆蓋掉某個特定條件，但最好還是乖乖用權重來算就好。