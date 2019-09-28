# 豆瓣静态项目

## 设置页面标签前端的图标
```html
<link rel="shortcut icon" href="../img/favicon.ico">
```
出错：icon 写成 ico
    

## iconfont 内容中图标的引用
先使用 @font-face 定义字体 i ，i拥有一个类名iconfont
对.iconfont 设置一些样式
到网站选取需要的iconfont，复制类名，在线链接地址写link

## 设置透明度
opacity 整个区域，包含子元素
rgba( , , , ) 子元素不受父元素透明度影响

## 给奇偶子元素设置不同样式

 :nth-child(){}
 前面跟的是需要选择的元素，而不是父元素
 奇 odd
 偶 even （写成了oven）

## 列表项水平排列
 使用float， 或者把li的 display 属性值改为inline-block

## a标签颜色与预想不一致
网页上未访问过的a标签的颜色是visited的而不是link的
解决方法：a标签的href属性值写上 具体的 或 占位符#

## 移过元素变淡
涉及css：rgba()、opacity
1. 写一个div做蒙层，设置移过时显示。
2. 直接用元素的 before 或 after
 注意：
 ```css
    content: ""; 
    display: block;
 ```

## 导航

有子菜单的情况用ul li，没有的时候直接用nav元素

某父元素边框有圆角，子元素有背景，溢出时，
可给子元素设置相同的border-radius
也可以父元素over-flow：hidden

## 减轻后期js压力

写input，按钮等时，在外面套form元素


## 主体区两侧边，中间主区
 1. 两边分别左浮动和右浮动，中间设为BFC自适应（方法：overflow：hidden）
 2. 三者皆左浮

## ul li 一行两列

外防止有一个li内容过多，可以将li变为inline-block，text-align：justify ，ul after一个长度为百分百的


元素内部有图片，且当文字多时，不希望形成文字环绕：
将存放文字的元素变成BFC(设置overflow:hidden即可)