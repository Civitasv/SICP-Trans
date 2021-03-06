# 前言

教育家、将军、营养师、心理学家和父母在现实中编程。士兵、学生、社会在一定程度上被编程。解决大型问题时，常需要一系列程序，其中大部分用于处理该问题衍生的小问题，对于特定问题，程序也往往会出现各种状况。编程本身是一种智力活动，为领会其中的魅力，你必须进入计算机编程的领域，必须亲自阅读和编写计算机程序。需要清楚，程序是什么和服务于什么并不重要，重要的是当他们与其他程序结合构造更大规模程序时，执行的是否足够好，与其他程序是否能够很好的结合。因此，程序员必须在部分的完善与整体的融合之间寻求平衡。本书中， 程序设计关注于编写、执行、研究由 Lisp 方言编写的程序。使用 Lisp 不会限制或约束我们编程的内容，但需要遵循其特定的语法。

本书主题主要关于三个方面：人的思维方式、计算机程序集和计算机本身。计算机程序是模型，孵化于人脑相关进程，或真实、或虚构。这些产生于经验和思考的进程，数量庞大，细节错综复杂，难以被完全理解。因此，计算机程序难以完美的对其进行建模。即便程序是精雕细琢的离散符号集，相互交织的图案，他们依然会持续进化：随着对模型的理解更为深刻、更为广泛、更为一般化时，我们就对其进行修改完善，直到该模型在另一个模型中达到一个相对稳定的状态。计算机程序设计的乐趣，也就在于思维的不断拓展，在于使用计算机程序表达计算机相关机制和与之诞生的感知爆炸。如果说艺术诠释了我们的梦想，那么计算机就可以使用程序实现它们！

所谓能力越大，责任越大，计算机绝对是个苛刻的工头，其运行的程序必须完全正确，我们表述的必须准确无误。与其他符号学相同，我们通过论证验证程序的正确性。Lisp 本身具有语义(另一个模型)，如果程序具有特定的功能，比如说，在谓词演算中，可以用逻辑的证明方法作出可接受的正确性论证。不幸的是，随着程序愈来愈复杂(往往如此)，其充分性、一致性和准确性往往存疑，这也导致很难对大型程序进行完整的正确性逻辑论证。而大型程序往往从小程序发展而来，因此，开发一套标准的确保正确的程序代码库(称之为[[https://en.wikipedia.org/wiki/Programming_idiom][idiom]])，并使用经过验证的组织技术进行代码的复用和组合是至关重要的。本书详细介绍了这些技术，理解它们对于参与名为编程的“普罗米修斯事业”极为重要。发现并掌握强大的项目组织技术可以加速我们创建大型、重要项目的能力，相反的是，由于编写大型程序非常费力，我们应努力创造适合大型程序的新方法，以减少各种繁文缛节。

与程序不同的是，计算机必须遵循物理定律。计算机想要运行很快(状态变化在几纳秒内)，电子之间的传输距离必须很小(最大不超过 1.5 英尺)，同时，大量元件产生的热量也必须及时的得到散发。而在平衡功能的多样性与元件的密度之中，精湛的计算机工程艺术就一步步发展起来。无论如何，相比于我们编写的程序，硬件总是在更底层运行，事实上，将 Lisp 程序转换为机器码的过程本身也是一层抽象模型，对此过程的研究也为设计其他程序模型的组织技术提供了很多灵感。当然，计算机本身也可以按照这种思路进行建模，试想，计算机中物理开关元件的状态，由使用微分方程描述的量子力学建模而来；而其具体状态又由运行在计算机上的数值估计程序捕获；该计算机程序又由......

本书将讨论的主题分为人的思维方式、计算机程序集和计算机本身，不仅仅是为了“战术”上的便捷。尽管一切都存在于人类的思维之中，这种逻辑上的分离却可以加速三者符号之间的流动，也许只有生命本身的进化才能超越其丰富性、活力和可能性。在最好的情况下，三者之间的关系应是相对稳定的。计算机始终可以更大、更快，硬件技术的突破往往会导致更多编程企业的出现，新的程序组织原则的提出以及更多抽象模型的诞生。每一个读者应该时不时问自己一个问题：“到哪里才是终点，到哪里才是终点？”，但也不要思考的过于频繁，这会使你陷入苦乐参半的哲学泥淖，而丧失了编程的乐趣。

在我们编写的程序中，有一些(但还远远不够)用于执行准确的数学函数，例如排序、序列最大值、确定素数、求解平方根。我们将这些程序称之为算法，大量算法以具有最佳性能被熟知，其中两个重要的评价参数是时间复杂度和空间复杂度。程序员需要掌握好的算法和程序的常用俚语，尽管有些程序难以精确的描述，但程序员有责任去估计并且尝试改进他们的性能。

Lisp 是幸存者，这是一门已经被使用了 25 年的编程语言。在目前仍活跃的编程语言中，只有 Fortran 更为久远。二者均对程序的重要应用领域有很好的支持，Fortran 常被用于科学和工程计算领域，Lisp 则常应用于人工智能领域。这些领域一如既往的重要，而且有许多程序员十分热爱这两门语言，因此 Lisp 和 Fortran 很可能会被继续使用 25 年。

Lisp 在变化，本书使用的 Scheme 方言是从最初的 Lisp 演变而来的，但在如变量绑定的静态作用域和允许使用函数作为函数的返回值等方面与原始的 Lisp 有着很大的不同。与早期的 Lisp 相同，Scheme 的语义结构与 Algol 60 非常相似。Algol 60，作为一个过时的语言，存在于 Scheme 和 Pascal 的“基因”中。与萦绕在二者周围的编程语言相比，很难找到像 Scheme 和 Pascal 这样两种用于沟通差异如此巨大的文化之间的语言。Pascal 用于构建金字塔——大批人搬运重石，构建壮观的、雄伟的静态结构；Lisp 用于构建有机体——各个小队建造并安装无数动态的简单有机体，构建壮观的、雄伟的动态结构。二者使用的组织原则是相同的，但有一个十分重要的区别：Lisp 程序员所具有的可自由导出功能比 Pascal 程序员要强上不止一个数量级。Lisp 应用所产生的函数大大扩充了其函数库，事实上，这些函数的实用性在一定程度上超越了产生其的应用。Lisp 借由其原生数据结构 List 大幅度增长了函数的实用性，而如此简单和自然的数据结构，也使函数具有令人惊叹的普适性。但在 Pascal 中，数据结构的过度声明导致函数只能作用于特定的数据结构(唯一性)，这也使得函数之间难以良好的配合使用。使用 100 个函数操作一种数据结构要比使用 10 个函数操作 10 个数据结构要更好，结果，金字塔必须保持不变，有机体要么进化，要么死亡。

要想理清两种语言之间的差异，读者可以将本书中的材料和练习与其它使用 Pascal 的入门书籍进行比较。请不要认为本书只适用于 MIT，任何一本关于 Lisp 的编程书籍都应该像本书一样，适合于所有人。

本书与大部分用于人工智能工作的 Lisp 书籍不同，主要介绍程序的设计，毕竟，随着所研究层次的不断扩大，软件工程和人工智能所面临的关键问题将趋于统一。这也是相关人员对人工智能领域之外的 Lisp 愈来愈感兴趣的原因之一。

从人工智能的目标可以看出，其研究必然会产生许多重要的编程问题。在其它编程文化中，这一系列问题往往会催生出新的编程语言。诚然，发明语言，以控制和隔离任务模块之间的流通，是大型程序设计工作之中十分有用的方法。但当语言接近人类最常交互的系统的边界时，往往会更为高级，这就导致此类系统往往包含重复的复杂语言解析功能。而 Lisp 极其简单的语法和语义使得语言的解析任务十分容易，语言处理器的构建也从未成为大型 Lisp 系统发展的障碍。最后，Lisp 程序员的自由及负担，皆来源于此，凡是 Lisp 程序(除寥寥数行外)，无不充盈着各类函数。发明、组合，组合并重新发明！敬那些将思想写在层层括号之中的 Lisp 程序员。

Alan J. Perlis
New Haven, Connecticu

译者：古月有三木
