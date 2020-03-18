# 详述 IntelliJ IDEA 遇到 Maven 项目打开（Open）或者导入（Import）失败的解决方法

## 问题背景

现有一个 Maven 项目，通过 IntelliJ IDEA 的`Open`或者`Import Project`来打开或者导入该项目：

![unable-import-maven-project](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/unable-import-maven-project/unable-import-maven-project.png)

如上图所示，导入 Maven 项目失败，提示：

> **Unable to import maven project: See logs for details**

就算我们点击`Event Log`，也获取不到详细的错误信息：

![event-log](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/unable-import-maven-project/event-log.png)

这时，我们需要通过`Help -> Show Log in Finder`来查看错误日志：

![show-log](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/unable-import-maven-project/show-log.png)

在我们点击`Show Log in Finder`之后，会在弹出的目录中找到一个名为`idea.log`的日志文件，打开该文件，即可查看详细的错误日志：

```bash
2020-03-16 14:40:03,808 [13325330]   INFO - ution.rmi.RemoteProcessSupport - Port/ID: 52340/Maven3ServerImpl952a326a 
2020-03-16 14:40:05,385 [13326907]  ERROR -      #org.jetbrains.idea.maven - com.google.inject.CreationException: Unable to create injector, see the following errors:

1) No implementation for org.apache.maven.model.path.PathTranslator was bound.
  while locating org.apache.maven.model.path.PathTranslator
    for field at org.apache.maven.model.interpolation.AbstractStringBasedModelInterpolator.pathTranslator(Unknown Source)
  at org.codehaus.plexus.DefaultPlexusContainer$1.configure(DefaultPlexusContainer.java:350)

2) No implementation for org.apache.maven.model.path.UrlNormalizer was bound.
  while locating org.apache.maven.model.path.UrlNormalizer
    for field at org.apache.maven.model.interpolation.AbstractStringBasedModelInterpolator.urlNormalizer(Unknown Source)
  at org.codehaus.plexus.DefaultPlexusContainer$1.configure(DefaultPlexusContainer.java:350)

2 errors 
java.lang.RuntimeException: com.google.inject.CreationException: Unable to create injector, see the following errors:

1) No implementation for org.apache.maven.model.path.PathTranslator was bound.
  while locating org.apache.maven.model.path.PathTranslator
    for field at org.apache.maven.model.interpolation.AbstractStringBasedModelInterpolator.pathTranslator(Unknown Source)
  at org.codehaus.plexus.DefaultPlexusContainer$1.configure(DefaultPlexusContainer.java:350)

2) No implementation for org.apache.maven.model.path.UrlNormalizer was bound.
  while locating org.apache.maven.model.path.UrlNormalizer
    for field at org.apache.maven.model.interpolation.AbstractStringBasedModelInterpolator.urlNormalizer(Unknown Source)
  at org.codehaus.plexus.DefaultPlexusContainer$1.configure(DefaultPlexusContainer.java:350)

2 errors
	at com.google.inject.internal.Errors.throwCreationExceptionIfErrorsExist(Errors.java:543)
	at com.google.inject.internal.InternalInjectorCreator.initializeStatically(InternalInjectorCreator.java:159)
	at com.google.inject.internal.InternalInjectorCreator.build(InternalInjectorCreator.java:106)
	at com.google.inject.Guice.createInjector(Guice.java:87)
	at com.google.inject.Guice.createInjector(Guice.java:69)
	at com.google.inject.Guice.createInjector(Guice.java:59)
	at org.codehaus.plexus.DefaultPlexusContainer.addComponent(DefaultPlexusContainer.java:344)
	at org.codehaus.plexus.DefaultPlexusContainer.addComponent(DefaultPlexusContainer.java:332)
	at org.jetbrains.idea.maven.server.Maven3ServerEmbedderImpl.customizeComponents(Maven3ServerEmbedderImpl.java:555)
	at org.jetbrains.idea.maven.server.Maven3ServerEmbedderImpl.customize(Maven3ServerEmbedderImpl.java:529)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
    ... omit some log ...
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1142)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:617)
	at java.lang.Thread.run(Thread.java:745)
2020-03-16 14:40:05,386 [13326908]  ERROR -      #org.jetbrains.idea.maven - IntelliJ IDEA 2017.1.6  Build #IU-171.4694.73 
2020-03-16 14:40:05,386 [13326908]  ERROR -      #org.jetbrains.idea.maven - JDK: 1.8.0_112 
2020-03-16 14:40:05,386 [13326908]  ERROR -      #org.jetbrains.idea.maven - VM: Java HotSpot(TM) 64-Bit Server VM 
2020-03-16 14:40:05,386 [13326908]  ERROR -      #org.jetbrains.idea.maven - Vendor: Oracle Corporation 
2020-03-16 14:40:05,386 [13326908]  ERROR -      #org.jetbrains.idea.maven - OS: Mac OS X 
2020-03-16 14:40:05,386 [13326908]  ERROR -      #org.jetbrains.idea.maven - Last Action: Maven.Reimport 
```

通过错误日志，我们可以知道到底出哪里出现了问题。

对于上述问题，实际上就是 Maven 的版本与 IntelliJ IDEA 的版本不兼容的问题。



## 解决方法
在本案例中，两者的版本分别为：

- IntelliJ IDEA（`2017.1.6`）
- Maven（`3.6.3`）

当我切换 Maven 的版本为`3.2.5`的时候，该问题解决。

![maven-config](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/unable-import-maven-project/maven-config.png)

说实话，无论是 IntelliJ IDEA 还是 Maven 版本更新的都比较快，想要找老版本有的安装包还真不太好找。

在此，给大家分享一个下载 Maven 各种版本的「[仓库](https://archive.apache.org/dist/maven/maven-3/)」，**强烈推荐收藏**！

----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
