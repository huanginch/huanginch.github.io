title: 'Ren''Py: screen types'
author: int
tags:
  - Ren'Py
categories: []
date: 2022-06-01 11:29:00
---
在Ren'Py中所有的畫面都是用screen來呈現，而screen又分為以下幾種:

1. window
	* 一個普通的視窗，給我的感覺有點像html裡的div，可以設定背景等等，可參考:[官方文件](https://www.renpy.org/doc/html/style_properties.html#window-style-properties)
2. frame
	* 跟window很像，最大的不同是背景樣式會套用gui資料夾裡的frame.png，所以你可以透過自訂frame.png以及gui.rpy中屬於frame的參數來修改他的樣式，同樣可參考[官方文件](https://www.renpy.org/doc/html/screens.html#frame)
3. vbox
	* 會給予一個透明背景的視窗，沒辦法自訂背景樣式，最大的特點是可以讓box內的元素垂直排列，[官方文件](https://www.renpy.org/doc/html/screens.html#vbox)
4. hbox
	* 和vbox基本上一模一樣，最大的不同是box內元素是水平排列，[官方文件](https://www.renpy.org/doc/html/screens.html#hbox)
5. imagemap
	* 完全用圖像來呈現，可以做出像地圖的感覺，[官方文件](https://www.renpy.org/doc/html/screens.html?highlight=imagemap#imagemap-statements) 
    
這篇文只是簡單列出screen可以用的種類，以後會在寫文針對每個的特性等等做更詳細的介紹。