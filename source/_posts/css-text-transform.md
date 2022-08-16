title: 'CSS: text-transform'
author: int
tags:
  - css
categories: []
date: 2022-08-16 20:06:00
---
text-transform可以改變文字的大小寫，基本上是針對英文字做使用。

## 屬性

### none
可以避免文字被套用text-transform。

```css
p {
	text-transform: none;
}
```

### uppercase

將文字全部轉換成大寫

```css
p {
	text-transform: uppercase;
}
```

### lowercase

將文字全部轉換成小寫

```css
p {
	text-transform: lowercase;
}
```

### capitalize

將文字字首轉成大寫

```css
p {
	text-transform: capitalize;
}
```

### full-width

將文字強迫塞滿整個格子，通常會作用在象形符號或是拉丁文，讓他們的對齊方式像中文或日文那樣

```css
p {
	text-transform: full-width;
}
```

### full-size-kana

通常用在[`<ruby>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ruby) tag上，他會將所有小寫kana字元轉成大的kana

## 結語

會用到這個是因為在寫六角第五週作業時某夜的文字在PC版和Pad版的字母大小寫有轉換，所以我就用上了text-transform來改變字母大小寫，至於他最後兩個屬性我還不太了解，kana似乎是用在類似日文的平假名或羅馬上標，有機會會再做介紹。