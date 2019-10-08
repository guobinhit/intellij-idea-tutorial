# 详述 IntelliJ IDEA 版本控制不显示颜色提示的解决方法

在使用 IntelliJ IDEA  版本控制功能的时候，有一个功能点特别好，那就是对于新增文件或者修改文件，IDEA 会给出颜色提示，以区分文件类型，如新增、修改或者未加入版本控制。但偶尔会出现导入新`check out`到本地的项目的时候，不显示颜色提示的问题！

![new-node](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/version-control-color-tips/new-node.png)

如上图所示，这是一个基于 Git 进行版本控制的名为`leetcodes`的项目。我们新建了一个名为`NewNode`的类文件，但是未显示任何颜色提示，以区分新增文件和原有文件的区别，即是否与远程仓库中的文件版本一致。现在，我们就来解决这个问题。

![preferences](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/version-control-color-tips/preferences.png)

如上图所示，以 Mac 版本的 IDEA 为例，点击`ItelliJ IDEA -> Preferences`按钮。

![version-control](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/version-control-color-tips/version-control.png)

- **标注 1**：`Version Control`，版本控制按钮；
- **标注 2**：未注册的项目根路径；
- **标注 3**：`Add`，新增按钮，即注册版本控制；
- **标注 4**：`Apply`，应用设置按钮。

如上图所示，进入`Preferences`页面，按顺序点击 **标注 1 ~ 4**，将未出注册到版本控制的项目根路径注册到 IDEA 的版本控制中，即可解决本文所述的问题。

![success](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/version-control-color-tips/success.png)

如上图所示，IDEA 的版本控制提示已经启动。

特别地，在上述操作中，有可能出现`Schedule for Addition`的问题，详见「[此篇](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/practical-skills/schedule.md)」文章。


--------


———— ☆☆☆ —— 返回 -> [史上最简单的 IntelliJ IDEA 教程](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) <- 目录 —— ☆☆☆ ————
