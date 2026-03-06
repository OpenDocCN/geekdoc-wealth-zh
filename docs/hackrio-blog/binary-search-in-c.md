# C 程序设计中的二分搜索法-源代码和解释

> 原文：<https://hackr.io/blog/binary-search-in-c>

二分搜索法是一种简单的算法，用于查找存储在有序列表中的项目的位置。C 程序中的二分搜索法有一些变化，例如在算法的每一步测试相等和小于。

C 语言中的二分搜索法是一个简单程序的例子，可以用来解决复杂的问题。因此，这是一个重要的基础概念，你会在几乎所有关于 C 编程语言 的 [好书中找到。](https://hackr.io/blog/10-best-c-cpp-books)

在给出 C 语言中建立二分搜索法的代码之前，我们先来了解一下算法到底是如何工作的。

## 它是如何工作的？

二进制搜索算法适用于在一个有序数组中搜索一个元素。搜索从比较目标元素和数组的中间元素开始。如果值匹配，则返回元素的位置。

如果目标元素小于数组的中间元素(考虑到数组遵循升序),则数组的后半部分被丢弃，通过划分前半部分继续搜索。

当目标元素大于中间元素时，过程是相同的，只是在这种情况下，数组的前半部分在继续搜索之前被丢弃。重复迭代，直到找到目标元素的匹配。

## **C 程序中的二分搜索法**

下面的代码用 C 编程语言实现了二分搜索法。虽然它只能用于排序数组，但与线性搜索相比，它的速度很快。

如果需求要求在未排序的数组上使用二分搜索法，那么在对其使用二分搜索法算法之前，需要先对其进行排序。为此，您可以使用一些排序技术，如 [冒泡排序](https://hackr.io/blog/bubble-sort-in-c) 或 [合并排序](https://hackr.io/blog/merge-sort-in-c) 。

注意:-下面提到的代码假设输入数字遵循升序！

这里是 C 语言中二分搜索法的代码:

```
#include 
int main()
{
   int c, first, last, middle, n, search, array[100];
   printf("Enter number of elements:\n");
   scanf("%d",&n); 
   printf("Enter %d integers:\n", n);
   for (c = 0; c < n; c++)
      scanf("%d",&array[c]); 
   printf("Enter the value to find:\n");
   scanf("%d", &search);
   first = 0;
   last = n - 1;
   middle = (first+last)/2;
   while (first <= last) {
      if (array[middle] < search)
         first = middle + 1;    
      else if (array[middle] == search) {
         printf("%d is present at index %d.\n", search, middle+1);
         break;
      }
      else
         last = middle - 1;
      middle = (first + last)/2;
   }
   if (first > last)
      printf("Not found! %d is not present in the list.\n", search);
   return 0;  
}

```

***样本输出:***

输入元素数量:

5

输入 5 个整数:

1
9
22
24
46

**输入要查找的值:**

24

24 出现在索引 4 处。

### **在 C 程序中实现二分搜索法的其他例子**

*   递归实现二分搜索法

注意 : - 该程序不允许您输入元素，因为列表已经在其中实现。这个程序简单地演示了 C 语言中二分搜索法程序的工作方式！

```
#include 
int binarySearch(int arr[], int l, int r, int x) 
{ 
if (r >= l) { 
int mid = l + (r - l) / 2; 
if (arr[mid] == x) 
return mid; 
if (arr[mid] > x) 
return binarySearch(arr, l, mid - 1, x); 
return binarySearch(arr, mid + 1, r, x); 
} 
return -1; 
}  
int main(void) 
{ 
int arr[] = { 2, 3, 4, 10, 40 }; 
int n = sizeof(arr) / sizeof(arr[0]); 
int x = 10; 
int result = binarySearch(arr, 0, n - 1, x); 
(result == -1) ? printf("The element is not present in array") 
: printf("The element is present at index %d", 
result); 
return 0; 
}

```

**输出:**

元素出现在索引 3 处。

*   二分搜索法的迭代实现

注意:-该程序不允许您输入元素，因为列表已经在其中实现。这个程序简单地演示了 C 语言中二分搜索法程序的工作方式！

```
#include 
int binarySearch(int arr[], int l, int r, int x) 
{ 
while (l <= r) { 
int m = l + (r - l) / 2; 
if (arr[m] == x) 
return m; 
if (arr[m] < x) 
l = m + 1; 
        else
r = m - 1; 
}  
return -1; 
}   
int main(void) 
{ 
int arr[] = { 2, 3, 4, 10, 40 }; 
int n = sizeof(arr) / sizeof(arr[0]); 
int x = 10; 
int result = binarySearch(arr, 0, n - 1, x); 
    (result == -1) ? printf("The element is not present"
" in array") 
                   : printf("The element is present at "
"index %d", 
result); 
return 0; 
} 

```

**输出:**

元素出现在索引 3 处。

推荐课程

### 二分搜索法算法的时间复杂度

假设 T(N)是一组 N 个元素的二分搜索法的时间复杂度。然后，

T(N) = T(N/2) + O(1)(通过递推关系) - (i)

现在，应用马斯特斯定理计算递归关系的运行时间复杂度，即

T(N)= aT(N/b)+f(N)-(ii)

比较等式(ii)和(I)，我们得到，

a = 1，b = 2

因此，log (a 基数 b) = 1 = c - (iii)

现在，f(n)= n^c log^k(n)//k = 0-(iv)

利用等式(ii)中的(iii)和(iv)，我们得到，

t(n)= o(n^c log^(k+1)n)= o(log(n))-(v)

对于二分搜索法来说，这是最坏情况下的时间复杂度。现在，进行唯一比较的最佳情况是。因此，N = 1。所以，我们得到，

O(log(1))= O(1)(as log(1)= 1)

因此，不同情况下二分搜索法的时间复杂度为:

**最佳情况**

O(1)

**最坏情况**

O(对数 n)

[掌握数据结构&使用 C 和 C++](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fdatastructurescncpp%2F) 算法

### **二分搜索法在 C 中的利弊**

**优点:**

*   一个相当简单的算法基于 [分而治之的方法](https://en.wikipedia.org/wiki/Divide-and-conquer_algorithm#Divide_and_conquer)
*   与线性搜索相比要快得多。线性搜索需要对平均和最坏情况进行 N/2 和 N 次比较。二分搜索法仅仅需要分别针对平均和最坏情况的总共 log2 (N)和 log 2 (N)的比较。简而言之，线性搜索平均需要对一组百万个元素进行 500，000 次比较。另一方面，二分搜索法只需要 20 次比较。
*   通常作为已经实现的库例程可用

**缺点:**

*   比线性搜索复杂
*   如果列表不支持随机访问，效率损失很大
*   仅适用于已排序并保持排序的列表

**程序完成！**

在 c #中实现二分搜索法并没有唯一权威的方法。因此，可能性是无限的。文章中提到的几个例子只是许多例子中的一部分。

理解二分搜索法是如何工作的不仅对掌握 C 语言很重要，对掌握其他编程语言也很重要。

你知道用 C 语言编写二分搜索法的其他有趣/有效的方法吗？通过下面的专用评论窗口与社区分享。

**人也在读:**