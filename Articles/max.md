`max`报告给定列表中的最大值。例如， `show max [14 -2 7]`将返回14. `max`常用于找到一个主体集合内的特定主体。例如，如果我们要创建一个细胞分裂模型，并在每个周期处将最大的细胞分裂变为两个，我们将编写以下代码：



```
ask cells [
	if size = max [size] of cells [
		set size (size / 2)
		hatch 1
	]
]
```



在下面的模型示例中，我们有一些人代表了一个非常简单的经济体。在每个时间步，随机选择的海龟通过随机选择另一只海龟并给该海龟5 个单位的钱来执行交易。这种交换用两只海龟之间的临时链接来表示。我们使用`max`将最富有（钱最多）的海龟的颜色更改为蓝色。我们还使用`min`将最穷（钱最少）的海龟的颜色更改为红色。
