`move-to`允许海龟将其x和y坐标设置为与另一只海龟或格子相同的x与y，而无需更改海龟的其他变量（例如，方向，颜色，大小）。例如，如果我们正在建立一个在房屋之间移动的人的模型，其中房屋和家庭都用房屋形状来表示，我们将编写以下代码：



```
ask families [
	if my-house != nobody [
		set my-house one-of houses
		move-to my-house
	]
]
```


在下面的模型示例中，我们有一个简单的环境。我们的一些格子是代表土地的棕色，而另一些格子是代表水的蓝色。在这种环境下，我们存在一些虫子，它们只需要在棕色补丁上移动即可。首先，我们在*setup*过程使用`move-to`关键字将每个虫子放置在随机的一个棕色格子上。其次，我们使用`move-to`关键字（而不是`forward` ）来让我们的虫子选择一个随机的，相邻的棕色补丁并移至该格子。
