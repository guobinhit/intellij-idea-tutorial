# 详述 IntelliJ IDEA 遇到快捷键以及删除键不好使的解决方法

## 问题背景

在 IntelliJ IDEA 的使用过程中，尤其是在我们安装后首次使用的时候，我们可以会遇到两个问题：

- **常用的快捷键不好使**
- **选中多行代码，按删除键不好使**

![choose-code](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/keymap-delete/choose-code.png)

如上图所示，这就是选中了多行代码，但按删除键不好使的情况。


## 解决方法
### 第一个问题：快捷键不好使

对于这个问题，常见于我们首次安装 IDEA，其默认的快捷键模式并不一定是我们习惯的，因此修改快捷键模式即可。

![keymap](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/keymap-delete/keymap.png)

如上图所示，依次进入`IntelliJ IDEA -> Preferences -> Keymap`配置页面，然后选择我们常用的快捷键模式就可以了。

### 第二个问题：删除键不好使

对于这个问题，实际上，它并不一定是问题，因为在我们选择了不同的编辑模式后，就有可能出现快捷键以及删除键“不好使”的情况。

![tools-vim](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/difficult-cases/keymap-delete/tools-vim.png)

如上图所示，我们设置了`Vim Emulator`编辑模式，这时我们常用的非`vim`编辑器模式下的快捷键自然也就是失效了。

既然我们知道了出现问题的原因，那么通过`Tools`菜单栏取消该编辑模式即可。

----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
