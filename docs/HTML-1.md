# HTML：文字

## 元素

元素是 HTML 的基本单位，用标签（tag）来表示。

例如一段文字（左边为代码，右边为显示效果，可编辑）：

[playground html init='<p>我是一段话</p>
<p>我是另一段话</p>']

`<p></p>` 是最常用标签之一，代表一个段落（paragraph），大部分标签都将内容[underline 包裹]了起来。

## 基本样式标签

[playground html init='<p>这是一个段落（paragraph）。</p>
<p>这是<i>斜体（italics）</i>。</p>
<p>这是<b>粗体（bold）</b>。</p>
<p>这是<u>下划线（underline）</u>。</p>']

另外还有 `<sup>`、`<sub>`、`<br>` [note `<br>` 可插入一个简单的换行符。<br />`<br>` 标签是空标签（意味着它没有结束标签，因此这是错误的：`<br></br>`）。<br />在 HTML 中，把结束标签放在开始标签中，也就是单独一个 `<br />`]、`<blockquote>`、`<del>` 等等。请自己试一试。

## 链接标签 `<a>`

[playground html init='<p>我是一个<a href="http://baidu.com">链接</a>。</p>']

其中 `href` 表示链接的地址，写在标签内部，称作标签的[underline 属性]。

## 标题标签 `<h1>` ……

[playground html init='<h1>一级标题</h1>
<h2>二级标题</h2>
...
<h6>六级标题</h6>']

`h` 表示 heading。

## 有序 / 无序列表（li，list）

有序列表（ol，ordered list）：

[playground html init='<ol>
	<li>复旦</li>
	<li>学生</li>
	<li>网</li>
</ol>']

无序列表（ul，unordered list）：

[playground html init='<ul>
	<li>复旦</li>
	<li>学生</li>
	<li>网</li>
</ul>']

## 元素嵌套

[playground html init='<ul>
	<li>复旦</li>
	<ol>
		<li><del>学渣</del>学生</li>
	</ol>
	<li>网</li>
</ul>']

### 练习

实现下图的 HTML 代码：

![exec.](docs/ex-1.png)