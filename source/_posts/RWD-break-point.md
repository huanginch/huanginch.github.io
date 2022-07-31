title: RWD 與常用斷點
author: int
tags:
  - css
  - RWD
categories: []
date: 2022-07-31 15:22:00
---
RWD (Responsive Web Design) 中文稱作響應式網頁，是為了因應不同裝置螢幕大小不同導致網頁必須適應各種螢幕尺寸而衍生出的技術。

## 語法

```css
@media (max-width: value) {
	...
}

@media (min-width: value) {
	...
}
```
通常我會使用max-width來開發，當螢幕寬度小於設定的值時會將樣式改變成括弧內的樣子。

max-width與min-width最大的區別在於max-width是以桌機使用者出發，min-width則是以手機使用者出發，一般來說會先學max-width比較容易上手。

## 常見斷點

所謂的斷點是當螢幕寬度達到某個數字時會改變樣式，那個數字就稱為斷點。一般網頁下的斷點為2~5個。

1. 1200px
2. 992px
3. 768px或767px[註]
4. 576px

以上是比較常用的斷點，1200為桌機，992為平板，768以下為手機，手機又視不同型號可以區分得更細，最小可以到320px。一般我在寫作業都是使用992與767兩個斷點，其他斷點的使用則是依專案需求來規劃。

[註]會有767px是因為平板的直式

## 其他斷點(手機螢幕尺寸)

* [傳送門](https://uiiiuiii.com/screen/)