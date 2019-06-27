# 修改 IntelliJ IDEA 模板注释的内容

在博文「[设置 IntelliJ IDEA 主题和字体的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/theme-and-font.md)」中，我们进一步了解了 IntelliJ IDEA 的个性化设置功能，包括主题和字体的常用设置等，修改后，具体的效果，如下图所示：

![default-template](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/modify-user-template/default-template.png)

观察上图，不知道大家有没有注意到：IntelliJ IDEA 自带模板注释的功能。如上图所示，在创建 Java 类的时候，其自带的模板注释内容如下：

```
/**
 * Created by think on 2017/3/16.
 */
```
查看`Settings`之后，我们会发现，其内容来自于：

```
/**
 * Created by ${USER} on ${DATE}.
 */
```
 * `${USER}`：表示主机名；
 * `${DATE}`：表示创建文件的时间。

两者相对比，我们发现：`${USER}`被设置成了`think`；`${DATE}`被设置成了`2017/3/16`。其中，`${DATE}`没什么问题，表示我们创建类的时间，但是`${USER}`设置成`think`看着不太爽啊！那该怎么办啊？啥也别说了，直接动手改了它呗！接下来，博主将演示两种修改模板注释中 user 内容的方法。

> 在`Settings`中进行修改

![settings](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/modify-user-template/settings.png)

如上图所示，我们定位到`Editor > File and Code Templates`界面，然后选择`Includes`中的`File Header`，将其中的`${USER}`直接修改成我们自己定义的名称，例如，博主将其设置为`维C果糖`，然后点击`Apply`。接下来，在`demo`目录下，创建测试类`CeshiUser`，其效果如下图所示：

![test-settings](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/modify-user-template/test-settings.png)

如上图所示，显然咱们的设置生效啦！

> 在`bin`目录下修改`idea.exe`配置文件

![bin-idea](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/modify-user-template/bin-idea.png)

如上图所示，我们打开了 IntelliJ IDEA 安装目录中`bin`目录下的`idea.exe`配置文件，并且添加了一行内容`-Duser.name=charies`，接下来，保存该配置文件，重新启动 IntelliJ IDEA，在`demo`目录下，创建测试类`CeshiUser2`，其效果如下图所示：

![test-bin-idea](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/modify-user-template/test-bin-idea.png)

如上图所示，显然我们的设置生效啦！不过在这里，有两点需要注意，那就是：

 - **① 在`idea.exe`配置文件中修改模板注释中 user 内容的时候，我们不能将其设置为中文，否则会出现中文乱码的情况。**
 - **② 修改`idea.exe`配置文件之后，需要重启 IntelliJ IDEA ，只有在重启之后，这些最新配置才能生效。**



----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————

