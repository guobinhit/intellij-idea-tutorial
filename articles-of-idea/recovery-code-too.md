# 详述 IntelliJ IDEA 中恢复代码的方法「进阶篇」

在博文“ [详述 IntelliJ IDEA 中恢复代码的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/recovery-code.md) ”中，咱们已经了解了如何将代码恢复至某一版本，但是通过`Local History`恢复代码有的时候并不方便，例如咱们将项目中的代码进行了多处修改，这时通过`Local History`恢复代码就显得很麻烦，因为它更倾向于恢复某一个文件的修改。

因此，如果咱们的项目是通过`Subversion`也就是`SVN`检出的，那么咱们就多了一种恢复代码的方法，即通过`Subversion`进行`Revert`操作。

**操作步骤：**

![1](http://img.blog.csdn.net/20170417114820755)

 - 标注1：项目名称
 - 标注2：Subversion 
 - 标注3：Revert

如上图所示，先鼠标右键点击项目名称，然后选择`Subversion`，再选择`Revert`，即可进行选择恢复代码的页面。

但是，在这里有一点需要咱们注意，那就是：**此`Revert`为直接将代码恢复至从`SVN`检出时的状态，需谨慎使用**。


----------

**温馨提示**：不要纠结于为啥上图中的`Revert`为灰色，因为这个项目根本就不是从`SVN`上检出的，而且也没有进行过任何的修改。

----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
