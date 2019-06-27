# 详述 IntelliJ IDEA 插件的安装及使用方法

> **温馨提示**：IntelliJ  IDEA 支持非常多的插件，熟练的使用插件，能够有效提高我们的开发效率以及用户体验。

## 正文

首先，进入插件安装界面：

 - Mac：`IntelliJ IDEA` -> `Preferences` -> `Plugins`;
 - Windows：`File` -> `Settings` -> `Plugins`.

![preferences-plugins](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/plugins/preferences-plugins.png)

- **标注 1**：显示 IntelliJ IDEA 的插件分类，
  - `All plugins`：显示 IntelliJ IDEA 支持的所有插件；
  - `Enabled`：显示当前以前启用的插件；
  - `Disabled`：显示当前未启用的插件；
  - `Bundled`：显示 IntelliJ IDEA 所有自带的插件；
  - `Custom`：显示我们自己安装的插件。
- **标注 2**：打钩`√`表示为已经启用的插件；
- **标注 3**：安装  JetBrains 开发的插件；
- **标注 4**：安装插件仓库提供的插件；
- **标注 5**：安装本地已经下载完的插件。

如上图所示，显示了 IntelliJ IDEA 对插件的良好支持。以阿里巴巴最近新推出的「阿里巴巴代码规范检查插件」为例，在搜索区输入`Alibaba`，就会显示出相近名称的插件（如果显示`No Plugins found`，则点击`Serach in repositories`进行仓库搜索），然后点击`Install`，即可安装此插件。在此，需要注意的是：**插件安装成功后，需要重新启动 IntelliJ IDEA 使插件生效**。

![alibaba-java-coding-guidelines](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/plugins/alibaba-java-coding-guidelines.png)

此外，当我们创建一个 IntelliJ IDEA 当前配置并不支持的文件格式时，IntelliJ IDEA 会自动识别此文件，并提示我们下载对应的插件，对其进行支持。如下图所示，我们创建了一个名为`MarkdownPlugins.md`的 Markdown 格式的文件，但当前我们的 IntelliJ IDEA 并没有支持 Markdown 的插件，这时 IntelliJ IDEA 就会自动提示我们安装 Markdown 插件：

![markdown-plugins](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/plugins/markdown-plugins.png)

如上图所示，当我们点击`Install plugins`之后，选择对应的插件下载并安装（自动），然后重新启动 IntelliJ IDEA，并输入 Markdown 格式的内容，进行测试：

![test-markdown-plugins](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/plugins/test-markdown-plugins.png)

如上图所示，显然 Markdown 插件安装成功，IntelliJ IDEA 已经能够识别 Markdown 的语法啦！

### 常用插件推荐

| 插件名称 | 插件介绍 | 官网地址 |
| ------------- |:-------------| :-----|
|Alibaba Java Coding Guidelines|	阿里巴巴代码规范检查插件	|https://plugins.jetbrains.com/plugin/10046-alibaba-java-coding-guidelines|
|Key promoter	|快捷键提示插件	|https://plugins.jetbrains.com/plugin/4455?pr=idea|
|Grep Console	|自定义控制台输出格式插件|	https://plugins.jetbrains.com/idea/plugin/7125-grep-console|
|CheckStyle-IDEA|	代码规范检查插件	|https://plugins.jetbrains.com/plugin/1065?pr=idea|
|FindBugs-IDEA	| 潜在 Bug 检查	|https://plugins.jetbrains.com/plugin/3847?pr=idea|
|MetricsReloaded	|代码复杂度检查	|https://plugins.jetbrains.com/plugin/93?pr=idea|
|Statistic	|代码统计插件|	https://plugins.jetbrains.com/plugin/4509?pr=idea|
|JRebel Plugin	|热部署插件|	https://plugins.jetbrains.com/plugin/?id=4441|
|CodeGlance	|显示代码地图插件	|https://plugins.jetbrains.com/plugin/7275?pr=idea|
|Markdown Navigator|	Markdown 编辑器插件|	https://plugins.jetbrains.com/plugin/7896?pr=idea|
|Eclipse Code Formatter|	Eclipse 代码风格格式化插件	|https://plugins.jetbrains.com/plugin/6546?pr=idea|
|Jindent-Source Code Formatter	|自定义模板插件	|http://plugins.jetbrains.com/plugin/2170?pr=idea|
|Maven Helper|	Maven 辅助插件	|https://plugins.jetbrains.com/plugin/7179-maven-helper|
|Properties to YAML Converter|	Properties 转 YAML 格式插件	|https://plugins.jetbrains.com/plugin/8000-properties-to-yaml-converter|
|Git Flow Integration|	Git Flow 集成插件	|https://plugins.jetbrains.com/plugin/7315-git-flow-integration|






----------

———— ☆☆☆ —— 返回 -> [史上最简单的 IntelliJ IDEA 教程](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) <- 目录 —— ☆☆☆ ————
