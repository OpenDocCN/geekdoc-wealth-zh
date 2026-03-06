# 下载 Python 备忘单 PDF 快速参考[2023]

> 原文：<https://hackr.io/blog/python-cheat-sheet>

Python 是一种广泛用于数据研究和软件开发的高级编程语言。有几十个模块和库可供选择，Python 是一种有利可图且易于使用的语言。曾经做过 python 项目，渴望 Python 命令备忘单来帮助你吗？你来对地方了。

Guido Van Rossum 在 1991 年发布 Python 0.9.0 时开发了 Python。目前，Python 的最新版本是 Python 3.9。

如果你是初学者，Python 可能会让人感到害怕。但是只要有一点支持，我们将向您展示它实际上是一种有益且简单的语言。今天，我们将展示一个 Python 备忘单，它将帮助你轻松使用 Python。最终，您将成为使用这种编程语言的专家，包括 Python 语法。

如果您对 Python 有一个基本的了解，并且在开发 Python 应用程序时想要一个简单的参考，那么这个 Python 3 备忘单就是为您准备的。

请继续阅读，我们将带您了解各种 Python 命令或函数、操作符、数据类型、数据结构等等。

让我们从 Python 基础备忘单开始吧！

## **Python 之禅**

在我们进入 Python 语法备忘单之前，先看看 Tim Peters 对 Python 原理的诗意描述:

```
>>> import this
The Zen of Python, by Tim Peters
Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

## **Python 基础知识备忘单**

[点击此处](https://drive.google.com/file/d/1EeV3EHWMqUliLq8Ub0hjMBzNCnW-oZLb/view?usp=sharing)下载 Python 备忘单 PDF。

### **1。数学运算符**

在 Python 中，可以使用算术运算符执行加、减、乘、除等数学运算。您还可以访问几个库，这些库可以帮助您解决更高级的算术问题。下面是一些运算符及其功能的快速列表:

**

1.找到**个指数**

%

2.求**余数**。

//

3.执行**整数除法**。

/

4.执行**除法**运算。

*

5.执行**乘法**运算。

-

6.执行**减法**操作。

+

7.执行**加法**操作。

#### **例题**

```
>>> 3 * 8 + 6 + 0
30
>>> (2 + 3) * 6
30
>>> 5 ** 6
15625
```

推荐 Python 课程

### [用 Python 完成从零到英雄的 Python boot camp](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fcomplete-python-bootcamp%2F)

**2。数据类型**

数据类型是一种通知编译器哪些数据(整数、字符、浮点等)的机制。)应该被存储以及结果要分配多少内存。

以下是 Python 的数据类型:

数字(浮点、复数或浮点)

1.  序列(字符串、列表、元组等。)
2.  布尔型(真或假)
3.  一组
4.  词典
5.  **3。变量**

```
>>> a = 5.5 # float datatype
>>> a
5.5
>>> a = 5 # int datatype
>>> a
5
>>> a = [1, 2, 3, 4, 5, 6] # list datatype
>>> a
[1, 2, 3, 4, 5, 6]
>>> a = 'hello' # string datatype
>>> a
'hello'
>>> a = {1, 2, 3} # set datatype
>>> a
{1, 2, 3}
>>> a = True # boolean datatype
>>> a
True
>>> a = {1: 2} # dictionary datatype
>>> a
{1: 2}
```

### 变量是任何编程语言中保存数据的内存区域。这个区域通常存在于 RAM 内部的给定地址。变量可以包含任何值，包括数字、文本和真/假值。因此，如果您希望在程序中的任何地方使用该值，您可以简单地使用具有该值的变量。

值得注意的是，因为 Python 不是一种高度类型化的语言，所以您不必根据变量包含的值来指定变量的类型。在 Python 中，存储在变量中的数据类型将在运行时隐式解码，并由存储在该变量中的数据类型决定。

一个好的编程实践是给自己和他人留下注释，不管编程语言是什么。虽然 python 比 [Java](https://hackr.io/blog/how-to-learn-java) 、c++和其他语言更容易理解，但是留下注释来澄清文件的用途只是礼貌的做法。

```
>>> a = 'This is a string variable'
>>> a
'This is a string variable'
```

```
>>> a = 5
>>> a
5
```

**5。打印输出**

```
# This is an inline comment
```

```
"""
This is a
multiline comment
"""
```

### **print** ()方法向屏幕或另一个标准输出设备发送消息。该消息可以是一个字符串或另一个对象，在屏幕上显示之前将被转换为字符串。

**6。输入()**

```
>>> print('How are you?')
How are you?
>>> x = 10
>>> print('Hello world!', x)
Hello world! 10
```

### 当调用**输入**()函数时，程序执行暂停，直到用户提供输入。

**7。Len()函数**

```
The input() Function
>>> print('How are you?')
>>> myStatus = input()
>>> print('Nice to meet you, {}'.format(myStatus))
How are you?
Al
Nice to meet you, Al
```

### 函数的作用是:返回列表、字符串、集合等顺序或随机数据结构中的元素个数。

**8。类型转换功能**

```
>>> len('Computer')
8
```

### 以下是如何将整数转换为浮点或字符串:

下面是如何将浮点数转换成整数:

```
>>> str(14)
'14'
>>> print('He is {} years old'.format(str(14)))
He is 14 years old.
>>> str(-4.89)
'-4.89'
```

**流量控制**

```
>>> int(6.7)
6
>>> int(6.6) + 1
7
```

## **1。比较运算符**

### ==

等于

！=

不等于

<

不到

>

大于

<=

小于或等于

>=

大于或等于

**2。布尔评估**

```
>>> 71 == 70
False
>>> 40 == 34
False
>>> 'man' == 'man'
True
>>> 'man' == 'Man'
False
>>> 'bat' != 'butterfly'
True
>>> 50 == 50.0
True
>>> 1 == '1'
False
```

### **3。布尔运算符**

```
>>> True == True
True
>>> True != False
True
>>> True is True
True
>>> True is not False
True
>>> if a is True:
>>> pass
>>> if a is not False:
>>> pass
>>> if a:
>>> pass
>>> if a is False:
>>> pass
>>> if a is not True:
>>> pass
>>> if not a:
>>> pass
```

### 布尔运算符有三种:**与**、**或**、**非**。

下面是“**和**运算符的真值表:

千真万确

真假假

假与真假

假假假

下面是“**而非**”运算符的真值表

是非

不正确不正确

最后，这里是“**或**操作符的真值表

真实还是真实

真或假真

假的还是真的

假还是假假

**4。混合布尔和比较运算符**

### 除了比较运算符，您还可以在表达式中使用几个布尔运算符:

```
>>> (43< 57) and (3 < 9)
True
>>> (14 < 15) and (92< 61)
False
>>> (1 == 3) or (4 == 4)
True
```

**5。If-Else 语句**

```
>>> 2 + 2 == 4 and not 2 + 2 == 6 and 2 * 2 == 2 + 2
True
```

### **输出**

```
name = 'Peter'
if name == 'Peter':
 print('Hello, Peter')
```

你好，彼得

**输出**

```
name = 'Mike'
if name == 'Peter':
 print('Hello, Peter.')
else:
 print('Hello, anonymous')
```

你好，无名氏

**6。组合 If 和 Else (elif 语句)**

### **输出**

```
name = 'Mike'
age = 5
if name == 'Peter':
 print('Hi, Peter.')
elif age < 10:
 print('Your age is less than 10')
name = 'Mike'
age = 30
if name == 'Peter':
 print('Hello, Peter.')
elif age < 10:
 print('Your age is less than 12')
else:
 print('Your age is more than 10')
```

你的年龄不到 10 岁

你的年龄超过 10 岁了

7 .**。While 循环语句**

### While 循环语句用于将代码块运行指定的次数:

**输出**

```
var = 0
while var < 10:
 print('Hello, world.')
 var = var + 1
```

你好，世界。

你好，世界。

你好，世界。

你好，世界。

你好，世界。

你好，世界。

你好，世界。

你好，世界。

你好，世界。

你好，世界。

**8。中断语句**

### 如果执行到达一个 **break** 语句，迭代停止，控制退出循环。

**输出**

```
var = 1
while True:
 print('This block of code is running...')
 if var == 10:
 break
 var += 1
print('Loop exited')
```

这段代码正在运行...

这段代码正在运行...

这段代码正在运行...

这段代码正在运行...

这段代码正在运行...

这段代码正在运行...

这段代码正在运行...

这段代码正在运行...

这段代码正在运行...

这段代码正在运行...

循环已退出

**9。继续语句**

### 一旦程序遇到 **continue** 语句，控制从循环的开始重新开始。

**输出**

```
var = 0
while var <= 10:
 var += 1
 if var == 5:
 continue
 print('This block of code is running for number... ', var)
print('Loop exited')
```

这段代码是为数字而运行的...一

这段代码是为数字而运行的...2

这段代码是为数字而运行的...3

这段代码是为数字而运行的...四

这段代码是为数字而运行的...6

这段代码是为数字而运行的...七

这段代码是为数字而运行的...8

这段代码是为数字而运行的...9

这段代码是为数字而运行的...10

这段代码是为数字而运行的...11

循环已退出

10。For 循环

### 循环的**由序列控制，例如迭代器、列表或其他集合类型。对序列中的每个项目运行循环体，当序列结束时循环结束。**

**输出**

```
for var in range(1, 10):
 print("Loop running...")
print('Loop exited')
```

循环运行...

循环运行...

循环运行...

循环运行...

循环运行...

循环运行...

循环运行...

循环运行...

循环运行...

循环已退出

**11。范围功能**

### 程序员使用 Python 的**范围**()运行指定次数的迭代。它采用以下参数:

**Start** :整数序列应该以的数字。

**Stop** :返回整数序列之前的整数。stop–1 是整数范围的结尾。stop–1 是整数范围的结尾。

**步骤**:决定序列中每个整数之间增量的整数值。

**输出**

```
for var in range(1, 20, 2):
 print("Loop running with step size of 2...")
print('Loop exited')
```

步长为 2 的循环运行...

步长为 2 的循环运行...

步长为 2 的循环运行...

步长为 2 的循环运行...

步长为 2 的循环运行...

步长为 2 的循环运行...

步长为 2 的循环运行...

步长为 2 的循环运行...

步长为 2 的循环运行...

步长为 2 的循环运行...

循环已退出

For-If- Else 语句组合

For-if-else 语句允许您在循环中提供条件语句，包括 if、else 和 elif。

**输出**

```
for var in range(1, 11):
 if(var%2==0):
 print("This is even integer")
 else:
 print("This is odd integer")
print('Loop exited')
```

这是奇数

这是偶数

这是奇数

这是偶数

这是奇数

这是偶数

这是奇数

这是偶数

这是奇数

这是偶数

循环已退出

**Python 中的模块**

## 我们可以通过使用 python 的 **import** 语句从其他 python 模块导入文件/函数来导入其他 Python 模块代码。 **import** 语句是触发导入机制最常用的方法，但不是导入的唯一手段。

**输出**

```
import random
for i in range(5):
 print("Random integer is", random.randint(1, 30))
```

随机整数是 8

随机整数是 10

随机整数是 11

随机整数是 3

随机整数是 8

我们也可以使用来自语句的**来导入模块的指定方法**

**输出**

```
from collections import Counter
List = [1, 2, 3, 4, 5, 5, 1]
Cnt = Counter(List)
print(Cnt)
```

计数器({1: 2，5: 2，2: 1，3: 1，4: 1})

**功能**

## 函数是一个可重用的、有序的代码块，它执行一个单一的、相互关联的活动。函数为你的程序提供了更多的模块性，并允许你重用大量的代码。Python 还包括几个内置函数，比如 print()，但是您也可以构建自己的函数。

**输出**

```
def checkParity(num):
 if(num % 2 == 0):
 print("Number is even")
 else:
 print("Number is odd")
num = 5
checkParity(num)
```

号码是奇数

下面是一个返回某些内容的函数:

**输出**

```
def checkParity(num):
 if(num % 2 == 0):
 return "Number is even"
 else:
 return "Number is odd"
num = 4
parity = checkParity(num)
print(parity)
```

数字是偶数

**异常处理**

## 在[编程语言](https://hackr.io/blog/best-programming-languages-to-learn)中，异常是发生错误阻止代码继续运行的情况。例如，如果你用零除任何东西，就会出现运行时异常，程序就会崩溃。然而，你可以在程序中写如果出现这种情况该怎么做，这就是所谓的*异常处理*。在 Python 中，主要代码写在 **try** 块中。除了块之外，异常在**内处理。无论是否发生异常，始终执行 **finally** 块。**

**输出**

```
def divideBy(num):
 try:
 print(10 / num)
 except:
 print("Cannot divide by 0")
 finally:
 print("Division finished")
num = 0
divideBy(num)
```

不能被 0 除

除法完成

**Python 中的列表**

## 列表是 Python 中不同种类元素的序列。它类似于一个数组，除了它可以保存来自几个来源的数据。可变列表的值可以改变。我们可以使用索引来解析列表中的每个值或访问列表元素。

我们也可以对列表使用负索引:

```
>>> list = ['truck', 'car', 'submarine', 'jet']
>>> list
['truck', 'car', 'submarine', 'jet']
>>> list = ['truck', 'car', 'submarine', 'jet']
>>> list[0]
'truck'
>>> list[1]
'car'
>>> list[2]
'submarine'
>>> list[3]
'jet'
```

**修改列表中元素的值**

```
>>> list = ['truck', 'car', 'submarine', 'jet']
>>> list[-2]
'submarine'
>>> list[-3]
'car'
>>> 'The {} is larger than a {}.'.format(list[-2], list[-3])
'The submarine is larger than a car.'
```

### **列表串联和列表复制**

```
>>> list = ['truck', 'car', 'submarine', 'jet']
>>> list[1] = 'bike'
>>> list
['cat', 'bike', 'rat', 'elephant']
>>> list[2] = list[1]
>>> list
['cat', 'bike', 'bike', 'elephant']
>>> list[-1] = 54321
>>> list
['cat', 'bike', 'bike', 54321]
```

### **从列表中删除值**

```
>>> [4, 5, 6] + ['P', 'Q', 'R']
[4, 5, 6, 'P', 'Q', 'R']
>>> ['A', 'B', 'C'] * 4
['A', 'B', 'C', 'A', 'B', 'C', 'A', 'B', 'C', 'A', 'B', 'C']
>>> list = [1, 2, 3]
>>> list = list + ['X', 'Y', 'Z']
>>> list
[1, 2, 3, 'X', 'Y', 'Z']
```

### **使用带有遍历列表的 for 循环**

```
>>> list = ['truck', 'car', 'submarine', 'jet']
>>> del list[2]
>>> list
['truck', 'car', 'jet']
>>> del list[2]
>>> list
['truck', 'car']
```

### **用 Zip()** 遍历多个列表

```
>>> products = ['bag', 'rubber', 'knife', 'cooker']
>>> for i, product in enumerate(products):
>>> print('Index {} in products is: {}'.format(str(i), product))
Index 0 in products is: bag
Index 1 in products is: rubber
Index 2 in products is: knife
Index 3 in products is: cooker
```

### **In 和 Not in 运算符**

```
>>> name = ['David', 'Mike', 'Tommy']
>>> age = [10, 31, 54]
>>> for n, a in zip(name, age):
>>> print('{} is {} years old'.format(n, a))
David is 10 years old
Mike is 31 years old
Tommy is 54 years old
```

### **使用 Index()方法在列表中查找值**

```
>>> 'pen' in ['cap', 'owl', 'pen', 'rubber']
True
>>> list = ['cap', 'owl', 'pen', 'rubber']
>>> 'truck' in list
False
>>> 'pen' not in list
False
>>> 'train' not in list
True
```

### **用 Append()和 Insert()方法向列表添加值**

```
>>> list = ['notebook', 'pen', 'eraser', 'sharpener']
>>> list.index('pen')
1
```

### **append()**

#### **插入()**

```
>>> list = ['car', 'truck', 'bike']
>>> list.append('bicycle')
>>> list
['car', 'truck', 'bike', 'bicycle']
```

#### **使用 Remove()从列表中移除值**

```
>>> list = ['car', 'truck', 'bike']
>>> list.insert(1, 'bicycle')
>>> list
['car', 'bicycle', 'truck', 'bike']
```

### 如果一个值在列表中出现多次，则只会删除该值的第一个实例。

```
>>> list = ['car', 'bike', 'submarine', 'jet']
>>> list.remove('bike')
>>> list
['car', 'submarine', 'jet']
```

**用 Sort()方法对列表中的值进行排序**

### **字典和结构化数据**

```
>>> list = [2, 3, 1]
>>> list.sort()
>>> list
[1, 2, 3]
```

## Python 字典是没有任何特定顺序的元素的集合。字典有一个键:值对，而其他复合数据类型只是将值作为一个元素。

**key()、Values()和 Items()方法**

### 遍历键和值:

```
>>> book = {'color': 'red', 'price': 160}
>>> for v in book.values():
>>> print(v)
red
160
```

```
>>> for k in book.keys():
>>> print(k)
color
price
```

*   for 循环可以分别使用 **keys** ()、 **values** ()、和 **items** ()方法来遍历字典中的键、值或键值对。

```
>>> for i in book.items():
>>> print(i)
('color', 'red')
('price', 160)
```

**Get()方法**

### **Get** ()接受两个参数:一个键和一个默认值(如果没有找到键的话)。

**检查字典中是否存在关键字**

```
>>> items = {'chairs': 5, 'tables': 2}
>>> 'There are {} tables.'.format(str(items.get('tables', 0)))
'There are 2 tables.'
>>> 'There are {} computers.'.format(str(items.get('computers', 0)))
'There are 0 computers.'
```

### **设置**

```
>>> 'color' in book
True
```

## 集合是唯一元素的无序集合。Python 集合类似于数学集合，允许所有与集合相关的操作，包括并、交和差。

**创建集合**

### 您可以使用花括号{}和内置函数 **set** ():

如果您使用花括号{}来创建一个空集，您将得到一个作为**字典**的数据结构。

```
>>> s = {2, 4, 6}
>>> s = set([2, 4, 6])
```

所有重复的值都会被集合自动删除:

```
>>> s = {}
>>> type(s)
<class 'dict'>
```

**添加到集合中**

```
>>> s = {1, 2, 3, 2, 3, 4, 4, 5}
>>> s
{1, 2, 3, 4, 5}
```

### **从器械包中移除**

```
>>> a = {1, 2, 3, 4, 5}
>>> a.add(6)
>>> a
{1, 2, 3, 4, 5, 6}
>>> set = {0, 1, 2, 3, 4}
>>> set.update([2, 3, 4, 5, 6])
>>> set
{0, 1, 2, 3, 4, 5, 6} 
```

### **移除**()和**丢弃**()方法从集合中移除一个元素；然而，如果该值不存在， **remove** ()将抛出一个键错误。

也可以用**丢弃**():

```
>>> set = {1, 2, 3, 4}
>>> set.remove(4)
>>> set
{1, 2, 3}
>>> set.remove(3)
Traceback (most recent call last):
 File "<stdin>", line 1, in <module>
KeyError: 3
```

**多个集合的并集**

```
>>> s = {1, 2, 3, 4}
>>> s.discard(4)
>>> s
{1, 2, 3}
>>> s.discard(4)
```

### **多个集合的交集**

```
>>> s1 = {1, 2, 3, 4}
>>> s2 = {3, 4, 5, 6}
>>> s1.union(s2)
{1, 2, 3, 4, 5, 6}
```

### **两组差异**

```
>>> s1 = {1, 2, 3, 4}
>>> s2 = {2, 3, 4}
>>> s3 = {3, 4, 5}
>>> s1.intersection(s2, s3)
{3, 4}
```

### **两组对称差**

```
>>> s1 = {1, 2, 3}
>>> s2 = {2, 3, 4}
>>> s1.difference(s2)
{1}
>>> s2.difference(s1)
{4}
```

### 在处理迭代器时，itertools 模块提供了一组快速且节省内存的工具(比如列表或字典)。

```
>>> s1 = {1, 2, 3}
>>> s2 = {2, 3, 4}
>>> s1.symmetric_difference(s2)
{1, 4}
```

**Accumulate()**

### 使用 accumulate()将函数的结果作为迭代器返回:

**输出**

```
import itertools
import operator
data = [1, 2, 3, 4, 5]
result = itertools.accumulate(data, operator.mul)
for each in result:
 print(each)
```

一

```
1
2
6
24
120
```

2

6

24

120

**operator.mul()** 取两个数并相乘:

我们也可以使用方法*而不用*任何迭代器:

```
operator.mul(3, 5)
15
operator.mul(4, 3)
12
operator.mul(6, 3)
18
operator.mul(2, 5)
10
```

**输出**

```
import itertools
data = [1, 2, 3, 4, 5, 6, 7]
result = itertools.accumulate(data)
for each in result:
 print(each)
```

一

```
1
3
6
10
15
21
28
```

3

6

10

15

21

28

**组合()**

### **输出**

```
import itertools
shapes = [1, 2, 3, 4, 5]
combinations = itertools.combinations(shapes, 2)
for combination in combinations:
 print(combination)
```

(1, 2)

```
(1, 2)
(1, 3)
(1, 4)
(1, 5)
(2, 3)
(2, 4)
(2, 5)
(3, 4)
(3, 5)
(4, 5)
```

(1, 3)

(1, 4)

(1, 5)

(2, 3)

(2, 4)

(2, 5)

(3, 4)

(3, 5)

(4, 5)

**Combinations _ with _ Replacement()**

### **输出**

```
import itertools
shapes = [1, 2, 3, 4, 5]
combinations = itertools.combinations_with_replacement(shapes, 2)
for combination in combinations:
 print(combination)
```

(1, 1)

```
(1, 1)
(1, 2)
(1, 3)
(1, 4)
(1, 5)
(2, 2)
(2, 3)
(2, 4)
(2, 5)
(3, 3)
(3, 4)
(3, 5)
(4, 4)
(4, 5)
(5, 5)
```

(1, 2)

(1, 3)

(1, 4)

(1, 5)

(2, 2)

(2, 3)

(2, 4)

(2, 5)

(3, 3)

(3, 4)

(3, 5)

(4, 4)

(4, 5)

(5, 5)

**Count()**

### 计数采用初始点和步长:

**输出**

```
import itertools
for i in itertools.count(1, 3):
 print(i)
 if i >= 15:
 break
```

一

```
1
4
7
10
13
16
```

四

七

10

13

16

**周期()**

### 下面是 itertools.cycle(iterable):

**输出**

```
import itertools
arr = [1, 2, 3, 4, 5]
c = 0
for itr in itertools.cycle(arr):
 if(c > 20):
 break
 print(itr)
 c += 1
```

一

```
1
2
3
4
5
1
2
3
4
5
1
2
3
4
5
1
2
3
4
5
1
```

2

3

四

5

一

2

3

4

5

1

2

3

4

5

1

2

3

4

5

1

**理解**

## **字典理解**

### **列表理解**

```
>>> dict = {1: 2, 3: 4, 5: 6}
>>> {value: key for key, value in dict.items()}
{2: 1, 4: 3, 6: 5}
```

### **设定理解**

```
>>> a= [i for i in range(1, 20)]
>>> a
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
```

### **λ函数**

```
>>> a = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
>>> a = [i+1 for i in a]
>>> a
[2, 3, 4, 5, 6, 7, 8, 9, 10, 11]
```

## Lambda 函数是 Python 的一行函数:

**字符串格式化**

```
>>> add = lambda a, b: a + b
>>> add(1, 2)
3
```

## **使用%运算符**

### **。格式()**

```
>>> a = 4
>>> 'Value is %x' % a
'Value is 4'
```

### **格式化字符串文字(F 字符串)**

```
>>> a = 4
>>> 'Value is {}'.format(a)
'Value is 4'
```

### **三元条件运算符**

```
>>> a = 4
>>> f'Value is {a}'
'Value is 4'
```

## 我们可以使用三元条件运算符在单行中编写条件运算符 **if** 和 **else** :

**结论**

```
>>> a = 5
>>> print('Number is even' if a % 2 ==0 else 'Number is odd')
Number is odd
>>>
```

## 把这个 Python 备忘单看作是关于 Python 的快速问题的一站式商店。如您所见，Python 拥有创建端到端程序和应用程序所需的所有功能和数据结构。

为了便于参考，请下载下面的 Python 备忘单 PDF:

[备忘单](https://drive.google.com/file/d/1EeV3EHWMqUliLq8Ub0hjMBzNCnW-oZLb/view?usp=sharing)

准备好让您的 Python 实践更上一层楼了吗？查看我们为初学者准备的又酷又简单的 Python 项目列表。

编码快乐！

**常见问题解答**

## **1。有 Python 备忘单吗？**

#### 这个 Python 备忘单为您提供了用 Python 开发应用程序所需的一切。您也可以[下载我们的 Python 备忘单 PDF 以方便参考。](https://drive.google.com/file/d/1EeV3EHWMqUliLq8Ub0hjMBzNCnW-oZLb/view?usp=sharing)

**2。什么是 Python 命令？**

#### Python 命令是在使用时执行特定任务的函数。Python 命令的一些例子是 len、round、string、loop、type、find copy 等。

**人也在读:**

**People are also reading:**