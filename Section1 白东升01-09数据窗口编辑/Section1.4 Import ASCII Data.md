# Import ASCII Data

- [Import ASCII Data](#import-ascii-data)
    - [ASCII file import](#ascii-file-import)
        - [For simple ASCII File](#for-simple-ascii-file)
        - [ASCII File with other information, using the Import wizard](#ascii-file-with-other-information-using-the-import-wizard)
        - [ASCII file multi-import](#ascii-file-multi-import)
    - [Import Database data](#import-database-data)
    - [Excel import](#excel-import)
    - [Import Wizard](#import-wizard)

Datafile type:

Type|Detail
---|---
ASCII file|以行为单位，每一行用comma, space, tab来间隔数据形成所谓的列
Binary file|确定二进制的数据结构的时候才能正确导入
Database file|通过ADO接口导入的文件, e.g. excel, access, sql server, 先要进行查询操作

## ASCII file import

### For simple ASCII File

```bash
#data.txt
1   0.5   0.2
2   0.8   0.5
3   0.68    0.8
4   0.56789   0.58
5   0.12    0.5
6   0.36    0.25
```

3 methods:

1. 直接拖拽文件到Book进行覆盖
1. 拖拽到空白处进行新建
1. 外部打开文件，复制，然后在workbook中粘贴

### ASCII File with other information, using the Import wizard

```bash
#data.txt
experiment data: 2018-01-02
by Grey
time  data1 data2
1   0.5   0.2
2   0.8   0.5
3   0.68    0.8
4   0.56789   0.58
5   0.12    0.5
6   0.36    0.25
```

File/Import/Single ASCII…, you can check or uncheck the **Show Options Dialog**

![](res/import01.png)

Or you can use the Toolbar menu

![](res/import02.png)

![](res/import03.png)

And the 0 always means that the value is determined by the Program:

![](res/import04.png)

### ASCII file multi-import

When use the Multi-ASCII: **File/Import/Multi-Import** or

![](res/import05.png)

会导入数据到不同的book中

## Import Database data

![](res/import06.png)

![](res/import07.png)

![](res/import08.png)

## Excel import

![](res/import09.png)

4 methods:

1. copy-paste

    ![](res/import10.png)
1. Drag

    If there is no Dialog, you should Tools/Options(**Ctrl +U**)

    ![](res/import11.png)
1. File/Import/Excel
1. File/Open Excel(Ctrl +E)

    在Origin中新建的默认为Internal, 用Open Excel打开的默认External

    ![](res/import12.png)

## Import Wizard

File/Import/Import Wizard(Ctrl +3)

![](res/import13.png)

1. Source Window

    ![](res/import14.png)

    The Clipboard only allow use the ASCII data

1. Headline window

    ![](res/import15.png)

1. Variable Extraction Window

    ![](res/import16.png)

    对于复杂的数据表或者若干个数据表组，提取表头信息作为变量，在编程的时候对图形和数据进行注解

1. Filename window

    ![](res/import17.png)

    Let it be;

1. Data Columns

    ![](res/import18.png)

    Right click the A(Y),B(Y),C(Y), you can set format or designation

    ![](res/import19.png)

1. Data Selection

    ![](res/import20.png)

1. Save Filter to later used(let it be)

    ![](res/import21.png)

    When you check "Specify advanced filter options", there will be another window

    ![](res/import22.png)

**Append** another **Project** to current project: File/Append

如果有多个Import Filter文件，拖拽文件的时候就会出现, Select Filter Dialog

如果把导入后的workbook另存为Template, 会包含所有的导入参数，以后相似的文件，可以直接拖拽

还可以直接拖拽到Graph中绘制Graph