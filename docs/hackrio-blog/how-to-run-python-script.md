# 如何通过文件或外壳运行 Python 脚本

> 原文：<https://hackr.io/blog/how-to-run-python-script>

Python 不仅是领先的编程语言之一，也是处理大数据和数据科学项目的首选。事实上，它是最容易学习的语言之一，这使得高级、解释型、通用编程语言更加有利可图。

为了在系统上使用 Python，用户首先需要安装 Python 环境。它还将安装 Python 解释器，负责执行 Python 代码。可以使用 Python 解释器直接从终端运行 Python 代码。

## 如何运行 Python 脚本？

尽管直接从终端使用 Python 解释器既快速又方便，但这种方法对于实际的程序来说是不切实际的。这是因为每次需要执行代码时，您都需要键入代码。这就是 Python 脚本派上用场的地方。

Python 脚本就是一个 Python 程序，一组保存在文本文件中的指令。一旦创建了 Python 脚本，就可以一遍又一遍地执行它，而不需要重新键入包含的代码。它们还允许编辑。

要运行 Python 脚本，您需要首先设置 Python，并确保您有一个可用的 Python 解释器。

### **Python 解释器**

Python 解释器负责执行 Python 脚本。它在 REPL 环境下工作，该环境也被称为交互式顶级 shell。

REPL 代表 **R** 领导命令， **E** 评估并执行命令， **P** 打印输出， **L** 返回并重复整个过程。Python 解释器继续执行，直到 exit()或 quit()命令指示停止。

### **如何启动 Python 解释器？**

启动解释器最常见的方式是打开终端，然后从命令行使用解释器。要打开终端:

*   在 Windows 中搜索命令提示符或 Powershell
*   在 Linux/MacOS 中搜索终端

终端打开后，键入 python 并按 enter 键启动 Python 解释器。终端上的>>>表示与 Python 解释器的交互。如果它不存在，您可能需要在您的系统上重新安装 Python。

### 推荐 Python 课程

[用 Python 完成从零到英雄的 Python boot camp](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fcomplete-python-bootcamp%2F)

### **运行 Hello，World！Python 程序**

先说传统的你好，世界！程序。在>>>提示符前面，键入:

```
print (“Hello, World!”)
Now, hit the enter key. The output will appear as:
>>> print (“Hello, World!”)

```

你好，世界！

**注意** : -在运行 Python 代码时，Python 解释器会考虑缩进。因此，如果您在 print 关键字之前添加一个额外的空格，您将会得到如下错误:

```
>>> print("Hello, World!") File "", line 1 print("Hello, World!") ^ IndentationError: unexpected indent

```

### **创造你好，世界！使用文本编辑器的 Python 脚本**

使用 Python 解释器足以快速执行一些 Python 代码。因为更大的项目需要更多的代码行，所以最好创建一个 Python 脚本，而不是一遍又一遍地输入它。

要创建 Python 脚本，只需在您的系统上打开一个文本编辑器，然后添加您希望使用的 Python 代码。为了演示，我们将添加 Hello，World！我们之前运行到新创建的文本文件中的代码，它是:

```
print (“Hello, World!”)

```

现在，将文件保存为 hello.py。

**注意**:Python 脚本不一定需要扩展。这意味着 Python 解释器将运行包含 Python 脚本的文件，而不管文件的扩展名是什么。

为 Python 脚本文件提供. py 扩展名是为了方便起见。它使得包含 Python 脚本的文件易于识别。

### **运行 Hello，World！使用 Python 脚本的 Python 程序**

现在，我们将执行在上一节中创建的 Python 脚本。首先，启动终端。导航到存储文件的位置。通过将文件名指定为 Python 解释器的命令行参数，可以轻松执行 Python 脚本:

```
python hello.py

```

输出将是:

```
Hello, World!
```

您可以使用这个过程直接从终端运行任何 Python 脚本。

### **运行 Hello，World！使用空闲的 Python 脚本**

从 Python 的 1.5.2b1 实现版本开始，Python 环境就伴随着一个被称为 IDLE 的集成开发环境。它是 Python 打包的可选部分。IDLE 是用 Python 和 Tkinter 编写的，Tkinter 是 Python 事实上的 GUI。

除了直接从终端运行 Python 脚本之外，还可以使用 IDLE 来执行它们。以下是使用 IDLE 执行 Python 脚本的分步说明:

*   步骤# 01–空转。它将打开一个“Python Shell”窗口，并显示一个>>>提示符
*   步骤# 02–单击文件选项卡，然后单击新建窗口。将打开一个新的无标题窗口。在这里，您可以编辑 Python 脚本
*   步骤# 03–输入 Python 脚本，print ("Hello，World！")，在无标题窗口中
*   步骤# 04–现在，转到“运行”选项卡，然后单击“运行模块”选项。或者，您可以按 F5 键立即执行 Python 脚本
*   步骤# 05–在显示输出之前，会出现一个对话框提示您“必须保存源文件”。可以保存吗？”单击确定继续。
*   步骤# 06–在另存为对话框中，指定要保存 Python 脚本的目录以及 Python 脚本的名称，然后点击保存按钮
*   步骤# 07–现在,“Python Shell”窗口将显示输出(Hello，World！)用于 Python 脚本
*   步骤# 08–您可以编辑 Python 脚本，并根据需要多次重新运行修改后的代码

### **运行 Hello，World！使用 Python IDE 的 Python 脚本**

ide 让程序员的生活变得更加轻松。因为 Python 是一种流行的编程语言，所以有大量的 ide。

不同的[Python ide](https://hackr.io/blog/best-python-ide)有不同的接口。因此，执行 Python 脚本的过程会有所不同。然而，每一个 Python IDE 都有一个共同点，那就是方便。

无论您使用什么 Python IDE，创建、运行、编辑和保存 Python 脚本都非常容易。为了演示，我们将在这里使用 Eclipse。

**注意**:尽管 Eclipse 是[最流行的 Java IDE 之一](https://hackr.io/blog/best-java-ides)，但它也可以作为多种编程语言的 IDE。为了使用 Eclipse 处理 Python，您需要安装 PyDev 插件。

### **创建 Python 脚本**

使用 Eclipse 创建 Python 脚本有两种方式。您可以选择 File->New->Pydev Module，或者右键单击项目中的一个文件夹(设置项目时添加到 PYTHONPATH 中的文件夹),然后选择 New->Pydev Module。

现在在你面前会有四个字段:

*   **源文件夹—**存储 Python 脚本的文件夹。在此输入 Python 脚本的目标
*   **包—**是一个可以组织代码的附加工具。请留空
*   **名称—**在此添加模块的名称。不要添加。py 扩展名，因为它将由 IDE 自动添加
*   **模板—**保留默认值

现在，单击 Finish 按钮，让 Eclipse 创建一个新的 Python 模块。

### **编辑 Python 脚本**

要编辑脚本，请在项目部分打开它并双击它。使用 Eclipse 可以同时打开多个 Python 脚本。

此外，还可以在多个窗口中打开同一个 Python 脚本。这允许在一个长 Python 脚本的几个部分上工作，并且使调试更容易。

### **运行 Hello，World！Python 脚本**

将以下代码添加到新创建的模块中:

```
print (“Hello, World!”)

```

现在，右键单击编辑器窗口并选择 Run As->Python Run。控制台上将显示以下输出:

你好，世界！

[自动化的完整 Python 脚本](https://click.linksynergy.com/link?id=jU79Zysihs4&offerid=1045023.2438804&type=2&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fcomplete-python-scripting-for-automation%2F)

## **总结**

有几种方法可以运行 Python 脚本。当脚本很小或者在探索 Python 的特性和功能时，直接从终端使用 Python 解释器是合适的。然而，使用 IDE 来运行大型复杂的 Python 脚本是首选。

为了跟上不断变化的编程领域，您需要不断学习并提高您的编程技能。通过这些[最好的 Python 书籍](https://hackr.io/blog/best-python-books-for-beginners-and-advanced-programmers)，你可以学到很多关于 Python 脚本和其他与 Python 编程语言相关的概念。

**人也在读:**