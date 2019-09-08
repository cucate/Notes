# 使用C++进行Win32编程

## 1. 什么是窗口

### 窗口类型

![Window](images/ApplicationWindow.png)  
上图称为程序窗口(Application Window)，包含标题栏、最大化、最小化按钮的这一部分叫做帧(Frame)，帧是非客户区域，由操作系统来管理，帧内部的白色区域则为客户区域，由编写的程序管理。

![Window](images/OkButton.png)  
这是另一种类型的窗口，UI控制必须放置在程序窗口上。

### 父窗口和附属窗口

![Window](images/window03.png)

程序窗口是控制窗口的父窗口，程序窗口是对话框窗口的拥有窗口，或者说对话框窗口是程序窗口的附属窗口。父窗口和子窗口的位置固定，子窗口不可能出现在父窗口外面，对话框窗口常显示在程序窗口前面，关系可表示如下：
![Window](images/window04.png)

## 2. 窗口句柄

窗口是一种对象，但不是C++的类的对象，程序通过一个值来引用窗口，这个值叫做句柄，句柄就是一个数，被操作系统用来标识一个对象，句柄不是指针，不指向某个值。