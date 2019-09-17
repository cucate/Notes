# NumPy学习

## ndarray数组创建方法

1. 用`array`函数将普通列表和元组转化为ndarray数组。可指定数组的类型。
2. 用`zeros`,`ones`函数创建全为零的数组。
3. `arange`函数，类似于`range`。

## 基本操作

1. Python中的`+`,`-`,`*`,`/`,`**`都是按元素运算进行的（可使用`+=`等运算符），与matlab相反，相当于matlab的`.*`的运算。
2. 矩阵乘法，用`@`运算符（in python >= 3.5），或使用`dot`方法。
3. 操作两种不同类型的数据时，结果类型取更精确的一种。(upcasting)
4. 求和之类操作，为ndarry类的方法。如sum()方法，可指定维数，如sum(axis=1)。(min(), max(), cumsum())。
5. 基本数学函数，为模块NumPy的函数，称为通用函数(Universal Functions)。如exp(),sqrt(),add()等。

## 索引，切片和迭代

* 和Python普通列表基本相似。

>补：Python迭代比C语言更加抽象，不依赖于下标，只要是可迭代对象都可以迭代。
>列表生成式：如[x * x for x in range(10)]。
>生成器（generator）：①将列表生成式的方括号`[]`换为圆括号`()`。
>②使用`def`定义‘函数’，用`yield`来输出返回值，用`next`获取一次`yield`的返回值。
>可用于迭代的对象：数据类型list, tuple, dict, set, str等，和generator。
>迭代器（iterator）：generator都是迭代器，列表等数据类型可迭代，但不是迭代器。
