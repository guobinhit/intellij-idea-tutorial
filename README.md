# 史上最简单的 IntelliJ IDEA 教程

## 前言

　　IntelliJ IDEA（简称 IDEA），是 Java 语言开发的集成环境，IDEA 在业界被公认为最好的 Java 开发工具之一，尤其在智能代码助手、代码自动提示、重构、J2EE 支持、各类版本工具（Git、SVN、GitHub 等）、JUnit、CVS 整合、代码分析和创新的 GUI 设计等方面的功能都值得称道。至于 Eclipse 本人接触的不多，因此也无法比较，但殊途同归，无论选择什么集成开发环境，都是为了辅助咱们编程，所以可以说：**没有最好的工具，只有最适合自己的工具**。因此，撰写本系列文章的目的很简单，就是想把自己的经验整理记录下来，当然，如果能够在此基础上帮助大家快速入门并掌握 Intellij IDEA 那就再好不过啦！
  
- **注：此教程使用的工具版本为 IntelliJ IDEA 2017(.1.5)**


## 目录

- 第 1 篇：安装 IDE 的方法

  - [在 Windows 系统下安装 IntelliJ IDEA 的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/install-intellij-idea-on-windows.md)
  - [在 Mac 系统下安装 PyCharm 的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/pycharm.md)

- 第 2 篇：[首次运行 IntelliJ IDEA 示例](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/first-run-idea.md)

- 第 3 篇：[IntelliJ IDEA 安装目录的核心文件讲解](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/core-file-talk.md)

- 第 4 篇：[详述 IntelliJ IDEA 的使用界面](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/use-face.md)

- 第 5 篇：[IntelliJ IDEA 之 HelloWorld 项目创建及相关配置文件介绍](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/hello-world.md)

- 第 6 篇：[设置 IntelliJ IDEA 主题和字体的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/theme-and-font.md)

- 第 7 篇：[修改 IntelliJ IDEA 模板注释中的 user 内容](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/modify-user-template.md)

- 第 8 篇：[IntelliJ IDEA 常见文件类型的图标介绍](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/idea-icon.md)

- 第 9 篇：[IntelliJ IDEA 缓存和索引的介绍及清理方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/index-and-cache.md)

- 第 10 篇：[IntelliJ IDEA 编译方式介绍及编译器的设置和选择](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/compile-method.md)

- 第 11 篇：[IntelliJ IDEA 中 Project 和 Module 的概念及区别](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/project-module.md)

- 第 12 篇：[详述 IntelliJ IDEA 中的版本控制机制](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/version-control-one.md)

- 第 13 篇：[详述 IntelliJ IDEA 插件的安装及使用方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/plugins.md)

- 第 14 篇：[详述 IntelliJ IDEA 创建 Maven 项目及设置 java 源目录的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/maven.md)

- 第 15 篇：[IntelliJ IDEA 中的 Maven 项目初体验及搭建 Spring MVC 框架](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/run-maven-springmvc.md)

- 第 N 篇：XXXXXX

## 小技巧

- 第 1 篇：[IntelliJ IDEA 常用快捷键 之 Mac 版](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/keymap-mac.md)

- 第 2 篇：[详述 IntelliJ IDEA 中恢复代码的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/recovery-code.md)

- 第 3 篇：[IntelliJ IDEA 控制台输出中文乱码问题的解决方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/solve-garbled-questions.md)

- 第 4 篇：[详述 IntelliJ IDEA 中自动生成 serialVersionUID 的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/serialVersionUID.md)

- 第 5 篇：[详述 IntelliJ IDEA 提交代码前的 Code Analysis 机制](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/code-analysis.md)

- 第 6 篇：[关于 IntelliJ IDEA 中 Schedule for Addition 的问题](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/schedule.md)

- 第 7 篇：[详述 IntelliJ IDEA 设置 Sublime 代码颜色的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/code-color.md)

- 第 8 篇：[详述 IntelliJ IDEA 远程调试 Tomcat 的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/remote.md)

- 第 9 篇：[利用 IntelliJ IDEA 进行代码对比的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/compare-code.md)

- 第 10 篇：[设置 IntelliJ IDEA 彩色代码主题](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/color-code.md)

- 第 11 篇：[详述使用 IntelliJ IDEA 解决 jar 包冲突的问题](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/conflict-jar.md)

## 致谢

　　作为一个初学者，刚接触 IntelliJ IDEA 的时候，就有幸阅读了 [@Judas.n](https://github.com/judasn) 写的关于 IntelliJ IDEA 的教程，也获益良多。但是随着自己接触的越来越多，却发现 Judas.n 写的教程与最新版本的 IntelliJ IDEA 略有出入，因此决定自己重新写一份关于 IntelliJ IDEA 的教程，这也是此系列教程的来源。在此感谢 Judas.n 写的教程对我的启发，本教程也对 Judas.n 写的教程多有借鉴，下面附上其 GitHub 地址，欢迎感兴趣的童鞋移步到 Judas.n 的教程观摩学习。

- IntelliJ-IDEA-Tutorial: https://github.com/judasn/IntelliJ-IDEA-Tutorial 


----------
此外，附上一句格言，望共勉：**好学若饥，谦卑若愚。**


