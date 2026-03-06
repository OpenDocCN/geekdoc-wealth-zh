# AngelList 市场之旅，第 2 部分:细节

> 原文：<https://web.archive.org/web/venturehacks.com/markets-details>

#### [Nivi](/web/20221208085959/https://venturehacks.com/about)2011 年 1 月 31 日

参见[第 1 部分](/web/20221208085959/https://venturehacks.com/articles/angellist-markets)了解 AngelList 上的新市场功能介绍。这部分讲的都是细节。

### 创造新市场

我们鼓励人们使用[现有市场](https://web.archive.org/web/20221208085959/http://angel.co/markets)，但任何人都可以创建新市场:

![](img/5bc1e867d11c502d46cb6c151e3e46c1.png)

### 管理员组织新的市场

管理员定期审查新的市场，删除、重命名、别名或合并(我们直接从 Quora(Quora)那里偷来的)。只有管理员有这些权力，只有管理员可以设置市场的父市场和子市场。例如，在 http://angel.co/internet的侧栏中可以看到互联网的父母和孩子:

![](img/d6314cc9a90467794653ff1bec95779b.png)

…你可以在 http://angel.co/internet/tree 看到完整的互联网树。

### 试图让它“正常工作”

我不认为我们可以列出 20 个规范市场，然后就此收工。相信我，我们试过了——事情会简单得多。点击这里查看丰富的市场——20 个精心挑选的市场不能公平对待投资者和创业公司的不同利益。

追逐新市场也是风险资本的本性，无论是像[移动](https://web.archive.org/web/20221208085959/http://angel.co/mobile)这样广阔的新市场，还是像[基于位置的服务](https://web.archive.org/web/20221208085959/http://angel.co/location-based-services)这样特定的市场。一套静态的市场违背了这个目的。

因此，我们让任何人创造一个新的市场，我们使用技巧来防止事情失去控制。我已经写过管理员如何组织市场。接下来，我们隐藏追随者少于 10 人的市场:

![](img/e833a3956a998b46ffc5089640222e9d.png)

第三，我们用颜色来表示跟踪一个市场也隐含地跟踪它的子市场。例如，我刚刚关注了 [Mobile](https://web.archive.org/web/20221208085959/http://angel.co/mobile) ，它的所有子代都变成了绿色:

![](img/d0856f8e4770c33577d19459f5be202a.png)

如果我将鼠标悬停在 Mobile 的一个孩子身上，我会看到这样的消息:

![](img/27061a9000b1991b8d9a71a842498956.png)

因此，如果你已经在关注[移动](https://web.archive.org/web/20221208085959/http://angel.co/mobile)，你不需要关注[移动商务](https://web.archive.org/web/20221208085959/http://angel.co/mobile-commerce)。但如果投资者想向初创公司表明他们对移动商务特别感兴趣，他们可以通过“关注”链接将移动商务添加到他们的个人资料中。

### 从技术上讲，市场不是一棵树

尽管我说市场像你的桌面文件系统一样组织成一棵树，但从技术上来说这是不正确的。它们实际上是一个[有向无环图](https://web.archive.org/web/20221208085959/http://www.quora.com/Are-Quora-topic-hierarchies-a-directed-acyclic-graph) (DAG)。DAG 和树的主要区别在于，一个市场可以有多个父市场。这就好像你桌面上的一个文件可以同时存在于两个文件夹中。

比如[游戏](https://web.archive.org/web/20221208085959/http://angel.co/games)有两个父母:[信息技术](https://web.archive.org/web/20221208085959/http://angel.co/information-technology)和[消费者](https://web.archive.org/web/20221208085959/http://angel.co/consumers)。你可以在[http://angel.co/games/tree](https://web.archive.org/web/20221208085959/http://angel.co/games/tree)看到游戏树:

![](img/8b493eb99d06cbab33be6aef9a08f2c6.png)

将市场构建成一个 DAG 是我从 Quora 偷来的另一个想法。用一棵真实的树来实现市场是非常困难的——我们必须将每个市场放在*的一个父市场中。你会把[游戏](https://web.archive.org/web/20221208085959/http://angel.co/games)或[移动企业](https://web.archive.org/web/20221208085959/http://angel.co/mobile-enterprise)或[数字媒体](https://web.archive.org/web/20221208085959/http://angel.co/digital-media)放在哪里？多个父母减轻了组织市场的负担。*

(疯狂的人可以了解更多不同的分类系统，如 DAGs、tags 和 tree[这里](https://web.archive.org/web/20221208085959/http://www.quora.com/What-are-the-different-types-of-classification-structures/answer/Robin-Green))。

### 世界上最准确的市场名称集？

过去，当投资者向 AngelList 申请时，我们有一个文本框，要求投资者列出他们感兴趣的市场，以及他们不感兴趣的市场。我们从这个文本中提取了最初的市场名称集。然后我们自动让那些投资者跟随并封锁那些市场。最后，我们用一个漂亮的自动完成表单替换了文本框:

![](img/9097214ccf0e20822ed58f9cf58ee481.png)

我认为我们现在拥有世界上最准确的风险资本市场名称。首先，最初的市场是投资者自我报告的，所以他们想出了自己的市场名称。第二，直到最近才出现自动完成功能，所以每个投资者独立命名他们的市场，而不看其他投资者在做什么。

换句话说，投资者独立地为市场名称投票，而不受其他投资者如何命名市场的影响——这是明智群体的重要组成部分。