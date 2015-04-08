# HTML：逻辑

## 盒模型

盒模型是排版系统中最重要的概念之一，HTML 也采用了盒子模型。举个豆瓣的栗子，这是一个常见的网页：

![figure-1](docs/figure-html-2-1.png)

## 盒模型 2

其实这个页面的 **「代码结构」** 是下图这样的，红方框代表一个盒子。所有元素都是盒子，盒子一层层包裹在一起。

![figure-2](docs/figure-html-2-2.png)

## 解构

![figure-2](docs/figure-html-2-3.png)

以这块区域为例，在逻辑上很容易发现，「兴趣／人文社科／生活／个人成长／其他」这五个部分互为[underline **并列关系**]。

而「兴趣」列表下的「电影／音乐／读书／…」则[underline **属于**]「兴趣」之中。

## 简化

![figure-2](docs/figure-html-2-3.png)

上图在逻辑上，对应于这样的结构：

![figure-2](docs/figure-html-2-4.png)

## to HTML

![figure-2](docs/figure-html-2-4.png)

很明显就对应于下面的 HTML 代码：

[playground html init='<ul>
  <li>
    兴趣
    <ul>
        <li>电影</li>
        <li>...</li>
    </ul>
  </li>
  <li>
    人文社科
    <ul>
        <li>...</li>
    </ul>
  </li>
  <li>
    ...
  </li>
</ul>']

## 盒模型 3

所谓盒模型，就和 HTML 代码中标签的结构一样。该并列的元素并列，该嵌套的元素嵌套。

所有可显示的 HTML 标签都会产生一个盒子，而 div 和 span 常被用来当包装盒（>_<）。

**`<div></div>` 是最常用的盒子标签（division），它将内容包裹在一个盒子里。**

**`<span></span>` 也是常用的盒子标签。**

## `<div>`

`<div>` 本身是没有边框效果的，为了展示逻辑，给 `<div>` 加上红色边框。

[playground html init="<div>盒子一<div>盒子一里面的盒子</div></div>\n<div>盒子二</div>" css="span, div{border: 1px solid #E82424;padding:5px;margin:5px}"]

`<div>` 是一个 **块级元素**，这意味着它的内容自动地开始一个新行。

[playground html init="我是一句话我是一句话<div>我是一个盒子</div>我是一句话。" css="span, div{border: 1px solid #E82424;padding:5px}"]

## `<span>`

与 `<div>` 相比，`<span>` 是一个 **行内元素**，它不会产生换行。

[playground html init="<span>盒子一<span>盒子一里面的盒子</span></span>\n<span>盒子二</span>" css="span, div{border: 1px solid #E82424;padding:5px;margin:5px}"]
