## HTML的基本概念

HTML(HyperText Markup Language):超文本标记语言，负责描述文档**语义**的语言，与之相关的概念有：超文本、标记、元素、标签、属性等。

## 1、超文本

1. 文档包含了图片、视频、音频、动画等内容，它们超出了文本的限制。
2. 超链接

## 2、标记语言

1. 标记语言是一套标记标签，`<a>超链接</a>`,带尖括号的a标签就是标记，本质就是书名号`《红楼梦》`之类的符号。HTML就不是编程语言，而是描述性的标记语言。
2. 标记语言直接由浏览器解析执行，没有编译过程。

注意：HTML是负责描述文档语义的语言。  
比如，`<h1>`标签什么用？

- 正确答案：给文本增加标题的语义。
- 错误答案：给文字加粗、变黑、变大。  

## 3、元素和标签

注意：元素就是标签，标签就是元素，

标签一般成对出现，但是也存在自结束标签。自结束标签的/可以省略。  

- `<head></head>,<img>或<img/>`

元素分为**块元素(block element)和行内元素(inline element)**。  

- 块元素独占一行，行内元素不会独占一行。  

html将所有标签分为两种：

- 文本级标签：p、span、a等，文本级标签只能放文字、图片、表单元素等,（a标签不能放a和input）。
- 容器级标签:div、h、li、dt、dd等，容器级标签可以放任何东西。

<img src="D:\user\Desktop\Script\note\material\html\标签分类.png">

## 4、属性

在标签中(开始标签中或者自结束标签)可以设置属性，属性是一个名值对(X="Y")，属性和标签名中间空格隔开，多个属性也用空格隔开。  
`<font color="red" size="3">文字</font>`  
属性按照文档的规定来写，属性名和属性值都要按规定写，有些属性可能没有属性值。

## 5、实体（转义字符）

实体的语法：`&实体的名字;`比较常用的有：

- 空格：`&nbsp;`
- 大于号：`&gt;`
- 小于号：`&lt;`
- 版权符号：`&copy;`