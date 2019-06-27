# IntelliJ IDEA 缓存和索引的介绍及清理方法

在博文「[详述 IntelliJ IDEA 的使用界面](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/basic-course/use-face.md)」中，博主说过这样一句话“**对于首次创建或打开的新项目，IntelliJ IDEA 都会创建项目索引，大型项目在创建索引的过程中可能会出现卡顿的现象，因此强烈建议在 IntelliJ IDEA 创建索引的过程中不要动项目**。”那么，索引到底是干什么用的呢？在本篇博文中，就让我们一起了解索引的用途，对了，还有缓存。

IntelliJ IDEA 的缓存和索引主要是用来加快文件查询的速度，从而提高各种查找、代码提示等操作的速度，因此索引对 IntelliJ IDEA 的高效性来说，具有至关重要的作用。但是，IntelliJ IDEA 的缓存和索引并不一定总是起到积极的作用，有的时候，反而会因为缓存和索引的损坏，例如突然断电、蓝屏引起的强制关机等等，造成 IntelliJ IDEA 出现一些莫名其妙的问题，例如项目打不开、个性化设置还原等等。现在，大家不用愁了，接下来，就让我们一起看一看如何清理缓存和索引：

![file-caches-restart](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/index-and-cache/file-caches-restart.png)

如上图所示，`File`下的`Invalidate Caches / Restart`就是清理缓存和索引的入口，表示“**无效缓存或者重新启动**”，点击进入如下界面：

![warning](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/index-and-cache/warning.png)

 - **标注 1**：无效并重启；
 - **标注 2**：无效缓存；
 - **标注 3**：重新启动；
 - **标注 4**：警告提示。

如上图所示，一般建议点击` Invalidate and Restart`，这样会清理的比较干净。但是，有一点需要注意，那就是：**标记 4** 所示的`WARNING`表示如果我们选择清理缓存和索引，那么 IntelliJ IDEA 的`Local History`也会被一并清理掉。因此，如果我们的项目没有加入到版本控制，而我们又需要项目文件的历史更改记录，那最好备份下该目录，其地址为`C:\Users\当前登录的系统用户名\\.IntelliJIdea\system\LocalHistory`。

通过上面的方式清除缓存和索引的本质其实就是删除`C`盘下的`system`目录下的对应的文件，因此如果我们不用上述的方法，也可以直接删除整个`system`目录，这样的话，当 IntelliJ IDEA 再次启动项目的时候就会重新创建新的`system`目录以及对应项目缓存和索引。如果我们遇到了因为缓存或者索引出现问题以至于打不开项目的时候，建议直接删除`system`目录，一般这样都可以很好地解决我们的问题。

此外，还有一点需要我们注意，那就是：**在安装 IntelliJ IDEA 的时候，默认是不启用`system`目录的，因此想要记录`Local History`，就得我们手动设置啦**！具体如何设置，可以参考「[IntelliJ IDEA 安装目录的核心文件讲解](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/core-file-talk.md)」这篇文章。



----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————

