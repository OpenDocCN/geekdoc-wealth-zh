# 下载 JQuery 备忘单[第 2 部分]作为快速参考

> 原文：<https://hackr.io/blog/jquery-cheat-sheet-part-2>

欢迎来到 Hackr 的第二部分 **jQuery 备忘单**。这涵盖了 jQuery 的**、AJAX** 、属性/CSS、操作和**遍历部分。准备好了吗？我们开始吧:**

## JQuery 备忘单 PDF

***P.S.*** -知道[如何快速学习 JavaScript】。](https://hackr.io/blog/how-to-learn-javascript)

### AJAX

#### **全局 Ajax 事件处理程序**

*   **。ajaxComplete(handler)** -注册一个事件处理程序，当 AJAX 请求完成时将调用该处理程序。
*   **。AJAX error(handler)**——注册一个事件处理程序，当 AJAX 请求完成但出现错误时，将调用这个事件处理程序。
*   **。ajaxSend(handler)** -添加一个在发送 AJAX 请求之前执行的函数。
*   **。AJAX start(handler)**——注册一个事件处理程序，当第一个 AJAX 请求开始时将调用这个事件处理程序。
*   **。ajaxStop(handler)** -注册一个事件处理程序，当所有的 AJAX 请求完成时，这个事件处理程序将被调用。
*   **。AJAX success(handler)**——注册一个事件处理程序，当 AJAX 请求成功完成时将调用该事件处理程序。

#### **助手功能**

*   **jQuery . param(obj)/jQuery . param(obj，traditional)** -创建适合在 URL 查询字符串或 AJAX 请求中使用的数组或 jQuery 对象的序列化表示。当传递一个 jQuery 对象时，它必须包含具有名称/值属性的输入元素。
*   **。serialize()** -将一组表单元素编码为字符串以供提交。
*   **。serializeArray()** -将一组表单元素编码为名称和值的数组。

#### **低级接口**

*   **jQuery.ajax(url [，settings])/jquery . ajax([settings])**-执行一个 AJAX，异步 HTTP，请求。
*   **jquery . ajaxprefilter([data types]，handler)** -在发送每个请求之前处理自定义 AJAX 选项或修改现有选项，并由*进行处理。ajax()* 。
*   **jquery . AJAX setup(options)**-为未来的 AJAX 请求设置默认值。
*   **jquery . ajaxtransport(dataType，handler)** -创建一个处理 AJAX 数据传输的对象。

#### **速记方法**

*   **jQuery.get(url [，data][，success][，dataType])/jquery . GET([settings])**-使用 HTTP GET 请求从服务器加载数据。
*   **jQuery.getJSON(url [，data][，success])** -使用 HTTP GET 请求从服务器加载 JSON 编码的数据。
*   **jQuery.getScript(url [，success])** -使用 HTTP GET 请求从服务器加载并执行 JS 文件。
*   **jQuery.post(url [，data][，success][，dataType])/jquery . POST([settings])**-使用 HTTP POST 请求从服务器加载数据。
*   **。load(url [，data][，complete])** -从服务器加载数据，并将返回的 HTML 放入匹配的元素中。

### **属性/CSS**

#### **属性**

*   **。attr()** -获取匹配元素集合中第一个元素的属性值，或者为每个匹配元素设置一个或多个属性。它的变体有:
*   **属性名**
*   **attr(属性名，值)/attr(属性)/attr(属性名，函数)**
*   **。prop()** -获取匹配元素集合中第一个元素的属性值，或者为每个匹配元素设置一个或多个属性。它的变体有:
*   **.prop(propertyName)**
*   **。prop(propertyName，value)/。prop(properties)/。prop(属性名，函数)**
*   **。removeAttr(attributeName)** -从匹配元素集中的每个元素中删除一个属性。
*   **。removeProp(propertyName)** -从匹配元素集中删除一个属性。
*   **。val()/。val(函数)/。val(value)** -获取匹配元素集合中第一个元素的当前值，或者设置每个匹配元素的值。

**CSS**

*   **。addClass(className)/。addClass(function)** -将指定的类添加到匹配元素集合中的每个元素。
*   **。css()** -获取匹配元素集合中第一个元素的计算样式属性的值，或者为每个匹配元素设置一个或多个 css 属性。它的变体有:
*   【t0 . CSS(属性名称)/.css(属性名称)
*   **。css(propertyName，value)/。css(属性名，函数)/。css(属性)**
*   jQuery.cssHooks -提供了一种定义函数来获取和设置特定 CSS 值的方法。它还可以用于创建新的 cssHooks 来规范化 CSS3 特性。
*   jQuery.cssNumber -它是一个包含所有 CSS 属性的对象，不需要单元就可以使用。
*   ***注*** :此物为*所用。css()* 方法检查是否需要将 *px* 加到无单位值上。
*   jquery . escape selector(selector)-对 CSS 选择器中具有特殊含义的字符进行转义。
*   **。hasClass(className)** -检查是否有任何匹配的元素被分配给指定的类。
*   **。removeClass([className])/。removeClass(function)** -从匹配元素集合中的每个元素中删除一个、多个或所有类。
*   **。toggleClass()** -根据 state 参数的值或类的存在，从匹配元素集合中的每个元素添加或删除一个或多个类。它的变体有:
*   **。toggleClass(className)/。toggleClass(className，state)/。toggleClass(函数[，状态])**
*   **toggle class([状态])**

#### **尺寸**

*   **。height()/。高度(功能)/。height(value)** -返回匹配元素集中第一个元素的当前计算高度，或者设置每个匹配元素的高度。
*   **。innerHeight()/。innerHeight(函数)/。innerHeight(value)** -返回匹配元素集中第一个元素的当前计算的内部高度，或者设置每个匹配元素的内部高度。
*   **。innerWidth()/。innerWidth(函数)/。innerWidth(value)** -返回匹配元素集中第一个元素的当前计算的内部宽度，或者设置每个匹配元素的内部宽度。
*   **。outerHeight([includeMargin])/。outerHeight(函数)/。outerHeight(value [，includeMargin])** -返回匹配元素集中第一个元素的当前计算外部高度，或者设置每个匹配元素的外部高度。
*   **。outerWidth([includeMargin])/。外部宽度(功能)/。outerWidth(value [，includeMargin])** -获取匹配元素集中第一个元素的当前计算外部宽度，或者设置每个匹配元素的外部宽度。
*   **。width()/。宽度(功能)/。width(value)** -返回匹配元素集中第一个元素的当前计算宽度，或者设置每个匹配元素的宽度。

#### **偏移**

*   **。offset()/。偏移量(坐标)/。offset(function)** -返回匹配元素集合中第一个元素的当前坐标，或者设置每个元素的坐标。
*   **。offsetParent()** -获取位置最近的祖先元素。
*   ***注意*** :如果一个元素有绝对、固定或相对的 CSS position 属性，则称之为 positioned。
*   **。position()** -获取一组匹配元素中第一个元素的当前坐标。
*   **。scrollLeft()/。scrollLeft(value)** -获取匹配元素集合中第一个元素的滚动条的当前水平位置，或者为每个匹配元素设置滚动条的水平位置。
*   **。scrollTop()/。scrollTop(value)** -获取匹配元素集合中第一个元素的滚动条的当前垂直位置，或者为每个匹配元素设置滚动条的垂直位置。

#### **数据**

*   **jquery . data(element)/jquery . data(element，key)/jQuery.data(element，key，value)** -存储与传递的元素相关的任意数据和/或返回设置的值。
*   **。data()/。日期(关键字)/。data(obj)/。data(key，value)** -存储与匹配元素相关联的任意数据，或者在指定的数据存储中为匹配元素集合中的第一个元素返回值。
*   **jQuery . hasdata(element)**-检查指定元素的任何相关联的 jQuery 数据。
*   **jQuery.removeData(element [，name])** -从传递的元素中删除指定的数据。
*   ***注*** :低级法。使用*。建议使用 removeData()* 方法。
*   **。remove data([名称])/。removeData([list])** -从传递的元素中移除指定的数据。

### **操纵**

#### **复印**

*   **。克隆([withDataAndEvents])/。clone([withDataAndEvents][，deepWithDataAndEvents])** -创建匹配元素集的深层副本。

#### [**DOM**](https://en.wikipedia.org/wiki/Document_Object_Model) **插入，左右**

*   **。wrap(函数)/。wrap(wrappingElement)** -在匹配元素集合中的每个元素周围包装一个 HTML 结构。
*   **。wrapAll(函数)/。wrapAll(wrappingElement)** -在匹配元素集合中的所有元素周围包装一个 HTML 结构。
*   **。wrapInner(函数)/。wrap inner(wrapping element)**-将一个 HTML 结构包装在匹配元素集合中每个元素的内容周围。

#### **DOM 检查，内部**

*   **。append(函数)/。append(content [，content])** -将由传递的参数指定的内容插入到匹配元素集合中每个元素的末尾。
*   **。appendTo(target)** -将匹配元素集中的每个元素插入到指定目标的末尾。
*   **。html()/。html(函数)/。html(htmlString)** -获取匹配元素集合中第一个元素的 html 内容，或者设置每个匹配元素的 HTML 内容。
*   **。prepend(content [，content])/。prepend(function)** -将由传递的参数指定的内容插入到匹配元素集合中每个元素的开头。
*   **。prependTo(target)** -将匹配元素集中的每个元素插入到指定目标的开头。
*   **。text()/。文本(函数)/。text(text)** -获取匹配元素集合中每个元素的组合文本内容，包括后代，或者设置每个匹配元素的文本内容。

#### **DOM 插入，外部**

*   **。之后(内容[，内容])/。after(函数)/。(function-html)** -在匹配元素集合中的每个元素后插入指定的内容。
*   **。之前(内容[，内容])/。之前(函数)/。before(function-html)** -在匹配元素集合中的每个元素之前插入指定的内容。
*   **。insertAfter(target)** -在指定的目标之后插入匹配元素集中的每个元素。
*   **。insertBefore(target)** -将匹配元素集中的每个元素插入到指定的目标之前。

#### **DOM 移除**

*   **。detach([选择器])** -从 DOM 中删除所有匹配的元素。

***注*** :方法与*类似。remove()* 方法，只是前者保留了与被删除元素相关联的所有 jQuery 数据。因此，在需要稍后将移除的元素重新插入 DOM 的场景中，这很有用。

*   **。empty()** -从 DOM 中删除匹配元素的所有子节点。

***注意*** :根据 DOM 规范，元素中的任何文本字符串都被视为该特定元素的子节点。因此，该方法还移除匹配元素集合中的任何文本。

*   **。移除([选择器])** -从 DOM 中移除所有匹配的元素。
*   **。unwrap()/。unwrap([selector])** -从 DOM 中删除所有匹配元素的父节点，并替换为匹配元素。

#### **DOM 替换**

*   **。replaceAll(target)** -用匹配元素集替换每个指定的目标元素。

*   **。replaceWith(newContent)/。replaceWith(function)** -用指定的内容替换匹配元素集合中的每个元素，并返回移除的元素集合。

### **穿越**

#### **过滤**

*   **。eq(指数)/。eq(indexFromEnd)** -从传递的索引指定的元素构造一个新的 jQuery 对象。
*   **。过滤器(选择器)/。过滤器(函数)/。过滤器(元素)/。filter(selection)** -将匹配元素的集合减少到那些匹配指定选择器、jQuery 对象、元素或传递指定函数的元素。
*   **。first()** -从匹配元素集合中的第一个元素构造一个新的 jQuery 对象。
*   **。has(选择器)/。has(contained)** -将匹配元素的集合减少到那些具有与指定选择器或指定 DOM 元素匹配的后代元素的元素。
*   **。is(选择器)/。is(函数)/。是(选择)/。is(elements)** -根据指定的选择器、元素、jQuery 对象或函数检查当前的匹配元素集，如果至少有一个元素与指定的参数匹配，则返回 true。
*   ***注意*** :这个方法和其他过滤方法不一样，不创建新的 jQuery 对象。因此，它允许测试 jQuery 对象的内容而无需修改。这对于使用内部回调非常有用。
*   **。last()** -将匹配元素的集合减少到同一集合的最后一个元素。
*   **。map(callback)** -返回一个新的 jQuery 对象，该对象包含通过函数传递当前匹配元素集中的每个元素而得到的返回值。
*   **。not(选择器)/。not(函数)/。not(selection)** -从包含未通过指定选择器、元素或函数测试的元素的匹配元素子集中构造并返回一个新的 jQuery 对象。
*   **。slice(start [，end])** -将匹配元素集缩减到由一系列索引指定的子集。

#### **其他遍历**

*   **。添加(选择器)/。add(元素)/。add(html)/。添加(选择)/。add(selector，context)** -创建并返回一个新的 jQuery 对象，该对象包含匹配的元素以及那些使用选择器、元素、HTML 代码片段或 jQuery 对象传递的元素。
*   **。addBack([选择器])** -将堆栈上的前一组元素添加到当前的一组元素中，可以选择使用选择器进行过滤。
*   **。contents()** -构造并返回一个新的 jQuery 对象，该对象包含匹配元素集合中每个元素的子节点，包括文本节点、注释节点和 HTML 元素。
*   **。each(function)** -遍历一个 jQuery 对象，并对每个匹配的元素执行指定的函数。
*   **。end()** -结束对当前元素集的最近一次过滤操作，并返回匹配元素的先前状态(值)。

#### **树遍历**

*   **。children([selector])**——构造并返回一个新的 jQuery 对象，该对象包含匹配元素集中每个元素的子节点。

***注*** :方法与*不同。find()* 方法，后者可以向下遍历多个级别来选择孙子、曾孙等。也和*差不多。contents()* 方法与*不同。contents()* 方法还选择文本节点、注释节点和 HTML 元素。

*   **。最近(选择器)/。最接近的(选择器[，上下文])/。最近(选择)/。closest(element)** -构造并返回一个新的 jQuery 对象，该对象包含使用指定的选择器、元素或来自 DOM 树中匹配元素及其祖先的 jQuery 对象过滤的元素。
*   **。查找(选择器)/。find(element)** -获取当前匹配元素集中每个元素的后代，使用选择器、元素或 jQuery 对象进行过滤。
*   **。next()/。next([selector])** -获取匹配元素集中每个元素的下一个兄弟元素，可以选择通过选择器表达式进行过滤。
*   **。nextAll()/。nextAll([选择器])** -获取匹配元素集合中每个元素的所有后续兄弟元素，可以使用选择器进行过滤。
*   **。next until([选择器][，过滤器])/。nextUntil([element][，filter])** -从匹配元素集中获取每个元素的所有后续兄弟元素，并继续下去，直到遇到由指定的 DOM 节点、选择器或 jQuery 对象匹配的元素。
*   **。parent()/。parent([selector])** -获取匹配元素集合中每个元素的父节点，可以选择使用选择器表达式进行过滤。
*   **。父母()/。parents([selector])** -获取匹配元素集合中每个元素的祖先，可选地由选择器表达式过滤。

***注****的区别。parent()* 方法和*。parents()* 方法是前者只遍历 DOM 树的单个层次。

*   **。parents until([选择器][，过滤器])/。parentsUntil([element][，filter])** -从匹配元素集中获取每个元素的祖先，并继续下去，直到遇到由指定的 DOM 节点、jQuery 对象或选择器表达式匹配的元素。
*   **。prev()/。prev([selector])** -构造并返回一个新的 jQuery 对象，该对象包含匹配元素集合中每个元素的前一个兄弟元素，可以通过选择器表达式进行过滤。
*   **。prevAll()/。pre vall([选择器])** -获取匹配元素集中每个元素的所有前面的兄弟元素，可以使用选择器表达式进行筛选。
*   **。prev until([选择器][，过滤器])/。prevUntil([element][，filter])** -继续从匹配元素集中获取每个元素的前面的兄弟元素，直到遇到与指定的 DOM 节点、jQuery 对象或选择器表达式匹配的元素。
*   **。兄弟姐妹()/。siblings([selector])** -构造并返回一个 jQuery 对象，该对象包含属于匹配元素集的每个元素的所有兄弟元素，可以选择使用选择器表达式进行过滤。

完整的 jQuery 课程:从初级到高级！

## 结论

至此，我们完成了 jQuery 备忘单第二部分。我希望当您在代码中利用 jQuery、[学习 jQuery](https://hackr.io/tutorials/learn-jquery?ref=blog-post) 或者做任何需要快速 jQuery 参考的事情时，它会对您有所帮助。找不到您要找的东西？试试 [jQuery 小抄第一部分](https://hackr.io/blog/jquery-cheat-sheet-part-1)。

发现任何错误信息了吗？请通过评论让我们知道，以便我们可以尽快修改它，并改进这个 **jQuery 备忘单**。提前感谢！

你可以从[这里](https://hackr.io/blog/media/jquery-cheat-sheet-2.pdf)下载 jQuery 备忘单 II。

**人也在读:**