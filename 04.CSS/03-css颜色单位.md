# css颜色单位

## 1、英文单词

在css中，可以直接使用颜色名来设置各种颜色。

- red，orange，yellow，blue，green，black

## 2、RGB值

### 2.1、RGB的写法

RGB通过三种颜色的不同浓度来调配出不同的颜色。

- R：red（红色）
- G：green（绿色）
- B：blue（蓝色）

每个颜色在0~255（0%-100%）之间

语法：

```css
background-color: rgb(0,0,0);/*黑色*/
background-color: rgb(255,255,255);/*白色*/
```

原理是光的三原色，000黑色，255表示白光

### 2.2、RGBA值

在RGB的基础上增加一个A不透明度，需要4个值

前三个一样，第四个值表示不透明度

- 1表示完全不透明
- 0表示完全透明
- 0.5表示半透明

```css
background-color: rgba(255,0,0,0.5)
```

### 2.3、十六进制

语法：#红色绿色蓝色，颜色浓度通过 00~ff表示

- #ff0000 红色

如果颜色两位两位的重复可以进行简写

```css
background-color: #000;/*黑色*/
background-color: #fff;/*白色*/
```

## 5、HSL值

### 5.1、HSL值

- H：色相（0 - 360）0或360表示红色、120表示绿色、240表示蓝色。
- S：饱和度，颜色浓度（0% - 100%）0表示灰色，值越大，越鲜艳。
- L：亮度，颜色的亮度（0% - 100%）0表示黑色

```css
background-color: hsl(0,100%,100%);/*红色*/
background-color: hsl(0,100%,0%);/*黑色*/
```

### 5.2、HSLA值

增加一个A不透明度

- 1表示完全不透明
- 0表示完全透明

```
background-color: hsla(240,50%,50%,0.4);
```

