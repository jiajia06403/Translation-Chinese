`create-turtles`是在模型中创建给定数量的新海龟的关键字。这些新的海龟都以相同的默认图形放置在模型的中心，但是具有随机的颜色和方向。此关键字的简写形式是`crt` 。



```
create-turtles 1015
crt 30
```


另外，我们可以使用方括号（ `[ ]` ）立即为新海龟提供一些命令。例如，以下代码不仅会创建100只新的海龟，还将所有这些海龟变成绿色，并使每只海龟都移动到一个随机格子。这样，我们就不需要使用单独的`ask`命令。



```
create-turtles 100 [
	set color green
	move-to one-of patches
]
```


使用`create-turtles`时要记住的事情：

- 您可以使用`create-<breed>`格式来创建特定自定义种类的新海龟，例如`create-dogs 100`或`create-buildings 5 [ set color gray ]` 。
- 只有`observer`可以创建新的海龟。您不能在`ask`关键字中使用此关键字。例如， `ask chickens [create-eggs 1]`和`ask patches [ create-plants 1 ]`都将显示错误消息。如果您需要已经存在的海龟来创建新的海龟，则应使用`hatch`关键字。如果需要格子来创建新的海龟，则应使用`sprout`关键字。


在下面的模型示例中，我们使用`create-turtles`命令创建带有房屋，一些植物，人，狗和云的景观。
