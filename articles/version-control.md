# IntelliJ IDEA 中的版本控制机制

在之前的「[史上最简单的 IntelliJ IDEA 教程](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md)」之中，咱们已经了解了很多关于 IntelliJ IDEA 的使用方法，至少可以独立的运用 IntelliJ IDEA 进行项目开发啦！但是一个人进行项目开发更趋向于理想化，更多的则是团队协同开发。这时，咱们就需要了解一个非常重要的概念啦，那就是“**版本控制**”。

在此，咱们可以简单回顾“版本控制”的发展史。起初，并没有关于版本控制的概念，在协同开发的时候，大家都是自己保持项目代码，或者互相拷贝代码，这样在合并代码的过程中就难免遇到很多不兼容的问题；这就促使“集中式版本控制系统（CVCS）”的出现，例如 SVN、CVS 等，但这仍然有一个风险，那就是如果源码库出现问题，导致项目代码丢失，那么大家手里的都是部分代码，就算勉强合并到一起，也不能保证项目源码的准确性；因此，这又促使“分布式版本控制系统（DVCS）”的出现，例如 Git，它的好处显而易见，每个人从源码库中检出的代码，都是作为一份独立的、完整的拷贝代码存在，这时就算源码库出现问题，甚至源码丢失，那么任何一个人的代码都可以作为源码进行共享，从而大大提高了协同开发的抗风险能力。

因此，在本文中，博主更倾向于推荐大家使用分布式版本控制系统。不过在一般情况下，咱们仅需要下载一个版本控制系统的客户端即可，在这里，根据操作系统分别推荐一个博主感觉非常好用的版本控制系统客户端：

 - Windows 版本控制系统客户端：**TortoiseSVN**；
 - Mac 版本控制系统客户端：**CornerStone**.

接下来，咱们就进入主题，正式开始介绍 IntelliJ IDEA 中的版本控制机制：

![1](http://img.blog.csdn.net/20170423212204772)

如上图所示，点击`Settings`，进行如下界面：

![2](http://img.blog.csdn.net/20170423213242461)

 - 标注1：Plugins，插件；
 - 标注2：Version Control，版本控制。

如上图所示，标记出了“插件”和“版本控制”两个选项。有些人可能会认为 IntelliJ IDEA 自带了 SVN 或者 Git 等版本控制系统，因此只要安装了 IntelliJ IDEA 就可以使用版本控制系统的所有功能啦，这显然是一个错误的想法。IntelliJ IDEA 只是自带了对这些版本控制系统的支持插件，但是咱们想使用什么版本控制系统仍然得安装什么版本控制系统的客户端，否则照样用不了。

如上图中 **标注1** 所示，IntelliJ IDEA 对版本控制的支持都是以插件的方式来实现的。旗舰版默认支持目前主流的版本控制软件包括：GitHub、CVS、ClearCase、Git、、Mercurial、Perforce、Subversion（SVN） 和 TFS 等。由于 IntelliJ IDEA 支持的版本控制工具非常的多，但咱们真正能够用到的也就两三个而已，因此在本篇博文中，咱们主要介绍 SVN、Git 和 GitHub 的配置方法。

SVN
---
如果想要在 IntelliJ IDEA 中使用 SVN，则需要事先安装 SVN 客户端或是 TortoiseSVN 这类图形化工具。对于 Windows 系统，推荐大家安装 TortoiseSVN；对于 Mac 系统，则推荐大家安装 CornerStone. 

![1](http://img.blog.csdn.net/20170424201139349)

 - 标注1：`Use command line client`，使用命令行客户端；
 - 标注2：`Clear Auth Cache`，清除缓存。

如上图所示，勾选 **标注1** 所示的选项后，表示使用 SVN 命令行客户端，在这里，建议 SVN 的路径根据咱们安装后的路径进行选择，否则 IntelliJ IDEA 可能无法识别到 SVN，以至于报出：`Cannot run program "svn"`这类错误；在咱们使用 SVN 一段时间之后，如果发现 SVN 有些问题无法解决的话，可以考虑点击 **标注2** 所示的清除缓存按钮。



Git
---
如果想要在 IntelliJ IDEA 中使用 Git，同样需要事先安装 Git 客户端，不过在安装 Git 客户端的过程中，咱们可以自由选择是否同时使用 Windows 命令行工具。此外，如果大家没有安装过 Git 的话，则可以参考「[Git 的安装流程及步骤](http://blog.csdn.net/qq_35246620/article/details/68951724)」了解具体的安装步骤。

![2](http://img.blog.csdn.net/20170424204304631)

如上图所示，如果咱们事先安装了 Git 客户端的话，则会在`Path to Git executable`中自动定位到 Git 的可执行文件，然后点击`Test`：

![3](http://img.blog.csdn.net/20170424204335725)

如上图所示，显示`Git executed successfully`，则表示分布式版本控制系统 Git 可用。


GitHub
------
对于一个励志于在互联网浪潮中闯出一番天地的高逼格程序猿来说，如果不知道 GitHub 的话，貌似有些太 low 啦！如果你之前知道 GitHub 的话，那好吧，我感觉很正常；如果你之前不知道 GitHub 的话，那么真心建议你通过「[史上最简单的 GitHub 教程](http://blog.csdn.net/qq_35246620/article/details/66973794)」了解一下 GitHub，就算是注册个账号之后再也不用啦，至少咱们也可以淡（装）然（逼）的说“在想当初，我也曾 XXX，只是 XXX”对吧？总不至于当别人问到 GitHub 的时候，咱们一脸懵逼啊！

![5](http://img.blog.csdn.net/20170424210151546)

 - 标注1：`Create API Token`，创建 API Token；
 - 标注2：`Login to GitHub`，登录 GitHub 账号；
 - 标注3：`Test`，测试连接是否成功。

如上图所示，在 IntelliJ IDEA 中，提供了对 GitHub 的支持功能。当咱们登录 GitHub 账号之后，点击`Test`进行测试：

![6](http://img.blog.csdn.net/20170424210750399)

如上图所示，显示`Connection successfully  for user guobinhit`，表示咱们已经将此 IntelliJ IDEA 连接到 GitHub 账号为`guobinhit`的账号之中啦！现在，我们已经简单了解了 IntelliJ IDEA 的版本控制机制，那么接下来，就让我们一起看看如何在 IntelliJ IDEA 中进行具体的版本控制操作。

![2](http://img.blog.csdn.net/20170426133629655)

 - 标注1：`Checkout from Version Control`，从版本控制系统中检出项目；
 - 标注2：IntelliJ IDEA 支持的版本控制系统，包括`GitHub`、`CVS`和`Git`等。

如上图所示，我们可以通过`Checkout from Version Control`，从版本控制系统，如`GitHub`、`CVS`和`Git`等中检查项目。相对的，既然我们可以从版本控制系统中检出项目，那么自然也可以将项目上传到版本控制系统之中。

![3](http://img.blog.csdn.net/20170426135104913)

- 标注1：`Import into Version Control`，将项目上传到版本控制系统；
- 标注2：IntelliJ IDEA 支持的版本控制系统，包括`GitHub`、`CVS`和`Git`等。

如上图所示，通过以上操作，就可以将代码上传到版本控制系统之中。

现在，以博主的 GitHub 上面的项目`mybatis-tutorial`为例，检出项目：

![GitHub](http://img.blog.csdn.net/20170929135933683)

如上图所示，首先选择`Checkout from Version Control -> GitHub`，登录账号，然后选择我们想要检出的项目，点击`Clone`，此“克隆”的概念来自于 Git，表示把远程仓库的项目检出到本地：

![check](http://img.blog.csdn.net/20170929150517240)

如上图所示，点击`Clone`之后，提示我们对将要检出的项目进行确认，点击`Yes`，然后一路`Next`，最后点击`Finish`：

![mybatis](http://img.blog.csdn.net/20170929150843075)

如上图所示，至此，项目`mybatis-tutorial`已经成功从 GitHub 检出到本地啦！

![button](http://img.blog.csdn.net/20170929150945326)

如上图红色标记所示，皆为进行版本控制的按钮，从左至右分别为：

- `Update Project`，更新项目，即从检出仓库下载最新版本的代码；
- `Commit changes`，提交此检出版本项目上所有变化的文件；
- `Compare with the Same Repository Version`，比较当前文件与远程仓库版本文件之间的差异；
- `Show history`，显示当前文件的历史记录；
- `Revert`，还原当前被修改的文件到未被修改的版本状态。

![commit](http://img.blog.csdn.net/20170929153436644)

- 标注 1：在检出项目中有过修改的文件；
- 标注 2：`Comiit Messsage`提交信息，需要我们自己填写；
- 标注 3：`Diff`，展示文件修改前后对比；
- 标注 4：展示修改了几个文件，新建了几个文件；
- 标注 5：`Before Commit`，在提交项目前，进行一些前置操作；
- 标注 6：`After Commit`，在提交项目后，进行一些后置操作。

其中，`Diff`展示了文件修改前后详细的对比，我们需要好好利用；`Before Commit`，默认进行提交前的代码分析，可以检查出一些错误与警告。此外，我们也可以通过双击 **标注1** 所示的文件，放大文件修改前后的差异对比。接下来，点击`Comiit`进行验证：

![Code](http://img.blog.csdn.net/20170929154539552)

如上图所示，显示了代码分析的结果，具体可以参考「[详述 IntelliJ IDEA 提交代码前的 Code Analysis 机制](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/code-analysis.md)」.

最后，我们再回到`Version Control`，了解一些常用的操作：

![config](http://img.blog.csdn.net/20170929154738667)

- 标注1 ：`When files are created`，表示当有新文件放进项目中的时候 IntelliJ IDEA 做如何处理，默认是 Show options before adding to version control，表示弹出提示选项，让我们自己决定是否将这些新文件加入到版本控制。如果不想弹出提示，则选择下面两个选项进行默认操作。
- 标注 2：`When files are deleted`，表示当有新文件在项目中被删除的时候 IntelliJ IDEA 做如何处理，默认是 Show options before removing from version control，表示弹出提示选项，让我们自己决定是否将这些被删除的文件从版本控制中删除。如果不想弹出提示，则选择下面两个选项进行默认操作。

![ignore](http://img.blog.csdn.net/20170929154754290)

如上图所示，我们可以通过红色标记圈出的`+`，把不想加入版本控制的文件或目录添加到忽略列表中；反之，我们也可以通过红色标记圈出的`-`，把想加入版本控制的文件或目录从忽略列表中移除。在这里，我们需要注意：**当某文件或目录被添加到此“忽略列表”的之后，则该文件或目录不能进行版本控制的相关操作，例如提交**。

----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
