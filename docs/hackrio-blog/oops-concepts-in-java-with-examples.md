# Java 中的 OOPS 概念及示例

> 原文：<https://hackr.io/blog/oops-concepts-in-java-with-examples>

面向对象编程是一种开发方法和组织，它试图通过将结构化编程的最佳特性与几个新概念相结合来消除传统编程方法的一些缺陷。它涉及组织和开发程序的新方法，而不涉及使用特定的语言。支持 OOP 特性的语言有 Smalltalk，Objective C， [C++](https://hackr.io//tutorials/learn-c-plus-plus?ref=blog-post) ，Ada， [Pascal](https://en.wikipedia.org/wiki/Pascal_(programming_language)) ，以及 [Java](https://hackr.io//tutorials/learn-java?ref=blog-post) 。

## Java 中 OOPS 概念的定义

所以我们可以将 OOP 编程定义为:

“面向对象编程是一种将程序模块化的方法，它为函数和数据创建一个分区内存区域，这些内存区域可用作模板，用于按需创建此类模块的副本。”

## 哎呀范例

面向对象方法的主要目标是消除[过程方法](https://hackr.io/blog/procedural-programming)中存在的一些缺陷。OOP 将数据视为程序中的一个元素，不允许它在系统中自由流动。它将数据与对其进行操作的函数紧密地联系在一起，并保护数据不被其他现有函数无意地修改。OOPS 允许将一个问题分解成几个称为对象的实体，然后从这些实体中构建数据和函数。数据的组合构成了一个对象。

![](img/9932471e77adba9bd7abd2c469746c24.png)

对象=方法+数据

对象的数据由与该对象关联的方法访问。但是，一个对象的方法可以访问其他对象的方法。

## OOPS 的功能

java 中面向对象编程的一些特性是:

*   重点是数据而不是程序
*   程序被分成对象
*   数据结构被设计用来描述对象的特征。
*   对对象数据进行操作的方法在数据结构中联系在一起。
*   数据是隐藏的，外部函数无法访问它。
*   对象通过方法相互通信
*   必要时，可以很容易地添加新方法和数据
*   在程序设计中遵循自下而上的方法

## Java 中 OOPS 概念的列表及示例

Java 中的一般 OOPS 概念是:

### **对象和类别**

对象是面向对象系统中的运行时实体。一个对象可以代表一个人，一个银行账户，一个地方，一个数据表。它也可以表示用户定义的数据类型，如列表和向量。任何编程问题都是基于对象以及它们之间如何通信来分析的。当一个程序被执行时，这些对象通过互相发送消息来进行交互。例如，“客户”和“帐户”是两个对象，它们可以向帐户对象发送请求余额的消息。每个对象都包含操作数据的代码和数据。对象甚至可以在不知道彼此代码或数据细节的情况下进行交互。

使用类的概念，可以将对象的全部代码和数据设置为用户定义的数据类型。一个类是一种“数据类型”,一个对象是该类型的“变量”。创建一个类后，可以创建任意数量的对象。

相似类型的对象的集合被称为一个类。例如，苹果、桔子和芒果是水果类的对象。类的行为类似于[编程语言](https://hackr.io/blog/what-is-programming-language)的内置数据类型，但是是用户定义的数据类型。

![](img/9d72c3829263fdddd48ce53690f290b9.png)

对象的表示

### **数据抽象和封装**

将数据和方法包装成一个单元称为封装。数据只能被包装在类中的那些方法访问，而不能被外界访问。这种将数据与程序的直接访问隔离开来的做法称为数据隐藏。对象的封装使得对象可以像执行特定任务的“黑盒”一样被处理，而无需考虑内部实现。

![](img/1158ee2d1298d7bba07421c16532120d.png)

封装——作为“黑盒”的对象

抽象是通过表示基本特征而不包括背景解释或细节来降低编程复杂性的行为。类是抽象的概念，被定义为抽象属性的列表，如大小、重量、成本和对这些属性进行操作的方法。类包装或封装了要创建的对象的所有基本属性。

#### **抽象类和抽象方法:**

1.  抽象类是带有抽象关键字的类。
2.  抽象方法是没有方法体的方法。
3.  一个抽象类可能没有所有的抽象方法。有些方法是具体的。
4.  定义抽象的方法必须在派生类中实现，因此方法重写是强制性的。使子类抽象可以避免重写。
5.  包含抽象方法的类必须用 abstract 关键字声明。
6.  抽象类的对象不能用 new 运算符进行实例化。
7.  抽象类可以有参数化的构造函数。

#### **实现抽象的方式:**

*   使用抽象关键字
*   使用接口

#### 示例代码:

下面的代码展示了一个抽象的例子。

```
abstract class Car
{
 Car()
 {
  System.out.println("Car is built. ");
 }
 abstract void drive();
 void gearChange()
 {
  System.out.println("Gearchanged!!");
 }
} 

class Tesla extends Car
 {
  void drive()
  {
   System.out.println("Drive Safely");
  }
 }

class Abstraction 
 {
  public static void main (String args[])
  {
   Car obj = new Tesla();
   obj.drive();
   obj. gearChange();
  }
 }
```

### **继承**

继承是一个类的对象获得另一个类的对象的一些属性的过程。继承支持层次分类的概念。例如，知更鸟是类的一部分，而不是哺乳动物，哺乳动物也是动物类的一部分。这种划分背后的原则是，每个子类共享来自其父类的类的共同特征。

![](img/e5ab58c0b31d8e144ae83b302167010a.png)

继承的属性

在 OOP 中，继承的思想提供了可重用性的概念。这意味着我们可以在不修改的情况下向父类添加额外的特性；这可以通过从父类派生一个新类来实现。新类由两个类的组合功能组成。在 Java 中，派生类也称为子类。

#### 继承的类型

*   单一的
*   多重
*   多层次的
*   混合物

#### 示例代码:

下面的代码演示了一个继承的例子。

```
class Animal 
{
 void eat()
 {
  System.out.println("I am a omnivorous!! ");
 }
}

class Mammal extends Animal 
{
 void nature()
 {
  System.out.println("I am a mammal!! ");
 }
}

class Dog extends Mammal 
{
 void sound()
 {
  System.out.println("I bark!! ");
 }
}

class Inheritance 
{
 public static void main(String args[])
 {
  Dog d = new Dog();
  d.eat();
  d.nature();
  d.sound();
 }
}
```

### **多态性**

多态性是一个重要的 OOP 概念；它意味着采取多种形式的能力。例如，一个操作在不同的情况下表现出不同的行为。该行为取决于操作中使用的数据类型。例如，在加法运算中，该运算生成两个数的和。如果操作数是字符串，那么第三个字符串是通过连接操作产生的。

下图演示了可以使用一个函数名来处理不同数量和不同类型的参数。

![](img/30eca935fc5725163bfc911bd190288a.png)

在多态中，具有不同内部结构的对象可以共享同一个外部接口；这意味着即使每个操作的动作可能不同，也可以以相同的方式访问一个操作类。继承广泛使用了多态的概念。

多态性可以通过两种方式实现:

#### **方法重载**

可以创建具有相同名称但不同参数列表和不同定义的方法。这被称为方法重载。当需要对象执行类似的任务但使用不同的输入参数时，就需要方法重载。当我们调用对象中的方法时，Java 首先匹配方法名，然后匹配参数的数量和类型，以决定执行哪个定义。

方法重载通过三种方式实现:

| **在**的基础上 | **例子** |
| **参数数量** | 

```
times(int, int)
times(int, int, int)
```

 |
| **参数的数据类型** | 

```
times(int, int)
times(int, float)
```

 |
| **参数数据类型的顺序** | 

```
times(int, float)
times(float, int)
```

 |

#### 示例代码:

下面的代码演示了方法重载的概念。

```
class CircleArea 
{
 double area(double x)
 {
  return 3.14 * x;
 }
}

class SquareArea 
{
 int area(int x)
 {
  return x * x;
 }
}

class RectangleArea 
{
 int area(int x, int y)
 {
  return x * y;
 }
}

class TriangleArea 
{
 int area(int y, int x)
 {
  return (y * x)/2;
 }
}

class Overloading 
{
 public static void main(String args[])
 {
  CircleArea ca = new CircleArea();
  SquareArea sa = new SquareArea();
  RectangleArea ra = new RectangleArea();
  TriangleArea ta = new TriangleArea();

  System.out.println("Circle area = "+ ca.area(1));
  System.out.println("Square area = "+ sa.area(2));
  System.out.println("Rectangle area = "+ ra.area(3,4));
  System.out.println("Triangle area = "+ ta.area(6,3));
 }
}
```

#### **方法覆盖**

超类中定义的方法由其子类继承，并由子类创建的对象使用。然而，可能有这样的情况，当一个对象应该响应相同的方法，但是在调用该方法时表现不同，这意味着超类中定义的方法被覆盖。重写是通过在子类中定义一个与超类中的方法具有相同名称、相同参数和相同返回类型的方法来实现的。因此，当调用方法时，调用并执行子类中定义的方法，而不是超类中的方法。

#### 示例代码:

下面的代码演示了方法重写的概念。

```
class Shape 
{
 void draw()
 {
  System.out.println("Mention shape here");
 }

 void  numberOfSides()
 {
  System.out.println("side = 0");
 }
}

class Circle extends Shape 
{
 void draw()
 {
  System.out.println("CIRCLE ");
 }

 void numberOfSides()
 {
  System.out.println("side = 0 "); 
 }
}

class Box extends Shape 
{
 void draw()
 {
  System.out.println("BOX ");
 }

 void numberOfSides()
 {
  System.out.println("side= 6"); 
 }
}

class Triangle extends Shape 
{
 void draw()
 {
  System.out.println("TRIANGLE ");
 }

 void numberOfSides()
 {
  System.out.println("side = 3 ");
 }
}

class Overriding 
{
 public static void main (String args[])
 {
  Circle c = new Circle();
  c.draw();
  c.numberOfSides();

  Box b = new Box();
  b.draw();
  b.numberOfSides();

  Triangle t = new Triangle();
  t.draw();
  t.numberOfSides();
 }
}
```

### **动态绑定**

绑定是将过程调用链接到响应调用而执行的代码的过程。这意味着与给定过程调用相关联的代码在运行时调用之前是未知的。它与遗传和多态性有关。

**消息通信**

对象在 OOPs 中相互通信。在 OOP 的情况下，编程过程包括以下内容:

*   创建定义对象及其行为的类。
*   创建对象
*   在对象之间建立通信。

相互通信的对象网络

![](img/50dae1e8c4f57b712eea01fba23af68a.png)

消息传递涉及到指定对象名、方法名和要发送的信息。

**例如，考虑语句。**

**![](img/12fe05888bcf018b71b524b252ebc786.png)**

对象可以被创建或销毁，因为它们有生命周期。它允许对象之间的通信，直到对象是活动的。

[Java 编程大师班更新到 Java 17](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fjava-the-complete-java-developer-course%2F)

## **Java 中 OOPs 概念的好处**

*   继承消除了冗余代码，并实现了可重用性。
*   由于消息传递允许与对象通信，这就意味着每次都要从头开始编写代码。因此，它节省了开发时间，提高了生产率。
*   分区基于类和对象在项目中工作。
*   系统升级很容易。

## **OOPs 概念在 Java 中的应用**

*   实时系统
*   模拟和建模
*   面向对象的数据库
*   超文本和超媒体
*   人工智能和专家系统
*   神经网络和并行编程
*   自动化系统

## **总结**

Java 是一种健壮的、可伸缩的面向对象的编程语言，它基于对象和类的概念。它为开发高效可靠的代码提供了继承、抽象、封装和多态等特性。

**人也在读:**