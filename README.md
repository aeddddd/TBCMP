### 相关说明 About
这本书所使用Tex模板来源于[elegantbook](https://github.com/ElegantLaTeX/ElegantBook).

这本书的编著目的是用于小组学习,主要包含了通往一般理论物理凝聚态期刊中的**重要**的知识体系,对于次要的,我推荐在实际使用时再去补充.事实上,想要如同国内高中时的方法学习这一部分*几乎是* 不可能的.

**正在重构部分内容,目前以pdf内容为准,重构完毕后会修改README文件**
**Part of the content is being reconstructed, currently the pdf content prevails, and the README file will be modified after the reconstruction**

主要参考书籍列表:List of main reference books:(斜体内容为并未实际参考内容,后续可能参考)
- Modern Quantum Mechanics 2nd.J.J.Sakurai
- *Quantum Field Theory in Condensed Matter Physics 2nd.Alexei M.Tsvellk*
- Entanglement in Many-Body Systems
- 物理学家用李群李代数
- *物理学中的泛函分析*
- Nicolas Dupuis - Field Theory of Condensed Matter and Ultracold Gases
- *Conformal Field Theory A.N. Schellekens*
- 列表不全,请参考讲义中最后附录

当前版本:2.0.1

*尚未制作完成,仅供参考.*

### 前言 Introduction
很多初学者在初次自学较高深的物理的时候往往会犯一个错误:被同等级的高深的数学所迷惑,认为学好这些物理离不开这些数学.但事实上,学好物理确实离不开数学,但仅仅是一小部分的数学.例如,学好量子力学离不开线性代数,但经常有很多物理系的学生拐去学习泛函分析,李代数,辛几何之类的内容,而这些数学内容往往只有一小部分应用在物理上面,打着先学完这些数学再开始学习物理的想法,只会让物理的学习一拖再拖.我们应当意识到,数学不过是物理的工具,切勿舍本逐末.

但这并不意味着数学不重要,离开数学的物理不亚于纸上谈兵,毫无意义.而对于本讲义,前面的部分并不十分紧要,仅作为开启凝聚态场论的先备知识,将重要的部分提取出来.

前言仅供参考,不代表最终前言内容和书中内容,该前言已经是第三版.

目前进度:第二章.

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

**后续会补充图片说明**


### 版本更新历史 History
#### 1.0.0 
*date:2024/07/18*
* 完成大纲部分.
#### 1.0.1 
*date:2024/07/19*
* 完成部分附录内容.
#### 1.0.3 
*date:2024/07/21*
* 开始完成第一章部分,对前言部分进行补充.
* 移除了原本在文章中的更新记录,改为在README中记录.
* 开始使用Git控制文档.
#### 1.0.4 
*date:2024/09/04*
* 第一章完成,开始第二章
* 更改了部分大纲,中间加入泛函分析和Lie群Lie代数的内容,删去一些重复内容.
#### 1.1.0 
*date:2024/09/19*
* 第二章大部分完成,修补了部分目录
* 重新组织了大纲,重新安排了tex文件结构.
#### 1.1.1 
*date:2024/10/1*
* 第二章完成
* 加入了部分第一章习题解析
#### 1.1.2
*date:2024/10/17*
* 第三章大部分完成
* 重新整理了后续大纲
#### 1.2.0 
*date:2024/11/3*
* 开始第四章,第三章后半部分暂且搁置
* 重新整理了前三章内容,删除一部分内容,尤其是第三章
#### 1.2.1 
*date:2024/11/16*
* 对于第四章,开始采取更新的公式样式
* 整理README内容,使其与当前状态相匹配
* 加入了配套Mathematica文件(从第四章开始)
* 加入了小组内配套使用的习题(仅供参考)
#### 2.0.0 
*date:2025/2/22*
* 开始重构全文逻辑
* 整理README内容
* 将原版的前两章移动到附录
#### 2.0.1 
*date:2025/3/12*
* 继续重构全文逻辑
* 整理README内容,添加新的公式样式使用说明
* 移动后的两章暂时隐藏
* 更新了简介
* 更新了部分正文内容