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

5. LINK: fatal error LNK1123: failure during conversion to COFF: file invalid or corrupt.
这是一个链接器错误，原因是VS用来COFF格式转换的工具cvtres.exe被破坏了，被破坏的原因是装了更新版本的VS，新的.Net
 Framework里自带一个更新的cvtres.exe，解决方法，将VS2010里原来的两个cvtres.exe删掉或改名就好了，文件夹为
C:\(vs2010安装文件夹)\VC\bin\cvtres.exe和C:\(vs2010安装文件夹)\VC\bin\amd64\cvtres.exe。

6. 错误: C2065 "IDC_...": undeclared identifier.
在`Resourse.h`文件里看看控件ID的定义是不是有问题。

7. 警告: C6387 `<argument>` may be `<value>`: this does not adhere to the specification for the function `<function name>`.
函数的批注中有`_In_`，表示该参数必须有效，所以不能为`NULL`，解决方法为在前面用判断语句判断该值是否为`NULL`，注：该判断语句必须和使用该参数的函数在同一代码块。

8. 警告：C26115 Failing to release lock `<lock>` in function `<func>`.
程序中可能会造成孤立锁，如使用`EnterCriticalSection`后，后面根据条件判断使用`LeaveCriticalSection`时，部分条件没有使用该语句，导致满足该条件时，
没有开锁，从而形成孤立锁。

9. 调试过程中出现"read access violation"。
编译可以通过但运行不了，调试出现这个异常，可能原因是在局部重新定义了和成员变量同名的对象，导致成员变量在局部被隐藏，而局部变量离开作用域就消失了。
