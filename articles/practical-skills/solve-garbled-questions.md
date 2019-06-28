# IntelliJ IDEA 控制台输出中文乱码问题的解决方法

首先，找到 IntelliJ IDEA 的安装目录，进入`bin`目录下，定位到`idea.vmoptions`文件，如下图所示：

![idea-bin](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/solve-garbled-questions/idea-bin.png)

双击打开`idea.vmoptions`文件，如下图所示：

![idea-vmoptions](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/solve-garbled-questions/idea-vmoptions.png)

然后，在其中追加`-Dfile.encoding=UTF-8`代码，如下图所示：

![edit-idea-vmoptions](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/solve-garbled-questions/edit-idea-vmoptions.png)

最后，在 IntelliJ IDEA 中的`Run/Debug Configurations`中，修改虚拟机参数`VM  options`，内容与在文件`idea.vmoptions`中追加的内容相同，皆为`-Dfile.encoding=UTF-8`，具体如下图所示：

![configurations](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/solve-garbled-questions/configurations.png)

到这里，IntelliJ IDEA 控制台输出中文乱码的问题就得到解决啦！



----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
