# HelloWorld 项目创建及相关配置文件介绍

在博文「[IntelliJ IDEA 的使用界面介绍](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/basic-course/use-face.md)」中，我们通过创建一个 Static Web 项目大致了解了 IntelliJ IDEA 的使用界面。接下来，趁着这个热乎劲，我们来创建第一个 Java 项目`HelloWorld`，进入如下界面：

![welcome-to-idea](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/welcome-to-idea.png)

如上图所示，点击`Create New Project`，进入如下界面：

![new-project](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/new-project.png)

上面的界面，我们在前一篇博文中已经进行了介绍。在这里，我们选择`Java --> Java EE`进行项目的创建，然后着重看一下第一个红色箭头所指的`Project SDK`，其表示在接下来我们的项目中所使用的 SDK，要想进行设置，这就需要我们在事先下载好 JDK 啦！那么如何下载并安装 JDK 呢？不用怕，在博文「[在 Win10 系统下安装 JDK 及配置环境变量的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/install-jdk-win10.md)」中，我们已经演示了具体的操作过程了，以 Win10 为例，Win7 同理。接下来，点击`Project SDK`后面的`New`进行 JDK 的设置：

![select-home-directory-for-jdk](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/select-home-directory-for-jdk.png)

如上图所示，IntelliJ IDEA 默认选择其自带的 JRE，我们选择事先下载好的 JDK，如下图所示：

![select-home-directory-for-jdk-2](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/select-home-directory-for-jdk-2.png)

如上图所示，我们只需要定位到`jdk 1.8.0_121`这层目录即可，然后点击`OK`确定：

![new-project-next](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/new-project-next.png)

如上图所示，展示了选择 JDK 后的样子，点击`Next`，进入下一步：

![create-project-from-template](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/create-project-from-template.png)

 - **标注 1**：`Command Line App`会自动创建一个带有`main`方法的类；
 - **标注 2**：`Java Hello World`会自动创建一个带有`main`方法的并且会打印输出 Hello World 的类。

如上图所示，可以选择`Create project from template`快速创建项目，在这里，咱们不勾选使用模板，手工创建，点击`Next`，进入如下界面：

![new-project-finish](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/new-project-finish.png)

如上图所示，输入项目名称，也不需要修改`More Settings`，直接点击`Finish`，进入如下界面：

![hello-world](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/hello-world.png)

 - **标注 1**：项目结构图；
 - **标注 2**：外部库。

如上图所示，在项目结构图中，`src`目录为默认的`Source root`，我们一般在该目录下创建包和类；在外部库中，显示了我们导入的 JDK 1.8 版本。接下来，我们在`src`目录下创建包和类：

![new-package](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/new-package.png)

如上图所示，将鼠标移动到`src`目录上，然后点击右键，选择`New`，再选择`Package`，创建包：

![com-hit-demo](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/com-hit-demo.png)

如上图所示，我们输入包名为`com.hit.demo`，其中用英文状态下的点`.`进行分隔，表示一次创建多个包，具体效果如下图所示：

![hide-empty-middle-package](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/hide-empty-middle-package.png)

 - **标注 1**：多个空包叠在一起；
 - **标注 2**：齿轮符号，一般表示设置；
 - **标注 3**：选择是否把空包叠在一起。

如上图所示，我们创建的多个空包默认是重叠在一起的，如果其中某个包非空，则自动拆开包。在这里，如果感觉空包叠在一起不爽的话，可以点击 **标注 2** 所示的齿轮按钮，再点击 **标注 3** 所示的`Hide Empty Middle Packages`把对勾去掉，变为`Compact Empty Middle Packages`，其效果如下图所示：

![compact-empty-middle-packge](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/compact-empty-middle-packge.png)

接下来，选择`demo`目录，点击鼠标右边，在选择`Java Class`，进入如下界面：

![create-new-class](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/create-new-class.png)

如上图所示，将类名（`Name`） 设置为`HelloWorld`，一般情况下，如果类名出现多个单词的话，则每个单词的首字母都大写。类创建完之后，在编辑区敲入代码，如下图所示：

![hello-world-class](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/hello-world-class.png)

接下来，在“编辑区”点击鼠标右键，选择`Run 'HelloWorld.main()'`，运行后，结果如下图所示：

![hello-world-go-go](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/hello-world-go-go.png)

 - **标注 1**：运行结果“HelloWorld！”
 - **标注 2**：存放`Module`编译文件的`out`目录。

在这里，对于 **标注 1** 所示的内容，毫无疑问，其为在控制台上的输出语句；对于 **标注 2** 所示的内容，则需要我们留心啦，其存放的是项目中所有`Module`的编译文件。如果我们细心一点的话，则会发现`out`和`src`目录的层次结构完全相同。最后，我们在来了解一下项目中的相关配置文件，如下图所示：

![idea-iml](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/hello-world/idea-iml.png)

 - **标注 1**：`.idea`为`Project`的配置文件目录；
 - **标注 2**：`.iml`为`Module`的配置文件。

如上图所示，IntelliJ IDEA 的配置文件都存在`.idea`目录下，以 XML 文件的形式存在，因此我们也可以通过了解这些 XML 文件来了解 IntelliJ IDEA 的相关配置。至于`.iml`文件，则为 IntelliJ IDEA 为每个 Module 自动生成的配置文件，一般情况下，我们是不需要动她的，就让她做一个安静的女神吧！**此外，IntelliJ IDEA 是一个没有 Ctrl + S 的 IDE，因此每次修改完代码之后，咱们只管运行或者调试即可，无需担心保存或者丢失代码的问题。**



----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————









