# IntelliJ IDEA 安装目录的核心文件讲解

首先，我们回顾一下前两篇关于 IntelliJ IDEA 的博文的内容：

 - 在「[在 Windows 系统下安装 IntelliJ IDEA  的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/basic-course/install-intellij-idea-on-windows.md)」中，我们知道了在 Windows 系统下如何下载并安装 IntelliJ IDEA 的方法；
 - 在「[首次运行 IntelliJ IDEA  示例](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/basic-course/first-run-idea.md)」中，我们体验了首次运行 IntelliJ IDEA 的向导功能，并完成了初步的配置。

在本篇博文中，我们主要讲解一下 IntelliJ IDEA 安装目录中的一些核心文件的功能及用法：

![intellij-idea-bin](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/core-file-talk/intellij-idea-bin.png)

如上图所示，我们定位到了 IntelliJ IDEA 安装目录的`bin`目录下，`bin`是 binary 的缩写，代表的意思是二进制，因此`bin`目录就是用来存放二进制文件的。在这里，我们主要了解上图中被红色方框圈出来的五个文件：

 - `idea.exe`文件是 IntelliJ IDEA 32 位的可行执行文件，IntelliJ IDEA  安装完默认发送到桌面的就是这个执行文件的快捷方式；
 - `idea.exe.vmoptions`文件是 IntelliJ IDEA 32 位的可执行文件的 VM 配置文件；
 - `idea.properties`文件是 IntelliJ IDEA 的一些属性配置文件；
 - `idea64.exe`文件是 IntelliJ IDEA 64 位的可行执行文件，要求电脑上必须装有 JDK 64 位版本，64 位的系统也是建议使用该文件；
 - `idea64.exe.vmoptions`文件是 IntelliJ IDEA 64 位的可执行文件的 VM 配置文件。

接下来，我们详细了解上述配置文件的作用：

![idea64-vmoptions](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/core-file-talk/idea64-vmoptions.png)

如上图所示，我们打开了`idea64.exe.vmoptions`配置文件。如果我们的电脑是 32 位系统，则应该打开`idea.exe.vmoptions`配置文件，但是由于 32 位系统内存一般都是 2G 左右，也没有多大空间可以调整，所以一般不需要修改。修改 JVM 配置文件的原则就是根据我们机器的内存情况来判断，个人建议 8G 以下的机器或是静态页面开发者无需修改，如果我们要开发大型的 Java 项目或是 Android 项目，并且内存大于 8G，建议进行修改，而且经常修改的也就是下面 4 个参数。在此处，我们以 16G 内存的机器为例：

 - `-Xms128m`，可尝试设置为`-Xms512m`
 - `-Xmx750m`，可尝试设置为`-Xmx1500m`
 - `-XX:ReservedCodeCacheSize=240m`，可尝试设置为`-XX:ReservedCodeCacheSize=500m`
 - `-XX:SoftRefLRUPolicyMSPerMB=50` ，可尝试设置为`-XX:SoftRefLRUPolicyMSPerMB=100`


在这里，我们只是举个修改示例，由于每台机器的配置不一样，因此每台机器的最佳的配置参数也是不一样的，最好的调整方式是根据 JConsole 这类工具进行观察后个性化调整。

![idea-properties](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/core-file-talk/idea-properties.png)

如上图所示，我们打开了`idea.properties`配置文件，其没有 32 位和 64 位之分，修改的原则主要是根据个人对 IntelliJ IDEA 的个性化配置情况来分析，经常修改的是下面 4 个参数：

 - `idea.config.path=${user.home}/.IntelliJIdea/config`，该属性主要用于指向 IntelliJ IDEA 的个性化配置目录，默认是被注释，打开注释之后才算启用该属性，这里需要特别注意的是斜杠方向，这里用的是正斜杠；
 - `idea.system.path=${user.home}/.IntelliJIdea/system`，该属性主要用于指向 IntelliJ IDEA 的系统文件目录，默认是被注释，打开注释之后才算启用该属性，这里需要特别注意的是斜杠方向，这里用的是正斜杠，如果咱们的项目很多，则该目录会很大，如果咱们的 C 盘空间不够的时候，还是建议把该目录转移到其他盘中；
 - `idea.max.intellisense.filesize=2500`，该属性主要用于提高在编辑大文件时候的代码帮助，IntelliJ IDEA 在编辑大文件的时候还是很容易卡顿的；
 - `idea.cycle.buffer.size=1024`，该属性主要用于控制控制台输出缓存。如果遇到项目开启很多输出的话，那么控制台很快就被刷满了，没办法再自动输出后面内容，这种项目建议增大该值或是直接禁用掉，禁用语句为 `idea.cycle.buffer.size=disabled`。

由于屏幕大小的关系，上面所示的配置文件的内容并没有显示完全，我们只需要滑动鼠标就可以看到上面我们经常修改的配置信息啦！至此，IntelliJ IDEA 安装目录的核心文件讲解完毕。


----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
