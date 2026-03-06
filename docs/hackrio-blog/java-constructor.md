# 关于 Java 构造函数你需要知道的

> 原文：<https://hackr.io/blog/java-constructor>

Java 中的构造函数是一个代码块，当创建一个对象的实例并为该对象分配内存时会调用它。这是一种用于初始化对象的特殊类型的方法。在声明构造函数时使用访问修饰符也是可能的。

构造函数是[有效学习 Java](https://hackr.io/tutorials/learn-java?ref=blog-post/) 的重要组成部分。因此，让我们从与创建 Java 构造函数相关的规则开始这篇全面的 Java 构造函数指南:

## **创建 Java 构造器的规则**

*   Java 构造函数不能有显式的返回类型
*   它不能是抽象的、最终的、静态的或同步的
*   构造函数名必须与其所属类的名称相同

### **Java 构造函数的类型**

Java 中有两种类型的构造函数:

#### **默认构造函数或无参数构造函数**

Java 默认构造函数没有参数。这就是它也被称为无参数构造函数的原因。Java 默认构造函数的一般语法是:

<class_name>(){}</class_name>

值得注意的是，如果 Java 类中没有定义构造函数，那么 Java 编译器会自动为该类创建一个默认的构造函数。根据对象的类型，默认构造函数为对象提供默认值。

使用由 javac 自动创建的默认构造函数的缺点是，程序员不能设置对象属性的初始值。

示例:

```
class ConstructorDemo
{
ConstructorDemo()
public static void main(String args[])
{
ConstructorDemo a = new ConstructorDemo();
}
}

```

输出:

```
The constructor is created successfully!

```

#### **参数化构造器**

任何带有多个参数的 Java 构造函数都被称为参数化构造函数。虽然参数化构造函数通常用于为不同的 Java 对象提供不同的值，但是它也可以为不同的 Java 对象提供相同的值。

示例:

```
class ParaConst
{
int id;
String name;
ParaConst(int i, String n)
{
id = i;
name = n;
}
void display()
public static void main(String args[])
{
ParaConst s1 = new ParaConst(121, “Akhil”);
ParaConst s2 = new ParaConst(232, “Vijay”);
s1.display();
s2.display();
}
}

```

输出:

```
121 Akhil
232 Vijay

```

### **构造函数重载**

像 Java 方法一样，在 Java 中重载构造函数是可能的。使用构造函数重载，可以有相同的构造函数，但有不同的参数列表。它们都是以这样的方式排列的，每一个都执行不同的任务。

Java 编译器根据列表中参数的总数和类型来区分重载的构造函数。以下代码片段演示了 Java 中的构造函数重载:

```
class OverloadConst
{
int id;
String name;
int age;
OverloadConst(int i,String n)
{
id = i;
name = n;
}
OverloadConst(int i, String n, int a)
{
id = i;
name = n;
age = a;
}
void display()
public static void main(String args[])
{
OverloadConst s1 = new OverloadConst(121, “Akhil”);
OverloadConst s2 = new OverloadConst(232, “Vijay”,25);
s1.display();
s2.display();
}
}

```

输出:

```
121 Akhil 0
232 Vijay 25

```

### **Java 中的构造函数与方法**

Java 方法是一段有特定名称的代码。只需使用方法名，就可以在程序的任何时候调用它。也可以理解为对数据进行操作并返回某个值的子程序。

Java 构造函数是一种特殊类型的方法。两者在许多方面相似，但不完全相同。以下是 Java 构造函数和 Java 方法之间的一些最重要的区别:

*   **调用–**当构造函数被隐式调用时，方法被显式调用
*   **Java 编译器—**Java 编译器从不提供 Java 方法。但是，如果 Java 类中没有定义构造函数，Java 编译器会提供一个默认的构造函数
*   命名约定 Java 中构造函数的名称必须与类的名称相同。但是，该方法可能与包含它的类同名，也可能不同
*   **调用次数–**Java 构造函数只在对象创建期间被调用一次。另一方面，Java 方法可以根据需要调用多次
*   **返回类型–**Java 方法必须有一个返回类型，但构造函数不一定要有相同的返回类型
*   使用–当一个方法被用于公开一个 Java 对象的行为时，一个构造函数被用于初始化该对象的状态

### **复制 Java 中的构造函数**

尽管 Java 中没有提供复制构造函数，但是可以将值从一个 Java 对象复制到另一个对象，就像在 C++中使用复制构造函数一样。

除了使用构造函数将值从一个对象复制到另一个对象，还可以通过以下方式实现:

*   将一个对象的值赋给另一个对象

或者

*   通过使用 Object 类的 clone()方法

以下程序演示了如何使用 Java 构造函数将值从一个 Java 对象复制到另一个对象:

```
class Copy
{
int id;
String name;
Copy(int i,String n)
{
id = i;
name = n;
}
Copy(Copy s)
{
id = s.id;
name = s.name;
}
void display()
public static void main(Strong args[])
{
Copy s1 = new Copy(121, ”Akhil”);
Copy s2 = new Coopy(s1);
s1.display();
s2.display();
}
}

```

输出:

```
121 Akhil
121 Akhil

```

### **关于 Java 构造器的一些常见问题**

以下是一些关于 Java 构造函数的最常见问题。以下是一些最受欢迎的 Java 面试问题:

问:构造函数返回任何值吗？
**A** :虽然不能对 Java 构造函数使用返回类型，但它会返回值。Java 构造函数返回当前的类实例。

**问:什么是 Java 中的构造函数链？**
**A** :构造函数链接(Constructor chaining)是 Java 编程语言中从某个其他构造函数调用一个构造函数的技术。this()方法用于调用同一个类构造函数，super()方法用于调用超类构造函数。

**问:Java 中可以从超类构造函数调用子类构造函数吗？**
**一**:没有

问:Java 有析构函数吗？
**A** : Java 没有析构函数，因为它是垃圾收集语言。在 Java 中，不可能预测一个对象何时被销毁。

问:除了初始化之外，Java 构造函数还可以执行哪些任务？
**A**:Java 构造函数可以执行任何可以用方法执行的操作。使用 Java 构造函数执行的一些最流行的任务是:

*   调用方法
*   对象创建
*   开始线程

问:Java 什么时候需要构造函数重载？
**A** :构造函数重载在 Java 中通常用在需要以几种不同的方式初始化 Java 对象的时候。

问:如果你为一个 Java 构造函数添加一个返回类型会发生什么？
**A** :带有返回类型的 Java 构造函数将被视为典型的 Java 方法，同时 Java 编译器会生成一个“[该方法有一个构造函数名](https://stackoverflow.com/questions/5163088/java-says-this-method-has-a-constructor-name)”警告。

[Java 编程大师班更新到 Java 17](https://click.linksynergy.com/link?id=jU79Zysihs4&offerid=1045023.533682&type=2&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fjava-the-complete-java-developer-course%2F)

## **总结**

这就是关于 Java 构造函数的全部内容。学习如何有效地使用构造函数是构建高级通用编程语言的重要部分。

您可以通过一些最好的 Java 书籍、教程、视频课程和代码练习来加深对 Java 构造函数的理解。

**人也在读:**