# Python 条件语句:If，Else & Switch

> 原文：<https://hackr.io/blog/python-conditional-statements-switch-if-else>

如果你刚刚开始[学习 Python](https://hackr.io/tutorials/learn-python?ref=blog-post) ，你很快就会明白，Python 中的条件语句真的很有用，可以根据条件或案例，以及它们是真还是假来执行各种动作。

## Python 条件语句

Python 中不同类型的语句及其解释如下:

### **If 语句**

“如果”语句用于决策。一旦定义了约束，它将仅在“If”语句为真时运行代码体。

**基本语法:**

```
if expression
statement

```

**举例:**

```
a, b = 11,32
if (a<b);
qw = “a is less than b”
print (qw)

```

### **If-Else 语句**

当不满足 If 条件时，就会出现此语句。If-Else 语句提供 and If 语句和一个 Else 语句。

**基本语法:**

```
If expression
statement

else
statement

```

**举例:**

```
a, b = 11,32
if (a<b);
qw=”a is less than b”
else
wq=”b is less than a”
print (qw)

```

### **Else-If (elif)语句**

当 Else 条件可能不满足时，使用 Else-If 语句。这主要用在你必须证明两个以上结果的情况下。

**基本语法:**

```
If expression
statement

elif expression
statement

else
statement

```

**举例:**

```
def main():
q,r =3,3
if(q< r):
yz= "q is less than r"
elif (q == r):
yz= "q is same as r"
else:
yz="q is greater than r"
print(yz)

```

### **嵌套的 Else-If 语句**

当需要定义多个结果时，使用嵌套的 Else-If 语句。

**基本语法:**

```
If expression
statement
elif expression
statement
elif expression
statement
elif expression
statement
.
.
.
else
statement

```

**举例:**

```
Cost = 125
#country = "IN"
if Cost <= 50:
print("Shipping Cost is 25")
elif total <= 100:
print("Shipping Cost is 10")
elif Cost <= 150:
print("Shipping Costs 5")
else:
print("FREE")

```

### **开关语句**

switch case 语句是一个多分支语句，它将变量值与 case 中指定的值进行比较。Python 没有 switch 语句，但是可以使用其他方法实现，这将在下面讨论。

基本语法:

```
function(argument){
switch(argument) {
case 0:
return "This is Case Zero";
case 1:
return " This is Case One";
case 2:
return " This is Case Two ";
default:
return "nothing";
};
};

```

#### **开关情况陈述**

在一般计算机程序设计和相关语言中，switch case 语句是一种选择方式，使用搜索和选择过程，通过预定义变量或表达式的值来改变程序执行的控制流。switch 语句在某种程度上类似于 if 语句，在多种[编程语言](https://hackr.io/blog/best-programming-languages-to-learn)中使用，包括 C、C++、Visual Basic、Python、Pascal 和 Java。该语句的许多变体在其他语言中使用，如 case、inspect 或 select。

在大多数语言中，switch case 语句的典型语法如下:

*   首先定义控制表达式，在此基础上实现 switch 语句
*   定义大小写值的连续行以及匹配时将执行的后续语句
*   结束上述声明的结束声明

#### **用 Python 实现 Switch Case**

与许多其他语言不同，Python 没有默认的开关结构。如果您来自 Java 或 C++背景，这可能会感到奇怪，但在 Python 中，Switch 需要以迂回的方式实现，而不是直接实现。为了解决这个问题，需要使用 Python 预先构建的字典结构来定义案例和结果(如果遇到案例的话)。下面我们举一个例子，我们将定义一个函数 month()来告诉我们一年中的某个月份。在此执行映射的字典称为 switcher。

**语法**

```
>>> def month(i):
switcher={
1:'January',
2:'February',
3:'March',
4:'April',
5:'May',
6:'June',
7:'July',
8:'August',
9:'September',
10:'October',
11:'Novmber',
12:'December'
}

```

return switcher.get(i，“一年中的无效月份”)

现在，我们用不同的值调用 month()。

```
>>> month(1)
'January'
>>> month(3)
'March'
>>> month(13)
'Invalid month of the year'
>>> month(10)
'October'

```

正如您所观察到的，switcher 将只打印出提供给它的值，并在输入另一个值时返回一个“无效的月份”。它是在使用字典的 get()方法被告知这样做时发生的。

为了在 Python 中实现开关情况，我们也可以使用

*   Python 函数& Lambdas
*   Python 类

### 推荐 Python 课程

[用 Python 完成从零到英雄的 Python boot camp](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fcomplete-python-bootcamp%2F)

##  **Python 函数& lambdas**

可以使用 Python 函数& lambdas 在 Python 中实现 Switch case，其语法如下所示:

```
>>> def zero():
return 'zero'
>>> def one():
return 'one'
>>> def example(i):
switcher={
0:zero,
1:one,
2:lambda:'two'
}
func=switcher.get(i,lambda :’Invalid’)
return func()

```

**当不同的值通过它时，我们得到:**

```
>>> example(7)
‘Invalid’
>>> example(1)
'one'
>>> example(3.12)
'Invalid'

```

## **Python 类**

使用类的概念，我们可以用以下语法实现 Switch case:

```
>>> class Switcher(object):
def example(self,i):
method_name='number_'+str(i)
method=getattr(self,method_name,lambda :'Invalid')
return method()
def number_0(self):
return 'zero'
def number_1(self):
return 'one'
def number_2(self):
return 'two'

```

**当不同的值通过它时，我们得到:**

```
>>> s=Switcher()
>>> s.exampe(2)
'two'
>>> s.example(1.2)
'Invalid'
>>> s.number_1()
'one'

```

## **切换 Case vs If Else**

在计算机程序设计中，if-else 和 switch 语句都是选择语句。选择语句将根据条件的性质(真或假)将程序流程更改为特定的语句集。if-else 和 switch 语句的根本区别在于，if-else 语句将根据 if 语句中表达式的计算结果来选择语句的执行，而 switch 语句则根据键盘命令来选择语句的执行。

**用其他语言实现**

**If-Else**

if-else 是面向对象编程中的选择语句。下面是 if 语句的一般形式:

```
if (stated expression) {
statement (X)
} else {
statement (Y)
}

```

这里‘if’和‘else’都是关键词，上述语句既可以是单个语句，也可以是一组语句。在 if 语句中，表达式可以是整数、字符、指针、浮点或布尔类型。如果表达式返回“true”，则执行 If 中的语句，否则执行 else 中的语句。

让我们用一个例子来更好地理解:

```
int i=1, j=2;
if (i==1 & j==2){
cout<< "Yes";
}else{
cout<< "No”;
}

```

由于表达式为真，输出将为“是”

**开关**

如上所述，Switch 语句基本上是一个多项选择语句。switch 语句的一般形式如下所示:

```
switch( expression ){
case constant1:
statement(s);
break;
case constant2:
statement(s);
break;
case constant3:
statement(s);
break;
.
.
default
statement(s);
}

```

上面的表达式将只检查相等性，其他什么都不检查。将根据 case 语句中的常量来确认表达式，如果发现匹配，将执行与 case 相关联的语句，直到定义了“break”。由于 break 语句在 case 语句中不是必需的，所以如果缺少 break，执行将不会停止，直到语句结束。下面是一个用 C++执行的 switch 语句的例子:

```
int c;
cout<<" choose a value from 1 to 3"; cin>>i;
switch( i ){
case 1:
cout<<"you choose Red";
break;
case 2:
cout<<"you choose Blue";
break;
case 3:
cout<<"you choose Orange";
break;
.
.
default
cout<<"you choose nothing";
}

```

在上面的代码中，I 的值通过用户提供的值决定执行哪种情况。如果用户给定的值不是 1、2 和 3，将执行默认情况。

### **If-Else 和 Switch Case 语句之间的比较**

| **比较参数** | **开关盒** | **If-Else** |
| **执行** | 用户决定将执行哪个语句 | if 语句中表达式的输出将决定执行哪条语句 |
| **评估** | Switch 语句只能计算字符或整数值 | If-Else 语句可以计算整数、字符、指针、浮点和布尔类型 |
| **测试** | switch 语句测试相等性 | If-Else 语句测试等式和逻辑表达式 |
| **表情** | 一个表达式用于多个选择 | 多重语句用于多重选择 |
| **执行顺序** | 要么执行 if 语句，要么执行 else 语句 | switch 语句将一个接一个地执行，直到出现中断或到达语句末尾 |
| **违约案例** | 如果输入值与 switch 语句中的任何事例都不匹配，则执行默认事例 | 如果 If 语句中的表达式为 false，则默认情况下执行 else 语句 |
| **易于编辑** | 编辑 switch case 语句很容易，因为代码更简洁，大小写更容易识别 | 如果使用嵌套的 if-else，编辑语句可能会很麻烦 |

## **结论**

这几乎是你应该知道的关于 Python Switch Case 语句的所有内容。这个选择语句使得错误检测更容易，因为程序通过指定的情况被分成单元。虽然它只能检查相等性，但当需要比较一个变量的多个值时，如果您希望保持代码的整洁，它确实很有帮助。

如果您对 Python Switch Case 语句有任何疑问或有任何建议，请通过下面的专用评论部分提出。

刚开始用 Python 编码？查看我们众多关于 [Python 编程](https://hackr.io/blog/python-programming-language)的初级课程。

**人也在读:**