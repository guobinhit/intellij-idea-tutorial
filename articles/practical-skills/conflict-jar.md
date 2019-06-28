# 详述使用 IntelliJ IDEA 解决 jar 包冲突的问题

在实际的 Maven 项目开发中，由于项目引入的依赖过多，遇到 jar 冲突算是一个很常见的问题了。在本文中，我们就一起来看看，如何使用 IntelliJ IDEA 解决 jar 包冲突的问题！简单粗暴，直接上示例：

![maven-project](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/conflict-jar/maven-project.png)

- **标注 1**： `Maven Project`，Maven 项目选项；
- **标注 2**：`Dependencies`，项目依赖；
- **标注 3**：`Show Dependencies`，展示项目依赖图。

其中，只有在点击 **标注 2** 所示的`Dependencies`之后，才会显示 **标注 3** 所示的`Show Dependencies`按钮。在这里，我们点击`Show Dependencies`按钮：

![show-dependencies](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/conflict-jar/show-dependencies.png)

如上图所示，展示了我们项目的依赖图。But，依赖图太小了，根本没法看啊？好办，点击鼠标右键，呼出右键菜单栏，然后点击`Actual Size`：

![actual-size](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/conflict-jar/actual-size.png)

如上图所示，项目依赖图的尺寸放大了，这回利于我们排除 jar 包冲突的问题啦！

![jar-picture](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/conflict-jar/jar-picture.png)

如果我们仔细观察上图，会发现在项目依赖图中，有一些红色标记的线，实际上，这些红色标记出来的线所指向的 jar 包，就是项目中冲突的 jar 包！且在我们点击 jar 包之后，还会显示出多条指向 jar 包的红色虚线，其代表着该 jar 包被多次引用，及具体引用路径。

![exclude-jar](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/conflict-jar/exclude-jar.png)

如上图所示，想要排除冲突的 jar 包，其方法为：**点击冲突的 jar 包，右键呼出菜单栏，点击`Exclude`选项**。

![test-exclude-jar](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/conflict-jar/test-exclude-jar.png)

如上图所示，在排除冲突的 jar 包之后，`pom.xml`文件会自动更新，添加排除语句。



----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
