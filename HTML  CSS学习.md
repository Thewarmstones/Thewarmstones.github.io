

# 前端学习

**C/S架构**

**B/S架构**

*名词解释：*

*C => client（客户端）、*

*B => browser（浏览器）、*

*S => server（服务器）。*

## HTML

### 一、HTML前置知识

#### 简介

全称：**HyperText Markup Language**（**超文本标记语言**）。

超文本：*暂且简单理解为 “超级的文本”，和普通文本比，内容更丰富。* 

标 记：*文本要变成超文本，就需要用到各种标记符号。* 

语 言：*每一个标记的写法、读音、使用规则，组成了一个标记语言。*





#### HTML 标签

1. 标签 又称 元素，是HTML的基本组成单位。

2. 标签分为：双标签 与 单标签 （绝大多数都是双标签）。

3. 标签名不区分大小写，但推荐小写，因为小写更规范。





#### HTML基本结构

```html
<html>
    <head>
        <title></title>
    </head>
    <body>
        ......
    </body>
</html>
```







#### 编译器

**vscode**

*插件：*

*Live Server     自动刷新网页*

*vscode-icons  优化图标*





#### HTML注释

```html
<!-- 填充注释内容 -->
or
<!--
	ps:注释不可以嵌套
-->
```

快捷键：   **Ctrl + /**     

*将选中内容注释（即用<!-- -->包起来），可以通过再次使用该快捷键撤销指令*





#### HTML文档声明

```html
<!DOCTYPE html>
<!--HTML5的文档声明-->
```





#### HTML字符编码

编码  解码 （方式应相同）

```html
<head>
    <meta charset="UTF-8"/>
    <title></title>
</head>
```



HTML

<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <!-- ...... -->
</body>
</html>



#### 快捷键汇总

删除光标所在行：**Ctrl + Shift + K**

注释所选中内容：**Ctrl + /**

复制选中行内容：**Shift + Alt + 上移键/下移键**     （每行都向指定方向复制一行）

整体右移/左移选中的内容所在（多）行：**Tab / Shift + Tab**

光标同时落在多行：**Alt + 鼠标点击**      （可以通过上下左右键移动这些光标）



#### 网页图标

**favicon.ico**    （名字要对，后缀也要对）

与HTML放在同一个文件夹或者外层文件夹都可，可更改网页图标



### 二、HTML开发者文档

#### W3C官网

[World Wide Web Consortium (W3C)](https://www.w3.org/)

#### W3School 

www.w3school.com.cn

#### MDN

https://developer.mozilla.org/zh-CN/



### 三、本地转网络

[Image Upload - SM.MS - Simple Free Image Hosting](https://sm.ms/)





### 四、HTML基础

#### 1.排版标签

<img src="C:\Users\Without exceotion\AppData\Roaming\Typora\typora-user-images\image-20230419233025318.png" alt="image-20230419233025318" style="zoom:60%;" />

```html
<!--  -->
```



#### 2.块级/行内 元素

##### 块级元素

独占一行（排版标签都是块级元素）

（h1~h6 不能互相嵌套）

##### 行内元素

不独占一行；行内元素中只能写行内元素（p 中不要写块级元素）



#### 3.文本标签

通常都是行内元素

<img src="C:\Users\Without exceotion\AppData\Roaming\Typora\typora-user-images\image-20230420234609836.png" alt="image-20230420234609836" style="zoom:80%;" />

![image-20230420234716765](C:\Users\Without exceotion\AppData\Roaming\Typora\typora-user-images\image-20230420234716765.png)





#### 4.图片标签

独占一行

| 标签名 | 标签语义 | 常用属性                                                     | 标签类型 |
| ------ | -------- | ------------------------------------------------------------ | -------- |
| img    | 图片     | src ：图片路径（又称：图片地址）—— 图片的具体位置<br />alt ：图片描述<br />width ：图片宽度，单位是像素，例如： 200px 或 200<br />height ：图片高度， 单位是像素，例如： 200px 或200 | 单       |



#### 5.路径分析

##### 相对路径

<img src="C:\Users\Without exceotion\AppData\Roaming\Typora\typora-user-images\image-20230420235851796.png" alt="image-20230420235851796" style="zoom:67%;" />

##### 绝对路径

1.本地绝对路径

2.网络绝对路径  （*详见**本地转网络***）

##### 常见图片格式

jpg   png   bmp   gif   webp   base63



#### 6.超链接

| 标签名 | 标签语义 | 常用属性                                                     | 单 / 双 标签 |
| ------ | -------- | ------------------------------------------------------------ | ------------ |
| a      | 超链接   | **href** ： 指定要跳转到的具体目标。<br />**target** ： 控制跳转时如何打开页面，常用值如下:  **_self** ：在本窗口打开。  **_blank** ：在新窗口打开。<br />**id** ： 元素的唯一 标识，可用于设置锚点。<br />**name** ： 元素的名字，写在 a 标签中，也能设置锚点。 | 双           |

1. *代码中的多个空格、多个回车，都会被浏览器解析成一个空格！*

2. *虽然 **a** 是行内元素，但 **a** 元素可以包裹除它自身外的任何元素！*

##### 跳转到文件

```html
<!-- 浏览器能直接打开的文件 -->
<a href="./XXX.mp4">XXX</a>

<!-- 浏览器不能打开的文件，会自动触发下载 -->
<a href="./YYY.zip">YYY</a>

<!-- 强制触发下载 -->
<a href="./XXX.mp4" download="<-- 任意字符 空也行 -->">下载MP4</a>
```

##### 跳转到页面

```html
<!-- 跳转其他网页 -->
<a href="https://www.jd.com/" target="_blank">京东</a>

<!-- 跳转本地网页 -->
<a href="./10_HTML排版标签.html" target="_self">排版标签</a>
```

##### 跳转到锚点

###### 设置锚点

```html
<!-- 第一种方式：a标签配合name属性 -->
<!-- 具有 href 属性的a标签是超链接，具有 name 属性的a标签是锚点 -->
<a name="test1"></a>

<!-- 第二种方式：其他标签配合id属性 -->
<h2 id="test2">我是一个位置</h2>

<!-- name 和 id 都是区分大小写的，且 id 最好别是数字开头 -->
```

###### 跳转锚点

```html
<!-- 跳转到test1锚点-->
<a href="#test1">去test1锚点</a>

<!-- 跳到本页面顶部 -->
<a href="#">回到顶部</a>

<!-- 跳转到其他页面锚点 -->
<a href="other.html#test1">去other.html页面的test1锚点</a>

<!-- 刷新本页面 -->
<a href="">刷新本页面</a>

<!-- 执行一段js,如果还不知道执行什么，可以留空，javascript:; -->
<a href="javascript:alert(1);">点我弹窗</a>
```

##### 唤起制定应用



#### 7.列表

##### 有序列表

```html
<ol>
	<li></li>
	<li></li>
	<!-- ...... -->
</ol>
```

##### 无序列表

```html
<ul>
	<li></li>
	<li></li>
	<!-- ...... -->
</ul>
```

##### 自定义列表

```html
<dl>
	<dt></dt>    <!-- 术语名称 -->
	<dd></dd>    <!-- 术语描述 -->
	<!-- ...... -->
</dl>
```



#### 8.表格

 

| 标签名    | 标签语义   | 常用属性                                                     | 单/双标签 |
| --------- | ---------- | ------------------------------------------------------------ | --------- |
| **table** | 表格       | **width** ：设置表格宽度<br/>**height** ：设置表格最小高度，表格最终高度可能比设置的值大<br/>**border** ：设置表格边框宽度<br/>**cellspacing** ： 设置单元格之间的间距 | 双        |
| **thead** | 表格头部   | **height** ：设置表格头部高度。<br/>**align** ： 设置单元格的水平对齐方式，可选值如下：<br/>               ***left*** ：左对齐<br/>              ***cente***r ：中间对齐<br/>              ***right*** ：右对齐<br/>**valign** ：设置单元格的垂直对齐方式，可选值如下：<br/>              ***top*** ：顶部对齐<br/>              ***middle*** ：中间对齐<br/>              ***bottom*** ：底部对齐 | 双        |
| **tfoot** | 表格脚注   | 常用属性与 thead 相同。                                      | 双        |
| **tbody** | 表格主体   | 常用属性与 thead 相同。                                      | 双        |
| **tr**    | 行         | 常用属性与 thead 相同。                                      | 双        |
| **td**    | 普通单元格 | **width** ：设置单元格的宽度，同列所有单元格全都受影响。<br/>**heigth** ：设置单元格的高度，同行所有单元格全都受影响。<br/>**align** ：设置单元格的水平对齐方式。<br/>**valign** ：设置单元格的垂直对齐方式。<br/>**rowspan** ：指定要跨的行数。<br/>**colspan** ：指定要跨的列数。 | 双        |
| **th**    | 表头单元格 | 常用属性与 td 相同                                           | 双        |

```
1. <table> 元素的 border 属性可以控制表格边框，但 border 值的大小，并不控制单元格
边框的宽度，只能控制表格最外侧边框的宽度，这个问题如何解决？—— 后期靠 CSS 控制。
2. 默认情况下，每列的宽度，得看这一列单元格最长的那个文字。
3. 给某个 th 或 td 设置了宽度之后，他们所在的那一列的宽度就确定了。
4. 给某个 th 或 td 设置了高度之后，他们所在的那一行的高度就确定了。
```





#### 9.常用标签补充

| 标签名 | 标签含义                                   | 单/双标签 |
| ------ | ------------------------------------------ | --------- |
| br     | 换行                                       | 单        |
| hr     | 分隔（一条分隔线）                         | 单        |
| pre    | 按原文显示（一般用于在页面中嵌入大段代码） | 双        |

```
1.不要用 <br> 来增加文本之间的行间隔，应使用 <p> 元素，或后面即将学到的 CSS 的margin属性
2.<hr> 语义是分隔，只是画线装饰的话用 CSS 即可
```



#### 10.表单

| 标签名       | 标签语义           | 常用属性                                                     |
| ------------ | ------------------ | ------------------------------------------------------------ |
| **form**     | 表单               | **action** 属性： 表单要提交的地址。<br/>**target** 属性： 要跳转的新地址打开位置; 值: <br />**_self** ：在本窗口打开<br /> **_blank**：在新窗口打开<br/>**method** 属性： 请求方式，值： **get** 、 **post** |
| **input**    | 多种形式的表单控件 | **type** 属性： 指定表单控件的类型。 <br/>值： **text 、 password 、 radio （多个radio的name相同可实现单选效果）、 checkbox 、 hidden 、 submit 、 res、button 等**。<br/>**name** 属性： 指定数据名称<br/>**value** 属性：<br/>对于输入框：指定默认输入的值；<br/>对于单选和复选框：实际提交的数据； <br/>对于按钮：显示按钮文字。<br/>**disabled** 属性： 设置表单控件不可用。<br/>**maxlength** 属性： 用于输入框，设置最大可输入长度。<br/>**checked** 属性： 用于单选按钮和复选框，默认选中 |
| **textarea** | 文本域             | **name** 属性： 指定数据名称<br/>**rows** 属性： 指定默认显示的行数，影响文本域的高度。<br/>**cols** 属性： 指定默认显示的列数，影响文本域的宽度。<br/>**disabled** 属性： 设置表单控件不可用。 |
| **select**   | 下拉框             | **name** 属性： 指定数据名称<br/>**disabled** 属性： 设置整个下拉框不可用。 |
| **option**   | 下拉框的选项       | **disabled** 属性： 设置拉下选项不可用。<br/>**value** 属性： 该选项事件提交的数据（不指定**value**，会把标签中的内容作为提交数据）<br/>**selected** 属性： 默认选中。 |
| **button**   | 按钮               | **disabled** 属性： 设置按钮不可用。<br/>**type** 属性： 设置按钮的类型，值： **submit** （默认）、 **reset** （重置）、 **button**<br />***button不要指定name属性***。 |
| **label**    | 与表单控件做关联   | **for** 属性： 值与要关联的表单控件的ID值相同。<br />**label** 标签可与表单控件相关联，关联之后点击文字，与之对应的表单控件就会获取焦点。<br/>*两种与 **label** 关联方式如下：<br/>**1.** 让 label 标签的 for 属性的值等于表单控件的 id 。       **2.** 把表单控件套在 label 标签的里面。* |
| **fieldset** | 表单边框           | **fieldset** 可以为表单控件分组、 **legend** 标签是分组的标题。 |



#### 11.框架标签

**iframe**:框架（在网页中嵌入其它文件）

​		**name** ：框架名字，可以与 target 属性配合。
​		**width** ： 框架的宽。
​		**height** ： 框架的高度。 
​		**frameborder** ：是否显示边框，值:0或者1。

**例：**

```html
    <a href="https://www.toutiao.com" target="container">头条新闻</a>
    <a href="https://www.taobao.com" target="container">淘宝</a><br>
    <!-- 与表单的target属性配合使用 -->
    <form action="https://so.toutiao.com/search" target="container">
        <input type="text" name="keyword">
        <input type="submit" value="搜索">
    </form>

    <iframe name="container" frameborder="0" width="900" height="300"></iframe>
```



#### 12.HTML实体

<img src="C:\Users\Without exceotion\Pictures\Snipaste_2023-04-22_19-10-44.bmp" style="zoom:75%;" />

完整可参考[https://html.spec.whatwg.org/multipage/named-characters.html#named-character-references](https://sm.ms/)



#### 13.全局属性

<img src="C:\Users\Without exceotion\AppData\Roaming\Typora\typora-user-images\image-20230422191547226.png" alt="image-20230422191547226" style="zoom: 60%;" />

***ltr/rtl -> bdo   阅读顺序***

***ltr/rtl -> dir  文字靠左/右***

详见：https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes















## CSS

### 一、CSS基础

#### 简介

**CSS** 的全称为：**层叠样式表** ( Cascading Style Sheets ) 。
**CSS** 也是一种标记语言，用于给 HTML 结构设置样式，例如：文字大小、颜色、元素宽高等等。

简单理解： CSS 可以美化 HTML , 让 HTML 更漂亮。
核心思想： HTML 搭建结构， CSS 添加样式，实现了：***结构与样式的分离***



#### 编写位置

##### 行内样式

写在标签的**style**属性中

```html
<h1 style="color:red;font-size:60px;">欢迎来到尚硅谷学习</h1>
```

行内样式表：*只能控制当前标签的样式，对其他标签无效*



##### 内部样式

写在 **html** 页面内部，将所有的 CSS 代码提取出来，单独放在 <style>标签中

```html
<!-- 应放在head标签中 -->
<style>
    h1{
        ......
    }
<style>
```



##### 外部样式

写在单独的 **.css 文件**中，随后在 HTML 文件中**引入**使用。

例如 ： （直接写CSS代码即可）<img src="C:\Users\Without exceotion\AppData\Roaming\Typora\typora-user-images\image-20230423120042035.png" alt="image-20230423120042035" style="zoom:60%;" />

**语法：**

**1.新建一个扩展名为 .css 的样式文件，把所有 CSS 代码都放入此文件中**

```css
h1{ color:red ; ... }
h2{ font-size:40px ; ... }
```

**2.在 HTML 文件中引入 .css 文件**

```html
<link rel="stylesheet" href="./xxx.css">

<!--
1. <link> 标签要写在 <head> 标签中。
2. <link> 标签属性说明：
href ：引入的文档来自于哪里。
rel ：( relation ：关系）说明引入的文档与当前文档之间的关系。
-->
```



#### 语法规范

<img src="C:\Users\Without exceotion\AppData\Roaming\Typora\typora-user-images\image-20230423120819002.png" alt="image-20230423120819002" style="zoom: 25%;" />

**注释格式**

```css
/* 给h1元素添加样式 */
h1 {
	/* 设置文字颜色为红色 */
	color: red;
	/* 设置文字大小为40px */
	font-size: 40px;
    /* 添加背景 */
    background-color: gray;
    /* 宽度 */
    width: 180px;
}
```



### 二、CSS选择器

#### 1.基本选择器

##### 1.1通配选择器

**特点：**选中所有标签，一般用于清除样式

**用法：**  

```css
/* 选中所有元素 */
* {
    color:red
}
```



##### 1.2元素选择器

**特点：**选中所有同种标签，但是不能差异化选择（如 h1、p 等）

**用法：**

```css
/* 选中所有h1元素 */
h1 {
    color:red
}
```



##### 1.3类选择器

**特点：**选中所有特定类名（ class 值）的元素

**用法：**

```css
/* 选中所有class值为say的元素 */
.say {
    color:red
}
```

```html
<!-- 一个元素的class值可以有多个，用空格隔开即可，即：-->
<h1 class="age time mind">人</h1>
<!-- 通过.age , .time 或 .mind 都可以选中该h1 -->
```



##### 1.4id选择器

**特点：**选中特定 id 值的那个元素（唯一的）

**用法：**

```css
/* 选中id值为earthy的那个元素 */
#earthy{
    color:red
}
```

<img src="C:\Users\Without exceotion\AppData\Roaming\Typora\typora-user-images\image-20230423122409796.png" alt="image-20230423122409796" style="zoom:67%;" />





#### 2.复合选择器

##### 2.1交集选择器

**作用**：选中同时符合多个条件的元素

```css
/* 有标签名，标签名必须写在前面 */
p.beauty{
    /* 选择p标签并且(class)类名为beauty的内容 */
}
.beauty.man{
    /* 选择(class)类名包含beauty与man的内容 */
}
```



##### 2.2并集选择器

**作用**：选中多个选择器对应的元素，又称 分组选择器

```css
/* 并集选择器一般竖着写 */
/* 任何形式的选择器，都可以作为并集选择器的一部分 
/* 选中类名为rich，或类名为power，或类名为high，或类名为wide的元素 */
.rich,
.power,
.high,
.wide{
    ......
}
/* 选中id为peiqi，或类名为rich，或类名为beauty的元素 */
#peiqi,
.rich,
.beauty {
    font-size: 40px;
    background-color: skyblue;
    width: 200px;
}
```



##### 2.3后代选择器

**作用**：选中指定元素中，符合要求的后代元素

```css
/* 选中ul中的所有li */
ul li {
	color: red;
}
/* 选中ul中所有li中的a */
ul li a {
	color: orange;
}
/* 选中类名为subject元素中的所有li */
.subject li {
	color: blue;
}
/* 选中类名为subject元素中的所有类名为front-end的li */
.subject li.front-end {
	color: blue;
}
```



##### 2.4子代选择器

**作用**：选中指定元素中，符合要求的子元素（儿子元素）

```css
/* div中的子代a元素 */
div>a {
	color: red;
}
/* 类名为persons的元素中的子代a元素的子代b元素的子代c元素 */
.persons>a>b>c{
	color: red;
}
```



##### 2.5兄弟选择器

```css
/* 选中div后  紧紧相邻的  兄弟p元素 */
div+p {
	color:red;
}

/* 选中div后的所有的兄弟p元素 */
div~p {
	color:red;
}
```



##### 2.6属性选择器

**作用**：选中属性值符合一定要求的元素

```css
/*
1. [属性名] 选中具有某个属性的元素。
2. [属性名="值"] 选中包含某个属性，且属性值等于指定值的元素。
3. [属性名^="值"] 选中包含某个属性，且属性值以指定的值开头的元素。
4. [属性名$="值"] 选中包含某个属性，且属性值以指定的值结尾的元素。
5. [属性名*=“值”] 选择包含某个属性，属性值包含指定值的元素。
*/
/* 选中具有title属性的元素 */
div[title]{color:red;}
/* 选中title属性值为atguigu的元素 */
div[title="atguigu"]{color:red;}
/* 选中title属性值以a开头的元素 */
div[title^="a"]{color:red;}
/* 选中title属性值以u结尾的元素 */
div[title$="u"]{color:red;}
/* 选中title属性值包含g的元素 */
div[title*="g"]{color:red;}
```



##### 2.7伪类选择器

```css

```



##### 2.8伪元素选择器

```css

```



### 三、CSS三大特性

#### 1.层叠性



#### 2.继承性

元素会自动拥有其父元素、或其祖先元素上所设置的某些样式。

*优先继承离得近的*



#### 3.优先级

**!important > 行内样式 > ID选择器 > 类选择器 > 元素选择器 > * > 继承的样式**





### 四、CSS常用属性

#### 1.颜色表示

可以利用Snipaste截图工具获取 三元颜色值



##### 1.1  颜色名

参考文档：https://developer.mozilla.org/en-US/docs/Web/CSS/named-color



##### 1.2  rgb或rgba

**编写方式**：使用 红(r)、绿(g)、蓝(b) 这三种光的三原色进行组合。a表示透明度

```css
/* 使用 0~255 之间的数字表示一种颜色 */
color: rgb(255, 0, 0);/* 红色 */
color: rgb(0, 255, 0);/* 绿色 */
color: rgb(0, 0, 255);/* 蓝色 */
color: rgb(0, 0, 0);/* 黑色 */
color: rgb(255, 255, 255);/* 白色 */

/* 也可以使用百分比表示一种颜色（用的少） */
color: rgb(100%, 0%, 0%);/* 红色 */
color: rgba(100%, 0%, 0%,50%);/* 半透明的红色 */
```



##### 1.3  HEX或HEXA

HEX 的原理同与 rgb 一样，依然是通过：红、绿、蓝 进行组合，只不过要用 6位 (分成3组) 来表达，
**格式**：# rr gg bb                       ——16进制

```css
color: #ff0000;/* 红色 */
color: #00ff00;/* 绿色 */
color: #0000ff;/* 蓝色 */
color: #000000;/* 黑色 */
color: #ffffff;/* 白色 */
/* 如果每种颜色的两位都是相同的，就可以简写*/
color: #ff9988;/* 可简为：#f98 */
/* 但要注意前三位简写了，那么透明度就也要简写 */
color: #ff998866;/* 可简为：#f986 */
```



##### 1.4  HSL或HSLA

HSL 是通过：色相、饱和度、亮度，来表示一个颜色的

**格式**： hsl( 色相 , 饱和度 , 亮度 [, 透明度])  —— （ n deg , % , % [, % ]） ——  deg为度数单位



#### 2.字体属性

##### 2.1  字体大小

控制字体大小：font-size

```css
div {
	font-size: 40px;
}
```



##### 2.2  字体族

控制字体类型：font-family

```css
div {
	font-family: "STCaiyun","Microsoft YaHei",sans-serif
}
/* 1. 使用字体的英文名字兼容性会更好，具体的英文名可以自行查询，或在电脑的设置里去寻找。
   2. 如果字体名包含空格，必须使用引号包裹起来。
   3. 可以设置多个字体，按照从左到右的顺序逐个查找，找到就用，没有找到就使用后面的，且通常在最后写上serif （衬线字体）或sans-serif (非衬线字体)  */
```



##### 2.3  字体风格

控制字体是否为斜体：font-style

```css
/*  1. normal ：正常（默认值）
    2. italic ：斜体（使用字体自带的斜体效果）
    3. oblique ：斜体（强制倾斜产生的斜体效果）  */
```



##### 2.4  字体粗细

控制字体的粗细：font-weight

```css
div {font-weight: bold;}
div {font-weight: 600;}
/*
关键词
1. lighter ：细
2. normal ： 正常
3. bold ：粗
4. bolder ：很粗 （多数字体不支持）
数值：
1. 100~1000 且无单位，数值越大，字体越粗 （或一样粗，具体得看字体设计时的
精确程度）。
2. 100~300 等同于lighter ， 400~500 等同于normal ， 600 及以上等同于
bold 。
*/
```



##### 2.5  字体复合写法

将上述所有字体相关的属性复合在一起编写： font
**编写规则**：

1. *字体大小、字体族必须都写上。*
2. *字体族必须是最后一位、字体大小必须是倒数第二位。*
3. *各个属性间用空格隔开。*



#### 3.文本属性



### 五、CSS盒子模型









## JavaScript

### JS-引入方式

#### 内部脚本

```html
<!-- JavaScript代码必须位于<script></script>标签之间 -->
<!--
     HTML文档中可以在任意位置放置任意数量的<script></script>
     但一般放在<body>元素的底部
-->
<script>
	alert("Hello world")
</script>
```



#### 外部脚本

```html
<!-- 在html外部创建js文件，然后引入 -->
<script src="xxxxx.js"></script>
```







### JS-基础语法

```javascript
//注释
```

#### 1.输出语句

window.alert()        写入警告框

document.write()   写入HTML输出

console.log()           写入浏览器控制台



#### 2.变量

不能以数字开头  /  建议使用驼峰命名法  /  

**var**：全局有效，可以重复定义（同名）

**let**：代码块内有效，不能重复定义

**const**：定义后变为常量，不能改变值



#### 3.数据类型

**number**:数字（整数、小数、NaN（Not a Number））

**null **:对象为空

**undefined**:当声明的变量未初始化时，该变量默认值是undefined

**类型转换**：

```javascript
//pareInt  string转换为number
alert(pareInt("12345"))//12345
alert(pareInt("123A4"))//123
alert(pareInt("A45"))  //NaN

//其它类型转boolean
if(0)
if(NaN)
if("")
if(Null)
if(undefined)
/*上述均转换为false  
  其余情况均转换为true*/
```



#### 4.运算符

基本和 Java 相同

特别的：**==**      ：会进行类型转换             

​				**===**   ：不会进行类型转换

```javascript
var a1=10;
var a2="10";
var a3=10;
alert(a1==a2) //true  进行了进行类型转换
alert(a1===a2)//false 未进行类型转换
alert(a1==a3) //ture
alert(a1===a3)//true
```



#### 5.流程控制

语法和 Java 一致。详见官网。















































