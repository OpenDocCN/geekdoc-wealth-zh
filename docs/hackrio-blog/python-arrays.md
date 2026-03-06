# 什么是 Python 数组？[逐步指南]

> 原文：<https://hackr.io/blog/python-arrays>

在编程中，数组是元素的同质(属于同一数据类型)集合。与 C++、Java 和 JavaScript 等语言不同，数组不属于[内置的 Python 数据结构](https://hackr.io/blog/python-data-structures)。

尽管 Python 没有对数组的内置支持，但这并不妨碍程序员实现它们。

## **什么是 Python 数组**

作为数组的替代，Python 有列表。尽管如此，Python 支持使用[数组模块](https://docs.python.org/2/library/array.html)的数值数组。

当使用 Python 中的 array 模块创建数组时，请记住数组的所有元素必须是同一类型。如果不是这种情况，那么将产生一个错误。举个例子，

a = [1，22，240]是有效的

但是

a = [1，22，240，" Akhil"]无效，因此会产生错误

### **数组长度**

len()方法返回数组的长度，即数组中元素的数量。

示例
返回 phones 数组中元素的数量:

x = len(电话)

### 推荐 Python 课程

[用 Python 完成从零到英雄的 Python boot camp](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fcomplete-python-bootcamp%2F)

### **创建数组/如何在 Python 中声明数组**

在声明数组之前，需要导入数组模块。例如，看看下面的代码片段:

```
import array as ar1
a = ar1.array(‘d’, [1.2, 2.2, 2.4, 4.6])
print (a)

```

**输出:**

数组(' d '，[1.2，2.2，2.4，4.6])

在导入数组模块后，我们创建了一个 float 类型的数组。字母“d”是一个类型代码，用于在创建过程中确定数组的类型。以下是 Python 中一些最重要的数组类型代码:

*   b '–带符号字符
*   b '–无符号字符
*   d '–双精度
*   f’–浮动
*   h '–带符号的短
*   h’–无符号短整型
*   ' I '–带符号整数
*   I '–无符号整数
*   l '–长签名
*   l '–无符号长整型

### **在 Python 中访问数组元素**

在 Python 中，索引用于访问数组的元素。像列表一样，索引从 0 开始。例如:

```
import array as ar1
a = ar1.array (‘i’, [22, 24, 46, 53])
print(“The first element of the array:”, a[0])
print(“The second element of the array:”, a[1])
print(“The last element of the array:”, a[2])

```

**输出:**

数组的第一个元素:22

数组的第二个元素:24

数组的最后一个元素:53

### **在 Python 中切片数组**

通过使用*切片操作符* ( *:* ，可以在 Python 编程语言中访问数组中的一系列元素。以下代码片段演示了如何在 Python 中对数组使用切片运算符:

```
import array as ar1
number_list = [2, 4, 22, 25, 24, 52, 46, 5]
number_array = ar1.array('i', number_list)
print(numbers_array[2:5]) # third to fifth
print(numbers_array[:-5]) # beginning to forth
print(numbers_array[5:]) # sixth to end
print(numbers_array[:]) # beginning to end

```

**输出:**

数组(' I '，[22，25，24])

数组(' I '，[2，4，22，25])

数组(' I '，[46，5])

数组(' I '，[2，4，22，25，24，52，46，5])

### **添加或改变元素**

数组是可变的。因此，它们的元素可以像列表一样被改变。考虑以下代码示例:

```
import array as ar1
numbers = ar1.array('i', [1, 2, 3, 4, 6, 10])
numbers[0] = 0 # replacing the first element 1 with 0
print(numbers)
numbers[2:5] = arr.array('i', [4, 6, 8]) # changing third, fourth, and fifth elements
print(numbers)

```

**输出:**

数组(' I '，[0，2，3，4，6，10])

数组(' I '，[0，2，4，6，8，10])

*append()* 方法用于向数组中添加一个元素，而 *extend()* 方法允许添加多个元素。这些新元素被添加到数组的末尾。观察以下代码片段:

```
import array as ar1
numbers = ar1.array('i', [1, 2, 3])
numbers.append(4) # adds 4 to the array at the last position
print(numbers)
numbers.extend([5, 6, 7]) # appends iterable to the end of the array
print(numbers)

```

**输出:**

数组(' I '，[1，2，3，4])

数组(' I '，[1，2，3，4，5，6，7])

在 Python 编程语言中，*连接运算符* ( *+* )用于连接两个数组。例如:

```
import array as ar1
odd = ar1.array('i', [11, 33, 55])
even = ar1.array('i', [22, 44, 66])
numbers = ar1.array('i') # creates an empty array of integer
numbers = odd + even
print(numbers)

```

**输出:**

数组(' I '，[11，22，33，44，55，66])

### **从数组中删除元素**

在 Python 中，del 语句可用于从数组中移除一个或多个元素。例如:

```
import array as ar1
number = ar1.array('i', [11, 22, 33, 33, 44])
del number[2] # removes the third element
print(number)
del number # deletes the entire array
print(number)

```

**输出:**

数组(' I '，[11，22，33，44])

错误:未定义数组

虽然 *remove()* 方法可用于从数组中移除特定元素，但 *pop()* 方法允许移除特定元素并显示它。下面的代码片段演示了这两种方法的用法:

```
import array as ar1
numbers = ar1.array('i', [10, 11, 12, 12, 13])
numbers.remove(12)
print(numbers)
print(numbers.pop(2))
print(numbers)

```

**输出:**

数组(' I '，[10，11，12，13])

12

数组(' I '，[10，11，13])

### **查找数组**中的元素

根据元素的索引或值，可以在数组中搜索相同的内容。 *index()* 方法用于根据值搜索数组中的元素。方法返回正在搜索的元素的索引。例如:

```
import array as ar1
numbers = ar1.array('i', [10,20,30,40,50])
print (array1.index(40)) # returns the index of the element 40

```

**输出:**

3

如果在一个数组中没有这样的元素被搜索，程序会给出一个错误。

## **数组方法**

以下是 Python 中用于数组的各种内置方法:

*   *append()–在数组列表的末尾添加一个元素*
*   clear()–从数组列表中删除所有元素
*   copy()–返回数组列表的副本
*   count()–返回元素及其总数
*   extend()–将数组列表的元素添加到当前列表的末尾
*   index()–返回具有指定值的数组列表中第一个元素的索引
*   insert()–将元素添加到数组列表中的指定位置
*   pop()–从指定位置移除元素
*   remove()–删除具有指定值的第一个元素
*   reverse()–反转数组列表的顺序
*   sort()–对数组列表进行排序

## **结论**

虽然知道如何处理数组不是学习 Python 的必修部分，但是能够这样做无疑是一个额外的优势。在处理大量的数组和矩阵时尤其如此。尽管如此，Python 中的列表比数组灵活得多。

与数组不同，列表能够存储属于不同数据类型的元素，并且速度更快。通常，与 C 代码接口需要数组模块。通常建议避免在 Python 中使用数组。然而，这并不意味着你不能学习它们。

看看这些[最好的 Python 书籍](https://hackr.io/blog/best-python-books-for-beginners-and-advanced-programmers)来帮助你，让你的 Python 学习变得更好、更有见地。

**人也在读:**