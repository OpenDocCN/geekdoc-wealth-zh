# Java 是什么？Java 初学者指南及其特性

> 原文：<https://hackr.io/blog/what-is-java>

哎呀… 对，这就是 Java！ [面向对象编程语言](https://www.youtube.com/watch?v=xoL6WvCARJY) 这是基于面向对象编程系统(OOPS)的概念。

Java 中的一切都是关于对象的。如果你得到了对象的本质，Java 就像吃了自己喜欢的食物一样简单，讨人喜欢。

好吧，但是你为什么要学 Java 呢？毕竟，有很多编程语言就像食物一样...

## **为什么是 Java？**

Java 就像你喜爱的各种美味(易于编码)和健康(安全和健壮)的食物！

除了 Java 是 2023 年[](https://hackr.io/blog/best-programming-languages-to-learn)顶级编程语言之一，并且可能至少在十年内保持这一地位之外，Java 已经在你能想到的几乎每个领域取得了成功！

由于 Java 是安全的和多线程的，它非常适合于银行业务、交易管理服务。 *电子商务* 商店和计费软件的逻辑都写在基于核心 Java 的框架中。像 *安卓* 这样的移动 OS 都是使用 Java APIs。 *股市* 算法都是基于 Java 开发出来的。而最近，所有的 *大数据*——海量数据用 Java 处理起来轻而易举。其实 Hadoop 的 MapReduce 框架是用 Java 写的。Java 和 Spring 之类的其他框架形成了一个强大的组合，可以在 *金融* 和 *IT* 领域对实现依赖进行排序并编写服务器端应用程序。

## **什么是 Java 编程？**

Java 是由 Sun Microsystems 开发的一种一次编写、随处运行的编程语言。它类似于 C 和 C++，但要简单得多。你可以把 Java 和很多技术结合起来，比如 Spring、node js、Android、Hadoop、J2EE 等等，来构建健壮的、可伸缩的、可移植的和分布式的成熟应用。Java 还提倡使用 Selenium 等工具进行持续集成和测试。

### **Java 的历史**

Java 最初是由詹姆斯·高斯林和他在太阳微系统公司的同事在 20 世纪 90 年代早期开发的。最初，它被称为“Oak”项目，其实现类似于 C 和 C++ 。Java 这个名字是经过充分的头脑风暴后选定的，它是基于一种浓缩咖啡豆的名字。Java 1.0 的第一个版本发布于 1995 年，口号是“一次编写，随处运行”。后来太阳微系统被甲骨文收购。从那以后，我们再也没有回头看。Java 的最新版本是 2019 年 3 月发布的 Java 12。

### **Java 的特性**

Java 提供了许多吸引人的特性-

*   平台无关语言
*   丰富的标准库使编码变得容易。您可以使用 Java 创建一个完整的独立应用程序。
*   Java 支持自动内存分配和回收(称为垃圾收集)。
*   由于 Java 支持多线程和并发性，它提供了很好的性能，从而使它成为一种高度交互式和响应性的语言。
*   安全简单

要了解 Java 的更多特性，请务必阅读[](https://hackr.io/blog/features-of-java)这篇好文章。

**什么是 Java 平台？**

你一定听说过很多关于 Java 作为编程语言的事情。但是，你知道它也是一个“平台”吗？Java 平台是一个纯软件平台，与 Windows、Mac、Linux 或 Solaris 等传统平台截然不同。前者运行在后者平台的硬件之上。 Java 程序通过 Java 虚拟机，将字节码转换成本机码，从而使程序可以在任何设备上运行！这意味着您不需要单独的特定于机器的编译器来运行 Java 代码。这也是 Java 被称为 *平台* 的原因。Java 编程语言是与 Java 平台不同的。Java 编程语言帮助你构建应用程序。你用 Java 编程语言写的东西是在一个现有的程序和工具集合的帮助下开发和运行的，这些程序和工具统称为 Java 平台。Java 平台由 JDK、JVM 和 JRE 组成。

Java 编程语言有四个 Java 平台—

*   Java SE (Java 平台，标准版)
*   Java EE (Java 平台，企业版)
*   Java 外汇
*   Java ME (Java 平台，微型版)

虽然可以在 Java SE 平台上构建独立的应用程序，但大多数万维网(互联网)都依赖于 Java EE。Java ME 适用于小型设备(如手机)上的应用程序。

### **Java 的组件**

Java 有三个主要组件——JVM、JDK 和 JRE。

JDK 或 Java 开发工具包是开发人员编写代码并通过 JRE 或 Java 运行时环境运行代码的地方。

代码是如何翻译的？那是通过 Java 虚拟机(JVM)实现的。使用 JVM，任何用 Java(或任何其他语言)编写的代码都可以翻译成 Java 字节码。任何机器都可以基于操作系统实现这些代码。JVM 和 java 包(库)一起驻留在 JRE 中。

| **JDK** | JVM | **JRE** |
| JRE +开发工具，如解释器(类加载器)、编译器(javac)、jar 文件(打包和归档)和 javadocs。 | java 字节码被执行的抽象机器。由一个描述 JVM 实现的 *规范* 文档，实际的 *实现* 程序和 JVM 的 *实例* (运行时)组成，在其中可以运行主程序。 | JVM 的物理实现(运行时实例)。它包含 JVM 用于运行程序的库包和支持文件。 |

如果你有一个系统，你可以在阅读这篇文章的时候尝试一些事情。为了练习，您需要在本地系统上安装 JDK (Java 开发工具包)和 JRE (Java 运行时环境)。 **[下载最新版本，点击这里](https://docs.oracle.com/javase/9/install/installation-jdk-and-jre-microsoft-windows-platforms.htm#JSJIG-GUID-2B9D2A17-176B-4BC8-AE2D-FD884161C958)** 。

然后，您可以在您的系统上设置一个 IDE，学习我们将要学习的概念。每当我需要在 Java 上运行程序时，Eclipse 是我使用的一个很好的 IDE。它很容易设置，不会打扰你太多。可以下载 [月蚀](https://www.eclipse.org/downloads/packages/release/2019-03/r/eclipse-ide-java-developers) 或者 易月蚀 。Easy Eclipse 是 Eclipse 的一个较轻版本，具有较少的特性。还有很多 IDE，看看这里的[](https://hackr.io/blog/best-java-ides)。

如果你现在不想做这些，而只想阅读关于 Java 的书籍，那也没关系！继续读下去，理解概念，然后随时开始编码！

还有哦，这是一个很好的 Java 认证课程( [Java 认证项目)。](https://hackr.io/blog/java-certification-courses) )，学完基础知识后你会爱上它的！

[JavaScript 全教程 2023:从零到专家！](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fthe-complete-javascript-course%2F)

### 你都准备好了吗？

在我们开始编码之前，让我们熟悉一些术语

每个 java 程序都是由类或接口定义的不同类型对象的集合。这是基本结构

```
class School {
//consists of several other objects and instance variables
public String schoolName;
public int ID;
Teacher[] teachers;
Student[] students;
…..
// and then some methods
public int getSchoolName()
{
}
}

```

逻辑都在**方法**中，可以简单到一个类的 getter 和 setter 方法，也可以复杂到根据多个条件从数据库中获取数据！

让我们写一个简单的程序，当我们学习更多的 Java 概念时，我们会添加它

注意，就像任何其他编程语言一样，Java 中的每个独立程序都应该有一个 **main 方法**来执行。

创建一个测试类，并向其中添加一些简单的代码。

```
class Test{
public static void main(String args[]){
int rollNumber = 34;
String name = “Humpty”;
System.out.println(“My name is ” + name + “ and my roll number is ” + rollNumber);
}
}

```

这段代码的每一行都有学问。

*   **类****–**该关键字用于创建一个 java 类。当你运行这个程序时，你可以给出命令 javac Test.java 来编译，Java Test.java 来执行。如果您使用的是 IDE，您只需右键单击该类并选择 Run。
*   **public****–**public 是表示可见性的访问修饰符。main 方法不能将访问修饰符作为 private(访问修饰符)。私有方法只能在类内部调用，而公共方法对所有人都是可见的。
*   **静态**-**-**变量和方法可以使用 static 关键字。*为什么*是静态的主要方法？对于静态方法，我们不必创建对象。因此，我们不必创建一个测试对象来调用 main 方法。
*   **void****–**如果一个方法不返回任何值，那么它的类型被设置为 void。
*   **int，String****–**这是 Java 使用的许多数据类型中的两种。因为它也使用基本类型，Java 不被认为是完全面向对象的语言。
*   **System . out . println****–**out 是类系统的静态字段。该字段存储 PrintStream 类的实例。println()是这个类的方法，它将所需的输出打印到控制台。

让我们稍微修改一下这个程序，从用户那里得到名字和卷号*作为输入。有很多方法可以做到这一点。对于这段代码，让我们使用最常见的方法——**扫描器**类。要使用这个类，我们需要将类导入为**import**Java . util . scanner；*

在前面的代码中，在 System.out.println (syso)之前，让我们添加以下代码行

```
Scanner scanInput = new Scanner(System.*in*);
System.*out*.println("Enter name: ");
name = scanInput.nextLine();
System.*out*.println("Enter roll number: ");
rollNumber = scanInput.nextInt();

```

运行该程序时，系统会提示您输入姓名，然后输入卷号。

另一种方法是通过 BufferedReader，这是传统的方法，但它有太多的包装，可能很难记住。

让我们获得更多学生的信息——他们的姓名、学号和科目。科目将在**数组**中，因为对于这个程序，让我们假设，一个学生将承担 3 个科目。

将数组定义为-

```
String[] subjects = new String[3];
//Get all the subjects from the student
for(int j=0; j<subjects.length;j++){
subjects[j] = scanInput.next();
}

```

*   这里我们使用一个循环的**从用户那里获取主题，并将其存储在字符串数组中。在最新的 java 版本中，loop 的语法发生了变化，但是这种语法更容易使用。‘j’是从 0 开始的临时计数器。注意我们做 j**
*   **subjects.length** 获取数组的长度，在本例中是 3。

要查看数组的内容，请键入 Arrays。 *toString* (主题)

如我们所见，我们有三个变量 name、rollNumber 和 subjects，它们都属于一个公共实体 Student。那么，为什么不创建一个类并将这 3 个变量作为类的成员呢？当我们将数据作为对象使用时，添加、修改和删除数据将变得更加容易！

让我们创建一个 Student.java 班级

```
public class Student {
int rollNumber = 0;
String name = "";
String[] subjects = new String[3];
}

```

我们必须修改代码来创建这个类的对象，并通过 getter 和 setter 方法访问变量。getter 和 setter 方法的一个例子是

```
public int getRollNumber() {
return rollNumber;
}
public void setRollNumber(int rollNumber) {
this.rollNumber = rollNumber;
}

```

IDE 会为你创建所有这些，但是对于你的练习，你自己做就好了。

现在，让我们回到我们的主要节目。

我们已经有了一个学生的所有数据，为什么不获取更多学生的详细信息呢！我们可以创建一个学生对象数组，并将每个学生的详细信息存储在数组中的一个对象中。

让我们从用户那里得到学生的数量

**int**number of students = scan input . nextint()；

现在，让我们开始另一个 for 循环，它将从所有学生那里获得详细信息

```
for(int i=0;i<numberOfStudents;i++){
//get details
}

```

我们现在要做的就是将数据设置到学生对象中。为此，创建一个与 numberOfStudents 大小相同的 Student 对象数组。

```
Student[] student = new Student[numberOfStudents];
for(int i=0;i<numberOfStudents;i++){
student[i] = new Student();
name = scanInput.next();
student[i].setName(name);
rollNumber = scanInput.nextInt();
student[i].setRollNumber(rollNumber);
// As we have written earlier
for(int j=0; j<subjects.length;j++){
subjects[j] = scanInput.next();
}
student[i].setSubjects(subjects);
}
```

**代码中的几件事—**

*   当我们创建 Student[]数组时，各个 Student 对象仍然为空。这就是为什么在 for 循环中，我们要创建新的 Student 对象。当我们试图使用 student[i]时，不这样做将抛出一个 NullPointerException..我们将在本文后面触及异常。
*   我们对字符串使用 next()而不是 nextLine()。nextLine()将跳过当前行，转到下一行。使用 next()总是更好。
*   比如说，用户给出的学生数量为 2。外部 for 循环将执行两次。主题数组的大小是 3，所以内部 for 循环将为每个外部循环执行 3 次，因此总共执行 6 次。
*   注意 Java 中的**命名约定。变量名和方法名以小写开头，但是我们将每个单词的第一个字母大写，而类名以大写字母开头。**

现在，我们拥有学生数组中的所有数据。我们可以使用一个 **[Java 构造函数](https://hackr.io/blog/java-constructor)****来改进代码，这是一种比 setter 方法更有效的存储对象的方式。当您有大量数据时，您可以一次设置构造函数中的所有值，而不是使用 set 方法 10 次。让我们在学生类中创建一个构造函数。**

```
public Student(String name, int rollNumber, String[] subjects){
this.name = name;
this.rollNumber = rollNumber;
this.subjects = subjects;
}

```

现在，让我们修改我们的测试类来使用这个构造函数。注意，现在这一行

```
student[i] = new Student();

```

将不起作用，因为我们还没有在我们的类中创建一个无参数构造函数。当没有定义其他构造函数时，java 编译器默认创建无参数构造函数，否则，我们应该使用我们在代码中创建的构造函数。

我们的代码现在将变成–

系统。*出*。println("输入姓名和卷号:")；

**Student[I]=****new****Student(scan input . next()，scanInput.nextInt()，subjects)；**

这为我们减少了大约 3-4 行代码。想象一下，当有更多的对象和成员变量时，它会多么有用。注意，subjects 数组将为空，因为我们在 name 和 rollNumber 之后获取 subjects 的值。

下一个问题是我们在哪里存储这些学生对象，以便我们可以在以后检索它们，并做一些修改或显示列表的内容？简单的回答就是 **ArrayList** 。创建一个数组列表并向其中添加对象非常简单。

数组列表的一些重要特性

*   数组列表是动态的。我们可以随时扩展 ArrayList，大小不是固定的，不像数组。
*   ArrayList 是 [**Java 集合框架**](https://hackr.io/blog/java-interview-questions) **的重要组成部分。**
*   我们可以随机访问列表中的任何对象。
*   我们只能在数组列表中存储对象。如果我们必须创建一个整数数组列表，我们需要将原始的 int 类型包装到 Integer 对象中。

回到我们的代码，让我们创建如下的数组列表

ArrayList student list =**new**ArrayList()；

要将对象添加到列表中，在获取所有细节后，只需将完整的对象添加到列表中。

student list . add(student[I])；

不要用循环遍历一个数组并把每个对象作为 student[0]、student[1]等等来迷惑我们自己，让我们使用一个**迭代器**来获取并显示数据。

可以把迭代器想象成一个光标，它遍历集合中的元素。您可以使用迭代器从集合中获取或移除任何元素。

```
Iterator itr = studentList.iterator();
System.*out*.println("The entered details of all the students are---");
while(itr.hasNext())
{
System.*out*.println(itr.next().toString());
}

```

*   我们不创建 Iterator()的新对象，而是使用列表的迭代器方法指向 itr。
*   **while 循环**使用 hasNext()方法检查列表中是否还有其他对象。当 hasNext()返回 false 时，while 循环将结束。
*   itr.next()获取列表中的下一项。

您可能希望输出是您输入的整洁的细节。对吗？但是 Java 会给我们这样的东西——

输入的所有学生的详细信息是-

**学生@e7b241**

为什么？

因为要单独打印对象的成员，我们需要在学生类中覆盖 toString()方法。

```
public String toString(){
String studentDetails = null;
studentDetails = "Student name: " + this.name + ", Student roll number: " + this.rollNumber + " , Chosen subjects: " + Arrays.*toString*(this.subjects) + "\n";
return studentDetails;
}

```

*   **this** 关键字是一个引用变量，指向当前类的实例变量。
*   为了从数组中获取值，我们使用实用程序类 **Arrays** 的 toString()方法。注意数组包含了静态的**方法，因此我们不需要创建一个对象来使用这些方法。我们直接使用类名和方法名。**

瞧啊。你现在会得到你想要的结果！

但是，有一个问题…

我们还没有考虑用户输入错误的情况！例如，如果有人为 rollNumber 输入一个字符串会怎么样？我们不会向用户抛出异常的整个堆栈跟踪。相反，我们可以向用户传递一条好消息。

尝试为 rollNumber 输入字符串，将在线程“main”Java . util . inputmismatchexception 中出现异常

为了确保这种情况不会发生，我们需要确保用户输入正确的值。但是，怎么做呢？让我们放一个 **try/catch 块**来捕捉异常，并在出现错误时向用户显示友好的消息。

```
try{
rollNumber = scanInput.nextInt();
}catch (InputMismatchException ime){
System.*out*.println("Please enter a valid number");
}

```

我们也可以对许多学生应用同样的方法。最佳实践是将整个代码放在 try 块中，以便可以在 catch 块中捕获任何异常。

这在 Java 中被称为异常处理。在现实世界的应用程序中，类可以**抛出**异常，最后一个类将捕获并向用户显示适当的消息。Java 中还有很多运行时异常，最常见的有 NullPointerException、ClassCastException、ArithmeticException、IllegalArgumentException、ArrayIndexOutOfBoundsException 等……

### **快速回顾一下**

在本文中，我已经接触了 Java 的基础知识，只要你知道什么是编程语言，并且以前使用过其他语言，你就可以开始用 Java 编写代码。我们已经理解了——的基本概念

*   类和对象
*   构造器
*   输入输出流
*   For 和 while 循环
*   原始和非原始数据类型
*   toString()方法
*   集合(数组列表)和迭代器
*   异常处理的基础

通过一个简单的程序。有许多高级概念不在本文的讨论范围内，但是，请继续关注，因为我们将推出更多关于高级概念的文章，如线程、内部类、接口、垃圾收集等等。

从最好的 Java 教程和课程开始学习 Java。

**人也在读:****