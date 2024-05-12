+++
title = "Markdown Examples"
date = 2020-07-06
taxonomies.tags = ["markdown"]
+++

> This article is for checking site styling and will be translated later.

Markdown 是一门轻量级标记语言，用简洁的语法替代了手动排版，让我们更专注于写作。简而言之，我们通过一些符号告诉计算机「应当怎样排列一段文字」。

这篇文章简单介绍了常用的语法，并附带一些示例与参考链接。这些语法占用了一部分标点符号，若正文中需要用到它们，使用 [转义字符](#zhuan-yi-zi-fu)。

<!-- more -->

# 块级元素

标题、段落、表格等至少会占用一整行空间的元素，被叫做块。另一些可混排在文字中的叫做[内联元素](#nei-lian-yuan-su)。

块：[段落](#duan-luo)、[标题](#biao-ti)、[引用块](#yin-yong-kuai)、[列表](#lie-biao)、[代码块](#dai-ma-kuai)、[表格](#biao-ge)、[分隔线](#fen-ge-xian)。

## 段落

输入一行或连续的多行文字自然形成一个段落。在段落内换行时，需在行末留下两个空格。

```markdown
Once is the inspirational tale of two kindred spirits who find each other on the bustling streets of Dublin.

One is a street musician who lacks the confidence to perform his own songs.  
The other is a young mother trying to find her way in a strange new town.

As their lives intertwine, they discover each others talents and push one another to realize what each had only dreamt about before. Once is their inspiring story.
```

> Once is the inspirational tale of two kindred spirits who find each other on the bustling streets of Dublin.
>
> One is a street musician who lacks the confidence to perform his own songs.  
> The other is a young mother trying to find her way in a strange new town.
>
> As their lives intertwine, they discover each others talents and push one another to realize what each had only dreamt about before. Once is their inspiring story.

## 标题

在行首放置一到六个 `#` 建立标题，`#` 越多标题越小。标题只占用一行，无需多余空行分隔下文的块。

```markdown
# Once

## Glen Hansard

## Marketa Irglova

##### Once is their inspiring story
```

> # Once
>
> ## Glen Hansard
>
> ## Marketa Irglova
>
> ##### Once is their inspiring story

## 引用块

在行首放置一个 `>` 建立引用块。引用块可容纳另一个块，如果内部的块占用多行，需在每一行前加上 `>`，并用空格将每一行的内容起始处对齐。

```markdown
> A thirty-something busker (Guy) performs with his guitar on Grafton Street,  
> a Dublin shopping district and chases a man who steals his money.
>
> > Lured by his music, a young Czech flower seller (Girl) talks to him about his songs.
```

> > A thirty-something busker (Guy) performs with his guitar on Grafton Street,
> > a Dublin shopping district and chases a man who steals his money.
> >
> > > Lured by his music, a young Czech flower seller (Girl) talks to him about his songs.

## 列表

列表有两种。一种是有序表，有从 1 开始的数字为每一项编号；另一种是无序表，每一项前面都有一个点作为标记。连续且同类型的列表项自然形成一个列表。单个列表项可容纳另一个块，如果内部的块占用多行，需用空格将每一行的内容起始处对齐，参考 [示例](#wu-xu-lie-biao)。

### 无序列表

在行首放置一个 `*`、`+` 或 `-` 建立一个无序表项。

```markdown
- Delighted to learn that he repairs hoovers, Girl insists that Guy fix her broken hoover.
- The next day Girl returns with her broken hoover and tells Guy that she is also a musician.

  At a music store where Girl regularly plays piano, Guy teaches her one of his songs ("Falling Slowly"); they sing and play together.
```

> - Delighted to learn that he repairs hoovers, Girl insists that Guy fix her broken hoover.
> - The next day Girl returns with her broken hoover and tells Guy that she is also a musician.
>
>   At a music store where Girl regularly plays piano, Guy teaches her one of his songs ("Falling Slowly"); they sing and play together.

### 有序列表

在序号之后接上一个 `.` 或 `)` 建立一个有序表项，序号不会影响最终显示的编号。

```markdown
1. Guy invites her to his father's shop, and on the bus home musically answers Girl's question about what his songs are about:
2. a long-time girlfriend who cheated on him, then left ("Broken Hearted Hoover Fixer Sucker Guy").
```

> 1. Guy invites her to his father's shop, and on the bus home musically answers Girl's question about what his songs are about:
> 2. a long-time girlfriend who cheated on him, then left ("Broken Hearted Hoover Fixer Sucker Guy").

## 代码块

通过一对 ` ``` ` 或 `~~~` 建立代码块。在首行的末尾可添加别名 (Alias) 设置高亮显示的语言。若高亮功能由 _highlight.js_ 提供，在 [这里](https://github.com/highlightjs/highlight.js/blob/master/SUPPORTED_LANGUAGES.md) 能够找到可用的别名。若高亮功能由 _prism.js_ 提供，在 [这里](https://prismjs.com/#supported-languages) 能够找到可用的别名。

````txt
``` rust
fn main() {
   println!("Hello, Markdown");
}
```
````

> ```rust
> fn main() {
>     println!("Hello, Markdown");
> }
> ```

## 表格

通过 `|` 分隔文本自然形成一个表格，第一行是表头。可选择在第二行的每一列中填满 `-`，然后添加 `:` 作为前后缀，设置列的对齐方向。

```txt
| cats  | always |            meow |
| :---- | :----: | --------------: |
| music | always | evokes memories |
| life  | always |       works out |
```

> | cats  | always |            meow |
> | :---- | :----: | --------------: |
> | music | always | evokes memories |
> | life  | always |       works out |

## 分隔线

输入 `***` 或 `---` 生成一条水平分隔线。

```markdown
At the shop, Guy introduces Girl to his father and takes her to his room, but when he asks her to stay the night, Girl feels insulted and leaves.

---

The next day, they reconcile and spend the week writing, rehearsing and recording songs.
```

> At the shop, Guy introduces Girl to his father and takes her to his room, but when he asks her to stay the night, Girl feels insulted and leaves.
>
> ---
>
> The next day, they reconcile and spend the week writing, rehearsing and recording songs.

# 内联元素

链接、加粗、图片这类用于装饰文字或与文字混合排列的元素被称为内联元素。它们可以相互嵌套，同时作用于一段文字，但无法包含[块级元素](#kuai-ji-yuan-su)。

内联元素：[链接](#lian-jie)、[图片](#tu-pian)、[强调](#qiang-diao)、[加粗](#jia-cu)、[内联代码](#nei-lian-dai-ma)、[脚注](#jiao-zhu)。

## 链接

链接包含 文字、[地址](#lian-jie-di-zhi)、标题 三部分，格式为 `[文字](<地址> "标题")`，标题部分可省略。光标悬停至链接上方时，标题若存在则会悬浮显示。

```markdown
Girl rehearses lyrics for one of Guy's songs ("[If You Want Me](http://music.163.com/song?id=4340760 "Music From The Motion Picture Once")"), singing to herself while walking down the street; at a party, people perform impromptu (including "Gold").
```

> Girl rehearses lyrics for one of Guy's songs ("[If You Want Me](http://music.163.com/song?id=4340760 "Music From The Motion Picture Once")"), singing to herself while walking down the street; at a party, people perform impromptu (including "Gold").

### 链接地址

链接地址可在正文中直接使用，也可以用 `<>` 括起来，避免一些特别的地址不被识别到。

```markdown
「If You Want Me」 is available at <http://music.163.com/song?id=4340760>.
```

> 「If You Want Me」 is available at <http://music.163.com/song?id=4340760>.

### 引用链接

通过一个标签，链接的 [地址](#lian-jie-di-zhi) 与标题，可同文字关联起来。引用时格式为 `[文字][标签]`，定义时格式为 `[标签]: <地址> "标题"`，标题可省略。当文字与标签相同时，文字部分的标签也可省略。

```markdown
Guy works on "[Lies]", a [song][Lies] about his ex-girlfriend, who moved to London. Girl encourages him to win her back. Invited to the woman's home, Guy discovers that Girl has a toddler and lives with her mother.

[Lies]: http://music.163.com/song?id=4340768 "Music From The Motion Picture Once"
```

> Guy works on "[Lies]", a [song][Lies] about his ex-girlfriend, who moved to London. Girl encourages him to win her back. Invited to the woman's home, Guy discovers that Girl has a toddler and lives with her mother.
>
> [Lies]: http://music.163.com/song?id=4340768 "Music From The Motion Picture Once"

## 图片

图片包含 文字、[地址](#lian-jie-di-zhi)、标题 三部分，格式为`![文字](<地址> "标题")`，标题可省略。文字部分在图像加载失败或语音朗读时被使用。如果有标题，光标悬停至图片上方时，标题会悬浮显示。

```markdown
![A piano](/banners/piano.jpg "Roland FP-18")
```

> ![A piano](/banners/piano.jpg "Roland FP-18")

## 强调

一对 `*` 或 `_` 包括的文字会被显示为斜体，词组中的 `_` 不受影响。

```markdown
Guy decides to move to London, but he wants to record a demo of his songs to take with him and asks Girl to record it with him. They secure a bank loan and reserve time at a recording studio. Guy learns Girl has a husband in the _Czech Republic_.
```

> Guy decides to move to London, but he wants to record a demo of his songs to take with him and asks Girl to record it with him. They secure a bank loan and reserve time at a recording studio. Guy learns Girl has a husband in the _Czech Republic_.

## 加粗

一对 `**` 或 `__` 包括的文字会被加粗，词组中的 `__` 不受影响。

```markdown
When he asks if she still loves her husband, Girl answers in Czech, "**Miluji tebe**" ("I love you"), but coyly declines to translate. After recruiting a band from other buskers, they go into the studio to record.
```

> When he asks if she still loves her husband, Girl answers in Czech, "**Miluji tebe**" ("I love you"), but coyly declines to translate. After recruiting a band from other buskers, they go into the studio to record.

## 内联代码

一对 `` ` `` 或 ` `` ` 包括的文字会被视作代码，以特别的等宽字体显示。

```markdown
They impress Eamon, the jaded studio engineer, with their first song ("When Your Mind's Made Up"). On a break in the early morning, Girl finds a piano in an empty studio and plays Guy one of her own compositions ("`The Hill`").
```

> They impress Eamon, the jaded studio engineer, with their first song ("When Your Mind's Made Up"). On a break in the early morning, Girl finds a piano in an empty studio and plays Guy one of her own compositions ("`The Hill`").

## 脚注

脚注由注解与引用两部分组成，被一个标签关联起来。注解部分格式为 `[^标签]: 注解`，会被放到页面的底部。引用部分格式为 `[^标签]`，可多次使用。

```markdown
"Falling Slowly"[^falling-slowly] won the 2007 Academy Award for Best Original Song.

[^falling-slowly]: "Falling Slowly", available at [NeteaseMusic](https://music.163.com/#/song?id=4340758).
```

> "Falling Slowly"[^falling-slowly] won the 2007 Academy Award for Best Original Song.
>
> [^falling-slowly]: "Falling Slowly", available at [NeteaseMusic](https://music.163.com/#/song?id=4340758).

# 转义字符

输入 `\` 可将紧随其后的一个标点符号转义为普通文本。例如，双反斜杠 `\\` 被显示为它自身 `\`。大多数时候标点符号不构成语法，可以不转义。

- 可被转义的字符：[ASCII](https://www.cs.cmu.edu/~pattis/15-1XX/common/handouts/ascii.html) 中的任意标点符号；特别的，换行符被转义为一个硬回车，表示段落内换行。
- 禁用转义的区域：[代码块](#dai-ma-kuai)、[内联代码](#nei-lian-dai-ma)、[链接地址](#lian-jie-di-zhi)、[HTML](#HTML)。

```markdown
Before leaving for the airport\, Guy buys Girl a piano and makes arrangements for its delivery\, then calls his ex\-girlfriend\, who is happy about his imminent arrival\. \
Girl reunites with her husband in Dublin and plays the piano in their home\.
```

> Before leaving for the airport\, Guy buys Girl a piano and makes arrangements for its delivery\, then calls his ex\-girlfriend\, who is happy about his imminent arrival\. \
> Girl reunites with her husband in Dublin and plays the piano in their home\.

# HTML

Markdown 中可以直接使用 HTML 标签。如果想在 HTML 标签内部再使用 Markdown 语法，需用空行分隔。

```markdown
<div style="background-color: #fadce1; padding: .2rem 2rem">

The story in the examples is taken from [Wikipedia](<https://en.wikipedia.org/wiki/Once_(film)>).

</div>
```

> <div style="background-color: #fadce1; padding: .2rem 2rem">
>
> The story in the examples is taken from [Wikipedia](<https://en.wikipedia.org/wiki/Once_(film)>).
>
> </div>
