title: 'Javascript: 運算子總整理'
author: int
tags:
  - javascript
categories:
  - js-operator
date: 2022-06-21 10:48:00
---
因為之前發的運算子文章都是分開發的，雖然有資料夾整理好，不過我覺得要調整一下順序跟增加優先級表格。


## 文章整理

* 順序大致會比照MDN的順序


1. [賦值運算子](https://huanginch.github.io/2022/06/05/js-assignment-operator/)

2. [比較運算子](https://huanginch.github.io/2022/06/14/js-compare-operator/)

3. [算數運算子](https://huanginch.github.io/2022/06/15/js-arthimetic-operator/)

4. [位元運算子](https://huanginch.github.io/2022/06/13/js-bit-operator/)

5. [邏輯運算子](https://huanginch.github.io/2022/06/04/Javascript-logic-operator/)

6. [三元運算子](https://huanginch.github.io/2022/06/16/js-conditional-operator/)

7. [關係運算子](https://huanginch.github.io/2022/06/17/js-relation-operator/)

8. 其他:
	1. [delete、逗號運算子、字串運算子](https://huanginch.github.io/2022/06/19/js-operator/)
    2. [typeof、void](https://huanginch.github.io/2022/06/20/js-typeof/)
    
## 運算子優先級

|運算子類型|屬於該類別的運算子|
|  ----  | ---- |
| 成員  | ```. []``` |
| 呼叫/建立 實例  | ```() new``` |
|反向/增加| ```! ~ - + ++ -- typeof void delete``` |
|乘法/除法| ```* / %``` |
|加法/減法| ```+ -``` |
|位元移動| ```<< >> >>>``` |
|關係運算子| ```< <= > >= in instanceof``` |
|相等性| ```== != === !==``` |
|位元 and| ```&``` |
|位元 xor| ```^``` |
|位元 or| ```\|``` |
|邏輯 and| ```&&``` |
|邏輯 or| ```\|\|``` |
|條件運算子| ```? :``` |
|指定運算子| ```= += -= *= /= %= <<= >>= >>>= &= ^= \|=``` |
|逗點運算子|```,```|