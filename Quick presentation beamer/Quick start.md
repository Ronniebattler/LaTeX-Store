# Quick start Beamer

## 调整Slides页面大小

正常的Slides大小如下：

<img src="D:\WPS_Renhe\WPS_Study\LaTeX-Store\Quick presentation beamer\Beamer_00.png" alt="Beamer_00" style="zoom: 33%;" />

修改documentclass，改为16:9大小的，则为：

<img src="D:\WPS_Renhe\WPS_Study\LaTeX-Store\Quick presentation beamer\Beamer_11.png" alt="Beamer_11" style="zoom:33%;" />

代码如下

```tex
\documentclass[UTF8,aspectratio=169]{beamer}%aspectratio=169将页面调整为16:9
```

## 更改主题

```tex
%更改主题
\usetheme{Copenhagen}%主题选Copenhagen
\usecolortheme{beaver}%但是颜色选beaver
```

查看主题的网站：https://deic.uab.cat/~iblanes/beamer_gallery/index_by_theme_and_color.html

## 关闭导航标签

在导言区输入：

```tex
%关闭导航标志
\setbeamertemplate{navigation symbols}{}
```

![navigation](D:\WPS_Renhe\WPS_Study\LaTeX-Store\Quick presentation beamer\navigation.png)

输入以上代码将以上的标志删除。

## 每页出现隐藏item

`\item<1-> Collaboration` 其中`<1->` 表示只在第一张slide显示

`\only<1>{这个文字只会出现在第一页.}`表示只在第一页显示

`\onslide<2>{This text only appear on the second slide.}`表示第二张显示

 `\onslide<3>{This text will continue appear on the third slide.}`表示第三张继续显示：

<img src="D:\WPS_Renhe\WPS_Study\LaTeX-Store\Quick presentation beamer\item1.png" alt="item1" style="zoom:75%;" />

首先，第一页`\alert<1>{警告}`,第二页`\textbf<2>{加粗}`. 表示第一页会警告色，第二页会加粗，这样可以变化要注意的地方，影响观感。

<img src="D:\WPS_Renhe\WPS_Study\LaTeX-Store\Quick presentation beamer\alert.png" alt="alert" style="zoom:75%;" />

## 分栏

```tex
\begin{frame}{Two Columns}
    \begin{columns}
        \column{0.5\textwidth}%占据一半页面文字长度
            第一栏
        \column{0.5\textwidth}
            第二栏
    \end{columns}
\end{frame}
```

## 目录

```tex
%目录
\begin{frame}{Title Page}
    \tableofcontents
\end{frame}
```

每一个section会出现目录：

```tex
\begin{frame}
\tableofcontents[sectionstyle=show,subsectionstyle=show/shaded/hide,subsubsectionstyle=show/shaded/hide]
\end{frame}
```

