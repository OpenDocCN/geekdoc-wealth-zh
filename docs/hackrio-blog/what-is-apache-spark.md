# 什么是阿帕奇火花？

> 原文：<https://hackr.io/blog/what-is-apache-spark>

目前，Apache Spark 是大规模批处理、机器学习、流处理和 SQL 操作的首选平台。自 2009 年发布以来，该平台在采用率和社区支持方面出现了大幅上升。

Apache Spark 由 1200 多名开发人员构建，由 300 多家组织贡献，由供应商中立的 Apache Software Foundation 托管，是大数据处理领域最大的社区之一。

## **什么是阿帕奇 Spark？**

Apache Spark 是一个统一的大数据分析引擎。它用 Scala 编写，是一个开源的分布式集群计算框架。Spark 提供了对整个集群(分布式计算机网络)进行编程的能力，具有隐式数据并行性和容错能力。

尽管 Apache Spark 作为一个独立的发行版免费提供，但对于那些对全面的企业管理服务感兴趣的人(通常遵循随用随付的方案)，它还提供了:

*   亚马逊 EMR(弹性 MapReduce)
*   谷歌云数据平台
*   MapR
*   微软 Azure HDInsight
*   来自 Databricks 的统一数据分析平台

分布式大数据处理框架能够对庞大规模的数据集执行快速处理任务。它将数据处理任务分布在各个集群上，或者自己完成，或者与上面提到的其他分布式计算工具一起完成。

Apache Spark 的这些品质不仅使它成为搅动大数据的理想工具，也是一个优秀的机器学习工具。组织通常使用 Apache Spark 来处理 Brobdingnagian 数据集，并得出有利可图的见解，以及构建可以做同样事情的健壮应用程序。

直观的 Spark API 抽象了大数据处理和分布式计算的复杂性，使开发人员可以根据自己的需求轻松使用分布式大数据处理框架，而不必担心过于深入其中的机制。

由于其通用性质，集群计算框架被不同细分市场的组织所采用。苹果、易贝、脸书、IBM、网飞和雅虎是利用 Apache Spark 的一些大公司。

所以，现在我们已经对 Apache Spark 有了一个简单的了解，是时候继续讨论 Apache Spark 架构了。

### Apache Spark 架构-什么和如何？

任何 Apache Spark 应用程序都由两个主要组件组成:

*   驱动程序——将用户代码转换成几个任务，这些任务分布在不同的工作节点上。
*   **Executor 进程**——运行在 worker 节点上，执行分配给它们的任务。

遵循分布式计算的原则，Apache Spark 依赖于一个驱动程序核心进程，该进程将一个应用程序分成几个任务，并在执行子任务的几个执行器进程之间分配这些任务。

这些执行器的一个令人惊奇的能力是，它们可以根据它们所属的应用程序的需求进行缩放。

为了使这两个组件(驱动程序和执行器)保持同步，也为了使整个过程保持高效，即以最佳方式分配工作节点，需要一个资源或集群管理系统。

默认情况下，Apache Spark 以独立集群模式运行。这要求集群中的每台机器都有 Apache Spark 框架和 JVM。然而，这只是一个基本的集群管理器，还有更好的选项可供选择。

这就是为什么在企业场景中，Hadoop YARN 被用作 Apache Spark 的集群管理系统的原因。然而，Spark 也可以在 Apache Mesos、Docker Swarm 和 Kubernetes 上运行。

Apache Spark 有一个 DAG(有向无环图)调度器。它是集群计算框架的调度层。Spark 将数据处理命令内置到 DAG 中。简而言之，它决定了任务和工作节点的内容和时间。

[面向 Java 开发人员的 Apache Spark】](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fapache-spark-for-java-developers%2F)

## **Apache Spark 生态系统**

Apache Spark 生态系统包括许多模块，我们将逐一讨论这些模块:

### **1。火花核心**

Apache Spark 中的一切都构建在 Spark 核心之上，Spark 核心是集群计算框架的底层执行引擎。它的特点是:

*   使用 Java、Python 和 Scala APIs 轻松开发
*   更快执行的内存计算能力，以及
*   通过通用的执行模型支持各种应用程序

大多数 Apache Spark 核心 API 都是基于 RDD(弹性分布式数据集)的概念构建的。虽然 Spark 内核简化了传统的 map 和 reduce 功能，但它还提供了对以下功能的内置支持:

*   聚合，
*   过滤，
*   连接数据集，以及
*   抽样

### **2。火花 SQL 和数据帧**

Spark SQL -以前称为 Shark - module，旨在用于结构化数据处理，充当分布式 SQL 查询引擎，并提供一个被称为 DataFrames 的编程抽象。

Spark SQL 允许未修改的 Hadoop Hive 查询在现有数据和部署上运行得更快。它还提供了与 Spark 生态系统其余部分的强大集成选项，例如将 SQL 查询处理与机器学习相集成。

这个结构化数据处理模块提供了对类似 SQL 2003 的接口的支持，使开发人员和分析人员同样可以使用它。Spark SQL 提供了开箱即用的标准接口，用于读取和写入:

*   阿帕奇蜂房
*   阿帕奇兽人
*   阿帕奇拼花地板
*   HDFS
*   JDBC
*   JSON

对其他流行数据存储的支持，如 Apache Cassandra、Apache HBase 和 [MongoDB](https://hackr.io/blog/what-is-mongodb-applications-advantages-examples) ，可以通过使用 Spark 包中不同的连接器来获得。一旦数据框注册为临时表，就可以在其上使用 SQL 查询。

在底层，Apache Spark 利用 Catalyst——一种查询优化器——负责检查数据和查询，为数据局部性和计算设计适当的查询计划，以便在整个集群中执行所需的计算。

**3。火花 RDDs**

RDDs 代表弹性分布式数据集。它是一种编程抽象，表示不可变的对象集合，分布在整个计算集群中。

这些允许实现快速和可伸缩的并行处理，使用跨集群分割 rdd 上的操作的能力，然后在并行批处理中执行它们。可以从一系列实体中创建 rdd，包括:

*   亚马逊 S3 桶
*   像 Apache Cassandra 和 MongoDB 这样的 NoSQL 数据存储
*   纯文本文件
*   SQL 数据库

**注意**:虽然 Spark 2 和更高版本仍然支持 RDD 接口，但是官方推荐使用 Spark SQL 模块。只有在 Spark SQL 模块无法满足项目的所有数据处理需求的情况下，您才应该使用 RDD 接口。

### **4。火花图 X**

Spark GraphX 是一个图形计算引擎，允许用户交互式地构建、管理和转换图形结构的数据。它具有一系列用于处理图形结构的分布式算法，甚至包括 Google PageRank 的实现。

GraphX 可用的算法利用了 Spark Core 的 RDD 数据建模方法。GraphFrames 包允许在数据帧上进行图形操作，同时受益于图形查询的催化剂。

### **5。火花流**

在 Apache Hadoop 的早期，批处理和流处理是两个独立的概念。对于批处理，需要编写 MapReduce 代码，而对于实时流，则需要使用 Apache Storm 之类的工具。

然而，现代应用不需要受限于分析和处理批量数据的能力。大多数甚至需要处理实时数据流。

经典 Hadoop 方法的一个主要缺点是不同的代码库需要保持同步。这是困难的，如果不是令人沮丧的话，因为技术所基于的框架、所需的资源、操作方法；一切都不同了。

为了解决这种看似矛盾的情况，Apache Spark 提供了 Spark 流模块。它遵循 Spark 的易用性和容错标准，同时为需要处理存储和实时数据的应用程序提供强大的接口。

### **6。微量配料**

Spark 流模块可以快速与一系列流行的数据源集成，如 Flume、HDFS、Kafka，甚至 Twitter。它将数据流分解成一系列连续的微批处理，之后可以使用 Spark API 对其进行操作。

这允许批处理和流形式的代码在相同的框架上运行时共享相同的代码。然而，微批处理被批评为在需要对传入数据进行低延迟响应的情况下速度很慢。

### **7。结构化流**

其他面向流的框架，如 Apache Apex 和 Apache Storm，由于使用了纯流方法，在上述场景中提供了更好的性能。这个问题通过使用结构化流解决了，这是 Apache Spark 2.x 版本中提供的一个特性。

高级 API 允许开发者创建无限的流数据帧和数据集。它还解决了几个紧迫的问题，如:

*   事件时间聚合，以及
*   邮件传递延迟

除了能够交互运行之外，对结构化流的每个查询都要经过 Catalyst。这允许对实时流数据执行 SQL 查询。

### **8。连续加工**

在 Apache Spark 2.3 之前，结构化流依赖于微批处理方案。Spark 2.3 中增加了连续处理，这是一种低延迟的处理模式。令人印象深刻的是，它允许处理延迟低至 1 毫秒的响应。

连续流模式支持一组有限的查询，在 Spark 2.4 中仍被标记为实验性的。

### **9。火花 MLib**

MLib 模块是 Apache Spark 生态系统中的一个可扩展的[机器学习库](https://hackr.io/blog/best-machine-learning-libraries)，允许使用快速、高质量的 ML 算法。它可以包含在完整的工作流中，因为该库可以在 Java、Python 和 Scala 编程语言中使用。

借助 Spark MLib，模块开发人员可以创建高效的机器学习管道。此外，他们可以轻松地在结构化数据集上实现特征提取、选择和转换。

MLib 的特点是聚类和分类算法的分布式实现，例如 k-means 聚类和随机森林。这些可以很容易地添加到定制的 ml 管道中或从中删除。

数据科学家可以利用 R 或 Python 在 Apache Spark 中训练机器学习模型，然后可以导入到 Java 或 Scala 管道中，几乎即时投入生产使用。

然而，MLib 只能用于基本的 ml 任务，即分类、聚类、过滤和回归。对于建模和训练深度神经网络，深度学习管道(仍在开发中)已经存在。

### 10。深度学习管道

Apache Spark 使用深度学习管道提供对深度学习的支持。这些利用了现有的 MLib 管道结构，用于:

*   将自定义 Keras 模型/张量流图应用于输入数据
*   调用构造分类器和低级深度学习库

深度学习管道甚至允许将深度学习模型应用于可用数据，作为 SQL 语句的一部分。它通过将 Keras 模型和/或张量流图注册为自定义 Spark SQL 用户定义函数(UDF)来实现这一点。

## **为什么是 Spark 而不是 Hadoop？**

Apache Spark 和 Apache Hadoop 都是姐妹技术，算是吧。虽然两者有一些相似之处，本质上都是大数据处理平台，但一些不同之处使它们成为不同的大数据处理技术。

有趣的是，Spark 包含在最近的许多 Apache Hadoop 发行版中。Hadoop 因其 MapReduce 范式而脱颖而出。然而，Apache Spark 有一个更好的替代方案。

在这个比较中，我们将基于两个主要参数来限制对两个 Apache 产品的比较；速度和开发者友好性。

### **1。速度**

Apache Spark 有一个内存数据引擎。这使得大数据处理框架能够更快地运行工作负载。在某些特定场景下，它可以比 [MapReduce 范式](https://en.wikipedia.org/wiki/MapReduce) (Apache Hadoop)快 100 倍。

例如，Spark 对于需要在不同阶段之间向磁盘写入状态的多阶段作业来说是高性能的。数据不能完全包含在内存中的 Apache Spark 作业仍然比使用 MapReduce 技术运行的作业快 10 倍左右。

MapReduce 处理技术仅限于包含数据映射和简化的两阶段执行图。另一方面，Spark 的 DAG(有向无环图)调度器具有多个阶段，能够更有效地分布。

### **2。开发者友好型**

Apache Spark 的构建考虑到了开发人员友好性。除了为流行的数据分析编程语言如 [R 和 Python](https://hackr.io/blog/r-vs-python) 提供绑定，集群计算框架还为通用编程语言如 Java 和 Scala 提供绑定。

由于其易用性，Apache Spark 提供的优势可以被任何人利用，从经验丰富的应用程序开发人员和专门的数据科学家到热情的学习者。使用 Apache Spark 可以用 Java、Python、R、Scala 和 SQL 快速编写应用程序。

集群计算框架包含 80 多个高级操作人员，有助于并行应用的开发。此外，Apache Spark 可以通过 Python、R、Scala 和 SQL shells 交互使用。

综上所述，Apache Hadoop 是一个老牌的大数据处理平台。同时，Apache Spark 是一个更高效的现代大数据处理平台，扩展了其前身 Hadoop 的功能。

想深入了解 Hadoop 和 Spark 的区别？查看这个详细的 [Hadoop 与 Spark](https://hackr.io/blog/hadoop-vs-spark) 对比。

## **总结**

Apache Spark 是目前最流行的分布式大数据处理框架。尽管它有一个复杂的底层架构，但它被抽象为提供一个更简单的工作时间的方式确实是一个非凡的壮举。

对于任何对大数据处理和分布式计算着迷的人来说，[学习 Spark](https://hackr.io/tutorials/learn-apache-spark?ref=blog-post) 无疑是有利的，而且是一个大大的肯定！

分布式集群计算框架与生俱来的用户友好性，加上巨大的、活跃的社区支持，使得理解和使用 Apache Spark 成为一项有益的、数字启发性的事业。所以，一切顺利！

你在准备 Apache Spark 的面试吗？查看这些[最佳 Apache Spark 面试问题](https://hackr.io/blog/apache-spark-interview-questions)。

**人也在读:**