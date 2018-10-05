# Origin Matrix

<!-- TOC -->

- [Origin Matrix](#origin-matrix)
    - [New Matrix](#new-matrix)
    - [Convert Between Matrix & workbook](#convert-between-matrix--workbook)
        - [Workbook to matrix](#workbook-to-matrix)
        - [matrix to workbook](#matrix-to-workbook)

<!-- /TOC -->

## New Matrix

Matrix View:
- View/Show X,Y
- View/Show Column/Row

Matrix value
> ![](res/matrix01.png)

convert to workbook
> ![](res/matrix02.png)  
> Expand: using interpolation method, Bi-Linear  
> Shrink: using interpolation method, average  

Insert or Add Matrix
> ![](res/matrix03.png)

## Convert Between Matrix & workbook

### Workbook to matrix

Select workbook, Worksheet/Convert to Matrix/
> ![](res/matrix04.png)  
> Direct:Too easy  
> Expand:  

Expand失败的例子:Factor=2, orientation=row,原来的两行变成1行，原始的两行数据必须是满的

![](res/matrix05.png)

Expand失败的例子:Factor=2, orientation=column,原来的两列变成1列，原始的两列数据必须是满的

![](res/matrix06.png)

### matrix to workbook

![](res/matrix07.png)