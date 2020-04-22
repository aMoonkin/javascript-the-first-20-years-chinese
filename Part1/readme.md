# 第一部分 Javascript 的起源

## 2. 前言

万维网的概念和基础技术是 Tim Berners-Lee 1989–1991 年期间在 CERN（欧洲核子研究中心） 提出的。Berners-Lee 的网络技术在高能物理学界流传了几年。然而，这些技术并没有得到社区外的关注，直到 1992-1993 年，本科生 Marc Andreessen 和在伊利诺伊大学香槟分校国家超级计算应用中心（NCSA）工作的 Eric Bina 开发了 Mosaic，才在社区外引起了很大的关注。

NCSA Mosaic 是一个易于安装、易于使用的 Web 客户端，具有图形用户界面。它从根本上定义了 "网络浏览器 "这一软件类别，并在物理学界之外普及了万维网的概念。Mosaic 被广泛传播，到了 1994 年初，商业利益集团纷纷争先恐后地加入到浏览器的行列中来，要么拿 NCSA Mosaic 代码授权，要么从头开始开发受 Mosaic 启发的浏览器。Silicon Graphics 公司的创始人 Jim Clark，获得了风险投资资金，并招募了 Marc Andreessen 和 Eric Bina。1994 年 4 月，他们共同创立了这家公司，并最终命名为 Netscape 通讯公司。Netscape 公司的目标是取代 NCSA Mosaic 成为世界上最受欢迎的浏览器。它从零开始开发了一个类似于 Mosaic 的下一代增强型浏览器，并于 1994 年 10 月开始广泛发行。到 1995 年年初，Netscape Navigator 已经实现了最初的目标，并迅速取代了 Mosaic。

Tim Berners-Lee 的 Web 技术是围绕着使用声明性的 HTML 标记语言来描述文档作为网页的表现形式。与之相对的是，业界对使用脚本语言产生了相当大的兴趣，脚本语言使终端用户能够编排应用程序的操作。诸如 Office，Visual Basic 和 AppleScript 等语言并不是为了实现主应用程序的核心部分的复杂数据结构和算法组件，相反，它们为用户提供了一种以新奇的方式将这些应用组件粘合在一起的方法。随着 Netscape 扩大了万维网的受众范围，一个重要的问题是，是否应该以及如何将脚本集成到网页中。

### 2.1 Brendan Eich 加入 Netscape

Brendan Eich 1985 年硕士毕业于 UIUC 后，前往 Silicon Graphics, Inc 工作。他最初主要致力于 Unix 内核和网络层的工作。1992 年，他离开了 SGI 加入了 MicroUnity，一家资金雄厚的初创公司，开发视频媒体处理器。在这两家公司他都为支持内核和网络编程任务实现了小型特殊用途语言。在 MicroUnity 的时候，他还做了一些 GCC 编译器的工作。

1995 年初，Brendan Eich 被“来做浏览器中的 Scheme(一种语言)”口号所吸引，加入了网景公司。但当 Eich 于 1995 年 4 月 3 日加入网景公司时，他发现了他发现了复杂产品的时长和编程语言的解决方案。1994 年底，网景公司曾拒绝了微软的低价收购要约，此后，网景公司管理层期望通过微软的 "拥抱、扩展、扩展、消灭 "战略直接出击。在比尔-盖茨的直接领导下，微软很快就意识到，随着 Web 作为跨 OS 平台的崛起，其即将推出的专有墙面信息实用程序 Project Blackbird 将变得无关紧要。盖茨的“互联网浪潮”备忘录将微软从黑鸟重新推向了 Internet Explorer 和全套服务器产品，因为 Netscape 急于在相同的市场上争夺利益。

网络脚本语言的候选语言包括诸如 Scheme 的研究型语言、诸如 Prel, Python 和 Tcl 等基于 Unix 的使用语言和微软的 Visual Basic。Brendan Eich 曾期望在浏览器中实现 Scheme。但在 1995 年初，Sun Microsystems 公司为其尚未发布的 Java 语言开展了一场游击营销活动。Sun 和 Netscape 公司很快就达成了协议，将 Java 集成到 Netscape 2 中。Eich 回忆说，Marc Andreessen 在 Netscape 会议上提出的口号是 "Netscape 加 Java 会杀死 Windows"。1995 年 5 月 23 日，在 Sun 公司公开宣布 Java 的时候，Netscape 宣布有意授权 Sun 公司的 Java 技术在浏览器中使用。

由于商业利益和/或市场化时间的考虑，Netscape 内部迅速制定了战略，选择脚本语言，而没有选择 Scheme、Perl、Python、Tcl 和 Visual Basic。Netscape 和 Sun 公司的高级管理人员，特别是 Marc Andreessen 和 Sun 公司的 Bill Joy 认为唯一可行的方法是设计和实现一种“小语言”来补充 Java。

持怀疑态度的人在 Sun 占主导地位，而在 Netscape 也占了大多数，它们质疑是否需要一种更简单的脚本语言：Java 不适合脚本吗？是否有可能解释为什么两种语言比一种语言更好？Netscape 公司是否有必要的专业知识来创建一种新的语言。

第一种反对意见很容易被反驳。1995 年春天的时候，Java 还不是一门适合新手的语言。人们不得不将主程序的代码体封装在一个包中的类声明中的一个名为 main 的静态方法中。人们也不得不为所有参数、返回值和变量声明静态类型。基于 Visual BASIC 补充 Visual C ++的经验以及许多 Unix 语言补充基于原生代码(native-code-based)的组件的经验，很明显 Java 对于“胶水”脚本编写者来说还不够简单。

第二种反对意见通过引用微软的产品而被克服。对于专业的 Windows 应用程序员，微软提供了 Visual C++。对于业余爱好者、兼职程序员、设计师、会计师等，微软提供了 Visual Basic 作为脚本语言，让那些经验不足的兼职程序员可以用 Visual C++"粘合"在一起并定制使用 Visual C++构建的组件。Visual Basic 的一个名为 "Visual Basic for Applications "的版本被集成到微软的 Office 应用程序中，以支持用户扩展和编写这些应用程序的脚本。

在克服了前两个反对意见后，Marc Andreessen 提出了浏览器脚本语言的代号 "Mocha"，据 Eich 说，希望在适当的时候将该语言改名为 "JavaScript"。这种与 Java 相伴的语言必须 "看起来像 Java"，同时保持简单易用，"基于对象"，而不是像 Java 那样基于类。

最后的反对意见依然存在：Netscape 公司是否拥有创建有效的脚本语言的专业知识，并为 1995 年 9 月的 Netscape 2 测试版做好了准备？Brendan Eich 的任务是通过创建 Mocha 来证明他们们有这个能力。
