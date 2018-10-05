# 2D Plot

<!-- TOC -->

- [2D Plot](#2d-plot)
    - [Group to change color](#group-to-change-color)
    - [2D Plot feature and application](#2d-plot-feature-and-application)
    - [Excel Plot](#excel-plot)
    - [Function Plot](#function-plot)
    - [Summary](#summary)
    - [statistics plot](#statistics-plot)

<!-- /TOC -->

workbook的绘图类型比matrix的绘图类型多一些

When want to plot the Y, it will auto find its X

Add a Y to existed Graph:
> ![](res/2plot01.png), then drag to Graph

## Group to change color

先取消所有Group, 然后再将它们弄到一个Group就可以实现颜色的区分了
> ![](res/2plot02.png)

具体的绘图：
> ![](res/2plot03.png)

- 红色部分可以和workbook中的不一致，绘图的结果以这个为准，不影响workbook中的数据
- 不同的Plot Type, 不能放到同一个Group中

使用workbook指定的XY…
> ![](res/2plot04.png)

把Word中的Origin Graph生成数据：双击word中的Graph,进行编辑，Create Workbook
> ![](res/2plot05.png)

## 2D Plot feature and application

- Line Series用于比较two colums的匹配度，只需要两个Y列。交叉较少表示匹配度高
> ![](res/2plot06.png)

- Multi-Y, Multi-Panel只是Layer的特殊应用而已
- 3D waterfall Y:Color Mapping这是沿着Y轴方向涂上了颜色
- 3D waterfall Z:Color Mapping这是沿着Z轴方向涂上了颜色
- Trellis Plot not understand
> ![](res/2plot07.png)

box chart
> ![](res/2plot08.png)  
> ![](res/2plot09.png)

- for Matrix, HeatMap is easy; for workbook, first it require that you convert the Data following the warning
- Tenary will normalized the X,Y,Z(that is to say, x+y+z=1)
- Piper not understand
- Smith Chart用于微波射频电路中，表征电阻电抗
> ![](res/2plot10.png)

## Excel Plot

Plot/Line/, Select the column as X, Y, Z…, and if you want to set multi-Y, you should multi-select Y at the same time
> ![](res/2plot11.png)

## Function Plot

<kbd>Ctrl</kbd>+<kbd>N</kbd>, Function

要先是设置坐标系，然后再添加图层，否则切换坐标系之后，之前的设置都没了

## Summary

Plot/Multi-Panel适合于不同自变量的数据，但是放到同一个Graph中；

Plot/Multi-Panel/Stack适合相同自变量，不同y的情况；

wind Rose:根据某一地区多年平均统计的各个方向风向的频率分布；

添加Layers:
- Layer Management
- Graph/New Layer
- Graph/Merge Graph windows
- Graph Toolbar

一般流程，先得到一个Graph1,然后得到一个Graph2，然后Graph/Merge Graph Windows/，得到的结果然后Tools/ThemeOrganizer/Physics Reveiw Letter/Apply

将一个Graph复制到另一个Graph中有两种方法：copy与copyPage

## statistics plot

如果用了plot/Statistics/Histogram之后，可以右击Graph/Go to Bin worksheet可以查看
- Bin center(区间段中心值)
- Counts
- Cumulative Sum
- Cumulative Probability

在PlotDetail对话框中的Data选项卡中的Type中修改**Type=Normal**可以添加正太曲线

