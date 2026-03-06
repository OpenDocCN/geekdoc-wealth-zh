# Hadoop MapReduce 和 Apache Spark 的区别

> 原文：<https://hackr.io/blog/hadoop-mapreduce-vs-apache-spark>

**因素** **Hadoop MapReduce** **阿帕奇火花** **核心定义** MapReduce is a programming model that is implemented in processing huge amounts of data.
MapReduce has been developed using Java
MapReduce Programs work in two phases:

*   地图阶段
*   还原阶段

整个 MapReduce 过程经历以下 4 个阶段:

*   **分割**:输入被分割成固定大小的分割，称为 input-splits。输入拆分由单个地图消耗。

*   **映射**:这里，每个映射中的数据被传递到一个映射函数中，以产生输出值。

*   **混排**:该阶段消耗映射阶段的输出，相关记录合并。

*   **Reducing** :在这个阶段，相关记录被聚合，返回一个输出值。这个阶段总结了完整的数据集。

Apache Spark 是一个用于大数据的开源分布式处理系统。Spark 是大规模数据处理的引擎。Spark 是使用 Scala 开发的。
Apache Spark 的主要组件如下:

*   Apache Spark Core :它是底层的通用执行引擎，所有其他功能都建立在它之上。它在外部存储系统中提供内存计算和数据集引用。

*   **Spark SQL** :它是提供关于数据结构和正在执行的计算的信息的模块

*   **火花流**:允许处理实时数据。然后，使用复杂的算法处理这些数据，并将其推送到文件系统、数据库和实时系统中。

*   **MLlib【机器学习】**:它是一个库，包含了大量的机器学习算法和工具，用于构建、评估和调优 ML 管道。

*   GraphX :它附带了一个库来操作图形数据库和执行计算。它将 ETL 过程、探索过程和迭代图计算统一在一个系统中。

**加工速度** MapReduce 从磁盘读取和写入数据。虽然它比传统系统快，但比 Spark 慢得多。 它在 RAM 上运行，将中间数据存储在内存中，减少了对磁盘的读/写周期数。因此，它比传统的 MapReduce 更快。 **数据处理** MapReduce was designed to perform Batch Processing for a voluminous amount of data. Hence, for extended data processing, it is dependent on different engines like Storm, Giraph, Impala, etc. Managing many different components adds to the hassle.

MapReduce 无法交互处理数据

在同一个集群中执行批处理、实时处理、迭代处理、图形处理、机器学习和流式处理。因此，它是一个完整的数据分析引擎，足以处理所有需求。Spark 具有高效处理实时流的能力。
Spark 可以交互处理数据。 **内存使用量** 不支持数据缓存。 通过在内存中缓存数据来提高系统性能。 **编码** MapReduce 需要处理低级 API，因此开发人员需要对每个操作进行编码，这使得操作非常困难。 Spark 易于使用，其弹性分布式数据集有助于使用高级操作符处理数据。它提供了丰富的 Java、Scala、Python 和 r 的 API。

**等待时间**

潜伏意味着延迟。这是 CPU 向 RAM 发出请求后等待响应的时间。

MapReduce 有一个高延迟的计算框架。 Spark 提供了低延迟计算。 **从故障中恢复** MapReduce 具有高度容错能力，能够应对系统故障和失败。在这种情况下，如果出现故障，不需要从头重新启动应用程序。 Spark 也是容错的。弹性分布式数据集[RDDs]允许在故障节点上恢复分区。它还支持通过检查点进行恢复，以减少对 RDD 的依赖性。因此，在失败的情况下，这里也不需要从头开始重新启动应用程序。 **调度器** MapReduce 依赖像 Oozie 这样的外部作业调度器来调度其复杂的流程。 由于内存中的计算，Spark 的行为就像它自己的流调度程序。 **安全** 由于 Kerberos 的存在，MapReduce 相对更安全。它还支持访问控制列表(ACL ),这是传统的文件权限模型。 Spark 只支持一种认证，即共享密码认证。 **成本** 就成本而言，MapReduce 是一个更便宜的选择。 Spark 的成本更高，因为它需要内存处理能力和 RAM。 **功能** MapReduce 是一个数据处理引擎。 Spark 是一个数据分析引擎，因此是数据科学家的选择。 **框架** 它是一个开源框架，用于将数据写入 HDFS，并处理 HDFS 的结构化和非结构化数据。 Spark 是一个独立的实时处理引擎，可以安装在任何分布式文件系统中。 **支持的编程语言** Java，C，C++，Ruby，Groovy，Perl，Python Scala，Java，Python，R，SQL **SQL 支持** 使用 Apache Hive 运行 SQL 查询 使用 Spark SQL 运行 [SQL 查询](https://hackr.io/blog/sql-commands) **硬件要求** MapReduce 可以在商用硬件上运行。 Apache Spark 需要中高级硬件配置才能高效运行。   Hadoop 需要一个机器学习工具，其中一个就是 Apache Mahout。 Spark 有自己的一套[机器学习](https://hackr.io/blog/what-is-machine-learning-definition-types)即 MLlib。 **冗余检查** MapReduce 不支持此功能。 Spark 对每条记录只处理一次，因此消除了重复。