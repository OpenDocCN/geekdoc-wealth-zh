# 2023 年如何学习 JQuery【循序渐进的初学者指南】

> 原文：<https://hackr.io/blog/how-to-learn-jquery>

## **简介**

**JQuery** 是一个 JavaScript 库。它快速、丰富、易学，是一个“多写少做”的库。在 JQuery 的帮助下，您可以将多行用 JS 编写的代码包装成函数，只需一小段代码就可以调用这些函数。它简化了许多复杂的任务，比如 DOM 操作、事件处理、动画、HTML 文档遍历和 AJAX。定义完善且易于使用的 JQuery API 可以在许多 web 浏览器上运行，并使 JavaScript 编程变得非常容易。此外，JQuery 的插件可以执行几乎所有的任务，这些任务在用普通 JavaScript 执行时需要大量的代码。

## **为什么要学习 JQuery？**

目前，成千上万的开发人员都加入了 JQuery 的行列，为什么他们不能呢？JQuery 解决了跨浏览器问题、互操作性问题和标准化问题。它创建了一个抽象层，负责所有的工作区。让我们先睹为快，看看为什么 JQuery 在企业级如此受欢迎。

*   它促进了简单性:任何进入 JavaScript 世界的人都会发现学习 JQuery 非常直观而且非常容易。它有一个简单的语法和开放的编码标准，允许你创建伟大的网站。
*   **即使 JS 被禁用，它也会显示:**如果 Adobe Flash 没有安装在任何浏览器上，可能会出现许多渲染问题。因此，开发者不得不花费大量时间为那些缺乏 flash 插件的浏览器编码。但是有了 JQuery，他们再也不用这么做了。
*   **它可以创建动画应用:**就像 Flash 一样，JQuery 使用 o、HTML、CSS、JS 和 AJAX 的组合，让您可以实现非常好看的效果。因此，您不必单独雇用一名 Flash 开发人员。
*   页面加载速度更快:页面加载速度慢的话，会降低你的网站在搜索引擎中的表现和排名。实现更快加载时间的最佳方式是采用需要很少代码行的编码实践，并且仍然可以实现期望的结果。JQuery 为您提供了仅在需要时加载标签的选项，从而提高了速度。
*   它是 SEO 友好的:有大量的插件可以帮助你为搜索引擎优化 JQuery 代码片段。您可以使用简单的无序列表嵌入所有元素，这是提高 SEO 排名的良好健康的做法。

不用说，有很多理由让你在下一个 [web 开发项目](https://hackr.io/blog/best-web-development-projects)中采用 JQuery。第一，免费，好用；它通过向客户端推送内容来减少等待时间；它比 flash 小，播放起来更流畅。此外，它可以在任何地方工作，消除了兼容性问题，并且学习曲线较低。最重要的是，它是 SEO 友好的和 CSS 兼容的。

虽然由于 ReactJs 和 AngularJs 获得了巨大的人气，JQuery 的使用在过去确实已经显著下降，但是，它仍然被认为是遗留技术，受到许多人的青睐。

*资料来源:https://insights.stackoverflow.com/trends?tags = jquery % 2c angular % 2c angular js % 2c reactjs % 2c vue . js*

JQuery 确实不可能重回它的显赫地位。但是，它会因为它的遗产而继续存在。这背后的主要原因是 Bootstrap 仍然在几乎所有的代码片段中使用 JQuery。因此，如果您是 bootstrap 的粉丝，您也必须学习 JQuery。

而且从工作角度来说，除了 Vue、React、Angular 等现代框架之外。，在你的投资组合中有 JavaScript 和 JQuery 总是好的。当你申请 web 开发角色，甚至是前端开发者一个人的时候，他们期望你对 JS、JQuery、AJAX 有一个基本的了解。话虽如此，JQuery 还是有自己的用处。从企业级电子商务应用程序到简单流畅的登录页面，它仍然被用于许多项目中。如果你不擅长 CSS 的话，对快速原型甚至动画还是有好处的。它可能已经过时，但肯定不会消亡。

## **先决条件**

在开始使用 JQuery 之前，您需要对以下主题有更深入的了解。

*   你应该知道并使用过 [CSS](https://hackr.io/blog/css-cheat-sheet) 和 [HTML](https://hackr.io/blog/html-cheat-sheet) 的基础知识。你应该有创建一个简单网站的实践经验，并理解 CSS 中的选择器，如类、id 和伪元素。
*   你也应该有一个基本的理解，并且已经学习了编程的基础知识。不具备高级的 JavaScript 知识[也可以开始使用 JQuery。不过，强烈建议您熟悉对象、变量、数据类型等基础知识。](https://hackr.io/blog/how-to-learn-javascript-quickly)
*   您还应该了解 DOM 操作，因为 JQuery 主要用于操作 HTML DOM 元素。

## **如何安装 JQuery？**

主要有两种方法可以将 JQuery 嵌入到网页中。请注意，JQuery 只是一个 JavaScript 文件，您需要将它与 HTML 文件链接起来。您可以:

*   要么从官方网页下载 JQuery 库。
*   或者，您可以通过 CDN 链接到该文件。一个**内容交付网络**或 **CDN** 是一组多个服务器，它们组合起来根据用户的地理位置向用户交付网络内容。通过 CDN 链接到 JQuery 文件比在自己的服务器上托管它速度更快，加载效率更高。

#### **下载 JQuery 的副本**

有两个版本的 JQuery 文件可供下载。

*   **生产版**，压缩缩小后用于直播网站。
*   **开发版本**，主要用于测试和开发，因为它是可读和未压缩的。

请访问 [JQuery](https://jquery.com/download/) 网站下载。

下载之后，您可以在 HTML 文件的 head 部分中使用

```
<head>
<script src="jquery-3.5.1.min.js">
</script>
</head>
```

#### **使用谷歌 CDN**

您可以将 Google CDN 用于 JQuery 库，只需将源代码嵌入脚本标记中。

请注意，您应该始终在结束 body 标记之前链接到 JQuery CDN，然后是您在项目中使用的定制 JavaScript 文件。

`<!doctype html>
<html lang="en">
<head>
  <title>Welcome to Hackr.io</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js"></script>
<script src="js/scripts.js"></script>
</body>
</html>`

 **IDE(集成开发环境)**

为了充分利用 JQuery，您必须使用真正理解 JQuery 真正功能的 ide。有大量的 ide 为 JQuery 提供了巨大的支持和插件。但是要选择正确的，能够帮助你遵循编码的最佳实践，在错误时给出提示，具有自动完成特性等等。使用 ide 比使用文本编辑器更容易，因为 ide 可以帮助你自动生成标准代码。他们帮助你编译。它们包含有用的插件，并且允许你无缝地导入库。让我们来看看一些流行的 ide，它们可以用来处理 JQuery 文件。

#### [**Visual Studio 代码:**](https://code.visualstudio.com/) Visual Studio 无疑是最流行的 IDE，不仅适用于 JavaScript 和 JQuery，也适用于所有流行的编程语言。它支持语法高亮显示，具有由智能感知支持的自动完成特性(提供智能完成)，函数定义，大量插件等。您可以轻松地使用扩展来添加新语言、安装调试器、主题等。所有重要的特性都已经嵌入，并为管理文件提供了巨大的支持。

#### [**崇高的文本:**](https://www.sublimetext.com/) 它是一个成熟的下一代文本编辑器，具有流畅的用户界面、非凡的功能和一流的性能。它利用了一个定制的工具包，旨在实现速度和优雅。一些用户喜欢的功能包括- GoTo anything 以几个按键打开文件，GoTo definition 以生成项目级索引，多重选择，命令调色板，强大的 API 和软件包生态系统，易于定制，分割编辑，即时项目切换，可用于所有平台。

#### [**Atom:**](https://atom.io/)**Atom 文本编辑器由 GitHub 开发，高度可定制，让你轻松安装包。要针对 JavaScript 编码优化 Atom，请安装 JavaScript 包。由于是开源的，它的核心是可以被黑客攻击的。它具有一些流行的特性，如独立于平台的编辑、管理包的实用程序、智能代码自动完成、浏览文件系统的浏览器、多个窗格、数千个包、优雅漂亮的主题，并且是高度可定制的。**

 **## **在线编译器**

如果你不想在你的系统中经历下载和安装 ide 的麻烦，你总是可以使用在浏览器上运行的在线编译器。它们和其他桌面 ide 一样有用，但是相对来说不太容易定制。Tutorialspoint 是一款免费、快速、安全的在线编译器，用于开发 JavaScript 和 JQuery 脚本。

## **如何学习 JQuery？**

JQuery 简单易学，几个小时就能学会。然而，在开始使用 JQuery 之前，我们总是建议您具备 HTML、CSS 和 JavaScript 的基础知识。JQuery 只是一个 JS 库。简单来说，它有 4 个基本用途。其中包括:

*   它使得 JavaScript 代码非常短。它只用 2 行代码就能完成 JavaScript 用 6-7 行代码就能完成的事情。
*   它可以在几行代码内执行复杂的任务，如 DOM 操作。
*   与普通的 JavaScript 相比，使用 JQuery 进行事件处理是小菜一碟。
*   它使得 AJAX 调用非常简单。

从初学者的角度来看，最好是尝试一下，比如测试 JQuery 提供的各种功能及其性能，而不是学习理论。让我们来看看可以立即开始使用 JQuery 的 4 个步骤。

#### **第一步。添加 JQuery 库**

之前，我们已经讨论了如何在 HTML 文件中使用 JQuery 库。有两种方法可以做到这一点——要么直接从网站下载 JQuery JavaScript 文件，并使用 Script 标记包含它，要么可以使用像 Google 这样的 CDN 来引用这个库。

使用 CDN 是一个更好的选择，因为它比下载文件并将其托管在我们自己的服务器上加载更快。此外，它还减少了项目中的文件数量。

#### **第二步。用 JQuery 处理事件。**

你可以很容易地编程事件，如按钮点击，鼠标进入，焦点，按键等。，在 JQuery 的帮助下。例如，在下面的代码中，当单击一个按钮时，它会显示一条警告消息。

|  |**