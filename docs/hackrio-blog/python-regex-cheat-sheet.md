# 下载 Python 正则表达式备忘单 PDF 以供快速参考

> 原文：<https://hackr.io/blog/python-regex-cheat-sheet>

正则表达式或 Regex 是 Python 编程或任何其他编程语言的一个重要方面。它用于通过字符、单词和模式匹配文本字符串。它还使用一组字符来创建搜索模式。

你的主要目标？记住语法和如何形成模式。但是说起来容易做起来难。在 Python 编程中，记住 RegEx 各个方面的每个语法是很困难的。这就是 Python 正则表达式备忘单派上用场的地方。如果你正在为即将到来的面试做准备，参考这个正则表达式 Python 备忘单来加速你的研究。

[点击这里](https://drive.google.com/file/d/1XPcNtR8z9MvP7Mkcwyubd3T6Rc0fmNj6/view?usp=sharing)下载 Hackr.io 的 Python Regex 备忘单 PDF。

那么，我们开始吧。

## **Python 正则表达式备忘单**

在这个 Python 正则表达式备忘单中，我们将用一个简单的例子来解释它是如何工作的。

[元字符](https://www.ibm.com/docs/en/informix-servers/12.10?topic=matching-metacharacters)是正则表达式构建块。下表突出显示了 Python 正则表达式中的不同元字符，以及它们的描述和合适的示例:

| **字符** | **描述** | **例子** |
| [] | 一组字符 | "[上午]" |
| \ | 表示特殊序列(也可用于转义特殊字符) | " \d " |
| 。 | 任何字符(换行符除外) | “他..o " |
| ^ | 始于 | 《^hello》 |
| $ | 结尾为 | "行星$ " |
| * | 零次或多次出现 | “他。*o " |
| + | 一次或多次出现 | “他。+o " |
| ？ | 零或一次出现 | “他。？o " |
| {} | 精确指定的出现次数 | “他。{2}o " |
| &#124; | 要么…要么… | “瀑布&#124;停留” |
| () | 捕获和分组 |

让我们在下面详细讨论每个元字符。

#### **[]方括号**

它是一个字符类，有一组我们想要匹配的字符。

例如，字符类[abc]将匹配任何单个字符 a、b 或 c。您可以根据需要指定任何范围的字符。

例如:

*   [0，3]与[0123]相同
*   【a-c】和【abc】一样。

您可以使用 caret(^符号反转字符类。例如:

*   [^0-3]是指除 0、1、2 或 3 以外的任何数字
*   [^a-c]是指除 a、b 或 c 以外的任何字符

例如:

```
import re
txt = "The rain in Spain"
x = re.findall("[a-m]", txt)
print(x)
```

输出

```
['h', 'e', 'a', 'i', 'i', 'a', 'i']
```

#### **\反斜杠**

反斜杠(\)确保字符不会被特殊处理。它用于转义元字符。

例如，如果要搜索点(。)在字符串中，搜索到的点将被视为特殊字符。因此，您需要在点()前使用反斜杠(\)。)

例如:

```
import re
txt = "That will be 59 dollars"
#Find all digit characters:
x = re.findall("\d", txt)
print(x)
```

输出:

```
['5', '9']
```

#### **。-点号**

使用点符号，您只能匹配一个字符，换行符除外。

*   **a.b** 将检查在点的位置包含任何字符的字符串，如 acb、acbd、abbb 等
*   **..**将检查字符串是否包含至少两个字符

例如:

```
import re
txt = "hello planet"
#Search for a sequence that starts with "he", followed by two (any) characters, and an "o":
x = re.findall("he..o", txt)
print(x)
```

输出:

```
['hello']
```

#### **^脱字符号(开头为)**

脱字符号(^)允许您匹配字符串的开头。它检查字符串是否以特定字符开头。

例如:

*   ^g 会检查字符串是否以 g 开头，如 girl，globe，gym，g 等。
*   ^ge 会检查字符串是否以 ge 开头，如 gem、gel 等。

例如:

```
import re
txt = "hello planet"
#Check if the string starts with 'hello':
x = re.findall("^hello", txt)
if x:
 print("Yes, the string starts with 'hello'")
else:
 print("No match")
```

输出:

```
Yes, the string starts with 'hello'
```

#### **$美元(结尾为)**

美元($)符号允许您匹配字符串的结尾。它检查字符串是否以给定的字符结尾。

例如:

*   s$将检查以 a 结尾的字符串，如 sis、ends、s 等。
*   ks$将检查以 ks 结尾的字符串，如 seeks、disks、ks 等。

例如:

```
import re
txt = "hello planet"
#Check if the string ends with 'planet':
x = re.findall("planet$", txt)
if x:
 print("Yes, the string ends with 'planet'")
else:
 print("No match")
```

输出:

```
Yes, the string ends with 'world'
```

#### **·明星**

此符号将匹配*符号前的正则表达式的零次或多次出现。

例如:

*   ab*c 将与字符串 ac、abc、abbbc、dabc 等匹配。但是不会与 abdc 匹配，因为 b 后面没有 c。

例如:

```
import re
txt = "hello planet"
#Search for a sequence that starts with "he", followed by 0 or more (any) characters, and an "o":
x = re.findall("he.*o", txt)
print(x)
```

输出:

```
['hello']
```

#### **+加上**

该符号将匹配+符号前面的正则表达式的一个或多个实例。

例如:

*   ab+c 将与字符串 abc，abbc，dabc 匹配，但不会与 ac，abdc 匹配，因为 ac 中没有 b，并且在 abdc 中 b 后面没有 c。

例如:

```
import re
txt = "hello planet"
#Search for a sequence that starts with "he", followed by 1 or more (any) characters, and an "o":
x = re.findall("he.+o", txt)
print(x)
```

输出:

```
['hello']
```

#### **？问号**

这个符号将检查问号前的字符串是至少出现一次，还是根本不出现。

例如:

*   ab？c 将匹配字符串 ac、acb 和 dabc，但不会匹配 abbc，因为有两个 b。同样，它不会与 abdc 匹配，因为 b 后面没有 c。

例如:

```
import re
txt = "hello planet"
#Search for a sequence that starts with "he", followed by 0 or 1 (any) character, and an "o":
x = re.findall("he.?o", txt)
print(x)
```

输出:

```
[]
```

#### **{m，n}-大括号**

大括号匹配正则表达式前面从 m 到 n(包括 m 和 n)的任何重复。

例如:

*   a{2，4}将与字符串 aaab，baaaac，gaad 匹配，但不会与 abc，bc 等字符串匹配，因为在这两种情况下都只有一个 a 或没有 a。

例如:

```
import re
txt = "hello planet"
#Search for a sequence that starts with "he", followed excactly 2 (any) characters, and an "o":
x = re.findall("he.{2}o", txt)
print(x)
```

输出:

```
['hello']
```

#### **| -或**

“或”符号检查“或”符号之前或之后的模式是否出现在字符串中。

例如:

*   a|b 将匹配任何包含 a 或 b 的字符串，如 acd、bcd、abcd 等。

例如:

```
import re
txt = "The rain in Spain falls mainly in the plain!"
#Check if the string contains either "falls" or "stays":
x = re.findall("falls|stays", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
['falls']
Yes, there is at least one match!
```

#### **( < RegEx > )-组**

分组符号用于分组子模式。

例如:

*   (a|b)cd 将匹配 acd、abcd、gacd 等字符串。

## [![](img/38dbc41f2fc5629ecc718a565194ce3f.png)](https://datacamp.pxf.io/oeZvdm)

## **特殊序列**

在 RegEx Python 备忘单的这一部分，我们将用合适的例子讨论各种特殊序列。

| **字符** | **描述** | **例子** |
| \A | 如果指定的字符位于字符串的开头，则返回匹配项 | " \AThe " |
| \b | 返回指定字符位于单词开头或结尾的匹配项(开头的“r”确保字符串被视为“原始字符串”) | r " \贝恩"r"ain\b " |
| \B | 返回存在指定字符但不在单词开头(或结尾)的匹配项(开头的“r”确保字符串被视为“原始字符串”) | r"\Bain "r"ain\B " |
| \d | 返回字符串包含数字(从 0 到 9 的数字)的匹配项 | " \d " |
| \D | 返回字符串不包含数字的匹配项 | " \D " |
| \s | 返回字符串包含空白字符的匹配项 | " \s " |
| \S | 返回字符串中不包含空白字符的匹配项 | " \S " |
| \w | 返回字符串包含任何单词字符(从 a 到 Z 的字符、从 0 到 9 的数字和下划线 _ 字符)的匹配项 | " \w " |
| \W | 返回字符串不包含任何单词字符的匹配项 | " \W " |
| \Z | 如果指定的字符位于字符串的末尾，则返回匹配项 | "西班牙\Z " |

#### **\A**

```
import re
txt = "The rain in Spain"
#Check if the string starts with "The":
x = re.findall("\AThe", txt)
print(x)
if x:
 print("Yes, there is a match!")
else:
 print("No match")
```

输出:

```
['The']
Yes, there is a match!
```

#### **\b**

```
import re
txt = "The rain in Spain"
#Check if "ain" is present at the beginning of a WORD:
x = re.findall(r"\bain", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
#Check if "ain" is present at the end of a WORD:
x = re.findall(r"ain\b", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
[]
No match
['ain', 'ain']
Yes, there is at least one match!
```

#### **\B**

```
import re
txt = "The rain in Spain"
#Check if "ain" is present, but NOT at the beginning of a word:
x = re.findall(r"\Bain", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
['ain', 'ain']
Yes, there is at least one match!
```

#### **\d**

```
import re
txt = "The rain in Spain"
#Check if the string contains any digits (numbers from 0-9):
x = re.findall("\d", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
[]
No match
```

#### **\D**

```
import re
txt = "The rain in Spain"
#Return a match at every no-digit character:
x = re.findall("\D", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
['T', 'h', 'e', ' ', 'r', 'a', 'i', 'n', ' ', 'i', 'n', ' ', 'S', 'p', 'a', 'i', 'n']
Yes, there is at least one match!
```

#### **\s**

```
import re
txt = "The rain in Spain"
#Return a match at every white-space character:
x = re.findall("\s", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
[' ', ' ', ' ']
Yes, there is at least one match!
```

#### **\S**

```
import re
txt = "The rain in Spain"
#Return a match at every NON white-space character:
x = re.findall("\S", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
['T', 'h', 'e', 'r', 'a', 'i', 'n', 'i', 'n', 'S', 'p', 'a', 'i', 'n']
Yes, there is at least one match!
```

### **\w**

```
import re
txt = "The rain in Spain"
#Return a match at evry word character (characters from a to Z, digits from 0-9, and the underscore _ character):
x = re.findall("\w", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
['T', 'h', 'e', 'r', 'a', 'i', 'n', 'i', 'n', 'S', 'p', 'a', 'i', 'n']
Yes, there is at least one match!
```

#### **\W**

```
import re
txt = "The rain in Spain"
#Return a match at every NON word character (characters NOT between a and Z. Like "!", "?" white-space etc.):
x = re.findall("\W", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
[' ', ' ', ' ']
Yes, there is at least one match!
```

#### **\Z**

```
import re
txt = "Te rain in Spain"
#Check if the string ends with "Spain":
x = re.findall("Spain\Z", txt)
print(x)
if x:
 print("Yes, there is a match!")
else:
 print("No match")
```

输出:

```
['Spain']
Yes, there is a match!
```

### **设置**

这是一组用方括号[]括起来的字符，具有特殊的含义。在 Python 正则表达式备忘单的这一部分，我们将用例子解释所有集合类型。

#### **【arn】**

这将返回其中一个指定字符(a、r 或 n)存在的匹配项。

例如:

```
import re
txt = "The rain in Spain"
#Check if the string has any a, r, or n characters:
x = re.findall("[arn]", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
['r', 'a', 'n', 'n', 'a', 'n']
Yes, there is at least one match!
```

#### **【a-n】**

这将返回任何小写字符的匹配，按字母顺序在 a 和 n 之间。

例如:

```
import re
txt = "The rain in Spain"
#Check if the string has any characters between a and n:
x = re.findall("[a-n]", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
['h', 'e', 'a', 'i', 'n', 'i', 'n', 'a', 'i', 'n']
Yes, there is at least one match!
```

#### **【^arn】**

这将返回除 a、r 和 n 之外的任何字符的匹配。

例如:

```
import re
txt = "The rain in Spain"
#Check if the string has other characters than a, r, or n:
x = re.findall("[^arn]", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
['T', 'h', 'e', ' ', 'i', ' ', 'i', ' ', 'S', 'p', 'i']
Yes, there is at least one match!
```

**【0123】**

这将返回包含任何指定数字(0、1、2 或 3)的匹配结果。

例如:

```
import re
txt = "The rain in Spain"
#Check if the string has any 0, 1, 2, or 3 digits:
x = re.findall("[0123]", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
[]
No match
```

#### **【0-9】**

这将返回 0 到 9 之间任何数字的匹配结果。

例如:

```
import re
txt = "8 times before 11:45 AM"
#Check if the string has any digits:
x = re.findall("[0-9]", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
['8', '1', '1', '4', '5']
Yes, there is at least one match!
```

#### **【0-5】【0-9】**

这将返回从 00 到 59 的任何两位数的匹配。

例如:

```
import re
txt = "8 times before 11:45 AM"
#Check if the string has any two-digit numbers, from 00 to 59:
x = re.findall("[0-5][0-9]", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
['11', '45']
Yes, there is at least one match!
```

 **这将返回 a 和 z 之间字母顺序的任何字符的匹配，小写或大写。

例如:

```
import re
txt = "8 times before 11:45 AM"
#Check if the string has any characters from a to z lower case, and A to Z upper case:
x = re.findall("[a-zA-Z]", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
['t', 'i', 'm', 'e', 's', 'b', 'e', 'f', 'o', 'r', 'e', 'A', 'M']
Yes, there is at least one match!
```

#### **[+]**

在集合中，+，*，。，|，()，$，{}没有特殊含义。所以，[+]的意思是:返回字符串中任意+字符的匹配。

例如:

```
import re
txt = "8 times before 11:45 AM"
#Check if the string has any + characters:
x = re.findall("[+]", txt)
print(x)
if x:
 print("Yes, there is at least one match!")
else:
 print("No match")
```

输出:

```
[]
No match
```

### **Python 中的 Regex 模块**

Python 附带了一个名为‘re’的模块。你一定注意到了在上面的例子中我们导入了模块“re”。该模块由几个功能组成，可帮助您执行各种操作。

#### **findall()函数**

这是“re；”的内置函数处理正则表达式的模块。

语法:

```
re.findall(pattern, string, flags=0)
```

*   模式是正则表达式。
*   字符串是用户提供的输入字符串。
*   标志用于修改标准模式行为。

从左到右计算每个字符串，并在字符串中查找所有匹配的模式。然而，结果取决于模式。

*   如果模式**没有捕获组**，findall()函数返回匹配整个模式的字符串列表。
*   如果模式有**个捕获组**，findall()函数返回与该组匹配的字符串列表。
*   如果模式有**多个捕获组**，findall()函数返回匹配这些组的字符串元组。
*   值得注意的是，非捕获组不会影响返回结果的形式。

例如:

*   **获取匹配字符串的列表**

```
import re
s = "black, blue and brown"
pattern = r'bl\w+'
matches = re.findall(pattern,s)
print(matches)
```

输出:

```
['black', 'blue']
```

*   **单组图案**

```
import re
s = "black, blue and brown"
pattern = r'bl(\w+)'
matches = re.findall(pattern,s)
print(matches)
```

输出:

```
['ack', 'ue']
```

*   **多组图案**

```
import re
s = "black, blue and brown"
pattern = r'(bl(\w+))'
matches = re.findall(pattern,s)
print(matches)
```

输出

```
[('black', 'ack'), ('blue', 'ue')]
```

*   **使用正则表达式标志**

```
import re
s = "Black, blue and brown"
pattern = r'(bl(\w+))'
matches = re.findall(pattern, s, re.IGNORECASE)
print(matches)
```

输出:

```
[('Black', 'ack'), ('blue', 'ue')]
```

#### **finditer()函数**

使用这个函数，您可以匹配字符串中的模式，并返回一个迭代器，产生所有非重叠匹配的匹配对象。

语法:

```
re.finditer(pattern, string, flags=0)
```

*   模式是正则表达式。
*   字符串是用户提供的输入字符串。
*   标志是可选的，默认为零。它接受一个或多个正则表达式标志。flags 参数更改正则表达式引擎匹配模式的方式。

例如:

```
import re
s = 'Readability counts.'
pattern = r'[aeoui]'
matches = re.finditer(pattern, s)
for match in matches:
 print(match)
```

输出:

```
<re.Match object; span=(1, 2), match='e'>
<re.Match object; span=(2, 3), match='a'>
<re.Match object; span=(4, 5), match='a'>
<re.Match object; span=(6, 7), match='i'>
<re.Match object; span=(8, 9), match='i'>
<re.Match object; span=(13, 14), match='o'>
<re.Match object; span=(14, 15), match='u'>
```

### **搜索()功能**

search()函数从左到右扫描字符串，找到模式产生匹配的第一个位置。如果搜索成功，它返回一个匹配对象，否则返回 None。

语法:

```
re.search(pattern, string, flags=0)
```

*   模式是正则表达式。
*   字符串是用户提供的输入字符串。
*   标志用于修改模式的标准模式行为。

例如:

```
import re
s = 'Python 3 was released on Dec 3, 2008'
pattern = '\d+'
match = re.search(pattern, s)
if match is not None:
 print(match.group())
else:
 print('No match found')
```

输出

```
re.Match object; span=(7, 8), match='3'>
```

*   **找到匹配模式的第一个单词**

```
import re
s = 'CPython, IronPython, or Cython'
pattern = r'\b((\w+)thon)\b'
match = re.search(pattern, s)
if match is not None:
 print(match.groups())
```

输出:

```
('CPython', 'CPy')
```

模式 r'\b((\w+)thon)\b '有两个捕获组:

*   (\ w+)–捕获单词开头的字符。
*   ((\ w+)thon)-捕获整个单词。

search()函数返回找到匹配项的第一个位置。

#### **fullmatch()函数**

如果整个字符串匹配正则表达式的搜索模式，该函数将返回一个 match 对象，否则不返回任何对象。

语法:

```
re.fullmatch(pattern, string, flags=0)
```

*   模式是正则表达式。
*   字符串是用户提供的输入字符串。
*   标志是可选的，默认为零。它接受一个或多个正则表达式标志。flags 参数更改正则表达式引擎匹配模式的方式。

例如:

*   **验证电子邮件地址**

```
import re
email = 'no-reply@pythontutorial.net'
pattern = r'[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}'
match = re.fullmatch(pattern, email)
if match is not None:
 print(f'The email "{match.group()}" is valid')
else:
 print(f'The email "{email}"" is not valid')
```

输出:

```
The email "no-reply@pythontutorial.net" is valid.
```

#### **Match()函数**

re 模块的 match 函数允许您在字符串的开头搜索一个模式。

语法:

```
re.match(pattern, string, flags=0)
```

*   模式是正则表达式。
*   字符串是用户提供的输入字符串。
*   标志用于修改模式的标准行为。

例如:

*   **检查字符串是否以数字开头。**

```
import re
s = '3 pieces cost 5 USD'
pattern = r'\d{1}'
match = re.match(pattern, s)
if match is not None:
 print(f'The string starts with a digit {match.group()}')
```

输出:

```
The string starts with a digit 3
```

#### **Sub()函数**

re 模块的这个函数允许你处理正则表达式。

语法:

```
re.sub(pattern, repl, string, count=0, flags=0)
```

*   模式是正则表达式或模式对象。
*   Repl 是替代品。
*   字符串是用户提供的输入字符串。
*   Count 参数指定 sub()函数应该替换的最大匹配数。如果您传递零或跳过它，sub()函数将替换所有匹配。
*   Fags 是一个或多个用于修改标准模式行为的正则表达式标志。

它将在字符串中搜索模式，并用替换(repl)替换匹配的字符串。如果 sub()函数找不到匹配，它将返回原始字符串。否则，sub()函数将在替换匹配项后返回字符串。

例如:

*   **将电话号码(212)-456-7890 转换为 2124567890**

```
import re
phone_no = '(212)-456-7890'
pattern = '\D'
result = re.sub(pattern, '',phone_no)
print(result)
```

输出:

```
2124567890
```

*   **替换模式最左边的非重叠出现**

```
import re
pattern = '00'
s = '00000'
result = re.sub(pattern,'',s)
print(result)
```

输出:

```
0
```

```
import re
s = 'Make the World a *Better Place*'
pattern = r'\*(.*?)\*'
replacement = r'<b>\1<\\b>'
html = re.sub(pattern, replacement, s)
print(html)
```

输出:

```
Make the World a <b>Better Place<\b>
```

#### **Subn()函数**

这个函数在所有方面都与 sub()相似，只是它提供输出的方式不同。它返回一个元组，包含替换和新字符串的总数，而不仅仅是字符串。

语法:

```
re.subn(pattern, repl, string, count=0, flags=0)
```

例如:

```
import re
print(re.subn('ub', '~*', 'Subject has Uber booked already'))
t = re.subn('ub', '~*', 'Subject has Uber booked already',
 flags=re.IGNORECASE)
print(t)
print(len(t))
# This will give same output as sub() would have
print(t[0])
```

输出:

```
('S~*ject has Uber booked already', 1)
('S~*ject has ~*er booked already', 2)
Length of Tuple is: 2
S~*ject has ~*er booked already
```

#### **escape()函数**

这个函数将返回一个包含所有非字母数字反斜杠的字符串。如果您想要匹配其中可能包含正则表达式元字符的任意文字字符串，这将非常有用。

语法:

```
re.escape(string)
```

例如:

```
import re
print(re.escape("This is Awesome even 1 AM"))
print(re.escape("I Asked what is this [a-9], he said \t ^WoW"))
```

输出:

```
This\ is\ Awesome\ even\ 1\ AM
I\ Asked\ what\ is\ this\ \[a\-9\]\,\ he\ said\ \ \ \^WoW
```

#### **编译()函数**

这个函数将把正则表达式编译成模式对象，这些对象具有用于各种操作的方法，比如搜索模式匹配或执行字符串替换。

语法:

```
re.compile(string)
```

例如:

```
import re
p = re.compile('[a-e]')
# findall() searches for the Regular Expression
# and return a list upon finding
print(p.findall("Aye, said Mr. Gibenson Stark"))
```

输出:

```
['e', 'a', 'd', 'b', 'e', 'a']
```

#### **Split()函数**

它通过正则表达式的匹配来拆分字符串。

语法:

```
split(pattern, string, maxsplit=0, flags=0)
```

*   模式是正则表达式。
*   字符串是用户提供的输入字符串。
*   标志是可选的，默认为零。它接受一个或多个正则表达式标志。flags 参数更改正则表达式引擎匹配模式的方式。
*   maxsplit 确定最多发生几次拆分。通常，如果 maxsplit 为 1，那么结果列表将包含两个元素。如果 maxsplit 是 2，那么结果列表将有 3 个元素，依此类推。

例如:

*   **拆分句子中的单词**

```
import re
s = 'A! B. C D'
pattern = r'\W+'
l = re.split(pattern, s)
print(l)
```

输出

```
['A', 'B', 'C', 'D']
```

```
import re
s = 'A! B. C D'
pattern = r'(\W+)'
l = re.split(pattern, s, 2)
print(l)
```

输出

```
['A', '! ', 'B', '. ', 'C D']
```

## **组**

组是包含在括号()元字符中的正则表达式的一部分。

| **表情** | **解释** |
| ( ) | 匹配括号内的表达式，并根据需要对其进行分组以进行捕获 |
| (?#…) | 阅读评论 |
| (?PAB) | 匹配表达式 AB，可以用组名检索该表达式。 |
| (?:A) | 匹配由表示的表达式，但之后无法检索。 |
| (?p =组) | 匹配先前名为“group”的组所匹配的表达式 |

例如:

```
import re
example = (re.search(r"(?:AB)","ACABC"))
print(example)
print(example.groups())
result = re.search(r"(\w*), (\w*)","seeks, zest")
print(result.groups())
```

输出:

```
<re.Match object; span=(2, 4), match='AB'>
()
('seeks', 'zest')
```

## **断言**

在 Python RegEx 中，我们使用 Lookahead 作为断言。它决定了模式是否在解析器当前位置的右边。

| **表情** | **解释** |
| 一(？=B) | 仅当表达式 A 后跟 b 时，才匹配表达式 A。(正向前瞻断言) |
| 一(？！b) | 仅当表达式 A 后面没有 b 时，才匹配表达式 A。(负的前瞻断言) |
| (?< =B)A | 仅当 B 紧挨着表达式 A 的左侧时，才匹配表达式 A。(断言背后的积极因素) |
| (? | 仅当 B 不在其左侧时，才匹配表达式 A。(断言背后的负面看法) |

例如:

```
import re
print(re.search(r"z(?=a)", "pizza"))
print(re.search(r"z(?!a)", "pizza"))
```

输出

```
<re.Match object; span=(3, 4), match='z'>
<re.Match object; span=(2, 3), match='z'>
```

## **标志或修饰符**

| **表情** | **解释** |
| a | 仅匹配 ASCII |
| 我 | 忽略大小写 |
| L | 区域设置字符类 |
| m | ^和$匹配行的开始和结束(多行) |
| s | 匹配包括换行符在内的所有内容 |
| u | 匹配 unicode 字符类 |
| x | 允许空格和注释(详细) |

例如:

```
import re
exp = """hello you
I am from
Hoolywood"""
print(re.search(r"and", "Sun And Moon", flags=re.IGNORECASE))
print(re.findall(r"^\w", exp, flags = re.MULTILINE))
```

输出:

```
<re.Match object; span=(4, 7), match='And'>
['h', 'I', 'H']
```

## 结论

在这个正则表达式备忘单中，您将可以访问无数的语法、解释和示例来增强 Python 正则表达式的学习。

准备好学习所有关于 RegEx 的知识并充分利用它了吗？[上个正则表达式教程！](https://hackr.io/tutorials/learn-regular-expressions-regex)

推荐 Python 课程

### [用 Python 完成从零到英雄的 Python boot camp](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fcomplete-python-bootcamp%2F)**