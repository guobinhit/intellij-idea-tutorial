# IntelliJ IDEA 常见文件类型的图标介绍

在之前的「[史上最简单的 IntelliJ IDEA 教程](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md)」系列博文中，我们已经了解了很多关于 IntelliJ IDEA 的内容啦，例如，在 Windows 系统下安装  IntelliJ IDEA、运行  IntelliJ IDEA 、创建 Java 项目以及修改  IntelliJ IDEA  主题等等，可以说，我们已经初步掌握了 IntelliJ IDEA 的使用方法啦！不过，有一个现象不知道大家注意到没有，那就是：**在我们使用 IntelliJ IDEA 创建文件的时候， 随着文件类型的不同，其显示的图标也不相同。**例如，我们分别创建`Java`、`Interface`、`Enum`和`JavaScript`文件，如下图所示：

![icons](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/icons.png)

如上图所示，显然不同的文件类型，其显示的图标也不相同。为了能够更好的掌握 IntelliJ IDEA，在这里，我们更进一步，了解一下  IntelliJ IDEA 各种文件类型的图标，主要分为三类：`Common`、`Data Sources`和`File Types`.

> **Common**

![common-1](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/common-1.png)
![common-2](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/common-2.png)
![common-3](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/common-3.png)

> **Data Sources**

![data-sources-1](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/data-sources-1.png)
![data-sources-2](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/data-sources-2.png)
![data-sources-3](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/data-sources-3.png)

> **File Types**

IntelliJ IDEA 识别众多的文件类型，每一个文件类型都用一个特殊图标表示，也允许自定义的文件类型。每个文件类型与一个或多个特定的模式进行关联扩展。文件类型及其扩展可以在文件类型的对话框中进行配置。默认的文件类型包括：

![file-types-1](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/file-types-1.png)
![file-types-2](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/file-types-2.png)
![file-types-3](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/file-types-3.png)
![file-types-4](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/file-types-4.png)
![file-types-5](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/file-types-5.png)
![file-types-6](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/file-types-6.png)
![file-types-7](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/file-types-7.png)

对于各种文件类型的图标，上面的`Description`已经介绍的非常详细啦，但是还有两个图标需要特别的说明一下，分别为：

 - ![tiny-1](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/tiny-1.png)`Source root`，我们可以理解为源目录，其作用就是用来专门存放 Java 类文件的，相对于编译出来的`class`文件而言，它就是源。一般默认名字叫`src`的目录就是源目录，但是在 IntelliJ IDEA 中，即使叫`srcs`也是可以设置为`Source root`的，所以源目录跟目录命名是没有关系的，因为 IntelliJ IDEA 支持将任意目录设置为`Source root`，其作用就是标记该目录下的文件是可编译的。
 - ![tiny-2](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/idea-icon/tiny-2.png)`Java class located out of the source root`，我们已经知道`Source root`目录是用来告诉 IntelliJ IDEA 这是存放可编译文件的目录，而如果我们的 Java 类文件没有放在该目录或是该目录的子包下，那么该 Java 类文件就无法进行编译，其前面就会显示这个图标。
 

----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
