

# Number

[Python3 的六个标准数据类型](https://www.runoob.com/python3/python3-data-type.html)中：

- **不可变数据（3 个）：**Number（数字）、String（字符串）、Tuple（元组）
- **可变数据（3 个）：**List（列表）、Dictionary（字典）、Set（集合）

## Number（数字）

Python3 支持 **int、float、bool、complex（复数）**，注意在Python 3里，只有一种整数类型 int，表示为长整型，没有 python2 中的 Long。*在 Python2 中是没有布尔型的，它用数字 0 表示 False，用 1 表示 True。到 Python3 中，把 True 和 False 定义成关键字了，但它们的值还是 1 和 0，它们可以和数字相加。*

```
int        # Python 3.x 仅int， Python2.x还区分int 和 long
float      #  如 1.23、3E-2
bool       # True  or Flase
complex    # 复数   如 1 + 2j、 1.1 + 2.2j
```

数值的除法包含两个运算符：**/** 返回一个浮点数，**//** 返回一个整数。

## 数值类型转换

利用type关键字进行类型检查

```
print(type(a))    # <class 'int'>
```

可以使用Python中内置的函数对变量类型进行转换。

- `int()`：将一个数值或字符串转换成整数，可以指定进制。
- `float()`：将一个字符串转换成浮点数。
- `str()`：将指定的对象转换成字符串形式，可以指定编码。
- `chr()`：将整数转换成该编码对应的字符串（一个字符）。
- `ord()`：将字符串（一个字符）转换成对应的编码（整数）。