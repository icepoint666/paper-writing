# cv论文相关latex笔记

### 1.基本语法
```tex
\documentclass{article}
 
\begin{document}
First document. This is a simple example, with no 
extra parameters or packages included.
\end{document}
```
\documentclass声明文档类型

```tex
\documentclass[12pt, letterpaper]{article}
\usepackage[utf8]{inputenc}
 
\title{First document}
\author{Hubert Farnsworth \thanks{funded by the ShareLaTeX team}}
\date{February 2014}
```
12pt, letterpaper 文字大小与纸张大小

```tex
\documentclass[12pt, letterpaper, twoside]{article}
\usepackage[utf8]{inputenc}
 
\title{First document}
\author{Hubert Farnsworth \thanks{funded by the ShareLaTeX team}}
\date{February 2014}
 
\begin{document}
 
\begin{titlepage}
\maketitle
\end{titlepage}
 
In this document some extra packages and parameters
were added. There is an encoding package
and pagesize and fontsize parameters.
 
\end{document}
```

前面定义好的\title 以及作者，邮箱,\maketitle可以将它们都显示出来

**注释是%**

**\def为了书写方便**
```tex
\def\E{\mathrm{E}}
\def\Var{\mathrm{Var}}
\def\Cov{\mathrm{Cov}}
```
**\include 和\input 命令**

\include 和\input都是将子.tex文件import到主.tex文件中的命令，因为当我们写一本书或者写作内容很长时，每个部分写成独立的.tex文件会方便一些。

基本用法:

在主.tex文件main.tex中在需要插入子.tex文件subfile.tex之处输入：\input{subfile.tex} 或 \include{subfile.tex}。

区别:
- \input进来的文本编译后将连续排版；
- \include进来的每一个文件将重新开始一页排版；

也就是说\include进来的文件是单独编译再和进主.tex的.pdf输出的，因此我们也看到使用\include时每个子.tex文件都会在编译后产生.aux文件；

\input可以写进Preamble，而\include不可以；

我在一个被\input的子.tex文件中使用了\include，结果编译错误。似乎是\include不可以递归使用，而\input是可以的。

原文链接：https://blog.csdn.net/weixin_42919606/article/details/82939495

**\vspace{1cm}来产生一个空格,利用命令\vskip{0.3cm}来产生垂直的空隙**
