# 在 Win10 系统下安装 JDK 及配置环境变量的方法

首先，在官网下载 JDK：[Oracle 官网](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

![oracle-jdk](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/oracle-jdk.png)

如上图所示，在 Oracle 官网下载 JDK，有一点需要注意，那就是在我们下载合适的 JDK 之前，需要先点击 **标记 1** 所在的按钮，选择接受。否则的话，直接点击 JDK 进行下载的时候，将会弹出如下界面：

![unaccept](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/unaccept.png)

选择`Accept License Agreement`之后，再点击 JDK 进行下载就会弹出下载提示框了，如下图所示：

![accept](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/accept.png)

下载完成后，双击可执行文件，以博主为例，双击`jdk-8u121-windows-x64`可执行文件，将会进入 JDK 的安装界面：

![download-jdk-1](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/download-jdk-1.png)

如上图所示，点击“下一步”，进入如下界面：

![download-jdk-2](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/download-jdk-2.png)

在这里有一点需要注意，那就是 JDK 默认安装在`C`盘的`Program Files`目录下，如果需要修改安装路径，则可以点击 **标记 1** 所示的“更改”，一般情况下，选择默认路径就可以，点击“下一步”，进入如下界面：

![download-jdk-3](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/download-jdk-3.png)

如上图所示，这个界面是安装与 JDK 同版本的 JRE，其实在 JDK 中已经包含 JRE 了，因此这个 JRE 实际上并没有起什么作用，安装也没有什么问题，在这里，我们选择安装，点击“下一步”，进入如下界面：

![download-jdk-4](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/download-jdk-4.png)

如上图所示，显示的是 JRE 正在安装中的界面，安装完成后，将会进入如下界面：

![download-jdk-5](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/download-jdk-5.png)

如上图所示，如果有需要的话，点击“后续步骤”，将会访问教程、API 文档和开发人员指南等内容；否则的话，直接点击“关闭”就可以啦！至此，在 Win10 系统下安装 JDK 完成。接下来，配置环境变量，使 JDK 全局生效。首先，找到 JDK 的安装目录，以博主为例，进入这一层 `C:\Program Files\Java\jdk1.8.0_121`目录，复制以备后用。然后，通过“控制面板”进入“系统”属性，实际上直接选择“此电脑”点击右键选择“属性”即可：

![system](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/system.png)

如上图所示，点击“高级系统设置”，进入如下界面：

![system-property](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/system-property.png)

再点击“环境变量”，进入如下界面：

![environment](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/environment.png)

在这里，就需要我们特别注意了，选择“系统变量”区域的“新建”功能，点击后，进入如下界面：

![new-environment](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/new-environment.png)

设置系统变量名为`JAVA_HOME`，变量值为`C:\Program Files\Java\jdk1.8.0_121`，点击“确定”，然后打开“系统变量”区域的`Path`，将这条语句`;%JAVA_HOME%\bin`追加到`Path`变量值的最后面，如下图所示：

![edit-path](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/edit-path.png)

至此，环境变量就已经设置完啦！但是空口无凭啊，我们再验证一下，用事实说话。因此，打开“命令行窗口”，输入命令`java`，结果如下图所示：

![cmd](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/cmd.png)

再输入命令`javac`，结果如下图所示：

![user-think-javac](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/user-think-javac.png)

如上图所示的结果，已经可以证明我们的环境变量配置成功啦！不过说实话，我们在`C`盘验证不是很好，因为配置环境变量就是为了在其它位置（如`D`盘）也可以运行 JDK，我们都把 JDK 安装到`C`盘了，再在`C`盘进行验证就有些取巧了，因为就算环境变量没有配置成功，如果我们进入相应的安装目录下，也是可以运行 JDK 的。因此，我们来一个狠的，直接在`D`盘的根目录下创建一个`.java`文件，然后在“命令行窗口”编译并运行，如果这样做还能成功的话，那毫无疑问，环境变量我们肯定配置成功啦！

![hello-world-txt](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/hello-world-txt.png)

如上图所示，我们先在`D`盘的根目录下创建一个名为`HelloWorld.txt`文件，输入以上代码，然后我们再修改文件的后缀`.txt`为`.java`即可。最后，在“命令行窗口”输入以下命令：

![java-hello-world](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/install-jdk-win10/java-hello-world.png)

观察运行结果，显然我们的环境变量配置成功啦！

----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
