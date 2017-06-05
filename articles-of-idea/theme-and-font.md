# 设置 IntelliJ IDEA 主题和字体的方法

# 1 前言

在博文“ [IntelliJ IDEA 之 HelloWorld 项目创建及相关配置文件介绍](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/hello-world.md) ”中，咱们已经用 IntelliJ IDEA 创建了第一个 Java 项目 HelloWorld，如下图所示：

![1](http://img.blog.csdn.net/20170318133709550?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzUyNDY2MjA=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

观察上图，大家有没有发现一些问题，例如，整个界面的字体是不是都太小了一点啊？不知道大家感受如何，反正博主看到这么小的字体，当真是头晕眼花啊！因此，接下来，就让咱们一起尝试着把 IntelliJ IDEA 的主题和字体都重新设置一遍，看看到底什么样的模式咱们看着最舒服。

# 2 主题修改

## 2.1 界面主题修改

![2](http://img.blog.csdn.net/20170318222625187?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzUyNDY2MjA=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

如上图所示，依次点击“ Files ”--> “ Settings ”，进入如下界面：

![3](http://img.blog.csdn.net/20170318223032457?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzUyNDY2MjA=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

 - 标注1：主题选择区；
 - 标注2：Darcula、IntelliJ 和 Windows，三个主题。

如上图所示，咱们定位到“ Appearance & Behavior > Appearance ”界面，在 Windows 系统上 IntelliJ IDEA 默认提供三个主题，分别为：Darcula、IntelliJ 和 Windows。其中，除了 Darcula 是黑色背景的主题，其余两个都是白色背景的主题。在这里，咱们以“  Windows ”主题为例，演示一下修改后的效果：

![4](http://img.blog.csdn.net/20170319130331816?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzUyNDY2MjA=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

如上图所示，这是咱们选择“ Windows ”主题、点击“ Apply ”之后的效果，为纯白色主题。

## 2.2 代码编辑区主题修改

![5](http://img.blog.csdn.net/20170319131122161?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzUyNDY2MjA=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

 - 标注1：主题选择区；
 - 标注2：Default 和 Darcula，两个主题。

如上图所示，咱们定位到“ Editor > Colors & Fonts ”界面，在 Windows 系统上 IntelliJ IDEA 默认提供两个编辑区主题，分别为：Default 和 Darcula。其中，Default 为默认主题；Darcula 为黑色主题。在这里，咱们以“  Darcula ”主题为例，演示一下修改后的效果：

![6](http://img.blog.csdn.net/20170319131552401?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzUyNDY2MjA=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

如上图所示，这是咱们选择“ Darcula ”主题、点击“ Apply ”之后的效果，为黑色编辑区主题。

通过以上的演示，咱们已经知道了，无论是界面还是编辑区的主题都是可以修改的，具体如何修改，这就看咱们的心情啦！对于博主来说，比较喜欢 “ Darcula ”主题，因此在接下来的内容中，咱们都在“ Darcula ”主题主题下进行演示。

# 3 字体修改

## 3.1 界面主题字体修改

![7](http://img.blog.csdn.net/20170319132854938?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzUyNDY2MjA=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

 - 标注1：重写默认字体（必选）；
 - 标注2：具体可以修改字体大小的数值。

如上图所示，咱们定位到“ Appearance & Behavior > Appearance ”界面，如果确定要修改字体大小的话，**标注1** 所示的`Override default fonts by XXX`为必选项，否则的话，不能修改字体，因为 IntelliJ IDEA 默认是不推荐修改的；**标注2** 所示的为咱们具体可以修改字体大小的数值。在这里，咱们选择`Size`为 14，演示一下修改后的效果：

![8](http://img.blog.csdn.net/20170319133634942?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzUyNDY2MjA=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

如上图所示，这是咱们选择`Size`为 14、点击“ Apply ”之后的效果，显然界面主题的字体明显都变大了很多。

在这里，有一点需要注意，那就是：**有的字体是包含中文的，有的字体则是不包含中文的**。一般情况下，使用英文的国家是不需要额外担心乱码问题的，但是咱们需要啊！如果咱们选择的字体不包含中文的话，很多位置上可能会出现类似于 口口口口口 这样的乱码问题。例如，`Courier New`和`Monaco`就是纯英文字体，而`Microsoft YaHei`就是包含中文的字体。

## 3.2 代码编辑区字体修改

![9](http://img.blog.csdn.net/20170319140153110?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzUyNDY2MjA=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

 - 标注1：Save as 主题（必选）；
 - 标注2：仅展示等宽字体；
 - 标注3：字体具体大小的数值；
 - 标注4：行宽（行与行之间的距离）；
 - 标注5：第二字体；
 - 标注6：字体、大小及行宽的示例展示区。

如上图所示，咱们定位到“ Editor > Colors & Fonts > Font ”界面，**标注1** 所示的`Save As`表示咱们需要另外复制一份编辑区主题，然后才能修改，因为 IntelliJ IDEA 是不能直接在默认的代码模板上修改字体的；**标注2** 所示的`Show only monospaced fonts`表示只显示系统上的等宽字体，取消勾选后，将显示系统上所有已安装的字体。**标注5** 所示的`Secondary font`表示第二字体，因为 IntelliJ IDEA 的编码字体有“ 第一字体 ”和“ 第二字体 ”之分，当有些字符在第一字体不能支持的时候，将会自动使用第二字体进行支持。在这里，咱们选择`Size`为 16，演示一下修改后的效果：

![10](http://img.blog.csdn.net/20170319141612098?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzUyNDY2MjA=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

如上图所示，这是咱们选择`Size`为 16、点击“ Apply ”之后的效果，显然编辑区主题的字体明显都变大了很多。

## 3.3 控制台输出字体修改

![11](http://img.blog.csdn.net/20170319142542486?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzUyNDY2MjA=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

如上图所示，咱们定位到“ Editor > Colors & Fonts > Console Font ”界面，细心观察之下，咱会发现这个界面和“ Editor > Colors & Fonts > Font ”界面完全相同，因此咱们就不重新介绍一遍啦！在这里，咱们选择`Size`为 14，演示一下修改后的效果：

![12](http://img.blog.csdn.net/20170319142857310?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzUyNDY2MjA=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

如上图所示，这是咱们选择`Size`为 14、点击“ Apply ”之后的效果，运行程序后，控制台的输出字体显示大了，也清晰了很多。

----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
