# MySQL 备忘单:下载 PDF 快速参考[排名]

> 原文：<https://hackr.io/blog/mysql-cheat-sheet>

创造

```
CREATE table (<table_name> <field1(type)>, <field2, (type)>…);
```

用于创建新表

插入

```
INSERT INTO
<table_name>(field1, field2, …)
VALUES(value1, value2,…)
```

该命令用于在表中插入一行或多行数据。

更新

```
UPDATE <table_name>
SET
field_name1 = value1,
field_name2 = value2,
[WHERE <condition>];
```

用于修改表中的现有数据。

这里的 WHERE 命令是可选的。

挑选

```
SELECT <field_list> FROM <table_name>;
```

用于从表格中选择列表值。

选择不同

```
SELECT DISTINCT <field_list> FROM <table_name>;
```

用于从列表中仅选择唯一值。

在哪里

```
SELECT <filed_list> FROM <table_name> WHERE <condition>;
```

WHERE 子句允许根据指定的条件选择值。

以...排序

```
SELECT <field_list> FROM <table_name> ORDER BY <field_name> [ASC|DESC];
```

ORDER BY 子句用于按升序或降序对查询的结果集进行排序。默认情况下，它将按升序排列。

和

```
… expression_1 AND expression_2
```

这是一个逻辑运算符。它主要与 WHERE 子句一起使用。这里，只有当两个表达式都为真时，才执行查询语句。

运筹学

```
… expression_1 OR expression_2
```

这是一个逻辑运算符。它主要与 WHERE 子句一起使用。这里，只有当一个或两个表达式都为真时，才执行查询语句。

在…里

```
SELECT <field_list> FROM <table_name> WHERE <expression|column_1> IN (value1, value2, …)
```

IN 运算符与 WHERE 子句一起使用。它能够确定列表中的指定值是否与另一组值相匹配。

在...之间

```
… expression [NOT] BETWEEN expression_1 AND expression_2
```

该运算符也与 WHERE 子句一起使用。它用于指定一个值是否在指定的范围内。

限制

```
SELECT <field_list> FROM <table_name> LIMIT <first_row_offset> <number of rows to be returned>;
```

此子句与 SELECT 语句一起使用，指定要返回的行数。

为空

```
Value IS NULL
```

它用于测试一个值是否为空。如果为空，表达式返回 true，否则返回 false。

内部连接

```
SELECT <field_list>
FROM <table1_name>
INNER JOIN <table2_name>
ON <join_condition>
```

这是一个筛选子句，它将一个表中的每一行与另一个表中的每一行进行匹配，从而能够只查询那些在两个表中都有相应列的行。

左连接

```
SELECT <field_names>
FROM <table1_name>
LEFT JOIN <table2_name>
ON join_condition;
```

它允许您从多个表中查询数据。它根据 join_condition 将第一个表中的每一行与第二个表中的每一行进行匹配

右连接

```
SELECT <field_names>
FROM <table1_name>
LEFT JOIN <table2_name>
ON join_condition;
```

与 LEFT_JOIN 相同，只是表操作的顺序相反。

它根据 join_condition 将第二个表中的每一行与第一个表中的每一行进行匹配

交叉连接

```
SELECT * FROM <table1_name>
CROSS JOIN <table2_name>;
```

它从连接的表中返回行的笛卡尔积。

分组依据

```
SELECT <field1, field2, field3…>
FROM <table1_name>
WHERE <condition/expression>
GROUP BY <field1, field2, field3…>
```

此命令允许根据列或表达式值将行分组到子组中。

拥有

```
SELECT <field1, field2, field3…>
FROM <table1_name>
WHERE <condition/expression>
GROUP BY <field1, field2, field3…>
HAVING <group_condition>
```

它通常与 GROUP BY 子句一起使用。用于指定一组行的过滤条件。

到达

```
SELECT <field_name1>,
SUM(column_name) <field_name2>
FROM <table_name>
GROUP BY <field_name1>WITH ROLLUP;
```

用于生成字段值的小计和总计。

存在

```
SELECT <field_list>
FROM <table_list>
WHERE [NOT] EXISTS(subquery);
```

它是一个布尔运算符，返回 true 或 false。它通常用于确定查询/子查询是否返回了任意数量的行。

横断

```
(SELECT <field_list> FROM <table1_name>) INTERSECT
(SELECT <field_list> FROM <table2_name>)
```

这是一个集合运算符，它只返回两个或更多查询的不同行。

联盟

```
SELECT <field_list>
UNION [DISTINCT | ALL]
SELECT <field_list>
UNION [DISTINCT | ALL]
```

该命令将来自多个选择查询的两个或多个结果集组合在一起，并返回一个结果集。

更新连接

```
UPDATE <table1>, <table2>.
[INNER JOIN | LEFT JOIN]
table1.common_field = table2.common_field
SET table1.field1 = newvalues …
WHERE <condition>
```

与 UPDATE 语句一起使用的 JOIN 子句称为 UPDATE JOIN。

删除

```
DELETE FROM <table_name>

WHERE <condition>
```

该命令用于从表中删除数据。

删除连接

```
DELETE <field1>,<field2>
FROM <table1>
INNER JOIN <table2>
ON table1.key = table2.key
WHERE <condition>;
```

该命令用于使用 JOIN 语句从多个表中删除数据。

在删除级联时

```
SELECT <table_name>
FROM <referential_constraints>
WHERE <constraint_schema = 'database_name'>
AND referenced_table_name = 'parent_table'
AND delete_rule = 'CASCADE'
```

当主表中的数据被删除时，该命令可以自动从子表中删除数据。

替换

```
REPLACE <table_name>(<field1>, <field2>,…)
VALUES (<value1>, <value2>, …)
```

该命令用于惰性化或更新表中的数据。