# 详述 IntelliJ IDEA 遇到 java -source 1.3 中不支持某某操作的解决方法

## 问题背景
在一个新的 Mac Pro 电脑中，安装 IntelliJ IDEA，并且配置了 JDK 1.8，打开测试项目，运行后，报出如下问题：

![error-jdk](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/java-source/error-jdk.png)

通过问题描述，显然 IDEA 并没有使用我配置的 JDK 1.8，而是使用了 JDK 1.3，这是为什么呢？

实际上，IDEA 默认是使用 JDK 1.3 进行编译，而在配置 JDK 的时候，我们有可能忽然了该配置。

## 解决方法
### 方法一

- `File -> Project Structure -> Modules`

![modules](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/java-source/modules.png)

如上图所示，进入该目录，修改当前模块的`Language level`，默认为`1.3`，修改为`8`即可。

### 方法二

- `File -> Project Structure -> Project`

![project](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/java-source/project.png)

如上图所示，进入该目录，修改当前项目的`Language level`，默认为`1.3`，修改为`8`即可。

无论是 **方法一** 还是 **方法二**，都是修改默认的`Language level`，其区别就是一个是对当前模块生效，一个是对当前项目生效。而有时，因为某种需要，我们可能会在一个项目里面建立多个模块，当然，常见的还是单模块项目。



----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
