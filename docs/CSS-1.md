# CSS 基础

## 关于 CSS
（HTML 定义了网页元素的逻辑结构）CSS 定义了网页中所有元素的样式，是网页中不可或缺的一部分。

## 初步使用 CSS

[playground html init='<p>复旦学生网</p>
<p style="color: red">复旦学生网</p>']

注意下面的 `p style="color: red"` 写法，表示：

__这个段落（p）的样式（style）为 `color: red`，也就是红色。__

「color: red」就是一条最简单的 CSS 规则。

## CSS 的语法

一套 CSS 样式由许多规则组成。每条规则基本上是「属性：值」的形式（例如 `color: red`），多条规则用「;」分隔开。

[playground html init='<p>复旦学生网</p>
<p style="color: white; background-color: red">复旦学生网</p>']

例如 `color: white; background-color: red` 就是「前景色：白色，背景色：红色」的一套样式。

## 常用语句

[playground html init='<p style="font-size: 25px">字号</p>
<p style="text-align: center">居中</p>
<p style="text-align: right">居右</p>']

除了 `color`、`background-color` 之外，常用的文字样式规则还有 `font-size`（表示字号，单位是 px，像素）、`text-align`（文字对齐）、`font-family`（字体）等等。

## 另一种写法

	<p style="color: red; font-size: 20px; text-align: center">一套 CSS 样式由许多规则组成。</p>

这一行代码太长了，读起来浑身难受。

我们需要把样式（CSS）和结构（HTML）分离开来。

## style 标签

[playground html init='<style>
p {
  color: red;
  font-size: 20px;
  text-align: center; 
}
</style>
<p>一套 CSS 样式由许多规则组成。</p>']

可以用 `<style>` 标签 __统一地__ 声明这个页面中的 CSS。

`p { ... }` 表示 __将花括号中的样式统一应用到 p 标签上__。

## 因此这样也都是可以的

`p { ... }` 会应用到 __所有__ p 标签上。

[playground html init='<style>
p {
  color: blue;
}
</style>
<p>段落 A</p>
<p>段落 B</p>']

样式之间会叠加和覆盖，例如：

[playground html init='<style>
p { color: blue; }
a { color: red; }
</style>
<p>蓝色段落 <a href="http://example.com">一个红色链接</a>。</p>']

## 一个问题

我希望两个段落颜色不同。

[playground html init='<style>
p { color: blue; }
p { color: red; }
</style>
<p>段落 A</p>
<p>段落 B</p>']

……it doesn't work

![](./docs/mood/11.png)

## 区分两个标签

[playground html init='<p id="p1">段落 A</p>
<p id="p2">段落 B</p>']

先给两个段落分别加上 __id__ 属性 `p1` 和 `p2`，用以区分它们。

[playground html init='<style>
p#p1 { color: blue; }
p#p2 { color: red; }
</style>
<p id="p1">段落 A</p>
<p id="p2">段落 B</p>']

`p#p1` 在 CSS 中表示「id 为 p1 的 p 标签」。

## 注意

不能有两个元素 id 相同，一个 id 唯一确定了一个元素。

因此 `p#p1` 在 CSS 中也可以干脆写成 `#p1`。

![](./docs/mood/50.png)

## 问题又来了

假设现在有 __五百个__ `<p>段落 A</p>`，__五百个__ `<p>段落 B</p>`。

要求段落 A 都是蓝色，段落 B 都是红色。如果只能用 id，那么解决方式是（1000 行各不相同的 HTML）：

	<p id="p1">段落 A</p>
	<p id="p2">段落 A</p>
	...
	<p id="p500">段落 A</p>
	<p id="p501">段落 B</p>
	<p id="p502">段落 B</p>
	...
	<p id="p1000">段落 B</p>
	
然后再写 1000 条 CSS 规则。

## 我们需要 class

`class` 划分了一类元素。

[playground html init='<style>
p.pr { color: red; }
</style>

<p class="pr">段落 A</p>
<p class="pr">段落 B</p>
<p>段落 C</p>']

`class` 属性在 CSS 中的标注是「.」，`id` 则是「#」。

`class` 和 `id` 最大的区别是，允许多个元素有同一个 `class` 值（从面向对象的角度就很容易理解 class 与 id 了）。

## 刚才的问题

	<p id="pb">段落 A</p>
	<p id="pb">段落 A</p>
	...
	<p id="pb">段落 A</p>
	<p id="pr">段落 B</p>
	...
	<p id="pr">段落 B</p>
	
加上

	p.pb { color: blue; }
	p.pr { color: red; }
	
没错，最大的变化是代码可以复制粘贴了，看起来也简洁明了。
