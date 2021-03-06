

#  Web前端开发入门基础教程

[TOC]

## 1.	网页相关概念

### 1.1	什么是网页

网页是构成网站的基本元素，它通常有图片、链接、文字、声音、视频等元素组成。通常我们看到的网页，常见以`.htm`或`.html`后缀结尾的文件，因此将其俗称为`HTML文件`。

### 1.2	什么是HTML

HTML 是用来描述网页的一种语言。

- HTML 指的是超文本标记语言 (**H**yper **T**ext **M**arkup **L**anguage)

- HTML 不是一种编程语言，而是一种*标记语言* (markup language)

- 标记语言是一套*标记标签* (markup tag)

- HTML 使用*标记标签*来描述网页

**超文本的含义**
1.它可以加入图片、声音、动画、多媒体等内容（超越了文本限制）。
2.它还可以从一个文件跳转到另外一个文件，与世界各地主机的文件链接（超级链接文本）。



## 2.	常用浏览器

浏览器是网页显示运行的平台。

### 2.1	常用的浏览器

1. IE浏览器

IE浏览器是世界上使用最广泛的浏览器，它由微软公司开发，预装在windows操作系统中。所以我们装完windows系统之后就会有IE浏览器。目前，最新的IE浏览器版本是IE 11。

2. Safari浏览器

Safari浏览器由苹果公司开发，它也是使用的比较广泛的浏览器之一。Safari预装在苹果操作系统当中，从2003年首发测试以来到现在已经11个年头。是苹果系统的专属浏览器，当然现在其他的操作系统也能装Safari。

3. Firefox浏览器

火狐浏览器是一个开源的浏览器，由Mozilla资金会和开源开发者一起开发。由于是开源的，所以它集成了很多小插件，开源拓展很多功能。发布于2002年，它也是世界上使用率前五的浏览器。

4. Opera浏览器

opera浏览器是由挪威一家软件公司开发，该浏览器创始于1995，目前其最新版本是opera 20，他有着快速小巧的特点，还有绿色版的，属于轻灵的浏览器。

5. Chrome浏览器

Chrome浏览器由谷歌公司开发，测试版本在2008年发布。虽说是比较年轻的浏览器，但是却以良好的稳定、快速、安全性获得使用者的亲睐。

6. 其他浏览器

像360浏览器，猎豹浏览器，百度浏览器等大多基于IE内核开发的。所以这里不详细介绍。

### 2.2	浏览器内核

浏览器内核（渲染引擎）：负责读取网页内容、整理讯息、计算网页的显示方式并显示页面。

|    浏览器    |  内核   |                        备注                         |
| :----------: | :-----: | :-------------------------------------------------: |
|      IE      | Trident |       IE、猎豹安全、360极速浏览器、百度浏览器       |
|   FireFox    |  Gecko  |                   火狐浏览器内核                    |
|    Safari    | Webkit  |                   苹果浏览器内核                    |
| Chrome/Opera |  Blink  | Chrome/Opera浏览器内核。Blink实际上是Webkit的分支。 |

目前国内浏览器都会采用Webkit /Blink内核。



## 3.	Web标准

Web标准是由W3C组织和其他标准化组织制定的一系列标准的集合。W3C（万维网联盟）组织是国际最著名的标准化组织。

### 3.1	为什么需要Web标准

浏览器不同，它们显示页面或者排版就有些差异。

遵循Web标准除了可以让不同的开发人员写出的界面更标准、更统一外，还有以下优点：

1.让Web的发展前景更广阔。

2.内容能被更广泛的设备访问。

3.更容易被搜索引擎搜索。

4.降低网站流量费用。

5.使网页更容易维护。

6.提高页面浏览速度。

### 3.2	Web标准的组成

 主要包括结构(Structure)、表现(Presentation)和行为(Behavior)三个方面。

| 标准 |                             说明                             |
| :--: | :----------------------------------------------------------: |
| 结构 |  结构用于对**网页元素**进行整理和分类，现阶段主要学习HTML。  |
| 表现 | 表现用于设置网页元素的版式、颜色、大小等**外观样式**，主要指的是CSS。 |
| 行为 | 行为是指网页模型的定义以及**交互**的编写，现阶段主要学习的是JavaScript。 |

Web标准提出的最佳解决方案是：**结构、样式、行为相分离**。

简单理解：结构写在HTML文件中，样式写在CSS文件中，行为写在js文件中。

![image-20210122231624701](C:\Users\sheny\AppData\Roaming\Typora\typora-user-images\image-20210122231624701.png)



## 4.	HTML标签

### 4.1	基本语法概述

1. HTML标签是**由尖括号包围的关键词**，例如`<html>`
2. HTML标签通常是成对出现的，例如`<html>` 和`</html>`，我们称之为**双标签**。标签对中的第一个标签是开始标签，第二个标签是结束标签。
3. 有些特殊的标签必须是单个标签（极少情况），例如`<br/>`，我们称之为**单标签**。



### 4.2	标签关系

双标签关系可以分为两类：**包含关系**和**并列关系**。

**包含关系**：

```html
<head>
    <title>
        
    </title>
</head>
```

**并列关系**：

```html
<head></head>
<body></body>
```

## 5.	HTML基本结构标签

### 5.1	第一个HTML网页

每个网页都会有一个基本的结构标签（也称为骨架标签），页面内容䦹在这些基本标签上书写。

HTML页面也被称为HTML文档。

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <meta name="description"content="This is an awesome website">
        <title>This is my first website</title>
    </head>
    <body>
        <!--六种标题和正文段落-->
        <h1>Headline 1</h1>
        <h2>Headline 2</h2>
        <h3>Headline 3</h3>
        <h4>Headline 4</h4>
        <h5>Headline 5</h5>
        <h6>Headline 6</h6>
        <p>"Hello World!"</p>
        <hr/>
    </body>
</html>
```

### 5.2	基本标签速查

https://www.runoob.com/tags/html-reference.html

https://www.w3school.com.cn/html/html_quick.asp

## 6.	图像标签

### 6.1	图像标签

在HTML标签中，`<img>`标签用于定义HTML页面中的图像

```html
<img src="图像URL" />
```

单词image的缩写，意为图像。

**src**是`<img>`标签的**必须属性**，它用于指定**图像文件的路径和文件名**。

## 7.	文件路径

### 7.1	基本信息

文件路径描述了网站文件夹结构中某个文件的位置。

文件路径会在链接外部文件时被用到：

- 网页
- 图像
- 样式表
- JavaScript



### 7.2	相对路径

**相对路径**：以**引用文件所在位置**为参考基础，而建立出的目录路径。

简单来说就是文件相对于HTML页面的位置。

| 路径       | 格式                            | 描述                                         |
| :--------- | ------------------------------- | -------------------------------------------- |
| 相同文件夹 | <img src="picture.jpg">         | picture.jpg 位于与当前网页相同的文件夹       |
| 同一级路径 | <img src="images/picture.jpg">  | picture.jpg 位于当前文件夹的 images 文件夹中 |
| 下一级路径 | <img src="/images/picture.jpg"> | picture.jpg 当前站点根目录的 images 文件夹中 |
| 上一级路径 | <img src="../picture.jpg">      | picture.jpg 位于当前文件夹的上一级文件夹中   |

### 7.3	绝对路径

**绝对路径：**是指目录下的绝对位置，直接到达目标位置，通常是从盘符开始的路径。



## 8	链接标签

### 8.1	超链接标签（重点）

在HTML标签中`<a>`标签用于定义超链接，作用是从一个页面链接到另一个页面。

 ```HTML
<a href="跳转目标" target="目标窗口的弹出方式">文本或图像</a>
 ```
 **两个属性的作用：**

| 属性   | 作用                                                         |
| ------ | ------------------------------------------------------------ |
| href   | 用于指定链接目标的url地址，（必须属性）当为标签应用href属性时，它就具有了超链接的功能。 |
| target | 用于指定链接页面的打开方式，其中`_self`为默认值，`_blank`为在新窗口中打开方式 |

**链接分类：**

 **1.外部链接**

```html
<a href="http://www.qq.com" target="_blank">腾讯</a>
<!--target打开窗口的方式：_self在当前页面打开，_blank在新窗口打开-->
```

**2.内部链接：网页内部页面之间的相互链接**

```html
<a href="test.html" target="_blank">测试网页</a>
```

**3.空链接**

```html
<a href="#">公司地址</a>
```

**4.下载链接：地址链接的是 文件 .exe 或者是 zip 等压缩包形式**

```html
<a href="img.zip">Download</a>
```

**5.网页元素链接**

在网页中的各种网页元素，如文本、图像、表格、音频、视频等都可以添加超链接。

**6.锚点链接**

- 在链接文本的`href`属性中，设置属性值为**`#name`**的形式，如

```html
<a href="#two">第二季</a>
```

- 找到目标位置标签，里面添加一个id属性=刚才的名字，如

```html
<h3 id="two">
    第二季介绍
</h3>
```



## 9.	注释标签和特殊字符

### 9.1	注释

如果需要在html文档中添加一些便于阅读和理解但又不仅需要显示在界面中的注释文字，就要使用注释标签。

HTML中的注释：

```html
<!--     -->
```

快捷键：`Ctrl`+`/`

### 9.2	特殊字符

 

| 特殊字符 |      描述      | 字符的代码 |
| :------: | :------------: | :--------: |
|     &nbsp;     |     空格符     |  `&nbsp;`   |
| &lt; |     小于号     | `&lt;` |
|     &gt;     |     大于号     | `&gt;` |
|     &amp;     |      和号      | `&amp;` |
|     &yen;     |     人民币     | `&yen;` |
|     &copy;     |      版权      | `&copy;` |
|     &reg;     |    注册商标    | `&reg;` |
|     &deg;     |     摄氏度     | `&deg;` |
|     &plusmn;     |     正负号     | `&plusmn;` |
|     &times;     |      乘号      | `&times;` |
|    &divide;      |      除号      | `&divide;` |
|     x&sup2;     | 平方2（上标2） | `&sup2;` |
|    x&sup3;    | 立方3（上标3） | `&sup3;` |

## 10.	表格标签

### 10.1	表格

表格由 <table> 标签来定义。每个表格均有若干行（由 <tr> 标签定义），每行被分割为若干单元格（由 <td> 标签定义）。字母 td 指表格数据（table data），即数据单元格的内容。数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等。

```html
<table border="1">
<tr>
<td>row 1, cell 1</td>
<td>row 1, cell 2</td>
</tr>
<tr>
<td>row 2, cell 1</td>
<td>row 2, cell 2</td>
</tr>
</table>
```

在浏览器显示如下：

| row 1, cell 1 | row 1, cell 2 |
| ------------- | ------------- |
| row 2, cell 1 | row 2, cell 2 |

### 10.2	表格和边框属性

如果不定义边框属性，表格将不显示边框。有时这很有用，但是大多数时候，我们希望显示边框。

使用边框属性来显示一个带有边框的表格：

```html
<table border="1">
<tr>
<td>Row 1, cell 1</td>
<td>Row 1, cell 2</td>
</tr>
</table>
```

### 10.3	表格的表头

表格的表头使用 **`<th> `**标签进行定义。

大多数浏览器会把表头显示为粗体居中的文本：

```html
<table border="1">
<tr>
<th>Heading</th>
<th>Another Heading</th>
</tr>
<tr>
<td>row 1, cell 1</td>
<td>row 1, cell 2</td>
</tr>
<tr>
<td>row 2, cell 1<html/td>
<td>row 2, cell 2</td>
</tr>
</table>
```

在浏览器显示如下：

| Heading       | Another Heading |
| ------------- | --------------- |
| row 1, cell 1 | row 1, cell 2   |
| row 2, cell 1 | row 2, cell 2   |

### 10.4	表格中的空单元格

在一些浏览器中，没有内容的表格单元显示得不太好。如果某个单元格是空的（没有内容），浏览器可能无法显示出这个单元格的边框。

```html
<table border="1">
<tr>
<td>row 1, cell 1</td>
<td>row 1, cell 2</td>
</tr>
<tr>
<td></td>
<td>row 2, cell 2</td>
</tr>
</table>
```

浏览器可能会这样显示：

![表格中的空单元格](https://www.w3school.com.cn/i/table_td_empty.gif)

**注意：**这个空的单元格的边框没有被显示出来。为了避免这种情况，在空单元格中添加一个空格占位符，就可以将边框显示出来。

```php+HTML
<table border="1">
<tr>
<td>row 1, cell 1</td>
<td>row 1, cell 2</td>
</tr>
<tr>
<td>&nbsp;</td>
<td>row 2, cell 2</td>
</tr>
</table>
```

在浏览器中显示如下：

| row 1, cell 1 | row 1, cell 2 |
| ------------- | ------------- |
|               | row 2, cell 2 |