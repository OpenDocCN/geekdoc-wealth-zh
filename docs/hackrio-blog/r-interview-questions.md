# 2023 年前 50 R 面试问答[更新]

> 原文：<https://hackr.io/blog/r-interview-questions>

r 编程语言用于**统计分析**，图形表示和报告。r 在 GNU 通用公共许可证(GNU GPL)下免费提供。GNU GPL 允许最终用户自由运行、共享和使用软件。r 编程语言用于回归分析、预测建模、概率估计、数据挖掘领域，进一步帮助进行[数据分析](https://hackr.io/blog/what-is-data-analysis-methods-techniques-tools)。这篇文章将让你用下面列出的最好的**面试问题和答案为即将到来的面试做准备。**

## 前 R 名面试问答

R 编程语言的特点:

1.  r 是用来处理大量数据和存储的设施。
2.  在处理数据的统计分析和图形表示时，r 非常方便。
3.  r 提供了大量的操作符来执行数组、列表、向量和度量的计算。

这里有一个面试问题列表，可以帮助你准备面试，并在数据科学领域找到一份工作。

#### **问题:**R 中的数据结构是什么，有助于统计分析和图形化表示？

**答案:**以下是 R 中的数据结构，应用广泛:

1.  排列
2.  [数]矩阵
3.  矢量
4.  数据帧
5.  目录
6.  桌子

#### **问题:**如何用 R 打印东西？<练习 R 基本语法>

**回答:**写东西，R 用**打印**命令。

```
>string_variable_name <- “R is an analytical language”
>print(string_variable_name)
```

#### **问题:**什么是 class()函数 R？

**答:**R 中的这个函数是一个字符向量，给出了对象继承的类的名字。

**举例:**

```
>x <- 1:10
>class(x)
[1] “integer”
```

#### **问题:**什么是矢量？

**答案:**向量是同一主类型的数据元素序列。向量中的成员称为分量。

举例。

```
>vector_example <- c(2,3,4,5)
> print(vector_example)
[1] 2,3,4,5
>print (length(vector_example)
[1] 4
```

#### **问题:**如何对向量进行算术运算？用一些例子来说明

**回答:**R 中使用了很多算术运算符，记住，R 是一个组件一个组件地使用运算符。我们用一些标准运算符来看一下。

```
>x <- c(1,2,3,4)
> y <- c(4,5,6,7)
> x+y
[1] 5 7 9 11
> x-y
[1] -3 -3 -3 -3
> z <- (4,4,4,4,4,4,4)
> x+z
[1] 5 6 7 8 5 6 7
```

当我们有两个长度不等的向量，并且我们需要对两个向量都进行操作时，那么较短的向量会被反复使用来匹配两个向量的长度。

#### **问题:**在 Vector 中定义索引。

**答:**向量中的 Index 用来给出向量那个位置的元素。少数[编程语言](https://hackr.io/blog/best-programming-languages-to-learn)从 0 开始索引，其他的从 1 开始。r 从 1 开始计算索引。在输入索引号时有许多可能性，即

**1。正值和范围内指数**

```
> x<- (1,3,4,5)
> x[2]
[1] “3”
```

**2。超出范围**

```
>x <- (2,3,4,5)
> x[110]
[1] NA
```

**3。负索引-删除此元素并回复所有剩余的数字。**

```
> x <- (3,4,5,6,7)
> x[-3]
[1] “3” “4” “6” “7”
```

**4。数值范围**

```
>x <- (3,4,5,6,7,8)
> x[2:5]
[1] “4” “5” “6” “7”
```

**5。重复索引**

```
>x <- (3,4,5,6,7)
>s[c(2,1,2,3)]
[1] “4” “3” “4” “5”
```

**6。逻辑索引**

如果我们要选择一组特定的索引号，那么就应该使用逻辑运算符即 TRUE 和 FALSE

```
> x <- (2,3,4,5,6)
> s[c(TRUE, FALSE, FALSE, TRUE, TRUE)
[1] “2” “5” “6”
```

#### **问题:**什么是列表？

**答案:**一个列表，顾名思义就是几个向量集合在一起。假设你有一个数字向量，一个字符向量，一个布尔向量和一些数字。我们想把它合二为一，显然不会有相同的数据类型。所以我们需要创建一个列表。

```
> n = c(2,3,5)
> s = c (“a”, “b”, “c”, “d”, “e”)
> b= c(TRUE, FALSE, TRUE, FALSE, FALSE)
> x = list (n, s, b, 3)
> print(x)
[[1]]
[1] 2 3 5
[[2]]
[1] “a” “b” “c” “d” “e”
[[3]]
[1] TRUE FALSE TRUE FALSE FALSE
[[4]]
[1] 3
```

#### **问题:**什么是矩阵？

**答案:**矩阵是二维矩形数据集。它可以使用矩阵函数的向量输入来创建。

举例。

```
# Matrix creation
> M = matrix(c(1,2,3,4,5,6), nrow=2, ncol=3, by-row =TRUE)
print(M)
[1] [2] [3]
[1] 1 2 3
[1] 4 5 6
Where
nrow = number of rows in the matrix
ncol = number of columns in the matrix
byrow = TRUE/FALSE will get value first by row or column.
```

#### **问题:**什么是数组？

**答案:**数组是矩阵的超集。一方面，矩阵可以是二维的，但是阵列可以是任意维数的。

举例。

```
> a<- array(c(“car”, “bike”), dim (3,3,2))
> print (a)
, , 1
[,1] [,2] [,3]
[1,] “car” “bike” “car”
[2,] “bike” “car” “bike”
[3,] “car” “bike” “car”
, , 2
[,1] [,2] [,3]
[1,] “bike” “car” “bike”
[2,] “car” “bike” “car”
[3,] “bike” “car” “bike”
>my_array <- array(1:24, dim = c(3,4,2))
< my_array
, , 1
[,1] [,2] [,3] [,4]
[1,] 1 4 7 10
[2,] 2 5 8 11
[3,] 3 6 9 12
, , 2
[,1] [,2] [,3] [,4]
[1,] 13 16 19 22
[2,] 14 17 20 23
[3,] 15 18 21 24
```

#### **问题:**因子是什么？

**答:**因素是使用矢量创建的 r 对象。R 中的因子存储为一个整数值向量，并带有一组相应的字符值，以便在显示因子时使用。因子函数用于创建因子。factor 唯一需要的参数是一个向量值，它将作为因子值的向量返回。它存储向量以及向量标签中元素的不同值。

因子是使用 factor()函数创建的。nlevels 函数给出了级别的计数。

举例。

```
#First let’s create a vector
>vector_example <- c(‘a’, ‘b’, ‘c’, ‘a’, ‘a’)
#Now create a factor object
>factor_example <- factor(vector_example)
>print(factor_example)
[1] a b c a a
>print(nlevels(factor_example))
[1] 3
```

nlevels 给出了向量中不同值的数量。

#### **问题:**矩阵和数组有什么区别？

**答:**矩阵只能有二维，而数组可以有任意多个维度。借助于数据、行数、列数以及元素是按行还是按列放置来定义矩阵。

在 array 中，需要给出数组的维数。数组可以有任意多个维度，每个维度都是一个矩阵。例如，3x3x2 数组表示两个矩阵，每个矩阵的维数为 3x3。

#### **问题:**什么是数据帧？

**答案:****数据帧是一列等长的向量。它可以由任何特定类型的向量组成，并可以将其合并为一个向量。因此，一个数据帧可以有一个逻辑向量和一个数值向量。唯一的条件是所有的向量应该有相同的长度。**

 **举例。

```
#This is how the data frame is created
> student_profile <- data.frame(
Name <-c(“Ray”, “Green”, “Justin”)
Age <- c(22,23,24)
Class <- c(6,7,8)
)
print(stuent_profile)
```

上面的代码将创建三列，列名分别为 name、age 和 class。

#### **问题:**矩阵和数据框有什么区别？

**答案:**一个数据帧可以包含不同输入的向量，一个矩阵不能。我们可以有一个由字符、整数甚至其他数据组成的数据框架，但是你不能用矩阵来实现，因为矩阵必须是相同的类型。

因此，数据帧可以有不同的字符、数字和逻辑向量。

但是，对于矩阵，我们只需要一种数据类型。

#### **问题:**如何在 R 中读取用户的输入？

**答案:**

```
Readinteger <- function()
{
n <- readline(prompt = “Enter an integer: “)
return(as.integer(n))
}
print(readinteger())
```

Readline 允许用户在 r 中输入一行字符串。

提示参数打印在用户的屏幕上。

#### **问题:**写一个函数求一个数的平方

**答案:**

```
Square <- function(x) {
return(x^2)
}
print(Square(4))
```

#### **问题:**用 R 写一个倒计时函数？

**答案:**

```
timer <- function(time)
{
print(time)
while(time!-0)
{
Sys.sleep(!)
Time <- time -1
print(time)
}
}
countdown(5)
[1] 5
[2] 4
[3] 3
[2] 2
[1] 1
```

#### **问题:**如何在 R 中使用 mode 函数？

**答案:**众数是一组数据中出现次数最多的值。与平均值和中值不同，该模式可以包含数字和字符数据。

r 没有标准的内置函数来计算模式。所以我们创建一个用户函数来计算 r 中一个数据集的模，这个函数把向量作为输入，把模值作为输出。

举例。

```
#Create the function
getmode <- function(v){
uniqv <- unique(v)
uniqv[which.max(tabulate(match(v,uniqv)))]
}
#Create the vector with numbers.
v <- c(2,1,2,3,1,2,3,4,1,5,5,3,2,3)
#Calculate the mode using the user function
result <- getmode(v)
print(result)
[1] 2
#Create the vector with characters
charv <- c(“o”, “it”, “the”, “it”, “it”)
#Calculate the mode using the user function.
result <- getmode(charv)
print(result)
[1] “it”
```

#### **问题:**enlist 函数是做什么的？

**回答:**它把一个列表转换成一个向量

#### **问题:**R 中的 apply 函数是什么？

**回答:** apply()，它的族是 r 中使用最多的函数之一，当我们要对矩阵的行或列应用一个函数时，我们就使用 apply。

示例:

```
M<- matrix(seq(1,16),4,4)
apply (M,1,min)
[1] 1 2 3 4
```

#### **问题:**R 中的 lapply()函数是什么？

**答:**当我们想对每个应用一个函数时，就使用 lapply()函数

#### **问题:**区分 lapply 和 sapply

**回答:**如果程序员希望输出是数据帧或者向量，那么就使用 sapply 函数，反之如果程序员希望输出是列表，那么就使用 lapply。

#### **问题:**如何在 R 中安装新的包？

**回答:**我们需要知道包的名字

语法:

```
install.packages(“name_of_package”)
```

#### **问题:**merge()函数的作用是什么？

**答案:**我们可以利用 merge 函数()合并两个数据帧。发生合并时，数据框必须具有相同的列名。

举例。

```
df1 <- data.frame(id <- c(1:6), name <-c(rep(“Amit”,3), rep(“Sumit”,3))
df2 < - data.frame(id <- c(7,8,9), name <- c(rep(“Nitin”,2),rep(“Paplu”,1))
*outer join
merge(x=df1, y= df2, by =”id”, all TRUE)
```

all = TRUE 将提供外部连接，因此新的数据集将包含 id 上合并的两个数据框的所有值。

#### **问题:**什么是数据清洗？

**回答:** [数据清理](https://hackr.io/blog/what-is-data-wrangling#step-3-data-cleaning-in-data-wrangling)是分析中的一个过程，涉及删除或修改数据库中不正确、不完整、格式不正确或重复的数据。

#### **问题:**什么是数据重塑？

**回答:**有时候，我们需要特定格式的数据。最初，我们从一个特定的。数据帧中的 csv 文件或 txt 文件。但是，大多数时候我们还需要一个不同于初始数据集的数据集，此外我们还需要添加列或列的位置。因此，所有这些都是数据整形，您可以根据需要给出初始数据框的形状。

#### **问题:**写一个函数把 R 中的两个数相加

**答案:**

```
add <- function(a,b)
{
c <- a+b
print(c)
}
```

#### **问题:**如何从命令行关闭 R？

**回答:**使用函数 q()

#### **问题:**如何读取 R 中的 csv_input 文件？

**答案:**

```
data <- read.csv(“csv_input.csv”)
```

#### **问题:**解释一下 r 中 scan 函数的用法。

**答:**scan()函数用于读取各种类型的数据或数据对象，例如数据向量。可以定制该命令来读取特定数据。该命令等待来自数据的输入，然后返回在提示符下输入的值。

#### **问题:**R 编程语言中使用的不同文件格式有哪些？

**答案:**

1.  。RDA 文件格式:这些是用于在 R 中附加和加载文件的 R 对象。
2.  。Rfiles:这些文件是由转储函数在 R 编辑器中创建的。
3.  。txt 文件。txt 文件用于存储数据集。r 使用 theread.table()和 write.table()函数。
4.  。csv 文件:逗号分隔值文件是常见的数据文件。

#### **问题:**函数 od summary()函数是什么？

**答:** summary()是一个重要的命令，帮助我们得到数据的统计汇总。它包含所有统计数据，如平均值、中值、最小值、最大值、第一个四分位数和第三个四分位数。

#### **问题:**如何在 R 中添加数据集？

**答:** rbind()函数可以用来添加 R 语言的数据集，前提是数据集中的列应该相同。

#### **问题:**R 语言中的因子变量有哪些？

**答:**因子变量是保存字符串或数值的分类变量。因子变量用于各种类型的图形中，特别是用于统计建模，其中正确的自由度数量被分配给它们。

#### **问题:**R 中的 seq()函数有什么用？

**答:**R 中的 seq()函数是用来给用户提供一个数列的。如果我们需要一个特定步长的数字序列，比如 4，8，12，16，那么我们需要提供另一个属性“by =？”这将提供步骤。

举例。

```
> print(seq(5,11, by = 2))

[1] 5,7,9,11
```

#### **问题:**定义重复循环

**答案:** Repeat 循环多次执行一个序列的语句。它没有把条件放在我们放关键字 repeat 的同一个地方。

举例。

```
>name <-c(“Parry”,”John”)
>temp <-5
> repeat {
print(name)
temp <- temp +2
if(temp >11){
Break
}
}
```

这将返回名称向量四次。首先，它打印名称，并将温度提高到 7，以此类推。

#### **问题:**如何在 R 中进行决策？

**答:**R 中的决策执行方式和其他语言中的一样。三个主要决策陈述包括:

1.  如果语句
2.  If.else 语句
3.  交换语句

#### **问题:**存在两个向量，a < - (3，4，5)和 b < - (1，2)，那么 c < - a * b 的输出会是什么？

**答案:** c < - (3，8，5)

#### **问题:**R 中有哪些可以应用二元运算符的二元函数？

**答案:**标量，矩阵，向量

#### **问题:**一个数据帧的主要特征是什么？

**答案:**以下是主要特点:

1.  行名应该是唯一的。
2.  列名不应为空
3.  数据框中存储的数据仅支持三种类型，即数字、因子和字符。
4.  每列应该有相同数量的数据项。这是数据框的主要规则之一。

#### **问题:**解释字符串函数在 R 中的用法

**答案:**R 中的 str()函数用于获取一个数据帧的结构以及前几个观察值。假设一个数据帧有四个变量，每个变量有三个值。那么这个函数的输出将是这样的:

```
‘data.frame’: 3 obs. And 4 variable
$name: chr “Nitin” “Kamal” “Xtramous”
$age : int 16 18 20
$class: int 6 8 10
```

#### **问题:**seq(4)和 seq_along(4)有什么区别

**答案:** seq(4)产生一个从 1 到 4 的向量(c(1，2，3，4))，而 seq_along(4)产生一个长度为(4)的向量，即 1(c(1))。

#### **问题:**如何在 R 中读取一个. csv 文件？

**答案:** read.csv()函数用于从当前工作目录中读取一个 csv(逗号分隔值)。

举例。

```
data_store<- read.csv(“abc.csv”)
print(data_store)
```

#### **问题:**获取有最高工资的人的所有数据。

**答案:**

```
max_salary_person <- subset(data,
salary == max(salary))
print(max_salary_person)
```

#### **问题:**如何获得外连接、左连接、右连接、内连接、交叉连接？

**答案:**

```
outer join - merge (x= df1, y=df2, by= “id”, all= TRUE)
left join - merge (x= df1, y= df2, by = “id”, all.x = TRUE)
right join - merge (x= df1, y= df2, by = “id”, all.y = TRUE)
inner join - merge (x= df1, y= df2, by = “id”)
cross join - merge (x= df1, y= df2, by = NULL)
```

#### **问题:**选角是什么意思？cast()函数有什么用？

**答案:**用于熔化后得到骨料()。所以，现在我们有了按某种顺序排列的数据，如果我们想要聚合具有相似 company_name 和 age 的列，那么我们应该使用 cast()函数。

举例。

```
Casted_data_set <- cast(new_data_set, company_name+age ~ variable, sum)
```

该函数给出了相同公司和年龄的总工资和子女数。

#### **问题:**样本函数在 R 编程中有什么用？

**答案:** Sample()函数可以用来从庞大的数据集中选择一个大小为‘n’的随机样本。

#### **问题:**子集函数在 R 编程中有什么用？

**答案:** Subset()函数用于从给定的数据集中选择变量和观测值。

#### **问题:**rn ORM()函数的作用是什么？用语法解释。

**答案:** rnorm 函数根据传递给函数的均值和标准差自变量生成“n”个正态随机数。

**语法:**

```
rnorm(n, mean = , sd= )
```

#### **问题:**如何在 R 中制作散点图？

**答:**散点图是一种显示许多点绘制在笛卡尔平面上的图形。每个点包含两个值，分别位于 x 轴和 y 轴上。简单散点图是使用 plot()函数绘制的。

散点图的语法是:

```
plot(x,y,main,xlab,ylab,xlim,ylim,axes)
```

在哪里

x 是其值是水平坐标的数据集

y 是数据集，其值是纵坐标

主要是图中的平铺

xlab 和 ylab 是水平和垂直轴上的标签

xlim 和 ylim 是绘图中使用的 x 和 y 值的极限

轴表示两个轴是否都应该在图上。

```
plot(x = input$wt,y = input$mpg,
xlab = “Weight”,
ylab = “Mileage”,
xlim = c(2.5,5)
ylim = c(15,30)
main = “Weight vs Mileage”
)
```

#### **问题:**R 中的 sink 函数是什么？

**答案:**sink()函数定义了输出的方向。

```
#direct output to a file
sink(“myfile”, append = FALSE, split = FALSE)
#return output to the terminal sink()
```

append 选项控制输出是覆盖文件还是添加文件。分割选项决定了输出是否也作为输出文件发送到屏幕。

# 摘要

我们为您提供了热门的 R [编程面试问题](https://hackr.io/blog/programming-interview-questions)，供您准备[数据科学面试](https://hackr.io/blog/data-science-interview-questions)。这 R 个面试问题是最好的一套面试问题。我们也建议你在参加面试前练习编码，有一个你参与过的虚拟项目总是一个优势。你在面试中还遇到过其他问题吗？或者你想和 R 社区分享的其他技巧？

我强烈建议遵循这些非常有用的面试问题。来自 Udemy **:** [数据科学面试指南](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https://www.udemy.com/course/data-science-career-guide-interview-preparation/)。

[数据科学问题](https://hackr.io/blog/data-science-interview-questions)钉在 R 面试里。考虑从书中准备同样的:[破解你的下一本数据科学面试书](https://geni.us/VWWYnL)

下面评论！

**人也在读:****