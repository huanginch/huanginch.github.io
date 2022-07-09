title: 'CSS: Position: fixed'
author: int
tags:
  - css
categories:
  - css position
date: 2022-07-09 11:09:00
---
很常會看到有些網頁的NavBar會跟著畫面滾動並停留在最上方，並不會因為畫面向下拉而消失，又或者是有些在最左下角的回頂端(如圖)

![蝦皮回頂端按鈕](../images/pasted-88.png)

想要實現這種功能就必須使用到 position: fixed

## 語法

```css
.box{
	position:fixed;
}
```
### 舉例
<iframe height="300" style="width: 100%;" scrolling="no" title="position: fixed" src="https://codepen.io/intHuang/embed/MWVyqmb?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/intHuang/pen/MWVyqmb">
  position: fixed</a> by int (<a href="https://codepen.io/intHuang">@intHuang</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

在上面的codepen中可以看到我在navbar中下了position:fixed;，所以當你滾動畫面時粉紅色navbar會一直固定在畫面上。

### top bottom left 和 right
但要注意，只寫position:fixed並不能將navbar固定在畫面最上方，你可以自己試試看，會發現他和上面有一些距離，所以這時候就要使用top。

透過top、bottom、left和right可以設定fixed元素的位置，以上面的codepen例子來說，top: 0;指的就是距離畫面頂端為0，所以會固定在畫面最上方，同理將其他值設成0就會與左邊右邊或底部沒有距離。

當然也可以設置成別的數值，px就是距離那個屬性的位置有幾個px，設定成%的話，假設是top:50%; 就會固定在由頂端往下50%的地方。

## 小結
fixed可以製作navbar等會固定在畫面上的元素，與fixed相似的還有sticky和relative，關於他們可以參考我的其他篇文章。