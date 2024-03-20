> ## **HTML** 超文本标记语言
>
> 定义网页内容的结构和含义,主要负责页面结构的搭建

## 1 HTML 简介

- 元素组成的标记语言
- 将文档结构逻辑化，组成页面结构
- 嵌入一些图片，影像等内容

## 2 HTML 具体内容

### 2.1 元素

- 开始标签
- 内容
- 结束标签
- 元素类型
  - 块级元素
  - 内联元素
  - 空元素（img）
- 属性
  - 布尔属性

### 2.2 HTML 文档

- `<html></html>` 根元素
- `<head></head>` 包含不在 html 页面中显示的内容
  - `<title></title>` 文档标题
  - `<meta>` 元数据，用于描述数据的数据，指定各种页面文档信息
    - `<meta charset="utf-8" />` 指定字符编码
    - `<meta name="" content=""/>` name 可使用 author、description 用于增强 `SEO`
  - `<link />`
    - `rel="stylesheet"` 引入样式表
    - `rel='icon'` 引用网页图标
  - `<script src defer></script>` 引用 js 内容
- `<body></body>` 包含访问页面时显示的内容

### 2.3 特殊字符

- `<` 等价 `&lt`;
- `>` 等价 `&gt`;
- `"` 等价 `&quot`;
- `'` 等价 `&apos`;
- `&` 等价 `&amp`;

### 2.4 全局属性

- `autofocus` 布尔类型属性，页面元素是否聚焦，在无障碍网站中慎用，可直接写在标签处 `<input type="text" autofocus />`
- `class` 元素的类名 可通过`class selectors`或`document.getElementsByClassName`获取相应元素
- `contenteditable` 表示元素是否可被用户编辑，是一个枚举属性
  - `true`
  - `false`
  - `plaintext-only`
- `data-*` 自定义数据属性，赋予我们在所有 HTML 元素上嵌入自定义数据属性的能力，并可以通过脚本在 HTML 与 DOM 表现之间进行专有数据的交换
- `dir` 一个指示元素中文本方向的枚举属性
  - `ltr`
  - `rtl`
  - `auto`
- `draggable` 枚举属性 标识元素是否允许使用浏览器原生行为或 HTML 拖放操作 API 拖动
  - `true`
  - `false`
- `hidden` 布尔属性 如果一个元素设置了这个属性，它就不会被显示，但是依然会渲染
- `id` 定义了一个全文档唯一的标识符
- `lang` 元素语言的定义
- `slot` 将一个 shadow DOM 树中的槽分配给一个元素
- `style` 包含应用到元素的 CSS 样式声明
- `tabindex` 指示元素是否可以聚焦，以及它是否/在何处参与顺序键盘导航
- `title` 使用`&#x000A;`可以让 title 换行
- `translate` 枚举属性，用来规定对应元素的可翻译属性值及其 Text 子节点内容是否跟随系统语言作出对应的翻译变化

### 2.5 常用属性

- `accept`
  - 用于`<input>`标签
  - 用于限制文件上传的类型
  - `accept=".jpg, .jpeg, .png"`
  - `accept=".doc"`
  - `accept="audio/*" ` 各种音频
  - `accept="video/*" ` 各种视频
  - `accept="image/*" ` 各种图片
- `autocomplete`
  - 用于`<input>` `<textarea>` `<select>` `<form>`
  - 属性允许 web 开发人员指定用户代理是否有权限在填写表单字段值时提供自动帮助，并指导浏览器填写该字段的预期信息类型
  - `on` 允许
  - `off` 不允许
- `crossorigin`
  - 用于`<audio>` `<img>` `<link>` `<script>` `<video>`
  - 它们提供对 CORS 的支持，定义该元素如何处理跨源请求，从而实现对该元素获取数据的 CORS 请求的配置
  - `anonymous` 请求使用了 CORS 标头，且证书标志被设置为 `same-origin`。没有通过 cookies、客户端 SSL 证书或 HTTP 认证交换用户凭据，除非目的地是同一来源
  - `use-credentials` 请求使用了 CORS 标头，且证书标志被设置为 `include`。总是包含用户凭据
- `disabled`
  - 用于`<button>` `<input>` `<select>` `<optgroup>` `<option>` `<textarea>` `<fieldset>`
  - 当布尔属性 disabled 存在时，元素将不可变、不能聚焦或与表单一同提交。用户将不能在表单控件本身或其子控件进行编辑或聚焦操作
- `for`
  - 用于 `<label>` `<output>`
  - 用于绑定标签的语义关系
- `max` `min` `maxlength` `minlength`
  - `<input>` `<textarea>`
  - 指定输入文本的长度或数值类型的边界值
- `multiple`
  - `<input>` `<select>`
  - 表明多选
- `pattern`
  - `<input>`
  - `input:valid` `input:invalid`伪类
  - 使用正则表达式赋值
- `placeholder`
  - `<textarea>`
  - `<input>`
- `readonly`
  - 布尔属性
  - 存在时不参与约束验证
- `required`
  - 布尔属性
  - 各种`<form>相关标签`
  - `:optional` 与 `:required`伪类
- `step`
  - `<input>`中各种有区间的类型`date` `time` `month` `range` `week` `number`

### 2.6 表单约束验证

- `表单验证`
  - `固有约束`
    - `type`类型的约束
  - `基本约束`
    - `pattern`
    - `min`
    - `max`
    - `required`
    - `minlength`
    - `maxlength`
    - `step`
- `约束验证API`
  - `HTMLFormElement.reportValidity()` `form`元素
  - `checkValidity()` 各种 form 类元素
  - `setCustomValidity(message)` 设置各元素校验信息
- `验证样式`各种相关的伪类
  - `:invalid`
  - `:valid`
  - `:optional`
  - `:required`
  - `:placeholder-shown`

### 2.7 常用标签

- `<a>` 锚元素
  - `href` 超链接所指向的 URL
    - `#链接到页面元素`
    - `mailto:email`
    - `tel:tellPhone`
    - **注意点** 经常被滥用为假按钮，href 设置为 # 或 javascript:void(0) 以防止页面刷新，然后监听其 click 事件，其实应该使用`<button>`
  - `download` 提供了下载文件名
  - `target`
- `<abbr>` 代表缩写的标签
  - `title`
  - 与`<dfn>`配合，更好的展示缩写元素内容
- `<address>` 表示地址的元素，字体为斜体
- `<area>` 在图片上定义一个热点区域，可以关联一个超链接，必须在 `<map>`内部使用（不一定非要是子元素）
  - `alt`
  - `href`
  - `shape`
  - `target`
  - `coords`
- `<article>` 表示文档、页面、应用或网站中的独立结构，可独立分配的或可复用的结构
- `<aside>` 表示一个和其余页面内容几乎无关的部分，通常表现为侧边栏或者标注框
- `<audio>` 音频元素
- `<b>` 用于吸引读者的注意到该元素的内容上，显示粗体
- `<blockquote>` 代表其中的文字是引用内容
- `<br>` 换行元素
- `<button>` 按钮
  - `form` 指向关联的 form 元素的 ID
  - `value` button 元素的值，会随着表单一起提交
  - `type`
    - `submit`
    - `reset`
    - `button`
- `<canvas>` 通过 JavaScript（Canvas API 或 WebGL API）绘制图形及图形动画
- `<caption>` 作为`<table>`元素的标题内容
- `<cite>` 文本的引用
- `<code>` 呈现一段计算机代码
- `<col>` 位于`<colgroup>`内，定义`<table>`中的列，并用于定义所有公共单元格上的公共语义
  - `span` 该属性值为一个正整数，表示该 <col> 元素横跨的列数。默认值为 1
- `<colgroup>` 表示表格列组，用来定义表中的一组列表
- `<data>` 将一个指定内容和机器可读的翻译联系在一起。但是，如果内容是与时间或者日期相关的，则一定要使用 `<time>`
  ```javascript
      <li><data value="398">迷你番茄酱</data></li>
      <style>
        li data:hover::after {
          content: ' (ID ' attr(value) ')';
          font-size: 0.7em;
        }
      </style>
  ```
- `<del>` 标签表示一些<del>被从文档中删除的文字内容</del>
- `<details>` 元素可创建一个组件，仅在被切换成展开状态时，它才会显示内含的信息。`<summary>` 元素可为该部件提供概要或者标签
  - `open` 布尔属性
  - `toggle` 事件
- `<dialog>` 元素表示一个对话框或其他交互式组件，例如一个可关闭警告、检查器或者窗口
  - `open` 布尔属性
  - `showModal() 或 show()` 方法，推荐使用该方法进行元素的展示
- `<dl>` `<dt>` `<dd>` 包含术语定义以及描述的列表，通常用于展示词汇表或者元数据 (键 - 值对列表)
- `<em>` 强调元素，斜体表示
- `<fieldset>` 元素用于对表单中的控制元素进行分组
  - `form` 设定为`<form>`的 id 属性，表明与这个 form 的关联
  - `disabled`
  - `<legend>` 配合，表示表单项的标题
- `<figure>` 元素代表一段独立的内容，可能包含 `<figcaption>` 元素定义的说明元素。该插图、标题和其中的内容通常作为一个独立的引用单元
- `<figcaption>` 作为 figure 元素的标题
- `<footer>` 结尾区域
- `<form>` 表示文档中的一个区域，此区域包含交互控件，用于向 Web 服务器提交信息。
  - `name`
  - `action` 处理表单提交的 URL
  - `method`
    - `get`
    - `post`
    - `dialog`
  - `novalidate` 布尔属性
  - `target`
- `<h1-h6>` 呈现了六个不同的级别的标题
- `<head>` 包含机器可读的文档相关信息
- `<header>` 头部区域
- `<hr>` 水平分割线
- `<i>` 用于表现因某些原因需要区分普通文本的一系列文本,斜体
- `<iframe>` 将另一个 HTML 页面嵌入到当前页面中
- `<img>` 展示图片
  - `usemap` 与 `<map>`元素进行关联
- `<kbd>` 键盘输入元素, 用于表示用户输入，它将产生一个行内元素
- `<label>` 表示用户界面中某个元素的说明
  - `for`
  - `form`
- `<li>` 无序列表
- `<main>` 应用的主体部分
- `<map>` 元素与 `<area>` 元素一起使用来定义一个图像映射（一个可点击的链接区域）
  - `name` 存在`id`时，两者必须一致, `<img>`的 usemap 需要关联当前`name`值
- `<mark>` 引用或符号目的而标记或突出显示的文本,高亮
- `<meter>` 显示已知范围的标量值或者分数值
  - `value`
  - `min`
  - `max`
  - `low`
  - `high`
- `<nav>` 导航区域
- `<ol>` 有序列表，通常渲染为一个带编号的列表
  - `type`
  - `start` 起始值
  - `reversed` 倒序
- `<optgroup>` 为`<select>`元素中的选项创建分组
  - `label` 分组名称
  - `disabled`
- `<option>` 用于定义在 `<select>`, `<optgroup>`元素中包含的项
  - `label` 分组名称
  - `disabled`
  - `value`
  - `selected` 布尔属性
- `<output>` 表示计算或用户操作的结果
  - `for` 影响结果计算的所有标签 ID
  - `form` 关联的表单
  - `name`
- `<p>` 段落
- `<picture>` 配合`<source>` 和 `<img>`标签显示图像内容
  - `<source>` 作为首选元素，浏览器显示最优匹配的值
  - `<img>` 作为备选元素，如果没有匹配的 source,就显示 src
- `<progress>` 显示一项任务的完成进度
  - `value`
  - `max`
- `<q>` 短文本的引用
  - `cite` 引用的链接
- `<ruby>` 用来展示东亚文字注音或字符注释
- `<rt>` 文字注音或者字符注释内容
- `<script>` 用于嵌入可执行代码或数据，这通常用作嵌入或者引用 JavaScript 代码
- `<section>` HTML 文档中一个通用独立章节，它没有更具体的语义元素来表示
- `<select>` 表示一个提供选项菜单的控件
  - `disabled` 布尔属性，用户是否能够交互
  - `multiple` 布尔属性，是否支持多选
  - `size` 多选时，表示为控件中同时可见的行数
  - `form` 所关联的 form 元素
- `<slot>` 作为 Web Component 技术套件的一部分，是 Web 组件内的一个占位符。该占位符可以在后期使用自己的标记语言填充，这样你就可以创建单独的 DOM 树，并将它与其他的组件组合在一起
  - `name` 具名的插槽
- `<small>` 样式表现为文本变小，定义为表示边注释和附属细则，包括版权和法律文本
- `<strong>` 文本非常重要，粗体显示
- `<sub>` 定义了一个文本区域，出于排版的原因，与主要的文本相比，应该展示得更低并且更小,可用做下标
- `<summary>` 指定了 `<details>`元素展开盒子的内容的摘要，标题或图例。点击 `<summary>`元素可以切换父元素 <details> 开启和关闭的状态
- `<sup>` 出于排版目的而显示为上标的行内文本
- `<template>` 内容模板（`<template>`）元素是一种用于保存客户端内容机制，该内容在加载页面时不会呈现，但随后可以在运行时使用 JavaScript 实例化。
  将模板视为一个可存储在文档中以便后续使用的内容片段。虽然解析器在加载页面时确实会处理 `<template>` 元素的内容，但这样做只是为了确保这些内容有效；但元素内容不会被渲染
- `<track>`
  - 当作`<audio>` 和 `<video>`的子元素使用，允许指定一种时序字幕
- `<var>` 元素表示数学表达式或编程上下文中的变量名称
- `<video>` 视频元素
  - `controls`
  - `controlslist`
    - 允许的值有 `nodownload`、`nofullscreen` 和 `noremoteplayback`
  - `loop` 布尔属性
  - `poster`
  - `preload`
    - `metadata`
    - `auto`
    - `none`

### 2.8 MathML

> 是一个用于描述数学公式、符号的一种 XML (en-US) 标记语言

- **`<math>`** 用于编写单个数学公式

### 2.9 案例

> code

<p>测试<code>ces</code></p>

```javascript
<p>
  测试<code>ces</code>
</p>
```

---

> ol

<ol>
  <li value="3">
    <data value="398">迷你番茄酱</data>
  </li>
  <li value="5">
    <data value="399">巨无霸番茄酱</data>
  </li>
  <li value="7">
    <data value="400">超级巨无霸番茄酱</data>
  </li>
</ol>

```javascript
<ol>
  <li value="3">
    <data value="398">迷你番茄酱</data>
  </li>
  <li value="5">
    <data value="399">巨无霸番茄酱</data>
  </li>
  <li value="7">
    <data value="400">超级巨无霸番茄酱</data>
  </li>
</ol>
```

---

> kbd

<kbd>ctrl</kbd>

```javascript
<kbd>ctrl</kbd>
```

---

> output

<form oninput="result.value=parseInt(a.value)+parseInt(b.value)">
  <input type="range" name="b" value="50" /> +
  <input type="number" name="a" value="10" /> =<output
    name="result"
    for="a,b"
  ></output>
</form>

```javascript
<form oninput="result.value=parseInt(a.value)+parseInt(b.value)">
  <input type="range" name="b" value="50" /> +
  <input type="number" name="a" value="10" /> =<output
    name="result"
    for="a,b"
  ></output>
</form>
```

> progress

<p>
  <label for="progress">70%</label>
<progress id="progress" value="70" max="100" title="70%"></progress>
</p>

```javascript
<progress id="progress" value="70" max="100" title="70%"></progress>
```

---

> ruby rt

<ruby>黄昏 <rt>huang hun</rt></ruby>

```javascript
<ruby>
  黄昏 <rt>huang hun</rt>
</ruby>
```

> sub sup

<span>H<sub>2</sub>O</span>
<span>2<sup>2</sup></span>

```javascript
<span>H<sub>2</sub>O</span>
<span>2<sup>2</sup></span>
```

---

## 3 TOC

[TOC]
