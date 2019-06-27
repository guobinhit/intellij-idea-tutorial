# 详述 IntelliJ IDEA 的使用界面

![welcome-idea](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/use-face/welcome-idea.png)

是否还记得在博文「[IntelliJ IDEA 安装目录的核心文件讲解](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/basic-course/first-run-idea.md)」中，这张充满神秘色彩的图片呢？进入她，让我们一起感受她的魅力吧！

![idea-begin](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/use-face/idea-begin.png)

如上图所示，打开 IntelliJ IDEA 后，首先迎接我们的就是这个界面：

 - **标注 1**：`Create New Project`创建一个新的项目；
 - **标注 2**：`Import Project`导入一个已有的项目；
 - **标注 3**： `Open`打开一个已有的项目；
 - **标注 4**：`Check out from Version Control`可以通过服务器上的项目地址 Checkout（俗称：检出） 项目。

在这里，为了进一步介绍 IntelliJ IDEA，我们创建一个 Static Web 项目，点击`Create New Project`，进入如下界面：

![new-project](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/use-face/new-project.png)

 - **标注 1**：IntelliJ IDEA 支持的框架及语言；
 - **标注 2**：与 **标注 1** 相对应的框架或语言的进一步分类。

在这里，我们选择`Static Web-->Static Web`，然后点击`Next`，进入下一步：

![new-project-2](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/use-face/new-project-2.png)

 - **标注 1**：项目名称（自定义，一般都小写，多个单词用下划线连接）；
 - **标注 2**：项目存储地址；
 - **标注 3**：模块名称（默认与项目名称相同）；
 - **标注 4**：内容根路径；
 - **标注 5**：模块文件存储地址；
 - **标注 6**：项目格式。

在这里，有一点需要说明，那就是：**在 IntelliJ IDEA 中，`Project`是最大单元，没有类似于  Eclipse 的工作空间（`Workspace`）的概念，但是我们可以在一个 `Project`下创建多个`Module`，默认是一个`Project`下创建一个`Module`，因此才出现项目名称与模块名称默认相同的现象**。一般情况下，我们是不需要在`More Settings `中进行修改的。接下来，点击`Finish`，完成项目的创建：

![project-go-go](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/use-face/project-go-go.png)

 - **标注 1**：项目结构图；
 - **标注 2**：在编辑区没有内容的时候，默认显示常用快捷键。

对于首次创建或打开的新项目，IntelliJ IDEA 都会创建项目索引，大型项目在创建索引的过程中可能会出现卡顿的现象，因此强烈建议在 IntelliJ IDEA 创建索引的过程中不要动项目。此外，IntelliJ IDEA 的默认界面是隐藏`Toolbar`和`Tool Buttons`的，博主比较喜欢把两者显示出来，大家可以按自己的个人爱好选择开启与否。但是无论我们是否选择开启，都要知道如何开启啊，省的在我们想开启的时候却不知道如何开启不是，那岂不是尴尬啦？因此，在这里，我们选择开启`Toolbar`和`Tool Buttons`，点击`View`，如下图所示：

![toolbar-toolbuttons](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/use-face/toolbar-toolbuttons.png)

如上图所示，`Toolbar`和`Tool Buttons`默认是没有选择的，我们分别点击`Toolbar`和`Tool Buttons`进行开启（出现对勾标记）：

![tool-show](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/use-face/tool-show.png)

 - **标注 1**：Toolbar
 - **标注 2**：Tool Buttons

如上图所示，`Toolbar`和`Tool Buttons`开启成功！至此，IntelliJ IDEA 的使用界面介绍完毕。


----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
