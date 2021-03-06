# Building Abstractions with Procedures

> 心灵，从三个方面对知识施加影响：
>
> 1. 组合，对简单的知识进行组合，从而产生复杂的；
> 2. 对比，将简单或复杂的知识进行对比，从而产生关系的；
> 3. 抽象，将知识从现实中与其相关的其它知识分离，从而产生一般的。
>
> John Locke, An Essay Concerning Human Understanding (1690)

我们将要学习计算过程。计算过程是栖息在计算机中的抽象存在，随着它们的演化，其可以操纵称为数据的抽象事物。而具有一定规则的程序能够指引过程的演化，因此编程者创建程序来描述过程，实际上，我们就是使用这种“咒语”来召唤计算机中的灵魂。

计算过程，同巫师对于灵魂的看法极为相像，不可视，不可触，没有形体。但是，它却很是真实，它可以思考，可以回答问题，可以通过如付钱，控制工厂中的机械臂等影响世界。我们用来召唤过程的程序如同巫师的咒语，咒语的组合产生了魔法，晦涩难懂的编程语言中的符号表达式的组合就描述了我们想要执行的任务。

计算过程，在工作正常的计算机中，可以准确的执行程序。因此，新手程序员就像魔法师的学徒一样，必须学会理解和预测召唤的结果，即使是程序中的小错误(常称为 bugs 或故障)也可能会产生复杂且无法预料的后果。

幸运的是，计算机中的灵魂很容易控制，因此学习编程比学习巫术要安全许多。但是，现实世界的编程任务需要细心、专业和智慧，例如计算机辅助程序中的小错误甚至可能会导致飞机的毁灭、大坝的倒塌或工业机器人的自毁。

高级软件工程师具备组织程序的能力，能够确定程序生成的过程将执行预期的任务。他们可以确定系统的行为，他们知晓如何构建程序，即使出现意料之外的问题，也不会导致灾难性后果，当问题出现时，他们也能调试程序。设计良好的计算机系统，如同设计良好的汽车或核反应堆，需要进行模块化处理，以使每个部分可以单独构建、更替和调试。

## 在 Lisp 中编程

我们需要一门合适的语言描述计算过程，为此我们将使用编程语言 Lisp。正如使用自然语言(如英语、法语或日语)对日常所思所想进行表达，使用数学符号对定量现象进行描述，我们使用 Lisp 表达计算过程。Lisp 作为计算模型，发明于 1950 年代后期，主要用于分析推理递归逻辑表达式。该语言由 John McCarthy 构思，并基于其论文 _Recursive Functions of Symbolic Expressions and Their Computation by Machine_ 进行了实现。

尽管 Lisp 最初表达为数学形式，但它仍是一种实用的编程语言。Lisp 解释器用于解释执行 Lisp 语言描述的过程。
