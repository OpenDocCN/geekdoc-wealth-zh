# 下载 JavaScript 备忘单 PDF 供您参考[更新]

> 原文：<https://hackr.io/blog/javascript-cheat-sheet>

## **Javascript 是什么？**

Javascript 是浏览器支持的客户端脚本语言。通常，当客户做一个动作时，会涉及到 JavaScript 函数，例如，提交表单、悬停鼠标、滚动等。由于 JS 代码的存在，网页变得更加生动、动态和交互式。

## **下载 JavaScript 备忘单**

**在这里，您可以使用快速指南或 JS 备忘单，它们将帮助您了解更多关于快捷方式和技巧的信息:**

要在页面上包含 javascript 代码，语法是–

```
<script type = “text/javascript”> 
// all the code
</script>
```

要创建单独的文件，使用**扩展名**。js 并在页面上包含该文件，格式为–

```
<script src="myjsfile.js"></script>
```

| **备注**单线多线 | 有两种类型的注释://这是单行注释/*当你必须写很多东西的时候，这是多行注释*/ |
| **变量**–保存数据以执行计算或其他操作的值 | 

*   var–使用最广泛。可以在声明的函数中访问。可以重新分配。
*   const–常量值，即不能重新分配
*   let–只能在其声明的块内使用，可以被重新分配

 |
| **数据类型** | 可以是不同的类型

*   数字，例如 var id = 20
*   未赋值变量，如变量 x
*   字符串，例如 var company = "hackr "
*   Boolean，如 windowopen = true
*   常数。例如，常量计数器= 1
*   操作，例如 var sum = 20 + 20
*   对象，例如 var student =

 |
| **物体** | 包含各种数据类型的单个对象，例如，var student =； |

### **数组**

数组将相似类型的数据组合在一起。Eg，var subjectlist = ["数学"，"科学"，"历史"，"计算机"]；阵列可以执行以下功能:

| **功能** | **描述** |
| concat() | 将不同的数组连接成一个数组。 |
| 加入() | 将一个数组的所有元素连接成一个字符串 |
| indexof() | 返回数组中元素的索引(第一个位置) |
| lastindexof() | 返回元素在数组中的最后一个位置 |
| 排序() | 数组元素的字母排序 |
| 反向() | 按降序排列元素 |
| 的值() | 指定元素的原始值 |
| 切片() | 剪切一个数组的一部分，放入一个新的数组中 |
| 拼接() | 以特定的方式和位置向数组中添加元素 |
| 未移位() | 开始时向数组中添加新元素 |
| shift() | 移除数组的第一个元素 |
| 流行() | 移除数组的最后一个元素 |
| 推送() | 将新元素作为最后一个元素添加到数组中 |
| tostring() | 打印数组元素的字符串值 |

### **操作员**

| **基础** | 加法(+)

*   减法(-)
*   乘法(*)
*   除法(/)
*   余数(%)
*   增量(++)
*   减量(-)
*   首先执行括号(…)
*   **逻辑**

 |
| **比较** | 等于(==) |
| 相等的值和类型(===) | 不等于(！=)

*   不相等的值或类型(！==)
*   大于(>)
*   小于(
*   大于或等于(> =)
*   小于或等于(< =)
*   三元运算符(？)
*   **按位**
*   和(&)
*   或者(&#124;)

 |
| 不是(~) | 异或(^)

*   左移(<
*   右移(>>)
*   零填充右移(>>>)
*   **功能**
*   一组任务可以在单个功能中执行。例如，
*   **输出数据**
*   警报()

 |

### 在一个小的弹出窗口中显示一些输出(警告框)

document.write()

```
function add(a, b){// code} 
```

将输出写入 html 文档

| console.log() | 主要用于调试，在浏览器控制台上写输出 |
| 提示() | 使用对话框提示用户输入 |
| 确认() | 以是/否打开对话框，并根据用户点击返回真/假 |
| **全局函数** | encodeURI() |
| 将 URI 编码成 UTF 8 | 

```
var uri = “hackr.io/blog”;
var enc = encodeURI(uri);
```

 |

### encodeURIComponent()

| URI 组件的编码 | 

```
var uri = “hackr.io/blog”;
var enccomp = encodeURIComponent(uri);
```

 | decodeURI() |
| 解码由 encodeURI 或类似软件创建的[统一资源标识符(URI)](https://en.wikipedia.org/wiki/Uniform_Resource_Identifier) | 

```
var dec = decodeURI(enc);
```

 | decodeURIComponent() |
| 解码 URI 分量 | 

```
var decomp = decodeURIComponent(enccomp);
```

 | parseInt() |
| 解析输入返回一个整数 | 

```
var a = parseInt(“2003 monday”);
```

 | 解析浮点() |
| 分析输入并返回一个浮点数 | 

```
var b = parseFloat(“23.333”);
```

 | eval() |
| 评估表示为字符串的 javascript 代码 | 

```
var x = eval(“2 * 2”);
```

 | 数字() |
| 返回一个从初始值转换而来的数字 | 

```
var y = new Date();
var z = Number(y);
```

 | isNaN() |
| 确定一个值是否为 NaN | 

```
isNan(25);
```

 | 无限的 |
| 确定传递的值是否为有限数字 | 

```
isFinite(-245);
```

 | 推荐 JavaScript 课程 |
| 【JavaScript 全教程 2023:从零到专家！ | **循环** | 为 |

### javascript 中的循环

```
var i;
for (i = 0; i < 5; i++
{ // code}
```

### 在…期间

| 当某个条件为真时执行代码块 | 

```
while (product.length > 5)
{// some code}
```

 | 做…的同时 |
| 类似于 while，但至少在代码执行后应用条件时执行 | 

```
do {
// code
}while (condition){
}
```

 | 破裂 |
| 根据某些条件中断并退出循环 | 

```
if (i <10)
    break;
```

 | 继续 |
| 如果满足某些条件，则继续下一次迭代 | 

```
if (j>10)
  continue;
```

 | **if-else 语句** |
| if-else 允许您设置各种条件– | **字符串方法** | **方法** |

### **意为**

**例子**

```
if (condition 1)
{
 //execute this code
} else if (condition 2)
{
 // execute new code
} else
{
 // execute if no other condition is true
}
```

### 长度

| 字符串的确定长度 | 

```
var a = “hackr.io”;
a.length;
```

 | indexof() |
| 查找字符串中某个字符或文本第一次出现的位置 | 

```
var a = “hackr.io is nice website”;
var b = a.indexof(“nice”);
```

 | lastindexof() |
| 返回字符串中最后一次出现的文本 | 

```
var a = “hackr.io is nice website”;
var b = a.indexof(“nice”, 6);
```

 | 搜索() |
| 搜索并返回指定值在字符串中的位置 | var a = "hackr.io 是个不错的网站"；var b = a . search(" nice ")； | 切片() |
| 提取并返回一个字符串的一部分作为另一个新字符串 | 

```
var a = “hackr.io is nice website”;
var b = a.slice(13); will return nice website.
```

 | 

```
substring()
```

 |
| substring 返回从指定的起始索引到结束索引的部分字符串。与 slice()不同，不能接受负值 | 

```
var a = “hackr.io is nice website”;
var b = a.substring(0, 7);
```

 | substr() |
| 返回字符串的切片部分，第二个参数是最终字符串的长度。 | 

```
var a = “hackr.io is nice website”;
var b = a.substr(13, 8);
```

 | 替换() |
| 用另一个值替换一个特定值 | 

```
var a = “hackr.io is nice website”;
var b = a.replace(“nice”, “good”);
```

 | touppercase() |
| 将所有字符改为大写 | 

```
var a = “hackr.io is nice website”;
var b = a.touppercase (a);
```

 | tolowercase() |
| 将所有字符变为小写 | 

```
var a = “hackr.io is nice website”;
var b = a.tolowercase(a);
```

 | concat() |
| 将两个或多个字符串连接成另一个字符串 | 

```
var a = “my name is”;
var b = “john”;
var c = a.concat(“: ”, b);
```

 | 修剪() |
| 删除字符串中的空格 | 

```
var a = “       hi, there!         ”;
a.trim();
```

 | 夏拉特() |
| 在指定位置查找字符 | a.charat(1)将返回一个 | charcodeat() |
| 返回指定位置的 unicode 字符 | 将返回 72 | 

```
var a = “hackr.io”;
```

拆分() |
| 根据特殊字符将字符串转换为数组 | 将返回一个由 h，a，c，k，r 等字符组成的数组.. | 

```
“hackr”.charcodeat(0); 
```

使用[]访问字符 |
| 使用索引访问字符串中的字符(在 ie 的某些版本上不起作用) | 

```
var a = “hackr.io”;
a[2] will return c
```

 | 

```
var a = “hackr.io”;
var arr = a.split(“”);
```

**转义字符** |
| \' | 单引号 | \" |

### 双引号

| \\ | 单反斜线 |
| \b | 退格 |
| \f | 换页 |
| \n | 换行 |
| \t | 横表 |
| \v | 垂直标签 |
| \r | 回车 |
| **正则表达式** | 正则表达式可以是模式修饰符、元字符、量词和括号的形式。**图案修改器** |
| e | 评估替换 |

### 我

不区分大小写的匹配

| g | 全局匹配–查找所有匹配 |
| m | 多行匹配 |
| s | 将字符串视为一行 |
| x | 模式中允许注释和空白 |
| u | 不整齐的图案 |
| **括号** | [abc] |
| 找出括号中的任何字符 | [^abc] |

### 找出不在括号中的任何字符

| [0-9] | 用于查找从 0 到 9 的任何数字 |
| [A-z] | 查找从大写 A 到小写 z 的任意字符 |
| (甲&#124;乙&#124;丙) | 寻找任何以&#124; |
| .  | 查找除换行符或行结束符之外的单个字符 |
| \w | 单词字符 |

| \W | 非文字字符 |
| \d | 一个数字 |
| \D | 非数字字符 |
| \s | 空白字符 |
| \S | 非空白字符 |
| \b | 在单词的开头/结尾查找匹配项 |
| \B | 不在单词开头/结尾的匹配 |
| \0 | 零字符 |
| \n | 新的行字符 |
| \f | 换页符 |
| \r | 回车字符 |
| \t | 制表符 |
| \v | 垂直制表符 |
| \xxx | 由八进制数 xxx 指定的字符 |
| \xdd | 由十六进制数字 dd 指定的字符 |
| \uxxxx | 十六进制数字 xxxx 指定的 Unicode 字符 |
| **量词** | n+ |
| 匹配至少包含一个“n”的字符串 | n* |

### 包含零个或多个 n 的任何字符串

| n？ | 没有或只有一次 n 的字符串 |
| n | 包含一系列 X n 的字符串 |
| n | 包含 X 到 Y n 序列的字符串 |
| n | 匹配至少有 X n 个序列的字符串 |
| n 美元 | 任何以 n 结尾的字符串 |
| n | 以 n 开头的字符串 |
| ？=n | 后面跟有字符串 n 的任何字符串 |
| ？！n | 后面没有字符串 n 的字符串 |
| **数字** | **数字属性** |
| 

&#124; MAX _ VALUE &#124; JavaScript 中可以表示的最大数值 &#124;
&#124; MIN _ VALUE &#124; JavaScript 中可能的最小正数值 &#124;
&#124; NaN &#124; 非数字 &#124;
&#124; 负无穷大 &#124; 负无穷大值 &#124;
&#124;  &#124;

 | 最大值 |

### JavaScript 中可以表示的最大数值

| 最小值 | JavaScript 中可能的最小正数值 |
| **例子** | toexponentail_) |
| LN2 | 以 2 为底的自然对数 |
| 返回 x 的绝对值(正值) | 助理文书主任(十) |

### 创建自定义日期对象。格式-(年、月、日、时、分、秒、毫秒)。除了年份和月份，所有参数都是可选的。

| 日期(“2019-10-21”) | 字符串形式的日期声明 |
| getDate() | 以数字(1-31)的形式获取一个月中的某一天 |
| getDay() | 以数字表示的工作日(0-6) |
| getFullYear() | 四位数的年份(yyyy) |
| getHours() | 获取小时数(0-23) |
| getMilliseconds() | 获取毫秒数(0-999) |
| getMinutes() | 获取分钟数(0-59) |
| getMonth() | 数字形式的月份(0-11) |
| getSeconds() | 获得第二名(0-59) |
| getTime() | 获取自 1970 年 1 月 1 日以来的毫秒数 |
| getUTCDate() | 根据世界时(也可用于日、月、整年、小时、分钟等)指定日期中的某一天(日期)。) |
| 从语法上分析 | 分析日期的字符串表示形式并返回数字 |
| setDate() | 将日期设置为数字(1-31) |
| setFullYear() | 设置年份(可选月和日) |
| 设置时间() | 设置小时(0-23) |
| setMilliseconds() | 设置毫秒数(0-999) |
| setMinutes() | 设置分钟数(0-59) |
| setMonth() | 设置月份(0-11) |
| setSeconds() | 设置秒数(0-59) |
| 塞蒂默 | 设置时间(自 1970 年 1 月 1 日起的毫秒数) |
| setUTCDate() | 根据世界时(也可用于日、月、整年、小时、分钟等)设置指定日期的日期。) |
| **DOM 模式** | **D** 文档 **O** 对象 **M** 模型)是页面结构的代码。HTML 元素(称为节点)可以使用 JavaScript 轻松操作。 |
| **节点属性** | 

&#124; 属性 &#124; 返回注册到元素的所有属性 &#124;
&#124; base uri &#124; 提供 HTML 元素的绝对基 URL &#124;
&#124; nodeName &#124; 节点名 &#124;
&#124; nodeType &#124; 节点类型 &#124;
&#124; nodeValue &#124;  &#124;
&#124; childNodes &#124; 一个元素的所有子节点 &#124;
&#124; first child &#124; 一个元素的第一个子节点 &#124;
&#124; last child &#124; 一个元素的最后一个子节点 &#124;
&#124; owner document &#124; 此(当前)的顶层文档对象 节点 &#124;
&#124; 上一个同级节点 &#124; 上一个同级节点 &#124;
&#124; 下一个同级节点 &#124; 同一节点树中的下一级节点 &#124;
&#124; 文本内容 &#124; 设置或返回一个节点及其后代 &#124;

的文本内容 |

### 属性

返回注册到元素的所有属性

| baseURI | 提供 HTML 元素的绝对基 URL |
| compareDocumentPosition() | 比较两个元素的文档位置 |
| getAttributeNS() | 返回具有指定命名空间和名称的属性的字符串值 |

### 检查窗户是否已经关闭

| 默认状态 | 设置或获取 windows 状态栏中的默认文本 |
| 模糊() | 从当前窗口中移除焦点 |
| 有效宽度 | 返回屏幕的宽度(不包括 Windows 任务栏) |

### onmouseover

#### 当鼠标移到一些柠檬或它的子代上时

| onmouseout | 用户将鼠标指针移出元素或其子元素 |
| 是 mouseup | 当用户在元素上释放鼠标按钮时 |
| onmousedown | 当用户在元素上按下鼠标按钮时 |
| onmouseenter | 指针移动到元素上 |
| onmouseleave | 指针移出元素 |
| onmousemove | 当指针在元素上时，它正在移动 |
| oncontextmenu | 用户右键单击元素打开上下文菜单 |
| ondblclick(点击鼠标) | 用户双击一个元素 |
| **2。键盘** | onkeydown |
| 当用户按下按键时 | onkeypress |

#### 当用户开始按键时

| onkeyup | 用户释放一个键 |
| **3。框架** | 奥纳博特 |
| 媒体加载被中止 | onbeforeunload |

#### 在卸载文档之前发生的事件

| 和他一起上传 | 事件在页面卸载后发生 |
| 不良事件 | 当加载外部文件时出现错误时 |
| onhashchange | URL 的锚定部分发生了更改 |
| 装载 | 当一个对象被加载时 |
| onpagehide | 用户导航离开网页 |
| onpageshow | 用户导航到网页 |
| onresize | 调整文档视图的大小 |
| onscroll | 元素的滚动条正在滚动 |
| **4。表单** | onblur |
| 当一个元素失去焦点时 | 昂哥 |

#### 当、<select>、</select><textarea>等表单元素的内容发生变化时</textarea>

| 专注 | 一个元素获得焦点 |
| onfocusin | 当一个元素将要获得焦点时 |
| 我很担心 | 当元素将要失去焦点时 |
| oninput | 元素上的用户输入 |
| on 无效 | 一个元素无效 |
| onreset | 表单重置 |
| 在线搜索 | 用户在输入类型搜索中写一些东西 |
| onselect | 用户选择一些文本(和<textarea>)</textarea> |
| 昂松宾 | 提交表单时发生的事件 |
| **5。拖动** | 翁德拉格 |
| 一个元素被拖动 | ondrop |

#### 被拖动的元素被拖放到拖放目标上

| ondragstart | 用户开始拖动元素 |
| 不可忍受 | 用户已经完成了元素的拖动 |
| 翁德拉贡特 | 被拖动的元素进入放置目标 |
| 软骨叶 | 被拖动的元素离开放置目标 |
| 翁德拉戈弗 | 被拖动的元素位于拖放目标的顶部 |
| **6。剪贴板** | oncut |
| 用户剪切元素内容时发生的事件 | oncopy |

#### 用户复制元素内容时发生的事件

| 粘贴时 | 用户粘贴元素内容时发生的事件 |
| 奥纳博特 | 媒体加载被中止 |
| 统一的 | 媒体结束了 |

| 不良事件 | 当加载外部文件时出现错误时发生 |
| 在线播放 | 浏览器可以开始播放媒体 |
| 在线播放 | 浏览器可以不间断地播放媒体 |
| 老化变化 | 媒体持续时间的变化 |
| onloadeddata | 媒体数据已加载 |
| onloadedmetadata | 加载元数据(例如维度、持续时间) |
| onloadstart | 浏览器开始查找指定的媒体 |
| 暂停 | 媒体由用户暂停或自动暂停 |
| monplay | 媒体开始播放或不再暂停 |
| 播放中 | 暂停或停止缓冲后，媒体正在播放 |
| onprogress | 浏览器正在下载媒体 |
| 最新变化 | 媒体的播放速度会改变 |
| 被发现 | 用户已完成移动/跳转到媒体中的新位置 |
| 观察 | 用户开始移动/跳跃 |
| 安装 | 浏览器正在尝试加载媒体，但它不可用 |
| 等待中 | 媒体暂停，但预计会恢复(如在缓冲中) |
| 暂停 | 浏览器故意不加载媒体 |
| 按时更新 | 播放位置已经改变(如在快进的情况下) |
| on volume exchange | 媒体音量增加或减少 |
| **8。动画** | 动画开始 |
| CSS 动画开始 | 动画结束 |

#### CSS 动画结束

| 动画迭代 | CSS 动画播放完毕 |
| **9。其他** | 过渡结束 |
| CSS 转换完成时触发的事件 | onmessage |

#### 通过事件源接收消息

| ononline | 浏览器开始在线工作 |
| 离线 | 浏览器开始脱机工作 |
| ontoggle | 用户打开或关闭<details>元素</details> |
| onpopstate | 当窗口的历史改变时 |
| 昂秀 | 一个

<menu>元素显示为上下文菜单</menu>

 |
| 储存 | 更新网络存储区域 |
| 车轮上 | 鼠标滚轮在元素上上下滚动 |
| ontouchstart | 手指放在触摸屏上 |
| ontouchend | 用户的手指从触摸屏上移开 |
| ontouchcancel | 屏幕触摸被中断 |
| ontouchmove | 用户手指在屏幕上拖动 |
| 10。错误 | 尝试 |
| 没有错误时要执行的代码块 | 捕捉 |

#### 出错时要执行的代码块

| 扔 | 创建自定义错误消息，而不是标准的 JavaScript 错误 |
| 最后 | 无论执行中是否有错误，总是执行的块 |
| **误差值** | 每个错误都有一个定义它的名称和消息属性。 |
| **名称:**设置或获取错误名称 | **消息:**以可理解的字符串格式设置或获取错误 |

### 评估错误

eval()函数中出现错误

*   范围误差
*   数字超出范围

| 参考错误 | 出现非法引用 |
| SyntaxError  | syntax error |
| 类型错误 | 类型错误 |
| URIError | encodeURI() error |
| 下载 [Javascript 备忘单](https://hackr.io/blog/media/javascript-cheat-sheet.pdf) | **推荐课程:** |
| [创意编码:用 JavaScript 制作视觉效果](https://domestika.sjv.io/c/2890636/1558123/17608?u=https%3A%2F%2Fwww.domestika.org%2Fen%2Fcourses%2F2729-creative-coding-making-visuals-with-javascript&partnerpropertyid=2722169) | **结论** |

这个备忘单拥有 javascript 的所有功能。我们在必要的地方提供了例子和描述。大多数函数都是不言自明的，但是，如果您有任何疑问或问题，请随时发表评论并让我们知道。

快乐脚本！

**人也在读:**

## **Conclusion**

This cheat sheet has all the functions of javascript. We have provided examples and descriptions where necessary. Most functions are self-explanatory, however, feel free to comment and let us know if you have any doubts or questions.

Happy scripting!

**People are also reading:**