# 50 大 JQuery 面试问答[更新]

> 原文：<https://hackr.io/blog/jquery-interview-questions>

如果你接到了一个 [jQuery](https://hackr.io/tutorials/learn-jquery?ref=blog-post) 程序员职位的面试电话，我们有一些你在面试中可能会想到的问题。顺便说一下，我假设您熟悉 JavaScript，因为这是一个重要的先决条件。如果没有，不用担心！你可以浏览我们的[最佳 JavaScript 教程](https://hackr.io/tutorials/learn-javascript?ref=blog-post)，它将帮助你顺利通过。

你也可以通过我们的博客来增长知识，这些博客阐述了当今流行的技术。

## JQuery 面试问答

这里有一些关于 Javascript 的有用博客:

参考 [10 本最好的 Javascript 书籍](https://hackr.io/blog/javascript-books) ， [如何快速学习 Javascript](https://hackr.io/blog/how-to-learn-javascript)， [最好的 JavaScript IDE &源代码编辑使用](https://hackr.io/blog/best-javascript-ide-source-code-editors)， 等等……那么，我们开始吧。

### 基础 JQuery 面试问题

#### **问题:什么是 jQuery？**

**回答** : jQuery 是一个功能丰富的 JavaScript 库，它使得 HTML 文档遍历和操作、事件处理、动画和 Ajax 变得更加简单快捷。jQuery 有一个易于使用的 API，可以跨许多浏览器 。使用 jQuery 可以用最少的代码行编写 UI 相关的函数。

#### **问题:JavaScript 和 jQuery 有什么区别？**

**回答** : JavaScript 是一种解释型编程语言，而 jQuery 是一个为 JavaScript 构建的 API 库。jQuery 简化了 JavaScript 语言的使用。

#### **问题:jQuery 中使用的*效果*方法有哪些？**

**回答** : jQuery 让我们能够在网页上添加效果。jQuery 效果可以分为淡化、滑动、隐藏/显示和动画效果。jQuery 为网页效果提供了很多方法

这些是 jQuery 中使用的 *效果* 方法:

*   show() -显示或显示选中的元素。
*   hide() -隐藏匹配或选择的元素。
*   toggle() -显示或隐藏匹配的元素。换句话说，它在 hide()和 shows()方法之间切换。
*   fadeIn() -通过将匹配的元素渐隐为不透明来显示它们。换句话说，它淡入选定的元素。
*   fadeOut() -通过将匹配的元素渐变为透明来显示它们。换句话说，它淡出选定的元素。

#### **问题:jQuery 有什么特点？**

**回答:**jQuery 的一些重要特性有:

*   使用 Sizzle 引擎轻松操纵 DOM。
*   事件处理和 AJAX 支持。
*   内置的效果和动画。
*   轻量级库。
*   跨浏览器兼容性。
*   支持 CSS3，基本 XPath，HTML5。

#### **问题:解释 jQuery 的优势？**

**答案:**jQuery 的优势在于:

*   简单易用。
*   以博客、代码片段、教程和其他资源的形式提供了大量的文档
*   简单明了的语法。
*   开放的编码标准，直观。
*   处理跨浏览器问题，开发人员不必担心这些问题。
*   轻量级，核心库只有 24kb。
*   开源库。
*   详尽的动画和效果集。
*   可扩展且快速。
*   它可以为搜索引擎优化更好的搜索引擎优化。

#### **问题:什么是 jQuery Ajax？**

**回答** : AJAX 是代表异步 JavaScript 和 XML 的首字母缩略词，这种技术帮助我们在不刷新浏览器页面的情况下加载数据并与服务器交换数据。JQuery 是一个很好的工具，它提供了一组丰富的 AJAX 方法来开发下一代 web 应用程序。

#### **问题:ajax()方法是做什么的？**

**答案:** 该方法向服务器发送异步 HTTP 请求。

#### **问题:ajax 方法 load()是做什么的？**

**回答:**load()方法 发送 HTTP 请求，从服务器加载 HTML 或文本内容，并将它们添加到 DOM 元素中。

#### **问题:jQuery Ajax 事件有哪些？**

**回答:**jQuery 库还包含了基于 *Ajax 请求状态* 会被触发的事件；这些被称为 Ajax 事件 。

#### **问题:jQuery Ajax 事件方法 ajaxComplete()是做什么的？**

**回答** :每当一个 Ajax 请求完成，jQuery 就会触发[*Ajax complete*](https://hackr.io/blog/media/jquery-cheat-sheet-2.pdf)事件。已注册到。 *此时执行 ajaxComplete* ()方法。

#### **问题:jQuery ajax 事件方法 ajaxStart()是做什么的？**

**回答:** 每当一个 Ajax 请求将要发送时，jQuery 会检查是否还有其他未完成的 Ajax 请求。如果没有正在进行的，jQuery 触发*Ajax start*事件。已向注册的任何和所有处理程序。*Ajax start*()方法此时被执行 。

#### **问题:jQuery 中有哪些事件？**

**答案:** 响应用户在网页上的动作称为事件。 jQuery 提供了将事件处理程序附加到选择的简单方法。当事件发生时，所提供的功能被执行。

#### **问题:jquery 事件中有哪些类别？**

**回答** :常见的**DOM 事件如下**

*   表格
*   键盘
*   鼠标
*   浏览器
*   文件装载

#### **问题:css()方法在 JQuery 中有什么用？**

**答:**jQuery CSS()方法用于 *get(返回* )或 *为选中的元素设置* 样式属性或值。它便于您获取一个或多个样式属性。

#### **问题:*找*和*找孩子*的方法有什么区别？**

**答案:** 两种方法都是用来过滤匹配元素的子元素。find 方法用于查找 DOM 树中的所有级别，但是 children 方法只搜索 DOM 树中的一个级别。

#### **问题:jQuery 中的选择器有哪些，选择器的类型有哪些？**

**答:** 如果你想处理网页上的一个元素，首先你需要找到或选择它。选择器使用 jQuery 找到 HTML 元素。

jQuery 库中有许多类型的选择器。一些基本的选择器有:

*   **名称** :用于选择所有与给定元素名称匹配的元素。
*   **#ID** :用于选择与给定 ID 匹配的单个元素
*   。 **类** :用于选择与给定类匹配的所有元素。
*   **通用** (*):用于选择一个 DOM 中所有可用的元素。
*   **多元素 E、F、G** :用于选择所有指定选择器 E、F 或 G 的组合结果
*   **属性选择器** :根据属性值选择元素。

#### **问题:jQuery 中的 ID 选择器和类选择器有什么区别？**

**回答**:ID 选择器和类选择器和 CSS 中的一样。ID 选择器使用 ID，而类选择器使用类来选择元素。使用 ID 选择器只选择一个元素。如果要选择一组元素，可以使用同一个 CSS 类来使用类选择器。

#### **问题:jQuery Ajax 方法的优点是什么？**

**回答:** 使用 jQuery Ajax 方法的优点是

*   跨浏览器支持
*   简单的使用方法
*   发送 GET 和 POST 请求的能力
*   加载 JSON、XML、HTML 或脚本的能力

#### **问题:onload()和 document.ready()方法有什么区别？**

**答案:** 身体。Onload()事件只有在 DOM 和图片等相关资源被加载后才会被调用，但是 jQuery 的 document.the ready()事件会在 DOM 加载后被调用，它不会等待图片等资源被加载 。

#### **问题:什么是 jQuery connect？**

**回答**:‘jQuery connect’是一个插件，用于将一个函数与另一个函数连接或绑定。Connect 用于在执行另一个对象或插件的函数时执行函数。

#### **问题:自举需要 jQuery 吗？**

**回答:**[Bootstrap](https://hackr.io/tutorials/learn-bootstrap?ref=blog-post)对 JavaScript 插件(像模型、工具提示等)使用 jQuery。).但是，如果只是使用 Bootstrap 的 CSS 部分，就不需要 jQuery 。

#### **问题:什么是 jQuery Mobile？**

**回答:j** Query Mobile 是一个基于 HTML5 的用户界面系统，旨在使所有智能手机、平板电脑和桌面设备都可以访问响应网站和应用程序。

#### **问题:jquery.min.js 和 jquery.js 有什么区别？**

**答案:** jquery.min.js 是 jquery.js 的压缩版本(删除了空格和注释，使用了更短的变量名，等等)以保留带宽。从功能上来说，它们是完全一样的。建议在生产环境中使用这个压缩版本。当使用最小化版本的 jQuery 时，web 页面的效率会提高。

#### 问题:jQuery HTML 有没有可能同时适用于 HTML 和 XML 文档？

**回答:** 不可以，jQuery HTML 只对 HTML 文档有效。它不适用于 XML 文档。

#### **问题:什么是 jQuery UI？**

**答案:** [jQuery UI](http://jqueryui.com/) 是构建在 jQuery JavaScript 库之上的一组用户界面交互、效果、小部件和主题。jQuery UI 适用于具有许多控件的高度交互的 web 应用程序，也适用于具有日期选取器控件的简单页面。

#### **问题:jQuery 的数据表插件是什么？**

**回答** : DataTables 是 jQuery Javascript 库的一个插件。这是一个高度灵活的工具，建立在渐进增强的基础上，可以为任何 HTML 表格 添加高级功能。

### **高级 JQuery 面试问题**

#### **问题:Qunit 是什么？**

**回答** : QUnit 是一个功能强大，简单易用的 JavaScript 单元测试框架。它由 jQuery、jQuery UI 和 jQuery Mobile 项目使用，能够测试任何通用的 JavaScript 代码。

#### 问题:使用 CDN 托管 jQuery 有什么好处？

**回答** : CDN 代表内容交付网络或内容分发网络。它是一个大型分布式服务器系统，部署在互联网上的多个数据中心。它以更高的带宽提供来自服务器的文件，从而加快加载速度。

使用 CDN 的优势有:

*   jQuery 库下载时间将会减少。比如——欧洲的用户会打欧洲的 CDN，美国的用户会打美国的 CDN。因此，这将减少整体页面加载时间 。
*   如果用户访问了引用相同 jQuery 库的另一个网站，jQuery 库将已经缓存在用户的浏览器中。在这种情况下，用户不需要下载 jQuery 库。

#### **问题:解释。jQuery 中的 detach()和 remove()方法。**

**答案:**[detach()](https://api.jquery.com/detach/)和[remove()](https://api.jquery.com/remove/)方法相同，除此之外。detach()保留所有与被删除的元素和。remove()不会。因此，当删除的元素可能需要在以后重新插入 DOM 时，detach()非常有用。

#### 问题:jQuery 库可以用于服务器脚本吗？

**回答** : jQuery 是为客户端脚本功能而设计的。jQuery 与服务器端脚本不兼容。

#### **问题:** **什么是 jQuery.noConflict？**

**回答:**通常 JS 函数和变量都是用$作为名称的。在 jQuery 中，$只是 jQuery 的别名，所以我们不需要使用$。如果我们必须使用 JS 库和 jQuery，那么$的控制权就交给了 JS 库。为了提供这种控制，我们使用 jQuery.noConflict()。它还用于给变量指定一个新名称。

```
var newname = jQuery.noConflict();
```

#### **问题:**区分。jQuery 中的 empty() vs .remove() vs .detach()。

**答案:**

**remove():** 删除元素及其子元素。可以恢复 DOM 中的数据；但是，事件处理程序无法恢复。

**empty():** 不删除元素；但是，请删除其内容以及关联的子元素

**detach():** 删除元素和所有关联的子元素，但是保留被删除元素的数据和事件处理程序，以便以后重用。

*示例用法:*

```
$(“#div-element”).remove();
$(“#div-element”).empty();
$(“#div-element”).detach();
```

#### **问题:** **解释 jQuery 中可用的各种 Ajax 函数？**

**回答:**有很多方法比如:

*   。ajaxStart() -注册第一个 Ajax 请求开始时要调用的处理程序。
*   。ajaxStop() -注册所有请求完成时要调用的处理程序。
*   。ajaxSuccess() -注册 Ajax 请求成功完成时要调用的处理程序。

查看[官方 jQuery 文档页面](https://api.jquery.com/category/ajax/)上的所有方法，其中用一个例子解释了每个方法。

#### **问题:****jQuery 中 width()与 css('width ')有什么区别？**

**回答:** CSS('width ')返回以像素为单位的宽度值，而 width()返回整数(不含单位值)。例如:

```
div{
width: 20cm;
}
```

如果打印这些值:

```
$(this).width();
$(this).css(‘width’);
```

您将分别得到类似于 756 和 756px 的值。注意，尽管我们以厘米为单位指定宽度，但出于输出目的，它被转换为像素(px)。

#### **问题:****jQuery 中的 bind() vs live() vs delegate()方法有什么区别？**

**答案:**

**bind():** 该方法将事件处理程序直接注册到所需的 DOM 元素中。例如:

```
$(“#members a”).bind(“click”, function(f){….});
```

这意味着任何匹配的锚点都将附加这个事件处理程序！

**live():** 这个方法将事件处理程序附加到文档的根。这意味着一个处理程序可以用于传播到根的所有事件。因此，处理程序只被附加一次。

**delegate():** 在这个方法中，您可以选择将处理程序附加到哪里。这是委托的最有效和最可靠的方法。

例如:

```
$(“#members”).delegate(“ul li a”, “click”, function(f){….});
```

#### **问题:** **描述一下 jQuery 中 param()方法的用法？**

**答:**param()方法输出一个对象或数组的序列化表示。

例如:

```
student = new Object();
student.name = “Mary”;
student.marks = 67;
$("div").text($.param(student);
```

当调用此代码的事件发生时，该方法将给出以下输出:

```
name=Mary&marks=67
```

#### **问题:** **解释一下 jQuery 中$(this)和 this 的区别？**

**答:** $()是 jQuery 构造函数，而这是对 DOM 元素的引用。为了使用 jQuery 方法，我们使用$(this)。

#### **问题:** **解释一下 jquery.size()和 jquery.length 的区别？**

**回答:**两者都返回元素个数。但是长度更快。从 jQuery 1.8 开始，size()已被弃用。

#### 问:jQuery Ajax 方法使用的四个参数是什么？

**答案:**这四个参数是:

*   **URL:** 用于发送请求的 URL
*   **类型:**获取/发布请求
*   **成功:**请求成功时的回调函数
*   **数据类型:**返回数据类型——HTML、XML、文本等。

#### **问题:** **在一个页面中包含 jQuery 的所有方法有哪些？**

**答案:**

1.  你可以使用

2.  将代码写在 HTML 文档中的

```
<script src='http://ajax.aspnetcdn.com/ajax/jQuery/jquery-3.2.1.js'></script>
<script type = “text/javascript”>
$(document)……… <jQuery code>
</script>
```

3.  包括。js 文件，该文件将 jQuery 代码转换成 HTML 文档。

#### **问题:****JQuery 中的 css()方法有什么用？**

**答:css** ()为所有选中的元素设置样式属性。它还返回指定 CSS 属性的第一个匹配元素。

```
<p>Welcome to styling</p>
<p>I will be styled just as the previous paragraph</p>
<button>click me to change the style</button>
<script>
$(document).ready(function(){
$("button").click(function(){
$("p").css("color", "blue");
});
});
</script>
```

#### **问题:****jQuery 中的 jQuery Datepicker 是什么？**

**回答:**是一个在 HTML 页面中增加 datepicker 功能的插件/小部件。它是高度可配置的，可以定制日期格式、语言、限制日期选择等。关于日期选择器选项，请参考此 [jQuery 文档](https://api.jqueryui.com/datepicker/)。

#### **问题:** **定义 slideToggle()效果？**

**答:**用于对选中的元素在向上滑动和向下滑动之间切换。

```
<h2>This is a paragraph.</h2>
<button>show me toggle</button>
<script>
$(document).ready(function(){
$("button").click(function(){
$("h2").slideToggle();
});
});
</script>
```

#### **问题:** **如何在 jQuery 中使用数组？**

**答:**用$创建数组。makeArray( <对象>)

```
var myObj = [“John”, “Jake”, “Jack”, “King”];
var myArr = $.makeArray(myobj);
```

您可以使用$在数组中搜索特定元素。inArray()

```
$.inArray(“Jack”, myArr);
```

要合并两个数组，请使用$。merge()方法

```
var arr1 = [“John”, “Jake”, “Jack”, “King”];
var arr2 = [“Mary”, “Katy”, “Jill”, “Queen”];
var mergeArr = $.merge(arr1, arr2);
```

#### **问题:** **什么是 jQuery 插件？**

**回答:**插件就是让开发者能够扩展 jQuery 原型对象的简单方法。插件是用标准的 javascript 文件编写的。jQuery 提供了很多插件，你可以从他们的[资源库链接](https://jquery.com/plugins)下载。[您可以使用](https://learn.jquery.com/plugins/)<script src = " jquery . plugin . js " type = " text/JavaScript "></script>在代码中包含插件

#### **问题:****jQuery 中 Map 和 Grep 函数的区别？**

**答:** Map 函数将一组元素翻译成 jQuery 数组中的另一组值，可以有也可以没有这些元素。这张地图叫做:

```
$(“<element>”).map(<function to execute for elements in the object>)
```

另一方面，Grep 在数组中查找元素。

```
jQuery.grep(myArr, function(){}
```

#### **问题:****jQuery 中的方法链接是什么，有什么优点？**

**答:**通过链接，可以一次执行特定元素上的多个 jQuery 命令。它有助于一次在一个元素上实现各种动作，而不是一个接一个地执行它们。

```
$("#h2").css("color","blue").animate((left: '100px'}).slideDown(1000);
```

#### **问题:****jquery . get()和 jQuery.ajax()的区别？**

**回答:**在 get()方法中，我们必须传递单个参数，而 ajax()方法将所有这些参数作为一个对象来获取。

```
jQuery.ajax({
url: 'mydoc.txt',
dataType: 'text',
type: “GET”,
success: function(data) {
console.log(data);
}
});
```

get()方法接受参数。通过的三个主要参数解释如下:

```
jQuery.get('mydoc.txt',function(data){
console.log(data)
},'text');
```

在这里，第一个参数是 url，第二个是回调函数，第三个(' text ')是返回类型。

#### **问题:** **道具和属性的区别？**

**答:**attr()和 prop()都可以用来设置或获取一个元素的值，但是 attr()返回原始(缺省)值，而 prop()返回最近(当前)的值。例如，如果一个文本输入的初始值为“男性”，后来用户将其更改为“女性”，attr()将返回值为“男性”，而 prop()将返回值为“女性”

#### **问题:****JQuery 中的 toggle()方法有什么用？**

**回答:**如果有点击事件，toggle()会给 toggle 附加函数。因此，第一次点击时发生第一个动作，第二次点击时发生第二个动作，以此类推。

```
<button>Change my color on each click</button>
<script>
$(document).ready(function(){
$("button").toggle(
function(){$("button").css({"color": "blue"});},
function(){$("button").css({"color": "yellow"});},
function(){$("button").css({"color": "red"});
});
});
</script>
```

#### **问题:** **什么是 CDN？**

**回答:** CDN 是云交付网络的简称。它是网络上的服务器系统(分布式的),提供特定的 web 内容，如图形、图像、文本等。基于用户的地理位置、页面的来源和内容交付服务器。CDN 提供高可用性和高性能。

#### **问题:** **如何使用 jQuery 向一个元素添加和移除 CSS 类？**

**回答:**可以用 addClass()和 removeClass()方法来做同样的事情。

```
$("h1").addClass("myclass");
$("h1").removeClass("myclass");
```

#### **问题:** **你能写一个 jQuery 代码来选择段落内的所有链接吗？**

**答案:**

```
$('a:visible').css('text-transform', 'uppercase');
```

#### **问题:****JQuery 中 fade toggle()方法的用途是什么？**

**答:**用于 fadeIn()和 fadeOut()功能之间的切换。这里有一个例子来说明这一点:

```
<div id="div1" style="color:orange;”>My text</div>
<button>fade in/out</button><br><br>
<script>
$("button").click(function(){
$("#div1").fadeToggle();
}
</script>
```

## 结论

这是一个很好的面试问题列表，可以帮助你准备 Jquery 面试。我们强烈建议你试试这个 udemy 课程，它将帮助你为即将到来的面试做好准备: [Jquery 速成班](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https://www.udemy.com/course/learn-jquery-crash-course/)。

如果你正在寻找更多的 jQuery 面试问题，那么你可以看看这本书:[破解 IT 架构师面试](https://www.packtpub.com/application-development/cracking-it-architect-interview)。

**人也在读:**