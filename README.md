# 史上最简单的 IntelliJ IDEA 教程

## 前言

　　IntelliJ IDEA（简称 IDEA），是 Java 语言开发的集成环境，IDEA 在业界被公认为最好的 Java 开发工具之一，尤其在智能代码助手、代码自动提示、重构、J2EE 支持、各类版本工具（Git、SVN、GitHub 等）、JUnit、CVS 整合、代码分析和创新的 GUI 设计等方面的功能都值得称道。至于 Eclipse 本人接触的不多，因此也无法比较，但殊途同归，无论选择什么集成开发环境，都是为了辅助咱们编程，所以可以说：**没有最好的工具，只有最适合自己的工具**。因此，撰写本系列文章的目的很简单，就是想把自己的经验整理记录下来，当然，如果能够在此基础上帮助大家快速入门并掌握 Intellij IDEA 那就再好不过啦！
  
- **注：此教程使用的工具版本为 IntelliJ IDEA 2017(.1.5)**


## 目录

第 1 篇：[在 Windows 系统下安装 IntelliJ IDEA 的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/install-intellij-idea-on-windows.md)

第 2 篇：[首次运行 IntelliJ IDEA 示例](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/first-run-idea.md)

第 3 篇：[IntelliJ IDEA 安装目录的核心文件讲解](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/core-file-talk.md)

第 4 篇：[详述 IntelliJ IDEA 的使用界面](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/use-face.md)

第 5 篇：[IntelliJ IDEA 之 HelloWorld 项目创建及相关配置文件介绍](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/hello-world.md)

第 6 篇：[设置 IntelliJ IDEA 主题和字体的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/theme-and-font.md)

第 7 篇：[修改 IntelliJ IDEA 模板注释中的 user 内容](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/modify-user-template.md)

第 8 篇：[IntelliJ IDEA 常见文件类型的图标介绍](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/idea-icon.md)

第 9 篇：[IntelliJ IDEA 缓存和索引的介绍及清理方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/index-and-cache.md)

第 10 篇：[IntelliJ IDEA 编译方式介绍及编译器的设置和选择](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/compile-method.md)

第 11 篇：[IntelliJ IDEA 中 Project 和 Module 的概念及区别](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/project-module.md)

第 12 篇：[IntelliJ IDEA 中的版本控制介绍（上）](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/version-control-one.md)

第 13 篇：[IntelliJ IDEA 中的版本控制介绍（中）](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/version-control-two.md)

第 14 篇：[IntelliJ IDEA 中的版本控制介绍（下）](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/version-control-three.md)

第 N 篇：XXXXXX

## 小技巧

第 1 篇：[详述 IntelliJ IDEA 中恢复代码的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/recovery-code.md)

第 2 篇：[详述 IntelliJ IDEA 中恢复代码的方法「进阶篇」](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/recovery-code-too.md)

第 3 篇：[IntelliJ IDEA 控制台输出中文乱码问题的解决方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/solve-garbled-questions.md)

第 4 篇：[详述 IntelliJ IDEA 中自动生成 serialVersionUID 的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/serialVersionUID.md)

第 5 篇：[详述 IntelliJ IDEA 提交代码前的 Code Analysis 机制](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/code-analysis.md)

第 6 篇：[关于 IntelliJ IDEA 中 Schedule for Addition 的问题](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/schedule.md)

第 7 篇：[详述 IntelliJ IDEA 设置 Sublime 代码颜色的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles-of-idea/code-color.md)

## 致谢

　　作为一个初学者，刚接触 IntelliJ IDEA 的时候，就有幸阅读了 [@Judas.n](https://github.com/judasn) 写的关于 IntelliJ IDEA 的教程，也获益良多。但是随着自己接触的越来越多，却发现 Judas.n 写的教程与最新版本的 IntelliJ IDEA 有些出入，因此决定自己重新写一份关于 IntelliJ IDEA 的教程，这也是此系列教程的来源。在此感谢 Judas.n 写的教程对我的启发，本教程也对 Judas.n 写的教程多有借鉴，下面附上其 GitHub 地址，欢迎感兴趣的童鞋移步到 Judas.n 的教程观摩学习。

- IntelliJ-IDEA-Tutorial: https://github.com/judasn/IntelliJ-IDEA-Tutorial 


----------
此外，附上一句格言，望共勉：**好学若饥，谦卑若愚。**


