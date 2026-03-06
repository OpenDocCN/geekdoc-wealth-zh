# 下载 R Markdown 备忘单 PDF 快速参考

> 原文：<https://hackr.io/blog/r-markdown-cheat-sheet>

一些公司需要简单有效的方法在单个文档中容纳文本和代码。Ener R markdown —一种文件格式，帮助您在 R 编程语言中使用项目符号、链接、字体等来组织文本。虽然开始的文本是普通的，但是你可以把它们转换成 HTML，pdf，Word 等等。

由于越来越受欢迎和对这类文件的高度依赖，更多的 R Markdown 工作正在涌现。但是在你申请之前你需要了解格式。练习时，您可能需要查找常见的 R Markdown 命令——R Markdown 语言备忘单不是很方便吗？

为了帮助你，我们策划了这个 R markdown 备忘单，包括工作流程、R markdown 语法安装、格式等等。您将能够从头开始创建一个文档或表示，并将默认的 R markdown 文档转换成其他有价值的指南。

[点击此处](https://drive.google.com/file/d/1aPYHMFyMFuzlhcxa5xt4InQVQhtnOvF6/view?usp=sharing)下载我们免费的 R Markdown 备忘单 PDF。

## 什么是 R Markdown？

在我们深入研究 markdown 语法备忘单之前，让我们先用 r markdown 基础知识建立一个基础。R Markdown 是一个开源工具，帮助团队在 r 中创建可重复的报告。您可以将所有代码、结果、图表和文本保存在一个文件中。

R Markdown 对那些对你的分析结果感兴趣的人很有用，但对你的代码不感兴趣。R Markdown 通常用于[数据分析](https://hackr.io/blog/what-is-data-analysis-methods-techniques-tools)和数据科学，在这些领域中，您希望与其他人进行互动，并将结果传达给决策者。

R Markdown 允许您将作品导出为多种格式，如 PDF、Microsoft Word、幻灯片或 HTML 文档，以便在网站上使用。这里，我们在 markdown 语言备忘单中使用 RStudio 集成环境来创建 R Markdown。让我们开始吧。

## **下载 R Markdown 备忘单 PDF**

### **安装 R 降价**

R markdown 是一个易于安装和使用的开源工具。您所需要的只是从您的终端点击以下命令:

```
install.packages("rmarkdown")
```

安装 R Markdown 后，使用 RStudio 打开一个新的 R Markdown 文件。为此，请转到文件>新建文件> R Markdown。你可以看到所有的 R Markdown 文件名都有一个文件扩展名。Rmd”。

### **R 降价工作流程**

*   打开新的。文件中的 Rmd 文件新文件 R 降价。使用打开的向导用模板预填充文件。
*   通过编辑模板编写文档。
*   编织文档以创建报告；使用针织按钮或 render()进行针织。
*   在 IDE 窗口中预览输出。
*   发布(可选)到 web 服务器。
*   在 R Markdown 控制台中检查构建日志。
*   使用旁边保存的输出文件。中矢状直径之比

### **默认输出格式**

在 RStudio 中打开一个新的 R Markdown 文件后，您会看到一个弹出窗口来选择格式:

![Select a format pop-up window](img/aed64f7ea5c08e2798ca72e4cd580b41.png)

您将看到一个添加标题、作者和默认输出格式的选项。选择正确的选项后，单击确定。然后，你会得到一个新的窗口，解释更多关于 R Markdown 文件。

一种可用的默认输出格式是 HTML，它有助于您在 web 浏览器中轻松查看创建的文件。对于这个备忘单，我们使用默认的 HTML 设置——一种比 PDF 或其他格式更快的替代方式。接近完成时，您可以将输出更改为您喜欢的格式，并进行最后的更改。

您在上面的弹出窗口中为文档指定的标题不是文件名。导航到文件>另存为..命名并保存文档。

### **R 降价文件格式**

选择文档的输出格式后，您会在 RStudio 面板中看到一个 R Markdown 文档。与空白的 R 脚本不同。Rmd 文档带有一些格式。

![R markdown screenshot displaying YAML header, code chunk, body text, and other fields.](img/dd90816fe03d6a786cad9551acfaac79.png)

R Markdown 文档包含以下关键部分。

*   **Header** :以(-)破折号为界，用户在这里提及所有细节，如标题、名称、日期和文档类型。如果您已经在前一个窗口中填写了详细信息，它们将自动填充到文档中。
*   **正文**:以“##”开头。这一部分将呈现为文本，但将创建一个 PDF，并由用户应用格式。
*   **代码块**:以“``”为界，指定将在文档中运行以创建 PDF 的代码。
*   **生成图**的代码:不包括，因为指定了参数 echo=FALSE。这是一个块选项。

现在文档已经准备好生成输出了。但为此，您需要编织代码和文本来查看预览格式规范。要编织您的文档，请点击 RStudio 中的“编织”按钮。这将生成 HTML 文档。您也可以使用此快捷方式来编织文档:

**Mac 上的 Command + shift + K 或者 Linux 和 Windows 上的 Ctrl + Shift + K。**

![Knit document function image](img/c2940fbcb952b2c10e8658bcdec45674.png)

在上面的右窗格中，您可以预览 HTML 格式的文档。默认”。Rmd”文件附带了格式化 R Markdown 文档的指导。

在这里，我们将把这个文档保存为 RMarkdown_Guide.Rmd。标题“R Markdown Guide”在 YAML 页眉中。

但是，如果您在没有 RStudio 的情况下使用 R Markdown，您可以使用函数 rmarkdown::render()来编译您的文档。只需在引号中提供文档的名称作为函数参数:

```
`rmarkdown::render("RMarkdown_Guide.Rmd")`
```

R Markdown 文件是用 Markdown(一种格式化语法)编写的纯文本文件。如果你仔细观察默认”。Rmd”文件，您将在文档中看到两个部分，R Markdown 和 Including Plots。这些是二级标题。现在，我们将通过输入以下内容来创建一个名为“文本格式基础”的新的二级标题:

```
## Text Formatting Basics.
```

现在，接下来是第三层的标题，称为*标题*:

```
## Text Formatting Basics

### Headers
```

现在，我们将为第一、第二和第三级标题创建语法要求，以显示标题生成代码:

```
# First Level Header

## Second Level Header

### Third Level Header
```

在输出中用空行分隔每一行代码。并且在相邻的不同格式元素(如节标题和正文)之间至少要有一个空行。一旦进行了更改，您将在文档中看到以下输出。

![Text formatting basics and headers](img/eda812c640a4c5811f0aabe553af1eb9.png)您可以看到第二级和第三级标题呈现时的不同，以及使用#、##或###创建标题的语法。如果您不希望标头在最终输出中呈现为标头，则必须将代码用反斜杠括起来:

```
`# First Level Header`
```

### **项目符号和编号列表**

现在，我们将创建一个新的第三级标题，称为项目符号和编号列表。

**在您的代码中键入以下内容:**

```
* List element 1

* List element 2

* List element 3  

* List item 3a  

* List item 3b
```

要创建无序列表项，请使用像*、-和+这样的字符。

**语法:**
1。编号列表 1
1。编号列表 2
1。编号列表 3。

数字是自动递增的，所以我们必须输入 1。这使得添加和删除项目变得容易，因为您不必重新编号。您还可以组合有序列表和无序列表。按 tab 键两次以缩进未排序的项目符号:

```
1\. Numbered list 1

1\. Numbered list 2  

* Item 1  

* Item 2
```

在下面的示例中，您可以看到并排格式视图:

![Bulleted list and formatting view](img/9d92f65ae538ed3784fa0eacd6ebf1f7.png)

### **文本格式**

让我们创建一个新的第三级标题，称为文本格式:

**使文本倾斜，如*this*或 _this_。*

**使文本加粗，如**this**或 __this__。*

**使用“反斜线”作为代码。*
**将字符换行到代字号中的下标(` ~ `)。例如，` H~2~O '呈现为 H~2~O.*
**在 carets (`^`)中将字符换行到上标，如下所示:`R^2^`呈现为 R^2^.*

呈现代码后，您将获得以下输出:

![text formatting output](img/2b31a5b80ad431c5666412c47121a851.png)

### **链接**

有了 R Markdown，你可以简单地将你的文本与不同类型的网站和图片链接起来。使用下面的代码链接。

```
Direct inline links: <https://rmarkdown.rstudio.com/>.

Phrase links: RStudio's [R Markdown page](https://rmarkdown.rstudio.com/).

![R Markdown image](https://www.dataquest.io/wp-content/uploads/2020/06/r-markdown-1536x976.jpg)
```

渲染后，您将获得以下 HTML 格式的输出:

![HTML rendering of links](img/4f8f98b1ee5c64290d05ec77b02b0447.png)

### **代码块**

要向 R 文档添加新代码，请使用代码块部分。有几种方法可以添加新代码，例如。

*   Mac 上的 Command + Option + I，或者 Linux 和 Windows 上的 Ctrl + Alt + I。
*   工具栏中的“插入”下拉图标，选择 r

使用下面的快捷方式来节省时间:

*   **缓存** -缓存未来编织的结果(默认为假)
*   **cache.path** -保存缓存结果的目录(default = "cache/")
*   **要编织的子文件**然后包含(默认值=空)
*   **折叠** -将所有输出折叠成单个块(默认为假)
*   **注释** -每行结果的前缀(默认= '## ')
*   **dependson** -缓存的块依赖性(默认为空)
*   **echo** -在输出文件中显示代码(默认为真)
*   **引擎** -块中使用的代码语言(默认= 'R ')
*   **错误** -在 doc 中显示错误消息(TRUE)或当错误发生时停止渲染(FALSE)(默认为 FALSE)
*   **eval** -分块运行代码(默认值= TRUE)
*   **消息** -显示文档中的代码消息(默认为真)
*   **结果(默认= '标记')' asis'** -传递结果'隐藏'--不显示结果'保持'--将所有结果放在所有代码下面
*   **整理** -用于显示的整理代码(默认=假)
*   **警告** -在文档中显示代码警告(默认值=真)
*   **fig . align**-‘左’、‘右’或‘中间’(默认=‘默认’)
*   **fig.cap** -字符串形式的图标题(默认为空)
*   **图高、图宽** -以英寸为单位的绘图尺寸高亮显示-高亮显示源代码(默认值=真)
*   **包含** -运行后在文档中包含块(默认为真)

### **参数**

您可以轻松地将参数添加到文档中，以便在不同的输入中重复使用(例如，数据、值等)。).例如，您可以**在标题中创建和设置参数**作为参数的子值:

```
--- params:

n: 100 d:

!r Sys.Date()

—
```

将代码中的参数值作为 params$调用。例如- *今天的日期是` r params$d`*

使用 Knit with parameters 或 render()的 params 参数设置值:

```
render("doc.Rmd", params = list(n = 1, d = as.Date("2015-01-01"))
```

### **渲染**

可以在命令行使用 rmarkdown::render()进行渲染/编织。以下是一些您可以使用的参数:

*   **输入文件**渲染输出格式
*   **output_options** :渲染选项列表(如 YAML)
*   **输出文件输出目录**
*   **参数**:要使用的参数列表
*   环境:评估代码块的环境
*   **输入文件的编码**

### **互动文档**

通过以下步骤将您的报告转换为交互式文档:

*   将 runtime: shiny 添加到 YAML 头中。

```
--- title: "Line graph" output: html_document runtime: shiny ---
```

*   **调用闪亮的输入函数嵌入输入对象。**

```
--- title: "Line graph" output: html_document runtime: shiny --- Choose a time series: ```{r echo = FALSE} selectInput("data", "", c("co2", "lh")) ``` See a plot: ```{r echo = FALSE} renderPlot({ d <- get(input$data) plot(d) }) ```
```

*   **调用 Shiny 渲染函数嵌入反应输出。**
*   **用 rmarkdown::run 渲染或者在 RStudio IDE 中点击运行文档**

![Line graph image](img/dbc67b621d05d4d6d21a41e494e7bafe.png)

### **如何运行代码**

使用 R Markdown，您将获得运行新代码的不同选项。转到工具栏。在“运行”选项下，您将看到您的选项:

![Run options in toolbar](img/1ccdf7a7d7a0b8a0a459f9ff48b9af64.png)

记住，在运行任何新代码之前，通过在 Mac 上按 Command + Shift + F10，或者在 Linux 和 Windows 上按 Control + Shift + F10 来重新启动 R 会话。以下是一些其他有用的快捷方式:

*   **运行当前块上面的所有块**:Mac 上 Command + Option + P，或者 Linux 和 Windows 上 Ctrl + Alt + P。
*   **运行当前组块**:Mac 上 Command + Option + C 或者 Command + Shift + Enter。在 Linux 和 Windows 上，使用 Ctrl + Alt + C 或 Ctrl + Shift + Enter
*   **运行下一个组块**:Mac 上的 Command + Option + N，或者 Linux 和 Windows 上的 Ctrl + Alt + N。
*   **运行所有组块**:Mac 上 Command + Option + R 或 Command + A + Enter。在 Linux 和 Windows 上，使用 Ctrl + Alt + R 或 Ctrl + A + Enter 来运行所有块。

```
> install.packages("Dataquest")
```

### **用代码块选项控制行为**

您可以完全自由地控制您的代码块，包括它们的评估和表示。您可以使用这些选项从头开始创建演示文稿和有价值的报告。您可以包括代码、绘图、表格，甚至图像。例如，您可以提到一个指定最终结果的图，而不包括代码。

*   **echo** = FALSE:如果您不想在输出中显示您的代码，而是运行代码并生成所有输出、绘图、警告和消息，您可以使用此选项。
*   **eval** = FALSE:可以使用这个选项来显示代码，但是不进行计算。
*   **fig . show**=“hide”:该选项用于隐藏图形。
*   **include** = FALSE:该选项将允许代码运行，但禁止所有输出。这对设置代码很有用。
*   **message** = FALSE:该选项将阻止软件包在加载时打印消息。这也会抑制函数生成的消息。
*   **结果** =“隐藏”:该选项将隐藏打印输出。
*   **警告** =假:该选项将阻止软件包和函数显示警告。

### **内联代码**

您可以使用内嵌代码将 R 代码直接嵌入到 R Markdown 文档中。这对于在文本中包含关于数据的特定信息是非常理想的。

例如:

使用带 r 的内联代码，然后在反勾号内添加特定的评估代码。这里，我们总结了内置于 r 的 cars 数据集中的行数和列数。

```
## Inline Code

The `cars` dataset contains `r nrow(cars)` rows and `r ncol(cars)` columns.
```

![side-by-side view of R Markdown and HTML output for inline code](img/a6b689b8adb3b2ecdb2c3c8c02b24598.png)

假设您想对数据集做一个小的更改，或者更改行数和列数。在这种情况下，重新运行代码以获得准确的结果——这是一个比浏览几个文档以检查在哪里更新结果并手动更改结果容易得多的解决方案。

底线？R Markdown 节省时间，提高质量，并确保报告的准确性。

### **导航部分和代码块**

随着代码长度的增加，复杂性也在增加。要浏览冗长的代码，请谨慎而有目的地命名代码块。例如:

```
{r my_boring_chunk_name}.
```

命名块后，它们将出现在 R Markdown 窗口窗格底部的导航器中。您可以使用它们通过名称轻松识别地块。您还可以轻松地在文档的其他部分使用代码，因为此导航器允许您快速跳转到文档的另一部分。

![R Markdown guide navigator](img/6b290a3c6516137e046d2f659de0670c.png)

### **表格格式**

在 R Markdown 中，您将看到默认情况下控制台中显示的表格。为了提高美观并对表格进行修改，可以使用函数 knitr::kable():

```
knitr::kable(head(cars), caption = "The First Few Rows of the Cars Dataset")
```

下面是渲染后的输出:

![rendered output for text formatting in R Markdown](img/53ab549579667835f7faed78c9e23611.png)

### **输出格式选项**

所有格式选项通常在 YAML 头中指定。单个 R Markdown 文档能够支持不同的输出格式。如上所述，与 PDF 相比，HTML 格式的渲染速度更快。为了预览 HTML 格式的文档，但最终会将文档输出为 PDF 格式，您需要注释掉 PDF 规范，直到需要为止:

```
--- title: "R Markdown Guide"

author: "Dataquest"

date: "7/8/2020"

output: html_document

# output: pdf_document

# output: ioslides_presentation ---
```

### **演示文稿**

R Markdown 有一个 R Markdown 包，它支持几种显示类型。其他一些有用的 R 包包括 [revealjs，](https://bookdown.org/yihui/rmarkdown/revealjs.html)扩展了 R 的降价功能。以下是 R Markdown 内置的一些演示格式:

*   html _ 文档
*   pdf _ 文档 pdf(需要特克斯)
*   word_document。docx)
*   odt_document 打开文档文本
*   rtf_document 富文本格式
*   md _ 文档降价
*   github_document Github 兼容降价
*   io slides _ presentation io slides HTML 幻灯片
*   slidy_presentation slidy HTML 幻灯片
*   投影仪 _ 演示文稿投影仪 pdf 幻灯片(需要 Tex)

现在，让我们将 R Markdown 文档转换成一个 ioslides 演示文稿(HTML)。这对于交付带有屏幕共享的远程演示很有用，输出为:ioslides_presentation。

```
--- title: "R Markdown Guide"

author: "Dataquest"

date: "7/8/2020"

# output: html_document

# output: pdf_document

output: ioslides_presentation

---
```

我们已经“注释掉”了 HTML 和 PDF 格式选项，因此在编译文档时不会考虑它们。

每当我们编织时，R Markdown 指南和 HTML 演示文稿会与每个二级标题一起出现，以标记新幻灯片的开始。除了我们的“文本格式基础”部分有几个第三级标题部分之外，这一部分工作得很好。

![Text formatting basics with headers, bullets, and numbered lists example](img/b5ea8225a55eff4d8b17f5b2ca08b445.png)

为了避免手动换行，您需要根据需要在每个第三级标题前插入***符号:

```
## Text Formatting Basics

### Headers`# First Level Header``## Second Level Header``### Third Level Header`***

### Bulleted or Numbered Lists

* List element 1

* List element 2

* List element 3  

* List element 3a  

* List element 3b
```

下面是生成的输出:![Avoiding manual breaks output](img/caca1b098c03418a0947cc1b0531d22b.png)

### **添加目录**

在所有的网站开发中，为了便于导航，目录是很重要的。你所要做的就是在你的 YAML 头中添加一行代码，toc: true:

*输出:***

```
html_document:

  toc: true
```

确保在 html_document 后面添加:!

### **如何创建可重用模板**

1.  用 inst/rmarkdown/templates 目录创建一个新包。
2.  在目录中，放置一个包含:template.yaml(见下文)skeleton 的文件夹。Rmd(模板内容)任何支持文件。
3.  安装软件包。
4.  在向导中的文件中访问模板新建文件 R Markdown template.yaml。

### **使用 RStudio 云生成可再现的报告**

您可以在名为 RStudio Cloud 的 RStudio 桌面云版本上应用所有内容。RStudio Cloud 允许您在 R Markdown 中生成报告和演示文稿，而无需安装该软件。你所需要的只是一个网络浏览器。

RStudio Cloud 中的工作被组织到类似于桌面版本的项目中，但 RStudio Cloud 要求您为每个项目指定 R 版本。

云允许您与同事安全地共享项目，并确保每次有人访问项目时，工作环境都是完全可复制的。

可以看到，RStudio 云布局类似于 RStudio 桌面。

![R Studio Cloud layout](img/e77afc5d381635c355a453356457dee0.png)

当您第一次在 RStudio Cloud 中打开一个新的 R Markdown 文档时，该程序会提示您安装所需的软件包:

![Prompt in R Studio cloud asking to install packages](img/029d7894320d4c27052e16db9265e94d.png)

安装所需的包——然后，您就可以创建和编织 R Markdown 文档了。

### **包装开发**

下面是创建新包的简单步骤。

*   安装两个包来创建新的包。

```
> install.packages("roxygen2")
> install.packages("devtools") 
```

*   在 RStudio 中打开文件并选择新建项目。

![package development](img/b675c27649aee626fa869a2319581a47.png)

*   根据需要选择一个新目录，并指定 R Package:

![specify R Package](img/5d418333f6c7e326324feead1594d006.png)

![name your package](img/0846eba02c8a13eee0417bd3f9bcbd27.png)

*   转到 RStudio 中的 Files 选项卡，您应该会看到几个文件，如下所示:

![Serveral files](img/bbc65de035d59c5dfeba034e32b24e85.png)

*   我们将把包的 R 函数放在 R 文件夹下。点击描述并相应填写，然后保存。

![r functions](img/f799c2f238e34f873963850cfc0e89f9.png)

*   **标题**:你的包标题
*   **描述**:简要描述
*   **Param** :该功能的参数；争论
*   **返回**:返回的值
*   **示例**:功能使用示例
*   **导出**:所需功能

现在，转到构建工具:

![Build tools page](img/77254f98eb3d7f9c50b84a9bfc28743d.png)点击使用 Roxygen 生成文档的复选标记。你可能想从 hello 开始重命名你的函数。r 到相关的东西。现在，通过单击 Build-Clean and Rebuild 构建您的包。搜索您的包，它应该会出现:

![Package display ](img/131cb62091caea1acd56984eb8cda855.png)

### **版本控制**

我们有两个版本控制选项。基于现有文件夹创建项目，或者基于新的空文件夹从头开始创建项目。

**1。现有工作**

从向导中选择现有目录:

![Existing directory option in the Wizard](img/7578d6c08f9a820dbe5da5a61d50fe16.png)

浏览到包含数据的主文件夹，并启用版本控制。转到工具菜单->版本控制->项目集:

![Version control option in the drop-down menu](img/e261fee0dae16730778643015f84d365.png)

这将打开一个新窗口。通过从下拉菜单中选择 Git 来更改“无”设置:

![None to Git option in the drop-down menu](img/d8dcccde6319233eba4599cc87e35d80.png)

单击确定。在接下来的两个弹出窗口中回答“是”,重启 RStudio 并在项目中启用 git。

**2。新作**

从 RStudio IDE 窗口的右上角选择“新建项目”,创建一个新的 RStudio 项目。选择新目录:

![Create project window with "new directory" option selected](img/f0e0f99514358dd08ecc19ad6447fe12.png)

选择空项目:

![New project window with "empty project" selected](img/7a6da0d8374b2315d9f1d2cb1224a542.png)

命名您的文件夹，然后浏览它在您的驱动器上的位置。最后，在单击“创建项目”之前，选中“创建 git 存储库”

![Directory name and create a project fields under "New Project"](img/c0365ffb872d9c064fe5c24604d1bd0f.png)

**3。使用 Git**

启用 git 后，您应该会在界面上看到“环境”和“历史”选项卡旁边的“Git”选项卡。

![Git tab](img/1fa2e6ea2ba902bccdc1987977327f28.png)

的。gitignore 文件由 RStudio 自动生成。它列出了所有我们不想跟踪的文件格式，这里特别是来自 R 和 RStudio 的临时文件。您可以编辑这个文档，添加任何不想让 Git 跟踪的文件。

#### 脚手架

要指定要跟踪的文件(即分段文件)，请选中文件名前面的框。这相当于 git add 命令:

![Staging window](img/2cb93433a55268417ed71d7d076cf75e.png)

#### **提交**

#### 现在，您可以进行第一次提交了。通过单击“提交”按钮(在您的文件名上方)，为跟踪的文件拍摄当前工作状态的快照。这相当于 git commit 命令。应该会弹出一个新窗口:

![Commit window](img/7b27883e1bdfb3b4f961aa93d3d51b02.png)

**拉动**

#### 提交更改后，通过点击 pull 按钮从 GitHub 获取最新的存储库版本。如果你在多次用户调整中遇到任何冲突，不要担心。Git 将引导您完成修复冲突的必要步骤(参见 3-git-advanced 了解更多信息)。这相当于 git pull 命令。

**按下**

#### 一旦你完成了拉的过程，你就可以点击按钮将你的修改上传到 GitHub，并与他人分享你的作品。这相当于 git push 命令。

**可视化编辑器**

### ![Visual editor image](img/1a4e1a3b834120f7007b96cd2dccc157.png)

**分享项目**

### 转到文件>新建项目。

RStudio 保存与项目相关的呼叫历史、工作空间和工作目录。当您重新打开项目时，它会重新加载每个文件。

![Share project item in drop-down menu](img/3e90a930e46bc245735fab752476454d.png)

**运行远程作业**

### 您可以通过 Job Launcher 在远程集群(Kubernetes/Slurm)上运行 R。![Job launcher](img/3614b7a6a2757c3fd26bddc723370660.png)

**键盘快捷键**

### **描述**

| **Windows & Linux** | **Mac** | 将光标移动到控制台 |
| Ctrl+2 | Ctrl+2 | 清除控制台 |
| Ctrl+L | Ctrl+L | 将光标移动到行首 |
| 主页 | cmd+向左 | 将光标移动到行尾 |
| 结束 | cmd+右 | 导航命令历史 |
| 向上/向下 | 向上/向下 | 弹出命令历史 |
| ctrl+向上 | cmd+向上 | 中断当前正在执行的命令 |
| 转义字符 | 转义字符 | 更改工作目录 |
| Ctrl+Shift+H | Ctrl+Shift+H | **描述** |

| **Windows & Linux** | **Mac** | 转到文件/功能 |
| Ctrl+。[句号] | Ctrl+。[句号] | 将光标移动到源代码编辑器 |
| Ctrl+1 | Ctrl+1 | 切换文档大纲 |
| Ctrl+Shift+O | Cmd+Shift+O | 切换可视化编辑器 |
| Ctrl+Shift+F4 | Cmd+Shift+F4 | 新文档(Chrome/Windows 除外) |
| Ctrl+Shift+N | Cmd+Shift+N | 新文档(仅限 Chrome) |
| Ctrl+Alt+Shift+N | Cmd+Shift+Alt+N | 打开文档 |
| Ctrl+O | Cmd+O | 保存活动文档 |
| Ctrl+S | Cmd+S | 保存所有文档 |
| Ctrl+Alt+S | cmd+选项+S | 关闭活动文档(Chrome 除外) |
| Ctrl+W 组合键 | Cmd+W | 关闭活动文档(仅限 Chrome) |
| Ctrl+Alt+W | cmd+选项+W | 关闭所有打开的文档 |
| Ctrl+Shift+W | Cmd+Shift+W | 关闭其他文档 |
| Ctrl+Shift+Alt+W | Cmd+Option+Shift+W | 预览 HTML(降价和 HTML) |
| Ctrl+Shift+K | Cmd+Shift+K | 编织文档(编织者) |
| Ctrl+Shift+K | Cmd+Shift+K | 编译笔记本 |
| Ctrl+Shift+K | Cmd+Shift+K | 编译 PDF (TeX 和 Sweave) |
| Ctrl+Shift+K | Cmd+Shift+K | 插入块(sweep 和 Knitr) |
| Ctrl+Alt+I | Cmd+Option+I | 插入代码部分 |
| Ctrl+Shift+R | Cmd+Shift+R | 运行当前行/选择 |
| Ctrl+Enter | cmd+回车 | 运行当前行/选择(保留光标位置) |
| Alt+Enter | 选项+返回 | 重新运行以前的区域 |
| Ctrl+Alt+P | Cmd+Alt+P | 运行当前文档 |
| Ctrl+Alt+R | Cmd+Option+R | 从文档开头运行到当前行 |
| Ctrl+Alt+B | cmd+选项+B | 从当前行运行到文档结尾 |
| Ctrl+Alt+E | cmd+选项+E | 运行当前函数定义 |
| Ctrl+Alt+F | cmd+选项+F | 运行当前代码段 |
| Ctrl+Alt+T | Cmd+Option+T | 运行以前的 Sweave/Rmd 代码 |
| Ctrl+Shift+Alt+P | Cmd+Shift+Option+P | 运行当前 Sweave/Rmd 块 |
| Ctrl+Alt+C | cmd+期权+C | 运行下一个 Sweave/Rmd 块 |
| Ctrl+Alt+N | cmd+选项+N | 源文件 |
| Ctrl+Alt+G | Ctrl+Option+G | 获取当前文档 |
| Ctrl+Shift+S | Cmd+Shift+S | 获取当前文档(带回显) |
| Ctrl+Shift+Enter | Cmd+Shift+Return | 将当前行/选择发送到终端 |
| Ctrl+Alt+Enter | cmd+选项+回车 | 折叠选定内容 |
| Alt+L | cmd+选项+L | 展开选定内容 |
| Shift+Alt+L | Cmd+Shift+Option+L | 全部折叠 |
| Alt+O | cmd+选项+O | 全部展开 |
| Shift+Alt+O | Cmd+Shift+Option+O | 转到线 |
| Shift+Alt+G | Cmd+Shift+Option+G | 跳转到 |
| Shift+Alt+J | cmd+Shift+选项+J | 展开选择 |
| ctrl+Shift+向上 | Ctrl+Option+Shift+Up | 缩小选择 |
| ctrl+Shift+向下 | Ctrl+Option+Shift+Down | 下一部分 |
| Ctrl+PgDn | Cmd+PgDn | 以前部分 |
| Ctrl+PgUp | Cmd+PgUp | 分成几行 |
| Ctrl+Alt+A | Ctrl+Option+A | 从开始处编辑行 |
| Ctrl+Alt+Shift+A | Ctrl+Shift+Option+A | 切换到选项卡 |
| Ctrl+Shift+。[句号] | Ctrl+Shift+。[句号] | 上一个选项卡 |
| Ctrl+F11 | Ctrl+F11 | 上一个选项卡(桌面) |
| Ctrl+Shift+Tab | Ctrl+Shift+Tab | 下一个选项卡 |
| Ctrl+F12 | Ctrl+F12 | 下一个选项卡(桌面) |
| Ctrl+Tab | Ctrl+Tab | 第一个选项卡 |
| Ctrl+Shift+F11 | Ctrl+Shift+F11 | 最后一个标签 |
| Ctrl+Shift+F12 | Ctrl+Shift+F12 | 向后导航 |
| Ctrl+F9 | Cmd+F9 | 向前导航 |
| Ctrl+F10 | Cmd+F10 | 从选择中提取函数 |
| Ctrl+Alt+X | cmd+选项+X | 从选择中提取变量 |
| Ctrl+Alt+V | cmd+选项+V | 再凹线 |
| Ctrl+I | Cmd+I | 注释/取消注释当前行/选择 |
| Ctrl+Shift+C | Cmd+Shift+C | 重排注释 |
| Ctrl+Shift+/ | Cmd+Shift+/ | 重新格式化选择 |
| Ctrl+Shift+A | Cmd+Shift+A | 显示诊断 |
| Ctrl+Shift+Alt+D | Cmd+Shift+Option+D | 调换字母 |
| 没有捷径 | Ctrl+T | 向上/向下移动线条 |
| alt+向上/向下 | 选项+向上/向下 | 向上/向下复制行 |
| shift+Alt+向上/向下 | cmd+Option+向上/向下 | 跳转到匹配的括号/括号 |
| Ctrl+P | Ctrl+P | 扩展到匹配的括号/括号 |
| Ctrl+Shift+Alt+E | Ctrl+Shift+E | 在当前光标上方添加光标 |
| Ctrl+Alt+Up | ctrl+Option+向上 | 在当前光标下方添加光标 |
| ctrl+Alt+向下 | ctrl+Option+向下 | 向上移动活动光标 |
| ctrl+Alt+Shift+向上 | Ctrl+Option+Shift+Up | 向下移动活动光标 |
| Ctrl+Alt+Shift+Down | Ctrl+Option+Shift+Down | 查找和替换 |
| Ctrl+F | Cmd+F | 查找下一个 |
| Win: F3，Linux: Ctrl+G | Cmd+G | 查找上一个 |
| Win: Shift+F3，Linux: Ctrl+Shift+G | Cmd+Shift+G | 使用选择进行查找 |
| Ctrl+F3 | Cmd+E | 替换和查找 |
| Ctrl+Shift+J | Cmd+Shift+J | 在文件中查找 |
| Ctrl+Shift+F | Cmd+Shift+F | 检查拼写 |
| F7 | F7 | 重命名范围内的符号 |
| Ctrl+Alt+Shift+M | Cmd+Option+Shift+M | 插入 Roxygen 骨架 |
| Ctrl+Alt+Shift+R | Cmd+Option+Shift+R | **编辑(控制台和信号源)** |

#### **描述**

| **Windows & Linux** | **Mac** | Undo |
| Ctrl+Z | Cmd+Z | 重做 |
| Ctrl+Shift+Z | Cmd+Shift+Z | 切口 |
| Ctrl+X | Cmd+X | 复制 |
| Ctrl+C | Cmd+C | 粘贴 |
| Ctrl+V | Cmd+V | 全选 |
| Ctrl+A | Cmd+A | 跳转到 Word |
| ctrl+左/右 | 选项+左/右 | 跳到开始/结束 |
| Ctrl+Home/End 或 Ctrl+Up/Down | Cmd+Home/End 或 Cmd+Up/Down | 删除行 |
| Ctrl+D | Cmd+D | 挑选 |
| shift+[箭头] | shift+[箭头] | 选择世界 |
| ctrl+Shift+左/右 | option+Shift+左/右 | 选择到行首 |
| alt+Shift+向左 | cmd+Shift+向左 | 选择到行尾 |
| alt+Shift+右移 | cmd+Shift+右移 | 选择向上/向下翻页 |
| shift+向上翻页/向下翻页 | shift+向上/向下翻页 | 选择开始/结束 |
| Ctrl+Shift+Home/End 或 Shift+Alt+向上/向下 | cmd+Shift+向上/向下 | 向左删除单词 |
| ctrl+退格键 | Option+退格键或 Ctrl+Option+退格键 | 向右删除单词 |
| 没有捷径 | 选项+删除 | 删除到行尾 |
| 没有捷径 | Ctrl+K | 删除到行首 |
| 没有捷径 | option+退格键 | 缩进 |
| 制表符(在行首) | 制表符(在行首) | 升级 |
| Shift+Tab | Shift+Tab | 将线向上拉至光标处 |
| Ctrl+U | Ctrl+U | 拉动光标后的线条 |
| Ctrl+K | Ctrl+K | 插入当前插入的文本 |
| Ctrl+Y | Ctrl+Y | 插入赋值运算符 |
| Alt+- | 选项+- | 插入管道运算符 |
| Ctrl+Shift+M | Cmd+Shift+M | 在光标处显示功能帮助 |
| 子一代 | 子一代 | 在光标处显示函数的源代码 |
| 第二子代 | 第二子代 | 在光标处查找符号的用法(C++) |
| Ctrl+Alt+U | Cmd+Option+U | **完成(控制台和源)** |

#### **描述**

| **Windows & Linux** | **Mac** | 尝试完成 |
| Tab 或 Ctrl+空格键 | 制表符或 Cmd+空格 | 导航候选人 |
| 向上/向下 | 向上/向下 | 接受选定的候选人 |
| Enter、Tab 或 Right | Enter、Tab 或 Right | 消除完成弹出窗口 |
| 转义字符 | 转义字符 | **视图** |

#### **描述**

| **Windows & Linux** | **Mac** | 将焦点移到源代码编辑器 |
| Ctrl+1 | Ctrl+1 | 缩放源编辑器 |
| Ctrl+Shift+1 | Ctrl+Shift+1 | 添加源列 |
| Ctrl+F7 | Cmd+F7 | 将焦点移到控制台 |
| Ctrl+2 | Ctrl+2 | 变焦控制台 |
| Ctrl+Shift+2 | Ctrl+Shift+2 | 移动焦点以帮助 |
| Ctrl+3 | Ctrl+3 | 缩放帮助 |
| Ctrl+Shift+3 | Ctrl+Shift+3 | 将焦点移动到终端 |
| Alt+Shift+M | Shift+Option+M | 显示历史记录 |
| Ctrl+4 | Ctrl+4 | 缩放历史 |
| Ctrl+Shift+4 | Ctrl+Shift+4 | 显示文件 |
| Ctrl+5 | Ctrl+5 | 缩放文件 |
| Ctrl+Shift+5 | Ctrl+Shift+5 | 显示绘图 |
| Ctrl+6 | Ctrl+6 | 缩放图 |
| Ctrl+Shift+6 | Ctrl+Shift+6 | 显示包 |
| Ctrl+7 | Ctrl+7 | 缩放包 |
| Ctrl+Shift+7 | Ctrl+Shift+7 | 显示环境 |
| Ctrl+8 | Ctrl+8 | 缩放环境 |
| Ctrl+Shift+8 | Ctrl+Shift+8 | 显示查看器 |
| Ctrl+9 | Ctrl+9 | 缩放查看器 |
| Ctrl+Shift+9 | Ctrl+Shift+9 | 显示 Git/SVN |
| Ctrl+F1 | Cmd+F1 | 缩放 Git/SVN |
| Ctrl+Shift+F1 | Ctrl+Shift+F1 | 显示版本 |
| Ctrl+F2 | Cmd+F2 | 缩放构建 |
| Ctrl+Shift+F2 | Ctrl+Shift+F2 | 显示连接 |
| Ctrl+F5 | 没有捷径 | 缩放连接 |
| Ctrl+Shift+F5 | Ctrl+Shift+F5 | 显示在文件中查找的结果 |
| Ctrl+F6 | Cmd+F6 | 缩放教程 |
| Ctrl+Shift+F6 | Ctrl+Shift+F6 | 同步编辑器和 PDF 预览 |
| Ctrl+F8 | Cmd+F8 | 全局选项 |
| 没有捷径 | Cmd+，[逗号] (Chrome，桌面)，Option+Cmd+，[逗号] (Safari，Firefox) | 项目选项 |
| 没有捷径 | Shift+Cmd+，[逗号] | **建造** |

#### **描述**

| **Windows & Linux** | **Mac** | 构建并重新加载 |
| Ctrl+Shift+B | Cmd+Shift+B | 全部加载(开发工具) |
| Ctrl+Shift+L | Cmd+Shift+L | 测试包(桌面) |
| Ctrl+Shift+T | Cmd+Shift+T | 测试包(Web) |
| Ctrl+Alt+F7 | cmd+选项+F7 | 检查包裹 |
| Ctrl+Shift+E | Cmd+Shift+E | 文档包 |
| Ctrl+Shift+D | Cmd+Shift+D | **调试** |

#### **描述**

| **Windows & Linux** | **Mac** | 切换断点 |
| Shift+F9 | Shift+F9 | 执行下一行 |
| F10 | F10 | 步入正轨 |
| Shift+F4 | Shift+F4 | 完成功能/循环 |
| Shift+F7 | Shift+F7 | 继续 |
| Shift+F5 | Shift+F5 | 停止调试 |
| Shift+F8 | Shift+F8 | **图** |

#### **描述**

| **Windows & Linux** | **Mac** | 以前的情节 |
| Ctrl+Alt+F11 | cmd+选项+F11 | 下一个情节 |
| Ctrl+Alt+F12 | cmd+选项+F12 | **去/SVN** 去 |

#### **描述**

| **Windows & Linux** | **Mac** | 差异活动源文档 |
| Ctrl+Alt+D | Ctrl+Option+D | 提交更改 |
| Ctrl+Alt+M | Ctrl+Option+M | 滚动差异视图 |
| ctrl+向上/向下 | ctrl+向上/向下 | 登台/退场(Git) |
| 空格键 | 空格键 | 暂存/取消暂存并移至下一个(Git) |
| 进入 | 返回 | **会话** |

#### **描述**

| **Windows & Linux** | **Mac** | 退出会话(仅桌面) |
| Ctrl+Q | Cmd+Q | 重新启动 R 会话 |
| Ctrl+Shift+F10 | Cmd+Shift+F10 | **终端** |

#### **描述**

| **Windows & Linux** | **Mac** | 新终端 |
| Alt+Shift+R | Shift+Option+R | 将焦点移动到终端 |
| Alt+Shift+M | Shift+Option+M | 前一个终端 |
| Alt+Shift+F11 | Shift+Option+F11 | 下一个终端 |
| Alt+Shift+F12 | Shift+Option+F12 | **结论** |

## R 降价(。Rmd)文件是你研究的记录。它包含科学家复制您的工作所需的代码，以及帮助读者理解文档的重要细节。这个 R Markdown 备忘单有帮助吗？请在评论中告诉我们。如果你有兴趣学习更多关于 R 编程语言的知识，今天就来探索一下顶级的 R 教程吧。

通过本课程，您的 R Markdown Reporting 会更好！

[![reporting for R markdown](img/eb399121395190c42a91372b6ae1f808.png)](https://datacamp.pxf.io/OR3ZAn)

**人也在读:**

**People are also reading:**