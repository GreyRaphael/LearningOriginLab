# With Other Math program

<!-- TOC -->

- [With Other Math program](#with-other-math-program)
    - [with Matlab](#with-matlab)
    - [with Mathematica](#with-mathematica)
    - [with LabView](#with-labview)

<!-- /TOC -->

## with Matlab

Origin可以直接导入MATLAB的.mat文件:File/Import/Matlab

Tools/MATLAB console: 可以在不打开MATLAB的基础上，调用kernel

数据交换: Tool/MATLAB console
- Pr: origin's real matrix to matlab;
- Gr: matlab's real matrix to origin;

- Pc: origin's complex matrix to matlab;
- Gc: matlab's complex matrix to origin;

- Pwr: origin workbook to matlab

    Pwr [Book1]Sheet1!col(A) P1

    P1 is the variable in matlab
- Pwc: origin workbook complex data to matlab

- Pws: origin workbook string to matlab

- Gwkspace m: matlab all variables to origin's matrix

- Gwkspace w:matlab all variables to origin's workbook

## with Mathematica

Tools/Mathematica link(choose the Kernel)

## with LabView

Tools/Copy Origin Sub-VI to LabView