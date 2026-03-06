# 2023 年 50 个最佳阿帕奇火花面试问答

> 原文：<https://hackr.io/blog/apache-spark-interview-questions>

Apache Spark 是最流行的分布式通用集群计算框架之一。该开源工具提供了一个接口，用于对具有隐式数据并行性和容错功能的整个计算机集群进行编程。

## 顶级 Apache Spark 面试问题和答案

在这里，我们整理了一份 Apache Spark 面试问题列表。这些将有助于你衡量你为即将到来的面试所做的准备。你认为你能得到正确的答案吗？嗯，你只有经历过才会知道！

#### **问题** : **你能解释一下 Apache Spark 的关键特性吗？**

**回答**:

*   **支持多种编程语言——**Spark 代码可以用四种编程语言中的任意一种编写，分别是 Java、Python、R 和 [Scala](https://hackr.io/tutorials/learn-scala?ref=blog-post) 。它还提供了这些编程语言的高级 API。此外，Apache Spark 提供了 Python 和 Scala 中的 shells。Python shell 是通过。/bin/pyspark 目录，而要访问 Scala shell，需要转到。bin/spark-shell 目录。
*   **惰性评估—**Apache Spark 利用了[惰性评估](https://wiki.haskell.org/Lazy_evaluation)的概念，即延迟评估，直到评估成为绝对必要的时候。
*   **机器学习—**对于大数据处理，Apache Spark 的 MLib 机器学习组件很有用。它消除了使用单独的引擎进行处理和机器学习的需要。
*   **多格式支持—**Apache Spark 支持多种数据源，包括 Cassandra、Hive、JSON 和 Parquet。数据源 API 提供了一种通过 Spark SQL 访问结构化数据的可插拔机制。这些数据源不仅仅是能够转换数据并将其导入 Spark 的简单管道。
*   **实时计算–**Spark 专为满足大规模可扩展性需求而设计。由于其内存计算，Spark 的计算是实时的，延迟更少。
*   **速度—**对于大规模数据处理，Spark 可以比 Hadoop MapReduce 快 100 倍。Apache Spark 能够通过控制分份来实现这一惊人的速度。分布式通用集群计算框架通过分区来管理数据，有助于以最小的网络流量并行处理分布式数据。
*   **Hadoop 集成–**Spark 提供与 Hadoop 的顺畅连接。除了作为 Hadoop MapReduce 功能的潜在替代品，Spark 还能够通过 YARN 在现有的 Hadoop 集群上运行，以进行资源调度。

#### **问题**:**Spark 相比 Hadoop MapReduce 有什么优势？**

**回答**:

*   **提高速度–**MapReduce 利用持久存储来执行任何数据处理任务。相反，Spark 使用内存处理，处理速度比 Hadoop MapReduce 快 10 到 100 倍。
*   **多任务处理–**Hadoop 仅支持通过内置库进行批处理。另一方面，Apache Spark 带有内置的库，用于从同一个核心执行多项任务，包括批处理、交互式 SQL 查询、机器学习和流式传输。
*   **无磁盘依赖性—**虽然 Hadoop MapReduce 高度依赖磁盘，但 Spark 主要使用缓存和内存数据存储。
*   **迭代计算—**对同一数据集进行多次计算称为迭代计算。Spark 能够进行迭代计算，而 Hadoop MapReduce 则不能。

#### **问题:** **请解释一下 RDD(Resilient Distributed Dataset)的概念。另外，说明如何在 Apache Spark 中创建 rdd。**

**答**:RDD 或弹性分布数据集是能够并行运行的操作元素的容错集合。RDD 中的任何分区数据都是分布式的和不可变的。

基本上，rdd 是存储在分布在许多节点上的内存中的数据部分。这些 rdd 在 Spark 中被延迟评估，这是 Apache Spark 获得更快速度的主要因素。rdd 有两种类型:

1.  **Hadoop 数据集—**对 HDFS (Hadoop 分布式文件系统)或其他类型的存储系统中的每个文件记录执行功能
2.  **并行集合–**现有的 rdd 彼此并行运行

在 Apache Spark 中创建 RDD 有两种方法:

*   通过在驱动程序中并行化一个集合。它利用了 SparkContext 的 parallelize()方法。例如:

```
method val DataArray = Array(22,24,46,81,101) val DataRDD = sc.parallelize(DataArray)
```

*   通过从一些外部存储器加载外部数据集，包括 HBase、HDFS 和共享文件系统

#### **问题**:**Spark Core 的各种功能是什么？**

**回答** : Spark Core 作为大规模并行、分布式数据处理的基础引擎。它是与 Java、Python 和 Scala APIs 结合使用的分布式执行引擎，为分布式 ETL(提取、转换、加载)应用程序开发提供了一个平台。

Spark Core 的各种功能包括:

1.  在群集上分发、监视和调度作业
2.  与存储系统交互
3.  内存管理和故障恢复

此外，在 Spark 核心之上构建的额外库允许它为机器学习、流和 SQL 查询处理提供多样化的工作负载。

#### **问题:** **请列举一下星火生态系统的各个组成部分。**

**回答**:

1.  GraphX–实现图形和图形并行计算
2.  MLib–用于机器学习
3.  Spark 核心——用于大规模并行和分布式数据处理的基础引擎
4.  Spark 流–负责处理实时流数据
5.  Spark SQL——将 Spark 的函数式编程 API 与关系处理相集成

#### **问题**:**Spark 中有没有实现图形的 API？**

**回答** : GraphX 是 Apache Spark 中用于实现图形和图形并行计算的 API。它用弹性分布式属性图扩展了 Spark RDD。它是一个有向多图，可以有几条平行的边。

弹性分布式属性图的每个边和顶点都具有与之相关联的用户定义的属性。平行边允许相同顶点之间的多种关系。

为了支持图形计算，GraphX 公开了一组基本操作符，如 joinVertices、mapReduceTriplets 和 subgraph，以及 Pregel API 的一个优化变体。

GraphX 组件还包括越来越多的图形算法和构建器，用于简化图形分析任务。

#### **问题** : **告诉我们你将如何在 Spark 中实现 SQL？**

**回答** : Spark SQL 模块有助于将关系处理与 Spark 的函数式编程 API 集成。它支持通过 SQL 或 HiveQL (Hive Query Language)查询数据。

此外，Spark SQL 支持大量的数据源，并允许用代码转换编织 SQL 查询。DataFrame API、数据源 API、解释器和优化器以及 SQL 服务是 Spark SQL 包含的四个库。

#### **问题:你对拼花文件的理解是什么？**

**答** : Parquet 是一种分栏格式，由多个数据处理系统支持。有了它，Spark SQL 既可以执行读操作，也可以执行写操作。采用列存储具有以下优势:

*   能够提取特定的列进行访问
*   消耗更少的空间
*   遵循特定于类型的编码
*   有限的 I/O 操作
*   提供更好的汇总数据

#### **问题** : **你能解释一下如何将 Apache Spark 与 Hadoop 结合使用吗？**

**回答**:兼容 Hadoop 是 Apache Spark 的主要优势之一。这对搭档组成了一个强大的技术组合。使用 Apache Spark 和 Hadoop 可以利用 Spark 无与伦比的处理能力，并与 Hadoop 的最佳 HDFS 和线程能力保持一致。

以下是在 Apache Spark 中使用 [Hadoop 组件](https://hackr.io/blog/hadoop-ecosystem-components)的方法:

*   批处理和实时处理——MapReduce 和 Spark 可以一起使用，前者负责批处理，后者负责实时处理
*   HDFS——Spark 能够在 HDFS 之上运行，以利用分布式复制存储
*   MapReduce——可以在同一个 Hadoop 集群中使用 Apache Spark 和 MapReduce，也可以单独作为一个处理框架使用
*   纱线——火花应用可以在纱线上运行

#### **问题** : **说出 Spark 中各种类型的集群管理器。**

**回答**:

1.  [Apache Mesos](https://en.wikipedia.org/wiki/Apache_Mesos)–常用的集群管理器
2.  独立–用于设置集群的基本集群管理器
3.  纱线-用于资源管理

#### **问题** : **可以使用 Apache Spark 来访问和分析存储在 Cassandra 数据库中的数据吗？**

**答**:是的，通过 Spark Cassandra 连接器，可以使用 Apache Spark 访问和分析存储在 [Cassandra](https://hackr.io/tutorials/learn-cassandra?ref=blog-post) 数据库中的数据。它需要被添加到 Spark 项目中，在此期间，Spark 执行器与本地 Cassandra 节点对话，并将只查询本地数据。

通过连接 Cassandra 和 Apache Spark，可以减少 Spark 执行器和 Cassandra 节点之间发送数据的网络使用，从而加快查询速度。

#### **问题** : **你说的工作者节点是什么意思？**

**回答**:任何能够在集群中运行代码的节点都可以说是工作者节点。驱动程序需要监听传入的连接，然后从它的执行器接受相同的连接。此外，驱动程序必须可以从工作节点通过网络寻址。

工作节点基本上是一个从节点。主节点分配工作，然后由工作节点执行。工作节点处理存储在节点上的数据，并向主节点报告资源。主节点基于资源可用性来调度任务。

#### **问题** : **请解释一下 Spark 中的稀疏向量。**

**回答**:稀疏向量用于存储非零条目，以节省空间。它有两个平行阵列:

1.  一个用于索引
2.  另一个是价值观

稀疏向量的一个示例如下:

Vectors.sparse(7，Array(0，1，2，3，4，5，6)，Array(1650d，50000d，800d，3.0，3.0，2009，95054))

#### **问题** : **你将如何连接 Apache Spark 和 Apache Mesos？**

**答**:连接 Apache Spark 和 Apache Mesos 的步骤如下:

1.  配置 Spark 驱动程序以连接 Apache Mesos
2.  将 Spark 二进制包放在 Mesos 可以访问的位置
3.  将 Apache Spark 安装在与 Apache Mesos 相同的位置
4.  配置 spark.mesos.executor.home 属性以指向 Apache Spark 的安装位置

#### **问题** : **你能解释一下在使用 Spark 时如何将数据传输减到最少吗？**

**回答**:最小化数据传输以及避免混乱有助于编写能够可靠快速运行的 Spark 程序。使用 Apache Spark 时，减少数据传输的几种方法是:

*   避免——通过按键操作、重新分区和其他负责触发洗牌的操作
*   使用累加器——累加器提供了一种在并行执行变量值的同时更新变量值的方法
*   使用广播变量——广播变量有助于提高小型和大型 rdd 之间的连接效率

#### **问题**:**Apache Spark 中的广播变量是什么？我们为什么需要它们？**

**回答**:广播变量有助于在每台机器上保存变量的只读缓存版本，而不是随任务一起发送变量的副本。

广播变量还用于为每个节点提供大型输入数据集的副本。Apache Spark 试图通过使用有效的广播算法来分配广播变量，以降低通信成本。

使用广播变量消除了为每个任务发送变量副本的需要。因此，可以快速处理数据。与 RDD 查找()相比，广播变量有助于在内存中存储查找表，从而提高检索效率。

#### **问题** : **请对 Spark 中的 DStream 进行解释。**

**答** : DStream 是离散化流的缩写。这是 Spark Streaming 提供的基本抽象，是一个连续的数据流。从通过转换输入流而产生的处理过的数据流或者直接从数据源接收数据流。

数据流由一系列连续的 RDD 表示，其中每个 RDD 包含来自某个间隔的数据。应用于数据流的操作类似于在底层 rdd 上应用相同的操作。数据流有两个操作:

1.  负责将数据写入外部系统的输出操作
2.  产生新数据流的变换

可以从各种来源创建数据流，包括 Apache Kafka、Apache Flume 和 HDFS。此外，Spark Streaming 还支持多种数据流转换。

#### **问题**:**Apache Spark 提供检查点吗？**

**回答**:是的，Apache Spark 提供了检查点。它们允许一个程序 24 小时不间断地运行，并使它对与应用程序逻辑无关的故障具有弹性。谱系图用于从故障中恢复 rdd。

Apache Spark 附带了一个用于添加和管理检查点的 API。然后，用户决定将哪些数据发送到检查点。当世系图较长且具有更广泛的依赖性时，检查点比世系图更受青睐。

#### **问题**:**Spark 有哪些不同层次的坚持？**

**回答:**虽然来自不同混洗操作的中间数据会自动持久化在 Spark 中，但是如果要重用数据，建议在 RDD 上使用 persist()方法。

Apache Spark 具有几个持久性级别，用于将 rdd 存储在磁盘、内存或两者的组合上，并具有不同的复制级别。这些不同的持久性级别是:

*   DISK_ONLY -仅在磁盘上存储 RDD 分区。
*   MEMORY _ AND _ DISK——将 RDD 作为反序列化的 Java 对象存储在 JVM 中。如果内存中容纳不下 RDD，磁盘上会存储额外的分区。每次出现需求时，都会从这里读取这些内容。
*   MEMORY _ ONLY _ SER——将 RDD 存储为序列化的 Java 对象，每个分区有一个字节的数组。
*   MEMORY _ AND _ DISK _ SER——与 MEMORY_ONLY_SER 相同，不同之处在于，它将内存中无法容纳的分区存储到磁盘中，而不是在需要时动态地重新计算它们。
*   MEMORY _ ONLY——默认级别，它将 RDD 作为反序列化的 Java 对象存储在 JVM 中。如果 RDD 不适合可用的内存，一些分区将不会被缓存，导致每次需要它们时都要重新计算。
*   OFF_HEAP -工作方式类似 MEMORY_ONLY_SER，但是将数据存储在堆外内存中。

#### **问题** : **你能列出使用 Apache Spark 的限制吗？**

**回答**:

*   它没有内置的文件管理系统。因此，它需要与 Hadoop 等其他平台集成，以便从文件管理系统中获益
*   延迟更高，但因此吞吐量更低
*   不支持真正的实时数据流处理。在 Apache Spark 中，实时数据流被划分成批，处理后再转换成批。因此，Spark 流是微批量处理，而不是真正的实时数据处理
*   可用的算法数量较少
*   Spark 流不支持基于记录的窗口标准
*   这项工作需要分布在多个集群上，而不是在单个节点上运行所有内容
*   当使用 Apache Spark 进行经济高效的大数据处理时，其“内存”能力成为一个瓶颈

#### **问题:定义 Apache Spark？**

**答:** Apache Spark 是一个易于使用、高度灵活且快速的处理框架，它拥有一个支持循环数据流和内存计算过程的高级引擎。它可以在云和 Hadoop 中独立运行，提供对卡珊德拉、HDFS、HBase 等各种数据源的访问。

#### **问题:火花发动机的主要用途是什么？**

**答:**Spark 引擎的主要用途是随集群一起调度、监控、分发数据应用。

#### **问题:在 Apache Spark 中定义分区？**

**答:**Apache Spark 中的分区旨在通过对数据进行更小、更相关、更符合逻辑的划分来拆分 MapReduce 中的数据。这是一个有助于导出数据逻辑单元的过程，以便快速处理数据。Apache Spark 在弹性分布数据集(RDD)中进行分区。

#### 问:RDD 的主要业务是什么？

**答案:**RDD 主要有两个操作，其中包括:

1.  转换
2.  动作

#### 问题:在 Spark 中定义转换？

**答:** 变换是应用于 RDD 的函数，有助于创造另一个 RDD。直到行动发生，转变才会发生。转换的例子有 Map()和 filer()。

#### **问题:Map()的作用是什么？**

**答:**Map()的作用是在 RDD 的每一条线上重复，之后，把它们分割成新的 RDD。

#### **问题:filer()的作用是什么？**

**答案:**filer()的作用是从已有的 RDD 中选取各种元素，开发出一个新的 RDD，它通过函数自变量。

#### **问题:Spark 中有哪些动作？**

**答:**Spark 中的动作有助于将数据从 RDD 带回本地机器。它包括给出非 RDD 值的各种 RDD 运算。Sparks 中的操作包括 reduce()和 take()等函数。

#### **问题:reducing()和 take()函数有什么区别？**

**答:** Reduce()函数是一个反复应用直到最后剩下一个值的动作，而 take()函数是一个考虑了从一个 RDD 到局部节点的所有值的动作。

#### **问题:Map Reduce 中 coalesce()和 repartition()的异同？**

**答案:** 相似之处在于 Map Reduce 中的 Coalesce()和 Repartition()都是用来修改一个 RDD 中的分区数量的。它们之间的区别在于 Coalesce()是 repartition()的一部分，re partition()使用 Coalesce()进行洗牌。这有助于 repartition()产生特定数量的分区，所有数据都由各种散列实践者的应用程序分发。

#### **问题:在 Spark 中定义纱线？**

**答:**Spark 中的 YARN 充当中央资源管理平台，帮助在整个集群中交付可扩展的操作，并执行分布式容器管理器的功能。

**答案:**Spark 中的 PageRank 是 Graphix 中的一种算法，它测量图中的每个顶点。例如，如果一个人在脸书、Instagram 或任何其他社交媒体平台上拥有大量粉丝，那么他/她的页面就会排名靠前。

#### **问题:Spark 中的滑动窗口是什么？举个例子？**

**答:**Spark 中的滑动窗口用于指定每一批要处理的 Spark 流。例如，您可以专门设置想要通过 Spark streaming 处理的批次间隔和几个批次。

#### **问题:滑动窗口操作有什么好处？**

**答案:** 滑动窗口操作有以下好处:

*   它有助于控制不同计算机网络之间的数据包传输。
*   它组合落在特定窗口内的 rdd，并对其进行操作，以创建窗口数据流的新 rdd。
*   它使用 Spark 流库提供窗口计算来支持 rdd 的转换过程。

#### 问:如何定义 RDD 血统？

**答案:** RDD 血统是一个重建丢失数据分区的过程，因为 Spark 无法支持其内存中的数据复制过程。它有助于回忆用于构建其他数据集的方法。

#### **问题:什么是火花驱动器？**

**答:** Spark Driver 是指在机器主节点上运行的程序，帮助声明数据 rdd 上的转换和动作。它有助于创建与给定 Spark Master 连接的 SparkContext，并在只有集群管理器运行的情况下向 Master 提供 RDD 图。

#### **问题:Spark 支持哪些类型的文件系统？**

**答案:** Spark 支持三种文件系统，包括以下几种:

*   亚马逊 S3
*   Hadoop 分布式文件系统(HDFS)
*   本地文件系统。

#### **问题:定义 Spark 执行器？**

**回答:** Spark Executor 支持 SparkContext 通过集群中的节点与集群管理器连接。它在工作节点上运行计算和数据存储过程。

#### 问题:我们可以在 Apache Mesos 上运行 Apache Spark 吗？

**回答:** 是的，我们可以通过使用由 Mesos 管理的硬件集群在 Apache Mesos 上运行 Apache Spark。

#### 问题:我们能在 Spark 中触发自动清理吗？

**回答:** 是的，我们可以在 Spark 中触发自动清理来处理累积的元数据。可以通过设置参数来完成，即“spark . cleaner . TTL”。

#### **问题:除了“Spark.cleaner.ttl”之外，在 Spark 中触发自动清理的另一种方法是什么？**

**答案:** 在 Spark 中，除了“Spark.clener.ttl”之外的另一种触发自动化清理的方法是，将长时间运行的作业分成不同的批次，并将中间结果写入磁盘。

#### **问题:Akka 在 Spark 中的作用是什么？**

**答案:** Akka 在 Spark 中帮助调度流程。它帮助工作进程和主进程发送和接收工作进程的任务消息和主进程的注册请求。

#### **问题:在 Apache Spark RDD 中定义 SchemaRDD？**

**答:** SchemmaRDD 是一个 RDD，它携带各种行对象，比如基本字符串或整数数组的包装器，以及关于每列中数据类型的模式信息。现在它被重命名为 DataFrame API。

#### **问题:为什么要设计 SchemaRDD？**

**答案:** SchemaRDD 的设计是为了让开发人员更容易在 SparkSQL 核心模块上进行代码调试和单元测试。

#### **问题:Spark SQL、HQL 和 SQL 的基本区别是什么？**

**答案:** Spark SQL 支持 SQL 和 Hiver 查询语言，不改变任何语法。我们可以用 Spark SQL 连接 SQL 和 HQL 表。

## 结论

这就完成了 50 个顶级 Spark 面试问题的列表。通过这些问题，您可以检查自己的 Spark 知识，并为即将到来的 Apache Spark 面试做好准备。

为了在 Apache Spark 面试中表现更好，你可能需要查看一下这个 best udemy 课程: [Apache Hadoop 面试问题准备课程](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https://www.udemy.com/course/apache-hadoop-interview-questions-preparation-course/)。

如果你在找一本适合 Apache 面试问题的书，那就买这本很棒的书: [99 Apache Spark 面试问题专业人士:Apache Spark 面试问题准备指南](https://geni.us/JNQ79kg)。

上述问题中有多少你已经知道答案了？哪些问题应该或不应该出现在列表中？请通过评论让我们知道！考虑查看这些[最佳 Spark 教程](https://hackr.io/tutorials/learn-apache-spark?ref=blog-post)来进一步完善您的 Apache Spark 技能。

万事如意！

**人也在读:**