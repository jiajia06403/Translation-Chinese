`if`是允许我们定义条件的关键字。它具有以下结构： `if 条件 [ 命令 ]` 。如果给定条件为true（真），则软件将在方括号内运行提供的代码。如果给定条件为false（假），则软件将不执行任何操作。



```
ask cars [
	if my-speed < 60 [
		accelerate
	]
]
```


使用`if`时要记住的事情：

- 您可以使用`and`和`or`关键字组合两个或多个条件语句。
- 您可以使用`not`关键字将true（真）的语句设为false（假），反之亦然。
- 如果提供的条件为false（假），且您需要主体跟随一组单独的规则，则应使用`ifelse`关键字。


在下面的模型示例中，我们有一些代表捕鼠器的格子和一些随机移动的老鼠。如果老鼠踩在捕鼠器上，它会设置其`trapped?`变量为`true` 。 `not trapped?`的老鼠将继续四处走动，而被捕捉（`trapped?`）的老鼠则保持静止。
