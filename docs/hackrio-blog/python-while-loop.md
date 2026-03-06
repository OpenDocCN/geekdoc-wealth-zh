# Python While 循环语句(无限迭代)

> 原文：<https://hackr.io/blog/python-while-loop>

循环是学习 Python 或任何编程语言不可或缺的一部分。当需要多次重复特定的代码块或语句集时，可以使用它们。

Python 编程语言支持三种类型的循环来满足不同的要求，即 for 循环、嵌套循环和 while 循环。通常，while 循环用于事先不知道所需迭代总数的情况。

## **什么是 Python While 循环？**

while loop 子句重复执行一组语句，直到给定的条件为假。Python while 循环语句的一般语法是:

```
while test_expression/condition:
statement body
```

语句体可以是单个语句，也可以是一组语句或语句块，而条件可以是也可以不是表达式。

在 Python while 循环中，测试表达式在开始时计算。当且仅当 test_expression 或条件的计算结果为真时，程序执行才会进入 while 循环体。while 循环体在每次迭代时都被求值。

继续计算 while 循环体，直到 test_expression/condition 的计算结果为 false。现在，程序控制被传递到 while 循环的下一行。在 Python 中，缩进用于确定 while 循环的主体。

Python 编程语言使用缩进作为语句分组的方法。因此，在一个编程构造之后缩进相同数量字符空间的所有语句都被视为一个代码块。

在 Python 编程语言中，while 循环体以缩进开始，第一个未缩进的行标志着 while 循环的结束。虽然任何非零值都被视为 true，但 Python 将 None 和 0 解释为 false。

需要注意的重要一点是，while 循环可能一次都不会运行。如果在循环的第一次迭代中条件评估为假，就会发生这种情况。

**一个简单的 Python While 循环示例**

```
loop_value = 0
while (loop_value < 9):
print ('The loop value is:', loop_value)
loop_value = loop_value + 1
print ('Demonstration of a simple Python while loop program is complete!')

```

输出:

```
The loop value is: 0
The loop value is: 1
The loop value is: 2
The loop value is: 3
The loop value is: 4
The loop value is: 5
The loop value is: 6
The loop value is: 7
The loop value is: 8

```

演示一个简单的 Python while 循环程序完成！

在上面的代码示例中，while 循环体的条件是 loop_value 变量必须小于 9。while 循环体包含一个 print 语句，该语句打印 loop_value 变量的当前值，然后使用下一个语句将该值递增 1。

while 循环将继续执行，直到 loop_value 达到 9，此时将执行最后一条 print 语句。

### 推荐 Python 课程

[用 Python 完成从零到英雄的 Python boot camp](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fcomplete-python-bootcamp%2F)

### **无限循环**

如果所陈述的条件永远不会变为假，那么任何循环都是无限的。这样的循环因此被称为无限循环。因此，建议在使用循环时特别注意防止无限循环的发生。

无限循环的一个应用领域是客户机/服务器编程。在这种情况下，服务器需要连续运行，以便在需要时允许大量的客户端程序与之通信。下面是无限循环的基本代码示例:

```
var = 1
while var == 1 :
num = input("Enter some number: ")
print ("You entered: ", num)
print ("Goodbye!") # the program execution never reaches this point

```

输出:

```
Enter some number: 22
You entered: 22
Enter some number: 24
You entered: 24
Enter some number: 46
You entered: 46

Enter a number:Traceback (most recent call last):
File “main.py”, line 3, in 
num = input(“Enter some number: ”)
KeyboardInterrupt
```

上述代码示例演示了一个永远不会自动退出的无限循环。你需要按 Ctrl + C 来手动退出程序。当您手动退出程序时，将显示输出的最后 4 行。

### **使用带有 While 循环的 Else 语句**

Python 支持在 else 语句中使用 loop 语句。当 else 语句与 while 循环一起使用时，当 while 循环条件变为 false 时，将执行 else 语句。

下面的代码演示了一个使用 while 循环和 else 语句的简单示例:

```
value = 0
while (value < 8):
print (value, " is smaller than 8")
value = value + 1
else: # executes once the condition in the while loop turns false
print (value, " is not smaller than 8")

```

输出:

```
0 is smaller than 8
1 is smaller than 8
2 is smaller than 8
3 is smaller than 8
4 is smaller than 8
5 is smaller than 8
6 is smaller than 8
7 is smaller than 8
8 is not smaller than 8

```

上面提到的代码示例演示了将 else 语句与 while 循环相结合，while 循环一直打印一个数字，直到它等于 8。

### **一行 While 子句**

是的，在 Python 中用一条语句编写一个 while 循环是可能的。这种 while 循环也称为单行 while 子句。除了将唯一语句添加到 while 循环体中，还可以将该语句放在“while”头的附近。

*通用语法*:

while test _ 表达式/条件:语句

以下是演示如何在 Python 编程语言中使用单行 while 子句的代码示例:

```
a = 0
while (a==0): print ("It is 0!")

```

**输出:**

```
It is 0!
It is 0!
It is 0!
It is 0!
It is 0!
It is 0!
It is 0!
It is 0!
It is 0!
It is 0!
It is 0!
Traceback (most recent call last):
File “main.py”, line 2, in 
While (a==0): print (It is 0!”)
KeyboardInterrupt

```

前面提到的例子将产生一个无限循环。因此，您需要按 Ctrl + C 来手动退出程序！

## **结论**

这就完成了您必须了解的关于 Python while 循环的所有内容。这是一种执行需要多次执行的语句的有效方式。您可以随时尝试 while loop 子句，以便更好地理解其工作原理。

如果你有任何关于 Python while 循环的重要信息想与我们分享，那么你可以通过下面的评论部分来分享！此外，您可以在那里询问与 Python while 循环相关的查询。我们会尽快回复你！

最近刚开始用 Python？然后看看这个[对 Python 的温和介绍](https://hackr.io/blog/python-programming-language)来更好地了解这种高级的、解释的、通用的编程语言！

**人也在读:**