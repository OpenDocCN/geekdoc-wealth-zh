# 下载 XPath 备忘单 PDF 作为快速参考

> 原文：<https://hackr.io/blog/xpath-cheat-sheet>

Selenium 框架帮助我们与 DOM(文档对象模型)中的 WebElements 进行交互。但是，您需要网络定位器才能继续。幸运的是，市面上有很多 Selenium web 定位器。您可能渴望一个 Selenium locators 备忘单来帮助您。唯一的问题是:对于与 [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction) 中的 WebElements 的最佳交互，哪一个是正确的？

Selenium 为 web 定位器提供了广泛的选项，比如 ID、名称、XPath、LinkText 和标记名。

XPath 是最常用的方法之一。XPath 或 XML 路径语言是一种表达式语言，支持 XML 文档的查询或转换。它可以很容易地遍历 DOM 元素和属性。

如果您计划使用 XPath web 定位器来创建测试自动化脚本，那么这个 XPath 备忘单就是为您准备的。我们的 Selenium XPath 备忘单将帮助您学习和记住 XPath 语法、表达式等等。

[点击这里](https://drive.google.com/file/d/1opAv6PCccceNutM8zfW0Xfc8p6vyu25J/view?usp=sharing)下载我们的免费 XPath 备忘单 PDF。

我们开始吧！

## 快速参考的 XPath 备忘单

当您需要快速浏览 XPath 语法和 XPath 定位器的其他方面时，这个 XPath 备忘单就派上了用场。

首先，让我们探索一下 Selenium 中 XPath web 位置的确切含义。

### Selenium 中的 XPath Web Locator 是什么？

XPath 使用类似路径的语法，帮助我们识别和导航 XML 和 HTML 文档中的节点。换句话说，它使用非 XML 语法，这使得它可以灵活地处理 XML 文档的各个部分。此外，XPath 遵循 [XSLT](https://developer.mozilla.org/en-US/docs/Web/XSLT) (可扩展样式表语言转换)标准，该标准通常用于导航 web 元素和属性。

DOM 对于浏览 HTML 文档是必不可少的。它就像一个包含所有 web 元素和您正在寻找的元素的地图。您可以使用适当的 web 定位器从 DOM 中找到所需的 WebElements。

### 不同类型的 XPath 定位器

有两种方法可以在 DOM 中定位所需的 WebElement。一个是通过绝对路径，另一个是通过相对路径。在 XPath 备忘单的这一部分，我们将研究使用 XPath 定位器在 DOM 中查找所需 WebElement 的不同方法。

#### 1.绝对 XPath

绝对路径指定从根元素到要使用的元素的完整路径。但是，使用绝对路径可能会遇到问题。如果在元素的路径中做了任何更改，就会导致 XPath 失败。

无论何时使用绝对路径，都必须使用单个正斜杠(/)开始 XPath。这表明您正在从文档的根节点中选择元素。

语法:

```
/html/body/div[x]/div[y]/
```

示例:

```
/html//div/div/div/div[1]/div/a/img
```

要定位一个元素，您可以右键单击 web 元素并单击 Inspect。然后您将看到 Elements 选项卡，您可以在其中编写定位器。在本例中，我们从 HTML 标记开始，一个接一个地遍历到 div，包含的标记一直到最终的 img 标记。

尽管这看起来很简单，但常见的缺点是，即使 DOM 结构中很小的变化也会导致几个自动化故障。

#### 2.相对 XPath

与绝对路径不同，相对 XPath 指的是我们希望在特定位置定位的元素。在这种情况下，元素相对于其实际位置进行定位。

要使用相对路径，必须在开头指定双正斜杠(//)。大多数情况下，相对 XPath 是 Selenium 自动化测试的首选。如果页面设计或 DOM 层次结构有任何变化，现有的 XPath 选择器不会受到影响。

语法:

| 

```
//tagname[@attribute='value']
```

 |

```
XPath Syntax
```

为了选择 HTML 文档中的节点，XPath 使用以下路径表达式:

```
XPath=//tagname[@Attribute="Value"]
```

![](img/8887f5e3d8a38bd1ee53380596fdc1d3.png)

下面是一些在 XML 文档中选择节点的常用路径表达式:

| **表达式/ XPath** | **描述** |
| 结节 | 选择名称为的所有元素 |
| / | 从根节点中选择 |
| // | 从当前元素中选择文档中与选择匹配的元素(无论它们在哪里) |
| 。 | 选择当前节点 |
| .. | 选择当前节点元素的父元素。 |
| @ | 选择属性 |

### XPath 表达式

XPath 表达式是用于选择一组节点并执行转换的模式。XPath 使用路径表达式从 XML 和 HTML 文档中选择节点。

**语法:**

```
//tagname[@attribute='value']
```

**举例:**

| 

```
<?xml version="1.0"standalone="yes"?>
<empinfo>
<employeeid="1">
<name>Opal Kole</name>
<designationdiscipline="web"experience="3 year">Senior Engineer</designation>
<email>OpalKole@myemail.com</email>
</employee>
<employeeid="2">
<namefrom="CA">Max Miller</name>
<designationdiscipline="DBA"experience="2 year">DBA Engineer</designation>
<email>maxmiller@email.com</email>
</employee>
<employeeid="3">
<name>Beccaa Moss</name>
<designationdiscipline="appdev">Application Developer</designation>
<email>beccaamoss@email.com</email>
</employee>
</empinfo>
```

 |

您将在下面找到轴和相应的步骤。

| 轴 | // | / |
| 步骤 | 保险商实验所 | 一个[@id='link'] |

#### 前缀表达式

我们可以在 XPath 表达式的开头使用前缀:

| **表情** | **例子** | **描述** |
| // | //p[@class='footer'] | 从 DOM 中的任意位置选择段落标签 |
| / | /a | 从给定节点中查找所有锚(a)标签 |
| / | /html/body/div | 从根元素开始查找所有 div |

以下是 XPath 中各种可用步骤的一些示例:

| **XPath** | **描述** |
| //div | 选择所有 div 标签 |
| //[@id=’btn’] | 选择 ID 为“btn”的所有元素 |
| //div[@name='post'] | 选择所有名为“post”的 div 元素 |
| //a/text() | 给出所有锚定标签的文本 |
| //a/@href | 给出定位标记的 href 值 |

### 需要更多帮助吗？检查本课程

[![xpath selium](img/c1b5ca4bb8a0944243f333fc07ca6a25.png)](https://imp.i384100.net/qn64Yb)

#### 选择节点

下表包括用于选择节点或 WebElements 的 XPath 表达式。

| **XPath** | **描述** |
| 差异 | 选择所有 div 元素 |
| /div | 从根元素中选择 div 元素 |
| 分区/tr | 选择作为 div 子元素的所有 tr 元素 |
| //tr | 选择文档中任意位置的所有 tr 元素 |
| div//tr | 在文档中任意位置选择 div 的所有子元素 tr |
| //@类 | 选择所有类别属性 |

#### 查找节点的谓词

可以在 XPath 中使用谓词来定位包含指定值的特定节点。它们被括在方括号中，如下表所示。

这些谓词标识符返回布尔值(真或假)。您甚至可以对它们使用关系运算符和布尔运算符。

| **XPath** | **描述** |
| /div/a[1 | 选择 div 元素中的第一个定位元素 |
| /div/a[last()] | 选择 div 元素中的最后一个定位元素 |
| /div/a[last()-1] | 选择 div 元素中倒数第二个定位元素 |
| /div/a[position()<3] | 选择 div 元素中的前两个定位元素 |
| //a[@class] | 选择所有具有类属性的锚元素 |
| //a[@class='btn'] | 选择具有类属性和值“btn”的所有锚元素 |
| /div/h1[1]a | 选择 h1 中作为 div 元素子元素的所有定位元素 |
| /div/h1/a[1] | 选择 div 元素中 h1 子元素的所有锚元素 |

例如:

| **表情** | **描述** |
| 元素名称[N] | 引用特定元素序列号(数组序列)的左方括号和右方括号。 |
| 员工信息/员工[2] | 子元素的第二个子元素；选择 empinfo 元素的第二个雇员。 |
| 雇员信息/雇员[2]/姓名 | 子元素序列；选择 empinfo 元素的第二个 employee 元素的 name 元素。 |
| 元素名称[@属性名称]empinfo/employee[@id] | 选择具有属性的元素选择具有给定 id 属性的所有 employee 元素。 |
| 元素名称[@属性名称=值]empinfo/employee[@id=2] | 选择具有指定属性值的元素；查找具有给定属性和值的雇员元素。仅匹配那些其属性和值在 XPath 表达式中指定的元素。 |
| empinfo/employee[@id=2][2] | 选择给定属性和值的所有雇员元素。最后，只选择第二个 employee 元素。 |
| empinfo/employee[1][@id=1] | 选择具有给定属性和值的第一个 employee 元素。 |
| //称号[@学科和@经验] | 选择具有给定的第一和第二两个属性的所有指定元素。 |
| //称号[@学科或@经验]//称号[@学科&#124; @经验] | 选择具有第一或第二属性的所有指定元素。 |

#### 链接顺序

XPath 的含义随着顺序的变化而变化。

例如:

a[1][@href='/']和

a[@href='/'][1]不同。

#### 索引

您必须在 XPath 中使用[]进行索引，其中[]包含一个数字，指定您想要选择的节点。还可以使用 XPath 中的索引函数，如 last()、position()等，来指定元素的索引。

例如:

| //a[1] | 选择第一个锚点标记 |
| //a[last()] | 选择最后一个锚点标签 |
| //ul/li[2] | 选择第二个 li 标签(ul 标签的子标签) |
| //ul/li[position()=2] | 选择第二个 li 标签，它是 ul 标签的子标签 |
| //ul/li[position()>1] | 选择不是 ul 标签的第一个子标签的 li 标签 |

#### 用于选择未知节点的表达式(通配符)

可以在 XPath 定位器中使用通配符来查找未知的 HTML 文档元素。

| * | 匹配任何 HTML 元素 |
| @* | 匹配元素的任何属性 |
| 节点() | 匹配任何类型的元素 |
| /div/* | 选择 div 元素的所有子元素 |
| //* | 选择 HTML 文档中的所有元素 |
| //a[@*] | 选择具有任何属性的所有锚元素 |
| 。 | 匹配任何 HTML 元素 |
| .. | 引用父上下文节点 |
| / | 指根节点 |
| // | 引用文档中任意位置的节点 |
| * | 指上下文节点的所有子元素 |
| &#124;或者 | 引用 OR 条件组合表达式第一个表达式或第二个表达式 |
| 和 | 指一个条件和组合表达式 |
| 文本() | 选择当前元素的所有文本节点子元素。 |

#### 选择多条路径的表达式

您可以在 XPath 表达式中使用“|”运算符来选择多条路径。以下是使用“|”运算符的方法:

| //div &#124; //a | 选择 HTML 文档中的所有 div 和锚元素 |
| //div/h1 &#124; //div/a | 选择 div 元素中的所有 h1 和锚元素 |

[XSLT XPATH 和 XQuery 基础知识](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fxslt-xpath-and-xquery-fundamentals%2F)

### XPath 轴

XPath 规范中有 13 个轴。这些轴表示上下文节点或引用节点之间的关系。XPath 中定义了 13 个轴，使您能够从当前上下文节点或根节点搜索 XML 文档中的不同节点部分。XPath 轴从文档内的上下文节点中选择节点。

轴示例和节点测试

AxesName ::= 'self '

| '孩子'

| '后裔'

| '自己的后代'

| '父级'

| '祖先'

| '祖先或自我'

| '属性'

| '跟随'

| '跟随-同级'

| '在前'

| '前置-同级'

|“命名空间”

*   自身:轴选择上下文节点。
*   子节点:轴选择上下文节点的子节点。
*   后代:轴选择上下文节点的所有后代，即任何级别深度的子节点。
*   descendant-or-self: Axes 选择上下文节点的所有后代，任何级别深度的子节点也为自己选择上下文节点。
*   parent:轴选择上下文节点的父节点。
*   祖先:轴选择上下文节点的所有父节点，直到根节点。
*   ancestor-or-self: Axes 选择上下文节点的所有父节点，直到根节点。此外，选择上下文节点本身。
*   属性:轴选择上下文节点的属性。
*   以下:轴选择上下文节点之后的所有节点，不包括属性节点或名称空间节点。
*   following-sibling:轴选择上下文节点的所有后续同级。如果上下文节点是空同级节点之后的属性节点或命名空间节点，则选择 none。
*   preceding:轴选择上下文节点之前的所有节点，不包括属性节点或名称空间节点。
*   previous-sibling:轴选择上下文节点的属性。
*   名称空间:轴选择上下文节点的所有名称空间节点。

语法:

| 

```
AxesName::node[predicate]
```

 |

```
Where:
```

*   谓词指定包含在[]中的节点序列。
*   轴名和节点由:::分隔。

示例:

```
<?xml version="1.0"standalone="yes"?>
<empinfo>
<employeeid="1">
<name>Opal Kole</name>
<designationdiscipline="web"experience="3 year">Senior Engineer</designation>
<email>OpalKole@myemail.com</email>
</employee>
<employeeid="2">
<namefrom="CA">Max Miller</name>
<designationdiscipline="DBA"experience="2 year">DBA Engineer</designation>
<email>maxmiller@email.com</email>
</employee>
<employeeid="3">
<name>Beccaa Moss</name>
<designationdiscipline="appdev">Application Developer</designation>
<email>beccaamoss@email.com</email>
</employee>
</empinfo>
```

### 节点测试

节点测试是 XPath 表达式的一部分，用于在 XML 文档中查找节点。

| **选择轴** | **描述** |
| //name/self::* | 选择名称上下文节点 |
| 孩子::* | 选择上下文节点的所有子节点。 |
| 子::节点() | 选择上下文节点的所有子节点 |
| 子级::empinfo | 选择 empinfo 节点的所有子元素 |
| //员工/后代::* | 选择雇员节点的所有后代 |
| //后代::员工 | 选择上下文节点中 employee 节点的所有后代。 |
| //员工/后代或自己::* | 选择 employee 节点和上下文节点本身的所有后代。 |
| //后代或自身::雇员 | 此轴选择 employee 节点及其上下文节点本身的所有后代。 |

#### 祖先

| //员工/祖先::* | 选择 employee 节点的所有祖先节点 |
| //祖先::名称 | 选择上下文节点中名称节点的所有祖先 |
| //员工/祖先或自己::* | 选择 employee 节点的所有祖先和上下文节点本身。 |
| //名称/祖先或自己::雇员 | 使用上下文节点本身选择名称节点的所有祖先 |
| //名称/父项::* | 选择名称上下文节点的父节点 |
| //姓名/父::员工 | 如果员工节点是上下文节点的父节点，则返回结果节点；否则找不到节点。 |
| //属性::id | 选择具有 id 属性的所有节点 |
| //属性::* | 选择具有任何属性的所有节点 |
| //员工[@ id = 1]/以下::* | 选择上下文节点之后的所有节点(及其子节点) |
| //employee[@ id = 1]/following-sibling::* | 选择上下文节点之后的所有同级节点 |
| //employee[@id=3]/preceding::* | 选择上下文节点之前的所有节点(及其子节点) |
| //employee[@ id = 3]/preceding-sibling::* | 选择上下文节点之前的所有同级节点 |

例如:

4.  <name>欧泊科尔</name>
5.  <designation discipline="web" experience="3 year">高级工程师</designation>
6.  <email>OpalKole@myemail.com</email>

9.  马克斯·米勒
10.  <designation discipline="DBA" experience="2 year">DBA 工程师</designation>
11.  <email>maxmiller@email.com</email>

14.  <name>Beccaa Moss</name>
15.  <designation discipline="appdev">应用开发者</designation>
16.  <email>beccaamoss@email.com</email>

其中:

*   //name/self::*(名称节点值- 4，9，14 行号)
*   子级::* (3 到 7 行、8 到 12 行、13 到 17 行)
*   child::node() name 节点值(4、9、14 行)。
*   child::empinfo 2 到 18 行。
*   /员工/后代::*4，5，6，9，10，11，14，15，16 行
*   //descendant::employee (3 到 7，8 到 12，13 到 17 行。)
*   //employee/descendant-or-self::*(4，5，6，8，9，10，11，13，14，15，16 行。)
*   //descendant-or-self::employee(3 到 7，8 到 12，13 到 17 行。)
*   //员工/祖先::* (2 到 18 行。)
*   //ancestor::name(名称节点值(4，9，14 行))。
*   //employee/ancestor-or-self::*(2，3，7，8，12，13，17，18 行(4 节点选择)。)
*   //name/ancestor-or-self::employee(3 到 7，8 到 12，13 到 17 行(3 个节点选择)。)
*   //名称/父::* (3 到 7，8 到 12，13 到 17 行(3 节点选择)。)
*   //name/parent::employee (3 到 7，8 到 12，13 到 17 行(3 节点选择)。)
*   //attribute::id (id 属性值(3，8，13 行)。)
*   //属性::* (3，5，8，9，10，13，15)
*   //employee[@ id = 1]/following::*(8 到 12，9，10，11，13 到 17，14，15，16 行(8 节点选择)。)
*   //employee[@ id = 1]/following-sibling::*(8 到 12，13 到 17 行(2 节点选择)。)
*   //employee[@ id = 3]/preceding::*(3 到 7，4，5，6，8 到 12，9，10，11 行(8 节点选择)。)
*   //employee[@ id = 3]/preceding-sibling::*(3 到 7，8 到 12 行(2 节点选择)。)

### XPath 运算符

XPath 表达式可以返回数字、布尔值(true 或 false)、节点集(div、a、li)或字符串。可以使用各种运算符来操作 XPath 表达式返回的值。

以下是 XPath 表达式中使用的各种运算符:

| **操作员** | **描述** |
| &#124; | 计算两个节点集。 |
| + | 加法算子 |
| - | 减法运算符 |
| * | 乘法运算符 |
| 差异 | 除法算符 |
| = | 相等运算符 |
| ！= | 不等运算符 |
| < | 小于运算符 |
| <= | 小于或等于运算符 |
| > | 大于运算符 |
| >= | 大于或等于运算符 |
| 或者 | Or 运算符 |
| 和 | 逻辑积算符 |
| 现代的 | 模数(除法余数) |

下面列出了五种不同类型的 XPath 运算符:

*   比较运算符
*   布尔运算符
*   数字运算符或函数
*   字符串函数
*   节点运算符或函数

#### 比较运算符

比较运算符比较两个不同的值。以下是 XPath 表达式中使用的各种比较运算符的示例:

| **操作员** | **描述** |
| = | 指定等于 |
| ！= | 指定不等于 |
| < | 指定小于 |
| > | 指定大于 |
| <= | 指定小于或等于 |
| >= | 指定大于或等于 |

在下面的例子中，我们通过迭代每个雇员来创建一个包含属性 id 和子元素<firstname>、<lastname>、<nickname>和<salary>的元素表。它检查薪金是否大于(>)25000，然后打印详细信息。</salary></nickname></lastname></firstname>

Employee.xml

```
<?xml version ="1.0"?>
<?xml-stylesheet type ="text/xsl"href ="employee.xsl"?>
<class>
<employeeid="001">
<firstname>Abhiram</firstname>
<lastname>Kushwaha</lastname>
<nickname>Manoj</nickname>
<salary>15000</salary>
</employee>
<employeeid="002">
<firstname>Akash</firstname>
<lastname>Singh</lastname>
<nickname>Bunty</nickname>
<salary>25000</salary>
</employee>
<employeeid="003">
<firstname>Brijesh</firstname>
<lastname>Kaushik</lastname>
<nickname>Ballu</nickname>
<salary>20000</salary>
</employee>
<employeeid="004">
<firstname>Zoya</firstname>
<lastname>Mansoori</lastname>
<nickname>Sonam</nickname>
<salary>30000</salary>
</employee>
</class>
```

雇员. xsl

```
<?xml version ="1.0"encoding ="UTF-8"?>
<xsl:stylesheetversion="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:templatematch="/">
<html>
<body>
<h2>Employee</h2>
<tableborder="1">
<trbgcolor="pink">
<th>ID</th>
<th>First Name</th>
<th>Last Name</th>
<th>Nick Name</th>
<th>Salary</th>
</tr>
<xsl:for-eachselect="class/employee">
<xsl:iftest="salary > 25000">
<tr>
<td><xsl:value-ofselect="@id"/></td>
<td><xsl:value-ofselect="firstname"/></td>
<td><xsl:value-ofselect="lastname"/></td>
<td><xsl:value-ofselect="nickname"/></td>
<td><xsl:value-ofselect="salary"/></td>
</tr>
</xsl:if>
</xsl:for-each>
</table>
</body>
</html>
</xsl:template>
</xsl:stylesheet>
```

```
<?xml version ="1.0"encoding ="UTF-8"?>
<xsl:stylesheetversion="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:templatematch="/">
<html>
<body>
<h2>Employee</h2>
<tableborder="1">
<trbgcolor="pink">
<th>ID</th>
<th>First Name</th>
<th>Last Name</th>
<th>Nick Name</th>
<th>Salary</th>
</tr>
<xsl:for-eachselect="class/employee">
<xsl:iftest="salary > 25000">
<tr>
<td><xsl:value-ofselect="@id"/></td>
<td><xsl:value-ofselect="firstname"/></td>
<td><xsl:value-ofselect="lastname"/></td>
<td><xsl:value-ofselect="nickname"/></td>
<td><xsl:value-ofselect="salary"/></td>
</tr>
</xsl:if>
</xsl:for-each>
</table>
</body>
</html>
</xsl:template>
</xsl:stylesheet>
```

#### 布尔运算符

这种类型的运算符返回 true 或 false 作为结果。以下是 XPath 中不同的布尔运算符:

| **操作员** | **描述** |
| 和 | 指定的两个条件都必须满足 |
| 或者 | 指定的任何一个条件都必须满足 |
| 不是() | 指定了检查不满足条件的函数 |

在这个例子中，我们创建了一个元素表，它包含属性 id 和子元素<firstname>、<lastname>、<nickname>和<salary>。该示例检查 id 是 001 还是 003，然后打印详细信息。</salary></nickname></lastname></firstname>

Employee.xml

```
<?xml version ="1.0"?>
<?xml-stylesheet type ="text/xsl"href ="employee.xsl"?>
<class>
<employeeid="001">
<firstname>Abhiram</firstname>
<lastname>Kushwaha</lastname>
<nickname>Manoj</nickname>
<salary>15000</salary>
</employee>
<employeeid="002">
<firstname>Akash</firstname>
<lastname>Singh</lastname>
<nickname>Bunty</nickname>
<salary>25000</salary>
</employee>
<employeeid="003">
<firstname>Brijesh</firstname>
<lastname>Kaushik</lastname>
<nickname>Ballu</nickname>
<salary>20000</salary>
</employee>
<employeeid="004">
<firstname>Zoya</firstname>
<lastname>Mansoori</lastname>
<nickname>Sonam</nickname>
<salary>30000</salary>
</employee>
</class>
```

雇员. xsl

```
<?xml version ="1.0"encoding ="UTF-8"?>
<xsl:stylesheetversion="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:templatematch="/">
<html>
<body>
<h2>Employee</h2>
<tableborder="1">
<trbgcolor="pink">
<th>ID</th>
<th>First Name</th>
<th>Last Name</th>
<th>Nick Name</th>
<th>Salary</th>
</tr>
<xsl:for-eachselect="class/employee[(@id = 001) or ((@id = 003))]">
<tr>
<td><xsl:value-ofselect="@id"/></td>
<td><xsl:value-ofselect="firstname"/></td>
<td><xsl:value-ofselect="lastname"/></td>
<td><xsl:value-ofselect="nickname"/></td>
<td><xsl:value-ofselect="salary"/></td>
</tr>
</xsl:for-each>
</table>
</body>
</html>
</xsl:template>
</xsl:stylesheet>
```

#### 数字运算符和函数

下面描述了可以在 Xpath 表达式中使用的各种数字运算符:

| **操作员** | **描述** |
| + | 加法运算 |
| - | 减法运算 |
| * | 乘法运算 |
| 差异 | 除法运算 |
| 现代的 | 模运算 |

以下是一些可以在 XPath 表达式上执行的函数:

| **功能** | **描述** |
| 天花板() | 返回大于所提供值的最小整数 |
| 地板() | 返回小于所提供值的最大整数 |
| 圆形() | 将舍入值返回到最接近的整数 |
| 总和() | 返回两个数的和 |

在这个例子中，我们创建了一个包含<employee>元素及其属性 id 和子元素<firstname>、<lastname>、<nickname>和<salary>的表。它计算雇员的工资，然后显示结果。</salary></nickname></lastname></firstname></employee>

Employee.xml

```
<?xml version ="1.0"?>
<?xml-stylesheet type ="text/xsl"href ="employee.xsl"?>
<class>
<employeeid="001">
<firstname>Abhiram</firstname>
<lastname>Kushwaha</lastname>
<nickname>Manoj</nickname>
<salary>15000</salary>
</employee>
<employeeid="002">
<firstname>Akash</firstname>
<lastname>Singh</lastname>
<nickname>Bunty</nickname>
<salary>25000</salary>
</employee>
<employeeid="003">
<firstname>Brijesh</firstname>
<lastname>Kaushik</lastname>
<nickname>Ballu</nickname>
<salary>20000</salary>
</employee>
<employeeid="004">
<firstname>Zoya</firstname>
<lastname>Mansoori</lastname>
<nickname>Sonam</nickname>
<salary>30000</salary>
</employee>
</class>
```

雇员. xsl

```
<?xml version ="1.0"encoding ="UTF-8"?>
<xsl:stylesheetversion="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:templatematch="/">
<html>
<body>
<h2>Employee</h2>
<tableborder="1">
<trbgcolor="pink">
<th>ID</th>
<th>First Name</th>
<th>Last Name</th>
<th>Nick Name</th>
<th>Salary</th>
<th>Grade</th>
</tr>
<xsl:for-eachselect="class/employee">
<tr>
<td><xsl:value-ofselect="@id"/></td>
<td><xsl:value-ofselect="firstname"/></td>
<td><xsl:value-ofselect="lastname"/></td>
<td><xsl:value-ofselect="nickname"/></td>
<td><xsl:value-ofselect="salary"/></td>
<td>
<xsl:choose>
<xsl:whentest="salary div 25000 > 1">
High
</xsl:when>
<xsl:whentest="salary div 20000 > 1">
Medium
</xsl:when>
<xsl:otherwise>
Low
</xsl:otherwise>
</xsl:choose>
</td>
</tr>
</xsl:for-each>
</table>
</body>
</html>
</xsl:template>
</xsl:stylesheet>
```

#### 字符串函数

以下是帮助您执行 XPath 表达式任务的各种字符串函数:

*   starts-with(string1，string2):当第一个字符串以第二个字符串开头时，返回 true
*   contains(string1，string2):当第一个字符串包含第二个字符串时，返回 true
*   子串(字符串，偏移量，长度？):结果得到字符串的一部分。该部分从偏移处开始，直到提供的长度。
*   substring-before(string1，string2):该函数返回第一次出现 string2 之前的 string1 部分。
*   substring-after(string1，string2):返回第一次出现 string2 之后的 string1 部分。
*   string-length(string):这个函数返回字符串的字符长度。
*   normalize-space(string):你可以用这个函数来修剪字符串的前导和尾随空格。
*   translate(string1，string2，string3):在 string2 中的任何匹配字符被 string3 中的字符替换后，它返回 string1。
*   concat(string1，string2，...):您可以使用此函数组合所有字符串。
*   format-number(number1，string1，string2):在将 string1 作为格式字符串应用后，它返回 number1 的格式化版本。String2 是可选的区域设置字符串。

在这个例子中，我们通过迭代每个雇员来创建一个包含<employee>元素的表，其中包含这些元素的名称和名称长度。它在连接名字和姓氏后计算雇员姓名的长度，然后显示雇员的详细信息。</employee>

Example.xml

```
<?xml version ="1.0"?>
<?xml-stylesheet type ="text/xsl"href ="employee.xsl"?>
<class>
<employeeid="001">
<firstname>Abhiram</firstname>
<lastname>Kushwaha</lastname>
<nickname>Manoj</nickname>
<salary>15000</salary>
</employee>
<employeeid="002">
<firstname>Akash</firstname>
<lastname>Singh</lastname>
<nickname>Bunty</nickname>
<salary>25000</salary>
</employee>
<employeeid="003">
<firstname>Brijesh</firstname>
<lastname>Kaushik</lastname>
<nickname>Ballu</nickname>
<salary>20000</salary>
</employee>
<employeeid="004">
<firstname>Zoya</firstname>
<lastname>Mansoori</lastname>
<nickname>Sonam</nickname>
<salary>30000</salary>
</employee>
</class>
```

示例. xsl

```
<?xml version ="1.0"encoding ="UTF-8"?>
<xsl:stylesheetversion="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:templatematch="/">
<html>
<body>
<h2>Employee</h2>
<tableborder="1">
<trbgcolor="pink">
<th>Name</th>
<th>Length of Name</th>
</tr>
<xsl:for-eachselect="class/employee">
<tr>
<td><xsl:value-ofselect="concat(firstname,' ',lastname)"/></td>
<td><xsl:value-ofselect="string-length(concat(firstname,' ',lastname))"/></td>
</tr>
</xsl:for-each>
</table>
</body>
</html>
</xsl:template>
</xsl:stylesheet>
```

### 节点功能

下表突出显示了各种节点运算符及其说明:

| **操作员** | **描述** |
| / | 选择特定节点下的节点。 |
| // | 从根节点中选择节点。 |
| [...] | 检查节点值。 |
| &#124; | 统一两个节点集。 |

以下是 XPath 表达式中使用的节点函数列表。

| **功能** | **描述** |
| 节点() | 选择所有类型的节点 |
| 处理指令() | 选择处理指令的节点 |
| 文本() | 选择一个文本节点 |
| 名称() | 提供节点名称 |
| 位置() | 提供节点位置 |
| 最后一个() | 选择相对于当前节点的最后一个节点 |
| 评论 | 选择作为注释的节点 |

在这个例子中，我们通过迭代每个雇员来创建一个包含<employee>元素及其详细信息的表。它计算学生节点的位置，然后显示带有序列号的雇员详细信息。</employee>

雇员. xml:

```
<?xml version ="1.0"?>
<?xml-stylesheet type ="text/xsl"href ="employee.xsl"?>
<class>
<employeeid="001">
<firstname>Abhiram</firstname>
<lastname>Kushwaha</lastname>
<nickname>Manoj</nickname>
<salary>15000</salary>
</employee>
<employeeid="002">
<firstname>Akash</firstname>
<lastname>Singh</lastname>
<nickname>Bunty</nickname>
<salary>25000</salary>
</employee>
<employeeid="003">
<firstname>Brijesh</firstname>
<lastname>Kaushik</lastname>
<nickname>Ballu</nickname>
<salary>20000</salary>
</employee>
<employeeid="004">
<firstname>Zoya</firstname>
<lastname>Mansoori</lastname>
<nickname>Sonam</nickname>
<salary>30000</salary>
</employee>
</class>
```

雇员. xsl:

```
<?xml version ="1.0"encoding ="UTF-8"?>
<xsl:stylesheetversion="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:templatematch="/">
<html>
<body>
<h2>Employee</h2>
<tableborder="1">
<trbgcolor="pink">
<th>Serial No</th>
<th>ID</th>
<th>First Name</th>
<th>Last Name</th>
<th>Nick Name</th>
<th>Salary</th>
</tr>
<xsl:for-eachselect="class/employee">
<tr>
<td><xsl:value-ofselect="position()"/></td>
<td><xsl:value-ofselect="@id"/></td>
<td><xsl:value-ofselect="firstname"/></td>
<td><xsl:value-ofselect="lastname"/></td>
<td><xsl:value-ofselect="nickname"/></td>
<td><xsl:value-ofselect="salary"/></td>
</tr>
</xsl:for-each>
</table>
</body>
</html>
</xsl:template>
</xsl:stylesheet>
```

### XPath 选择器

借助 XPath 选择器，您可以只选择 HTML 文档中由 XPath 元素指定的特定部分。XPath 有许多不同类型的 selectos。

#### 后代选择器

后代选择器代表当前节点的所有子节点，以及每个子节点的所有子节点，等等。这些选择器不包括属性和名称空间节点。属性节点的父节点是其元素节点，而属性节点不是其父节点的后代。

| 差异 | //div | 选择所有 div 元素 |
| 部门 h1 | //div//h1 | 选择 div 元素中的所有 h1 |
| ul > li | //ul/li | 选择作为 ul 子元素的所有 li 元素 |
| 一个 | /div/p/a | 选择 div 元素的段落标记内的所有锚点标记 |
| div > * | //div/* | 选择 div 标签中的所有元素 |
| :根 | / | 选择 DOM 的根元素 |
| :根>正文 | /body | 选择正文标签 |

#### 属性选择器

XPath 属性选择器根据给定属性的存在或值来匹配元素。

| **元素** | **Xpath** | **描述** |
| #id | //*[@id="id"] | 选择具有匹配 ID 属性的所有元素 |
| 。班级 | //*[@class="class"] | 选择具有匹配类属性的所有元素 |
| [rel] | //和[@ with] | 选择所有具有 rel 属性的锚点标记。 |
| a[href^='/'] | //a[以(@href，'/')开头] | 选择 href 以“/”开头的所有锚点标记 |
| a[href$='txt'] | //a[以(@href，')结尾。txt')] | 选择所有 href 以'结尾的锚点标记。'文本' |
| a[rel~='details'] | //a[包含(@rel，' details')] | 选择所有具有相关值“详细信息”的锚点标记 |
| 输入[type="password"] | //input[@type="password"] | 选择所有密码类型的输入标签 |
| a#btn[for="XYZ"] | //a[@id="btn"][@for="XYZ"] | 选择“BTN”ID 与 XYZ 链接的所有锚定标签 |

#### 订单选择器

可以在 XPath 中使用顺序选择器来检索列表元素。

| **元素** | **XPath** | **描述** |
| ul >李:一流 | //ul/li[1] | 选择作为 ul 子标签的第一个 li 标签 |
| ul > li:第 n 种类型(2) | //ul/li[2] | 选择第二个 li 标签，它是 ul 的子标签 |
| li#id:第一款 | //李[1][@id="id"] | 选择 id 值为“id”的第一个 li |
| ul >李:最新型 | //ul/li[last()] | 选择 ul 的子级的最后一个 li |
| 答:第一胎 | //*[1][name()="a"] | 选择锚点标签的第一个子标签 |
| 答:最后一个孩子 | //*[last()][name()="a"] | 选择锚点标签的最后一个子标签 |

#### 同科

在 Selenium WebDriver 中，可以检索作为父元素同级的 WebElement。以下是如何在 Selenium WebDriver 中使用同级获取元素:

| **元素** | **XPath** | **描述** |
| h1 ~ ul | //h1/following-sibling::ul | 选择 h1 标签同级之后的所有 ul 标签 |
| h1 ~ #id | //h1/following-sibling::[@ id = " id "] | 选择所有 id 值为“ID”的元素，它们是 h1 的同级元素 |
| h1 + ul | //h1/following-sibling::ul[1] | 选择 h1 同级之后的第一个 ul 标签 |

#### 不同的操作员

XPathto 中还有其他操作符来定位元素:

| **操作员** | **XPath** | **描述** |
| 非运算符 | //p[not(@id)] | 选择属性与 id 不匹配的所有段落标签 |
| 文本匹配 | //button[text()="Submit"] | 选择带有文本输入“提交”的按钮 |
| 文本匹配(子字符串) | //button[contains(text()，" pass")] | 选择包含字符串“pass”的按钮 |
| 算术 | //产品[@price > 3] | 选择值大于 3 的价格 |
| 有孩子 | //ul[*] | 如果有子代，请选择带有任意数字(或类型)的 ul |
| 有孩子(特定) | //ul[li] | 选择带有任何数字和 li 标签的 ul 作为子标签 |
| 逻辑 | //a[@name 或@href] | 选择具有名称和 href 属性的所有锚点标记 |
| 联合(连接结果) | //a &#124; //div | a 和 div 标记的联合 |

#### 上下文选择器

| **定位器** | **描述** |
| //img | 图像元素 |
| //img/*[1] | 元素 img 的第一个子元素 |
| //ul/child::李 | ul 的第一个孩子 li |
| //img[1] | 第一个 img 孩子 |
| //img/*[last()] | 元素 img 的最后一个子元素 |
| //img[last()] | 最后一个 img 子代 |
| //img[last()-1] | 倒数第二个 img 子代 |
| //ul[*] | 有孩子的人 |

#### 属性选择器

| **定位器** | **描述** |
| //img[@id='myId'] | @id= 'myId '的图像元素 |
| //img[@id！='myId'] | @id 不等于“myId”的图像元素 |
| //img[@name] | 具有名称属性的图像元素 |
| //*[包含(@id，' Id')] | 包含@id 的元素 |
| //*[以(@id，' id '))开头] | 以@id 开头的元素 |
| //*[以(@id，' id '))结尾] | 以@id 结尾的元素 |
| //*[匹配(@id，' r')] | @id 与正则表达式“r”匹配的元素 |
| //*[@name='myName'] | @name= 'myName '的图像元素 |
| //*[@id='X '或@name='X'] | 具有@id X 或名称 X 的元素 |
| //*[@name="N"][@value="v"] | 具有@name N 和指定@value 'v '的元素 |
| //*[@name="N" and @value="v"] | 具有@name N 和指定@value 'v '的元素 |
| //*[@ name = " N " and not(@ value = " v ")] | @name 为 N 的元素&未指定@value 'v ' |
| //input[@type="submit"] | 提交类型的输入 |
| //a[@href="url"] | 带有目标链接的锚点' url ' |
| //section[//h1[@id='hi']] | 如果它有一个@id= 'hi '的

# 后代，则返回

 |
| //*[@ id = " test table "]//tr[3]//TD[2] | 按行和列的单元格 |
| //输入[@checked] | 选中的复选框(或单选按钮) |
| //a[@disabled] | 所有被禁用的“a”元素 |
| //a[@price > 2.50] | ' a '价格> 2.5 英镑 |

### XPath 方法

以下是一些不同的 XPath 方法:

| **定位器** | **解释** |
| //table[count(tr) > 1] | 返回多于一行的表格 |
| //*[.="t"] | 恰好包含文本“t”的元素 |
| //a[contains(text()，" Log Out")] | 内部文本包含“注销”的锚点 |
| //a[not(contains(text()，" Log Out))] | 内部文本不包含“注销”的锚点 |
| //a[not(@disabled)] | 所有未禁用的“a”元素 |

#### 数学方法

| **定位器** | **解释** |
| 上限(数量) | 计算一个小数，并返回大于或等于该小数的小整数 |
| 楼层(编号) | 计算一个小数，并返回小于或等于该小数的大整数 |
| 四舍五入(十进制) | 返回与给定数字最接近的整数 |
| 总和(节点集) | 返回给定节点集中每个节点的数值之和 |

#### 字符串方法

| **定位器** | **解释** |
| 包含(空间字符串，行星字符串) | 确定第一个参数字符串是否包含第二个参数字符串，并返回布尔值 true 或 false |
| concat(string1, string2 [stringn]*) | 连接两个或多个字符串并返回结果字符串 |
| 规范化-空格(字符串) | 从字符串中去除前导和尾随空白；用一个空格替换空白字符序列；返回结果字符串 |
| 开头为(spacetrack，space) | 检查第一个字符串是否以第二个字符串开始，并返回 true 或 false |
| 字符串长度([字符串]) | 返回一个等于给定字符串中字符数的数字 |
| 子字符串(字符串，开始[长度]) | 返回给定字符串的一部分 |
| 子串-after(spacetrack，track) | 返回给定子串之后给定字符串的剩余部分 |
| 子串-before(spacetrack，tra) | 返回给定子串之前给定字符串的剩余部分 |
| 翻译(字符串，ghj，GHJ) | 计算要翻译的字符串和一组字符，并返回翻译后的字符串 |

## 使用 JQuery 获取 XPath

JQuery 支持所有基本类型的 XPath 表达式。在我们的 XPath 备忘单的下一部分中列出了主要的错误！

| JQuery XPath | XPath | 描述 |
| $('ul > li ')。父级() | //ul/li/.. | 选择作为 li 标签父级的所有 ul 元素 |
| $('李')。最近的(“部分”) | //李/祖先或自己::节 | 选择所有具有 href 属性的锚点标签 |
| $('p ')。文本() | //p/text() | 选择段落标签中的文本 |

## 结论

我们已经到了 XPath 备忘单的末尾。XPath 是 Selenium 中常用的 web 定位器。但是要获得高效的 XPath，必须依赖于文档的结构和 WebElement 的当前位置。

在这篇详尽的 Selenium web locator 备忘单中，我们涵盖了 XPath 定位器的所有主要方面。需要时，将它放在身边，让您的工作更上一层楼。

有兴趣了解更多关于 Selenium WebDriver 的知识并找到一个附带的 Selenium 备忘单吗？查看我们的 [Selenium WebDriver 指南](https://hackr.io/blog/what-is-selenium-webdriver)。

## 常见问题

#### 1.什么是 XPath 示例？

想象一个有很多书的书店。每本书都有不同的书名、作者、价格、出版年份和内容——所有的信息都储存在书店的电脑里。数据从书店的计算机传输到我们的计算机的一种方式是通过 XML 文件。XML 文件包含数据，如下所示:

```
<?xml version='1.0'?>

<bookstore>

<category>Cooking</Category>

<language>Chinese</language>

<title>Chinese Noodles</title>

<author>Chen Li</author>

<year>2010</year>

<price>$12.99</price>

</bookstore>
```

注意，第一行说明了 XML 版本。如果您查看 XML 文件，它的结构类似于一个文件柜。文件柜的名字是书店。文件柜包含不同的文件或不同的信息——类别、语言、标题、作者、年份、价格等。

书店被称为根元素或根节点，因为所有其他信息都在书店内。根节点中的每条信息都称为一个节点。节点是标签< >和 >之间的名称。

在这个 XML 文件中，根节点是书店。这些节点是类别、语言、标题、作者、年份和价格。

#### 2.查找 XPath 最简单的方法是什么？

下面是如何用最简单的方法找到 XPath:

*   转到名字选项卡，右键单击>>检查。
*   您将看到一个输入标签和类似 classandid 的属性。
*   使用 id 和属性来构造 XPath，该 XPath 将定位名字字段。

#### 3.正确的 XPath 语法是什么？

XPath 包含位于网页上的元素路径。创建 XPath 的标准 XPath 语法是:

```
Xpath=//tagname[@attribute='value']
```

//:选择当前节点。

标记名:特定节点的标记名。

@:选择属性。

属性:节点的属性名。

值:属性的值。

#### 4.如何在 HTML 中获取 XPath？

如果你使用 Chrome 为 HTML 元素寻找 XPath，你不需要安装任何扩展。

1.  在 Chrome 中打开想要检查的网站。按 F12 打开网站检查器，它将出现在窗口的右侧。

2.  点按元素检查器按钮。您可以在网站检查器面板的左上角找到它。这个按钮看起来像一个有鼠标指针指向的盒子。

3.  单击网站上要检查的元素。当您将光标移动到站点的元素上时，您会看到这些元素高亮显示。

4.  右键单击检查器面板中突出显示的代码。当您使用检查器点按某个元素时，相关代码将在窗口底部的检查器面板中自动高亮显示。

5.  右键单击突出显示的代码。选择“复制”= >“复制 XPath”这将把元素的 XPath 信息复制到剪贴板。

注意:这只是复制了最少的 XPath 信息。Firefox 的 Firebug 可以提供完整的 XPath 信息。