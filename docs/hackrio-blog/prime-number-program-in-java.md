# Java 中的质数程序|一个数是否是质数

> 原文：<https://hackr.io/blog/prime-number-program-in-java>

任何 Java 开发人员需要回答的最常见的问题之一是用 Java 编写一个素数程序。它是关于领先的高级通用编程语言的基本概念之一。

用 Java 写程序来检查一个数是否是质数有几种方法。然而，基本逻辑保持不变，即:你需要检查输入的数字(或者已经在程序中定义的)是否有除数。

质数程序是学习 Java 必不可少的一部分。因此，大多数关于 Java 的伟大书籍都涉及到了它。在继续讨论 Java 中的质数程序之前，让我们先了解一下质数的概念及其重要性。

## **质数——定义和重要性**

任何只能被除它之外的一个数整除的数都称为素数。3，5，23，47，241，1009 都是质数的例子。虽然 0 和 1 不能成为素数，但 2 是整个无限长的素数集中唯一的偶数。

质数展现出许多奇怪的数学性质，使它们有广泛的应用，其中许多属于信息技术领域。例如，素数可用于伪随机数发生器和计算机哈希表。

历史上有几个使用加密隐藏信息的例子。令人惊讶的是，这是使用质数对信息进行编码的过程。

随着计算机的引入，现代密码学也随之引入。生成更复杂、更长、更难破解的代码变得可行。

大多数现代计算机密码术依赖于利用大数的质因数。由于质数是整数的组成部分，它们对于数论者来说也是最重要的。

### **Java 中的质数程序**

如前所述，用 Java 实现素数程序有几种方法。在这一节中，我们将研究三种不同的方法，以及两个额外的打印素数的程序。

#### **类型 1——不提供输入的简单程序**

这是在 Java 中实现检查一个数是否是质数的程序的最简单的方法之一。它不需要任何输入，只是告诉定义的数(由整数变量 n 定义)是否是一个质数。代码如下:

```
public class PrimeCheck{
public static void main(String args[]){
int i,m=0,flag=0;
int n=3;
m=n/2;
if(n==0||n==1){
System.out.println(n+" is not a prime number.");
}
else{
for(i=2;i<=m;i++){
if(n%i==0){
System.out.println(n+" is not a prime number.");
flag=1;
break;
}
}
if(flag==0) { System.out.println(n+" is a prime number."); }
}
}
}
```

**输出:**

3 是一个质数。

#### **类型 2——使用方法的 Java 程序(无需用户输入)**

这段 Java 代码演示了一个使用方法的质数程序的实现。像前面提到的程序一样，它不要求任何用户输入，只处理输入到程序中定义的方法(名为 checkPrime)的数字。代码如下:

```
public class PrimeCheckUsingMethod{
static void checkPrime(int n){
int i,m=0,flag=0;
m=n/2;
if(n==0||n==1){
System.out.println(n+" is not a prime number.");
}else{
for(i=2;i<=m;i++){
if(n%i==0){
System.out.println(n+" is not a prime number.");
flag=1;
break;
}
}
if(flag==0) { System.out.println(n+" is a prime number."); }
}
}
public static void main(String args[]){
checkPrime(1);
checkPrime(3);
checkPrime(17);
checkPrime(20);
}
}

```

**输出:**

一不是质数。3 是一个质数。17 是一个质数。
20 不是质数。

#### **类型 3–使用扫描仪类的 Java 质数程序**

这个 Java 程序类似于前面提到的程序。但是，该程序会提示用户输入。代码如下:

```
import java.util.Scanner;
import java.util.Scanner;
public class PrimeCheckUsingMethod2 {
public static void main(String[] args) {
Scanner s = new Scanner(System.in);
System.out.print("Enter a number: ");
int n = s.nextInt();
if (isPrime(n)) {
System.out.println(n + " is a prime number.");
} else {
System.out.println(n + " is not a prime number.");
}
}
public static boolean isPrime(int n) {
if (n <= 1) {
return false;
}
for (int i = 2; i < Math.sqrt(n); i++) {
if (n % i == 0) {
return false;
}
}
return true;
}
}
)

```

**样本输出:**

输入一个数字:22
22 不是质数。

[Java 编程/ Java 编码仅供完全初学者使用](https://click.linksynergy.com/link?id=jU79Zysihs4&offerid=1045023.3347252&type=2&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fjava-programming-java-coding-for-complete-beginners-only%2F)

#### **【奖金程序】Type 4——一个用 Java 编写的程序，打印从 1 到 100 的质数**

#### **使用 Scanner 类和 For 循环的 Java 质数程序**

这段代码将演示一个 Java 程序，它能够打印 1 到 100 之间的所有质数。该程序的代码是:

```
class PrimeNumbers
{
public static void main (String[] args)
{
int i =0;
int num =0;
String primeNumbers = "";
for (i = 1; i <= 100; i++)
{
int counter=0;
for(num =i; num>=1; num--)
{
if(i%num==0)
{
counter = counter + 1;
}
}
if (counter ==2)
{
primeNumbers = primeNumbers + i + " ";
}
}
System.out.println("Prime numbers between 1 and 100 are :"\n);
System.out.println(primeNumbers);
}
}

```

**输出:**

1 到 100 之间的质数是:
2 3 5 7 11 13 17 19 23 29 31 37 41 43 47 53 59 61 67 71 73 79 83 89 97

#### **【奖金程序】Type 5–一个 Java 程序，打印从 1 到 n 的质数(用户输入)**

#### **使用扫描器和 For 循环的 Java 质数程序**

这个 Java 程序打印所有存在于 1 和 n 之间的质数，其中 n 是用户输入的数字。代码如下:

```
import java.util.Scanner;
class PrimeNumbers2
{
public static void main (String[] args)
{
Scanner scanner = new Scanner(System.in);
int i =0;
int num =0;
String primeNumbers = "";
System.out.println("Enter a number:");
int n = scanner.nextInt();
scanner.close();
for (i = 1; i <= n; i++)
{
int counter=0;
for(num =i; num>=1; num--)
{
if(i%num==0)
{
counter = counter + 1;
}
}
if (counter ==2)
{
primeNumbers = primeNumbers + i + " ";
}
}
System.out.println("Prime numbers between 1 and n are:"/n);
System.out.println(primeNumbers);
}
}

```

**样本输出:**

输入一个数字:22

1 到 22 之间的质数是:
2 3 5 7 11 13 17 19

## **结论**

这就是 Java 中的质数程序。不管 Java 开发人员的技术水平如何，能够编写一个关于素数的程序是非常重要的，至少可以用来检查一个给定的数(或一组数)是否是素数。

持续学习对于编码的进步非常重要。一个你现在能够编写的程序，当你在获得新知识后编写时，可能会更好。如果你想进一步提高你的 Java 技能，可以考虑看看一些最好的 Java 教程。

你知道用 Java 实现素数程序的一些有趣的方法吗？介意和我们分享一下吗？那么你可以通过下面的评论窗口来完成。提前感谢。

**人也在读:**