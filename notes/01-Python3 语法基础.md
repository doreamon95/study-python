# 01-Python 3 语法基础

## 1. 编码

默认情况下，Python 3源码文件以 UTF-8 编码，所有字符串都是 unicode 字符串。

## 2. 标识符

- 第一个字符必须是字母表中字母或下划线'_'。
- 标识符的其他的部分有字母、数字和下划线组成。
- 标识符对大小写敏感。

在Python 3中，非-ASCII 标识符也是允许的了。

变量类型硬性要求：字母开头，大小写敏感，不要跟关键字冲突

PEP 8要求：

- 用小写字母拼写，多个单词用下划线连接。
- 受保护的实例属性用单个下划线开头（后面会讲到）。
- 私有的实例属性用两个下划线开头（后面会讲到）。

## 3. Python保留字

保留字即关键字，我们不能把它们用作任何标识符名称。Python的标准库提供了一个keyword module，可以输出当前版本的所有关键字：

```python
>>> import keyword
>>> keyword.kwlist
['False', 'None', 'True', 'and', 'as', 'assert', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```

## 4. 注释

```
单行注释：用 # 号
多行注释：用三个单引号'''   '''   或者用  三个双引号"""  """
```

## 5. 查看版本和执行Python

```
python --version  # win10  or linux(python2)
python3 --version # linux
## 以下命令也一样
python3 -V
```

执行Python脚本

```
python3   hello.py     #  python3 也可替换成python
```

## 6. 数据类型

[Python3 的六个标准数据类型](https://www.runoob.com/python3/python3-data-type.html)中：

- **不可变数据（3 个）：**Number（数字）、String（字符串）、Tuple（元组）
- **可变数据（3 个）：**List（列表）、Dictionary（字典）、Set（集合）

Python中内置的 type() 函数可以用来查询变量所指的对象类型，还可以用 isinstance 来判断，二者区别在于：

- type()不会认为子类是一种父类类型
- isinstance()会认为子类是一种父类类型

string、list 和 tuple 都属于 sequence（序列）