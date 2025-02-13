`other`返回一个主体集合，这个主体集合会排除来源主体。当我们希望海龟相互连接时，它非常有用。例如，如果我们想创建一个网络模型，其中每个海龟都通过链接连接到另一个随机挑选的海龟，我们将编写以下代码：



```
ask turtles [
	create-link-with one-of other turtles
]
```


我们在这种情况下使用`other`是因为如果我们不这样做， `one-of turtles`可能会返回同一个海龟。如果发生这种情况，编译器将显示错误，因为海龟无法与自己建立链接。

在下面的模型示例中，我们有一些随机分布在世界中的静止的海龟代表人，我们有一个代表医生的移动的海龟。医生会四处随机走动，当遇到`other turtles` 时，它会要求同格子上的其他海龟在健康时变绿，在被感染时变红。
