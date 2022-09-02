title: 'CSS: BEM'
author: int
tags:
  - css
  - bem
categories: []
date: 2022-09-02 13:02:00
---
BEM命名法(Block-Element-Modifier)是一種CSS class的命名方式，和OOCSS以及SMACSS相同，都是為了讓css更結構化、更具可讀性。

## Block、Element、Modifier

* Block指的是區塊，一般來說我們都會把網頁切分成很多區塊，並以語意化的方式幫他命名，ex: menu、navbar等等。

* Element指的是區塊內的元素，比如說navbar裡的item。

* Modifier指的是修飾符，用來表示元素的狀態，比如active、disabled等等。

## 命名方式

BEM的寫法是使用兩個下底線或破折號連接
```
Block__Element
Block__Element--Modifier
```

ex: 

```css
navbar
navbar__item
navbar__item--active
```

## 在SCSS中使用

之前介紹[scss](https://huanginch.github.io/2022/08/29/SCSS/)時有介紹到scss可以用&來做連接，所以BEM命名法就可以完美的套用到scss結構中

```scss
navbar {
	....
    &__item {
    	....
        &--active {
        	...
        }
    }
}
```

## 結語

BEM綜合了OOCSS清晰架構，也不會像SMACSS那樣會非語意化的class，算是三者中我最喜歡的一種命名方式，不過並不會每個元素都使用BEM，依照需求調整才是最好的做法。


