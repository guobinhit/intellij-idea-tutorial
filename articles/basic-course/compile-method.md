# IntelliJ IDEA 编译方式介绍及编译器的设置和选择

相对于 Eclipse 的实时自动编译，IntelliJ IDEA 的编译更加手动化，虽然 IntelliJ IDEA 也可以通过设置开启实时编译，但是太浪费资源了，因此不建议这样做。IntelliJ IDEA 编译方式除了手工点击编译按钮进行编译之外，还可以在“容器”运行之前配置一个编译事件，先编译后运行。在默认情况下，IntelliJ IDEA 也都是这样设置的，因此在实际开发中，我们也不用太注意编译这件事。虽然 IntelliJ IDEA 没有实时编译（未设置时），但是这并不影响代码的自动检查。但是对于多个类之间的关联关系，还是要等`Build`或`Rebuild`触发的时候才会做相关检查的。

![build](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/compile-method/build.png)

 - **标注 1**：`Build Project`，编译项目；
 - **标注 2**：`Build Module`，编译模块；
 - **标注 3**：`Recomplie`，重新编译类文件；
 - **标注 4**：`Rebuild Project`，重新编译项目。

如上图所示，在 IntelliJ IDEA 中，编译方式有以上 3 种，分别为：

 - `Build`：对选定的目标（Project 或  Module）进行编译，但只编译修改过的文件，没有修改过的文件则不会进行编译。
 - `Recompile`：对选定的目标（Java 类文件），进行强制性编译，不管目标是否是被修改过。
 - `Rebuild`：对选定的目标（Project），进行强制性编译，不管目标是否是被修改过，由于 Rebuild 的目标只有 Project，因此每次 Rebuild 花的时间都比较长。

接下来，我们一起看看运行之前的编译情况：

![run-debug-configuration](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/compile-method/run-debug-configuration.png)

如上图所示，IntelliJ IDEA 默认在运行项目之前先进行`Build`操作。那么，我们再一起看看 IntelliJ IDEA 编译器的设置和选择：

![settings-1](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/compile-method/settings-1.png)

 - **标注 1**：设置自动编译项目；
 - **标注2**：设置编译时`heap`大小；
 - **标注 3**：设置编译时的`VM`参数。

如上图所示，我们定位到`Build、Execution、Deployment > Complie`页面，通过勾选 **标注 1** 所示的`Build project automatically`，我们可以设置 IntelliJ IDEA 进行自动编译；**标注 2** 表示设置编译`heap`大小，默认为 700，如果使用 64 位的机器，在内存足够的情况下，可以尝试修改为 1500 或以上，此外，如果我们在编译的时候报出`OutOfMemoryError`的错误，也可以来修改（减小）这个参数；**标注 3** 表示设置编译时的虚拟机参数，这个可以根据需求进行个性化设置，一般情况下，默认就可以。

![settings-2](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/compile-method/settings-2.png)

如上图所示，我们定位到`Build、Execution、Deployment > Compiler > Excludes`页面，可以通过点击 **标注 1** 所示的`+`和`-`，任意添加或删减目录（或文件）进行编译排除。在编译项目的时候，如果任何一个可编译的文件没有编译通过，那么 IntelliJ IDEA 就无法运行起来，必须等全部问题解决并且编译通过之后，IntelliJ IDEA 才能运行起来。不过有可能在开发过程中，某一个包目录的文件编译无法通过，但是我们又不急着改，这时我们就可以考虑把该包加入到排除编译列表中，这样的话，项目就可以运行起来啦！

![settings-3](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/compile-method/settings-3.png)

 - **标注 1**：`Use compile`；
 - **标注 2**：`Project bytecode version`；
 - **标注 3**：`Per-module bytecode version`.

如上图所示，我们定位到`Build、Execution、Deployment > Compiler > Java Compiler`页面，**标注 1** 所示为 IntelliJ IDEA 支持的编译器，包括`Javac`、`Eclipse`、`Ajc`等，默认是`Javac`，也推荐使用`Javac`；**标注 2** 所示为针对项目字节码编译版本，一般选择的是当前项目主 JDK 的版本；**标注 3** 表示可以针对`Project`下各个`Module`的特殊需求单独设置不同的`bytecode version`，当然，前提是我们的电脑上必须事先安装对应的 JDK 版本。


----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
