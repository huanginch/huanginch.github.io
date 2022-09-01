title: 'CSS: SMACSS'
author: int
tags:
  - css
  - smacss
categories: []
date: 2022-09-01 12:44:00
---
SMACSS(Scalable and Modular Architecture for CSS)，使用結構分類，將CSS拆分成不同類別，在使用SCSS開發時也會用到SMACSS，將樣式拆分成多個檔案，主要會拆成以下五個類別:

* base: css基礎設定，包含h1~h2、html、body上等等的設定。
* layout: 網頁基礎架構，包含header及footer。
* module: 各種元件，例如button、form等等。
* state: 元件狀態，例如a:hover、button:focus。
* theme: 元件的顏色或大小。

命名方式會用-分隔，比如bs5中的btn-primary就是SMACSS的方式。

SMACSS雖然在排列組合上很方便，但結構分類是使用者自己劃分，界線較為模糊。
SMACSS與[OOCSS](https://huanginch.github.io/2022/08/31/CSS-OOCSS/)很相似，也有相同的優點，都能夠讓程式碼更加易於維護。