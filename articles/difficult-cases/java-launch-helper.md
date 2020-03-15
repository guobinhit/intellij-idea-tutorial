# 详述 IntelliJ IDEA 遇到 JavaLaunchHelper 多种实现的解决方法

## 问题背景

在 IntelliJ IDEA 中，运行项目，报出如下问题：

> objc[2150]: Class JavaLaunchHelper is implemented in both 
>  /Library/Java/JavaVirtualMachines/jdk1.8.0_112.jdk/Contents/Home/bin/java (0x1081bc4c0) and 
> /Library/Java/JavaVirtualMachines/jdk1.8.0_112.jdk/Contents/Home/jre/lib/libinstrument.dylib (0x1091d44e0). 
> One of the two will be used. Which one is undefined.

该问题主要出现于 Mac 版本的 IntelliJ IDEA 之中，而引起该问题的原因，则是 Mac 中 JDK 的一个 BUG，它是由启动应用程序时 IDE 使用的 Java 代理触发的，此警告是无害的，我们可以安全地忽略，并且该问题已经在后续的 JDK 中得到了解决。

但如果我们在实际的开发中遇到了该问题，我们可以通过下面的两种方法进行解决。

## 解决方法
### 方法一

既然该问题是由于 IDEA 启用代理引起的，那么我们禁止 IDEA 启动代理，即可解决该问题。

![idea-help](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/java-launch-helper/idea-help.png)

如上图所示，依次点击`Help -> Edit Custom Properties`，打开`idea.properties`配置文件。

![idea-no-launcher](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/java-launch-helper/idea-no-launcher.png)

如上图所示，在`idea.properties`配置文件添加`idea.no.launcher=true`语句，即可禁止 IDEA 启用代理，**该配置会在重启 IDEA 后生效**。

### 方法二

如果我们不想为了修复一条无害的警告消息而禁止 IDEA 启用代理，我们可以选择将此消息折叠，即隐藏起来。

![preferences](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/java-launch-helper/preferences.png)

如上图所示，依次点击`IntelliJ IDEA -> Preferences`，进入`Preferences`配置页面。

![console-fold](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/java-launch-helper/console-fold.png)

如上图所示，选择`Editor -> General -> Console`，进行`Console` 配置页面。

在此页面，点击标注的`+`按钮，将`Class JavaLaunchHelper is implemented in both`这条语句配置上，点击`Apply`后，即可生效。



----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
