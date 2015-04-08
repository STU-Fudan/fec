# CSS基础

## 关于CSS
CSS定义了网页中所有元素的样式，是网页中不可或缺的一部分。

## 使用CSS

1. 引入式：通过`<link>`标签引入外部的CSS文件

	`<link rel="stylesheet" href="/css/example.css" />`

2. 嵌入式：在`<head>`标签中写入CSS

	<head>
		<!-- Other part in head-->
		<style type="text/css">/* css here */</style>
	</head>

3. 内联式：在HTML标签中直接定义`style`属性（不推荐）

	`<p style="color:#f00; line-height:150%;">This is not a good idea.</p>`

## CSS选择器

CSS选择器可以帮助浏览器将样式应用于部分特定的元素。我们将用以下这段代码来演示不同类型的选择器所起到的作用。

	<div class="box" id="article">
		<h1>New Photos <small>10:30</small></h1>
		<p class="first">Paragraph 1</p>
		<p class="second">Paragraph 2</p>
		<p class="thirs">Paragraph 3</p>
		<a href="#" class="btn back">Back</a>
		<a href="#" class="btn edit">Edit</a>
	</div>
	<p>Paragraph 4</p>
	<a href="#" class="btn top">Top</a>

## CSS选择器

#### 标签选择器 `tagname{}`
[playground css init='h1{
	color:#f00;
	font-size:24px;
	font-weight:bold;
}' html='<div class="box" id="article">	<h1>New Photos <small>10:30</small></h1><p class="first">Paragraph 1</p><p class="second">Paragraph 2</p><p class="thirs">Paragraph 3</p><a href="#" class="btn back">Back</a><a href="#" class="btn edit">Edit</a></div><p>Paragraph 4</p><a href="#" class="btn top">Top</a>']

## CSS选择器

#### Id选择器 `#ElementId{}`
[playground css init='#box{
	color:#f00;
	margin:0;
	padding:10px;
}' html='<div class="box" id="article">	<h1>New Photos <small>10:30</small></h1><p class="first">Paragraph 1</p><p class="second">Paragraph 2</p><p class="thirs">Paragraph 3</p><a href="#" class="btn back">Back</a><a href="#" class="btn edit">Edit</a></div><p>Paragraph 4</p><a href="#" class="btn top">Top</a>']

## CSS选择器

#### Class选择器 `.classname{}`
[playground css init='.btn{
	background-color:#f00;
	color:#fff;
	display:block;
	height:20px;
	width:120px;
}' html='<div class="box" id="article">	<h1>New Photos <small>10:30</small></h1><p class="first">Paragraph 1</p><p class="second">Paragraph 2</p><p class="thirs">Paragraph 3</p><a href="#" class="btn back">Back</a><a href="#" class="btn edit">Edit</a></div><p>Paragraph 4</p><a href="#" class="btn top">Top</a>']

## CSS选择器

#### 部分选择器
[playground css init='.btn:hover{
	background-color:#00f;
}' html='<div class="box" id="article">	<h1>New Photos <small>10:30</small></h1><p class="first">Paragraph 1</p><p class="second">Paragraph 2</p><p class="thirs">Paragraph 3</p><a href="#" class="btn back">Back</a><a href="#" class="btn edit">Edit</a></div><p>Paragraph 4</p><a href="#" class="btn top">Top</a>']

## CSS选择器
#### 组合使用
* 选择器可以组合使用
	* 选择器间以**逗号**分隔：用于统一定义不同选择器共有的样式
	* 选择器间以**空格**分隔：用于定义某一特定部分中选择器所选中的元素的样式
* **选择器内不能够嵌套选择器**

[playground css init='#article .btn{
	color:#00f;
}

.box .first{
	color:green;
}' html='<div class="box" id="article">	<h1>New Photos <small>10:30</small></h1><p class="first">Paragraph 1</p><p class="second">Paragraph 2</p><p class="thirs">Paragraph 3</p><a href="#" class="btn back">Back</a><a href="#" class="btn edit">Edit</a></div><p>Paragraph 4</p><a href="#" class="btn top">Top</a>']

## CSS选择器
#### 练习
解释以下选择器的意义

* `#footer ul li a {}`
* `.icon.green span {}`
* `p.first span.number {}`
* `#header li.first a:hover {}`
* `#result li:hover a.btn_del {}`

## 常见的CSS属性（部分）
* 版面：`position`、`float`、`text-align`、`z-index`
* 布局：`height`、`width`、`margin`、`padding`
* 背景：`background`、`border`
* 前景：`color`
* 段落：`text-indent`、`line-height`
* 字体：`font-family`、`font-size`、`font-weight`、`text-decoration`

练习：请自行查阅[W3School](http://www.w3school.com.cn/)以了解以上标签的含义与用法。
