# 关于 IntelliJ IDEA 中 Schedule for Addition 的问题

在我们使用 IntelliJ IDEA 的时候，经常会遇到这种情况，即：

- 从 SVN 检出项目之后，并用 IDEA 首次打开项目，IDEA 会弹出如下选择框：


![schedule-open](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/schedule/schedule-open.png)

如上图所示，让我们选择是否将`XXX.iml`文件添加到 SVN 版本中。在这里，我们唯一有些疑惑的就是`XXX.iml`文件是什么鬼？在项目中，原本并就没有这个文件啊！实际上，`XXX.iml`文件是 IDEA 自动为我们（首次）打开的项目生成的配置文件，例如我们的项目名为`accounting-hessian`，那么 IDEA 就自动为我们的项目生产了一个名为`accounting-hessian.iml`的配置文件。

无论我们选择`No`还是`Yes`，IDEA 都会自动在项目中添加此配置文件，两者的区别就在于：如果我们选择`No`，那么在我们向 SVN 提交代码的时候，IDEA 在检索项目版本变更的时候会自动忽略此文件；如果我们选择`Yes`，那么在我们向 SVN 提交代码的时候，IDEA 会将其添加到项目的版本变更中。同理，当我们在项目中新建文件时，IDEA 也会弹出选择框：

![schedule-newfile](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/schedule/schedule-newfile.png)

如上图所示，当我们创建了一个名为`IdeaTest`的 Java 类的时候，IDEA 给出了同样的提示。当然，前提是我们并没有选择`Remember,don't ask again`，如果勾选了此内容，则不会再给出提示，并默认我们当时的选择。最后，我们尝试提交代码，测试 IDEA 的表现：

![commit-changes](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/schedule/commit-changes.png)

如上图所示，当我们对第一次弹框选择了`No`，对第二个弹框选择了`Yes`，则在提交代码的时候，IDEA 忽略了自动创建的`XXX.iml`文件，并将我们创建的`IdeaTest`包含进了项目的版本变更之中。此外，观察右下角的`New:1 Unversioned: 0 of 174`，我们也能看出来 IDEA 的检索结果，仅显示了一个`New`，即新建了一个文件。


----------

**温馨提示**：对于 IDEA 自动生成的`XXX.iml`配置文件，强烈建议不要随代码一起提交到 SVN！

