# IntelliJ IDEA 控制台输出中文乱码问题的解决方法

首先，找到 IntelliJ IDEA 的安装目录，进入`bin`目录下，定位到`idea.vmoptions`文件，如下图所示：

![bin](http://img.blog.csdn.net/20170209210349535)

双击打开`idea.vmoptions`文件：

![idea](http://img.blog.csdn.net/20170209210440395)

然后，在其中追加`-Dfile.encoding=UTF-8`代码：

![追加](http://img.blog.csdn.net/20170209210610302)

最后，在 IntelliJ IDEA 中的“Run/Debug Configurations”中，修改虚拟机参数“ VM  options ”，内容与在文件`idea.vmoptions`中追加的内容相同，皆为`-Dfile.encoding=UTF-8`，具体如下图所示：

![修改参数](http://img.blog.csdn.net/20170209210834318)

到这里，IntelliJ IDEA 控制台输出中文乱码的问题就得到解决啦！



----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/cg-blog/blob/master/README.md) —— ☆☆☆ ————
