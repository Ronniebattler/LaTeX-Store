# TikZ学习

## Chapter 1 BASIC

### 1.1 加载宏包与程序库

```tex
\usepackage{tikz} % LATEX
\input tikz.tex % plain TEX
\usemodule[tikz] % ConTEXt
```

`\usetikzlibrary{⟨list of libraries⟩}`

当载入 Ti*k*Z 后，就可以用这个命令载入 libraries. 列出的 libraries 名称之间用逗号分隔。本命令中的花括号可以换成方括号

```tex
\usetikzlibrary[⟨list of libraries]
```

例如

```tex
\usetikzlibrary{arrows.meta,animations}
```

### 1.2 创建一个picture

Ti*k*Z 的最外层绘图区域是 {tikzpicture} 环境，<u>所有绘图命令 (除了命令 \tikzset) 都要放在环境内。环境内的选项仅在环境内有效。</u>该环境可以用于大多数 LATEX 模式、环境、命令内，例如用于页眉、页脚命令内，数学模式内。

```tex
\begin{tikzpicture}⟨animations spec⟩[⟨options⟩]

⟨environment content⟩

\end{tikzpicture}
```

