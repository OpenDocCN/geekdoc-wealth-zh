# SQL 命令教程:DDL，DML，TCL 和 DQL 命令

> 原文：<https://hackr.io/blog/sql-commands>

结构化查询语言或 SQL 是在关系数据库管理系统中用于管理数据的最广泛使用的编程语言。它还用于关系数据流管理系统中的流处理。

Oracle 数据库、MySQL、Microsoft SQL Server、PostgreSQL 和 [MariaDB](https://hackr.io/tutorials/learn-mariadb?ref=blog-post) 是一些最流行的关系数据库管理系统。

SQL 命令用于与数据库通信。从创建表和添加数据到修改表和设置用户权限，一切都是使用基本的 SQL 命令完成的。

## 带示例的 SQL 命令

所以，通过例子学习 SQL 命令是[学习 SQL](https://hackr.io/tutorials/learn-sql?ref=blog-post) 的第一步。共有 5 种类型的 SQL 命令，如下所述:

### **1。DDL 命令-数据定义语言**

SQL 中的数据定义语言或 DDL 命令用于改变表的结构。换句话说，DDL 命令能够创建、删除和修改数据。所有 DDL 命令都是自动提交的，这意味着它们所做的更改会自动保存在数据库中。以下是各种 DDL 命令:

#### **改变**

用于改变数据库的结构。通常，ALTER 命令用于添加新属性或修改某些现有属性的特征。

要向表中添加新列:

通用语法

```
ALTER TABLE table_name ADD (column_name1 data_type (size), column_name2 data_type (size),….., column_nameN data_type (size));

```

例子

```
ALTER TABLE Student ADD (Address varchar2(20));
ALTER TABLE Student ADD (Age number(2), Marks number(3));

```

要修改表中的现有列:

常规语法:

```
ALTER TABLE table_name MODIFY (column_name new_data_type(new_size));

```

示例:

```
ALTER TABLE Student MODIFY (Name varchar2(20));

```

ALTER 命令也可用于从表中删除列:

常规语法:

```
ALTER TABLE table_name DROP COLUMN column_name;

```

示例:

```
ALTER TABLE Student DROP COLUMN Age;
</pre.
*Note*: - It is not possible to do the following using the ALTER command:
```

*   更改列的名称
    *   更改表的名称
    *   减小列的大小
    *   **创建**

#### 用于在数据库中创建新表。常规语法:

示例:

```
CREATE TABLE table_name (column_name1 data_type(size), column_name2 data_type(size),…., column_nameN data_type(size));

```

**下降**

```
CREATE TABLE Employee(Name varchar2(20), D.O.B. date, Salary number(6);

```

#### 用于从数据库中删除整个表以及存储在其中的所有数据。

常规语法:

示例:

```
DROP TABLE table_name;

```

**重命名**

```
DROP TABLE Student;

```

#### 用于重命名表格。

常规语法:

示例:

```
RENAME old_table_name TO new_table_name

```

**截断**

```
RENAME Student TO Student_Details

```

#### 用于删除表中的所有行，并释放包含该表的空间。

常规语法:

示例:

```
TRUNCATE TABLE table_name;

```

**2。DML 命令-数据操作语言**

```
TRUNCATE TABLE Student;

```

### DML 或数据操作语言命令有助于修改关系数据库。这些命令不是自动提交的，这意味着使用 DML 命令对数据库所做的所有更改都不会自动保存。

可以回滚 DML 命令。各种 DML 命令包括:

**删除**

#### 用于从表格中删除一行或多行。

常规语法:

从表名中删除；(*删除表中的所有行* )
从表名中删除 WHERE some _ condition(*仅删除条件为真的行*)

*举例*:

**插入**

```
DELETE FROM Student;
DELETE FROM Student WHERE Name = “Akhil”;

```

#### 用于将数据插入表格的行中。

常规语法:

示例:

```
INSERT INTO table_name (column_name1, column_name2,….,column_nameN) VALUES (value1, value2,….,valueN);
OR
INSERT INTO table_name VALUES (value1, value2,….,valueN);

```

插入命令也可以用于将数据从另一个表插入到另一个表中。

```
INSERT INTO Student (Name, Age) VALUES (“Vijay”, “25”);

```

常规语法:

示例:

```
INSERT INTO table_name1 SELECT column_name1, column_name2,….,column_nameN FROM table_name2;

```

**更新**

```
INSERT INTO Student SELECT Id, Stream FROM Student_Subject_Details

```

#### 用于修改或更新表中某一列的值。它可以更新表中的所有行或一些有选择的行。

常规语法:

示例:

```
UPDATE table_name SET column_name1 = value1, column_name2 = value2,….,column_nameN = valueN (*for updating all rows*)
UPDATE table_name SET column_name1 = value1, column_name2 = value2,….,column_nameN = valueN [WHERE CONDITION] (*for updating particular rows*)

```

**3。DCL 命令-数据控制语言**

```
UPDATE Student SET Name = “Akhil” WHERE Id = 22;
```

### 为了防止表中的信息受到未经授权的访问，使用了 DCL 命令。DCL 命令可以允许或禁止用户访问数据库中的信息。用户访问权限列表:

改变

*   删除
*   指数
*   插入
*   挑选
*   更新
*   **授予**

#### 用于授予用户对数据库的访问权限。

常规语法:

示例:

```
GRANT object_privileges ON table_name TO user_name1, user_name2,….,user_nameN;
GRANT object_privileges ON table_name TO user_name1, user_name2,….,user_nameN WITH GRANT OPTION; (*allows the grantee to grant user access privileges to others*)

```

这将允许用户只对 Student 表运行选择和更新操作。

```
GRANT SELECT, UPDATE ON Student TO Akhil Bhadwal

```

允许用户运行表上的所有命令，并授予其他用户访问权限。

```
GRANT ALL ON Student TO Akhil Bhadwal WITH GRANT OPTION

```

**撤销**

#### 用于收回授予用户的权限。

常规语法:

示例:

```
REVOKE object_privileges ON table_name FROM user1, user2,… userN;

```

***注意*** : -不是表的所有者但被授予了向其他用户授予权限的用户也可以撤销权限。

```
REVOKE UPDATE ON Student FROM Akhil;

```

**4。TCL 命令-交易控制语言**

### 事务控制语言命令只能与 DML 命令一起使用。因为这些操作是在数据库中自动提交的，所以在创建或删除表时不能使用它们。各种 TCL 命令包括:

**提交**

#### 用于保存对数据库进行的所有事务。结束当前事务，并使事务期间所做的所有更改永久化。释放在表上获取的所有事务锁。

常规语法:

示例:

```
COMMIT;

```

**回滚**

```
DELETE FROM Student WHERE Age = 25;
COMMIT;

```

#### 用于撤消尚未保存在数据库中的事务。结束事务并撤消事务期间所做的所有更改。释放在表上获取的所有事务锁。

常规语法:

示例:

```
ROLLBACK;

```

**保存点**

```
DELETE FROM Student WHERE Age = 25;
ROLLBACK;

```

#### 用于回滚到称为保存点的特定状态。需要首先创建保存点，以便它们可以用于部分回滚事务。

常规语法:

保存点保存点名称；

***注意*** : -活动保存点是自上一次提交或回滚命令以来指定的保存点。

**5。DQL 命令-数据查询语言**

### DQL 命令用于从关系数据库中获取数据。只有一个命令，就是 SELECT 命令。

相当于关系代数中的[投影操作](https://en.wikipedia.org/wiki/Projection_(relational_algebra))，SELECT 命令根据 WHERE 子句描述的条件选择属性。

常规语法:

*举例*:

```
SELECT expressions
FROM table_name
WHERE condition1, condition2,…., conditionN;

```

假设我们有一个名为 Student 的关系表，其中有关于一个学生的所有信息，比如姓名、学号、流、年龄、地址等。并且我们需要获取关于所有 18 岁以下学生姓名的数据，那么我们可以使用 SELECT 命令，如下所示:

结果将是所有未满 18 岁的学生姓名的列表。

```
SELECT student_name
FROM student
WHERE age < 18;

```

SELECT 命令也可用于消除表中的重复项。

常规语法:

示例:

```
SELECT DISTINCT column_name1, column_name2,…., column_nameN FROM table_name;

```

该命令将扫描整行，并删除相同的行。

```
SELECT DISTINCT Name, Age FROM Student;

```

使用 SELECT 命令检索的行可以按升序或降序排序。

常规语法:

示例:

```
SELECT column_name1, column_name2,…., column_nameN FROM table_name ORDER BY column_name; (*gives results in ascending order*)
SELECT column_name1, column_name2,…., column_nameN FROM table_name ORDER BY column_name DESC; (*gives results in descending order*)

```

**[终极 MySQL 训练营:从 SQL 初学者到专家](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fthe-ultimate-mysql-bootcamp-go-from-sql-beginner-to-expert%2F)**

```
SELECT Name, Age FROM Student ORDER BY Name;
SELECT Name, Age FROM Student ORDER BY Name DESC;

```

**结论**

## 了解常用命令[SQl 命令列表]是理解和使用 SQl 数据库的第一步。掌握 SQL 命令需要大量的实践，我们希望这篇文章能帮助你开始你的旅程！

准备 SQL 面试？查看这些[最重要的 SQL 面试问题](https://hackr.io/blog/top-sql-interview-questions)以抓住机会。

**人也在读:**

**People are also reading:**