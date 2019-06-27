# 详述 IntelliJ IDEA 之 Debug 篇


在我们的编程生涯中，调试代码是免不了的，而如何调试代码就显得尤为重要了，其中利用 IDE 自带的调试工具，是我们快速定位问题的重要手段之一。在此，我们就一起来了解一下 IntelliJ IDEA 自带的调试工具，熟悉常用的`Debug`技巧。

![debug-common-button](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/debug-skills/debug-common-button.png)

- **标注 1**：`Show Execution Point `，显示执行端点(`Alt + F10`)；
- **标注 2**：`Step Over`，跳到下一步(`F8`)；
- **标注 3**：`Step Into`，进入代码或者说进入到方法内部(`F7`)；
- **标注 4**：`Force Step Into`，强制进入代码或者说进入到方法内部(`Alt + Shift + F7`)；
- **标注 5**：`Step Out`，跳到下一个断点或者跳出方法(`Shift + F8`)；
- **标注 6**：`Drop Frame`，放弃当前 debug，重新执行 debug；
- **标注 7**：`Run to Cursor`，运行到光标处(`Alt + F9`)；
- **标注 8**：`Evaluate Expression`，评估表达式；
- **标注 9**：`View Breakpoints`，查看断点，展示更多高级设置；
- **标注 10**：`Mute Breakpoints`，置灰所有断点，再次点击，恢复；
- **标注 11**：`Get thread dunp `，获得当前的线程堆栈。

如上述所示，都是一些常用的功能。其中，点击 **标注 9** 所示的`View Breakpoints`按钮，如下图所示：

![show-breakpoints-control](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/debug-skills/show-breakpoints-control.png)

- **标注 1**：`View Breakpoints`，查看断点，展示更多高级设置；
- **标注 2**：`Java Line Breakpoints`，展示项目中设置的所有断点；
- **标注 3**：`Conditions`，设置条件断点；
- **标注 4**：`Remove once hit`，设置击中一次断点后，取消该断点；
- **标注 5**：`Pass count `，设置当循环若干次后，进入断点，常用于循环语句。

在上述的标注中，通过 **标注 3** 我们可以很方便的设置条件断点；通过 **标注 4** 我们可以设置一次性断点，不用我们每次手动的设置和取消断点；通过 **标注 5** 我们可以设置更加高级的断点击中条件。特别地，在`Debug`模式下，我们也可以双击鼠标右键，唤出常用的工具菜单，其效果如下图红框标记所示，提供了评估表达式、进入光标位置、强制进入光标位置和添加`Watches`等快捷按钮：

![double-click-right-key](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/debug-skills/double-click-right-key.png)

当我们点击`Evaluate Expression`按钮之后，会弹出如下界面：

![evaluate-expression](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/debug-skills/evaluate-expression.png)

- **标注 1**：`Condition expression`，待评估的表达式；
- **标注 2**：`Evaluate`，评估按钮，点击后进行评估。

此外，在评估表达式的时候，我们并不一定非得输入代码中的现有的表达式，可以按实际需要，自定义表达式，而且 IntelliJ IDEA 提供了代码提示功能，很方便。熟练的使用上述功能，可以有效的提高我们的调试效率，祝大家好运！


----------

———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————


