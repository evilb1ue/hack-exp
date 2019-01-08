# GCC

> gcc安全编译参数（gcc (Debian 8.2.0-9) 8.2.0测试）：   
> * NX：-z execstack / -z noexecstack (关闭 / 开启（默认）)   
> * Canary：-fno-stack-protector /-fstack-protector / -fstack-protector-all (关闭（默认）/ 开启 / 全开启)  
>   * -fstack-protector:启用堆栈保护，不过只为局部变量中含有 char 数组的函数插入保护代码  
>   * -fstack-protector-all:启用堆栈保护，为所有函数插入保护代码    
> * PIE：-no-pie / -pie (关闭 / 开启（默认）)  
>   * -no-pie：可以直接使用  
>   * -pie: -pie 用于链接,但要生成PIE程序，必须配合使用-fpie或-fPIE,-fpie与-fPIE用于编译,单独使用是无法达到效果的。   
>   * 注:These options(-fpie -fPIE) are similar to -fpic and -fPIC, but generated position independent code can be only linked into executables. Usually these options are used when -pie GCC option will be used during linking.-fpie and -fPIE both define the macros \_\_pie\_\_ and \_\_PIE\_\_. The macros have the value 1 for -fpie and 2 for -fPIE.  
> * RELRO：-z norelro / -z lazy / -z now (关闭 / 部分开启（默认）/ 完全开启)  

