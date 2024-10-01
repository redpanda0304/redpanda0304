+++
author = "Hugo Authors"
title = "Markdown 语法指南"
date = "2019-03-11"
description = "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags = [
    "markdown",
    "css",
    "html",
    "themes",
]
categories = [
    "themes",
    "syntax",
]
series = ["Themes Guide"]
aliases = ["migrate-from-jekyl"]
image = "pawel-czerwinski-8uZPynIu-rQ-unsplash.jpg"
+++

这篇文章提供了一些基本的Markdown语法示例，可以用于编写Hugo内容文件，同时展示了在Hugo主题中如何使用CSS装饰HTML元素。
<!--more-->

## 标题

以下HTML中的`<h1>`至`<h6>`元素代表六个级别的章节标题。`<h1>`是最高级别的章节，而`<h6>`是最低级别的章节。
# H1 `# H1`
## H2 `## H2`
### H3 `### H3`
#### H4 `#### H4`
##### H5 `##### H5`
###### H6 `###### H6`


## 段落

在Markdown文档中，段落通常是通过空行来分隔的。即在不同的段落之间需要有一个空行，这样Markdown解析器才能正确地识别和显示不同的段落内容。

这是第二个段落。

## Blockquotes

`<blockquote>` 元素用于表示从另一个来源引用的内容，在引用内容中可以选择性地包含引文（citation），引文通常应该位于 `<footer>` 或 `<cite>` 元素内，并且可以包含内联更改，例如注释和缩略语。
The blockquote element represents content that is quoted from another source, optionally with a citation which must be within a `footer` or `cite` element, and optionally with in-line changes such as annotations and abbreviations.

具体解释如下：
* 表示引用内容：`<blockquote` 元素用于包裹引用的内容，表明这部分内容是引用自其他来源的。
* 引文（citation）：如果引用内容有引文（作者、来源等信息），这些引文通常应该包含在 `<footer>` 或 `<cite>` 元素中，以提供引文的来源信息。
* 内联更改：在引用内容中，可以包含内联更改，比如注释和缩略语，以便更好地解释或补充引用内容。

#### Blockquote without attribution  无来源的块引用

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **Note** that you can use *Markdown syntax* within a blockquote.

```
> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **Note** that you can use *Markdown syntax* within a blockquote.
```
#### Blockquote with attribution 有来源的块引用

> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

```
> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.
```

## Tables 表格

表格不是 Markdown 核心规范的一部分，但 Hugo 支持表格开箱即用。
Tables aren't part of the core Markdown spec, but Hugo supports supports them out-of-the-box.

   Name | Age
--------|------
    Bob | 27
  Alice | 23

```
   Name | Age
------- |------
    Bob | 27
  Alice | 23
```


#### Inline Markdown within tables 表格中使用Markdown嵌入元素

| Italics   | Bold     | Code   |
| --------  | -------- | ------ |
| *italics* | **bold** | `code` |

```
| Italics   | Bold     | Code   |
| --------  | -------- | ------ |
| *italics* | **bold** | `code` |
```

| A                                                        | B                                                                                                             | C                                                                                                                                    | D                                                 | E                                                          | F                                                                    |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|------------------------------------------------------------|----------------------------------------------------------------------|
| Lorem ipsum dolor sit amet, consectetur adipiscing elit. | Phasellus ultricies, sapien non euismod aliquam, dui ligula tincidunt odio, at accumsan nulla sapien eget ex. | Proin eleifend dictum ipsum, non euismod ipsum pulvinar et. Vivamus sollicitudin, quam in pulvinar aliquam, metus elit pretium purus | Proin sit amet velit nec enim imperdiet vehicula. | Ut bibendum vestibulum quam, eu egestas turpis gravida nec | Sed scelerisque nec turpis vel viverra. Vivamus vitae pretium sapien |

```
|A|B|C|D|E|F|
|-|-|-|-|-|-|
| Lorem ipsum dolor sit amet, consectetur adipiscing elit. | Phasellus ultricies, sapien non euismod aliquam, dui ligula tincidunt odio, at accumsan nulla sapien eget ex. | Proin eleifend dictum ipsum, non euismod ipsum pulvinar et. Vivamus sollicitudin, quam in pulvinar aliquam, metus elit pretium purus | Proin sit amet velit nec enim imperdiet vehicula. | Ut bibendum vestibulum quam, eu egestas turpis gravida nec | Sed scelerisque nec turpis vel viverra. Vivamus vitae pretium sapien |
```
## Code Blocks 代码块

#### Code block with backticks 带三个反引号的代码块

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
```

#### Code block indented with four spaces 缩进四个空格的代码块

    <!doctype html>
    <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>Example HTML5 Document</title>
    </head>
    <body>
      <p>Test</p>
    </body>
    </html>

#### Code block with Hugo's internal highlight shortcode 带有 Hugo 内部高亮短代码的代码块
{{< highlight html >}}
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
{{< /highlight >}}

#### Diff code block 有差异的代码块

```diff
[dependencies.bevy]
git = "https://github.com/bevyengine/bevy"
rev = "11f52b8c72fc3a568e8bb4a4cd1f3eb025ac2e13"
- features = ["dynamic"]
+ features = ["jpeg", "dynamic"]
```

## List Types 列属性

#### Ordered List 有序号列

1. First item
2. Second item
3. Third item

```
1. First item
2. Second item
3. Third item
```

#### Unordered List 无序号列

* List item
* Another item
* And another item

```
* List item
* Another item
* And another item
```

#### Nested list 嵌套列

* Fruit
  * Apple
  * Orange
  * Banana
* Dairy
  * Milk
  * Cheese

```
* Fruit
  * Apple
  * Orange
  * Banana
* Dairy
  * Milk
  * Cheese
```

## Other Elements — abbr, sub, sup, kbd, mark
`<abbr>` 缩写元素

<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

```
<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.
```

`<sub>`下标元素
H<sub>2</sub>O
```
H<sub>2</sub>O
```

`<sup>`上标元素
X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>
```
X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>
```

`<kbd>`键盘输入元素
Press <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Delete</kbd> to end the session.
```
Press <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Delete</kbd> to end the session.
```

`mark`元素
Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.
```
Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.
```

## Hyperlinked image 超链接图片

[![Google](https://www.google.com/images/branding/googlelogo/1x/googlelogo_light_color_272x92dp.png)](https://google.com)
```
[![Google](https://www.google.com/images/branding/googlelogo/1x/googlelogo_light_color_272x92dp.png)](https://google.com)
```