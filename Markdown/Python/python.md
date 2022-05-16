python 2.* 不支持中文
需要加上
```python
#!/usr/bin/python3
# --conding=utf-8 --

```

```python

```

## **变量**
变量是存放数据值的容器。

**变量名称：**

- 变量可以使用短名称（如 x 和 y）或更具描述性的名称（age、carname、-total_volume）。

***Python 变量命名规则：***

- 变量名必须以字母或下划线字符开头
- 变量名称不能以数字开头
- 变量名只能包含字母数字字符和下划线（A-z、0-9 和 _）
- 变量名称区分大小写（age、Age 和 AGE 是三个不同的变量）
- 请记住，变量名称区分大小写

**向多个变量赋值**
Python 允许您在一行中为多个变量赋值：
```python
x, y, z = "Orange", "Banana", "Cherry"
```

**Python 的 print 语句通常用于输出变量。
如需结合文本和变量，Python 使用 + 字符：**

```python
x = "awesome"
print("Python is " + x)
```
**如果您尝试组合字符串和数字，Python 会给出错误：**

```python
x = 10
y = "Bill"
print(x + y)
```

**全局变量
在函数外部创建的变量（如上述所有实例所示）称为全局变量。全局变量可以被函数内部和外部的每个人使用。**

```python
在函数外部创建变量，并在函数内部使用它：
x = "awesome"

def myfunc():
  print("Python is " + x)

myfunc()
```

**全局变量
在函数外部创建的变量（如上述所有实例所示）称为全局变量。全局变量可以被函数内部和外部的每个人使用。**
```python
在函数外部创建变量，并在函数内部使用它：
x = "awesome"

def myfunc():
  print("Python is " + x)

myfunc()

```

## **Python 数据类型**
内置数据类型在编程中，数据类型是一个重要的概念。变量可以存储不同类型的数据，并且不同类型可以执行不同的操作。在这些类别中，Python 默认拥有以下内置数据类型：
文本类型|关键字
:-|:-:|
文本类型|str
数值类型|int, float, complex
序列类型|list, tuple, range
映射类型|dict
集合类型|set, frozenset
布尔类型|bool
二进制类型|bytes, bytearray, memoryview

**获取数据类型**
您可以使用 type() 函数获取任何对象的数据类型：

```python
x = 10
print(type(x))
```





## **Python 数字**
Python 中有三种数字类型：
```python
int
float
complex
为变量赋值时，将创建数值类型的变量：

x = 10   # int
y = 6.3  # float
z = 2j   # complex
```

```python
Int
Int 或整数是完整的数字，正数或负数，没有小数，长度不限。

整数：

x = 10
y = 37216654545182186317
z = -465167846

print(type(x))
print(type(y))
print(type(z))

Float
浮动或“浮点数”是包含小数的正数或负数。

浮点：

x = 3.50
y = 2.0
z = -63.78

print(type(x))
print(type(y))
print(type(z))

浮点数也可以是带有“e”的科学数字，表示 10 的幂。

浮点：

x = 27e4
y = 15E2
z = -49.8e100

print(type(x))
print(type(y))
print(type(z))



复数
复数用 "j" 作为虚部编写：

复数：

x = 2+3j
y = 7j
z = -7j

print(type(x))
print(type(y))
print(type(z))

```

**随机数**

Python 没有 random() 函数来创建随机数，但 Python 有一个名为 random 的内置模块，可用于生成随机数：
```python
导入 random 模块，并显示 1 到 9 之间的随机数：

import random

print(random.randrange(1,10))
```


## **Python 字符串**
python 中的字符串字面量由单引号或双引号括起。

'hello' 等同于 "hello"。

多行字符串
可以使用三个引号将多行字符串赋值给变量：结果中，换行符插入与代码中相同的位置。
```python
a = """Python is a widely used general-purpose, high level programming language. 
It was initially designed by Guido van Rossum in 1991 
and developed by Python Software Foundation. 
It was mainly developed for emphasis on code readability, 
and its syntax allows programmers to express concepts in fewer lines of code."""
print(a)
```

**字符串是数组**

像许多其他流行的编程语言一样，Python 中的字符串是表示 unicode 字符的字节数组。

但是，Python 没有字符数据类型，单个字符就是长度为 1 的字符串。

方括号可用于访问字符串的元素。

```python

a = "Hello, World!"
print(a[1])
```

**裁切**

您可以使用裁切语法返回一定范围的字符。

指定开始索引和结束索引，以冒号分隔，以返回字符串的一部分。

```python
获取从位置 2 到位置 5（不包括）的字符：

b = "Hello, World!"
print(b[2:5])

```

**负的索引**

使用负索引从字符串末尾开始切片：

```python
获取从位置 5 到位置 1 的字符，从字符串末尾开始计数：

b = "Hello, World!"
print(b[-5:-2])

```
**字符串长度**

如需获取字符串的长度，请使用 len() 函数。

```python
len() 函数返回字符串的长度：

a = "Hello, World!"
print(len(a))
```

**字符串格式**

但是我们可以使用 format() 方法组合字符串和数字！

format() 方法接受传递的参数，格式化它们，并将它们放在占位符 {} 所在的字符串中：
```python
quantity = 3
itemno = 567
price = 49.95
myorder = "I want to pay {2} dollars for {0} pieces of item {1}."
print(myorder.format(quantity, itemno, price))
```

## **Python 布尔**
布尔表示两值之一：True 或 False。

在编程中，通常需要知道表达式是 True 还是 False。

您可以计算 Python 中的任何表达式，并获得两个答案之一，即 True 或 False。

比较两个值时，将对表达式求值，Python 返回布尔值答案：

如果有某种内容，则几乎所有值都将评估为 True。

除空字符串外，任何字符串均为 True。

除 0 外，任何数字均为 True。

除空列表外，任何列表、元组、集合和字典均为 True。


## **Python 运算符**
Python 在以下组中划分运算符：

- 算术运算符
- 赋值运算符
- 比较运算符
- 逻辑运算符
- 身份运算符
- 成员运算符
- 位运算符

![](photos/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202022-05-16%20202413.png)
![](photos/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202022-05-16%20202455.png)
![](photos/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202022-05-16%20202509.png)
![](photos/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202022-05-16%20202548.png)
![](photos/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202022-05-16%20202603.png)
![](photos/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202022-05-16%20202636.png)
![](photos/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202022-05-16%20202658.png)




## **Python 列表**
Python 集合（数组）
Python 编程语言中有四种集合数据类型：

- 列表（List）是一种有序和可更改的集合。允许重复的成员。
- 元组（Tuple）是一种有序且不可更改的集合。允许重复的成员。
- 集合（Set）是一个无序和无索引的集合。没有重复的成员。
- 词典（Dictionary）是一个无序，可变和有索引的集合。没有重复的成员。
- 选择集合类型时，了解该类型的属性很有用。

为特定数据集选择正确的类型可能意味着保留含义，并且可能意味着提高效率或安全性。

**列表**

```python
#列表
thislist = ["apple", "banana", "cherry"]
print(thislist)
#可以通过引用索引号来访问列表项：
thislist = ["apple", "banana", "cherry"]
print(thislist[1]) # banana


#负索引表示从末尾开始，-1 表示最后一个项目，-2 表示倒数第二个项目，依此类推。
thislist = ["apple", "banana", "cherry"]
print(thislist[-1])

#遍历列表
#您可以使用 for 循环遍历列表项：
#逐个打印列表中的所有项目：

thislist = ["apple", "banana", "cherry"]
for x in thislist:
  print(x)

#添加项目
#如需将项目添加到列表的末尾，请使用 append() 方法：

thislist = ["apple", "banana", "cherry"]
thislist.append("orange")
print(thislist)

#要在指定的索引处添加项目，请使用 insert() 方法：

#实例
#插入项目作为第二个位置：

thislist = ["apple", "banana", "cherry"]
thislist.insert(1, "orange")
print(thislist)


#删除项目
#有几种方法可以从列表中删除项目：

thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")
print(thislist)


#pop() 方法删除指定的索引（如果未指定索引，则删除最后一项）：

thislist = ["apple", "banana", "cherry"]
thislist.pop()
print(thislist)


#del 关键字删除指定的索引：

thislist = ["apple", "banana", "cherry"]
del thislist[0]
print(thislist)

#del 关键字也能完整地删除列表：

thislist = ["apple", "banana", "cherry"]
del thislist

#clear() 方法清空列表：

thislist = ["apple", "banana", "cherry"]
thislist.clear()
print(thislist)



#检查项目是否存在
#如需确定列表中是否存在指定的项，请使用 in 关键字：
#检查列表中是否存在 “apple”：

thislist = ["apple", "banana", "cherry"]
if "apple" in thislist:
  print("Yes, 'apple' is in the fruits list")


#列表长度
#如需确定列表中有多少项，请使用 len() 方法：

thislist = ["apple", "banana", "cherry"]
print(len(thislist))


#复制列表
#只能通过键入 list2 = list1 来复制列表，因为：list2 将只是对 list1 的引用，list1 中所做的更改也将自动在 list2 中进行。

#有一些方法可以进行复制，一种方法是使用内置的 List 方法 copy()。
#使用 copy() 方法来复制列表：

thislist = ["apple", "banana", "cherry"]
mylist = thislist.copy()
print(mylist)


#制作副本的另一种方法是使用内建的方法 list()。
#使用 list() 方法复制列表：

thislist = ["apple", "banana", "cherry"]
mylist = list(thislist)
print(mylist)


#合并两个列表
#在 Python 中，有几种方法可以连接或串联两个或多个列表。
#最简单的方法之一是使用 + 运算符。
#合并两个列表：

list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]

list3 = list1 + list2
print(list3)



```

## **Python 元组**
元组（Tuple）
元组是有序且不可更改的集合。在 Python 中，元组是用圆括号编写的。
```python
#创建元组：
#访问元组项目
#可以通过引用方括号内的索引号来访问元组项目：

#打印元组中的第二个项目：

thistuple = ("apple", "banana", "cherry")
print(thistuple[1])

#负索引
#负索引表示从末尾开始，-1 表示最后一个项目，-2 表示倒数第二个项目，依此类推。

#打印元组的最后一个项目：

thistuple = ("apple", "banana", "cherry")
print(thistuple[-1])

#索引范围
#您可以通过指定范围的起点和终点来指定索引范围。

#指定范围后，返回值将是带有指定项目的新元组。

#返回第三、第四、第五个项目：

thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[2:5])

#注释：搜索将从索引 2（包括）开始，到索引 5（不包括）结束。


#更改元组值
#创建元组后，您将无法更改其值。元组是不可变的，或者也称为恒定的。

#但是有一种解决方法。您可以将元组转换为列表，更改列表，然后将列表转换回元组。

#把元组转换为列表即可进行更改：

x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"
x = tuple(y)

print(x)

#遍历元组
#可以使用 for 循环遍历元组项目。

#遍历项目并打印值：

thistuple = ("apple", "banana", "cherry")
for x in thistuple:
  print(x)

#将在 Python For 循环 这一章中学习有关 for 循环的更多知识。

#检查项目是否存在
#要确定元组中是否存在指定的项，请使用 in 关键字：

#检查元组中是否存在 "apple"：

thistuple = ("apple", "banana", "cherry")
if "apple" in thistuple:
  print("Yes, 'apple' is in the fruits tuple")

#元组长度
#要确定元组有多少项，请使用 len() 方法：

thistuple = ("apple", "banana", "cherry")
print(len(thistuple))


#添加项目
元组一旦创建，您就无法向其添加项目。元组是不可改变的。


#无法向元组添加项目：

thistuple = ("apple", "banana", "cherry")
thistuple[3] = "orange" # 会引发错误
print(thistuple)

#创建有一个项目的元组
#如需创建仅包含一个项目的元组，您必须在该项目后添加一个逗号，否则 Python 无法将变量识别为元组。

#单项元组，别忘了逗号：

thistuple = ("apple",)
print(type(thistuple))

#不是元组
thistuple = ("apple")
print(type(thistuple))

#删除项目
#注释：您无法删除元组中的项目。

#元组是不可更改的，因此您无法从中删除项目，但您可以完全删除元组：

del 关键字可以完全删除元组：

thistuple = ("apple", "banana", "cherry")
del thistuple

print(thistuple) # 这会引发错误，因为元组已不存在。

#合并两个元组
#如需连接两个或多个元组，您可以使用 + 运算符：

#合并这个元组：

tuple1 = ("a", "b" , "c")
tuple2 = (1, 2, 3)

tuple3 = tuple1 + tuple2
print(tuple3)

#tuple() 构造函数
#也可以使用 tuple() 构造函数来创建元组。

#使用 tuple() 方法来创建元组：

thistuple = tuple(("apple", "banana", "cherry")) # 请注意双括号
print(thistuple)
```

## **Python 集合**
集合（Set）
集合是无序和无索引的集合。在 Python 中，集合用花括号编写。
```python
#Python 集合
#创建集合：
thisset = {"apple", "banana", "cherry"}
print(thisset)

#注释：集合是无序的，因此您无法确定项目的显示顺序。

#访问项目
#您无法通过引用索引来访问 set 中的项目，因为 set 是无序的，项目没有索引。

#但是您可以使用 for 循环遍历 set 项目，或者使用 in 关键字查询集合中是否存在指定值。

thisset = {"apple", "banana", "cherry"}

for x in thisset:
  print(x)

#检查 set 中是否存在 “banana”：


thisset = {"apple", "banana", "cherry"}

print("banana" in thisset)


#更改项目
#集合一旦创建，您就无法更改项目，但是您可以添加新项目。

#添加项目
#要将一个项添加到集合，请使用 add() 方法。

#要向集合中添加多个项目，请使用 update() 方法。

#使用 add() 方法向 set 添加项目：

thisset = {"apple", "banana", "cherry"}

thisset.add("orange")

print(thisset)


# 使用 update() 方法将多个项添加到集合中：

thisset = {"apple", "banana", "cherry"}

thisset.update(["orange", "mango", "grapes"])

print(thisset)

#获取 Set 的长度
#要确定集合中有多少项，请使用 len() 方法。
thisset = {"apple", "banana", "cherry"}
print(len(thisset))


#删除项目
#要删除集合中的项目，请使用 remove() 或 discard() 方法。

#使用 remove() 方法来删除 “banana”：

thisset = {"apple", "banana", "cherry"}

thisset.remove("banana")

print(thisset)

#注释：如果要删除的项目不存在，则 remove() 将引发错误。


thisset = {"apple", "banana", "cherry"}

thisset.discard("banana")

print(thisset)

#注释：如果要删除的项目不存在，则 discard() 不会引发错误。

#您还可以使用 pop() 方法删除项目，但此方法将删除最后一项。请记住，set 是无序的，因此您不会知道被删除的是什么项目。

#pop() 方法的返回值是被删除的项目。

#使用 pop() 方法删除最后一项：

thisset = {"apple", "banana", "cherry"}

x = thisset.pop()

print(x)

print(thisset)
#注释：集合是无序的，因此在使用 pop() 方法时，您不会知道删除的是哪个项目。


#clear() 方法清空集合：

thisset = {"apple", "banana", "cherry"}

thisset.clear()

print(thisset)

#del 彻底删除集合：

thisset = {"apple", "banana", "cherry"}

del thisset

print(thisset)

#合并两个集合
#在 Python 中，有几种方法可以连接两个或多个集合。

#您可以使用 union() 方法返回包含两个集合中所有项目的新集合，也可以使用 update() 方法将一个集合中的所有项目插入另一个集合中：


#union() 方法返回一个新集合，其中包含两个集合中的所有项目：

set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}

set3 = set1.union(set2)
print(set3)

#update() 方法将 set2 中的项目插入 set1 中：

set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}

set1.update(set2)
print(set1)

#注释：union() 和 update() 都将排除任何重复项。

#还有其他方法将两个集合连接起来，并且仅保留重复项，或者永远不保留重复项，请查看此页面底部的集合方法完整列表。

#set() 构造函数
#也可以使用 set() 构造函数来创建集合。


#使用 set() 构造函数来创建集合：

thisset = set(("apple", "banana", "cherry")) # 请留意这个双括号
print(thisset)

```



## **Python 字典**

字典（Dictionary）
字典是一个无序、可变和有索引的集合。在 Python 中，字典用花括号编写，拥有键和值。

```python

#创建并打印字典：

thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
print(thisdict)

#访问项目
#可以通过在方括号内引用其键名来访问字典的项目：

#获取 "model" 键的值：

x = thisdict["model"]

#还有一个名为 get() 的方法会给你相同的结果：

#获取 "model" 键的值：

x = thisdict.get("model")

#更改值
#您可以通过引用其键名来更改特定项的值：


#把 "year" 改为 2019：

thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
thisdict["year"] = 2019

#遍历字典
#您可以使用 for 循环遍历字典。

#循环遍历字典时，返回值是字典的键，但也有返回值的方法。
#逐个打印字典中的所有键名：

for x in thisdict:
  print(x)


#逐个打印字典中的所有值：

for x in thisdict:
  print(thisdict[x])

#您还可以使用 values() 函数返回字典的值：

for x in thisdict.values():
  print(x)

#通过使用 items() 函数遍历键和值：

for x, y in thisdict.items():
  print(x, y)

#检查键是否存在
#要确定字典中是否存在指定的键，请使用 in 关键字：


#检查字典中是否存在 "model"：

thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
if "model" in thisdict:
  print("Yes, 'model' is one of the keys in the thisdict dictionary")

#字典长度
#要确定字典有多少项目（键值对），请使用 len() 方法。

print(len(thisdict))

#添加项目
通过使用新的索引键并为其赋值，可以将项目添加到字典中：

thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
thisdict["color"] = "red"
print(thisdict)

#删除项目
#有几种方法可以从字典中删除项目：
pop() 方法删除具有指定键名的项：

thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
thisdict.pop("model")
print(thisdict)
#popitem() 方法删除最后插入的项目（在 3.7 之前的版本中，删除随机项目）：

thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
thisdict.popitem()
print(thisdict)

#del 关键字删除具有指定键名的项目：

thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
del thisdict["model"]
print(thisdict)
#del 关键字也可以完全删除字典：

thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
del thisdict

print(thisdict) #this 会导致错误，因为 "thisdict" 不再存在。
#clear() 关键字清空字典：

thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
thisdict.clear()
print(thisdict)

#复制字典
#您不能通过键入 dict2 = dict1 来复制字典，因为：dict2 只是对 dict1 的引用，而 dict1 中的更改也将自动在 dict2 中进行。

有一些方法可以进行复制，一种方法是使用内建的字典方法 copy()。


#使用 copy() 方法来复制字典：

thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
mydict = thisdict.copy()
print(mydict)

#制作副本的另一种方法是使用内建方法 dict()。
#使用 dict() 方法创建字典的副本：
thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
mydict = dict(thisdict)
print(mydict)

#嵌套字典
#词典也可以包含许多词典，这被称为嵌套词典。


myfamily = {
  "child1" : {
    "name" : "Phoebe Adele",
    "year" : 2002
  },
  "child2" : {
    "name" : "Jennifer Katharine",
    "year" : 1996
  },
  "child3" : {
    "name" : "Rory John",
    "year" : 1999
  }
}
#或者，如果您想嵌套三个已经作为字典存在的字典：


child1 = {
  "name" : "Phoebe Adele",
  "year" : 2002
}
child2 = {
  "name" : "Jennifer Katharine",
  "year" : 1996
}
child3 = {
  "name" : "Rory John",
  "year" : 1999
}

myfamily = {
  "child1" : child1,
  "child2" : child2,
  "child3" : child3
}


##也可以使用 dict() 构造函数创建新的字典：
thisdict = dict(brand="Porsche", model="911", year=1963)
# 请注意，关键字不是字符串字面量
# 请注意，使用了等号而不是冒号来赋值
print(thisdict)

```














## ****

## ****



# **Python 文件处理**
文件处理是任何 Web 应用程序的重要组成部分。

Python 有几个用于创建、读取、更新和删除文件的函数。
## **文件处理**

在 Python 中使用文件的关键函数是 open() 函数。

open() 函数有两个参数：文件名和模式。

有四种打开文件的不同方法（模式）：

- "r" - 读取 - 默认值。打开文件进行读取，如果文件不存在则报错。
- "a" - 追加 - 打开供追加的文件，如果不存在则创建该文件。
- "w" - 写入 - 打开文件进行写入，如果文件不存在则创建该文件。
- "x" - 创建 - 创建指定的文件，如果文件存在则返回错误。
此外，您可以指定文件是应该作为二进制还是文本模式进行处理。

- "t" - 文本 - 默认值。文本模式。
- "b" - 二进制 - 二进制模式（例如图像）。

## **文件打开**
```python
#语法
#此外，您可以指定文件是应该作为二进制还是文本模式进行处理：

f = open("demofile.txt")
#以上代码等同于：

f = open("demofile.txt", "rt")
#因为 "r" (读取)和 "t" (文本)是默认值，所以不需要指定它们。

#注释：请确保文件存在，否则您将收到错误消息。
```

## **文件读取**
在服务器上打开文件
假设我们有以下文件，位于与 Python 相同的文件夹中：
demofile.txt

Hello! Welcome to demofile.txt
This file is for testing purposes.
Good Luck!
```python

#如需打开文件，请使用内建的 open() 函数。

#open() 函数返回文件对象，此对象有一个 read() 方法用于读取文件的内容：


f = open("demofile.txt", "r")
print(f.read())

#只读取文件的一部分
#默认情况下，read() 方法返回整个文本，但您也可以指定要返回的字符数：


#返回文件中的前五个字符：

f = open("demofile.txt", "r")
print(f.read(5))

#读行
#您可以使用 readline() 方法返回一行：

#读取文件中的一行：

f = open("demofile.txt", "r")
print(f.readline())

#通过两次调用 readline()，您可以读取前两行：


#读取文件中的两行：

f = open("demofile.txt", "r")
print(f.readline())
print(f.readline())

#通过循环遍历文件中的行，您可以逐行读取整个文件：


#逐行遍历文件：

f = open("demofile.txt", "r")
for x in f:
  print(x)

#关闭文件
#完成后始终关闭文件是一个好习惯。

#完成后关闭文件：

f = open("demofile.txt", "r")
print(f.readline())
f.close()

#注释：在某些情况下，由于缓冲，您应该始终关闭文件，在关闭文件之前，对文件所做的更改可能不会显示。
```

## **Python 文件写入**
写入已有文件
如需写入已有的文件，必须向 open() 函数添加参数：

- "a" - 追加 - 会追加到文件的末尾
- "w" - 写入 - 会覆盖任何已有的内容

```python

#打开文件 "demofile2.txt" 并将内容追加到文件中：

f = open("demofile2.txt", "a")
f.write("Now the file has more content!")
f.close()

# 追加后，打开并读取该文件：
f = open("demofile2.txt", "r")
print(f.read())



# 打开文件 "demofile3.txt" 并覆盖内容：

f = open("demofile3.txt", "w")
f.write("Woops! I have deleted the content!")
f.close()

# 写入后，打开并读取该文件：
f = open("demofile3.txt", "r")
print(f.read())

#注释："w" 方法会覆盖全部内容。


#创建新文件
#如需在 Python 中创建新文件，请使用 open() 方法，并使用以下参数之一：

#"x" - 创建 - 将创建一个文件，如果文件存在则返回错误
#"a" - 追加 - 如果指定的文件不存在，将创建一个文件
#"w" - 写入 - 如果指定的文件不存在，将创建一个文件

#创建名为 "myfile.txt" 的文件：

f = open("myfile.txt", "x")
#结果：已创建新的空文件！

#如果不存在，则创建新文件：

f = open("myfile.txt", "w")

```

## **Python 删除文件**
```python

#删除文件
#如需删除文件，必须导入 OS 模块，并运行其 os.remove() 函数：


#删除文件 "demofile.txt"：

import os
if os.path.exists("文件"):
    os.remove("文件/a.txt")
else:
    print("文件不存在")



import os
os.remove("demofile.txt")
#检查文件是否存在
#为避免出现错误，您可能需要在尝试删除文件之前检查该文件是否存在：


#检查文件是否存在，然后删除它：

import os
if os.path.exists("demofile.txt"):
  os.remove("demofile.txt")
else:
  print("The file does not exist")
#删除文件
#如需删除整个文件夹，请使用 os.rmdir() 方法：

#实例
#删除文件夹 "myfolder"：

import os
os.rmdir("myfolder")
#提示：您只能删除空文件夹。

# 删除文件夹不管有没有文件
import shutil
shutil.rmtree("文件")



```