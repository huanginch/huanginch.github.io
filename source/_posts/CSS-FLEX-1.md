title: 'CSS排版: FLEX(1)'
author: int
tags:
  - css
  - css-flex
categories:
  - css flex
date: 2022-05-24 13:42:00
---
## 前言
### 此文章為觀看[六角學院CSS Flex 超詳解，彈性版型任你操控！](https://youtu.be/88ymaHaStoQ)影片後整理之筆記

整理下來有點太多，可能會分成兩篇來記錄，想看下一篇可以到[這裡](https://huanginch.github.io/2022/05/25/CSS-Flex-2/)

## FLex介紹

Flex是一個CSS中很常使用的排版工具，他能夠自由操作div容器，主要概念為下圖

![](../images/pasted-8.png)

可以透過操作主軸與交錯軸來達成排版，預設主軸線為由左至右，交錯軸為由上至下

### 語法介紹
#### 外容器:
1. display: flex;(**需加在外容器上**)
2. flex-flow:
    * flex-direction-控制主軸方向:
        * row (預設值，由左至右)![](../images/pasted-18.png)
        * row-reverse(由右至左)![](../images/pasted-19.png)
        * column(由上至下)![](../images/pasted-45.png)
        * column-reverse(由下至上)![](../images/pasted-21.png)
    * flex-wrap-換行方式:
        * nowrap(不使用)![](../images/pasted-22.png)
        * wrap(遇到邊界自動換行)![](../images/pasted-23.png)
3. justify-content-對齊主軸線方式:
	* center(置中)![](../images/pasted-24.png)
    * flex-start(靠主軸起點)![](../images/pasted-25.png)
    * flex-end(靠主軸終點)![](../images/pasted-26.png)
    * space-between(中間留空格)![](../images/pasted-27.png)
    * space-around(元素左右都留空格，但比例為1:2:1)![](../images/pasted-28.png)
    * space-evenly(元素左右平均分配空格)![](../images/pasted-29.png)
4. align-items-與交錯軸對齊方式:
    * center(置中)![](../images/pasted-30.png)
    * flex-start(靠交錯軸起點)![](../images/pasted-31.png)
    * flex-end(靠交錯軸終點)![](../images/pasted-32.png)
    * strech(預設值，撐開至flexbox大小)![](../images/pasted-33.png)
    * baseline(對齊內容物基線)![](../images/pasted-34.png)
5. align-content-內容物對齊方式
	* center(每行對齊交錯軸線中間)![](../images/pasted-35.png)
    * flex-start(每行貼齊交錯軸線最前端)![](../images/pasted-36.png)
    * flex-end(每行貼齊交錯軸線最末端)![](../images/pasted-37.png)
    * space-between(第一行與最後一行分別對齊交錯軸線最前端與最末端)![](../images/pasted-38.png)
    * space-around(每行平均分配每行間距)![](../images/pasted-39.png)
    * strech(預設值，每行內容元素全部撐開至 flexbox 大小)![](../images/pasted-40.png)
    
#### 內容器:
1. flex:
	* flex-grow(子元素伸展比例分配)
    * flex-shrink(子元素壓縮比例分配)
    * flex-basis(子元素基本大小)
2. order: 老師這裡沒有特別介紹，以後學會再補上
3. align-self:
	* center(置中)![](../images/pasted-41.png)
    * flex-start(靠交錯軸起點)![](../images/pasted-42.png)
    * flex-end(靠交錯軸終點)![](../images/pasted-43.png)
    * strech(撐開至flexbox大小)![](../images/pasted-44.png)
4. margin-子元素邊界![](../images/pasted-46.png)
    
下一篇將會以程式碼做與實例做更進一步的講解。