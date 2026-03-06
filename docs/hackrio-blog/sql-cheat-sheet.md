# 快速参考的 SQL 备忘单[PDF 下载]

> 原文：<https://hackr.io/blog/sql-cheat-sheet>

无论你是在面试前需要一个主要 SQL 概念的快速参考，还是想提高你现有的 SQL 技能，我们的 SQL 备忘单都是理想的起点。此外，我们将它分解为 11 个基本的 SQL 主题，以帮助您从这个 SQL 查询备忘单中获得最大收益。

期待[从零开始学习 SQL](https://hackr.io/blog/how-to-learn-sql) ，或者想知道 [SQL 和 MySQL](https://hackr.io/blog/sql-vs-mysql) 的区别？你一定要看看我们的 SQL 内容的[部分。但是现在，让我们深入这个 SQL 命令备忘单。](https://hackr.io/blog/category/sql)

[**在这里下载 Hackr.io 的 SQL 备忘单 PDF。**](https://drive.google.com/file/d/1XgQP_UE_v5EPTN0omgMVW1j3F4uxlfj_/view?usp=sharing)

## **SQL 备忘单**

### **1。什么是 SQL？我们为什么需要它？**

SQL 是一种数据库语言，用于查询和操作数据库中的数据，同时为您提供一个高效便捷的数据库管理环境。

我们可以将命令分为以下几类 **SQL 语句:**

#### **数据定义语言(DDL)命令**

*   **CREATE:** 创建一个新的数据库对象，比如一个表
*   **修改:**用于修改数据库对象
*   **删除:**用于删除数据库对象

#### **数据操作语言(DML)命令**

*   **插入:**用于在数据库表中插入新的一行(记录)
*   **更新:**用于修改数据库表中已有的行(记录)
*   **删除:**用于从数据库表中删除一行(记录)

#### **数据控制语言(DCL)命令**

*   **GRANT:** 用于分配用户访问数据库对象的权限
*   **撤销:**用于删除之前授予的用户访问数据库对象的权限

#### **数据查询语言(DQL)命令**

*   **选择:**用于从数据库中选择并返回数据(查询)

#### **数据传输语言(DTL)命令**

*   **提交:**用于在数据库中永久保存事务
*   **回滚:**将数据库恢复到上次提交的状态

### **2。SQL 数据类型**

[数据类型](https://en.wikibooks.org/wiki/Structured_Query_Language/Data_Types)指定一个对象可以包含的数据类型，如数字数据或字符数据。我们需要选择一种数据类型来匹配将使用下面的**基本预定义数据类型**列表存储的数据:

| **数据类型** | **用于存储** |
| （同 Internationalorganizations）国际组织 | 整数数据(精确数值) |
| 斯莫列特 | 整数数据(精确数值) |
| tinyint | 整数数据(精确数值) |
| 比吉斯本 | 整数数据(精确数值) |
| 小数 | 具有固定精度和小数位数的数值数据类型(精确数值) |
| 数字的 | 具有固定精度和小数位数的数值数据类型(精确数值) |
| 漂浮物 | 浮点精度数据(近似数字) |
| 钱 | 货币数据 |
| 日期时间 | 日期和时间数据 |
| 字符 | 固定长度字符数据 |
| 可变字符 | 可变长度字符数据 |
| 文本 | 字符串 |
| 少量 | 为 0 或 1 的整数数据(二进制) |
| 图像 | 存储图像文件的可变长度二进制数据 |
| 真实的 | 浮点精度数字(近似数字) |
| 二进制的 | 固定长度二进制数据 |
| 光标 | 光标引用 |
| sql _ 变量 | 允许列存储不同的数据类型 |
| 时间戳 | 每次插入或更新行时更新的唯一数据库 |
| 桌子 | 运行表值函数后返回的临时行集(TVF) |
| 可扩展标记语言 | 存储 xml 数据 |

### **3。管理表格**

在我们创建了一个数据库之后，下一步是使用我们的 **DDL 命令**创建并随后管理一个数据库表。

#### **创建表格**

可以用 **CREATE TABLE** 语句创建一个表。

**创建表的语法:**

```
CREATE TABLE table_name

(

col_name1 data_type,

col_name2 data_type,

col_name3 data_type,

…

);
```

**示例:**在人力资源模式中创建一个名为 EmployeeLeave 的表，该表具有以下属性。

| **列** | **数据类型** | **检查** |
| 员工 ID | （同 Internationalorganizations）国际组织 | 不为空 |
| LeaveStartDate | 日期 | 不为空 |
| LeaveEndDate | 日期 | 不为空 |
| 离开原因 | varchar(100) | 不为空 |
| 树叶类型 | char(2) | 不为空 |

```
CREATETABLE HumanResources.EmployeeLeave

(

EmployeeID INTNOTNULL,

LeaveStartDate DATETIMENOTNULL,

LeaveEndDate DATETIMENOTNULL,

LeaveReason VARCHAR(100),

LeaveType CHAR(2) NOTNULL

);
```

#### **SQL 表约束**

约束定义了确保数据一致性和正确性的规则。一个**约束**可以用以下方法之一创建。

```
CREATETABLEstatement;

ALTERTABLEstatement;

CREATETABLE table_name

( Col_name data_type,

CONSTRAINT constraint_name constraint_type col_name(s) 

);
```

以下列表详细说明了**约束的各种选项:**

| **约束** | **描述** | **语法** |
| 主关键字 | 唯一标识表中每行的一列或多列。 | 

```
CREATETABLE table_name  (  col_name data_type,   CONSTRAINT constraint_name  PRIMARYKEY (col_name(s))   );
```

 |
| 唯一键 | 强制非主键列的唯一性。 | 

```
CREATETABLE table_name  (  col_name data_type,   CONSTRAINT constraint_name  UNIQUEKEY (col_name(s))   );
```

 |
| 外键 | 链接两个表(父表和子表)，并确保在插入数据之前子表的外键作为主键存在于父表中。 | 

```
CREATETABLE table_name  (  col_name data_type,   CONSTRAINT constraint_name  FOREIGNKEY (col_name)  REFERENCES  table_name(col_name)  );
```

 |
| 支票 | 通过限制可以插入到列中的值来实施域完整性。 | 

```
CREATETABLE table_name  (  col_name data_type,   CONSTRAINT constraint_name  CHECK (expression)   );
```

 |

#### **修改表格**

在下列情况下，我们可以使用 **ALTER TABLE** 语句来**修改一个表:**

1.  添加列
2.  改变列的数据类型
3.  添加或移除约束

**ALTER TABLE 的语法:**

```
ALTERTABLE table_name

ADD column_name data_type;

ALTERTABLE table_name

DROPCOLUMN column_name;

ALTERTABLE table_name

ALTERCOLUMN column_name data_type;
```

#### **重命名表格**

可以使用**重命名表语句来重命名表:**

```
RENAMETABLE old_table_name TO new_table_name;
```

#### **删除表格与截断表格**

使用 **DROP TABLE 语句:**可以删除一个表

```
DROPTABLE table_name;
```

使用 **TRUNCATE TABLE 语句:**可以删除表的内容(不删除表)

```
TRUNCATETABLE table_name;
```

[完整的 SQL Bootcamp 2023:从零到英雄](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fthe-complete-sql-bootcamp%2F)

### **4。操纵数据**

数据库表很少是静态的，我们经常需要使用我们的 **DML 命令**添加新数据、更改现有数据或删除数据。

#### **在表格中存储数据**

可以使用 **INSERT** 语句将数据添加到表格中。

**插入的语法:**

```
INSERTINTO table_name ( col_name1, col_name2, col_name3… )

VALUES ( value1, value2, value3… );
```

**示例:**向学生表中插入数据。

```
INSERTINTO Student ( StudentID, FirstName, LastName, Marks )

VALUES ( ‘101’, ’John’, ’Ray’, ’78’ );
```

**示例:**向学生表中插入多行数据。

```
INSERTINTO Student 

VALUES ( 101, ’John’, ’Ray’, 78 ),

( 102, ‘Steve’, ’Jobs’, 89 ),

( 103, ‘Ben’, ’Matt’, 77 ),

( 104, ‘Ron’, ’Neil’, 65 ),

( 105, ‘Andy’, ’Clifton’, 65 ),

( 106, ‘Park’, ’Jin’, 90 );
```

使用 **INSERT 语句将数据从一个表复制到另一个表的语法:**

```
INSERTINTO table_name2

SELECT * FROM table_name1

WHERE [condition];
```

#### **更新表格中的数据**

可以用 **UPDATE** 语句更新表中的数据。

**更新的语法:**

```
UPDATE table_name

SET col_name1 = value1, col_name2 = value2…

WHERE condition;
```

**示例:**当名字等于“安迪”时，将“标记”列中的值更新为“85”

```
UPDATE table_name

SET Marks = 85

WHERE FirstName = ‘Andy’;
```

#### **从表格中删除数据**

可以用 **DELETE** 语句删除一行。

**删除的语法:**

```
DELETEFROM table_name

WHERE condition;

DELETEFROM Student

WHERE StudentID = ‘103’;
```

用 **DELETE:** 从表格中删除所有行(记录)而不删除表格

```
DELETEFROM table_name;
```

### **5。正在检索数据**

从表中检索数据时，我们可以显示一列或多列。例如，我们可能想要查看 Employee 表中的所有详细信息，或者我们可能想要查看特定列的选择。

可以使用 **SELECT** 语句从数据库表中检索数据。

**选择的语法:**

```
SELECT [ALL | DISTINCT] column_list

FROM [table_name | view_name]

WHERE condition;
```

考虑下面学生表的数据和模式。

| **StudentID** | **名字** | **姓氏** | **标记** |
| 101 | 约翰 | 光线 | 78 |
| 102 | 史蒂夫(男子名) | 乔布斯 | 89 |
| 103 | 本(男子名) | 马特(男子名ˌ等于 Matthew) | 77 |
| 104 | 留宿（remain overnight 的缩写） | 尼尔 | 65 |
| 105 | 安迪(男子名ˌ等于 Andrew) | 克利夫顿（m.） | 65 |
| 106 | 公园 | 金 | 90 |

#### **检索选中的行**

我们可以使用 **WHERE** 子句和 **SELECT 语句:**从一个表中检索一组行

```
SELECT * FROM Student 

WHERE StudentID = 104;
```

**注意:**我们应该使用 **HAVING** 子句，而不是**WHERE**with aggregate functions。

#### **比较运算符**

比较运算符测试两个表达式之间的相似性。

**比较的语法:**

```
SELECT column_list FROM table_name

WHERE expression1 [COMP_OPERATOR] expression2;
```

**举例:**各种比较操作。

```
SELECT StudentID, Marks FROM Student 
WHERE Marks = 90;

SELECT StudentID, Marks FROM Student 
WHERE StudentID > 101;

SELECT StudentID, Marks FROM Student 
WHERE Marks != 89;

SELECT StudentID, Marks FROM Student 
WHERE Marks >= 50;
```

#### **逻辑运算符**

逻辑运算符与 **SELECT** 语句一起使用，根据一个或多个逻辑条件检索记录。您可以组合多个逻辑运算符来应用多个搜索条件。

**逻辑运算符的语法:**

##### **逻辑运算符的类型**

我们可以使用一系列逻辑运算符来过滤我们的数据选择。

**逻辑或运算符的语法:**

```
SELECT StudentID, Marks FROM Student

WHERE Marks = 40OR Marks = 56OR Marks = 65;
```

**逻辑 AND 运算符的语法:**

```
SELECT StudentID, Marks FROM Student

WHERE Marks = 89AND LastName = ‘Jones’;
```

**逻辑非运算符的语法:**

```
SELECT StudentID, Marks FROM Student

WHERENOT LastName = ‘Jobs’;
```

#### **范围操作**

我们可以在和**之间使用**而不是在**语句之间使用**来检索基于范围的数据。****

**范围操作的语法:**

```
SELECT column_name1, col_name2… FROM table_name

WHERE expression1 RANGE_OPERATOR expression2 [LOGICAL_OPERATOR expression3…];
```

之间的**的语法**

```
SELECT StudentID, Marks FROM Student

WHERE Marks BETWEEN40AND70;
```

**的语法不在:**之间

```
SELECT FirstName, Marks FROM Student

WHERE Marks NOTBETWEEN40AND50;
```

#### **检索与模式匹配的记录**

如果数据匹配特定的字符串模式，可以使用 **LIKE** 语句从表中获取数据。字符串模式可以是精确的，也可以使用 **'% '和' _ '通配符**。

**与“%”相似的语法:**

```
SELECT * FROM Student 

WHERE FirstName LIKE ‘Ro%’;
```

**的语法与' _ '相似:**

```
SELECT *FROM Student 

WHERE FirstName LIKE ‘_e’;
```

#### **按顺序显示数据**

我们可以用 **ORDER BY:** 按特定顺序(升序或降序)显示检索到的数据

```
SELECT StudentID, LastName FROM Student

ORDERBY Marks DESC;
```

#### **无重复显示数据**

**DISTINCT** 关键字可用于消除特定列中具有重复值的行。

**DISTINCT:** 的语法

```
SELECT[ALL]DISTINCT col_names FROM table_name

WHERE search_condition;

SELECTDISTINCT Marks FROM Student

WHERE LastName LIKE ‘o%’;
```

### **6。SQL 连接**

联接用于从多个表中检索数据，在这些表中，结果被“联接”到一个组合的返回数据集中。两个或多个表可以基于一个公共属性进行联接。

考虑两个数据库表，Employees 和 EmployeeSalary，我们将用它们来演示连接。

| **员工 ID (PK)** | **名字** | **姓氏** | **标题** |
| 1001 | 留宿（remain overnight 的缩写） | 黑雁 | 开发者 |
| 1002 | 亚历克斯 | 马特(男子名ˌ等于 Matthew) | 经理 |
| 1003 | 光线 | 迷嬉装 | 测试员 |
| 1004 | 八月 | 冰山 | 质量 |

| **雇员 ID (FK)** | **部门** | **工资** |
| 1001 | 应用 | 65000 |
| 1002 | 数字营销 | 75000 |
| 1003 | 网 | 45000 |
| 1004 | 软件工具 | 68000 |

#### **连接类型**

两种主要的连接类型是**内部连接**和**外部连接。**

##### **内部连接**

当某个公共列的比较操作返回 true 时，内部联接从多个表中检索记录。这可以返回两个表中的所有列，或者一组选定的列。

**内部连接的语法:**

```
SELECT table1.column_name1, table2.colomn_name2,…

FROM table1

INNERJOIN table2 

ON table1.column_name = table2.column_name;
```

**示例:**Employees 上的内部连接&Employees ary 表。

```
SELECT Employees.LastName, Employees.Title, EmployeeSalary.salary,

FROM Employees

INNERJOIN EmployeeSalary

ON Employees.EmployeeID = EmployeeSalary.EmployeeID;
```

##### **外部连接**

外部连接显示下面的**组合数据集:**

*   其中一个表中的每一行(取决于左连接或右连接)
*   满足给定条件的一个表中的行

对于没有找到匹配记录的列，外部连接将显示空值。

**外部连接的语法:**

```
SELECT table1.column_name1, table2.colomn_name2,… FROM table1

[LEFT|RIGHT|FULL]OUTERJOIN table2

ON table1.column_name = table2.column_name;
```

**LEFT OUTER JOIN:** 返回“LEFT”表中的每一行(LEFT OUTER JOIN 关键字的左边)，返回“right”表中的匹配行。

**示例:**左外连接。

```
SELECT Employees.LastName, Employees.Title, EmployeeSalary.salary

FROM Employees 

LEFTOUTERJOIN EmployeeSalary

ON Employees.EmployeeID = EmployeeSalary.EmployeeID;
```

**右外连接:**返回“右”表中的每一行(右外连接关键字的右侧)，并返回“左”表中的匹配行。

**示例:**右外连接。

```
SELECT Employees.LastName, Employees.Title, EmployeeSalary.salary

FROM Employees 

RIGHTOUTERJOIN EmployeeSalary

ON Employees.EmployeeID = EmployeeSalary.EmployeeID;
```

**完全外部连接:**返回两个表中所有匹配和不匹配的行，每行只显示一次。

**示例:**全外连接。

```
SELECT Employees.LastName, Employees.Title, EmployeeSalary.salary

FROM Employees 

FULLOUTERJOIN EmployeeSalary

ON Employees.EmployeeID = EmployeeSalary.EmployeeID;
```

##### **交叉连接**

也被称为**笛卡尔积**，两个表(A 和 B)之间的**交叉连接**将表 A 中的每一行与表 B 中的每一行“连接”，形成行的“对”。连接的数据集包含来自表 A 和表 b 的行“对”的“组合”

连接数据集中的行数等于表 A 中的行数乘以表 b 中的行数。

**交叉连接的语法:**

```
SELECT col_1, col_2 FROM table1

CROSSJOIN table2;
```

##### **等价连接**

一个**等价连接**是在一个连接操作中对表键使用一个**相等**条件的连接。这意味着如果条件子句是相等的，那么内部和外部连接可以是相等的连接。

##### **自加入**

一个**自连接**是当你连接一个表和它自己。当您希望查询并返回单个表中行之间的相关信息时，这很有用。当同一表中的行之间存在“父”和“子”关系时，这很有帮助。

**示例:**如果 Employees 表包含将雇员链接到主管(也是同一表中的雇员)的引用。

为了防止不明确的问题，在执行自连接时，对每个表引用使用别名是很重要的。

**自连接的语法:**

```
SELECT t1.col1 AS “Column 1”, t2.col2 AS “Column 2” 

FROM table1 AS t1 

JOIN table1 AS t2

WHERE condition;
```

### **7。SQL 子查询**

放在另一个 SQL 语句中的 SQL 语句是一个**子查询**。

**子查询嵌套在用于 SELECT、INSERT、UPDATE 和 DELETE 语句的 WHERE、HAVING 或 FROM 子句中。**

*   **外部查询:**代表**主查询**
*   **内部查询:**代表**子查询**

#### **使用 IN 关键字**

我们可以使用关键字中的**作为逻辑运算符，根据子查询结果列表过滤主查询(外部查询)的数据。这是因为由于内部嵌套位置，将首先计算子查询。这种过滤是主查询的条件子句的一部分。**

**示例:**运行带有条件的子查询以返回数据集。然后，子查询结果成为主查询的条件子句的一部分。然后，我们可以使用关键字中的**来根据特定列的子查询结果过滤主查询结果。**

关键字:中**的语法**

```
SELECT column_1 FROM table_name

WHERE column_2 [NOT]IN

( SELECT column_2

FROM table_name [WHERE conditional_expression] );
```

#### **使用 EXISTS 关键字**

我们可以使用 **EXISTS** 关键字作为一种逻辑运算符来检查子查询是否返回一组记录。这意味着如果被评估的子查询返回任何与子查询语句匹配的行，操作符将返回 **TRUE** 。

我们还可以使用 **EXISTS** 根据任何提供的条件过滤子查询结果。您可以将它看作是对子查询语句处理的任何数据的条件“成员资格”检查。

**EXISTS 关键字的语法:**

```
SELECT column FROM table_name

WHEREEXISTS

( SELECT column_name FROM table_name [WHERE condition] );
```

#### **使用嵌套子查询**

任何单个子查询还可以包含一个或多个额外的**嵌套子查询**。这类似于传统编程中的嵌套条件语句，这意味着查询将从最内层开始向外计算。

当一个查询的条件依赖于另一个查询的结果，而另一个查询又依赖于另一个查询的结果时，我们使用嵌套子查询。

**嵌套子查询的语法:**

```
SELECT col_name FROM table_name

WHERE col_name(s) [LOGICAL | CONDITIONAL | COMPARISON OPERATOR]

( SELECT col_name(s) FROM table_name

WHERE col_name(s) [LOGICAL | CONDITIONAL | COMPARISON OPERATOR]

( SELECT col_name(s) FROM table_name

WHERE [condition] )

);
```

相关子查询是一种特殊类型的子查询，它使用外部查询中引用的表中的数据作为自己评估的一部分。

### **8。使用函数定制结果集**

各种内置函数可用于自定义结果集。

**函数的语法:**

```
SELECT function_name (parameters);
```

#### **使用字符串函数**

当我们的结果集包含数据类型为 **char** 和 **varchar** 的字符串时，我们可以通过使用**字符串函数**来操作这些字符串值:

| **功能名称** | **例子** |
| 左边的 | **选择** **离开**(【理查】，4)； |
| 低输入联网（low-entry networking 的缩写） | **选择****len**(‘理查德’)； |
| 降低 | **选择** **降低**(‘理查德’)； |
| 反面的 | **选择** **反转**(‘动作’)； |
| 正确 | **选择** **右**(【理查】，4)； |
| 空间 | **选择**‘理查德’+**空间**(2)+‘希尔’； |
| 潜艇用热中子反应堆（submarine thermal reactor 的缩写） | **选择** **str** (123.45，6，2)； |
| 子链 | **选择** **子串**(天气'，2，2)； |
| 上面的 | **选择** **上位**(‘理’)； |

#### **使用日期功能**

当我们的结果集包含日期和时间数据时，我们可能希望操作它来提取日、月、年或时间，并且我们可能还希望将类似日期的数据解析为 datetime 数据类型。我们可以通过使用**日期函数来做到这一点:**

| **功能名称** | **参数** | **描述** |
| dateadd | (日期部分、编号、日期) | 将日期部分的“数字”添加到日期中 |
| datediff | (日期部分，日期 1，日期 2) | 计算两个日期之间日期部分的“数目” |
| 日期名称 | (日期部分，日期) | 以字符值形式返回给定日期的日期部分 |
| 日期部分 | (日期部分，日期) | 以整数值形式返回给定日期的日期部分 |
| getdate | 0 | 返回当前日期和时间 |
| 天 | (日期) | 返回一个整数来表示给定日期的第几天 |
| 月 | (日期) | 返回一个整数，表示给定日期的月份 |
| 年 | (日期) | 返回一个整数，表示给定日期的年份 |

#### **使用数学函数**

我们可以通过使用**数学函数:**在结果集中操作数字数据类型

| **功能名称** | **参数** | **描述** |
| 丙烯腈-丁二烯-苯乙烯 | (数值表达式) | 返回绝对值 |
| acos，asin，atan | (数值表达式) | 返回以弧度表示的反正弦角、反正弦角或反正切角 |
| cos，sin，tan，cot | (数值表达式) | 返回以弧度表示的余弦、正弦、正切或余切值 |
| 度 | (弧度) | 返回从弧度转换而来的角度(以度为单位) |
| 经历 | (数值表达式) | 返回 e 的给定数字或表达式的幂的值 |
| 地面 | (数值表达式) | 返回小于或等于给定值的最大整数值 |
| 原木 | (数值表达式) | 返回给定值的自然对数 |
| 圆周率 | 0 | 返回 pi 的常数值 3.141592653589793… |
| 力量 | (数值表达式，y) | 返回数值表达式的 y 次方值 |
| 弧度 | (度) | 返回以弧度为单位的角度，该角度由度数转换而来 |
| 边缘 | ([种子]) | 返回一个介于 0 和 1 之间的随机浮点数 |
| 轮次 | (数字，精度) | 根据精度，将给定数值舍入为给定整数值 |
| 符号 | (数值表达式) | 返回给定值的符号，可以是正数、负数或零 |
| 平方根计算 | (数值表达式) | 返回给定值的平方根 |

#### **使用排名函数**

**排名函数**(也称为**窗口函数**)基于给定的标准生成并返回顺序号来表示每个的排名。为了对记录进行排序，我们使用下面的**排序函数:**

*   **row_number() :** 根据给定的列，为结果集中的每一行返回从 1 开始的序列号
*   **rank() :** 根据指定的条件返回结果集中每一行的排名(可能导致重复的排名值)
*   **dense_rank() :** 当给定标准需要连续的排名值时使用(没有重复的排名值)

每个排名函数都使用 **OVER** 子句来指定排名标准。在这里，我们选择一个列来分配一个等级，同时使用关键字的**来确定等级是基于升序还是降序来应用。**

#### **使用聚合函数**

聚合函数汇总一列或一组列的值，以生成单个(聚合)值。

**聚合函数的语法:**

```
SELECTAGG_FUNCTION( [ALL |DISTINCT] expression )

FROM table_name;
```

下表总结了各种 **SQL** **聚合函数:**

| **功能名称** | **描述** |
| 平均 | 返回给定数据集或表达式中一系列值的平均值。可以包括**所有的**值或**不同的**值 |
| 数数 | 返回给定数据集或表达式中值的数量(计数)。可以包括**所有的**值或**不同的**值 |
| 部 | 返回给定数据集或表达式中的最小值 |
| 最大 | 返回给定数据集或表达式中的最大值 |
| 总和 | 返回给定数据集或表达式中值的总和。可以包括**所有的**值或**不同的**值 |

### **9。分组数据**

我们可以选择根据特定的标准对结果集中的数据进行分组。我们通过使用可选的 **GROUP BY** 、 **COMPUTE** 、 **COMPUTE BY** 和 **PIVOT** 子句以及 **SELECT** 语句来实现这一点。

#### **GROUP BY 子句**

在没有附加条件的情况下使用时， **GROUP BY** 将结果集中的数据放入唯一的组中。但是当与聚合函数一起使用时，我们可以将数据汇总(聚合)到每个组的各个行中。

**分组依据:**的语法

```
SELECT column(s) FROM table_name

GROUPBY expression

[HAVING search_condition];
```

#### **计算和按子句计算**

我们可以使用带有 **SELECT** 语句和**聚合函数**的 **COMPUTE** 子句来生成汇总行，作为我们查询的单独结果。我们还可以使用可选的 **BY** 关键字来逐列计算汇总值。

**COMPUTE [BY]的语法:**

```
SELECT column(s) FROM table_name

[ORDERBY column_name]

COMPUTE [BY column_name]AGG_FUNCTION(column_name)
```

**注意:**MS SQL Server 在 2012 年放弃了对该关键字的支持。

#### **PIVOT 子句**

**PIVOT** 操作符用于将唯一的行转换为列标题。您可以将此视为将数据旋转或透视到一个新的“数据透视表”中，该数据透视表包含每个旋转列的汇总(聚合)值。使用此表，您可以在列的基础上检查趋势或汇总值。

**透视的语法:**

```
SELECT * FROM table_name

PIVOT ( AGG_FUNCTION (value_column) 

FOR pivot_column

IN column(s) ) 

AS pivot_table_alias;
```

### 10。酸性属性

术语**酸**代表**原子数**、**稠度**、**隔离度**、**耐久性**。这些单独的属性代表一个标准化的组，需要这些属性来确保可靠地处理数据库事务。

#### **原子数**

整个交易必须完全处理或根本不处理的概念。

#### **一致性**

要求数据库在事务完成前后保持一致(有效的数据类型、约束等)。

#### **隔离**

交易必须单独处理，并且不得干扰其他交易。

#### **耐久性**

交易开始后，必须成功处理。即使在事务开始后不久出现系统故障，这一点也适用。

### **11。RDBMS**

**关系数据库管理系统** (RDBMS)是一个软件，它允许你在关系数据库上执行数据库管理任务，包括创建、读取、更新和删除数据( **CRUD** )。

关系数据库通过各种表中的列和行来存储数据集合。每个表都可以通过主键和外键形式的公共属性与其他表相关联。

## **结论**

这就是我们的 SQL 备忘单。无论您是在寻找面试用的 SQL 备忘单，还是想提高您现有的 SQL 技能，或者您需要 SQL 基础知识备忘单来帮助您首次学习 SQL，我们希望它能帮助您！

请记住，我们的 SQL 备忘单 PDF 是一个有用的工具，但真正重要的是您将所有这些理论付诸实践。一如既往，这是最好的学习方式！

**如果你想学习 SQL，可以查看网上提供的** [**最佳 SQL 课程**](https://hackr.io/blog/best-sql-courses) **。**

**也可以下载 Hackr.io 的** [**SQL 注入小抄**](https://drive.google.com/file/d/1XgQP_UE_v5EPTN0omgMVW1j3F4uxlfj_/view?usp=sharing) **。**

## **常见问题解答**

#### **1。什么是 SQL 语法备忘单？**

SQL 备忘单是该语言所有主要概念的简要总结，便于参考。我们上面详述的 SQL 备忘单涵盖了所有基本概念。

#### **2。我如何记忆 SQL 查询？**

实践是记忆 SQL 查询的最好方法。你会发现，当你把它们投入实际使用时，学习起来会容易得多。

#### **3。5 个基本的 SQL 命令是什么？**

基本的 SQL 命令备忘单对于快速学习很有用。5 个基本 SQL 命令组是数据定义语言、数据操作语言、数据控制语言、数据查询语言和数据传输语言。

**人也在读:**