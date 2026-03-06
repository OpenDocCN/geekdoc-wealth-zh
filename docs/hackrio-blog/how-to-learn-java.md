# 2023 年如何学习 Java(循序渐进指南)

> 原文：<https://hackr.io/blog/how-to-learn-java>

Java 是 2023 年顶级编程语言之一。Java 是一种健壮的、静态类型的、安全的、基于类的编程语言，已经统治 web 一段时间了。几乎所有领域都使用 Java，如零售、金融、医疗保健、物流等。它具有兼容性和通用性，可用于移动、桌面和 web 应用程序、游戏、web 服务器、应用服务器、**数据库连接**、客户端验证等等。

该产品是免费的，开源增加了它的受欢迎程度。此外，大多数毕业生将学习 C/C++作为他们课程的一部分，所以学习 Java[](https://hackr.io/tutorials/learn-java)**变得很容易，这篇博文将为你提供如何学习 Java 编程的详细指导。**

 **## 为什么要学 Java？

在你知道如何学习 Java 之前，你要确信你为什么要学习它！

与其他语言相比，学习 Java 有很多优势。你可以在 Java 中执行任何任务，因为有丰富的库和插件。Java 在源代码和二进制级别上是独立于平台的，这意味着你编译的代码可以在任何地方使用。因为 Java 是面向对象的，所以代码被分割成独立的模块，使得代码可以重用并且没有 bug。

Java 有很多安全特性和跨平台能力。也是[数据科学和机器学习](https://hackr.io/blog/data-science-vs-machine-learning)的正确选择，当然是在 [Python 和 R](https://hackr.io/blog/r-vs-python) 之后。许多网站和 web 应用程序继续构建在 Java 平台上，因此对 Java 开发人员和设计人员的需求一直处于较高水平。

根据薪资表，开发人员的平均年薪范围是 47，169 美元到 106，610 美元。旧金山和阿灵顿支付给 Java 开发人员的薪水最高，平均每年约为 97000 美元。

由于它的许多优点和独特的特性，即使在 25 年前第一次发布之后，Java 仍然是最受欢迎的语言。通过学习 Java，你可以用核心 Java 编写代码，并朝着成为 JavaScript 专家、使用 J2EE 和相关 web 技术的 web 应用程序开发人员、首席架构师、设计师等方向前进。大多数安卓手机的操作系统都是用 Java 编写的，占全球智能手机市场的 88%。

如果你学习 Java，你也可以在更短的时间内更容易地学习任何其他基于 OOP 的编程语言。

### 先决条件

学习 Java，必须对计算机科学有一点了解。Java 可能是您首先要学习的编程语言，但是您应该首先熟悉以下计算机科学概念:

### OOP 概念

因为 Java 是一种面向对象的编程语言(OOP)，所以你需要了解多态、继承、抽象、封装和其他 OOP 概念。了解更多关于面向对象概念的信息。

### 数据结构和算法

数据结构是以特定格式组织、管理和存储的数据值的集合。它还定义了数据值之间的关系，以便可以轻松地操作这些值。

Java 使用许多集合对象以不同的方式组织和存储数据。例如，一个简单的列表可以存储一些整数，或学生的名字，或使用对象定义一个人的完整信息集:

```
List<String> myList = new ArrayList<String>();
myList.add("James");
myList.add("Shane");
myList.add("Abby");
System.out.println(myList);
```

这将给出[James，Shane，Abby]这样的输出。

类似的还有像[二分搜索法、](https://hackr.io/blog/binary-search-in-c)归并排序、冒泡排序等算法。，非常普遍，您应该熟悉它们，以了解 Java 集合的内部工作方式。

通过[最受欢迎的数据结构和算法教程](https://hackr.io/tutorials/learn-data-structures-algorithms)和课程进行学习。

### 如何设置环境

要在您的机器上安装 Java，请安装 JDK 或 Java 开发工具包和 JRE，即 Java 运行时引擎。您应该有安装两者所需的系统内存空间。JDK 和 JRE 都可以从甲骨文网站下载，适用于任何平台(Windows、macOS、Linux 等)。).按照屏幕上的说明进行安装很简单；这很简单。安装后，您必须在您的机器上设置环境变量(路径)。这个路径就是 JDK 和 JRE 的安装位置(很可能是 C:\Program Files)。

#### 集成开发环境

为了便于开发、构建和测试，最好使用 IDE 来更多地关注编码方面。IDE 帮助您遵循代码中的最佳实践，提示编译(有时是运行时)错误，给出建议，生成标准代码，添加注释，等等。使用 IDE 时，在工作区中导入和包含库也更容易。一些流行的 Java IDEs 有:

1.  Eclipse: Eclipse 是一个完整的 Java 和 J2EE 开发包。您可以添加任意多的库和插件，尽管它会占用空间，但 Eclipse 从来不会慢。[在这里下载 Eclipse】。您还可以调试代码、编写 Junit 测试、生成存根和 WSDLs，并轻松添加日志语句。Eclipse 很直观，您可以定制它的特性以适合您的项目。除了 Java，您可以使用简单的插件将 Eclipse 用作 Python IDE、C/C++ IDE 和 Scala。如果你不想要完整的功能，你也可以下载一个更简单的 Eclipse 版本，叫做](https://www.eclipse.org/downloads/packages/release/oxygen/3a/eclipse-ide-java-developers) [Easy Eclipse](http://www.easyeclipse.org/site/home/) 。
2.  NetBeans: NetBeans 提供了快速的 UI 开发、跨平台支持以及对 Java 技术的最佳支持。它也有强大的 HTML、JS 和 CSS 工具。NetBeans 速度很快，您甚至可以进行项目版本管理和基本的项目管理。NetBeans 还支持 C/C++、PHP 和 JSP。您可以重构您的代码，检查正确性，并验证最佳实践——下载 [Apache NetBeans](http://netbeans.apache.org/download/index.html) 。
3.  IntelliJ IDEA: IDEA 支持多种语言和框架，并集成了版本控制系统、剖析工具、数据库工具等。通过自动完成建议和动态编译，开发变得更快。它还为 Java 以外的语言提供了基于上下文的帮助，比如 SQL、HTML 和 JavaScript。你可以抛开所有重复繁琐的任务，专注于你的业务逻辑。工具建议很直观，帮助开发人员继续工作而不中断他们的流程——下载 [IntelliJ IDEA](https://www.jetbrains.com/idea/) 。

### 在线编译器

出于您自己的原因，如果您不想在您的系统上安装 IDE，您也可以使用在线编译器。与其他在线编译器相比，Tutorialspoint 提供了相对更快的在线 Java 编译器。

## 如何学习 Java

Java 很容易学，你不必花太多时间去学习概念。一旦你把基础打好，你就可以开始练习了。

如果您的系统上已经安装了 IDE，请尝试以下简单的程序:

1.  创建一个新项目，比如说，MyFirstJavaProj。
2.  创建一个名为 practice 的包。
3.  在这个包中，创建一个名为 MyFirstProgram.java 的类，并选中复选框来添加 main 方法:**public****static****void**main(String[]args)
4.  只需在 main 方法中添加以下代码:

System.out.println("欢迎来到 Java 世界！");

将该程序作为 Java 应用程序运行，消息将显示在控制台上。

不用担心程序中使用的所有关键字。关键是，让一个 Java 项目运行起来需要这么多步骤！要理解这些关键字和修饰语，请阅读这篇简短的 Java 简介，然后开始。您可以参加以下优秀课程，进一步丰富您的实践学习经验:

### Java 课程和教程(免费和付费)

Udemy 的这一付费畅销书课程教授核心 java 技能、JavaEE、Spring 框架、Android 开发等。本课程重点介绍 Java 8 和 11，并为您准备 Oracle Java 认证考试。它涵盖了 OOP 概念、集合、控制流语句、泛型、并发性、网络编程以及许多介绍性和中级 Java 主题。它价格合理，而且你不时会得到折扣。

这是一个大约 4-6 个月的专业化内容，涵盖了 Java OOP、数据结构和高级数据结构(如图形)、性能调优以及清除 Java 访问的技巧和机会。这是一门中级课程，有来自 Google 的真实项目和讲座。你可以选修该专业的全部或个别课程。Coursera 是按月订阅的，所以你可以选修任意数量的课程。

本课程涵盖了基本的 OOP 概念以及如何在 Java 中使用它们来开发 web 应用程序。你将在不同的层面上做很多实际的项目。这是一门入门课程，不需要任何先决条件。你将学习条件、控制流、数组、数组列表、字符串、继承等等。代码还包括调试异常、编译时和运行时错误。Codecademy 有免费和付费课程，这是一个免费的。

Pluralsight 提供了一系列不同级别的 Java 课程。每门课程约 3 小时。你可以从基础课程开始，即使用类和接口，然后开始中级课程，如 Java 设计模式、web 基础、持久性 API 等。订阅 Pluralsight，或者如果这是你的第一门课程，你可以免费试用。

#### 5.商务化人际关系网

LinkedIn 提供了很多学习 Java 的短期课程。像[学习 Java](https://www.linkedin.com/learning/learning-java-4/welcome-to-learning-java) 、[高级 Java 编程](https://www.linkedin.com/learning/advanced-java-programming-2)和[数据结构介绍&Java 中的算法](https://www.linkedin.com/learning/introduction-to-data-structures-algorithms-in-java)这样的热门课程是一些很好的开始课程。这三门课程涵盖了 Java 的基本概念和高级概念。LinkedIn 提供按月订阅选项，第一个月对学习者免费。

关于最佳 Java 课程 [的详细描述和信息，请访问这里](https://hackr.io/blog/best-java-courses)。

### Java 官方文档

要了解更多关于 Java 的 API 和各种实用方法，你应该经常查阅官方的 [API 文档页面](https://docs.oracle.com/javase/8/docs/api/)。您还将通过 API 了解继承结构、接口、抽象类、实用程序类和其他 OOP 风格。

## 项目

大多数教程还会通过项目进行实践。然而，在没有任何外部帮助的情况下做更多的项目会增强你的信心，提高你的专业水平。项目将帮助你尽快掌握 Java。

试试 Hackr.io. 为初学者提供的这 [10 个免费 Java 项目](https://hackr.io/blog/java-projects)

除了这些项目，你还可以自己尝试一些简单的项目，比如，

*   建立房屋租赁系统或汽车租赁系统，
*   刽子手游戏，
*   在线产品购买(将产品添加到购物车并结账)，
*   学生信息系统，
*   缺陷跟踪系统，
*   垃圾邮件过滤，
*   火车票预订系统，等等。

## 证书

所以，现在你已经通过教程学习完了 Java，也做了一些项目。你必须有足够的信心拿起证书，并把它们添加到你的简历中。证书会给你的简历增色不少，让你比其他有类似经历的候选人更有优势。查看 Java 开发者推荐的[顶级 Java 认证](https://hackr.io/blog/java-certification-courses)。

## Java 面试问题

现在，是时候把你所有的知识放在一起，为这个大日子做准备了。如果你对 Java 的实际问题和基于概念的问题了如指掌，那将是最好的。例如，评估者可能会要求您编写斐波那契数列的代码，或者询问您 Hashmap 的实现！了解垃圾收集，收集(LinkedList，Map，Tree 等。)、异常处理和线程等主题！这些是每个 Java 面试中都会被问到的重要问题。一些关键问题是:

查看 100 多个顶级 Java 面试问题的完整列表,这将帮助你解决最难的问题！

## 包扎

*   总而言之，我们已经涵盖了以下内容:要学习 Java，您必须熟悉一些编程概念，如数组、LinkedList、堆栈、队列、树、图等数据结构。基本算法，如二分搜索法、线性搜索、桶排序、快速排序等。
*   此外，您应该理解基本的 OOP 概念，如多态、封装、继承、抽象，它们构成了 Java 的基础。
*   对于 Java，离线或在线练习使用 IDE 总是更好。你不应该花太多时间阅读理论；相反，让自己尽快编写简单的程序。
*   从基本的编程概念开始，比如变量、数据类型、操作、条件、集合、循环、获取用户输入。然后更深入地了解文件处理、连接到数据库、处理异常、线程、泛型、垃圾收集、设计模式的概念，然后慢慢转向创建项目和 web 服务。
*   没有困难或不可能的任务。即使你以前没有编程经验，只要付出一点额外的努力，你也可以很快变得和专业开发人员一样优秀。
*   参加课程和认证，不断提高您的技能，让自己了解最新的版本和方法。

我们希望你喜欢阅读这本学习 Java 的指南，并且它敦促你一读完就开始编码。尝试一下，并让我们知道您的反馈。

**人也在读:****