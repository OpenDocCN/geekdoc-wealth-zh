# C#与 Python:面对面的比较[更新]

> 原文：<https://hackr.io/blog/c-sharp-vs-python>

C#和 Python 都是 2023 年 的 [流行编程语言。两者都基于面向对象的概念，易于学习和编码，并提供快速开发和良好的性能。在我们深入研究差异之前，让我们快速了解一下每种差异，以便更好地理解差异。](https://hackr.io/blog/best-programming-languages-to-learn)

## **c#概述**

C#是一种功能强大的语言，它紧跟传统的 C [&c++结构，但是它更现代，也更容易学习。由微软开发的这种面向对象的编程语言与 Java 也有许多共同之处。C#代码可以在不同的平台上编译，并且有很多强大的特性，比如–

*   与…结合。NET 框架
*   面向组件
*   高级结构化语言
*   现代句法；简单易学
*   丰富的标准库
*   自动垃圾收集

C#程序的基本结构类似于 C++和 Java。一个名称空间声明、类定义(变量和方法)、main 方法——就是这样。下面是一个简单的程序，它打印出一个用户的名字。

```
using System;
namespace PrintNameApplication {
   class PrintUserName {
      static void Main(string[] args) {
         /* Write user name to console */
 String userName;
userName = Console.ReadLine();
         Console.WriteLine("Hello, " + username + ". How are you today?");
      }
   }
} 

```

以下是代码的解释—

*   想想 **使用** 关键字类似于 import 或 include 语句，这意味着如果我们想在程序中使用系统命名空间，我们使用‘using’语句来包含它。一个程序中可以有许多“using”语句。
*   **命名空间** 包含了一个类的集合。如果有多个同名的类，每个类都可以用名称空间唯一标识。
*   **包含了类方法(本例中的 **主** 方法)。当我们运行程序时，main 方法被执行。Main 方法是任何 C#程序的入口点。**
***   在这个程序中，我们获取用户输入，并显示同样的信息。因为我们从控制台获取它，所以我们使用一些基本的 I/O 方法，比如 ReadLine()和 WriteLine()。**

 **### **c#的好处**

C#与强大的集成在一起。NET 框架。另外，如果你懂 Java，想搬到。NET，学习 C#可以给你必要的提升。C#的一些好处是-

*   简单、强大且可扩展
*   类型安全代码，C#不允许不安全的强制转换
*   快速编译和执行时间
*   结构化编程语言
*   支持语言互操作性

## **Python 概述**

就像 C#，Python 是一种通用编程语言。它的大多数特性都遵循 C & Java。这种具有高级编程能力的语言易于移植和学习。

### **你想知道-**

既然已经有这么多种编程语言，为什么还要有另一种呢？嗯，因为 Python 是从许多其他语言派生出来的，所以它拥有所有语言中最好的特性。首先，我们可以说它是一种动态类型语言(即类型检查是在运行时完成的)。其次，如果你想对现有的遗留系统进行修改，Python 是你应该选择的语言。最后，如果你是编程新手，那么 [Python 是你开始](https://hackr.io/blog/python-programming-language) 编程之旅的起点。

### **Python 的一些特性—**

*   支持面向对象编程以及函数式和结构化编程
*   易于编码、读取、维护和移植
*   一个丰富的标准库，可移植并兼容各种平台，如 Windows、Mac 或 Unix。
*   支持自动垃圾收集

让我们用 Python 编写相同的 PrintName 程序，感受一下代码的感觉—

```
# print name
name = input("Enter your name-")
print("Your name is ", name)

```

我们在 C#中用大约 10 行代码完成的工作，在 Python 中只用 2 行代码就完成了。代码就像用英语输入一个句子一样！请注意，这里没有“；”(分号)在每一行的末尾。与 C#中的“/*”相比，注释是使用“#”添加的。没有类型声明。我没有写过“字符串名称”代码中的任何地方。没有进口货！

嗯——这就是我们谈论的轻松程度！

### 推荐 Python 课程

[用 Python 完成从零到英雄的 Python boot camp](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fcomplete-python-bootcamp%2F)

### **Python 的更多优势**

*   使用 Python 包索引(PyPI ), Python 可以与大多数其他语言和平台进行交互。PyPI 有一套第三方模块来实现这一点。
*   庞大的标准库，包括操作系统接口、web 服务工具等等。
*   免费使用和分发；Python 是在开源许可下开发的
*   适用于使用多种协议的网络应用。

## **C# vs Python:面对面比较:**

现在我们对这两种语言都有了基本的了解，让我们一起来比较一下更深刻的差异

| **C#** | **Python** |
| 由微软开发。有执照的。 | 开源开发和发布，甚至用于商业用途 |
| 基于面向对象的概念 | 支持多范例编程(OOP，过程化) |
| 静态类型化。编译器会给出错误类型转换的错误信息 | 动态铅字铸造。不需要变量声明。 |
| 支持工作。NET 框架 | 可与 Java (JVM)集成。NET、C 和 JavaScript |
| 依赖注入非常有效。 | 没有 DI 这样的概念，但是，你可以在运行时给任何对象添加定制的标签或者做 [猴子补丁](https://stackoverflow.com/questions/5626193/what-is-monkey-patching) 来指向不同的第三方代码进行测试。 |
| 更加有条理和一致的语法和格式。 | 简单，易于阅读和编码，不包含太多的符号或格式。 |
| 多静态语言。一切都要构建(编译)然后运行。 | 由于一切都是动态的，在运行时挑选，减少了开发周期中的整个步骤。 |
| 没有翻译 | 交互式解释器轻松编写程序 |
| 由于有了公共语言基础设施(CLI)框架，C#速度更快，性能更好 | 开发工作更快，但相比 C#，性能稍有欠缺。 |
| 库支持是好的，有其基础。NET 框架 | 其 [庞大的一套预打包库](https://hackr.io/blog/top-python-libraries) 中没有跳动的 Python。许多代码可以重用，这使得开发人员的工作变得容易 |
| 使用多线程非常容易。NET 框架 | 由于全局解释器锁(GIL)，多线程需要多个进程。 |

**结论**

不可否认，C#像面向对象语言一样有更有组织的结构。这意味着语法和格式规则没有不一致。然而，Python 中的代码很容易编写，因为有大量的标准库。C#可以做 Python 能做的所有事情，并提供更好的性能。Python 让你快速而简洁地进行编码。不像 C#中那样有多个大括号({})的混淆。Python 有一些很棒的内置数据类型。如果你既想用 Python 又想用 C#，那就去用[【IronPython】](https://hackr.io/blog/python-interpreters)，这是为那些想用 Python 写的人开发的。NET 框架。它是 Python 的微软实现，用 C#编写。这样你可以探索两种语言的优点，并在适当的时候使用它们。最后 2 美分——想想 Windows 上的 C#和 Linux 上的 Python！

**人也在读:****