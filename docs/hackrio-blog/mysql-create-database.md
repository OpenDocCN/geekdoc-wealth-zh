# MySQL Create Database 语句:表，数据类型

> 原文：<https://hackr.io/blog/mysql-create-database>

MySQL 是最流行的关系数据库管理系统之一。它由 Oracle 公司开发和维护。除了 Drupal、Joomla 和 WordPress，MySQL 还被脸书、Flickr、Twitter 和 YouTube 等全球品牌使用。

## MySQL 创建数据库

除了作为 GNU 通用公共许可证下的免费开源软件之外，MySQL 也可以通过大量的专有许可证获得。

## **在 MySQL 中创建数据库**

创建数据库是处理任何数据库管理系统项目的第一步，或者也可以说是最基本的一步。

根据规模和范围，一个数据库管理项目可以有一个或多个数据库。一旦你成功地创建了一个数据库， [SQL 命令](https://hackr.io/blog/sql-commands)被用来操作数据库。

不同的数据库管理系统有不同的实现数据库的方式。MySQL 将数据库实现为一个目录，其中包含与该数据库中的表相对应的所有文件。

尽管基本原理保持不变，但在 MySQL 中有两种创建数据库的方法。第一种方法是直接从 MySQL 创建数据库，而另一种方法是使用 MySQL Workbench。

在解释在 MySQL 中创建数据库的两种方法之前，让我们首先检查 MySQL Create Database 语句。

## **MySQL 创建数据库语句**

CREATE DATABASE 语句用于在服务器中创建新的数据库。它的一般语法是:

```
CREATE DATABASE database_name
[CHARACTER SET charset_name]
[COLLATE collation_name]
```

您可以通过指定数据库名称来启动 create database 语句。它在 MySQL 服务器实例中必须是唯一的。如果您给正在创建的数据库起了一个已经分配给其他数据库的名字，那么 MySQL 将会产生一个错误。

可以在创建时为新数据库指定字符集和排序规则。但是，如果您选择不这样做，那么 MySQL 将为新创建的数据库使用默认的字符和排序规则。

## **使用**创建 MySQL 数据库

### **(一)MySQL 程序**

在 MySQL 中创建数据库的一种方法是使用 MySQL 程序和 CREATE DATABASE 语句。要以这种方式创建数据库，您需要:

**第一步**——以 root 用户身份登录 MySQL。为此，请使用以下命令:

```
>mysql -u root -p
```

现在，系统会提示您输入 root 用户密码，如下所示:

```
Enter password: _
```

键入 root 用户密码，然后按 Enter 键

**第 2 步**——要检查并确保您实际上没有创建一个数据库，而该数据库的名称已经被分配给 MySQL 服务器实例中的其他数据库，您可以使用 SHOW DATABASES 命令。它将返回当前正在使用的所有数据库名称

**步骤 3** -现在，使用 CREATE DATABASE 命令在 MySQL 服务器实例中创建新数据库，如下所示:

```
mysql> CREATE DATABASE database_name;
```

要查看新创建的数据库，可以使用 SHOW CREATE DATABASE 命令:

```
mysql> SHOW CREATE DATABASE database_name;
```

它将返回数据库的详细信息以及字符集和排序规则。

**步骤 4** -使用 use 命令访问新创建的数据库，如下所示:

```
mysql> USE database_name;
```

数据库已更改

可以开始创建表，存储值等。从现在开始在新创建的数据库中。

### **(二)MySQL 工作台**

MySQL Workbench 集合了 SQL 管理、开发、数据库管理等等:所有这些都可以从一个访问点访问。这是一个简化你用 MySQL 做的一切的好方法。

显然，您也可以使用 MySQL Workbench 在 MySQL 中创建数据库。但是，这样做时，您不需要使用 CREATE DATABASE 命令。相反，你将创建一个图形数据库，即通过输入一些细节和做大量的点击。

下面是使用 MySQL Workbench 创建新数据库的逐步过程:

*   **步骤 1** -启动 MySQL 工作台，点击“设置新连接”按钮(带有“+”号的按钮)
*   **步骤 2** -输入连接名称，然后点击测试连接按钮
*   **步骤 3** -现在会出现一个对话框提示您输入 root 密码。输入密码，选中“将密码保存在保险库中”复选框(如果尚未选中)，然后点击“确定”按钮
*   **步骤 4** -接下来，双击本地连接名称，以连接到 MySQL 服务器实例。现在您将被带到 MySQL Workbench 主窗口，该窗口由 4 个部分组成，即信息、导航器、输出和查询
*   **步骤 5** -点击工具栏中的在连接的服务器上创建新模式按钮(在 MySQL 中，模式只是引用数据库的另一个名称)
*   第六步 -现在会弹出一个窗口。如果需要，为它提供模式名并更改字符集和排序规则设置。最后，单击应用按钮
*   **步骤 7**——接下来，MySQL Workbench 将打开一个窗口，显示将要执行的 SQL 脚本。您会注意到这里有一个 CREATE SCHEMA 命令，它相当于 CREATE DATABASE 命令。因此，它后面是数据库名称。要继续，请单击“应用”按钮
*   **步骤 8** -新创建的数据库将反映在 MySQL Workbench 窗口的 Navigator 部分的 SCHEMAS 选项卡中
*   **步骤 9** -要选择新创建的数据库，右键单击它并选择 Set as Default Schema 选项

现在，您可以通过 MySQL Workbench 使用新创建的数据库。现在，您可以从这里或从 MySQL 程序向数据库添加新的表和数据。

[终极 MySQL 训练营:从 SQL 初学者到专家](https://click.linksynergy.com/link?id=jU79Zysihs4&offerid=1045023.1187016&type=2&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fthe-ultimate-mysql-bootcamp-go-from-sql-beginner-to-expert%2F)

## **全部完成！**

这就完成了在 MySQL 中创建新数据库和 MySQL Create Database 语句。创建数据库是开始数据库管理项目的切入点。

现在您已经知道了如何使用 Create Database 语句在 MySQL 中创建数据库，是时候开始使用您的数据库项目了。

你觉得这个帖子有用吗？还是你失望了？通过评论让我们知道。如果博文中有任何错误或任何改进的方法，请通过下面的专用评论窗口与我们分享。提前感谢！

希望提高您的 MySQL 技能，或者对学习流行的关系数据库管理系统的新知识感兴趣？现在就来看看这些[最佳 MySQL 教程](https://hackr.io/tutorials/learn-mysql?ref=blog-post)！

**人也在读:**