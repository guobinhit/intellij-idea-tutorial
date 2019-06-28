# 详述  IntelliJ IDEA 提交代码前的 Code Analysis 机制

在我们用 IntelliJ IDEA 向 SVN 或者 Git 提交代码的时候，IntelliJ IDEA 提供了一个自动分析代码的功能，即`Perform code analysis`： 

![subversion](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/code-analysis/subversion.png)

如上图所示，当我们勾选`Perform code analysis`之后，点击`commit`，IntelliJ IDEA 就会在提交代码之前对项目的代码进行分析检查，并将检查结果以错误和警告的形式展示出来：

![code-analysis](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/code-analysis/code-analysis.png)

如上图所示，这是`Code Analysis`的结果示例，为`No errors and 6 warnings`. 如果我们想进一步查看`Code Analysis`的结果，即`errors`和`warnings`的详情，可以点击`Review`，点击`Review`之后， IntelliJ IDEA 会展示出一系列具体发生错误和警告的类及位置，这有助于我们解决问题。

在这里，有一点需要着重说明，那就是：**IntelliJ IDEA 的`Code Analysis`机制比较敏感，就算我们在文本注释中用错了标签或者注释时方法的参数与实际参数不一致，在`Code Analysis`的时候，都会以错误和警告的形式给出**。因此我们常常会遇到这样的情况，就算代码中一点错误（提示）都没有（至少看起来是这样，没有飘红啊），当我们提交代码并进行`Code Analysis`的时候，仍然会收到一大堆的错误和警告提示，虽然这些错误和警告并不影响代码的运行。

此外，在我们提交代码之前和之后都可以利用 IntelliJ IDEA 的自动化机制执行一些操作，例如勾选：

 - `Reformat code`，提交代码之前对代码进行格式化；
 - `Optimize imports`，提交代码之前对代码进行导入包的优化；
 - `Upload files`，提交代码之后上传文件。
 - ……

IntelliJ IDEA 还有很多功能等待我们去探索，接触的越多，我们越能发现她的优雅。 

----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](http://blog.csdn.net/qq_35246620/article/details/61191375) —— ☆☆☆ ————
