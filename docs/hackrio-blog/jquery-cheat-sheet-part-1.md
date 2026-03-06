# 下载 JQuery 备忘单[第 1 部分]作为快速参考

> 原文：<https://hackr.io/blog/jquery-cheat-sheet-part-1>

jQuery 被认为是最流行的 JavaScript 库之一。事实上，它的使用量比其他任何 JavaScript 库都多 3 到 4 倍。截至 2019 年 5 月，jQuery 已经成为 1000 万最受欢迎网站中超过 73%的首选 **JS 库**。

在 MIT 许可下发布的开源 [**JavaScript 库**](https://hackr.io/blog/top-javascript-libraries) 旨在通过提供简单有效的方法来简化 JS:

*   HTML DOM 树遍历
*   事件处理
*   DOM 操作
*   CSS 动画
*   创建交互式、快速动态网页应用的网页开发技术

## Jquery 备忘单 PDF

jQuery 易于理解和入门。然而，与其他 JS 库一样，它需要一些时间来加快速度。为了帮助您，这里有 jQuery 备忘单 PDF 第一部分供您参考:

## **使用 jQuery**

jQuery 可以像任何其他 JavaScript 库一样使用，也就是说，在编写需要 jQuery 的代码之前，使用 HTML script 标记添加它。例如:

```
<script src="jsquery.js">
<script> // Enter code leveraging jQuery here. </script>
```

## **核心**

### **jQuery 对象**

*   **jQuery()** -返回匹配元素的集合，这些匹配元素或者是通过传递 HTML 字符串创建的，或者是基于传递的参数在 DOM 中找到的。它有以下变化:
*   **jQuery(选择器[，上下文])/jQuery(元素)/jQuery(元素数组)/jQuery(对象)/jQuery(选择)/jQuery()**
*   **jQuery(html [，ownerDocument])/jQuery(html，attributes)**
*   **jQuery(回调)**
*   **jQuery . no conflict([remove all])**-将 jQuery 对$变量的控制返回给其他 JS 库。例如:

```
<script src="someJSlibrary.js"></script>
<script src="jquery.js"></script> <script> jQuery.noConflict();
// Enter code leveraging $ of someJSlibrary. </script>
```

*   **jQuery.holdReady(hold)** -允许调用者延迟 jQuery 的就绪事件。通常由动态脚本加载器在 ready 事件发生之前用来加载额外的 JS，比如 jQuery 插件。
*   **jQuery.when(deferred)** -提供了一种基于零个、一个或多个有效对象执行回调函数的方法。当没有传递参数时，返回一个解析的承诺。

### **延期对象**

*   **jQuery。延期([beforeStart])** -返回/创建一个处于挂起状态的可链接实用程序对象([延期对象](https://en.wikipedia.org/wiki/Futures_and_promises))。这是一个工厂功能。
*   **Deferred . always(always callbacks[，alwaysCallbacks])** -当延迟对象被解析或拒绝时调用处理程序。延迟对象的其他方法可以链接到此方法。回调的执行顺序与它们被添加的顺序相同。
*   **deferred.done(done callback [，doneCallbacks])** -解析延迟对象时调用处理程序。接受一个或多个参数。这些函数可以是单个函数，也可以是函数的数组。
*   **Deferred . fail(fail callbacks[，failCallbacks])** -当延迟对象被拒绝时调用处理程序。接受一个或多个参数，可以是单个函数或函数数组。按照添加回调的顺序执行回调。
*   **deferred.notify(args)** -调用由 deferred.then 或 deferred.progress 在具有给定参数的延迟对象上添加的 progress 回调。参数被传递给每个 progressCallback。
*   **Deferred . notify with(context[，args])** -使用给定的参数和上下文调用延迟对象上的 progressCallbacks。
*   **【jQuery 1.8 中已弃用】****Deferred . pipe([done filter][，failFilter])** -过滤和/或链接延迟对象的实用方法。返回一个新的承诺，该承诺通过函数过滤延迟对象的状态和值。
*   **Deferred . progress(progress callbacks[，progressCallbacks])** -当延迟对象生成进度通知时调用处理程序。延迟对象的其他方法可以链接到此方法。
*   **deferred . promise([target])**-允许异步函数防止其他代码干扰其内部请求的进度或状态。当提供一个目标时，它将方法附加到其上，然后返回这个对象，而不是创建一个新的对象。
*   **Deferred . reject([args])**-拒绝一个延迟的对象，并用给定的参数调用任何 failCallbacks。
*   **deferred.rejectWith([，args])** -拒绝一个延迟的对象，并使用给定的上下文和参数调用任何 failCallbacks。
*   **Deferred . resolve([args])**-解析一个延迟的对象，并用给定的参数调用任何 doneCallbacks。
*   **Deferred . resolve with(context[，args])** -解析一个延迟的对象，并使用给定的参数和上下文调用任何 doneCallbacks。
*   **deferred.state()** -返回一个表示延迟对象当前状态的字符串。换句话说，它决定了延迟对象的当前状态。延迟对象可以处于以下三种状态之一:
*   **待定-** 未处于完成状态。
*   **Resolved -** 已调用 deferred.resolve()或 deferred.resolveWith()，并且已调用或即将调用 doneCallbacks。
*   **Rejected -** 已调用 deferred.reject()或 deferred.rejectWith()，并且已调用或即将调用 failCallbacks。
*   **deferred.then(doneFilter[，failFilter][，progressFilter])** -当延迟对象被解析、拒绝或挂起时调用处理程序。返回一个新的 promise，它可以通过一个函数过滤延迟对象的状态和值。允许将 Promise 对象的其他方法链接到它。
*   **。promise([type][，target])** -返回一个动态生成的 promise 对象，当绑定到集合的某个类型的所有操作(无论是否排队)结束时，该对象被解析。

### **实用程序**

*   **jQuery.contains(container，contained)** -检查一个 DOM 元素是否是其他 DOM 元素的后代。仅支持元素节点。第一个参数不能是 jQuery 对象或普通 JS 对象，它必须是 DOM 元素。例如:

```
$.contains(document.documentElement, document.Body); // Returns true
$.contains(document.Body, document.documentElement); // Returns false
```

*   **jQuery .每个(数组/对象，回调)** -无缝迭代数组和对象。尽管具有 length 属性的数组和类似数组的对象由数字索引迭代(从 0 开始，以 length - 1 结束)，但其他对象通过其命名属性迭代。返回第一个参数，即迭代的对象。
*   jQuery.extend(目标，[，对象 1]，[，对象 2]，。…，[，objectN]) -将两个或多个对象的内容合并到目标中，即第一个对象。忽略 null 或未定义的参数。如果只提供了一个参数，即省略了目标参数，则 jQuery 对象被假定为目标对象。这有助于向 jQuery 名称空间添加新函数。
*   **jQuery.globalEval(code[，options])** -在全局上下文中执行提到的 JS 代码。通常用于动态加载外部脚本。
*   **jQuery.grep(array，function，[，invert])** -查找满足过滤函数的数组成员。原始数组不受影响。两个参数被传递给过滤函数，当前数组项及其索引。
*   **jQuery.inArray(value，Array，[，fromIndex])** -搜索并返回数组中指定值的索引。如果未找到，则返回-1。
*   **jQuery.isArray(object)** -检查/测试对象是否为数组。
*   **jquery . isemptyobject(object)**-检查/测试对象是否为空，即不包含可枚举的属性。例如:

```
jQuery.isEmptyObject({}); // Returns true
jQuery.isEmptyObject({ not: "empty" }); // Returns false
```

*   **【在 jQuery 3.3 中已弃用】****jQuery . is function(value)**-如果传递的参数是可调用函数，则返回 true。否则为假。
*   **jquery . isnumeric(value)**-如果传递的参数是数字或字符串类型，则返回 true。否则为假。
*   **jquery . isplainobject(object)**-检查所提供的对象是否是普通对象。
*   **【在 jQuery 3.3 中已弃用】****jQuery . is window(object)**-如果传递的参数是窗口，则返回 true。
*   **jQuery.isXMLDoc(node)** -检查 DOM 节点是 XML 文档还是在 XML 文档中。
*   **jquery . make array(object)**-将类似数组的对象转换为真正的 JS 数组。转换后，该对象拥有的任何特殊功能都将不再可用。
*   **jQuery。**[**map(array**](https://hackr.io/blog/javascript-map)**/object，callback)** -对数组或对象的每个元素应用一个函数，并将处理后的元素映射到一个新数组中。
*   **jQuery.merge(first，second)** -返回包含两个数组中所有元素的数组。元素的顺序保持不变，第二个数组中的项被追加到第一个数组中。举个例子，

```
jQuery.merge ([0, 1, 2 , 3], [4, 5, 6, 7]) // Returns [0, 1, 2, 3, 4, 5, 6, 7]
```

*   jQuery.noop() -当需要传递一个什么都不做的函数时使用的空函数。对于 jQuery 插件作者提供可选回调非常有用。该函数在没有回调时执行。
*   **jQuery.now()** -返回表示当前时间的数字。类似于(新日期)。getTime()表达式。
*   **jQuery.parseHTML(data[，context][，keepScripts])** -使用本地方法将给定的字符串转换(解析)为 DOM 节点数组。
*   **【在 jQuery 3.0 中已弃用】** **jQuery.parseJSON()** -从格式良好的 JSON 字符串中返回等效的 JavaScript 值。如果传递了格式错误的 JSON 字符串，则会引发 JS 异常。
*   **jQuery.parseXML(data)** -使用浏览器的本地解析功能将字符串解析/转换为 XML 文档。然后，可以将创建的 XML 文档传递给 jQuery，以创建一个典型的 jQuery 对象，可以对其进行操作和遍历。
*   **jQuery.proxy(function，context)** -返回一个函数，该函数将始终具有特定的上下文..适用于将事件处理程序附加到上下文指向不同对象的元素。
*   **【在 jQuery 1.9 中已弃用】****jQuery . support**——代表不同浏览器特性或 bug 存在的一组属性。供 jQuery 内部使用。
*   **jQuery.trim(string)** -删除所提供字符串开头和结尾的空白(换行符、空格和制表符)。除了字符串的开头和结尾以外，中存在的空白字符将被保留。
*   **jQuery.type(object)** -确定被传递对象的内部 JavaScript [[Class]]。
*   **【在 jQuery 3.0 中已弃用】****jQuery . unique(array)**-搜索 DOM 元素数组，执行排序，并删除重复元素。不适用于数字或字符串数组。
*   **jQuery.unique sort(array)**-jQuery 3.0 中 jQuery . unique()方法的替代。

### **DOM 元素方法**

*   **。get(index)** -返回索引匹配的元素/DOM 节点。如果索引值超出界限，则返回 undefined。如果没有提供索引，该方法将返回所有元素的数组。
*   **。index(element/selector)** -获取一个 DOM 节点并返回一个索引。根据三种不同情况返回整数值:
*   **当没有参数被传递时** -返回一个整数，表示 jQuery 对象中第一个元素的位置。
*   **当在元素集合上调用该方法，并且传递了一个 DOM 元素或 jQuery 对象时** -返回一个整数，表示所传递的元素在原始集合中的位置。
*   **当一个选择器字符串被传递时** -返回一个整数值，指示 jQuery 对象中第一个元素的位置。选择器字符串匹配的元素。找不到元素时返回-1。
*   **。toArray()** -返回 jQuery 集合中所有元素的数组。

### **内部构件**

*   **。jquery** -包含 jquery 版本号的字符串。该属性被分配给 jQuery 原型，即$.fn。例如，

```
alert ("The jQuery version you’re using is:" + $.fn.jquery); // Returns the version number of jQuery you’re running.
```

*   **jQuery.error(message)** -接受一个字符串并抛出包含该字符串的异常。插件开发人员主要使用它们来覆盖方法，为错误消息提供更好/更丰富的显示。
*   **。length** -返回一个表示 jQuery 对象中元素数量的整数值。类似于。size()方法。
*   **。pushStack(元素)/。pushStack(elements，name，arguments)** -将一组 DOM 元素添加到 jQuery 堆栈中。

### **回调对象**

*   **jQuery。callbacks(flags)**——在内部用于向 jQuery $提供基本功能。ajax()和$。延期()组件。这是一种多用途的方法，提供了一种管理回调列表的强大方式。提供对多种方法的支持，如 callbacks.add()、callbacks.disable()和 callbacks.remove()。
    可选标志参数决定了返回的回调列表的行为。支持的标志有:
*   **memory** -跟踪先前的值，并调用任何在列表被激活后添加的回调函数，并立即使用最新存储的值。
*   **once** -确保回调列表只被触发一次。
*   **stopOnFalse** -遇到回调时中断调用，返回 False。
*   **unique** -确保回调只添加一次。
*   **callbacks . add(callbacks)**-向回调列表添加单个或多个回调。
*   **callbacks.disable()** -禁止回调列表进一步执行。
*   **callbacks.disabled()** -检查回调列表是否被禁用。
*   **callbacks.empty()** -从回调列表中删除所有回调。
*   **callbacks . fire(arguments)**-使用传递的参数调用/调用回调列表中的所有回调。
*   **callbacks.fired()** -检查回调列表中的回调是否至少被调用过一次。
*   **callbacks . fire with([context][，arguments])** -使用传递的参数和上下文触发回调列表中的所有回调。
*   **callbacks . has([callback])**-检查回调列表是否附加了任何回调。如果回调作为参数传递，则确定它是否在回调列表中。
*   **callbacks.lock()** -锁定当前状态的回调列表。如果回调对象是用内存标志作为它的参数创建的，那么在回调列表被锁定后，可以添加和触发额外的函数。
*   **callbacks.locked()** -确定回调列表的锁定状态。
*   **callbacks . remove(callbacks)**-从回调列表中删除一个或多个或所有回调。

### **效果**

通过设置以下内容，可以全局关闭所有 jQuery 效果:

```
jQuery.fx.off = true
```

### **基础知识**

*   **。hide()/。隐藏([持续时间][，完成])/。隐藏(选项)/。hide(duration[，easing][，complete])** -隐藏匹配的元素。
*   **。show()/。show([持续时间][，完成])/。显示(选项)/。show(duration[，easing][，complete])** -显示匹配元素。
*   **。toggle()/。切换([持续时间][完成])/。切换(选项)/。toggle(持续时间[，缓解][，完成])/。切换(显示)** -切换匹配元素的可见性。

### **自定义**

*   **。animate(属性[，持续时间][，缓动][，完成])/。animate(properties，options)** -在任何数字 CSS 属性上创建动画效果。
*   **。clearQueue(queueName)** -从传递的队列中删除所有等待执行的函数。在没有指定队列(即没有指定参数)的情况下调用 fx 时，从标准效果队列中删除剩余的函数。
*   **。delay(duration[，queueName])** -用定时器延迟指定队列中的未决函数。
*   **。出列(queueName)** -从指定队列中删除下一个函数，然后执行相同的函数。
*   **jQuery.dequeue(element[，queueName])** -与的相同。出列()。
    **注**:低级法。使用。首选出列()。
*   **。finish(queue)** -停止正在进行的(当前正在运行的)动画，删除所有排队的动画，并通过将其 CSS 属性设置为目标值来完成所有动画。如果传递了一个字符串，则只有由该字符串表示的动画才会从队列中停止。
    注:T3。finish()方法与。stop(true，true ),但前者也会导致将所有排队动画的 CSS 属性设置为其最终值。
*   **【在 jQuery 3.0 中已弃用】** **jQuery.fx.interval** -用于调整动画播放速率的属性，以毫秒为单位。
    默认为 13 毫秒**注意**:在支持 requestAnimationFrame 方法的浏览器中没有效果。
*   **jQuery.fx.off** -当设置为 true 时，该属性禁用所有动画，即所有动画方法将其元素设置为最终状态，而不是显示效果。将该属性设置为 false 可打开动画。
*   **jQuery.speed([duration][，settings])/jquery . speed([duration][，easing][，complete])/jquery . speed(settings)**-允许通过创建包含属性的对象来定义可在自定义动画中使用的属性，这些属性可在自定义动画的定义中立即使用。实现处理默认值和可选参数以定义动画效果的逻辑的替代方法。
*   **。queue([queueName])** -显示匹配元素上等待执行的函数队列。
*   **。队列([队列名]，新队列)/。queue([queueName]，callback)** -处理等待执行的函数队列，对每个匹配的元素执行一次。
*   **jQuery.queue(element[，queueName])** -与的相同。queue([queueName])方法。
    **注**:低级法。。建议使用队列([queueName])。
*   **jQuery.queue(element，queueName，newQueue)/jQuery.queue(element，queueName，callback)** -同。用于操作的 queue()方法。
    **注**:低级法。。建议使用 queue()。
*   **。stop([clearQueue][，jumpToEnd])/。stop([queue][，clearQueue][，jumpToEnd])** -停止正在进行的匹配元素的动画。

### **褪色**

*   **。fade in([持续时间][，完成])/。淡入(选项)/。fadeIn([duration][，easing][，complete])** -通过使匹配的元素变得完全不透明来显示它们。
*   **。fade out([持续时间][，完成])/。淡出(选项)/。fadeOut([duration][，easing][，complete])** -通过将匹配的元素渐变为透明来隐藏它们。
*   **。fadeTo(持续时间，不透明度[，完成])/。fadeTo(持续时间，不透明度[，缓动][，完成])** -调整匹配元素的不透明度。
*   **。fade toggle([持续时间][，缓动][，完成])/。fadeToggle(options)** -通过动画显示匹配元素的不透明度来显示或隐藏它们。

### **滑动**

*   **。向下滑动([持续时间][，完成])/。向下滑动(选项)/。slideDown([duration][，easing][，complete])** -以滑动动作显示匹配的元素。
*   **。slide toggle([持续时间][，完成])/。slideToggle(选项)/。slideToggle([duration][，easing][，complete])** -以滑动动作显示或隐藏匹配的元素。
*   **。上滑([持续时间][，完成])/。上滑(选项)/。slideUp([duration][，easing][，complete])** -以滑动动作隐藏匹配的元素。

### **事件**

#### **浏览器事件**

*   **。调整大小(处理程序)/。调整大小([eventData]，处理程序)/。resize()** -触发元素上的 resize JS 事件。也可用于将事件处理程序绑定到 resize 事件。
*   **。scroll(处理程序)/。scroll([eventData]，处理程序)/。scroll()** -触发元素上的 scroll JS 事件。也用于将事件处理程序绑定到滚动事件。

#### **文件装载**

*   **。ready(handler)** -指定 DOM 完全加载后要执行的函数。它提供了一种方法，只要网页的 DOM 变得可以安全操作，就可以运行 JS 代码。

#### **事件处理程序附件**

*   **【jQuery 3.0 中已弃用】** **。bind(事件类型[，事件数据]，处理程序)/。bind(eventType [，eventData] [，preventBubble])/。bind(events)** -为元素的一个或多个事件附加一个处理程序。
*   **【jQuery 3.0 中已弃用】** **。委托(选择器、事件类型、处理程序)/。delegat(选择器，事件类型，事件数据，处理程序)/。delegate(selector，events)**——根据一组特定的根元素，立即或稍后为所有匹配元素的单个或多个事件附加一个处理程序。
*   **。off()/。关(事件)/。off(事件[，选择器])/。off(事件[，选择器][处理程序])** -删除附带的指定事件处理程序。在()。当没有指定参数时，移除附加到元素的所有处理程序。
*   **。on(事件[，选择器[，数据]，处理程序)/。on(events [，selector][，data])** -将单个或多个事件的一个或多个事件处理程序附加到所选元素。
*   **。一个(事件[，数据]，处理程序)/。on(事件[，选择器[，数据]，处理程序)/。一个(事件[，选择器][，数据])** -几乎等同于。on()方法，只是元素和事件类型的处理程序在第一次调用后被解除绑定。
*   **。trigger(eventType [，extraParameters])/。trigger(event [，extraParameters])** -执行附加到事件的匹配元素的所有事件处理程序和行为。事件处理程序的执行顺序被保留，即，如果由用户自然触发，事件处理程序以与它们被执行的顺序相同的顺序被执行。
*   **。triggerHandler(eventType [，extraParameters])/。triggerHandler(event [，extraParameters])** -执行附加到事件匹配元素的所有事件处理程序。
*   **【jQuery 3.0 中已弃用】** **。unbind()/。解除绑定(事件)/。unbind(eventType，false)/。unbind(eventType，[，handler])** -从匹配的元素中删除事件处理程序。
*   **【jQuery 3.0 中已弃用】** **。undelegate()/。取消删除(命名空间)/。undelegate(selector，eventType)/。undelegate(选择器、事件类型、处理程序)/。undelegate(selector，events)** -删除使用。委托()。

#### **表单事件**

*   **。blur()/。模糊(处理程序)/。blur([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 blur JS 事件。
*   **。change()/。change(处理程序)/。change([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 change JS 事件。
*   **。focus()/。焦点(处理程序)/。focus([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 focus JS 事件。
*   **。focusin()/。focusin(处理程序)/。focusin([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 focusin JS 事件。
*   **。focusout()/。focusout(处理程序)/。focusout([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 focusout JS 事件。
*   **。select()/。select(处理程序)/。select([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 select JS 事件。
*   **。submit()/。提交(处理程序)/。submit([eventData]，handler)** -将事件绑定或触发到元素上的 submit JS 事件。

#### **键盘事件**

*   **。keydown()/。keydown(处理程序)/。keydown([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 keydown JS 事件。
*   **。按键()/。按键(处理程序)/。keypress([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 keypress JS 事件。
*   **。keyup()/。keyup(处理程序)/。keyup([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 keyup JS 事件。

#### **鼠标事件**

*   **。单击()/。单击(处理程序)/。click([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 click JS 事件。
*   **。contextmenu()/。contextmenu(处理程序)/。contextmenu([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 contextmenu JS 事件。
*   **。dblclick()/。dblclick(处理程序)/。dblclick([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 dblclick JS 事件。
*   **。hover(handlerIn，handlerOut)** -将两个事件处理程序绑定到匹配的元素，当鼠标指针进入和离开元素时执行。若要绑定一个事件处理程序，请使用。悬停(handlerInOut)。
*   **。mousedown()/。mousedown(处理程序)/。mousedown([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 mousedown JS 事件。
*   **。mouseenter()/。mouseenter(处理程序)/。mouseenter([eventData]，handler)** -当鼠标进入一个元素时绑定或触发一个事件处理程序。
*   **。mouseleave()/。mouseleave(处理程序)/。mouseleave([eventData]，handler)** -当鼠标离开一个元素时绑定或触发一个事件处理程序。
*   **。mousemove()/。mousemove(处理程序)/。mousemove([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 mousemove JS 事件。
*   **。mouseout()/。mouseout(处理程序)/。mouseout([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 mouseout JS 事件。
*   **。mouseover()/。mouseover(处理程序)/。mouseover([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 mouseover JS 事件。
*   **。mouseup()/。mouseup(处理程序)。/mouseup([eventData]，handler)** -将事件处理程序绑定或触发到元素上的 mouseup JS 事件。

#### **事件对象**

### **选择器**

#### **基础知识**

*   **jQuery(*************)**-选择所有元素。被称为全部或通用选择器。
    **注意**:极慢，除非自己用。****
*****   **jQuery(******)。class****"**-选择指定类的所有元素。被称为类选择器。*****   **jQuery(** **"** **元素****"】**-选择所有具有指定标签名称的元素。称为元素选择器。*   **jQuery(****"****" # id****")**-选择具有传递的 id 属性的元素。被称为 ID 选择器。*   **jQuery(******)select or 1，selector2，...，selectorN)** -选择所有指定选择器的组合结果。被称为多重选择器。********

 ****#### **层级**

#### **基本过滤器**

#### **内容过滤器**

*   **jQuery(** **"** **:包含(文本)****"**-选择包含指定文本的所有元素。
*   **jQuery(****"****:empty****"】**-选择所有没有子元素的元素，包括文本节点。
*   **jQuery(****"****:has(选择器)****"**-选择至少包含一个与指定选择器匹配的元素的所有元素。
*   **jQuery(****"****:parent****"】**-选择至少有一个子节点的所有元素，可以是元素，也可以是文本。

#### **可见度过滤器**

*   **jQuery(****“****:隐藏****”)**-选择所有隐藏的元素。
*   **jQuery(** **"** **:可见****"】**-选择所有可见的元素。

#### **属性**

*   **jQuery(****"****[attribute | =****'****value****'****]****"**-选择具有指定属性值的所有元素，该属性值等于指定的字符串或以相同的字符串开头，后跟一个-。
*   **jQuery(****"****[attribute * =****'****value****'****]****"**-选择具有指定属性且值包含指定子串的所有元素。
*   **jQuery(** **"** **【名称~=** **'** **值****'****]****"**-选择具有指定属性的元素，该属性的值包含指定的单词，用空格分隔。
*   **jQuery(****"****【name $ =****'****value****'****]****"**-选择具有指定属性的元素，其值以指定的字符串结尾。进行区分大小写的比较。
*   **jQuery("****【name =****'****value****'****]****"**-选择具有与指定值完全相等的指定属性的元素。
*   **jQuery(******【姓名！=** **'** **值****'****]****"**-选择不具有指定属性的元素以及具有指定属性而非指定值的元素。**
***   **jquery("****【name^=****'****value****'****]****"**-选择具有指定属性的元素，其值恰好以指定的字符串开始。*   **jQuery(** **"** **【名称】****"】**-选择具有指定属性的元素，而不考虑它们所具有的值。*   **jQuery(******【属性过滤器 1】【属性过滤器 2】...[attribute filtern]****"****)**-选择与所有指定属性过滤器匹配的元素。称为多属性选择器。****

 ****#### **子过滤器**

完整的 jQuery 课程:从初级到高级！

#### **表格**

*   **jQuery(****"****:button****"】**-选择所有按钮元素以及按钮类型的元素。
*   **jQuery(** **"** **:复选框****"】**-选择类型复选框的所有元素。
*   **jQuery(** **"** **:选中****"】**-选择所有被选中(或选中)的元素。
*   **jQuery(** **"** **:禁用****"】**-选择所有被禁用的元素。
*   **jQuery(****"****:enabled****"】**-选择所有被启用的元素。
*   **jQuery(****"****:focus****"】**-如果当前被聚焦，则选择一个元素。
*   **jQuery(****"****:file****"】**-选择类型文件的所有元素。
*   **jQuery(****"****:image****"】**-选择图片类型的所有元素。
*   **jQuery(****“****:input****”)**-选择所有的按钮、input、select 和 textarea 元素。
*   **jQuery(** **"** **:密码****"】**-选择密码类型的所有元素。
*   **jQuery(****"****:radio****"】**-选择 radio 类型的所有元素。
*   **jQuery(****"****:reset****"】**-选择 reset 类型的所有元素。
*   **jQuery(****"****:selected****"】**-选择所有被选中的元素。

这就完成了 jQuery 备忘单的第一部分。我们在这里解释了核心、效果、事件和选择器。在第二部分中，我们将关注 AJAX、属性/CSS、操作和 jQuery 中的遍历。您可以通过[这个链接](https://hackr.io/blog/jquery-cheat-sheet-part-2)继续阅读第 2 部分的 Jquery 清单。

**附言**——看看这些[排名前五的 JavaScript 认证](https://hackr.io/blog/best-javascript-certification)。

在这里下载 Jquery 备忘单。

**人也在读:**********