`pen-down` （简写为`pd` ）用于绘制海龟的运动轨迹。画笔的颜色和海龟的颜色是一致的。 `pen-down`开始绘制时，使用`pen-up` （简写为`pu`）可以停止绘制海龟的运动轨迹。想像一下，`pen-up`和`pen-down`像海龟的腹部上的一个画笔; `pen-down`可将画笔放到地面上，留下痕迹，而`pen-up`放笔可将画笔往上提，不再留下痕迹。 `Pen-down`和 `pen-up`是海龟命令。例如，如果我们希望海龟画一个正方形，我们将编写以下代码：



```
ask turtles [
	pen-down
	repeat 4 [
		right 90
		forward 5
	]
	pen-up
]
```


在下面的模型中，一架飞机在两个神话中才有的目的地之间飞行：亚特兰蒂斯和瓦尔哈拉。在飞行过程中，当`draw-path?`控件开关打开时，飞机回留下痕迹。飞机每次到达目的地并转向时，都会更改其颜色，从而产生新的轨迹颜色。如果`draw-path?`开关关闭后，我们的飞机将“提起画笔”停止绘制轨迹。当`draw-path?`打开时，我们还使用`clear-drawing`关键字（简写为`cd`）清除所有先前的轨迹。请注意， `clear-drawing`是仅用于观察者的关键字，因此我们只能在`ask turtles`语句之外使用它。
