# Origin C

- [Origin C](#origin-c)
    - [Example: 输出乘法表](#example-%E8%BE%93%E5%87%BA%E4%B9%98%E6%B3%95%E8%A1%A8)
    - [Example: 自定义按钮](#example-%E8%87%AA%E5%AE%9A%E4%B9%89%E6%8C%89%E9%92%AE)
    - [Example: 自定义工具栏按钮](#example-%E8%87%AA%E5%AE%9A%E4%B9%89%E5%B7%A5%E5%85%B7%E6%A0%8F%E6%8C%89%E9%92%AE)

处理大数据的时候，速度较快

- View/Code Builder;
- Alt+4

OriginC vs C:

- Origin C不支持C language的main函数
- 与C语言一样，OriginC也不是完全OOP架构的的语言，由一些基本数据类型、一些全局函数、大量的class构成
- OriginC不支持2维以上的数组，二维数组用matrix代替`matrix<int> myMatrix(4,3)`
- OriginC中`^`表示幂

OriginC vs C++:

OriginC vs C#:

![](res/originc01.png)

## Example: 输出乘法表

```c
//test.c
#include <Origin.h>

void fillnumbers()
{
    matrix mat(9,9);
    for(int x=0;x<mat.GetNumRows();x++)
    {
        for(int y=0;y<=x;y++)
        {
            mat[x][y]=(x+1)*(y+1);
            printf("%d*%d=%g ",x+1,y+1,mat[x][y]);//注意%g
        }
        printf("\n");
    }
}
```

![](res/originc02.png)

## Example: 自定义按钮

```c
//customBtn.c
// Start your functions here.
void plot(string strTemplate, string strData)
{
	GraphPage grph;
	BOOL bOK=grph.Create(strTemplate,CREATE_VISIBLE);
	if(!bOK)
		return;
	GraphLayer grlay=grph.Layers(0);
	Curve cv(strData);
	int nplot=grlay.AddPlot(cv);
	if(nplot>=0)
	{
		grlay.DataPlots(nplot).SetColor(2,TRUE);
		grlay.Rescale();
	}
}
```

Add a text to the workbook, right-click, **Programming Control**

![](res/originc03.png)
![](res/originc04.png)

![](res/originc05.png)

## Example: 自定义工具栏按钮

New a ogs file:

![](res/originc06.png)

View/Toolbar:

![](res/originc07.png)

![](res/originc08.png)

![](res/originc09.png)

Tip: 按住Ctrl +Shift同时点击，自动跳转到对应的C代码