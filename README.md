### 相关说明 About
这本书所使用Tex模板来源于[elegantbook](https://github.com/ElegantLaTeX/ElegantBook).

这本书的编著目的是用于小组学习,主要包含了通往一般理论物理凝聚态期刊中的**重要**的知识体系,对于次要的,我推荐在实际使用时再去补充.事实上,想要如同国内高中时的方法学习这一部分*几乎是* 不可能的.

**正在重构部分内容,目前以pdf内容为准,重构完毕后会修改README文件**
**Part of the content is being reconstructed, currently the pdf content prevails, and the README file will be modified after the reconstruction**

主要参考书籍列表:List of main reference books:
- Modern Quantum Mechanics 2nd.J.J.Sakurai
- Quantum Field Theory in Condensed Matter Physics 2nd.Alexei M.Tsvellk
- Entanglement in Many-Body Systems
- 物理学家用李群李代数
- 物理学中的泛函分析
- Nicolas Dupuis - Field Theory of Condensed Matter and Ultracold Gases
- Conformal Field Theory A.N. Schellekens
- 列表不全,请参考讲义中最后附录

当前版本:1.2.1
vision:1.2.1

*尚未制作完成,仅供参考. 
It has not been made yet and is for reference only.*

### 前言 Introduction
很多初学者在初次自学较高深的物理的时候往往会犯一个错误:被同等级的高深的数学所迷惑,认为学好这些物理离不开这些数学.但事实上,学好物理确实离不开数学,但仅仅是一小部分的数学.例如,学好量子力学离不开线性代数,但经常有很多物理系的学生拐去学习泛函分析,李代数,辛几何之类的内容,而这些数学内容往往只有一小部分应用在物理上面,打着先学完这些数学再开始学习物理的想法,只会让物理的学习一拖再拖.我们应当意识到,数学不过是物理的工具,切勿舍本逐末.

但这并不意味着数学不重要,离开数学的物理不亚于纸上谈兵,毫无意义.而对于本讲义,前面的部分并不十分紧要,仅作为开启凝聚态场论的先备知识,将重要的部分提取出来,作为前两章.第三章是为后续的大量使用做铺垫,第四章开始是文章的主体部分,最后的几章为目前在做的研究方向的总结.

对于前三章,可能出现许多笔误的情况,后续会逐一修正,第一第二章的讲述方式极大的参考了樱井纯的现代量子力学.

前言仅供参考,不代表最终前言内容和书中内容,该前言已经是第二版.

目前进度:第四章.

Many beginners often make a mistake when they first self-study advanced physics: they are confused by the advanced mathematics of the same level and think that learning these physics well is inseparable from these mathematics. But in fact, learning physics well is indeed inseparable from mathematics, but only a small part of mathematics. For example, learning quantum mechanics well is inseparable from linear algebra, but there are often many physics students who go to learn functional analysis, Lie algebra, symplectic geometry and other contents, and these mathematical contents are often only a small part of physics. The idea of ​​learning these mathematics first and then starting to learn physics will only delay the study of physics. We should realize that mathematics is just a tool for physics, and we should not lose sight of the main purpose. 

But this does not mean that mathematics is not a tool for physics. Learning is not important. Physics without mathematics is no less than talking on paper and meaningless. For this lecture, the previous part is not very important. It is only used as the prerequisite knowledge for opening the condensed matter field theory. The important part is extracted as the first two chapters. The third chapter paves the way for subsequent extensive use. The fourth chapter is the main part of the article. The last few chapters are a summary of the current research direction. 

For the first three chapters, there may be many typos, which will be corrected one by one later. The narration of the first and second chapters is largely based on Sakurai Jun's modern quantum mechanics. 

The preface is for reference only and does not represent the final preface content and the content of the book. This preface is already the second edition. 

Current progress: Chapter 4.

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