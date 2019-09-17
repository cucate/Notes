# VS bug排除

1. 警告：对路径...的访问被拒绝  
通常是由于该程序上一次打开后还未关闭，可在任务管理器中将程序关闭后再执行。

2. 警告：C28251 "wWinMain"的批注不一致：此实例包含 无批注。
WinBase.h文件中wWinMain函数的声明是带批注的，加上与函数声明相同的批注就可以消除，批注详见SAL annotation。

3. 错误：MSB6006 “CL.exe”已退出，代码为 2
出错原因为一个类内部的定义的方法没有写return语句。或变量没有初始化。

4. 控件安装：
    在64位Windows下：
    64位exe和dll在目录c:\windows\system32目录下；
    32位exe和dll在目录c:\windows\syswow64目录下；
    所以要注意：
    在win64位系统下注册32位ocx或dll需要将32位ocx或dll拷贝到c:\windows\syswow64\目录下。
    且注册要用c:\windows\syswow64\regsvr32 xxxxxxx.ocx或dll
