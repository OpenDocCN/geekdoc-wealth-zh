# 下载 C#备忘单 PDF 供您快速参考

> 原文：<https://hackr.io/blog/c-sharp-cheat-sheet>

**属性**

**描述**

**例子**

[**是固定大小的**](https://www.geeksforgeeks.org/c-check-if-an-array-has-fixed-size-or-not/)

检查数组是否有固定的大小。

string[]arr val = new string[]{ " stud 1 "，" stud2 "，" stud 3 " }；

阿尔瓦尔。IsFixedSize

[**是只读的**](https://www.geeksforgeeks.org/c-check-if-an-array-is-read-only-or-not/)

检查数组是否是只读的。

IsReadOnly 设置：

[**被同步**](https://www.geeksforgeeks.org/c-check-if-an-array-is-synchronized-thread-safe-or-not/)

检查对数组的访问是否同步(线程安全)。

阿尔瓦尔。is 同步；

[**长度**](https://www.geeksforgeeks.org/how-to-find-the-length-of-an-array-in-c/)

获取数组所有维度中的元素总数。

阿尔瓦尔。长度；

**长**长

64 位整数长度

阿瓦勒。长长度；

[**排名**](https://www.geeksforgeeks.org/how-to-find-the-rank-of-an-array-in-c/)

获取数组的秩(维数)。例如，一维数组返回 1，二维数组返回 2，依此类推。

阿尔瓦尔。排名；

[](https://www.geeksforgeeks.org/how-to-get-synchronize-access-to-the-array-in-c-sharp/)

 **获取用于同步数组访问的对象

阿尔瓦尔。SyncRoot

[**AsReadOnly()**](https://www.geeksforgeeks.org/c-array-asreadonlyt-method/)

返回指定数组的只读包装。

数组。AsReadOnly(arr val)；

[](https://www.geeksforgeeks.org/how-to-use-array-binarysearch-method-in-c-sharp-set-1/)

 **使用[二分搜索法](https://hackr.io/blog/binary-search-in-c)算法在一维排序数组中搜索一个值。

数组。BinarySearch(arrVal，obj)；其中 obj 是要搜索的对象。

[](https://www.geeksforgeeks.org/c-array-clear-method/)

 **将数组中的元素范围设置为每种元素类型的默认值。

数组。Clear(arrVal，0，2)；

如果 arrVal 是一个整数数组，那么在执行 Clear()后，位置 0 到 2 的元素将被设置为零。

**克隆()**

创建数组的浅表副本。

数组。克隆(arr val)；

[](https://www.geeksforgeeks.org/c-array-constrainedcopy-method/)

 **从指定的源索引处开始复制数组中的一系列元素，并将其粘贴到从指定的目标索引处开始的另一个数组中。保证如果复制没有完全成功，所有更改都将被撤消。

数组。ConstrainedCopy(srcArr，0，destArr，3，5)；

其中 srcArr 是源数组，

0 是复制应该开始的起始索引，

destArr 是目标数组，

3 是复制应该在目标数组中开始的位置，

5 是要复制的元素数

[](https://www.geeksforgeeks.org/c-converting-an-array-of-one-type-to-an-array-of-another-type/)

 **将一种数据类型的数组转换为另一种数据类型的数组。

conArr =数组。ConvertAll(arrVal，新转换器<dtype1 dtype2="">(方法))；</dtype1>

**复制()**

将一个数组中的一系列元素复制到另一个数组，并根据需要执行类型转换和装箱。

数组。Copy(srcArr，destArr，2)；

将前两个元素从 srcArr 复制到 destArr

**CopyTo()**

将当前一维数组的所有元素复制到指定的一维数组中。

数组。CopyTo(destArr，4)；

复制从索引 4 开始

**CreateInstance()**

初始化 Array 类的新实例。

数组。CreateInstance(typeof(String)，长度)；

**空()**

返回一个空数组。

阿尔瓦尔。空()

[**等于()**](https://www.geeksforgeeks.org/c-check-if-an-array-object-is-equal-to-another-array-object/)

确定指定的对象是否等于当前对象。

阿尔瓦尔。等于(arr val 2)；

[**存在()**](https://www.geeksforgeeks.org/c-check-if-an-array-contain-the-elements-that-match-the-specified-conditions/)

确定指定数组是否包含与指定谓词定义的条件相匹配的元素。

数组。存在(srcArr，"<elementname>")；</elementname>

[**找到()**](https://www.geeksforgeeks.org/c-array-find-method/)

搜索与指定谓词定义的条件相匹配的元素，并返回整个数组中的第一个匹配项。

数组。Find(arrVal，<matching pattern="">)；</matching>

[**FindAll()**](https://www.geeksforgeeks.org/c-array-findall-method/)

检索与指定谓词定义的条件匹配的所有元素。

数组。FindAll(arrVal，<matching pattern="">)；</matching>

**FindIndex()**

搜索与指定谓词定义的条件匹配的元素，并返回数组或数组的一部分中第一个匹配项的从零开始的索引。

数组。FindIndex(arrVal，<matching pattern="">)；</matching>

**FindLast()**

搜索与指定谓词定义的条件相匹配的元素，并返回整个数组中最后一个匹配项。

数组。FindLast(arrVal，<matching pattern="">)；</matching>

**FindLastIndex()**

搜索与指定谓词定义的条件匹配的元素，并返回数组或数组的一部分中最后一个匹配项的从零开始的索引。

数组。FindLastIndex(arrVal，<matching pattern="">)；</matching>

**ForEach()**

循环遍历数组的每个元素并执行指定的操作

数组。ForEach(数组，动作)

[**【get 分子()**](https://www.geeksforgeeks.org/c-array-getenumerator-method/)

返回数组的 IEnumerator。

阿尔瓦尔。GetEnumerator()

**GetHashCode()**

默认哈希函数。

阿尔瓦尔。GetHashCode()

[**GetLength()**](https://www.geeksforgeeks.org/c-total-number-of-elements-present-in-an-array/)

获取一个 32 位整数，表示数组的指定维度中的元素数。

阿尔瓦尔。GetLength(i)其中 I 是一个整数

[](https://www.geeksforgeeks.org/total-number-of-elements-in-a-specified-dimension-of-an-array-in-c/)

 **获取一个 64 位整数，表示数组的指定维度中的元素数。

阿尔瓦尔。GetLongLength(i ),其中 I 是整数

[**【get power bound()**](https://www.geeksforgeeks.org/c-finding-the-index-of-first-element-in-the-array/)

获取数组中指定维度的第一个元素的索引。

阿尔瓦尔。GetLowerBound(i ),其中 I 是整数

gettype()

获取当前实例的类型。

阿尔瓦尔。GetType()

[**GetUpperBound()**](https://www.geeksforgeeks.org/c-finding-the-index-of-last-element-in-the-array/)

获取数组中指定维度的最后一个元素的索引。

阿尔瓦尔。GetUpperBound(i ),其中 I 是整数

**GetValue()**

获取当前数组中指定元素的值。

**IndexOf()**

搜索指定的对象，并返回它在一维数组或数组中某个元素范围内的第一个匹配项的索引。

arrVal.IndexOf(object)

**Initialize()**

通过调用值类型的默认构造函数来初始化值类型数组的每个元素。

[**LastIndexOf()**](https://www.geeksforgeeks.org/array-lastindexof-method-in-c-sharp-set-1/)

返回一维数组或数组的一部分中某个值的最后一个匹配项的索引。

arrVal.LastIndexOf(i)

**memberwisecolone()**

创建当前对象的浅表副本。

[**Resize()**](https://www.geeksforgeeks.org/c-how-to-change-the-size-of-one-dimensional-array/)

将一维数组的元素数更改为指定的新大小。

数组。调整大小(ref arrVal，len-2)；

其中 len 是数组的原始长度

**反转()**

反转一维数组或部分数组中元素的顺序。

阿尔瓦尔。反向()

**SetValue()**

将当前数组中的指定元素设置为指定值。

Array.SetValue(arrVal[i])

[**排序()**](https://www.geeksforgeeks.org/how-to-sort-an-array-in-c-sharp-array-sort-method-set-1/)

对一维数组中的元素进行排序。

数组。排序(数组)

**ToString()**

返回一个表示当前对象的字符串。
(从对象继承)

阿尔瓦尔。ToString()

[](https://www.geeksforgeeks.org/c-array-trueforall-method/)

 **确定数组中的每个元素是否与指定谓词定义的条件匹配。

数组。TrueForAll(arrVal，<matching pattern="">)</matching>

Determines whether every element in the array matches the conditions defined by the specified predicate.

Array.TrueForAll(arrVal, <matching pattern>)**************