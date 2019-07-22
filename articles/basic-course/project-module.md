# IntelliJ IDEA 中 Project 和 Module 的概念及区别

在 IntelliJ IDEA 中，没有类似于 Eclipse 工作空间（`Workspace`）的概念，而是提出了`Project`和`Module`这两个概念。接下来，就让我们一起看看  IntelliJ IDEA 官方是如何描述两者的吧！**对于 Project，IntelliJ IDEA 官方是这样介绍的**：

`A project is a top-level organizational unit for your development work in IntelliJ IDEA. In its finished form, a project may represent a complete software solution. A project is a collection of:`

 - `Your work results: source code, build scripts, configuration files, documentation, artifacts, etc.`
 - `SDKs and libraries that you use to develop, compile, run and test your code.`
 - `Project settings that represent your working preferences in the context of a project.`

`A project has one or more modules as its parts.`

**对于 Module，IntelliJ IDEA 官方是这样介绍的**：

 - `A module is a part of a project that you can compile, run, test and debug independently.`
 - `Modules are a way to reduce complexity of large projects while maintaining a common (project) configuration.`
 - `Modules are reusable: if necessary, a module can be included in more than one project.`

通过上面的介绍，我们知道：在 IntelliJ IDEA 中`Project`是最顶级的结构单元，然后就是`Module`，一个`Project`可以有多个`Module`。目前，主流的大型项目结构基本都是多`Module`的结构，这类项目一般是按功能划分的，比如：`user-core-module`、`user-facade-module`和`user-hessian-module`等等，模块之间彼此可以相互依赖。通过这些`Module`的命名可以看出，它们都是处于同一个项目中的模块，彼此之间是有着不可分割的业务关系。因此，我们可以大致总结出：一个`Project`是由一个或多个`Module`组成，

- 当为单`Module`项目的时候，这个单独的`Module`实际上就是一个`Project`；
- 当为多`Module`项目的时候，多个模块处于同一个`Project`之中，此时彼此之间具有互相依赖的关联关系。

此外， IntelliJ IDEA 的`Project`是一个不具备任何编码设置、构建等开发功能的概念，其主要作用就是起到一个项目定义、范围约束、规范类型的效果，或许，我们也可以简单地理解`Project`就是一个单纯的目录，只是这个目录在命名上必须有其代表性的意义。在缺省情况下，IntelliJ IDEA 是默认单`Project`单`Module`的，这时`Project`和`Module`合二为一，在没有修改存储路径的时候，显然`Project`对`Module`具有强约束作用！不过说实话，这里就是将`Module`的内容放在了`Project`的目录下，实际上还是`Module`自己约束自己。

![new-project](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/project-module/new-project.png)

 - **标注 1**：`Project name`，项目名称；
 - **标注 2**：`Project location`，项目存储地址；
 - **标注 3**：`Module name`，模块名称；
 - **标注 4**：`Module file location`，模块存储地址。

如上图所示，通过观察`Project`和`Module`的存储地址，我们可以发现，IntelliJ IDEA 在此处建立了一个名为`user-core-module`的目录，并将其放在了名为`user-modules-project`的目录下，而没有将两个目录合二为一，也就为我们建立多`Module`的`Project`作了准备。

![user-modules-project](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/project-module/user-modules-project.png)

如上图所示，显然`user-modules-project`仅表现为一个目录而已。

![new-module](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/project-module/new-module.png)

如上图所示，依次点击`File -> New -> Module`，进入如下界面：

![user-hessian-module](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/project-module/user-hessian-module.png)

如上图所示，输入`Module name`之后，`Content root`和`Module file location`自动发生改变，然后点击`Finish`，完成：

![more-module](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/project-module/more-module.png)

如上图所示，我们在项目`user-modules-project`中，建立了两个`Module`，分别为`user-core-module`和`user-hessian-module`，然后我们再来看看存储目录：

![more-module-package](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/project-module/more-module-package.png)

如上图所示，显然在`user-modules-project`目录中，又多了一个名为`user-hessian-module`的目录。

至此，多`Module`的`Project`构建完成！


----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
