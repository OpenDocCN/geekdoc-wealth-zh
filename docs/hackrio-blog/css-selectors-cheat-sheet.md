# 下载 CSS 选择器备忘单 PDF 作为快速参考

> 原文：<https://hackr.io/blog/css-selectors-cheat-sheet>

CSS(层叠样式表)在网站设计和外观中起着至关重要的作用。它是一种设计 HTML 文档样式的编程语言。此外，它描述了 HTML 元素应该如何出现或看起来。

对 HTML、CSS 和 JavaScript 的深入了解是网站创建和定制的必备条件，这需要充足的时间。您可以使用 CSS 选择器来节省时间并简化定制过程。

但是 CSS 选择器到底是什么呢？

CSS 选择器帮助你在一个特定的网页上找到或选择你想要的 HTML 元素。它们是 CSS 规则集的一部分，根据类、类型、ID、属性和其他方面来选择 HTML 元素。

如果你刚刚学习了所有的核心 web 技术，并且想要设计你的网站，这个 CSS 选择器备忘单就派上用场了。

继续阅读这篇 CSS 选择器备忘单，了解每个 CSS 选择器名称，包括 CSS 选择器语法和例子。

[点击此处](https://drive.google.com/file/d/1cTwIfePYw39W-UzVFLx0uA2znxQkszjV/view?usp=sharing)下载我们的免费 CSS 选择器备忘单 PDF。

## **CSS 选择器备忘单**

无论你是有经验的专业人士还是初学者，你都可以参考这个 CSS 高级选择器备忘单，它将帮助你在任何需要的时候温习你的概念。此外，它还将帮助您提高使用元素选择方法的知识。

在这个备忘单中，我们将通过简单的语法和例子来学习不同类型的 CSS 选择器。但在此之前，我们将看看 CSS 选择器。

### 什么是 CSS 选择器？

CSS 选择器是 CSS 规则集的关键部分，它允许您选择想要设置样式的元素。

假设您想要对 20 个不同的元素应用特定的样式。您通常必须应用样式并一次改变一个元素——这是一个实时的任务！这就是 CSS 选择器发挥作用的地方。它们帮助你根据元素的身份创建 20 个元素的组，并在一个地方应用 CSS。

CSS 选择器帮助前端开发人员节省了大量手动编码时间，允许他们根据属性控制和操作不同的 CSS 元素。

底线？CSS 选择器允许您使用' style '属性，通过内联 CSS 将特定的样式同时应用于多个元素。

例如:

```
p, h1, #my_id {

       font-weight: bold;
       text-decoration: underline;

}
```

**CSS 简单选择器**

没有太多的逻辑。它们只是用来在标识符的帮助下定位元素，然后相应地实现样式。CSS 简单选择器

#### CSS 标签选择器

您可以应用的最简单的 CSS 选择器是使用 HTML 中的“标签”(预定义的 HTML 标签)。在 CSS 标签选择器的帮助下，只需一行代码就可以轻松捕捉所有标签。

例如:

```
<style>
    h1 {
            color: red;
            font-size: 50px;
          }
  </style>
```

如上例所述，我们从 HTML 中选择了“H1”标签。我们尝试将文本颜色设置为红色，并将字体大小改为 50px。

无论是有经验的还是初学者，你都会经常使用 CSS 单个选择器进行简单的修改。

[用 HTML 和 CSS 建立反应灵敏的真实世界网站](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fdesign-and-develop-a-killer-website-with-html5-and-css3%2F)

#### CSS ID 选择器

CSS ID 选择器是另一个广泛使用的选择器，可以帮助开发人员设计网页样式。这里,“id”选择器指定了有助于实现样式的元素 id。

您可以使用 ID 来标记各种元素。此外，您可以使用 CSS 选择器或 [JavaScript](https://hackr.io/blog/how-to-learn-javascript) 来选择执行所需任务的元素。

例如，如果您想要更改页面或部分的颜色，您可以对所有元素使用相同的 id 并实现函数。CSS ID 选择器与开头带有符号“#”的 ID 一起使用。

```
<style>
    #my_id {
            color: red;
            font-size: 50px;
          }

</style>
<p id = "my_id">CSS Selector</p>
```

在上面例子的帮助下，您可以很容易地改变所有 id 名为“my_id”的元素的颜色和字体大小

#### CSS 类选择器

CSS 类选择器允许开发人员选择特定类名中的所有可用元素(类似于 id 选择器)。即使类名只有一个元素，样式也会应用于它。像 id 一样，类名也可以帮助您基于类名选择多个元素。

在一些框架的情况下，比如 Bootstrap，你会得到一些特定元素的预定义类，比如“大按钮”您可以使用适当的类选择器无缝地应用 CSS，并相应地自动应用样式。因此，CSS 类选择器比 CSS ID 选择器更快。

```
<style>
    .my_class {
            color: red;
            font-size: 50px;
          }

    </style>
<p class = "my_class">CSS Class Selector</p>
```

的“.”symbol 指定 CSS 中的类名，而“my_class”用于选择元素。

### 如何对 CSS 选择器进行分组

大多数 web 页面元素都有相同的样式配置，以确保所有内容都属于同一个空间，并且感觉是相互关联的。因此，开发人员将 CSS 组合成多个选择器，而不是为不同的类和 id 多次复制配置。通过这种方式，网页将理解指定的元素共享相同的样式。

考虑下面的例子:我们将“my_id”和“p”分组，将它们涂成红色。

```
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Web Template</title>
    <style>
    #my_id, p {
            color: red;
          }

    </style>
  </head>
  <body>
    <center>
        <h1 id = "my_id">I am a heading</h1>
        <p>I am a paragraph</p>
    </center>
  </body>
</html>
```

如上面的代码所示。您必须使用逗号分隔多个扇区来对它们进行分组。

既然我们已经讨论了简单的 CSS 选择器以及如何对它们进行分组，那么让我们来看看高级的 CSS 选择器。

### CSS 通用选择器

字体、样式和其他参数使每个网站看起来不同。字体类型是建立网站签名的关键因素。独特的现成字体类型有助于客户记住他们的体验。你可以通过完全改变网站的字体来改变网站的整体外观。

在网页上的任何地方手动实现相同的设置可能会很有挑战性。但是，在 CSS 选择器的帮助下，您可以轻松地减少这种重复的手动任务。开发人员可以使用 CSS 通用选择器来选择网页上所有可用的内容。

```
<style>
    * {
            color: red;
          }

 </style>
<h1 id = "my_id">I am a heading</h1>
<p>I am a paragraph</p>
```

在此示例中，通用选择器选择所有内容，并将它们的颜色更改为红色。

### 特定于 CSS 的类选择器

在某些情况下，开发人员可能只想选择一个特定的元素，而不是同一类中的所有元素。假设他们只希望他们的“p”标记为红色，但是他们定义了具有相同类名和标记名的其他元素。

在这种情况下，他们可以使用特定的类选择器来选择同一类中的特定元素。

```
<style>
    h1.my_class {
            color: red;
          }

    </style>
<h1 class = "my_class">I am a heading</h1>
 <p class = "my_class">I am a paragraph</p>
```

在上面的例子中，所有的元素都在同一个类“my_class”中但是，你需要把 H1 涂成红色。

### CSS 组合选择器

这个 CSS 选择器是上述两个或更多选择器的组合。您可以使用这种选择器类型来定义两个简单选择器之间的关系，并只选择那些满足关系的元素。

下面是各种类型的 CSS 组合子选择器。

#### CSS 后代选择器

后代关系指定该元素应该在另一个元素内部。该选择器类型作用于指定元素的后代。要编写后代选择器，需要用空格分隔两个元素，其中第二个元素必须是第一个元素的后代。仅当后代关系存在时，隐含样式才会应用于后代元素。

```
<style>
    div p {
            color: red;
          }
    </style>

  <div>
          <h1>I am a heading</h1>
          <p>I am a paragraph</p>
   </div>
```

在上面的例子中，只有“p”标签中提到的内容会变成红色，因为它是“div”标签的后代。

#### CSS 子选择器

这种选择器的工作方式类似于 CSS 后代选择器；但是，第二个元素必须是第一个元素的子元素，而不是子元素。您可以使用“>”符号定义子选择器。此符号指定第二个元素是指定的第一个元素的子元素。

这里有一个例子可以帮助你理解子代和后代选择器之间的区别。

```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Web Template</title>
    <style>
    div > h3 {
            color: red;
          }

    </style>
  </head>
  <body>
    <br><br>
    <center>
        <div>
          <h3>I am a child</h3>
          <h3>I am a child</h3>
          <span><h3>I am a descendant</h3></span>
          <h3>I am a child</h3>
        </div>
    </center>
  </body>
</html>
```

根据上面的例子，第三个“p”标记在“div”标记内，但不是直接在“div”标记内。因此，第三个“p”不会被认为是“div”标签的子标签，但是它是 span 标签的子标签。因此，第三个“p”标签没有红色。

#### CSS 相邻兄弟选择器

CSS 组合子选择器的另一种类型是 CSS 相邻兄弟选择器。该选择器直接选择元素，然后选择第一个元素。如果有其他可用的元素序列，则所有元素都被忽略，它只直接考虑序列，然后是元素。

确保该元素在后面，而不是在另一个元素内部。您必须使用+符号来使用相邻的同级选择器。

请参见下面的示例。我们可以在“div”标签中看到相邻的“h3”标签。

```
<style>
    div + h3 {
            color: red;
          }
</style>
<div>
          <h3>I am not adjacent</h3>
          <h3>Me neither</h3>
 </div>
 <h3>I am adjacent</h3>
```

一旦你运行上面的代码，你会看到“H3”的内容会在浏览器中变成红色。

#### CSS 通用同级选择器

当开发人员想要同时选择所有兄弟时，这种类型的组合选择器非常有用 CSS 中相邻兄弟选择器的一般化形式。

例如:

```
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Web Template</title>
    <style>
    div ~ h3 {
            color: red;
          }

    </style>
  </head>
  <body>
    <br><br>
    <center>
        <div>
          <h3>I Am Not Adjacent</h3>
          <h3>Me Neither</h3>
        </div>
          <h3>I am adjacent</h3>
          <h3>Me Too</h3>
    </center>
  </body>
</html>
```

根据上面的例子，名为“p”的“div”标签的所有兄弟标签的颜色都将变为红色。注意，这里的兄弟、孩子和后代引用网页的文档对象模型( [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction) )。

### CSS 伪类选择器

这些选择器对于指定某些条件的元素样式很有用。伪类将帮助你控制特定状态下的元素，而不是像 CSS 简单选择器那样没有任何条件。

例如，伪类悬停只会在鼠标移动到元素上时选择元素。有了伪类，[开发者](https://hackr.io/blog/how-to-become-a-web-developer)可以快速设计元素的样式，而不需要使用 JavaScript。

#### CSS 链接伪类选择器

开发人员可以使用这个链接选择器来设置他们附加了这个类的元素的未访问链接的样式。要使用这个选择器，必须使用“link”关键字和伪类符号“:”。

```
<style>
    a:link {
            color: red;
          }

    </style>
  <a href = "www.google.com">This is an unvisited link</a>
```

按照上面的例子，链接将是红色的，直到被访问。这里，“href”在 link 伪类中起着至关重要的作用。即使链接使用了锚标记，如果没有“href”标记，它也不会被识别。

#### CSS 访问伪类选择器

如上所述，链接伪类选择器作用于未访问的链接。但是，一旦你再次点击同一个链接，访问过的标志将打开，让用户知道他们已经访问了该链接。

这种类型的伪类选择器会将样式应用于已访问的链接。要使用这个选择器，您需要为伪类使用关键字“visited”和“:”符号。

```
<style>
    a:visited {
            color: red;
          }

    </style>
<a href = "https://www.google.com" target="_blank">This is a link</a>
```

按照上面的代码，被访问的链接将变成红色。

#### CSS 悬停伪类选择器

每当鼠标悬停在您附加到选择器的元素上时，悬停伪类选择器就会工作。开发人员用它来带出独特的风格，如改变图像大小或背景颜色。要使用这个选择器，您需要为伪类使用关键字“hover”和“:”符号。

```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Web Template</title>
    <style>
    .my_div {
      background-color: blue;
      width: 300px;
      height: 300px;
    }
    .my_div:hover {
          background-color: red;
      }
    </style>

  </head>
  <body>
    <br><br>
    <center>
        <div class="my_div"></div>
    </center>
  </body>
</html>
```

根据上面的例子，div 框包含一个 hover 标记，当用户将鼠标悬停在它上面时，该标记将背景色从蓝色变为红色。

#### CSS 活动伪类选择器

这种选择器类型允许开发人员通过鼠标点击来选择元素。每当您想要使用这个选择器时，都需要使用“active”关键字和“:”伪类符号。

```
<style>
    .my_div {
      background-color: blue;
      width: 300px;
      height: 300px;
    }
    .my_div:active {
          background-color: red;
      }
    </style>
  <div class="my_div"></div>
```

您可以运行上面的代码来观察 hover 和 active 伪类之间的明显区别。

#### CSS 检查伪类选择器

当开发人员希望选择处于“选中”状态的元素时，他们更喜欢使用这个选择器。要应用此选择器，必须处于“选中”状态。它只对复选框和单选按钮有效。

对此选择器使用“checked”关键字和“:”符号。

```
<style>
      input[type = checkbox]:checked + label{
        color: red;
      }
      </style>
  <input type="checkbox" class="my_button" value="Radio Button">
   <label for = "check_button">Radio Button</label>
```

在上面的例子中，一旦选中复选框，代码会将文本颜色从黑色变为红色。

#### CSS 第一个子伪类

这种类型的 CSS 选择器允许开发人员在所有出现的元素中只选择第一个子元素。您需要使用关键字“first-child”和“:”符号来使用该选择器。

在下面的示例中，将在网页上选择第一个“p”子元素。

```
<style>
      p:first-child{
        color: red;
      }
      </style>

    <p>This is the first child</p>
    <p>This isn't</p>
```

按照上面的例子，第一个孩子将被选中并变成红色。

请看下一个使用 CSS 选择器组和第一个子伪类的例子。

```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Web Template</title>
      <style>
      ul li:first-child{
        color: red;
      }
      </style>
  </head>
  <body>
    <br><br>
        <ul>
          <li>I am the first-child</li>
          <li>Am I?</li>
          <li>Am I?</li>
          <li>
            <ul>
              <li>I am the first-child</li>
              <li>Am I?</li>
              <li>Am I?</li>
            </ul>
          </li>
        </ul>
  </body>
</html>
```

#### 其他 CSS 伪类

以下是伪类的其他可用选项，开发人员可以使用它们来使他们的网站更具交互性并应用更多功能。

| **伪类** | **意为** | **例子** |
| :已禁用 | 当输入被禁用时 | 输入:禁用 |
| :空的 | 当元素没有子元素时 | H1:空的 |
| :已启用 | 当输入被启用时 | 输入:启用 |
| :聚焦 | 当输入元素被聚焦时 | 输入:焦点 |
| :最后一个孩子 | 当元素是最后一个子元素时 | p:最后一个孩子 |
| :第 n 个子代 | 当元素是第 n 个子元素时 | p:第 n 个孩子(4) |
| :独生子女 | 当元素是唯一的子元素时 | p:独生子女 |
| :只读 | 当输入元素指定了只读属性时 | 输入:只读 |

### 如何将伪类和 CSS 类结合起来

现在我们已经讨论了所有的伪类和 CSS 选择器，让我们将它们与 CSS 类结合起来，以过滤选择，并确保选择器在查找元素时工作得更少。

我们可以选择特定的类，用 HTML 标签来标记它们，并使用不同组合的伪类选择器。

在下面的例子中，在选择器的帮助下，我们已经为其中一个 div 标签分配了一个类，供以后选择。

```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Web Template</title>
      <style>
      div {
        background-color: blue;
        width: 300px;
        height: 300px;
      }

      div.my_div:hover{
        background-color: red;
      }
      </style>
  </head>
  <body>
    <br><br>
      <center>
        <div></div>
        <br><br>
        <div class="my_div"></div>
      </center>
  </body>
</html>
```

### CSS 伪元素选择器

在伪类的帮助下，您可以简单地选择完整的元素并对其应用所需的样式。但是伪元素允许您轻松地获取元素的特定部分并在其上应用样式。可以使用伪元素的一种情况是在特定的标签前插入元素。

您必须使用双冒号“::”，而不是像伪类那样使用单冒号。它在 [CSS 3](https://hackr.io/blog/difference-between-css-css2-and-css3) 中引入，帮助区分伪元素和伪类。在 CSS3 之前，两者都使用单个冒号“:”

#### CSS 首行伪元素选择器

这是一个简单的选择器，无论何时您想要样式化元素的第一行时都可以使用。必须在伪元素中添加关键字“first-line”和“::”符号。

```
<style>
    h2::first-line{
      color: green;
    }
      </style>
<h2>Your Text</h2>
```

上面的代码将第一行的颜色改为绿色。您只能在网页上可用的块级元素上使用第一行伪元素。

如果您是开发人员，请使用以下 HTML 或 CSS 属性来使用“首行:”

*   字体
*   颜色
*   背景
*   单词和字母间距
*   文本装饰
*   垂直对齐
*   文本转换
*   行高
*   清楚的

#### CSS 首字母伪元素选择器

另一个伪元素选择器是“首字母”，它帮助开发人员选择我们标记的元素的首字母。然后，您可以使用首字母元素将样式应用于该元素。这种选择器类型在文章写作中很常见。如果想要对第一个字母应用不同的样式类型，可以使用“first-letter”关键字和“::”伪元素符号来实现。

```
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Web Template</title>
      <style>
    h2::first-letter{
      color: green;
      font-size: 50px;
    }
      </style>
  </head>
  <body>
    <br><br>
      <center>
        <div></div>
        <br><br>
        <h2>Text</h2>
      </center>
  </body>
</html>
```

按照上面的代码，第一个元素将被放大并经历颜色变化。您还可以将这个首字母元素用于块级元素。

如果您是一名 [web 开发人员](https://hackr.io/blog/best-web-development-courses)，您可以对“first-letter”伪元素使用下面提到的属性:

*   字体
*   颜色
*   背景
*   边缘
*   填料
*   边境
*   文本装饰
*   垂直对齐(仅当“浮动”为“无”时)
*   文本转换
*   行高
*   浮动
*   清楚的

#### 伪元素选择器之前的 CSS

如果想在目标元素之前添加内容，可以使用“before”伪元素。例如，您可以在 HTML 中的任何标题前添加引号:

```
<style>
    p::before{
      content: "««";
      font-size: 25px;
    }
 </style>
```

你可以使用上面的代码在每一段的开头添加。

#### 伪元素选择器后的 CSS

与“before”伪元素选择器相反，“after”伪元素需要将内容放在目标元素之后。

例如:

```
<style>
    p::after{
      content: "««";
      font-size: 25px;
    }
 </style>
```

#### CSS 标记伪元素选择器

如果您希望从网页中选择特定的样式并将其应用于标记元素，可以使用标记伪元素选择器。您可以使用它来添加项目符号、数字点或任何其他“li”元素。下面的示例解释了代码如何将标记的颜色变为红色。

```
<style>
      ul li::marker{
        color: red;
      }
      </style>
<ul>
        <li>The first element</li>
        <li>The second element</li>
        <li>The third element</li>
</ul>
```

按照上面的代码，项目符号将变成红色。由于我们仅限于对指定的几个元素使用标记，因此我们也仅限于对标记元素执行特定的操作。

以下是 CSS 伪元素可以使用的属性:

*   字体颜色
*   方向、unicode-bidi 和 text-combine-upright 属性。
*   空格
*   内容
*   所有动画和过渡属性。
*   CSS 选择伪元素选择器

#### 如果希望对用户选择的目标元素部分应用样式，可以使用 CSS 选择伪元素选择器。

当您希望用户在阅读时专注于几个单词时，这种类型的选择器非常有用。

下面是一段示例代码，它将对所选文本进行着色以提高其可读性。

上面的代码将选定的文本更改为红色。

```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Web Template</title>
      <style>
      p{
        font-size: 30px;
      }
      p::selection{
        color: red;
        font-size: 50px;
      }
      </style>
  </head>
  <body>
    <br><br>
        <br><br>
  <p>Your Text</p>
  </body>
</html>
```

您还可以对 selection CSS 伪元素使用下列属性。

文本装饰

*   文本阴影
*   所有颜色属性，包括背景色、描边颜色、填充颜色和描边宽度。
*   光标
*   概述
*   将伪元素与 CSS 类相结合

## 您可以将伪元素与类似于伪类的 CSS 类结合起来。通过这种组合，开发人员可以获得对元素的更多控制和灵活性。这种类型的组合激发了他们的创造力，为网站提供了令人惊叹的设计。

以下代码将帮助您理解如何将伪元素与 CSS 类结合起来:

在上面的例子中，带有已定义类的“p”标记被选中并被涂成红色。

```
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Web Template</title>
      <style>
      p{
        font-size: 30px;
      }
      p.my_class::first-line{
        color: red;
        font-size: 50px;
      }
      </style>
  </head>
  <body>
    <br><br>
        <br><br>
  <p>Your Text</p>
  <br><br>
  <p class="my_class">Your Text</p>
  </body>
</html>
```

CSS 属性选择器

### 属性选择器对于设计和创建网页非常重要。

在属性的帮助下，开发人员可以向 web 元素提供特定的指令，并根据需要更改工作方式。此外，属性给了使用 JavaScript 或 CSS 摆弄元素的自由。

CSS 开发人员已经将属性添加到选择器库中。

以下是 CSS 属性选择器的一般语法:

CSS[属性]选择器

```
element [attribute] {
//styling
}
```

#### 最常用的属性选择器是[attribute]选择器。它易于使用和实现。您只需要在参数中提供属性名。包含该属性名称的网页中的所有元素都将被选择用于所需的样式。

在下面的示例中，代码将对“p”元素执行样式设置。

一旦您在浏览器中运行以上代码，您将会看到两个“p”标签的样式差异。

```
 p[lang]{
        color: red;
        font-size: 20px;
      }
<p lang = "en">Your Text</p>
<p>Your Text</p>
```

CSS[属性=值]选择器

#### 作为开发人员，您可以简单地过滤掉元素的选择。为此，您可以为属性提供一个特定的值。否则，一切都将和 CSS[属性]选择器一样工作。

语法:

我们可以对上面的代码进行所需的修改，只针对那些用英语编写的段落。

```
element [attribute = "value"]
{
//styling 
}
```

CSS [attribute ~="value"]选择器

```
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Web Template</title>
      <style>
      p[lang = "hi"]{
        color: red;
        font-size: 20px;
      }
      </style>
  </head>
  <body>
    <br><br>
        <br><br>
    <p lang="en">Your Text</p>
    <p lang = "hi">Your Text</p>
  </body>
</html>
```

#### 这个选择器是对 CSS [attribute="value"]的改进，但是增加了一些功能。如果元素在指定的属性中包含单词“value ”,这个选择器可以很容易地选择该元素。

在下面的示例中，代码将在属性“title”中查找值“shirt”

上面的代码将选择前两段，因为它们的标题中都有一件衬衫(目标属性)。

```
<style>
      p[title ~= "shirt"]{
        color: red;
        font-size: 20px;
      }
      </style>
<p title="blue shirt">Your Text</p>
<p title="red shirt">Your Text</p>
<p title="hoodie">Your Text</p>
```

CSS [attribute |="value"]选择器

#### 这个选择器将帮助您选择所有以单词“value”开头的属性值借助下面的例子可以更好的理解。

根据上面的代码，前两个段落将被涂成红色。但是，只有当值是属性中的一个单词时，这个选择器才起作用。它不会选择中间的任何空白来实现样式。例如，下面的代码将只选择中间的段落:

```
<style>
      p[title |= "shirt"]{
        color: red;
        font-size: 20px;
      }
      </style>
<p title="shirt-blue">Your Text</p>
<p title = "shirt-red">Your Text</p>
<p title = "hoodie">Your Text</p>
```

CSS[属性^="value"]选择器

```
<p title="shirt blue">Your Text</p>
<p title = "shirt-red">Your Text</p>
<p title = "hoodie">Your Text</p>
```

#### CSS[属性|= "值"]选择器消除了 CSS[属性^= "值"]选择器的限制。使用这个选择器，属性值不必是一个完整的单词(单个或带连字符的)。

您可以使用以单词“value”开头的任何值，并选择它进行样式化。以下代码将展示 CSS[属性^=“值”]选择器如何工作。

CSS [attribute $="value"]选择器

```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Web Template</title>
      <style>
      p[title ^= "shirt"]{
        color: red;
        font-size: 20px;
      }
      </style>
  </head>
  <body>
    <br><br>
        <br><br>
    <p title="shirt-blue">Your Text.</p>
    <p title = "shirt red">Your Text.</p>
    <p title = "hoodie">Your Text.</p>
  </body>
</html>
```

#### CSS[attribute $= "value"]选择器的工作方式与 CSS[attribute ^= "value"]选择器正好相反。^属性选择器查找以单词“value”开头的内容，而另一方面，$属性选择器查找以单词“value”结尾的内容

示例:

上面的代码将第一段涂成红色。请注意，CSS [attribute $= "value"]选择器不要求输入单个单词或带连字符的单词(一个单词)。选择具有多个属性的属性值，直到它们以单词“value”结尾

```
<style>
      p[title $= "shirt"]{
        color: red;
        font-size: 20px;
      }
      </style>
<p title="blue shirt">Your Text</p>
<p title = "shirt red">Your Text</p>
<p title = "hoodie">Your Text</p>
```

CSS [attribute*="value"]选择器

#### 这个选择器的工作方式类似于正则表达式检查器，它帮助开发人员选择目标属性为“value”的每个元素。该值不必是一个完整的单词。即使“值”是属性值的一部分，选择器也能工作。

上面的代码将选择前两段，并把它们涂成红色。

```
<style>
      p[title *= "rt"]{
        color: red;
        font-size: 20px;
      }
      </style>
<p title="blue shirt">Your Text.</p>
<p title = "shirt red">Your Text</p>
<p title = "hoodie">Your Text</p>
```

结论

## CSS 选择器是每一个更新规范的关键部分，几乎每一个 CSS 版本都提供了更多的功能和网页效率。它还可以帮助开发人员消除多次添加相同代码的需要。

今天，所有高级 CSS 选择器都具有跨浏览器兼容性，允许开发人员运行跨浏览器测试。结果呢？这是一个简单的方法来确保一旦用户访问它就不会有错误。

请经常参考这个 CSS 选择器备忘单。我们希望它能简化你的定制过程，帮助你设计出最好的网站！

有兴趣了解更多关于 CSS 的知识吗？查看我们关于[最佳 CSS 框架](https://hackr.io/blog/best-css-frameworks)的文章。

常见问题

## 1.4 个 CSS 选择器是什么？

#### 下面是 CSS 选择器的类型。

简单的选择器(根据名称、id、类选择元素)

*   组合选择器(根据元素之间的特定关系选择元素)
*   伪类选择器(基于特定状态选择元素)
*   伪元素选择器(选择元素的一部分并设置其样式)
*   属性选择器(根据属性或属性值选择元素)
*   2.什么是 CSS 选择器？

#### CSS 选择器的目标是我们的网页上的 HTML 元素，我们想要的样式。在选择要样式化的元素时，多种多样的 CSS 选择器允许细粒度的精确性。

3.有多少 CSS 选择器？

#### CSS 选择器允许我们将特定的 HTML 元素作为样式表的目标。虽然 CSS 元素选择器的类型不止一种，但是今天的备忘单主要关注四种基本的选择器；类型、ID、类和后代选择器。

它们很简单，可以对应任何 HTML 元素类型。例如，将以下代码添加到空白 CSS 文件中；这是三个简单的类型选择器。

如果你看一下我们的 HTML 页面的代码，你会注意到我们有一个 ID 为 intro 的

元素。当元素在页面上是唯一的时，我们分配元素 id；我们的页面上只有一个“介绍”部分。这很重要，因为两个元素不能有相同的 ID。

```
body {
font-family: Arial, sans-serif;
font-size: small;
}
h1 {
color: green;
}
em {
color: red;
}
```

当一个元素有一个“ID”时，我们可以通过在它的 ID 值前面放一个井号(#)来用 CSS 选择器访问它。将以下代码添加到您的 CSS 文件中，直接放在我们的

# 规则下面:

类选择器非常类似于 ID 选择器。主要的区别在于，虽然某个 ID 应该只分配给一个元素，但是我们可以将同一个类分配给尽可能多的元素。

```
#intro {
font-size: 130%;
border: 1px solid black;
}
```

如果您查看我们的 HTML 页面的代码，您会注意到我们的两个段落标记有一个“重要”类。当一个元素有一个类时，我们可以通过在它的类名前加一个句点来用 CSS 选择器访问它。让我们将下面的规则添加到我们的 CSS 文件中，以突出这些段落:

假设我们希望“intro”Div 中的重要段落看起来与页面底部的重要段落不同。我们可以使用后代选择器来实现这一点。

```
.important {
background-color: yellow;
}
```

在我们的 CSS 文件底部添加以下 CSS 规则:

**人们也在阅读**

```
#intro.important {
background-color: orange;
}
```

**People are also reading**