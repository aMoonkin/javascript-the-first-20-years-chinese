# 引言

2020 年，随着无数联网设备与无数网站相连接，万维网已经无处不在。这些设备里都运行着一个浏览器，或者类似的程序，使得它们可以处理和展示网站中的页面。这些页面大多嵌入着加载着用 JavaScript 写成的代码。可以说，在 2020 年，JavaScript 是世界范围内部署最广泛的编程语言。而 Stack Overflow 2018 年的调查显示，JavaScript 正在被 71.5%的专业开发者使用，使得它也成为世界上使用最广泛的语言。

这篇文章将告诉你在 1995-2015 这 20 年来，javascript 的创造，设计，演变和标准化的故事。这个故事不只包括 js 的技术细节，也包括了人和组织的如何通过竞争与合作，来塑造这个主导 2020 年网络世界的 JavaScript。

这是一个漫长而复杂的故事。为了让它更易读懂，这篇文章将分为四个主要部分，每部分分别覆盖了一个 js 发展和演化的主要阶段。在每个部分之间都有一个简短的插曲，介绍了当时软件开发者是如何应对使用 js 的。

在 1995 年，网络和浏览器还是新兴事物，那时 Netscape 公司正在领导 web 浏览器的开发工作。js 最初被该书的作者之一 Brendan Eich 设计和实现，它旨在成为一种简单，易于使用的动态语言，并使代码片段可以被包含在网页的定义之中。浏览器将这些片段解析渲染为页面，并使这些页面可以动态展示并对用户行为做出响应。

第一部分，JavaScript 起源，关于 JavaScript 的创造和早期发展，探究了 js 第一个版本的动机与取舍。因为名字的原因，js 经常会与 java 扯上关系。第一部分解释了 js 起名的过程、两种语言之间的关系，以及发生了什么。包括早期特性的 overview 以及驱动这些特性的设计决策。第一部分还介绍了最初几年中语言的在 Netscape 和其他公司的发展。

开放技术是 web 的基石。每个人都可以创建创建 web 页面，这些页面托管在不同的 web 服务器中，并可以被各种浏览器访问。共同的规范促进了独立的浏览器实现之间的互操作性。在 js 诞生之初，人们就知道 JavaScript 需要某种形式的标准规范。第一年，web 开发者就在 Netscape 和微软逆向得来的 js 实现间遇到了互操作性问题。1996 年，Ecma 国际标准化组织主持推进了 js 标准化进程。第一个官方标准规范该语言于 1997 年以“ECMAScript”的名称发行。另外两个主要基于 Netscape 语言的演变的修订和增强功能版本，于 1999 年底发行。

第二部分，标准创立。此部分探究了 JavaScript 标准化工作时如何启动的，谁为这项工作做出了贡献以及如何制定决策。

在 2000 年之前，js 被广泛的应用在 web 中，但 Netscape 却走向衰败，Eich 也投向了其他项目。在缺失了公司和个人的独裁后，谁能领导 js 未来的演进呢？发展 JavaScript 的责任就落在了 ECMAScript 标准委员会身上。这种设计责任的转移并不顺利。ECMAScript 组织试图找到自己发展语言路线的同时，也是长达 10 年错误的开始、标准化的中断和错误的努力。与此同时，js 的实际使用量迅速增长，并且经常使用特定的扩展。这造成了大量依赖 JavaScript 的 Web 页面未被维护，并暴露了新的互操作性问题。

第三部分，改革失败。这部分探究了修改语言的不成功尝试，由此引发的标准委员会内部动荡，以及该动荡最终如何解决的。

2008 年，标准委员会恢复了和谐的运作，并在 09 年发布了一个标准的现代增强版本。随着这次成功，标准委员会也终于准备好了成功地承担起使语言现代化的任务。再后来七年的时间里，委员会对该语言及其规范进行了重大改进。结果就是大家熟知的 ECMAScript 2015，也是语言能够持续发展的基础。在完成 ECMAScript 2015 版本发布之后，委员会再次修改了它的流程，来确保有一个更快的版本发布时间。现在，定期每年完成修订工作。

第四部分，现代化的 js，是关于在 2009 和 2015 版本中均起到了作用人与过程的故事。故事涵盖了每个版本的目标，以及他们如何解决 JavaScript 开发社区不断变化的需求。本部分探究在每个版本中对语言进行的重大基础更改以及重要的新内容语言中添加的功能。

本文件的原始资料尽可能是当时的原始文献。幸运的是，这些资料非常丰富。作者确保了几乎所有的原始文件都可以通过参考文献中的网址从可靠的 archives 免费和方便地在网上查阅。主要文献资料来源还辅以与一些直接参与报道的人的访谈和个人通信。两位作者都是本文所涉及的许多事件的重要参与者。他们的回忆与其他信息提供者的回忆相似。

JavaScript 的完整二十年的故事很长，本文也是如此。它设计了数百个不同的时间以及数十个个人和组织。提供附录 A 到 E 列出了这些详细信息。附录 A 和附录 B 提供了故事中出现的人物和组织的名单。附录 C 是一个词汇表，其中包含了 JavaScript 独有的术语和在 2020 年的含义可能与计算机界的通用用法不同、含义可能会发生变化或者对未来的读者来说可能会变得陌生的一些术语。

在本文中，术语的首次使用通常用斜体字，并以 "g "上标，如： "term." 附录 D 定义了读者会遇到的缩略语。附录 E 包含四个详细的事件时间轴，本文的四个部分各有一个。

### 1.1 名称，版本和缩写

在 js 的世界里，多个名称代表着相同的事物，这让人感到疑惑。在标准制定组织的世界里，这种情况就更加严重了，因为这些组织经常使用两个和三个字母的缩写和数字来标识其组织单位和工作产出。为了尽量减少这种混乱，我们将首先对其中的一些名称和缩写进行定义，并确定一些在本文其余部分中使用的惯例。

"Javascript"是最初由 Netscape 开发、用在 web 页面中编程语言的通用名称。它在网页和其他环境中大量使用，远远超过了最初的范围，现在每天都有成千上万的程序员使用 JavaScript 来谈论这种语言。js 与 java 在技术上面讲完全不同，但他们名字的相似造成人们经常对其感到迷惑。

JavaScript® 也是一个注册商标。这个商标最初是 Sun Microsystems 注册的，现在归 Oracle Corporation 所有。Sun 将该商标授权给 Netscape，然后又授权给 Mozilla Foundation。Netscape 和 Mozilla 使用“ JavaScript 1.4”之类的名称来描述其实现的特定版本。有些版本的实现也是用其他的名字来避免版权问题。由于名称过多，版权问题和与 java 关系的迷惑性。许多用户，作者和工具的开发者都将语言称为"JS"，".js"也被用作 Javascript 源码的文件扩展名。在本文中，在没有特定的诸如版本，环境和实现等上下文的情况下，我们使用非限定词"Javascript"来讨论该语言以及它的用法。

在为语言制定规范时，避免了使用"Javascript"一词。该规范使用的是"ECMAScript"。"Javascript"和"ECMAScript"基本上是同一事物的不同名字。在本文中，当我们使用术语"ECMAScript"时，专门指标准定义的语言。

"ECMASCript"中的"ECMA"部分源自瑞士标准组织 Ecma International，该组织主持了语言标准的制定。"ECMA"原本是 European Computer Manufacturers Association（欧洲计算机制造商协会）的缩写，该协会后来演变为 Ecma International 组织。该组织现在不再把"Ecma"当作首字母缩写词，仅仅把"Ecma"中的"E"大写。但在过去，它们使用全大写字母。ECMAScript 最初的制定是在这种情况下，因此存在五个大写字母。在本文中，我们使用单词"Ecma"通常是指 Ecma 国际标准化组织。

Ecma 制定了许多与计算相关的标准。制定标准的实际工作是在 Ecma 技术委员会（简称 "TC"）内进行的。当创建一个新的 Ecma TC 时，它被分配了一个序列号来唯一标识它。TC39 是为规范 JavaScript 而创建的 TC。一些 Ecma 的 TC 被细分为任务组，简称为 "TG"，有特定的职责。从 2000 年到 2007 年，TC39 的职责范围扩大到了除 JavaScript 之外的其他编程语言。在这期间，ECMAScript 的责任被分配给了 TC39-TG1。本文中，我们用 "TG1 "作为 TC39-TG1 的缩写。

ECMAScript 标准被指定为 "ECMA-262"。当一个标准修订后，新的版本会用相同的版本号作为后缀。例如，ECMAScript 标准的第三版正式名称为 "ECMA-262，第三版"。在 TC39 内部，以及最终在更广泛的 JavaScript 社区中，形成了一个惯例，即使用 "ES3 "这样的缩写作为正式版本的缩写，"ES "代表 "ECMAScript"。表 1 列出了 ECMA-262g 的版本以及本文所使用的缩略词。

| 缩写           | 版本 | 日期             | 项目编辑                           | 页数 |
| :------------- | :--- | :--------------- | :--------------------------------- | :--- |
| ES1            | 1st  | 1997.6           | Guy Steele                         | 95   |
| ES2            | 2nd  | 1998.8           | Mike Cowlishaw                     | 101  |
| ES3            | 3rd  | 1999.12          | Mike Cowlishaw                     | 172  |
| ES3.1          | 5th  | 第五版的内部名称 |                                    |      |
| ES4_1 and ES42 | 4th  | 废弃，未完成     |                                    |      |
| ES5            | 5th  | 1999.12          | Pratap Lakshman, Allen Wirfs-Brock | 245  |
| ES5.1          | 5.1  | 2011.6           | Allen Wirfs-Brock                  | 245  |
| ES6 or ES2015  | 6th  | 2015.6           | Allen Wirfs-Brock                  | 545  |
| ES2016         | 7th  | 2016.6           | Brian Terlson                      | 546  |

制定第 4 版规范的尝试历时近 10 年，由两项基本独立的设计工作组成。在本文中，"ES4_1"和 "ES4_2"分别指这两个成果，ES4 是指为创建第 4 版的总体努力。

从第 6 版出版开始，TC39 采用了以出版年份作为缩写的惯例。因此，"ES6"和 "ES2015"都是 "ECMA-262，第 6 版"的非正式缩写，但以 "ES2015 "为首选。但是，在第 6 版的制定过程中，"ES6"是最常用的缩写。TC39 成员还使用 "Harmony"和 "ES next"作为代号来指代第 6 版开发项目。

本文使用大量的内联代码片段来说明 JavaScript 的概念。其中一些代码片段只适用于特定版本的 JavaScript/ECMAScript，一些片段说明了从未成为语言的一部分的拟议特性。在本文中，不是对所有版本的 JavaScript/ECMAScript 都有效的片段都会被标注出来。
