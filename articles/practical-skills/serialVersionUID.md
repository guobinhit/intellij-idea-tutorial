# 详述 IntelliJ IDEA 中自动生成 serialVersionUID 的方法

当我们用 IntelliJ IDEA 编写类并实现 Serializable（序列化）接口的时候，可能会遇到这样一个问题，那就是：

 - **无法自动生成`serialVersionUID`**.

而`serialVersionUID`又是一个非常重要的字段，因为 Java 的序列化机制是通过在运行时判断类的`serialVersionUID`来验证版本一致性的。在进行反序列化时，JVM 会把传来的字节流中的`serialVersionUID`与本地相应实体（类）的`serialVersionUID`进行比较，如果相同就认为是一致的，可以进行反序列化，否则就会出现序列化版本不一致的异常。 

一般来说，定义`serialVersionUID`的方式有两种，分别为：

 - 采用默认的`1L`，具体为`private static final long serialVersionUID = 1L;`
 - 根据类名、接口名、成员方法及属性等来生成一个`64`位的哈希字段，例如  `private static final long serialVersionUID = XXXL;`

而 Java 类进行序列化也两个主要目的，分别为：

 - 把对象的字节序列永久地保存到硬盘上，通常存放在一个文件中；
 - 在网络上传送对象的字节序列。

在这里，我们就一起来看看如何利用 IntelliJ IDEA 自动生成`serialVersionUID`.

**第 1 步：安装`GenerateSerialVersionUID`插件**

![preferences](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/serialVersionUID/preferences.png)

如上图所示，点击`Preferences`，进入如下界面：

![plugins](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/serialVersionUID/plugins.png)

在这里，选择`Plugins`，并搜索`GenerateSerialVersionUID`，如果没有发现此插件，则可以点击`Search in repositories`进行搜索：

![browse-repositories](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/serialVersionUID/browse-repositories.png)

如上图所示，点击`install`，即可安装此插件。

**第 2 步：设置`Inspections`功能**

![inspections](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/serialVersionUID/inspections.png)

如上图所示，进入`Default Settings`，在`Inspections`设置页面中，勾选`Serializable class without 'serialVersionUID'`，并且还可以在`Severity`中设置提示级别，如`Warning`、`Error`等，默认为`Warning`，也建议选择`Warning`级别的提示。

![generate-uid](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/serialVersionUID/generate-uid.png)

如上图所示，创建一个类并实现`Serializable`接口，然后按`alt`+`Enter`键，即可收到提示，然后选择`SerialVersionUID`：

![test-generate-uid](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/practical-skills/serialVersionUID/test-generate-uid.png)

如上图所示，显然我们已经利用 IntelliJ IDEA 中自动生成`serialVersionUID`啦！








----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
