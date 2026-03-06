# 2023 年脸书顶级面试问答[更新]

> 原文：<https://hackr.io/blog/facebook-interview-questions>

脸书是一家社交媒体网站公司，由马克·扎克伯格和他的哈佛大学同学 T2 以及室友爱德华多·萨维林、安德鲁·麦科勒姆、达斯汀·莫斯科维茨和克里斯·休斯于 2004 年创立。脸书是一家每个人都想去工作的公司，因为它为员工提供最好的福利和良好的体验。

破解脸书的采访可能是一颗难以下咽的药丸。然而，通过严密的技术准备和冷静的头脑，你可以在世界上最大的社交媒体巨头获得一个工作机会。

## 脸书面试问答

通常，脸书面试流程包括:

*   **两轮电话会谈**–关注基本的问题解决和数据结构
*   **2 或 3 轮现场编码**–包括略高于平均水平的数据结构/算法问题的白板解决方案。经验不足者多打几轮
*   **1 或 2 轮现场系统设计**–旨在评估受访者为现实生活中的产品提出高效的高级设计架构的能力。更有经验的候选人将面临更多这样的回合
*   **1 次文化契合现场调查**-旨在评估受访者是否适合脸书的文化。不需要任何专业技术

虽然电话面试会涉及到关于数据结构和问题解决的问题，但是[系统设计](https://hackr.io/tutorials/learn-system-architecture)只针对少数候选人。所以，剩下的就是现场编码了，这是最重要的。

以下是 16 个最重要的脸书面试问题，你可能会在编码现场遇到:

**回答**:假设我们有如下矩阵:

1 2 3
4 5 6
7 8 9

然后，将其逆时针旋转 90 度，将得到以下矩阵:

3 6 9
2 5 8
1 4 7

在检查上述结果矩阵之后，可以做出以下推论:

*   源矩阵的第一行将以相反的顺序产生所获得矩阵的第一列
*   源矩阵的第二行将以相反的顺序产生所获得矩阵的第二列
    。
    。
    。
*   源矩阵的最后一行将以相反的顺序导致所获得的矩阵的最后一列

任何 N×N 矩阵都有地板(N/2)平方圈。对于每个平方周期，相应单元中的元素将逆时针方向交换；从上到下，从左到下，从下到右，从右到上。

为了实现上述目标，我们只需要一个临时变量。下面是如何在 C++中实现 N×N 矩阵逆时针旋转 90 度:

```
#include <bits/stdc++.h>
#define N 4
using namespace std;
void displayMatrix(int mat[N][N]);
void rotateMatrix(int mat[][N])
{
 for (int x = 0; x < N / 2; x++) 
 {
 for (int y = x; y < N-x-1; y++) 
 { 
 int temp = mat[x][y]; 
 mat[x][y] = mat[y][N-1-x]; 
 mat[y][N-1-x] = mat[N-1-x][N-1-y]; 
 mat[N-1-x][N-1-y] = mat[N-1-y][x]; 
 mat[N-1-y][x] = temp; 
 } 
 } 
}
void displayMatrix(int mat[N][N]) 
{ 
 for (int i = 0; i < N; i++) 
 { 
 for (int j = 0; j < N; j++) 
 printf("%2d ", mat[i][j]);
 printf("\n"); 
 } 
 printf("\n"); 
} 
int main() 
{ 
 int mat[N][N] = 
 { 
 , 
 , 
 , 

 }; 
 rotateMatrix(mat); 
 displayMatrix(mat); 
 return 0; 
}

```

**输出:**

4 8 12 16
3 7 11 15
2 6 10 14
1 5 9 13

### **问题** : **给你一个正数数组。解释如何找到包含斐波纳契数列元素的数组的最大子集。**

**回答**:找出包含斐波纳契数的正数数组的最大子集的一个简单方法是遍历数组的所有元素。然后，检查每个数字是否是斐波纳契数。如果它把它加到结果中。

尽管前面提到的方法很简单，但效率不高。可以遵循以下步骤来设计实现该目的的有效方式:

*   找出数组中的最大值
*   生成斐波纳契数，直到数组的最大值，并将其存储在哈希表中
*   再次遍历数组，将数组和哈希表中出现的所有数字添加到结果中

下面的 C++代码演示了一个有效的解决方案:

```
#include<bits/stdc++.h>
using namespace std;
void findFibSubset(int arr[], int n)
{
int max = *std::max_element(arr, arr+n);
int a = 0, b = 1;
unordered_set hash;
hash.insert(a);
hash.insert(b);
while (b < max)
{
int c = a + b;
a = b;
b = c;
hash.insert(b);
}
for (int i=0; i<n; i++)
if (hash.find(arr[i]) != hash.end())
printf("%d ", arr[i]);
}
int main()
{
int arr[] = ;
int n = sizeof(arr)/sizeof(arr[0]);
findFibSubset(arr, n);
return 0;
}

```

**输出:**

8 5 2 1 13

### **问题** : **假设你有一个整数数组和一个正整数 k，你将如何计算所有差异等于 k 的不同对？**

**回答**:有几种方法可以达到要求。我们将讨论其中的两个:

**方法 1–考虑所有对(注意:不适用于有重复的数组)**

这种基本方法包括逐个考虑整数数组中的所有对，并检查它们的差是否等于给定的正整数 k。如果是，则将它们添加到结果中。下面是该方法在 C++中的实现:

```
#include 
using namespace std; 
int countPairsWithDiffK(int arr[], int n, int k) 
{ 
 int count = 0; 
 for (int i = 0; i < n; i++) 
 { 
 for (int j = i+1; j < n; j++) 
 if (arr[i] - arr[j] == k || arr[j] - arr[i] == k ) 
 count++; 
 } 
 return count; 
} 

int main() 
{ 
 int arr[] = ; 
 int n = sizeof(arr)/sizeof(arr[0]); 
 int k = 3;
 cout << "Total number of pairs with the given difference is: "
 << countPairsWithDiffK(arr, n, k); 
 return 0;
}

```

**输出:**

具有给定差异的对的总数是:2

**方法 2–使用排序**

找到对计数的另一种方法是使用 O(nLogn)排序算法，比如堆排序和[合并排序](https://hackr.io/blog/merge-sort-in-c)。以下步骤描述了该方法:

*   将计数初始化为 0
*   按升序对数组元素进行排序
*   消除数组中的重复项(如果有)
*   对于每个元素 arr[i]:
*   从 i+1 到 n-1 的子阵列中 arr[i] + k 的二分搜索法
*   如果找到 arr[i] + k，则递增计数
*   返回计数

下面是实现上述方法的 C++代码:

```
#include 
#include 
using namespace std;
int binarySearch(int arr[], int low, int high, int x)
{
if (high >= low)
{
int mid = low + (high - low)/2;
if (x == arr[mid])
return mid;
if (x > arr[mid])
return binarySearch(arr, (mid + 1), high, x);
else
return binarySearch(arr, low, (mid -1), x);
}
return -1;
}
int countPairsWithDiffK(int arr[], int n, int k)
{
int count = 0, i;
sort(arr, arr+n);
for (i = 0; i < n-1; i++)
if (binarySearch(arr, i+1, n-1, arr[i] + k) != -1)
count++;
return count;
}
int main()
{
int arr[] = ;
int n = sizeof(arr)/sizeof(arr[0]);
int k = 3;
cout << "Total number of pairs with the given difference is: "
<< countPairsWithDiffK(arr, n, k);
return 0;
}

```

**输出:**

具有给定差异的对的总数是:2

### **问题** : **你能解释一下如何在计数和说出序列中找到第 n 项吗？**

**回答**:首先，我们需要生成从 1 到 n 的所有项，前两项初始化为 1 和 11。第三项由第二项产生，第四项由第三项产生，依此类推。为了生成下一个术语，我们需要扫描上一个术语。

在扫描前一项时，我们需要跟踪所有连续字符的计数。对于相同字符的序列，我们将在字符后添加计数以生成下一项。

下面是在计数和说出序列中查找第 n 项的 C++代码:

```
#include <bits/stdc++.h>
using namespace std;
string countnndSay(int n)
{
if (n == 1) return "1";
if (n == 2) return "11";
string str = "11";
for (int i = 3; i<=n; i++)
{
str += '$';
int len = str.length();
int cnt = 1;
string tmp = "";
for (int j = 1; j < len; j++)
{
if (str[j] != str[j-1])
{
tmp += cnt + '0';
tmp += str[j-1];
cnt = 1;
}
else cnt++;
}
str = tmp;
}
return str;
}
int main()
{
int N = 4;
cout << countnndSay(N) << endl;
return 0;
}

```

**输出:**

1211

### **问题** : **如果给你一个包含大写字母和整数的字符串，你将如何打印这个字符串，其中字母按照字典顺序排列，后跟整数之和？**

**回答**:以下是如何实现预期目标的逐步说明:

*   遍历给定的字符串
*   (对于字母表)将其出现计数递增到哈希表中
*   (对于整数)单独存储，并将其添加到之前的总和中
*   使用哈希表首先将所有字母按照字典顺序添加到一个字符串中，然后在末尾添加整数之和
*   返回结果字符串

下面的代码演示了在 C++中实现输出:

```
#include<bits/stdc++.h>
using namespace std;
const int MAX_CHAR = 26;
string arrangeString(string str)
{
int char_count[MAX_CHAR] = ;
int sum = 0;
for (int i = 0; i < str.length(); i++)
{
if (str[i]>='A' && str[i] <='Z')
char_count[str[i]-'A']++;
else
sum = sum + (str[i]-'0');
}
string res = "";
for (int i = 0; i < MAX_CHAR; i++)
{
char ch = (char)('A'+i);
while (char_count[i]--)
res = res + ch;
}
if (sum > 0)
res = res + to_string(sum);
return res;
}
int main()
{
string str = "AKHIL20BHADWAL24";
cout << arrangeString(str);
return 0;
}

```

**输出:**

AAABDHHIKLLW8

### **问题** : **将一个罗马数字转换成其对应的整数。**

**回答**:我们将使用以下算法将罗马数字转换成等价的整数:

*   将可用的罗马数字字符串拆分成罗马符号
*   将每个罗马符号转换为其等效的整数值
*   对于每个符号，从索引 0 开始:
*   (如果罗马符号的当前值大于或等于下一个罗马符号的值)将该值加到总数中
*   (如果罗马符号的当前值小于下一个罗马符号的值)通过将下一个符号的值加到总数中来减去该值

下面的 C++代码演示了该算法:

```
#include<bits/stdc++.h>
using namespace std;
int value(char r)
{
if (r == 'I')
return 1;
if (r == 'V')
return 5;
if (r == 'X')
return 10;
if (r == 'L')
return 50;
if (r == 'C')
return 100;
if (r == 'D')
return 500;
if (r == 'M')
return 1000;
return -1;
}
int romanToDecimal(string &str)
{
int res = 0;
for (int i=0; i<str.length(); i++)
{
int s1 = value(str[i]);
if (i+1 < str.length())
{
int s2 = value(str[i+1]);
if (s1 >= s2)
{
res = res + s1;
}
else
{
res = res + s2 - s1;
i++;
}
}
else
{
res = res + s1;
i++;
}
}
return res;
}
int main()
{
string str ="MMCDXXII";
cout << "Integer equivalent for the Roman Numeral is: "
<< romanToDecimal(str) << endl;
return 0;
}

```

**输出:**

罗马数字的整数等价物是:2422

### **问题** : **求给定数组中和大于给定值 x 的最小子数组的个数**

**回答**:我们将使用两个嵌套循环来寻找给定数组中总和大于给定值 x 的最小子数组。虽然外循环将选取一个起始元素，但内循环将所有元素视为结束元素。

每当当前开始和结束之间存在的元素的总和大于给定的数 x 时，如果当前长度小于先前的最小长度，则结果被更新。

该方法可以使用以下代码在 C++中实现:

```
#include 
using namespace std;
int smallestSubWithSum(int arr[], int n, int x)
{
int min_len = n + 1;
for (int start=0; start<n; start++)
{
int curr_sum = arr[start];
if (curr_sum > x) return 1;
for (int end=start+1; end<n; end++)
{
curr_sum += arr[end];
if (curr_sum > x && (end - start + 1) < min_len)
min_len = (end - start + 1);
}
}
return min_len;
}
int main()
{
int arr1[] = ;
int x = 51
int n1 = sizeof(arr1)/sizeof(arr1[0]);
int res1 = smallestSubWithSum(arr1, n1, x);
(res1 == n1+1)? cout << "Not possible\n" :
cout << res1 << endl;
return 0;
}

```

**输出:**

3

### **问题** : **从给定的数组中，找出一个至少有 k 个数并具有最大可能和的子数组。**

**回答**:我们会先计算最大和，直到每个索引都被覆盖，并存储在一个名为 maxSum[]的数组中。接下来，我们将使用大小为 k 的滑动窗口概念。然后，我们将跟踪当前 k 个元素的总和。

为了计算当前窗口的总和，我们需要删除前一个窗口的第一个元素并添加当前元素。一旦我们得到当前窗口的总和，我们将加上前一个窗口的 maxSum[]，如果它将大于当前的 maxSum[]。

下面是一个实现上述想法的 C++程序:

```
#include<bits/stdc++.h>
using namespace std;
int maxSumWithK(int a[], int n, int k)
{
int maxSum[n];
maxSum[0] = a[0];
int curr_max = a[0];
for (int i = 1; i < n; i++)
{
curr_max = max(a[i], curr_max+a[i]);
maxSum[i] = curr_max;
}
int sum = 0;
for (int i = 0; i < k; i++)
sum += a[i];
int result = sum;
for (int i = k; i < n; i++)
{
sum = sum + a[i] - a[i-k];
result = max(result, sum);
result = max(result, sum + maxSum[i-k]);
}
return result;
}
int main()
{
int a[] = ;
int k = 2;
int n = sizeof(a)/sizeof(a[0]);
cout << maxSumWithK(a, n, k);
return 0;
}

```

**输出:**

46

子阵列是 22，24

### **问题** : **如何将三元表达式转换成二叉树？**

**回答**:我们将从遍历字符串开始，将第一个字符作为词根，然后:

*   添加下一个字符作为根的左子字符(当遇到“？”时)符号)
*   添加下一个字符作为根的右子字符(当遇到“.”时)符号)
*   重复步骤 1 和 2，直到遍历完字符串的所有元素

以下是使用 C++代码的方法演示:

```
#include<bits/stdc++.h>
using namespace std;
struct Node
{
char data;
Node *left, *right;
};
Node *newNode(char Data)
{
Node *new_node = new Node;
new_node->data = Data;
new_node->left = new_node->right = NULL;
return new_node;
}
Node *convertExpression(string str, int & i)
{
Node * root =newNode(str[i]);
if(i==str.length()-1) return root;
i++;
if(str[i]=='?')
{
i++;
root->left = convertExpression(str,i);
i++;
root->right = convertExpression(str,i);
return root;
}
else return root;
}
void printTree( Node *root)
{
if (!root)
return ;
cout << root->data <<" ";
printTree(root->left);
printTree(root->right);
}
int main()
{
string expression = "a?b?c:d:e";
int i=0;
Node *root = convertExpression(expression, i);
printTree(root) ;
return 0;
}

```

**输出:**

a b c d e

### **问题** : **解释寻找总和为 0 的数组中所有三元组的各种方法。**

**回答**:我们可以有三种不同的方法来找到一个数组中所有总和为 0 的三元组。让我们简单讨论一下:

**方法 1**–最简单的方法是运行三个循环。将检查数组的每个三元组的元素之和是否为 0。如果找到，则打印三元组，否则，打印未找到的三元组。这种方法的时间复杂度将是 O(n3)。

**方法 2**–这种方法利用了散列法。在遍历数组的每个元素 arr[i]时，我们会找到一个 sum -arr[i]的对。这种方法的时间复杂度将是 O(n2)。

**方法 3**–第三种方法使用排序，需要额外的空间。虽然这种方法的时间复杂度将为 O(n2)，但相比于其他两种方法所需的 O(n)辅助空间，这种方法只需要 O(1)辅助空间。该方法按以下步骤工作:

*   对给定数组的所有元素进行排序
*   从 i=0 到 n-2 运行循环
*   初始化两个索引变量 l = i+1 和 r = n-1
*   While (l
*   如果总和小于零，则 l++
*   如果总和大于零，那么 r -
*   如果总和为零，则打印三联体，并执行 l++和 r -

下面的 C++程序实现了方法 3:

```
#include<bits/stdc++.h>
using namespace std;
void findTriplets(int arr[], int n)
{
bool found = false;
sort(arr, arr+n);
for (int i=0; i<n-1; i++)
{
int l = i + 1;
int r = n - 1;
int x = arr[i];
while (l < r)
{
if (x + arr[l] + arr[r] == 0)
{
printf("%d %d %d\n", x, arr[l], arr[r]);
l++;
r--;
found = true;
}
else if (x + arr[l] + arr[r] < 0)
l++;
else
r--;
}
}
if (found == false)
cout << " Not found!" << endl;
}
int main()
{
int arr[] = ;
int n = sizeof(arr)/sizeof(arr[0]);
findTriplets(arr, n);
return 0;
}

```

**输出:**

-43 1 42
-10 0 10

### **问题** : **假设给你一棵二叉树。解释你将如何找到它的最小深度？**

**答**:寻找二叉树最小深度的方法包括遍历给定的二叉树。对于每个节点，检查它是否是叶节点:

*   如果是，则返回 1
*   如果不是，那么:
    *   如果左子树为空，则对右子树进行递归
    *   如果右边的子树为空，则对左边的子树递归
    *   如果左右子树都不为空，则取两个深度中的最小值

下面是使用 C++代码实现的上述方法:

```
#include<bits/stdc++.h>
using namespace std;
struct Node
{
int data;
struct Node* left, *right;
};
int minDepth(Node *root)
{
if (root == NULL)
return 0;
if (root->left == NULL && root->right == NULL)
return 1;
if (!root->left)
return minDepth(root->right) + 1;
if (!root->right)
return minDepth(root->left) + 1;
return min(minDepth(root->left), minDepth(root->right)) + 1;
}
Node *newNode(int data)
{
Node *temp = new Node;
temp->data = data;
temp->left = temp->right = NULL;
return (temp);
}
int main()
{
Node *root = newNode(1);
root->left = newNode(2);
root->right = newNode(3);
root->left->left = newNode(4);
root->left->right = newNode(5);
root->left->left->left = newNode(6);
root->left->left->right = newNode(7);
cout <<"The minimum depth of the given binary tree is: "<< minDepth(root);
return 0;
}

```

**输出:**

给定二叉树的最小深度是:2

### **问题** : **请** **解释一下你将如何把 1 到 3999 之间的任何整数值转换成它的罗马数字等价物。**

**回答**:下面的算法将用于将 1 到 3999 之间的任何整数值转换成其罗马数字等价物:

*   按顺序将给定的数字与基值 1000、900、500、400、50、40、10、9、5、4 和 1 进行比较
*   最接近、较小或相等的值将作为初始基值
*   现在，用给定的数除以初始基值
*   初始基值的相应罗马符号将重复商次，而余数将遵循步骤 1
*   该过程将被重复，直到余数变为 0

可以使用以下代码在 C++中实现该算法:

```
#include <bits/stdc++.h>
using namespace std;
int sub_digit(char num1, char num2, int i, char *c)
{
c[i++] = num1;
c[i++] = num2;
return i;
}
int digit(char ch, int n, int i, char *c)
{
for (int j = 0; j < n; j++)
c[i++] = ch;
return i;
}
void printRoman(int number)
{
char c[10001];
int i = 0;
if (number <= 0)
{
printf("Invalid number");
return;
}
while (number != 0)
{
if (number >= 1000)
{
i = digit('M', number/1000, i, c);
number = number%1000;
}
else if (number >= 500)
{
if (number < 900)
{
i = digit('D', number/500, i, c);
number = number%500;
}
else
{
i = sub_digit('C', 'M', i, c);
number = number%100 ;
}
}
else if (number >= 100)
{
if (number < 400)
{
i = digit('C', number/100, i, c);
number = number%100;
}
else
{
i = sub_digit('C','D',i,c);
number = number%100;
}
}
else if (number >= 50 )
{
if (number < 90)
{
i = digit('L', number/50,i,c);
number = number%50;
}
else
{
i = sub_digit('X','C',i,c);
number = number%10;
}
}
else if (number >= 10)
{
if (number < 40)
{
i = digit('X', number/10,i,c);
number = number%10;
}
else
{
i = sub_digit('X','L',i,c);
number = number%10;
}
}
else if (number >= 5)
{
if (number < 9)
{
i = digit('V', number/5,i,c);
number = number%5;
}
else
{
i = sub_digit('I','X',i,c);
number = 0;
}
}
else if (number >= 1)
{
if (number < 4)
{
i = digit('I', number,i,c);
number = 0;
}
else
{
i = sub_digit('I', 'V', i, c);
number = 0;
}
}
}
printf("The Roman Numeral equivalent for the given number is: ");
for (int j = 0; j < i; j++)
printf("%c", c[j]);
}
int main()
{
int number = 2422;
printRoman(number);
return 0;
}

```

**输出:**

与给定数字等价的罗马数字是:MMCDXXII

### **问题** : **如何检查给定的字符串是否是 K-回文？**

**回答**:我们将从寻找给定字符串的最长回文子序列开始。如果前述与给定字符串之差小于或等于 k，则给定字符串将是 k-回文，否则不是。

我们可以使用下面的 C++程序来检查给定的字符串是否是 K-回文:

```
#include <bits/stdc++.h>
using namespace std;
int lcs( string X, string Y, int m, int n )
{
int L[m + 1][n + 1];
for (int i = 0; i <= m; i++)
{
for (int j = 0; j <= n; j++)
{
if (i == 0 || j == 0)
L[i][j] = 0;
else if (X[i - 1] == Y[j - 1])
L[i][j] = L[i - 1][j - 1] + 1;
else
L[i][j] = max(L[i - 1][j], L[i][j - 1]);
}
}
return L[m][n];
}
bool isKPal(string str, int k)
{
int n = str.length();
string revStr = str;
reverse(revStr.begin(), revStr.end());
int lps = lcs(str, revStr, n, n);
return (n - lps <= k);
}
int main()
{
string str = "abvcdeca";
int k = 3;
isKPal(str, k) ? cout << "Yes" : cout << "No";
return 0;
}

```

**输出:**

是

### **问题** : **你能解释一下用字符串表示的大数如何相乘吗？**

**回答**:我们先从第二个数的最后一位数字乘以第一个数开始，接着是第二个数的倒数第二位数字乘以第一个数，两者相加。该过程将继续，直到第二个数字的所有数字都完成。

下面是如何在 C++中实现同样的功能:

```
#include<bits/stdc++.h>
using namespace std;
string multiply(string num1, string num2)
{
int n1 = num1.size();
int n2 = num2.size();
if (n1 == 0 || n2 == 0)
return "0";
vector result(n1 + n2, 0);
int i_n1 = 0;
int i_n2 = 0;
for (int i=n1-1; i>=0; i--)
{
int carry = 0;
int n1 = num1[i] - '0';
i_n2 = 0;
for (int j=n2-1; j>=0; j--)
{
int n2 = num2[j] - '0';
int sum = n1*n2 + result[i_n1 + i_n2] + carry;
carry = sum/10;
result[i_n1 + i_n2] = sum % 10;
i_n2++;
}
if (carry > 0)
result[i_n1 + i_n2] += carry;
i_n1++;
}
int i = result.size() - 1;
while (i>=0 && result[i] == 0)
i--;
if (i == -1)
return "0";
string s = "";
while (i >= 0)
s += std::to_string(result[i--]);
return s;
}
int main()
{
string str1 = "24224620578";
string str2 = "98055650629857338077";
if((str1.at(0) == '-' || str2.at(0) == '-') &&
(str1.at(0) != '-' || str2.at(0) != '-' ))
cout<<"-";
if(str1.at(0) == '-' && str2.at(0)!='-')
{
str1 = str1.substr(1);
}
else if(str1.at(0) != '-' && str2.at(0) == '-')
{
str2 = str2.substr(1);
}
else if(str1.at(0) == '-' && str2.at(0) == '-')
{
str1 = str1.substr(1);
str2 = str2.substr(1);
}
cout << multiply(str1, str2);
return 0;
}

```

**输出:**

2375360932037220733184397148506

### **问题** : **你如何检查一个数组中两个元素的和是否等于给定的数 x？**

**答**:我们可以用下面的算法来检验一个数组中两个元素的和是否等于给定的数 x:

*   给定数组按降序排序
*   初始化两个索引变量:
*   l = 0 到最左边的索引
*   r = ar_size-1 到最右边的索引
*   当 l
*   如果 A[l] + A[r] == sum，则返回 1
*   l++，如果 A[l] + A[r] < sum
*   否则 r -
*   继续循环步骤 3，直到数组中的所有元素都用完

下面是一个演示上述方法的 C++程序:

```
#include <bits/stdc++.h>
using namespace std;
bool hasArrayTwoCandidates(int A[], int arr_size, int sum)
{
int l, r;
sort(A, A + arr_size);
l = 0;
r = arr_size - 1;
while (l < r)
{
if(A[l] + A[r] == sum)
return 1;
else if(A[l] + A[r] < sum)
l++;
else // A[i] + A[j] > sum
r--;
}
return 0;
}
int main()
{
int A[] = ;
int x = 32;
int arr_size = sizeof(A) / sizeof(A[0]);
if (hasArrayTwoCandidates(A, arr_size, n))
cout << "The array has two elements with the given sum!";
else
cout << "The given array doesn't have two elements with the given sum!";
return 0;
}

```

**输出:**

给定的数组中有两个元素具有给定的和！

**回答**:

**输入**——输入的第一行包含一个整数 N，表示流中元素的总数。接下来的 N 行包含整数 x，它表示要插入到流中的数字。

**输出** -对于添加到流中的每个元素，在新的一行中打印新的中位数的下限。

为了输出正确，我们需要遵循两个约束:

*   n 大于或等于 1 且小于或等于 106
*   x 大于或等于 1 且小于或等于 106

一个例子:

**输入:**

4(元素数量，即 N)
5 *
15 *
1 *
3 *
* =流的元素

输出将是:

5
10
5
4

**说明:**

5 去流->中值 5 (5)
15 去流- >中值 10 (5，15)
1 去流- >中值 5 (5，15，1)
3 去流- >中值 4 (5，15，1，3)

## 结论

这总结了最重要的脸书编码面试问题列表。希望这些问题能帮助你打开即将到来的脸书面试。

寻找更多面试问题？这是一门优秀的 udemy 课程，可以让你为编程面试做好准备:

[脱离:编程和编码面试](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https://www.udemy.com/course/break-away-coding-interviews-1/)

这里有一本很棒的书，里面有一些常见的编码问题和答案，可以帮助你做好准备:

[破解编码面试:189 个编程问题及解决方案。](https://geni.us/MmRP)

万事如意！

**人也在读:**