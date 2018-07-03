# Origin LabTalk

- [Origin LabTalk](#origin-labtalk)

Lab-Talk: 脚本语言，通过命令行批处理的方式实现功能，不需要编译，用的是C语言的语法

Open Command window:

- Window/command window;
- Alt + 3;

```bash
#simple example
1+sin(pi/6)=;

#Ctrl +Enter: 换行，不执行
Sum=0;
For(i=1;i<=100;i++)
{sum+=I;}
Sum=;
```

```bash
#new workbook
window -t;

#maximize the window
window -z;

#col(a)
col(a)=data(1,44,1);

#col(b)
for(i=1;i<=44;i++){col(b)[i]=ran();}

#col(c)
for(i=1;i<=44;i++)
{
  col(c)[i]=0;
  for(j=1;j<=i;j++)
  {
    col(c)[i]=col(c)[i]+col(b)[j];
  }
  col(c)[i]=col(c)[i]/i;
}

#plotxy and there is a space between 'plotxy' and '('
plotxy (col(a),col(c));
```

```bash
#Macro, 关闭originLab, macro消失
define macro1
{
window -t;
window -z;
col(a)=data(1,44,1);
for(i=1;i<=44;i++){col(b)[i]=ran();};
wks.addcol(C);
for(i=1;i<=44;i++)
{
  col(c)[i]=0;
  for(j=1;j<=i;j++)
  {
    col(c)[i]=col(c)[i]+col(b)[j];
  }
  col(c)[i]=col(c)[i]/i;
};
plotxy (col(a),col(c));}

#to run
>>macro1
>>macro1
>>macro1
```