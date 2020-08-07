# 字典 { }

[Python3 的六个标准数据类型](https://www.runoob.com/python3/python3-data-type.html)中：

- **不可变数据（3 个）：**Number（数字）、String（字符串）、Tuple（元组）
- **可变数据（3 个）：**List（列表）、Dictionary（字典）、Set（集合）

字典（dictionary）是Python中另一个非常有用的内置数据类型。列表是有序的对象集合，字典是无序的对象集合。两者之间的区别在于：字典当中的元素是通过键来存取的，而不是通过偏移存取。字典是一种映射类型，字典用 **{ }** 标识，它是一个无序的 **键(key) : 值(value)** 的集合。键(key)必须使用不可变类型。在同一个字典中，键(key)必须是唯一的。

下面的代码演示了如何定义和使用字典。

```Python
# 创建字典的字面量语法
scores = {'王一': 95, '王二': 78, '王三': 82}
print(scores)
# 创建字典的构造器语法
items1 = dict(one=1, two=2, three=3, four=4)
# 通过zip函数将两个序列压成字典
items2 = dict(zip(['a', 'b', 'c'], '123'))
# 创建字典的推导式语法
items3 = {num: num ** 2 for num in range(1, 10)}
print(items1, items2, items3)
# 通过键可以获取字典中对应的值
print(scores['王一'])
print(scores['王二'])
# 对字典中所有键值对进行遍历
for key in scores:
    print(f'{key}: {scores[key]}')
# 更新字典中的元素
scores['王二'] = 65
scores['王一'] = 71
scores.update(冷面=67, 方启鹤=85)
print(scores)
if '王一' in scores:
    print(scores['王一'])
print(scores.get('王一'))
# get方法也是通过键获取对应的值但是可以设置默认值
print(scores.get('王一', 60))
# 删除字典中的元素
print(scores.popitem())
print(scores.popitem())
print(scores.pop('王一', 100))
# 清空字典
scores.clear()
print(scores)
```

