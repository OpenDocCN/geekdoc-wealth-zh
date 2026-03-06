# 谷歌云 vs. AWS vs. Azure:云对比[更新]

> 原文：<https://hackr.io/blog/google-cloud-vs-aws-vs-azure>

云已经成为 IT 行业的主要市场之一。越来越多的企业和专业人士已经将他们的工作转移到了云上。他们为什么不应该？依靠云技术有很多优势。

通常，公共云服务用于:

*   IaaS(基础设施即服务)
*   平台即服务
*   SaaS(软件即服务)

根据 Gartner 调查报告，到 2021 年，公共云市场的总价值预计将达到 4110 多亿美元。云技术被用于备份、存储数据、合作办公等等。

目前，Amazon Web Services、Google Cloud 和 Microsoft Azure 是云技术的三巨头。哪个最好？嗯，没有明确的答案。

然而，这里有一个公共云计算中这三个最大的名字之间的比较，以帮助您为自己决定赢家。

## **谷歌云 vs. AWS vs. Azure:云主导权之战**

### **计算服务**

任何高效的云提供商都标榜自己有能力在短短几分钟内扩展数千个节点。Amazon 使用 EC2(弹性计算云)为用户提供计算服务，以便使用定制和预配置的 ami 来配置虚拟机。

除了虚拟机的总数、功率、内存容量和大小，用户还可以在各种可用的区域和分区中进行选择。此外，EC2 还支持自动伸缩和 ELB(负载平衡)特性。

前一个特性允许跨实例分布负载，而后一个特性支持虚拟机容量的自动扩展。Azure 提供 VHD(虚拟硬盘)来配置虚拟机，而谷歌提供 GCE(谷歌计算引擎)来做同样的事情。

VHD 可以由 Microsoft 或第三方预定义，也可以由用户定义。对于来自 Microsoft Azure 的每个虚拟机，用户还需要指定所需的内核数量和内存量。

像 AWS 一样，谷歌允许用户从可用区域中选择。GCE 于 2013 年推出，具有多种功能，如更快的持久磁盘、负载平衡、各种操作系统支持、实时迁移和额外的内核。

### **数据库**

亚马逊网络服务提供短暂的存储。一启动实例就分配它，当实例终止时销毁它。AWS 提供块存储，相当于硬盘，因此可以附加到任何实例或单独使用。

对于对象存储，AWS 提供 S3 服务，而 Glacier 则提供归档服务。AWS 完全支持 NoSQL 数据库、关系数据库和大数据。

微软 Azure 依赖于基于虚拟机的卷的 D 驱动器和页面 Blobs。前者是临时存储选项，后者是微软的块存储选项。

借助 Windows Azure Table 和 HDInsight，微软 Azure 为关系和 NoSQL 数据库以及大数据提供支持。

谷歌云平台还提供临时和永久磁盘存储。Google 云存储可用于对象存储。云提供商提供对大查询、大表和 Hadoop 的支持。

Google Cloud 通过 Google Cloud SQL 支持关系数据库，并通过 Google Cloud Nearline 提供无延迟的廉价归档。[标准化数据库](https://hackr.io/blog/dbms-normalization)被公共云计算的三巨头所使用。

除了提供云服务，云提供商还迎合开发工具的需求。这些工具有助于构建、调试、部署、诊断和管理多平台可扩展应用和服务，这些应用和服务旨在用作云服务。

Google Cloud 分别为应用测试和 Git 存储库提供了云测试实验室和云源代码存储库。然而，它不提供 DevOps、开发者工具和媒体转码，而这些是亚马逊 Web 服务和微软 Azure 提供的。

Amazon Web Services 附带了 Elastic Transcoder、Device Farm 和 CodeBuild，分别用于媒体代码转换、应用测试和开发运维。微软 Azure 为媒体转码提供媒体服务，为应用测试提供 DevTest Labs，为 DevOps 提供 Visual Studio Team Services。

### **管理和监控**

管理和监控是云计算非常重要的方面。三大云提供商都提供广泛的监控和管理服务。

在管理方面，AWS 有 3 个选项:

1.  应用程序发现服务
2.  个人健康仪表板
3.  系统经理

Microsoft Azure 在管理方面有 4 个选项，即:

### **日志分析**

*   运营管理套件
*   资源健康
*   存储浏览器

谷歌有用于管理的云控制台。三大云提供商都有计费 API。Cloudwatch、管理控制台和 X-Ray 是 AWS 的可用云顾问功能。Azure 拥有同样的应用洞察、监视器和门户。

Google 云平台的云顾问功能包括 CloudShell、调试器、错误报告、Stackdriver 监控和跟踪。

### **市场份额**

亚马逊网络服务独自拥有 62%的云市场份额。微软 Azure 拥有 20%的份额，而谷歌云拥有 12%的云市场份额。

除了谷歌云、微软 Azure 和谷歌云之外，其他云提供商仅拥有 6%的市场份额。因此，从市场份额来看，这些是最大的云服务提供商。

### **网络和内容交付**

不同的云服务提供商依赖不同类型的虚拟网络。虽然亚马逊网络服务依赖于虚拟专用云网络，但微软 Azure 在虚拟网络上工作。使用子网网络使谷歌云服务成为可能。

为了使最终用户能够将虚拟机分组到云中的隔离网络中，Amazon 和 Azure 分别利用 VPCs(虚拟私有云)和 VNET(虚拟网络)。

除了创建和定义路由表和网络网关之外，这些技术还允许创建子网和定义网络拓扑。AWS 提供独特的 Route 53，这是一种 DNS web 服务。

为了将内部数据中心扩展到公共或混合云中，AWS 和 Azure 都提供了许多解决方案。

谷歌计算引擎的每个实例都属于一个单独的网络。地址范围和网关地址取决于所选的网络。允许防火墙规则应用于实例并为其分配一个公共 IP 地址是可能的。

### **定价结构**

为了迎合用户的广泛需求，云服务的领导者提供了一个简单明了的定价结构。三大云服务都有一个定价模型。您不需要购买云解决方案，而是按需付费。

您需要支付给云服务提供商的费用取决于您将使用的服务数量。亚马逊网络服务根据使用的总小时数收费。AWS 提供三种类型的成本模型:

*   按需–无需前期成本，按需付费
*   保留—保留实例 1 年或 3 年，前期成本基于利用率
*   现货——客户为可用的额外容量付费

虽然 AWS 用户的最低收费时长是 1 小时，但谷歌云用户的最低收费时长是 10 分钟。与 AWS 不同，Google Cloud 为保留的实例提供了灵活的支付方案。

Microsoft Azure 用户根据总的使用分钟数付费。云提供商还提供短期承诺和折扣。

### **安全**

公共云计算服务的三大巨头都非常重视安全性。AWS 和微软 Azure 都依赖 Fortinet 来提供强大的安全功能。但是，这两家云提供商在使用相同技术时存在一些差异。

AWS 的 Fortinet 根据需求在几个可用性区域为亚马逊 VPC(虚拟私有云)提供安全措施。在微软 Azure 的情况下，Fortinet 为数据和应用程序提供了优化的安全性，同时消除了迁移期间所需的额外安全开销。

谷歌云依靠 FortiGate 下一代防火墙来实现高级安全和关键的防火墙保护。

### **存储**

亚马逊网络服务提供长期运行的存储服务。微软 Azure 和谷歌云提供的存储服务也是可靠和强大的。

对于对象存储服务，AWS 提供 S3(简单存储服务)，Azure 提供 Blob 存储，Google 提供云存储。AWS 提供 3 种类型的归档存储，即数据归档、冰川和 S3 非频繁访问。

Azure 和 Google 都提供两种类型的归档存储；Azure 的 Cool 和 Archive 以及 Google 的 Nearline 和 Coldine。混合存储方面，AWS 提供存储网关，Azure 自带 StorSimple，Google Cloud 有 Egnyte Sync。

[GCP 协理云工程师-谷歌云认证](https://click.linksynergy.com/link?id=jU79Zysihs4&offerid=1045023.3827154&type=2&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fgoogle-cloud-certification-associate-cloud-engineer%2F)

## 谷歌云 vs AWS vs Azure:面对面的比较

| **参数** | **谷歌云** | **AWS** | **蔚蓝色** |
| **由**提供 | 谷歌 | 亚马孙 | 微软 |
| **计算服务** | 应用引擎

*   码头集装箱登记处
*   即时群组
*   计算引擎
*   图形处理单元
*   Knative
*   库伯内特斯
*   功能
*   AWS 豆茎

 | 亚马逊 EC2

*   亚马逊 EC2 自动缩放
*   亚马逊弹性容器注册中心
*   亚马逊弹性库柏服务
*   亚马逊光帆
*   AWS 无服务器应用程序存储库
*   面向 AWS 的 VMware 云
*   AWS 批次
*   AWS Fargate
*   自动气象站λ
*   AWS 前哨站
*   弹性负载平衡
*   平台即服务(PaaS)
*   功能即服务(FaaS)

 | 服务结构

*   天蓝色批料
*   云服务
*   容器实例批处理
*   Azure 集装箱服务公司(AKS)
*   虚拟机计算引擎
*   虚拟机规模集
*   **数据库服务**
*   云 SQL
*   云大表

 |
| 云扳手 | 云数据存储

*   奥罗拉
*   无线电数据系统
*   DynamoDB
*   弹性缓存

 | 红移

*   海王星
*   数据库迁移服务
*   SQL 数据库
*   MySQL 数据库
*   PostgreSQL 数据库
*   数据仓库
*   服务器伸展数据库

 | 宇宙数据库

*   表格存储
*   重定向高速缓存
*   数据工厂
*   **缓存**
*   云 CDN
*   弹性缓存
*   重定向高速缓存
*   **存储服务**
*   云存储

 |
| 永久磁盘 | 转移用具 | 转接业务 | 简单存储服务(S3) |
| 弹性块存储 | 弹性文件系统(EFS)

*   存储网关
*   雪球
*   雪球边缘
*   雪地车

 | Blob 存储

*   队列存储
*   文件存储器
*   磁盘存储器
*   数据湖存储
*   **无服务器计算**
*   谷歌云功能
*   希腊字母的第 11 个

 | 无服务器应用程序存储库

*   功能
*   **文件存储**
*   ZFS 和阿威
*   electrical field stimulation 电场刺激
*   Azure 文件

 |
| **可用区域** | 73 | 77

*   60+
*   **DNS 服务**

 | 云 DNS |
| 亚马逊 53 号公路 | Azure 流量管理器 | **负载均衡** | 云负载平衡 |
| 弹性负载平衡 | Azure 的负载平衡 | **符合性** | 谷歌云平台安全 |
| AWS 云 HSM | Azure 信任中心 | **安全性** | 云安全指挥中心 |
| AWS 安全中心 | Azure 安全中心 | **定价** | 按秒付费 |
| 按分钟付费 | 按分钟付费 | **结论** | 任何其他云服务提供商都很难挑战三巨头中的任何一家，即亚马逊网络服务、谷歌云和微软 Azure。它们中的每一个都非常适合用作您企业的云主干。 |
| 这三家云提供商之间的主要区别是基于用户的偏好和特定要求。除此之外，三者在各方面几乎不相上下。 | **人也在读:** | AWS Security Hub | Azure Security Center |
| **Pricing** | Pay as per second | Pay as per minute | Pay as per minute |

## **Conclusion**

It is very difficult for any other cloud service provider to challenge any of the big three, namely Amazon Web Services, Google Cloud, and Microsoft Azure. Each of them is great for using as the cloud backbone of your enterprise.

The major distinction that lies between these three cloud providers is based on the user’s preference and specific requirements. Other than that, all three are almost equal in all respects.

**People are also Reading:**