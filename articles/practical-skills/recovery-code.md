# 详述 IntelliJ IDEA 中恢复代码的方法

在我们日常开发项目的时候，难免遇到在开发过程中由于某种原因，想要将代码恢复到前一版本的情景。特别地，在我们删除了某些代码，想要恢复之前删除的代码的时候，了解这个在 IntelliJ IDEA 中恢复代码的方法就显得尤为重要啦！现在，以博主之前写的测试代码为例，进行详细的讲解：

![equalsAndHD](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/recovery-code/equalsAndHD.png)

如上图所示，这是博主之前写的测试恒等运算符和`equals()`区别的测试类。接下来，我们在这段代码中添加一条输出语句：

![equalsAndHD-system](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/recovery-code/equalsAndHD-system.png)

如上图所示，我们添加了一条输出`hello world`的代码。现在嘛，有这样一个场景，那就是：**要求我们仅输出`==`和`equal()`的区别即可，不需要添加额外的输出语句**。这就要求我们将代码恢复到之前的状态啦！在此忽略直接删除代码的方法，那该怎么办呢？

![local-show-history](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/recovery-code/local-show-history.png)

如上图所示，我们只需要选择对应的类文件，点击鼠标右键，然后依次选择`Local History`和`Show History`，进入如下界面：

![compare-history-current](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/recovery-code/compare-history-current.png)

如上图所示，最左边展示了版本记录，由于博主仅进行过这一次修改，因此这里只显示了`2 minutes ago`的版本记录；在往右看，依次展示了前一版本与当前版本的代码，并给出了区别，可谓是清晰简洁：

![revert](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/recovery-code/revert.png)

然后，选择我们想要恢复的版本，呃，好吧，现在我们仅有一个版本可以选择，点击鼠标右键，选择`Revert`：

![reverted-to-ago](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/recovery-code/reverted-to-ago.png)

如上图所示，当我们点击`Revert`之后，右侧的两个版本同步至“前一版本”，并给出了恢复提示。最后，我们再回到代码编辑区检查一下是否真的恢复到前一版本了呢？

![revert-result](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/recovery-code/revert-result.png)

如上图所示，显然我们的操作成功了，代码已经恢复至前一版本啦！But，通过`Local History`恢复代码有的时候并不方便，例如我们将项目中的代码进行了多处修改，这时通过`Local History`恢复代码就显得很麻烦，因为它更倾向于恢复某一个文件的修改。在这里，如果我们的项目是通过`Subversion`也就是`SVN`检出的，那么我们就多了一种恢复代码的方法，即通过`Subversion`进行`Revert`操作。

**操作步骤**：

![subversion](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/recovery-code/subversion.png)

 - **标注 1**：项目名称；
 - **标注 2**：`Subversion`；
 - **标注 3**：`Revert`.

如上图所示，先鼠标右键点击项目名称，然后选择`Subversion`，再选择`Revert`，即可进行选择恢复代码的页面。但是，在这里有一点需要我们注意，那就是：**此`Revert`为直接将代码恢复至从`SVN`检出时的状态，需谨慎使用**。


----------

**温馨提示**：不要纠结于为啥上图中的`Revert`为灰色，因为这个项目根本就不是从`SVN`上检出的，而且也没有进行过任何的修改。

----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
