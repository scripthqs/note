# CSS选择器

css语法是选择器加上声明块

```css
选择器 { 
	属性名: 属性值; 
	属性名: 属性值; 
}
/*一个属性有多个值的话，那么多个值用空格隔开*/
/*css只有这一种注释*/
```

## 1、基本选择器

一般来说，类上样式，id上行为，css都使用class，js上使用id。所以类选择器比id选择器使用更多。

### 1.1、元素选择器

```css
p {
	font-size:16px;
    color: red;
}
```

### 1.2、类选择器

`.`开头

```css
.box {
	width: 200px;
	height: 200px;
}
```



### 1.3、ID选择器

`#`开头，id值不要重复，class可以重复。

```css
#app {
	width: 100px;
	heigth: 100px;
}
```

### 1.4、通用选择器

`*`，所有的元素

```css
* {
	margin: 0;
	padding 0;
}
```

## 2、复合选择器

### 2.1、交集选择器

选中同时符合多个条件的元素，选择器之间紧密连接，要写元素选择器时必须用元素选择器开头

```css
div.box1 {
	color: red;
}
div#box2 {
    color: green;
    /*这种写法语法上没问题，但是id选择器都是唯一的，没必要*/
}
.a.b.c {
    color: black;
    /*当一个元素同时有a,b,c的class时生效*/
}
```

### 2.2、并集选择器

同时选择多个选择器对应的元素，多个选择器之间用逗号隔开

```css
p,h1,.box1,#id {
    color: red;
}
```

## 3、关系选择器

### 3.1、后代选择器

多个选择器之间，使用空格隔开

```css
ul li{
	font-size: 16px;
}
div ul li {
    font-size: 16px;
}
```

### 3.2、子代选择器

子代选择器只能选儿子，和后代不同，但是可以多写一个`>`号

```css
ul > li {
	color: red;
}
div > span {
	font-size: 16px;
}
```

### 3.3、兄弟选择器

下一个兄弟选择器：兄+弟，兄弟必须紧挨着，只能选后面的兄弟元素

```css
p + span {
	font-size: 16px;
}
/*选中p后面相邻的第一个span*/
```

选择下面所有的兄弟选择器：`兄~弟`，只能选后面的兄弟元素

```
p ~ span {
	color: red;
}
/*选中的p后面所有的span*/
```

## 4、属性选择器

  - `元素[属性名]{}`选择含有这种属性的选择器，元素可以省略不写
  - `元素[属性名=属性值]{}`选择含有这种属性名和属性值的选择器，元素可以省略不写
  - `元素[属性名^=属性值]{}`选择这种属性值开头的选择器，元素可以省略不写
  - `元素[属性名$=属性值]{}`选择这种属性值结尾的选择器，元素可以省略不写
  - `元素[属性名*=属性值]{}`选择含有这种属性值的选择器，元素可以省略不写

## 5、伪类选择器

**伪类**：用于描述一个元素的特殊状态，比如第一个子元素，被点击的元素，鼠标移入的元素。伪类用冒号来表示。

### 5.1、超链接伪类

```css
a:link {
	/*超链接点击之前，只能a使用*/
}
a:visited {
	/*超链接被访问后，只能a使用*/
    /*由于隐私的原因，这个伪类只能改超链接的颜色*/
}
a:hover {
	/*鼠标悬停在标签时*/
}
a:active {
	/*鼠标点击标签，但是不松手时*/
}

/*下面这伪类a不能使用*/
:focus {
	/*某个标签获得焦点时的样式（比如某个输入框获得焦点）*/
}
```

超链接a，这四种状态必须按照固定的顺序，`a:link 、a:visited 、a:hover 、a:active`，否则失效，“爱恨准则”：love hate，先爱后恨。

### 5.2、结构伪类选择器

- `E:first-child` 匹配父元素的第一个子元素E。
- `E:last-child` 匹配父元素的最后一个子元素E。
- `E:nth-child(n)` 匹配父元素的第n个子元素E。n的范围是（0~∞）
- `E:nth-child(odd)` 匹配奇数，或者2n+1
- `E:nth-child(even)` 匹配偶数，或者2n
- `E:nth-last-child(n)` 匹配父元素的倒数第n个子元素E。
- `E:not(nth-of-type(n))` 除了第n个子元素。

nth-child排所有的子元素，nth-of-type根据指定的元素排列

### 5.3、伪元素选择器

**伪元素**：表示页面中一些特殊的并不真实存在的元素（特殊的位置）。

**一个冒号`:`叫伪类（特殊的状态），两个冒号`::`叫伪元素（特殊的位置）**

- `::before`：元素的开始
- `::after`：元素的最后
 - before 和 after 必须结合content属性使用，很重要

```
p::before {
	content: 'abc'
}
div::after {
	content； 'xyz'
}
/*通过这个加入的内容不能被选中*/
p::before{
	content: '『'
}
p::after{
	content: '』'
}
/*通过这个t*/
```

- `::first-letter`：表示第一个字母
- `::fitst-line`：表示第一行
- `p::selection`：表示选中的内容

