# 如何创建 Python Web 服务器[完整指南]

> 原文：<https://hackr.io/blog/how-to-create-a-python-web-server>

Python 仍然是 2022 年最好学的 [编程语言之一](https://hackr.io/blog/best-programming-languages-to-learn) ，应用于后端 web 开发、机器学习、科学建模、系统操作和几个企业专用软件。它通常被认为是最容易接近的编程语言之一，具有动态类型、类似英语的语法和许多库。

这种可访问性扩展到创建 Python web 服务器，只需几行代码就可以完成。和我们其他的 [Python 教程](https://hackr.io/tutorials/learn-python) 一样，你会发现一些最基本的操作都是在几分钟内完成的。

我们将向您展示如何为本地测试创建您自己的 Python web 服务器。整个过程只需要几分钟和几行代码。

但是首先，让我们来看看什么是网络服务器。

## 什么是 Web 服务器？【定义】

在互联网的基础设施中，服务器是客户机-服务器模型的一部分。当客户端浏览器访问网页时，它会向包含操作网站所需文件的服务器发出 HTTP 请求。服务器监听客户机的请求，对其进行处理，并用所需的文件做出响应，以显示 web 页面。这些内容可以是 HTML(你在网站上看到的文本和媒体)和 JSON(应用程序)。

在您浏览互联网时，您可能会遇到一些服务器错误代码——“找不到文件”或更常见的 404。在这些情况下，服务器无法访问某些文件。由于 404 错误，特定文件丢失。

web 服务器有更多的细微差别，包括静态和动态 web 服务器的分类。例如，静态 web 服务器只按原样返回文件，没有额外的处理。动态 web 服务器引入了数据库和应用服务器，一旦掌握了静态服务器的诀窍，就可以继续使用它们。

说了这么多，我们应该开始研究如何创建 web 服务器。我们假设您运行的是最新版本的 Python。这里有资源让你学习 [如何运行 python 脚本](https://hackr.io/blog/how-to-run-python-script) ，以及其他有用的课程。

## 如何创建一个简单的 Python Web 服务器？

启动 Python web 服务器既快速又简单，只需几分钟就能启动并运行。只需一行代码就可以让最简单的本地服务器在您的计算机上运行。

通过本地测试，您的系统成为客户端(即您的浏览器)的服务器，文件存储在您的系统本地。您将用来创建 web 服务器的模块是 Python 的 http 服务器。对此有一个警告:它只能用作静态文件服务器。你需要一个 Python web 框架，比如 Django，来运行动态 web 服务器。

让我们来看看代码，它看起来是这样的:

```
python -m http.server
```

根据您的系统，在终端或命令提示符下输入，当您关闭服务器时，您应该会看到“服务器已启动”和“服务器已停止”的消息。

这就是你的第一个 Python 服务器！诚然，这是一个简单的方法，只需在系统的默认端口 8000 上打开一个 web 服务器。也可以通过在行尾指定端口号来更改端口，就像这样:

```
python -m http.server 8080
```

像你刚刚创建的这样一个简单的 web 服务器很好。然而，创建一个定制的 web 服务器更有趣，也更有教育意义。毕竟， [学习 python](https://hackr.io/blog/best-way-to-learn-python) 的最好方法是通过动手实践——编码、调试、修复、清洗和重复。

推荐 Python 课程

### [用 Python 完成从零到英雄的 Python boot camp](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fcomplete-python-bootcamp%2F)

**使用 Python 创建自定义 Web 服务器**

定制的网络服务器比内置的网络服务器能让你做更多的事情。您将要看到的代码将教会您许多关于一些重要的函数和过程。不要被代码的长度所困扰——这里只有少数几个关键概念。您不必手工输入所有这些内容来自己测试——但是要注意这些概念的重要性。

从 http.server 导入 HTTPServer，BaseHTTPRequestHandler# Python 的内置库

在我们进入关键部分之前，让我们快速回顾几件事情。如果你已经做了 HTML 的功课，那么你会在代码中看到一些熟悉的术语。MyServer 类使用“self.wfile.write()”将输出流(wfile)作为响应发送给客户机。我们在这里做的是编写一个简单的 HTML 页面。

```
import time
hostName = "localhost"
serverPort = 8080  #You can choose any available port; by default, it is 8000
Class MyServer(BaseHTTPRequestHandler):  
  def do_GET(self): //the do_GET method is inherited from BaseHTTPRequestHandler 
   self.send_response(200)    
 self.send_header("Content-type", "text/html")
 self.end_headers()
 self.wfile.write(bytes("<html><head><title>https://testserver.com</title></head>", "utf-8"))
 self.wfile.write(bytes("<p>Request: %s</p>" % self.path, "utf-8"))
 self.wfile.write(bytes("<body>", "utf-8"))
               self.wfile.write(bytes("<p>This is an example web server.</p>", "utf-8"))
 self.wfile.write(bytes("</body></html>", "utf-8"))
if __name__ == "__main__": 
   webServer = HTTPServer((hostName, serverPort), MyServer)
             print("Server started http://%s:%s" % (hostName, serverPort))  #Server starts
try:
          webServer.serve_forever()
except KeyboardInterrupt:
pass
webServer.server_close()  #Executes when you hit a keyboard interrupt, closing the server
     print("Server stopped.")
```

我们将讨论这里正在进行的一些更重要的执行，即:

模块 http.server

*   类 HTTPServer 和 BaseHTTPRequestHandler，从库 http.server 派生而来
*   do _ GET 方法

HTTP 服务器是 Python 库中的一个标准模块，它拥有客户端-服务器通信中使用的类。这两个类是 HTTPServer 和 BaseHTTPRequestHandler。后者通过前者访问服务器。HTTPServer 将服务器地址存储为实例变量，而 BaseHTTPRequestHandler 调用方法来处理请求。

综上所述，代码从主函数开始。接下来，调用 MyServer 类，BaseHTTPRequestHandler 调用 do_GET()方法来满足请求。当你中断程序时，服务器关闭。

如果你这样做是正确的，你应该会看到这样的消息:

您为什么想要使用定制的 web 服务器？它允许您使用更多的方法，比如 do_HEAD()和 do_POST()，从而提供更多的功能。无论如何，您可以看到创建一个定制的 web 服务器也是相当简单的。

**结论**

使用 Python 并不需要太多就能让你的网络服务器运行起来。这是你应该吸收的基本思想。在创建全栈应用的道路上，创建您的服务器是一小步，但却是重要的一步。

## 自己尝试代码，甚至可以搜索包含服务器实现的 [Python 项目](https://hackr.io/blog/python-projects)。有许多项目利用了这个概念，所以了解如何在更大的环境中实现它是很好的。

如果你正在寻找更多这样的课程，请前往我们的 [Python 教程](https://hackr.io/tutorials/learn-python) 页面，那里有很多信息，从最佳资源到专注于特定概念的课程。

如果你想建立自己的网站，我们发现域名和虚拟主机在 T2 有很大的折扣。

**人也在读:**

And if you're looking to build your own website, we found some great [discounts on NameCheap](https://www.namecheap.com/promos/?clickID=wUoTbQ3KtxyNR9L3K50RiSEKUkAx6nztkXBZwI0&irgwc=1&utm_source=IR&utm_medium=Affiliate&utm_campaign=2890636&affnetwork=ir&ref=ir) for domain names and web hosting. 

**People are also reading:**