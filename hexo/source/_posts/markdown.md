---
title: Markdown指南
date: 2018-04-06 19:22:27
tags:
- Markdown
categories:
- 计算机
---

![i-love-markdown](markdown/i-love-markdown.png)

> Markdown 是一个 Web 上使用的文本到HTML的转换工具，可以通过简单、易读易写的文本格式生成结构化的HTML文档。目前 github、Stackoverflow 等网站均支持这种格式。

<!--more-->

# 写在最前

之前看到一篇用Markdown写学术论文的教程，才知晓Markdown也是博大精深，今天就先铺垫一下，日后准备学会用Markdown写学术论文的操作。

在下面的内容中，在编辑器中键入的内容都将采用`键入代码`的格式，而实际会在Markdown中看到的效果，会用引用的方式给出，就比如下面的：

> 实际效果

# 宗旨

> Markdown 的目标是实现「易读易写」。
>
> 可读性，无论如何，都是最重要的。一份使用 Markdown 格式撰写的文件应该可以直接以纯文本发布，并且看起来不会像是由许多标签或是格式指令所构成。Markdown 语法受到一些既有 text-to-HTML 格式的影响，包括 [Setext](http://docutils.sourceforge.net/mirror/setext.html)、[atx](http://www.aaronsw.com/2002/atx/)、[Textile](http://textism.com/tools/textile/)、[reStructuredText](http://docutils.sourceforge.net/rst.html)、[Grutatext](http://www.triptico.com/software/grutatxt.html) 和 [EtText](http://ettext.taint.org/doc/)，而最大灵感来源其实是纯文本电子邮件的格式。

# 基本语法

## 标题

在Markdown中设置标题有两种方法，分别是`#`和`===`，个人更加习惯使用第一种，因为可以支持从一级到六级的标题，后面那种只能支持两种（`===`是一级标题，`---`是二级标题，任何数量的`=`和`-`都没区别）

- `#一级标题`


- `######六级标题`

## 列表

列表是在Makdown中使用频率仅次于标题的部分了，就比如在上面的标题部分，对于一级标题和六级标题的示例，就采用了无序列表。

在Markdown中无序列表的使用有很多种`-`，`*`，`+` ，都可以实现无序列表

`- List1`

> - List1

`+ list2`

> - List2

`* List3`

> - List3

有序列表则使用`1.  ` 这样的形式进行输入（**点号后有空格**）。但是事实上有序列表前面的数字并不是取决于输入的数字，这就是说，你完全可以随意输入数字：

`1. List1`

> 1. List1

`3. List1`

> 1. List1

虽然有这样的特性，但是还是建议正常顺序输入。

## 任务列表

任务列表和列表的使用比较相似，需要在列表的`-` 后加入`[]`或者`[x]`，表示任务是否完成

`- [] 选项一`

> - [ ] 选项一

`- [x] 选项二`

> - [x] 选项二

## 引用

在之前的部分已经出现了相当多的引用的部分了，在Markdown的使用中，引用也是会经常用到的，引用的使用方式是输入`>` 

`>这里是引用`

> 这里是引用

引用中还可以继续引用，只需要键入`>>`

`>这是引用`

`>>这是引用里面的引用` 

> 这是引用
>
> > 这是引用里面的引用

## 加粗，斜体与删除

- 加粗：`**加粗**`

  > **加粗**

- 斜体：`*斜体*`

  > *斜体*

- 删除：`~~删除~~`

  > ~~删除~~

## 链接

`[RoseLand](https://rosecabbage.cc)`

> [RoseLand](https://rosecabbage.cc)

方括号中表示要在链接上显示的文字，圆括号中就是链接的地址

## 图片

图片的插入和链接比较相似

`![Mou icon](http://mouapp.com/Mou_128.png)`

> ![Mou icon](http://mouapp.com/Mou_128.png)

本地的图片是一样的原理，但是**不能改变**图片的路径，否则md文件就找不到图片了

## 代码块

在上面的部分也使用了多次代码块了，键入两个反引号，就可以在他们之间插入代码了

> `import numpy as np`

或者直接使用`Tab`即可

## 分割线

要在Markdown中使用分割线，方法很多：

`---`

`***`

`* * *`

> ------
>
> ------
>
> ------

## 目录

要插入目录，只需要键入`[TOC]`

# 进阶操作

## 表格

和$\LaTeX$非常相似的是，Markdown在表格上的表现也比较让人头疼，插入表格几乎变成了一件让人崩溃的事情，首先来看基本操作：

- 第一行是标题
  - `:---` 左对齐
  - `:--:`  居中
  - `---:` 右对齐

下面是示例

```markdown
| Title 1 | Title 2 | Title 3 |
|:--------|:-------:|--------:|
| Item 1  | Item 2  | Item 3  |
| Item 4  | Item 5  | Item 6  |
```

> | Title 1 | Title 2 | Title 3 |
> | :------ | :-----: | ------: |
> | Item 1  | Item 2  |  Item 3 |
> | Item 4  | Item 5  |  Item 6 |

**但是，Markdown似乎对合并单元格这样其实比较常用的操作无能为力**

这里推荐一个网站，可以在线生成HTML代码，方便插入——[Tables Generator](http://www.tablesgenerator.com/) 

## 内嵌CSS样式

`<p style="color: #AD5D0F;font-size: 30px; font-family: '宋体';">内嵌样式</p>`

> <p style="color: #AD5D0F;font-size: 30px; font-family: '宋体';">内嵌样式</p> 

## 脚注

可以实现参考文献的效果，使用的方法是加入`[1]`，在文章最后显示脚注

```markdown
Markdown 的目标是实现「易读易写」。[^1]
[^1]:[markdown.cn](http://markdown.cn/)
```

## 自动邮箱链接

`<1525568340@qq.com>`

> <1525568340@qq.com>

# 免费编辑器

- Windows 平台
  - [MarkdownPad](http://markdownpad.com/)
  - [typora](typora.io) 关于这个软件的介绍可以看[这篇](https://rosecabbage.cc/2018/04/03/typora-into/)，个人使用中
- Linux 平台
  - [ReText](https://pkgs.org/download/retext)
- Mac平台
  - [Mou](http://25.io/mou/)
- 其他编辑器
  - [Sublime Text 3](http://www.sublimetext.com/3)