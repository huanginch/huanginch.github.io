title: 'CSS: OOCSS'
author: int
tags:
  - css
  - oocss
categories: []
date: 2022-08-31 16:58:00
---
物件導向CSS(Object-Oriented CSS，OOCSS)，是一種常見的css命名方式，目的是鼓勵開發者設計出的class能夠最大化的重複使用，讓程式碼更結構化、更易於管理與維護，未來在新增樣式上就不需要撰寫新的class。

## 兩大原則

* 樣式與結構分離: 元素的大小、樣式、顏色做分離，不要寫在同一個class。
	* 類似bs5中的btn、btn-primary之間的關係，元件的基礎樣式是一個class，其他可更改的，比如說大小、顏色等等會獨立出來成另一個class，如此一來程式碼會變得更加靈活。
    ```html
	<div class="box box-large box-primary"></div>
	<div class="box box-small box-secondary"></div>
	```
    * box的結構與樣式分離
    ```css
    .box {
    	width: 100px;
        height: 100px;
        border: 1px solid transparent;
    }
    
    .box-large {
    	width: 200px;
        height: 200px;
        border: 2px solid transparent;
    }
    
    .box-small {
    	width: 50px;
        height: 50px;
    }
    
    .box-primary {
    	background: #000;
        border-color: #fff;
    }
    
    .box-secondary {
    	background: #fff;
        border-color: #000;
    }
    ```
    
* 內容與容器分離: 少用標籤選擇器，盡量使用類別去撰寫。
	* 比如說我現在有一個p段落，想讓他的顏色和其他p段落不同，為他設置一個新的class，而不是直接用子代選擇器或者後代選擇器，如此一來如果以後有其他元素也想使用這個樣式就可以直接使用，在bs5或tailwind中utilities就是這個目標的體現。
    ```html
    <div class="section1">
    	<p class="highlight">Lorem ipsum dolor sit amet consectetur </p>
    </div>
    ```
    * 不要使用:
    ```css
    .section1 p {
    	color: gray;
        font-weight: bold;
    }
    ```
    
    * 推薦使用:
    ```css
    .highlight {
    	color: gray;
        font-weight: bold;
    }
    ```

## 總結
適當的使用可以減少class的重複率，使得程式碼更加乾淨，但因為命名方式不夠語意化，所以相當仰賴文件的撰寫，若是網站規模不大不使用oocss或許會是更好的選擇。除了OOCSS，還有SMACSS、BEM兩種命名方式，之後也會撰寫文章來介紹。
