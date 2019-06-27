# 详述 IntelliJ IDEA 创建 Maven 项目及设置 java 源目录的方法

Maven 是一个优秀的项目管理工具，它为我们提供了一个构建完整的生命周期框架。现在，就让我们一起看看如何利用 IntelliJ IDEA 快速的创建 Maven 项目吧！

![create-new-project](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/create-new-project.png)

如上图所示，点击`Create New Project`：

![new-project](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/new-project.png)

- **标注 1**：`Maven`选项；
- **标注 2**：`Project SDK`，项目 SDK；
- **标注 3**：`archetype`，Web 项目框架。

如上图所示，先点击 Maven 选项，然后选择 SDK，再从框架中选择`maven-archetype-webapp`用于创建 Web 项目。当然，我们也可以根本不同的需求选择不同的框架以便 IDEA 自动为我们生成项目框架。在这里，有一点需要我们特别注意，那就是：**`Maven 3.3.1+`以上的版本需要`JDK 1.7+`以上的版本与之搭配使用**，否则会出现异常，以至于 Maven 项目创建失败。在上述操作完成后，点击`Next`：

![new-project-2](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/new-project-2.png)

- **标注 1**：`GroupId`，项目坐标，与`ArtifactId`搭配使用，用于标记项目；
- **标注 2**：`ArtifactId`，项目坐标，与`GroupId`搭配使用，用于标记项目；
- **标注 3**：`Version`，项目版本，与`ArtifactId`、`GroupId`搭配使用，用于唯一标记项目。

如上图所示，`ArtifactId`、`GroupId`需要我们自己命名，`Version`默认为`1.0-SNAPSHOT`，表示该项目属于不稳定的快照版本，默认即可。输入完成后，点击`Next`：

![new-project-3](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/new-project-3.png)

- **标注 1**：`Maven home directory`，Maven 主目录，即最外层目录；
- **标注 2**：`User settings file`，Maven 配置文件；
- **标注 3**：`Local repository`，Maven 本地仓库，用于存储依赖包。

如上图所示，依次配置完之后，点击`Next`：

![new-project-4](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/new-project-4.png)

- **标注 1**：`Project name`，项目名称；
- **标注 2**：`Project location`，项目保存位置；
- **标注 3**：`More Settings`，更多配置，如配置项目模块位置、项目格式等。

如上图所示，我们将`Project name`和`Module name`统一命名为`gitcode`，依次配置完之后，点击`Next`：

![gitcode](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/gitcode.png)

- **标注 1**：`.idea`，自动生成的 IDEA 配置文件；
- **标注 2**：`src`，自动生成的 Maven 目录结构；
- **标注 3**：`BUILD SUCESS`，Maven 项目创建成功的标志。

如上图所示，当控制台输出`BUILD SUCESS`的时候，这意味着 Maven 已经创建完成。但是，如果我们仔细观察 IDEA 自动为我们生成的 Maven 目录结构，会发现这与我们认知中的 Maven 项目的目录结构大不相同，它没有与`main`同级的`test`目录、没有`resources`目录、也没有`java`目录，甚至连源目录都没有标记出来，为啥？实际上，Maven 并没有强制我们必须创建`test`、`resources`、`java`这样的目录，之所以建立这样的目录结构，仅仅是出于我们的习惯以及方便管理项目而已。接下来，我们就手动创建`test`、`resources`、`java`这样的结构，并标记`java`为`Sources Root`，即源目录：

![project-structure](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/project-structure.png)

如上图所示，以 Mac 电脑为例，依次点击`File`、`Project Structure`选项：

![modules](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/modules.png)

如上图所示，在最左边的`Project Structure`列表中选择`Modules`，再点击`Sources`进入我们的项目结构视图，然后点击`src`目录，右键呼出菜单栏，点击`New Folder`即可创建新目录：

![modules-2](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/modules-2.png)

如上图所示，这就是我们新创建的目录结构。

![modules-3](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/modules-3.png)

现在，选择`java`目录，点击`Mark as: Sources`即可将`java`目录标记为源目录：

![modules-4](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/modules-4.png)

如上图所示，以同样的方法，我们相继标记了`Tests`、`Resources`和`Test Resources`目录，其中`webapp`目录比较特殊，需要我们将其标记为 Web 的项目的资源目录。在这里，点击`gitcode`上面的`+`选项：

![modules-5](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/modules-5.png)

- **标注 1**：`+`，`Add`选项；
- **标注 2**：`Web`，项目类型。

如上图所示，依次点击`+`选项以及`Web`类型：

![modules-6](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/modules-6.png)

- **标注 1**：修改按钮；
- **标注 2**：快捷目录选项。

如上图所示，`Deploy Descriptor`需要指向项目的`web.xml`文件，一般情况下，默认的目录都是不准确，需要我们重新选择。

![modules-7](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/modules-7.png)

- **标注 1**：修改按钮；
- **标注 2**：快捷目录选项。

如上图所示，`Web Resources Directories`需要指向项目的资源目录即`webapp`目录，与`Deploy Descriptor`一样，需要我们重新选择。

![gitcode-success](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/maven-project/gitcode-success.png)

如上图所示，至此 Maven 项目创建完成，`java`源目录设置成功。

----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————

