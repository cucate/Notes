# Excel笔记

## 一、Excel软件简介

### Excel能做什么

* 数据存储
* 数据处理
* 数据分析
* 数据呈现

### 基础操作

工作簿、工作表、单元格基础操作：  

1. 新建工作表

2. 更改工作表标签颜色

3. 插入/删除多个工作表

4. 插入行/列，插入多行/列，移动行/列，调整行高列宽
    * 插入行/列：右键点击行号选择插入，删除同理  
    * 移动行/列：选中行/列，鼠标放在边框上（出现四箭头光标）点击拖拽，按住`Shift`拖拽可以交换顺序。  
    * 调整行高列宽：选中行/列，鼠标放在行/列号的边框上（出现两箭头光标），点击拖拽改变列宽，双击使单元格大小为容纳内容的最小宽度。选择多列可以同时调整多列
5. 单元格选取、整行整列选取、数据区域选取。
    * 小技巧：选中单元格，鼠标放在下边线（出现四箭头光标）双击，可以直接定位到该列的最后一个单元格。同理可以双击上左右边线。
    * 也可以用快捷键`Ctrl + ↑/↓/←/→`完成相应操作，`Ctrl + Home/End/PgUp/PgDn`可以起到定位工作表首/末单元格、工作表切换的功能。

### 实用小工具

1. 冻结窗格
    * 在拖动滚动表格是使某一行不动，如固定表头。选定某单元格冻结可以使该单元格上方的行和左边的列都冻结。

2. 自动填充
    * 选择单个单元格，鼠标放在边框右下角（出现十字光标）点击拖拽可以复制当前内容。选择连续两个单元格，拖拽可以形成等差序列。
    * 选择单个单元格，直接拖拽进行复制，按下`Ctrl`键拖拽形成序列。
    * 选择单个单元格，右键拖拽可以选择填充方式。
    * 文件->选项->高级里可以自定义自动填充序列。

3. 插入时间
    * 选择单元格，按下快捷键`Ctrl + ;`插入日期，按下`Ctrl + Shift + ;`插入时间。
    * 按照技巧2直接拖拽日期可以得到以天递增的日期，按下`Ctrl`键拖拽进行复制，直接拖拽时间可以得到以小时递增的时间。

## 二、单元格格式设置

### 单元格格式美化工具

1. 选择单元格，右键选择设置单元格格式可以设置单元格所有格式。

2. 分列工具，可以对数值显示格式进行转换，如文本转日期。

## 查找、替换与定位

### 查找与替换

1. 按值查找
    * 替换时选择单元格匹配：只有单元格内容与查找内容完全一致时会被替换。
2. 按格式查找
    * 替换时选择格式，可以选择单元格格式，如填充。
3. 模糊查找
    * 使用`'*','?'`等通配符进行模糊查找。
    * `'?'`只代表一个字符，`'*'`代表所有字符。
    * 若要替换的值中带有`'*'`，则在`'*'`前加`'~'`使通配符不起作用。

### 定位工具

1. 通过名称框定位
2. 可以在名称框里定义区域名称
3. 使用定位条件
    * 批注：右键单元格选择批注，有批注的单元格右上角有红色小三角。
    * 选择定位条件，可以定位不同类型的对象。

## 排序和筛选