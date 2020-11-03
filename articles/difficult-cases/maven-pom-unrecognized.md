#  详述 IntelliJ IDEA 遇到 Maven 项目 pom.xml 文件没有识别的解决方法

## 问题现象

有的时候，我们可能会遇到 IDEA 没有识别 Maven 项目`pom.xml`的问题，其表现出来的现象就是：

![pom-xml](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/maven-pom-unrecognized/pom-xml.png)

究其原因，就是 IDEA 把`pom.xml`文件当成了普通的`xml`格式文件。

## 解决方法

这个问题的解决方法比较简单，IDEA 已经提供了相应的功能。

![as-maven-project](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/maven-pom-unrecognized/as-maven-project.png)

如上图所示，鼠标右键点击`pom.xml`文件，呼出菜单栏，点击上图标记出来的`Add as Maven Project`按钮即可。


----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
