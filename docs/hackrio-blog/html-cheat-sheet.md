# HTML 备忘单[更新] -下载 PDF 快速参考

> 原文：<https://hackr.io/blog/html-cheat-sheet>

## HTML 代表超文本标记语言

用于:创建在[万维网](https://en.wikipedia.org/wiki/World_Wide_Web)(网站)上显示的[网页](https://en.wikipedia.org/wiki/Web_page)(文档)。页面可以是文本、图像、视频和其他元素的混合。它可以用记事本、文本板或任何文本编辑器创建。

另存为:。html 文件

## HTML 备忘单

在这里，我们与您分享完整的 HTML 备忘单:

### 基本结构

```
<!DOCTYPE html>
<html>
 <head>
 <title></title>
 </head>
 <body>
 body tags and main content
 </body>
</html>

```

HTML 中的主要元素是标签。标签以不同的形式构建和呈现数据。

### 标题

```
<h1>Heading 1</h1>
<h2>Heading 2 </h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6 </h6>

```

### 段落

```
<p>write a paragraph</p>
Attribute ‘style’ can be used with <p> to display the text inside <p> in a specific manner. For example,
<p style = "color:blue">I will appear blue</p>
<p style = "background-color:blue">Highlighting as blue</p>
<br> line break

```

### 跨度

Span 标记用于样式化内联元素。

```
<span style = “color:green”> Address </span> 
```

-以指定颜色(此处为绿色)打印单词“地址”。style 属性用于设置 HTML 元素的样式。

### 特性

*   **&nbsp；–**空格(不间断)
*   **&quot；-** 添加引号(")
*   **&lt；-** 小于符号(<)
*   **&gt；-** 大于符号(>)
*   **&amp；-**'&'或&符号
*   **&临摹；-** 版权符号
*   **&贸易；-** 商标符号

### 格式化

*   **粗体文本**
*   **斜体文字* < /i >*
*   *下划线文字* < /u >
*   我以黄色突出显示 -用黄色标记文本。如果需要其他颜色，使用 span。
*   <spanstyle = " background-color:# ff 00 ff ">我用粉色突出显示 < /span >
*   <强> 我强</强>——给特定的文字以强调；大多是大胆的
*   <字体></字体> - 为文本选择字体
*   HTML 5 中不使用字体，使用 CSS。的属性-
*   **<>-**字体家族，例如快递新
*   **<字号> -** 字号的文字
*   **<颜色> -** 十六进制值的文本颜色(如#FF000F)或文本颜色(如红色)
*   <小></小> - 较小的文字，小字尺寸
*   <划掉> 划掉</划掉> -划掉标签内的文字
*   -上标(正常文字上方的文字类似指数数字)
*   <sub></sub>-下标
*   < em > < /em > -强调
*   <></pre>-预格式化文本
*   <></TT>-打字机文字

### 身体

<正文> - 主要内容在于正文。在 <体内> 可以有很多段。**属性—**

*   **背景="" -** 背景图片来源；如果没有图像，可以留空
*   **bgcolor="" -** 以十六进制值表示的背景颜色
*   **text="" -** 页面文字颜色
*   **链接="" -** 链接颜色
*   **alink="" -** 活动(当前)链接颜色
*   **vlink="" -** 访问过的链接颜色
*   **bgproperties="" -** 背景属性。值“固定”意味着不滚动水印
*   **topmargin= "？-** 以像素为单位的上边距大小
*   **leftmargin="" -** 以像素为单位的侧边距大小

**< meta >** 标签是 **< head >** 的一部分，描述关于数据的信息。元数据最常见的用途是由搜索引擎搜索关键字。**<meta charset = " UTF-8 ">-**最常用字符集**属性—**

*   **名称= " "–**可以是关键字、作者、描述等名称
*   **content = " "–**上述名称对应的值

**举例-**<meta name = " keywords " content = "什么是 HTML，如何学习 HTML" >

### 科和处

*   **< div > < /div >** 新增章节；当需要多个子部分时，嵌套的 div 标签非常常见
*   **< hr > -** 水平线

**<人力资源>具有以下属性—**

*   * * *

*   **大小—**线条的粗细，以像素为单位
*   **宽度—**以像素或百分比表示(任意一个)
*   **颜色—**十六进制值的颜色
*   **对齐—**对齐；左侧、右侧或中间

### 桌子

```
<table>
 <tr>
 <td></td>
 <td></td>
 <td></td>
 </tr>
 <tr>
 <td></td>
 <td></td>
 <td></td>
 </tr>
</table>

```

*   **<表> -** 创建一个表，
*   **< tr > -** 创建一行，
*   **< td > -** 创建列，
*   **< th > -** 创建标题列

**<表>属性—**

*   **border="" -** 外边框的粗细，以像素为单位
*   **bordercolor="" -** 以十六进制值表示的边框颜色
*   **cellspacing="" -** 每个单元格之间的间距，以像素为单位
*   **cellpadding="" -** 单元格边框和内容之间的间距
*   **align="" -** 水平对齐；左、右、中间
*   **bgcolor="" -** 背景颜色十六进制值
*   **width="" -** 表格宽度，以像素或%为单位
*   **height="" -** 以像素或%为单位的表格高度

**< td >属性**

*   **colspan="" -** 单元格跨越的列数
*   **rowspan="" -** 单元格跨越的行数
*   **width="" -** 单元格的宽度，以像素或%为单位
*   **height="" -** 单元格的高度，以像素或%为单位
*   **bgcolor = " "–**单元格(列)背景颜色的十六进制值
*   **align="" -** 水平对齐；左、中、右
*   **valign="" -** 垂直对齐；顶部、中间、底部
*   **< colgroup > - i** 用于定义表格中特定列的属性。

**示例—**

```
<colgroup>
 <col span="1" style="background-color:green">
 <col style="background-color:blue">
</colgroup>

```

第一列将以绿色突出显示，而其他列将以蓝色突出显示。

### 表单(HTML 备忘单)

大多数动态内容，如用户输入、提交页面、填写表单，都发生在这个标签中。它是一组相关的输入。

```
<form>
 <input>
 <select><option></option></select>
 <textarea>
</form>

```

**<表单>标签属性—**

*   **action="url" -** 提交表单时的目标 url
*   **方法="" -** 表单方法- get，post
*   **编码类型="" -** 编码类型；对于文件上传，它是“多部分/形式数据”

**<输入>标签属性—**

*   **type="" -** 必填字段类型:文本、密码、复选框、提交等。
*   **name="" -** 表单字段名称(表单处理时必须填写)
*   **值="" -** 值(用户输入)或默认值
*   **size="" -** 字段大小
*   **maxlength="" -** 输入字段数据可接受的最大长度
*   **选中-** 在复选框(多选)或单选按钮(单选)中标记所选字段

<选择></选择> - 从下拉列表中选择选项 **<选择>标签属性:**

*   **名称="" -** 下拉组合框名称；对于表单处理是必需的
*   **size = "-s**下拉列表的大小
*   **多选-** 允许多选

<选项></选项> - 下拉列表的单项 **<选项>标签属性:**

*   **值="" -** 选项值被选中或缺省值被设置
*   <【textarea】>大量文字喜欢描述 < /textarea > - 大面积文字输入

**< textarea >标签属性:**

*   **name="" -** 用于表单处理的文本区域名称
*   **rows="" -** 显示的文本行数
*   **cols="" -** 列数(每行字符数)
*   **wrap="" -** 文本换行

### 内联框架

*   **<iframe src = " "></iframe>-**在框架中的当前文档(页面)内嵌入另一个文档。
*   **属性“src”–要嵌入的文档的位置**

### 链接

HTML 链接，也称为超链接，是由“a”标签—<a></a>**属性—**定义的

*   **href = " "–**点击链接时要访问的 url
*   **target = " "–**指定打开链接的位置- _blank(新选项卡/窗口)、_self(同一窗口/选项卡)、_parent(在父框架中)、framename–在特定框架中打开。
*   **title = " "–**给出关于元素的信息
*   **id = " "–**在页面中创建书签，可以用作 href 属性中的值。

**示例—**

*   [转到 hackr.io](https://hackr.io/)
*   [从给定位置打开资源](C:\Users\Public)
*   [到达一个由名称](#divprop)指定的 div 元素

[用 HTML5 和 CSS3 构建响应迅速的真实世界网站](https://click.linksynergy.com/link?id=jU79Zysihs4&offerid=1045023.1701404&type=2&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fbuild-3-real-world-websites-using-html5-css3-js-bootstrap4%2F)

### 风格

对于样式，有许多属性与各种标签一起使用。这些属性是

```
<style>
 text-align= “” – align text; left, right, center
 background-color = “” – background color of the element
 color=”” – for color of texts
 font-family = “” – for various fonts
 font-size = “” size of the font
 border = “” – border thickness and color for a table
</style>

```

这些样式元素放在一个 CSS 中。

### 列表

有两种类型的列表——有序列表和无序列表。 **< ol > < /ol > -** 有序列表**属性-**

*   **type = " "–**列表的编号–A，A，I，1，I
*   **start = " "–**起始值
*   **< ul > < /ul > -** 无序列表

**属性—**

*   **type = " "–项目符号的类型–**方形、圆形、圆盘形
*   **<李></李> -** 列表中的个人值

**属性**--

*   **<值>= " "–**列表项的值
*   **<类型>= " "–**列表项的类型

### 形象

**< img > -** 显示页面加载时的图像**属性-**

*   **src = " source of image "-**图像的来源；url 或文件位置；命令的
*   **alt = "替代文本"–**替代文本；命令的
*   **align = " left/right/center "-**相对于周围项目(文本)对齐
*   **宽度= " "–**以像素或百分比表示
*   **高度= "" -** 以像素或百分比表示
*   **border = " "–**以像素为单位的边框粗细
*   **hspace = " "–**图像两侧的像素间距
*   **vspace = " "–**图像顶部和底部的像素间距

*   **<搁置> -** 不属于任何元素的内容，但必须放在主要内容旁边
*   **<图> -** 任何插图，如照片、图表、代码清单等。
*   -元素的标题

*   **<页眉> -** 一节的标题(类似于 MS word 中的标题)，页眉可以有其他内容，如导航链接、表格等...
*   **<页脚> -** 页面/部分底部的内容，如版权信息、条款和条件等...
*   **< main > -** 标签是页面主要内容开始的指示器
*   **<细节> -** 具有扩展/折叠功能的框，允许更多的文本空间
*   **<摘要> -** 特定元素内容的摘要。可以是描述、标题等...
*   **<标记> -** 突出文字的一部分以突出
*   **<导航> -** 部分，带有导航链接，可链接到页面上的部分或其他页面
*   **<版块> -** 页面上的某个特定部分(群体)，例如，关于我们或一个网页上的奖状版块
*   **<时间> -** 以机器可读格式提到的时间。它可以有日期，时间，时区偏移，持续时间等...
*   **< datalist > -** 类似于自动完成；为输入控件定义的预设选项
*   **< keygen > -** 表单的密钥对(公钥和私钥)生成器。提交表单时，公钥被发送到服务器，而私钥存储在本地密钥库中
*   **<输出> -** 任何计算的结果
*   **<进度> -** 通过进度条显示任务进度
*   **<嵌入> -** 嵌入来自外部源的媒体
*   **<信号源> -** 音频或视频信号源
*   **<音频> -** 为音乐内容或声音
*   **<视频> -** 呈现电影或视频

从[这里](https://drive.google.com/file/d/1jRPJ59Jpyo4FTCH0GuKXYz7ebRTXN_XR/view?usp=sharing)下载 HTML 备忘单 PDF。

如果您希望使用您的 HTML 技巧来构建自己的网站，我们建议您使用 name 廉价工具

[buy your domain name](https://www.namecheap.com/?clickID=wUoTbQ3KtxyNR9L3K50RiSEKUkAx6n2NkXBZwI0&irgwc=1&utm_source=IR&utm_medium=Affiliate&utm_campaign=2890636&affnetwork=ir&ref=ir)

和

[web hosting services](https://www.namecheap.com/hosting/shared/?clickID=wUoTbQ3KtxyNR9L3K50RiSEKUkAx6E09kXBZwI0&irgwc=1&utm_source=IR&utm_medium=Affiliate&utm_campaign=2890636&affnetwork=ir&ref=ir)

。它们是业内最好的，而且超级实惠。

**人也在读:**