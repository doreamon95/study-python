# String（字符串）

[Python3 的六个标准数据类型](https://www.runoob.com/python3/python3-data-type.html)中：

- **不可变数据（3 个）：**Number（数字）、String（字符串）、Tuple（元组）
- **可变数据（3 个）：**List（列表）、Dictionary（字典）、Set（集合）

而字符串类型是一种结构化的、非标量类型，所以才会有一系列的属性和方法。

Python中的字符串用单引号 **'** 或双引号 **"** 括起来

```python
s1 = 'hello, world!'
s2 = "hello, world!"
# 以三个双引号或单引号开头的字符串可以折行
s3 = """
hello, 
world!
"""
```

Python同时使用反斜杠 \ 转义特殊字符。**如果你不想让反斜杠发生转义，可以在字符串前面添加一个 r**，表示原始字符串：

```
>>> print('He\nllo')
He
llo
>>> print(r'He\nllo')
He\nllo
>>>
```

## 运算符

Python为字符串类型提供了非常丰富的运算符，加号 **+** 是字符串的连接符， 星号 ***** 表示复制当前字符串，与之结合的数字为复制的次数。比如：

- 使用`+`运算符来实现字符串的拼接

  ```
  s1 = 'hello ' * 3
  ```

- 使用`*`运算符来重复一个字符串的内容

  ```
  s1 += s2
  ```

- 使用`in`和`not in`来判断一个字符串是否包含另外一个字符串（成员运算）

  ```
  print('ll' in s1) # True
  ```

- 使用`[]`和`[:]`运算符从字符串取出某个字符或某些字符（切片运算），字符串的截取的语法格式：`变量[头下标:尾下标]`

  ```
  print(str2[2:5]) # c12
  ```

### 典型Python字符串运算符

```python
# 通过内置函数len计算字符串的长度
print(len(str1))
# 获得字符串首字母大写的拷贝
print(str1.capitalize()) # Hello, world!
# 获得字符串每个单词首字母大写的拷贝
print(str1.title()) # Hello, World!
# 获得字符串变大写后的拷贝
print(str1.upper()) # HELLO, WORLD!
# 从字符串中查找子串所在位置
print(str1.find('or')) # 8
print(str1.find('shit')) # -1
# 与find类似但找不到子串时会引发异常
# print(str1.index('or'))
# print(str1.index('shit'))
# 检查字符串是否以指定的字符串开头
print(str1.startswith('He')) # False
print(str1.startswith('hel')) # True
# 检查字符串是否以指定的字符串结尾
print(str1.endswith('!')) # True
# 将字符串以指定的宽度居中并在两侧填充指定的字符
print(str1.center(50, '*'))
# 将字符串以指定的宽度靠右放置左侧填充指定的字符
print(str1.rjust(50, ' '))
str2 = 'abc123456'
# 检查字符串是否由数字构成
print(str2.isdigit())  # False
# 检查字符串是否以字母构成
print(str2.isalpha())  # False
# 检查字符串是否以数字和字母构成
print(str2.isalnum())  # True
str3 = 'doreamon95@163.com '
print(str3)
# 获得字符串修剪左右两侧空格之后的拷贝
print(str3.strip())
```

## 格式化输出

常规方式：

```python
a, b = 5, 10
print('%d * %d = %d' % (a, b, a * b))
```

字符串提供的方法来完成字符串的格式：

```python
a, b = 5, 10
print('{0} * {1} = {2}'.format(a, b, a * b))
```

Python 3.6以后，格式化字符串还有更为简洁的书写方式，就是在字符串前加上字母`f`，我们可以使用下面的语法糖来简化上面的代码。

```Python
a, b = 5, 10
print(f'{a} * {b} = {a * b}')
```





