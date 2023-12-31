---
layout: post
title: python简易教程
date: 2018-01-29
categories: 技术
---

## 安装

#### python运行环境安装

* mac环境

  * 安装依赖包：`brew install python3`
  * 检查python版本`python -V`

* window环境

  * 安装包[下载](https://www.python.org/downloads/windows/)并安装
  * 环境变量中添加Python目录
  * 环境检查`python -V`

  [激活教程](https://blog.csdn.net/u014044812/article/details/78727496)

#### pycharm安装

* 下载[地址](https://www.jetbrains.com/pycharm/)
* 执行下载安装包
* 点击`Create New Project`
* 输入项目名、路径、选择`python解释器`

#### pycharm使用

* 编辑器设置 - 字体大小设置`Settings-->Editor-->Colors & Fonts-->Font`
* 断点调试
   1. 设置断点 - 鼠标单击进行设置断点
   2. 运行断点 - 点击那个绿色的甲虫图标进行断点调试
* 搜索
   * 全局搜索`Ctrl + Shift + F`
   * 当前文件搜索`Ctrl + F`
   * 文件跳转`Ctrl + Shift + O`
* 快捷键
   * ctrl+alt+t：弹出下拉菜单，选择可使用范围控制结构
   * ctrl+alt+l：代码格式化
   * F8 :单步调试
   * F9 :debugger模式执行
   * ctrl+shift+F8:查看断点
   * ctrl+alt+S:settings面板弹出

   * python目录说明(`基于macOS系统`)
       * bin - python可执行文件
       * etc
       * headers
       * include - Python提供的所有头文件
       * lib - Python标准库
       * Resources - python标准库文档
       * share - 案例和帮助说明

## python基础

#### 输入/输出

1. `input("请输入：")`是python内置标准输入函数,默认读取键盘输入
2. 标准输出:`print("The length of %s is %d" % (s,x))`

[参考](http://www.runoob.com/python3/python3-inputoutput.html)

#### 变量

标准数据类型：

  * Numbers(数字)
  * String(字符串)
  * List(列表)
  * Tuple(元组)
  * Dictionary(字典)

>列表操作:

  1. 内置函数
      * cmp(list1,list2)  比较两个列表的元素
      * len(list) 返回列表长度
      * max(list) 返回列表最大值
      * min(list) 返回列表最小值
      * list(seq) 将元组转化为列表
  2. 实例操作函数
	  * append(obj) 在列表末尾插入新对象
	  * insert(index,obj) 将对象插入列表指定位置
	  * count(obj) 统计元素出现次数
	  * extend(seq) 追加序列的多个元素
	  * index(obj) 返回元素第一个匹配项位置
	  * pop(obj) 移除列表的第一个匹配项，并返回元素值
	  * remove(obj) 移除项目指定值
	  * reverse() 将列表反向操作
	  * sort([func]) 将列表进行排序
3. 遍历操作

* 方法一:

```
    for i in list:
      print("序号：%s   值：%s" % (list.index(i) + 1, i))
```

* 方法二:

```
    for i in list:
      print("序号：%s   值：%s" % (list.index(i) + 1, i)) 
```

* 方法三:
  
```
    for i in list:
      print("序号：%s   值：%s" % (list.index(i) + 1, i))        
```

>字典操作:

  1. 内置函数
	  - cmp(dict1,dict2) 比较两个字典元素
	  - len(dict) 返回字典长度
	  - str(dict) 返回字典的字符串表示
	  - type(varivable) 返回元素类型
  2. 实例操作函数
	  - clear() 删除字典内所有元素
	  - copy() 字典浅复制操作
	  - items() 返回字典元组数组
	  - keys() 返回字典所有键
	  - values() 返回字典所有值
	  - fromkeys(sequence[,val]) 根据元组创建新字典,可设置初始值
	  - get(key) 返回字典指定键值，不存在则返回默认值
	  - has_key(key) 判断指定键值是否存在
	  - setDefault(key,default) 判断指定键值是否存在，不存在则设置默认值
	  - update(dict2) 将新字典更新到字典内
	  - pop(key) 删除指定键值，并返回删除值
	  - popitem() 随机删除一对键值
3. 遍历
  1. 方法一:

```
    for key in d:
       print key, 'corresponds to', d[key]
```

  1. 方法二:

```
    for key, value in d.items():
       print key, 'corresponds to', value    
```

><span style="color:red">del语句删除一些 Number 对象引用</span>

### 运算符

  - 算术运算符`+`,`-`,`*`,`/`,`%`,`**`,`//`
  - 关系运算符`==`,`!=`,`<>`,`<`,`>`,`>=`,`<=`
  - 赋值运算符`=`,`+=`,`-=`,`*=`,`/=`,`%=`,`**=`,`//=`
  - 位运算符`&`,`|`,`^`,`~`,`<<`,`>>`
  - 逻辑运算符`and`,`or`,`not`
  - 成员运算符`in`,`not in`
  - 身份运算符`is`,`is not`

### 注释

  * 单行注释`#`
  * 多行注释`'''`

### 函数/模块

>函数是组织好的，可重复使用的，用来实现单一，或相关联功能的代码段

    def functionname( parameters ):
      "函数_文档字符串"
      function_suite
      return [expression]

参数传递:
  - 必备参数
  - 关键字参数
  - 默认参数
  - 不定长参数      

lambda表达式:

### 包

>注意：任意包含 __init__.py 文件的目录都被认为是一个Python包

<h4 style="color:red">包和模块的区别？</h4>

### 文件I/O

文件操作函数:

  - close()关闭文件
  - flush()刷新文件内部缓冲
  - fileno()返回文件整型描述符
  - isatty()判断文件是否连接终端
  - next()返回文件下一行
  - read([size])从文件读取相应字节数
  - readline([size])读取整行
  - readlines([sizehint])读取所有行并返回列表
  - seek(offset[,whence])设置文件当前位置
  - tell()返回文件当前位置
  - truncate([size])文件截取
  - write([str])将字符串写入文件
  - writelines(sequence)向文件写入一个序列字符串列表

### 异常

(1) 异常处理:

    try:
    <语句>        #运行别的代码
    except <名字>：
    <语句>        #如果在try部份引发了'name'异常
    except <名字>，<数据>:
    <语句>        #如果引发了'name'异常，获得附加的数据
    else:
    <语句>        #如果没有异常发生

(2) 异常自定义:

    class Networkerror(RuntimeError):
      def __init__(self, arg):
          self.args = arg

## python扩展

#### 函数式编程

#### 面向对象编程

类定义:
属性定义:
内置类属性:

`区分静态变量和实例变量`
`区分静态函数和实例函数`
`变量作用域`

#### 进程和线程

#### 网络编程

#### 数据库连接

(1)数据库模块包`mysql-connector-python`
  a. 安装:`pip install mysql-connector-python`
  b. 模块包导入: `import mysql-connector`

(2)数据库连接:
a. 获取数据库连接
> conn = mysql.connector.connect(host="218.61.208.122", port="3306", user="root", password="shgd_2017", database="test", use_unicode=True)

b. 获取数据库操作实例
> cursor = conn.cursor()

(3)数据库操作
a. 查询语句执行
> cursor.execute(" select * from tableName")
> values = cursor.fetchall()

b. 动作语句执行
> cursor.execute("INSERT INTO tableName(cloumns_name1,cloumns_name2) VALUES (cloumns_value1,columns_value2)")
> conn.commit()

## python函数库

