# 什么是 MongoDB？简介、应用、优势和示例

> 原文：<https://hackr.io/blog/what-is-mongodb-applications-advantages-examples>

## 什么是 MongoDB？概述和历史

MongoDB 是一个强大的、高度可伸缩的、基于 NoSQL 的免费开源数据库。MongoDB 最初是在大约 9 年前的 2009 年 2 月 11 日发布的，从那时起，它已经成为领先的 NoSQL 数据库。公司 [MongoDB Inc.](https://www.mongodb.com) (美国纽约)维护和管理 MongoDB 的开发。他们还提供了 MongoDB 的商业版本，其中也包括支持。在 Github 上可以找到 MongoDB 的源代码。

多年来，MongoDB 已经成为一个高度可伸缩的数据库的流行选择，它目前被用作许多知名组织的后端数据存储，如 IBM、Twitter、Zendesk、Forbes、脸书、Google 和其他许多组织。MongoDB 也吸引了开源社区的目光，许多开发人员都在从事各种基于 MongoDB 的开源项目。你可以在这里下载 MongoDB [，在这里](https://www.mongodb.com/download-center)找到 MongoDB 文档[。](https://docs.mongodb.com/)

## MongoDB 的应用

MongoDB 作为主数据存储被广泛用于各种 web 应用程序。最流行的 web 开发栈之一，MEAN 栈采用 MongoDB 作为数据存储(MEAN 代表 MongoDB、ExpressJS、AngularJS 和 NodeJS)。

## 什么时候如何使用 MongoDB？

MongoDB 是一个基于文档的数据存储，这意味着它以一种非结构化的格式存储信息，而不是像 MySQL 或 PostgreSQL 那样的结构化表。这实质上意味着存储在 MongoDB 中的数据是“无模式的”。因此，MongoDB 提供了快速和可伸缩的数据存储服务，这使得它成为性能关键型应用程序的热门选择。此外，MongoDB 是用 C++编写的，这使得它比许多其他数据库更快。

MongoDB 不应该用在需要表连接的应用程序中，因为它不支持连接(比如在 SQL 中)。这是因为存储在 MongoDB 中的数据不是结构化的，因此，执行连接是一个非常耗时的过程，可能会导致性能下降。

让我们考虑一个学生模型的简单例子，其中学生可以选修各种大学课程。下面是一个简单的基于 MongoDB 的学生模型的样子:

使用 MongoDB 的优势

## 从上面的例子中可以看出，在 MongoDB 中，我们不是像在 SQL 中那样将学生和课程存储在单独的数据库表中，而是将它们一起存储在一个“文档”中。这加快了数据检索过程。大多数大规模应用程序(如脸书)都需要这种微小的性能提升，因为有数十亿用户在使用该应用程序，因此，即使是微小的性能提升也可能产生巨大的整体影响。这是使用 MongoDB 最重要的优势之一。

其他优势包括:

**集群化:** MongoDB 允许跨集群中的节点进行数据分片，以确保数据库服务器中没有单点故障。

*   对二级索引的支持: MongoDB 不仅支持一级索引，还支持二级索引，这在许多应用程序中都很重要。
*   **缓存:** MongoDB 缓存大量数据，以便更快地检索查询结果。
*   **伟大的特性集**:MongoDB 上有各种各样的特性(即席查询、索引、复制、负载平衡、文件存储、聚合、服务器端 JavaScript 执行、封顶集合等。)这使它成为一个非常用户友好的数据库。
*   什么时候不用 MongoDB？

## MongoDB 是一个 NoSQL 数据库，因此它不是 ACID 兼容的(原子性、一致性、隔离性、持久性)。因此，在要求遵守 ACID 的应用程序中(例如，要求数据库级事务的应用程序)，不能使用 MongoDB。例如，在为银行设计核心银行系统时，可能不希望使用 MongoDB。

此外，与许多数据库不同，MongoDB 不提供存储过程。

MongoDB 性能

## 数据库的确切性能因许多因素而异。例如:

**用例:**一些应用程序要求数据结构化。在这种情况下，最好使用基于 SQL 的数据库。在其他应用程序中，组织数据几乎是不可能的。MongoDB 在这里效果最好。

*   **存储:**自然，性能(每秒读写次数)将在很大程度上取决于底层存储机制。例如，固态硬盘肯定比普通硬盘更快，因此，固态硬盘的性能更好。
*   **RAM:** 数据库性能在很大程度上取决于缓存，可以缓存的信息量取决于数据库可用的 RAM。
*   **集群化:** MongoDB 可以用来轻松搭建一个高可用性、高性能的数据库集群。这在基于 SQL 的数据库中通常是困难的。
*   MongoDB 在要求数据非结构化的应用程序中表现出色。例如，各种 MapReduce 应用程序、大数据系统、社交网络应用程序、新闻论坛等。在这种用例中，跨表组织数据是很困难的。即使可以跨表构建数据，也不总是可取的，因为在需要数据库连接的查询中，会对数据库的性能产生巨大影响。

[MongoDB-2023 年完整开发者指南](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fmongodb-the-complete-developers-guide%2F)

如何学习使用 MongoDB？

## 学习 MongoDB 的最好方法是实际开发一个使用 MongoDB 作为后端数据库的 web 应用程序。数据库通常与 web 应用程序结合使用(而不是独立使用)，因此建议您尝试以下简单的 web 应用程序思想:

一个社交网站，用户可以分享帖子，喜欢彼此的帖子，并对彼此的帖子发表评论。

*   基于问答的论坛，支持多个主题。
*   您可以使用自己选择的任何 web 应用程序框架。一些推荐的方法是:

Django: Django 是一个基于 Python 的 web 应用程序框架，可以无缝地与 MongoDB 一起用作后端数据库。这里有一个同样的教程。

*   NodeJS: Node 是一个基于 JavaScript 的 web 应用程序框架，它和 MongoDB 一起在 MEAN stack 中被广泛使用。[在这里结账的意思是](http://meanjs.org/)。
*   摘要

## 总结一下，这里我们分享了一个关于什么是 MongoDB 的简介？MongoDB 是一个快速可靠的数据库，在设计需要存储非结构化数据的可伸缩 web 应用程序时，它是推荐的数据库之一。如果您正在设计一个需要高可用性、集群、高性能的应用程序，那么您必须考虑使用 MongoDB 作为应用程序的后端数据库。你可以在这里查看编程社区推荐的最好的 MongoDB 教程。

**人也在读:**

**People are also reading:**