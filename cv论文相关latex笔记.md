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

前面定义好的\title 以及作者邮箱,\maketitle可以将它们都显示出来

**注释是%**

**\def为了书写方便**
```tex
\def\E{\mathrm{E}}
\def\Var{\mathrm{Var}}
\def\Cov{\mathrm{Cov}}
```
