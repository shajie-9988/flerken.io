### CSS

#### 含义

层叠样式表，是一种用于描述HTML或XML文档呈现方式的样式表语言。它可以控制网页的布局、字体、颜色等样式，从而提升网页的视觉效果和用户体验。

#### Class选择器

在`HTML`元素中设置`CSS`样式，需要在元素中设置 "`class`"选择器。

例如：`<div class='box'></div>`

`class`是标签上的一个属性，其值对应了一个样式表

``` 
.box{
	color:red
}
```

并且以**内部样式**的方式引用

#### CSS属性

#### 文本与字体

1. 字体颜色：color
2. 字体大小：font-size:，单位`px`
3. 行高：line-height,   字号 (font-size) + 行间距
4. 文本的对齐方式 ：text-align
   - 居中：center
   - 左对齐或右对齐：left&right
5. 文本的垂直对齐方式：vertical-align
6. 下划线 ：text-decoration:  underline;
7. 字体粗细：font-weight: bold  （加粗）

#### CSS盒子模型

所有HTML元素可以看作盒子；

对于任意一个元素，从左往右分别为：左外边距，左边框，左内边距，内容，右内边距，右边框，右外边距。

![CSS box-model](https://www.runoob.com/images/box-model.gif)

```
div {
    width: 300px;
    border: 25px solid green;
    padding: 25px;
    margin: 25px;
}
```

1. 内容宽度：width；内容高度：height，单位px

2. 边框：border：宽度 类型 颜色

3. 内边距：padding

4. 外边距：margin

5. 背景颜色：background-color

   - 颜色关键字

   - rgb()函数与rgba()函数
   - 十六进制表示法：#000000

#### 元素居中

水平居中，再让文本的行高与content的高度保持一致