title: 'Javascript: bit operator'
author: int
tags:
  - javascript
categories:
  - js-operator
date: 2022-06-13 13:25:00
---
我們在前幾篇有介紹到邏輯運算子，這篇會來介紹新手很容易與邏輯運算子搞錯的位元運算子，其實我之前也有介紹過C的位元運算子，不過javascript能用的指令比C多了一些，就讓我們來看一下吧。

* and: &
	* 兩個位元都為1就設為1
* or: |
	* 其中一個位元為1就設為1
* xor: ^
	* 兩個位元不同就設為1
* not: ~
	* 位元為0設為1，位元為1設為0
* zero fill left shift: <<
	* 全部位元往左移動，空著的地方補0
* signed right shift: >>
	* 全部位元往右移動，但最右邊的會被推到最左邊(循環的概念)
* zero fill right shift: >>>
	* 全部位元往右移動，空著的地方補0
    
與C最不同的是，js提供了signed right shift，讓我們不用自己寫(話說前幾天考試才剛考如何用C寫出signed right shift XD)，算是相當方便，不過其他的部分就大同小異，重要的還是要注意這是針對位元來做邏輯運算，而不是對整個資料。