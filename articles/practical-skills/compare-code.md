# 利用 IntelliJ IDEA 进行代码对比的方法

Sometimes，我们会有这样的需求，即：**想对比出两个不同版本代码的区别**。如何实现？

 - **第 1 种**：如果我们是从 SVN 检出的项目，并且想比较本地代码与从 SVN 检出时的代码相比都有那些区别，可以按如下步骤操作，

![show-history](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/compare-code/show-history.png)

如上图所示，在代码编辑区，`右键`唤出功能菜单，然后选择`Subversion`，进而会展示出更多的可选项，例如：

- `Compare with the Same Repository Version`，与 SVN 仓库相同版本做对比；
- `Compare with Latest Repository Version`，与 SVN 仓库最新版本做对比；
- `Compare with...`，点击后选择本分支的不同版本做对比；
- `Compare with Branch`，点击后需要先配置具体要对比的分支，然后与指定分支做比对；
- `Show History`，同`Compare with...`类似，只不过是先展示出此分支的版本历史。

通过上述方法，已经可以满足我们比较线上分支代码的需求啦！

- **第 2 种**：比较本地两份代码的区别，可以按如下步骤操作，

![compare-with](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/compare-code/compare-with.png)

首先，选中目标文件夹（图中选择`src`文件夹），`右键`唤出功能菜单，然后点击`Compare With`：

![local-project](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/compare-code/local-project.png)

如上图所示，选中本地另一份想要与之对比的代码的相同目录，然后点击`Open`或者`打开`、`确定`按钮：

![show-diff](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/compare-code/show-diff.png)

如上图所示，清晰明了的展示了两份代码的区别。

----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
