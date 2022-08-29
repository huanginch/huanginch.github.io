title: SCSS介紹
author: int
tags:
  - scss
categories: []
date: 2022-08-29 18:57:00
---
SCSS是用來更方便、更有結構性撰寫CSS的一種語言，撰寫後的SCSS會被編譯成CSS。
這篇會來介紹SCSS的特色以及與CSS的不同之處。

## 巢狀結構

scss可以使用巢狀結構，將子元素包在父元素的大括弧裡。

```scss
.box {
	width: 100%
	a {
    	color: #2D2D2D;
    }
}

```

編譯後的CSS檔案會長這樣

```css
.box {
	width: 100%
}

.box a {
	color: #2D2D2D;
}
```

如果名稱相同也可以用&來代替

```scss
.box {
	width: 100%
	a {
    	color: #2D2D2D;
        
        &:hover {
        	color: #1C1C1C;
        }
    }
    
    &-image { //if the class name is box-image
    	width: 50%
    }
}
```

## 變數

SCSS可以像js那樣設定變數，並帶入到選擇器中

```scss
$primary: #2D2D2D;
$secondary: #1C1C1C;

$font-size-lg: 48px;
$font-size-md: 24px;

.box {
	color: $primary;
    font-size: $font-size-lg;
}
```

## mixin

mixin有點類似函數，可以將常用的語法包裝成mixin，要使用時可以直接拿出來，不過要注意，使用時須搭配@include。

```scss
@mixin rounded-border() {
	border-radius: 24px;
    border: 1px solid black;
}

.box {
	width: 100%;
    @include rounded-border();
}
```

## 結語

以上就是scss的一些簡單介紹，其他我沒介紹到的語法因為我自己還沒用過也還沒學會，之後會再補上。