# 第1章 开始 Lisp 之旅 GETTING STARTED WITH LISP

翻译者：Freeblues

github版本：https://github.com/FreeBlues/Land-of-lisp-CN

开源中国版本：http://my.oschina.net/freeblues/blog?catalog=516771

##	目录

*	Lisp 方言
	*	两种 Lisp 的故事 A Tale of Two Lisps
	*	Lisp 的前景 Up-and-Coming Lisps
	*	被用于脚本的 Lisp 方言 Lisp Dialects Used for Scripting
	*	ANSI Common Lisp
*	开始 CLISP 之旅
	*	安装 CLISP Installing CLISP
	*	启动 CLISP Starting Up CLISP
*	本章你学到的 What You’ve Learned


本章从介绍 Lisp 的各种方言开始。然后我们会讨论一点 ANSI Common Lisp，也就是我们将会在本书使用的 Lisp 方言。最后你将会从安装和试验 CLISP 开始，这是 ANSI Common Lisp 的一种实现，它将会运行本书中你所创建的所有 Lisp 游戏程序。

##	Lisp 方言

任何遵守 Lisp 核心原则的程序语言都被认为是一种 Lisp 方言。既然这些原则是如此简单，所以毫不奇怪确确实实有一百多种 Lisp 方言被创造出来。事实上，既然这么多崭露头角的 Lisper 创造出他们自己的 Lisp 方言来作为一种练习，遍及整个星球可能会有上千种部分完成的 Lisp 沉睡于硬盘的冗长目录中。然而，绝大多数的 Lisp 社区使用这两种 Lisp 方言：ANSI Common Lisp（常被缩写为 CL）和 Scheme。

在本书中，我们将仅仅讨论 ANSI Common Lisp 方言，它在这两种方言中稍微流行一些。尽管如此，你从阅读本书获得的大多数知识也与 Scheme 有关（尽管在两种方言之间关于函数名字的内容趋于不同）。

###	两种 Lisp 的故事 A Tale of Two Lisps

在 ANSI Common Lisp 和 Scheme 之间存在一些深刻的哲学思想的不同，并且它们引来对不同程序员的人身攻击。一旦你学习到更多 Lisp 语言的知识，你就能决定你更喜欢哪一种方言。这里的选择不存在对或错。

为了帮助你做出自己的决定，我为你创建了下面的个人化测试：

![C1-1个性测试图](file:///)	

如果你选择 A，你喜欢具备原始能力的语言。你不在乎你的语言是否有一点丑陋，因为大量出于务实的妥协，只要你仍然可以写出紧凑的代码。ANSI Common Lisp 是你最好的语言！ANSI Common Lisp 追溯它的起源更直接来自原始的 Lisp 方言，建立在数以百万的程序员小时之上，赋予它极其丰富的功能。固然，它有一些巴洛克式的函数名带来无数的历史事故，但是这种 Lisp 确实能够在正确的黑客手中飞翔。

如果你选择 B，你喜欢洁净和优雅的语言。你对基本编程问题更感兴趣	，并且乐于在美丽的草地上消磨时光，深入思考你代码的美丽，偶尔写写关于理论计算问题的研究论文。Scheme 就是为你准备的语言！它在1970年代中期由 Guy L. Steele 和 Gerald Jay Sussman 创造，并且受到一些对理想 Lisp 反省式的影响。Scheme 的代码趋于稍微啰嗦，因为比起创建最短程序的可能性， Schemer 更关注他们代码的数学纯粹性。

如果你选择 C，你就是那种希望希望同时得到两者的人： ANSI CL 的威力和 Scheme 的数学美。现在，还没有任何一种 Lisp 方言完全符合你的要求，不过这一点将会在未来发生改变。有一种可能满足你要求的语言（尽管在一本 Lisp 书中做出这个断言是一种亵渎/不敬）是 Haskell。它不被看做是一种 Lisp 方言，不过它的追随者们遵守那些流行于 Lisper 中的范例，比如保持语法统一性，支持本地列表，并且严重依赖高阶函数。更重要的是，它具备极端的数学严格（甚至超过 Scheme）允许它把非常强大的功能隐藏在一个机器洁净的界面下。它本质上就是一只披着羊皮的狼。跟 Lisp 一样，Haskell 是这样一种语言，任何程序员都会在未来对它的研究中获益。

###	Lisp 的前景 Up-and-Coming Lisps

就像刚才提到的，实际上不存在一种 Lisp 方言，它既拥有 ANSI Common Lisp 的强大和灵活，又有 Scheme 的优雅。然而，一些新崛起的挑战者可能赢得这两个世界最好的奖杯在不远的将来。

一种前景很好的新的 Lisp 是 Clojure，由 Rich Hickey 开发的一种方言。Clojure 构建于 Java 平台之上，使得它获得大量成熟 Java 库的立即可用的影响。Clojure 还包括一些聪明而且深思熟虑的特性用于简化多线程编程，使得它成为一种有用的工具用于为看起来随处可见的多核 CPU 编程。

另一个有趣的挑战者是 Arc。它是一种主要由著名 Lisper Paul Graham 开发的真正的 Lisp 语言。Arc现在仍然处于开发的早期阶段，关于它在其他 Lisp 之上做了多大改善，还存在很多争议。它的开发进度目前还在以被冻结一样的缓慢速度进行着。在任何人宣称 Arc 将成为一个有意义的挑战者之前还需要一段时间。

我们将在结语中对 Arc 和 Clojure 略作品鉴。

###	被用于脚本的 Lisp 方言 Lisp Dialects Used for Scripting

一些 Lisp 方言被用于脚本编程，如下：

Emacs Lisp 被流行的（） Emacs 文本编辑器用作内部的脚本。

Guile Scheme 在一些开源应用中被作为一种脚本语言来使用。

Script-Fu Scheme 被用于 GIMP 图形编辑器。

这些方言是 Lisp 主要分支的更旧版本的分支，并且很少被用于建立独立的应用程序。然而，他们仍然是完美体面的 Lisp 方言。

###	ANSI Common Lisp

1981年，为了应付这种语言那令人眩晕的方言数量，各个不同的 Lisp 社区共同起草了一份被称为 Common Lisp 的新方言的规格。在1986年，经过一些调整之后，这种语言变成了 ANSI Common Lisp 标准。很多老版本 Lisp 的开发者修改了他们的解释器和编译器来使之符合新标准，这个新标准就此成为最流行的 Lisp 版本并且保持至今。

注意

贯穿本书，术语 Common Lisp 指的是按照 ANSI 标准定义的 Common Lisp 版本。

Common Lisp 的一个关键设计目标是创建一种多范式语言，意思是它要包括对许多种不同编程模式的支持。你可能听说过面向对象编程，可以非常好地在 Common Lisp 中做到。其他你可能没有听说过的编程模式，包括函数式编程，通用编程以及特定领域语言编程（DSL）。这些在 Common Lisp 中都可以很好地支持。你将会学习这里的每一种编程模式，一个接着一个，随着我们这本书的推进。


##	开始 CLISP 之旅

很多伟大的 Lisp 编译器都可以用，不过有一种尤其容易上手：CLISP，一种开源的 Common Lisp。CLISP的安装非常简单，而且可以运行在任何操作系统上。

其他流行的 Lisp 包括 Steel Bank Common Lisp (SBCL)，一种快速的 Lisp，被认为比 CLISP 更重型一点；Allegro Common Lisp，由 Franz，Inc 开发的强大的商业 Lisp；Clozure CL；以及 CMUCL。Mac 用户可能认为 LispWorks 或 Clozure CL 更容易运行在他们的机器上。然而，对于我们的目标来说，CLISP 是最好的选择。

注意

从第12章开始，我们将会使用一些 CLISP特定的命令，这些命令被认为是非标准的。不过，直到那一章，Common Lisp 的任一种实现都可以运行本书中的例子。

###	安装 CLISP Installing CLISP

你可以从 http://clisp.cons.org/ 下载一个 CLISP 安装程序，它可以在 Windows PC，Mac，以及不同变体的 Linux 上运行。在一台 Windows PC 上，你只要简单运行一个安装程序即可。在一台 Mac 上，有一些额外的步骤，这些细节都在网站上有详细描述。

在一台基于 Debian 的 Linux 机器上，你应该可以发现 CLISP 以及存在你的标准源代码中了。只需要在命令行输入  
	
	apt-get install clisp 

然后，CLISP 就会自动安装好。

对于其他的 Linux 发行版本（如 Fedora，SUSE 等等），你可以使用列在 CLISP 网站的 “Linux packages”下的标准包。而且，有经验的 Linux 用户可以通过源代码来编译 CLISP。

###	启动 CLISP Starting Up CLISP

在你的命令行输入：

	clisp
	
就可以运行 CLISP。如果一切正常，你将会看到如下的提示画面：

$ clisp
  i i i i i i i       ooooo    o        ooooooo   ooooo   ooooo
  I I I I I I I      8     8   8           8     8     o  8    8
  I  \ `+' /  I      8         8           8     8        8    8
   \  `-+-'  /       8         8           8      ooooo   8oooo
    `-__|__-'        8         8           8           8  8
        |            8     o   8           8     o     8  8
  ------+------       ooooo    8oooooo  ooo8ooo   ooooo   8

Welcome to GNU CLISP 2.49 (2010-07-07) <http://clisp.cons.org/>

Copyright (c) Bruno Haible, Michael Stoll 1992, 1993
Copyright (c) Bruno Haible, Marcus Daniels 1994-1997
Copyright (c) Bruno Haible, Pierpaolo Bernardi, Sam Steingold 1998
Copyright (c) Bruno Haible, Sam Steingold 1999-2000
Copyright (c) Sam Steingold, Bruno Haible 2001-2010

Type :h and hit Enter for context help.

[1]>

和所有的 Common Lisp 环境一样，CLISP 在你启动它之后会自动把你带到它的一个 读取-求值-打印-循环（REPL）中（read-eval-print loop）。这意味着你能立即开始输入 Lisp 代码。

试着输入：

	(+ 3 (* 2 4))
	
你将会看到结果被打印在这个表达式下面：

[1]> (+ 3 (* 2 4)) 
11

这个实验演示了 REPL 是如何工作的。你输入一个表达式，然后 Lisp 将会立即求值并且返回结果值。当你想要关闭 CLISP 时，输入（quit）即可（译者注：需要连括号一起输入）。

不论如何你已经让 CLISP 运行在你的计算机上了，做好准备编写一个 Lisp 游戏！

##	本章你学到的 What You’ve Learned

在本章中，我们讨论了 Lisp 的不同方言并且安装了 CLISP。通过这种方法你学到如下内容：

*	有两种主要的 Lisp 方言：Common Lisp 和 Scheme。它们都提供了很多功能，不过在本书中我们将会聚焦于 Common Lisp。

*	Common Lisp 是一种多范式语言，意味着它支持许多不同的编程模式。

*	CLISP 是这样一种 Common Lisp 实现，它非常容易设置，使得对于一个 Lisp 初学者来说，它是一种出色的选择。

*	你可以从 CLISP 的 REPL 中直接输入 Lisp 命令。

![C1-2漫画图](file:///)





























