# Markdown 基本语法

[TOC]



## Markdown 标题语法

要创建标题，请在单词或短语前面添加井号 (`#`) 。`#` 的数量代表了标题的级别。例如，添加三个 `#` 表示创建一个三级标题 (`<h3>`) (例如：`### My Header`)。

### 三个#三级标题

还可以在文本下方添加任意数量的 == 号来标识一级标题，或者 -- 号来标识二级标题。

## 二级标题



##  Markdown 段落

要创建段落，请使用空白行将一行或多行文本进行分隔。

这是一个段落

直接按回车键进行分隔

**不要用空格（spaces）或制表符（ tabs）缩进段落**



## Markdown 换行语法

在一行的末尾添加两个或多个空格然后按回车键<br>即可创建一个换行(`<br>`)

为了兼容性，请在行尾添加**“结尾空格”**或 **HTML 的 `<br>` **标签来实现换行。



## Markdown 强调语法

### 粗体

要加粗文本，请在单词或短语的前后各添加**两个星号**（asterisks）或__下划线__（underscores）

为兼容考虑，在单词或短语中间部分加粗的话，请使用星号（asterisks）。

### 斜体（Italic）

要用斜体显示文本，请在单词或短语前后添加一个*星号*（asterisk）或_下划线_（underscore）。

为兼容考虑，在单词或短语中间部分加粗的话，请使用星号（asterisks）。

### 粗体（Bold）和斜体（Italic）

要同时用粗体和斜体突出显示文本，请在单词或短语的前后各添加三个星号或下划线。要加粗并用斜体显示单词或短语的中间部分，请在要突出显示的部分前后各添加三个星号，中间不要带空格。

为了实现兼容性，请使用***星号***将单词或短语的中间部分加粗并以斜体显示，以示重要。



## Markdown 引用语法

要创建块引用，请在段落前添加一个 `>` 符号。

> 创建块引用
>
> 块引用可以包含多个段落。为段落之间的空白行添加一个 `>` 符号。
> 
> >> 块引用可以嵌套。在要嵌套的段落前添加一个 `>>` 符号。


> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.


## Markdown 列表语法

可以将多个条目组织成有序或无序列表。

### 有序列表

请在每个列表项前添加数字并紧跟一个英文句点。数字不必按数学顺序排列，但是列表应当以数字 1 起始。

1. First item
2. Second item
   * 您可以将无序列表嵌套在有序列表中，反之亦然。
3. Third item
4. Fourth item

### 无序列表

请在每个列表项前面添加破折号 (-)、星号 (*) 或加号 (+) 。缩进一个或多个列表项可创建嵌套列表。

- 为了兼容性
* 不要在同一个列表中混合和匹配定界符

  > 在列表中嵌套其他元素 -- 缩进四个空格或一个制表符 -- Tab
+ 选择一个并坚持使用。

## Markdown 代码语法

要将单词或短语表示为代码，请将其包裹在反引号 (`` ` ``) 中。

### 转义反引号

如果你要表示为代码的单词或短语中包含一个或多个反引号，则可以通过将单词或短语包裹在双反引号(````)中。

``Use `code` in your Markdown file.``

## Markdown 分隔线语法

要创建分隔线，请在单独一行上使用三个或多个星号 (`***`)、破折号 (`---`) 或下划线 (`___`) ，并且不能包含其他内容。

为了兼容性，请在分隔线的前后均添加空白行。



---



## Markdown 链接语法

链接文本放在中括号内，链接地址放在后面的括号中，链接title可选。

超链接Markdown语法代码：`[超链接显示名](超链接地址 "超链接title")`

这是一个链接 [ Markdown语法 ](https://markdown.com.cn)

### 给链接增加 Title

链接title是当鼠标悬停在链接上时会出现的文字，这个title是可选的，它放在圆括号中链接地址后面，跟链接地址之间以空格分隔。

这是一个链接 [ Markdown语法 ](https://markdown.com.cn "最好的markdown教程")

### 网址和Email地址

使用尖括号可以很方便地把URL或者email地址变成可点击的链接。

<https://markdown.com.cn>

<y226039081@gmail.com>

### 带格式化的链接

在链接语法前后增加星号。 要将链接表示为代码，请在方括号中添加反引号。

这是一个链接 **[ Markdown语法 ](https://markdown.com.cn "最好的markdown教程")**

 

## Markdown 图片语法

要添加图像，请使用感叹号 (`!`), 然后在方括号增加替代文本，图片链接放在圆括号里，括号里的链接后可以增加一个可选的图片标题文本。

插入图片Markdown语法代码：`![图片alt](图片链接 "图片title")`。

![This is images](D:\images\backgroud\wallhaven-j3m8y5.png)

### 链接图片

给图片增加链接，请将图像的Markdown 括在方括号中，然后将链接添加在圆括号中。

`[![图片alt](图片链接 "图片title")](网址链接)`



## Markdown 转义字符语法

要显示原本用于格式化 Markdown 文档的字符，请在字符前面添加反斜杠字符 \ 。

\* 如果没有反斜杠，这将是无序列表中的一个项目符号。



## 插入代码

`` println() ``

``` java
public class Test{
  public static void main(String[] args){
    System.out.println(args);
  }
}
```



## 流程图

对于Flowchart，可以使用下面的code，然后语言选择flow

```flow
st=>start: java
op=>operation: JP
cond=>condition: English?
e=>end: xxxx

st->op->cond
cond(yes)->e
cond(no)->op
```



## 时序图 sequence

只需要敲入以下代码，然后选择语言为`sequence`即可生成下面的图

```sequence
周 -> 林: 不上班行不行啊  
林 --> 周: 不上班你养我啊？
周 -> 林: 嘿！     
林 --> 周: 又怎么了？
周 -> 林: 我养你啊！
林 --> 周: 你先养好自己吧，傻瓜。
```



## 表格

- 创建表格：在 Typora 中，您可以使用以下快捷键创建表格：Ctrl + T。
- 插入行：您可以在当前光标处插入新行，使用以下快捷键：Ctrl + Enter。
- 插入列：您可以在当前光标处插入新列，使用以下快捷键：Alt + Enter。
- 合并单元格：您可以合并多个单元格，使用以下快捷键：Alt + Shift + 鼠标左键点击。





