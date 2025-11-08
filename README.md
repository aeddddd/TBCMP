当前版本:`3.0.0`
### 相关说明 About
**来源说明**:本书所使用Tex模板来源于[kaobook](https://github.com/yhua123/kaobook/tree/master)的中文版本.

主要参考书籍列表:List of main reference books:
- Modern Quantum Mechanics 2nd.J.J.Sakurai 
- Entanglement in Many-Body Systems
- 物理学家用李群李代数
- Nicolas Dupuis - Field Theory of Condensed Matter and Ultracold Gases 
- etc
### 前言 Introduction

本书作为学习凝聚态场论的记录, 以及一些自己的看法, 尽量做到每一步都自己尝试过推导, 以及相应计算的完成. 部分内容还在整理中, 仅由`markdown`文档存在 , 没有完全上传.

### 特殊公式标注
使用tikz达成该效果,具体参照来源github某库(尚未溯源)

```tex
\begin{equation}
	\vspace{\baselineskip}
	%公式编号: %<eq:num%>
	%<eqa%:id:111%>
    \tikzmarknode{%<num%:mirror%>   eq1}{\highlight{red}{$%<eqb%:id:112%>$}}
    %<eqf%:id:514%>
    \tikzmarknode{%<num%:mirror%>   eq2}{\highlight{blue}{$%<eqc%:id:113%>$}}
    %<eqg%:id:116%>
\end{equation}
\begin{tikzpicture}[overlay,remember picture,>=stealth,nodes={align=left,inner ysep=1pt},<-]
	% 对于 "1" 定位点
	\path (%<num%:mirror%>   eq1.north) ++ (0,2em) node[anchor=south east,color=red!67] (eq%<num%:mirror%>   /1){\textbf{%<d%:id:114%>}};
	\draw [color=red!87](%<num%:mirror%>   eq1.north) |- ([xshift=-0.3ex,color=red]eq%<num%:mirror%>   /1.south west);
	% 对于 "2" 定位点
	\path (%<num%:mirror%>   eq2.south) ++ (0,-1.5em) node[anchor=north west,color=blue!67] (eq%<num%:mirror%>   /2){\textbf{%<e%:id:115%>}};
	\draw [color=blue!57](%<num%:mirror%>   eq2.south) |- ([xshift=-0.3ex,color=blue]eq%<num%:mirror%>   /2.south east);
\end{tikzpicture}
```
其中第三行`%<eq:num%>`内填入公式标号(实际使用该宏只会显示`num`),分别在`eqa`,`eqf`,`eqg`内填入无需框选的公式部分,在`eqb`,`eqc`内分别填入被框选标记的公式

在`d`,`e`内填入需要标记的文本,具体使用快捷键输出样式参考下面:`num`仅需要填写一次,后续会自动填充.

```tex
\begin{equation}
	\vspace{\baselineskip}
	%公式编号: eq:num
	eqa\tikzmarknode{eq:numeq1}{\highlight{red}{$eqb$}}eqf\tikzmarknode{eq:numeq2}{\highlight{blue}{$eqc$}}
\end{equation}
\begin{tikzpicture}[overlay,remember picture,>=stealth,nodes={align=left,inner ysep=1pt},<-]
	% 对于 "1" 定位点
	\path (eq:numeq1.north) ++ (0,2em) node[anchor=south east,color=red!67] (eqeq:num/1){\textbf{d}};
	\draw [color=red!87](eq:numeq1.north) |- ([xshift=-0.3ex,color=red]eqeq:num/1.south west);
	% 对于 "2" 定位点
	\path (eq:numeq2.south) ++ (0,-1.5em) node[anchor=north west,color=blue!67] (eqeq:num/2){\textbf{e}};
	\draw [color=blue!57](eq:numeq2.south) |- ([xshift=-0.3ex,color=blue]eqeq:num/2.south east);
\end{tikzpicture}
```
`2em`和`-1.5em`可以改为`0.5em`和`-0.5em`,这样可以避免换行.