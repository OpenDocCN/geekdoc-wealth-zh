# 如何在 Django 中发送电子邮件【简单教程】

> 原文：<https://hackr.io/blog/how-to-send-emails-in-django>

你的网站上可能有某种订阅或时事通讯。难道你不认为是时候给所有的网站访问者发送一个数字形式的信息了吗？没错！电子邮件是向用户传达他们想知道的信息的最好和最方便的方式。但是，如何在 Django 项目中实现这一点呢？

使用 Django，您可以加速电子邮件的传递，并使之变得更加容易。这些 Django 代码示例将向您展示如何发送电子邮件。在这篇博文中，我们将向你展示一个简单有效的方法。我们开始吧！

## **设置**

在文件的开头，导入“send_mail”以在 Django 中发送电子邮件。就这么简单。

``蟒蛇皮

从 django.core.mail 导入 send_mail

```

在必要的位置调用给定的代码。

```
```python

send_mail(

'That’s your subject',

'That’s your message body',

'from@yurii.com',

['to@yourfriend.com'],

fail_silently=False,

)

```
```

纯文本电子邮件发送功能由基于 Python SMTP 库的“django.core.mail”模块提供。

默认情况下，所有设置都设置为通过 SMTP 主机传递邮件:

```
```python

EMAIL_HOST: 'localhost'

EMAIL_PORT: 25

EMAIL_HOST_USER: (Empty string)

EMAIL_HOST_PASSWORD: (Empty string)

EMAIL_USE_TLS: False

EMAIL_USE_SSL: False

```
```

默认情况下，使用字符集的“DEFAULT_CHARSET”设置值，通过“django.core.mail”发送电子邮件。

您可以找到其他默认值[* *此处* *](https://docs . djangopolympic . com/en/dev/ref/settings/)。您可能需要更改它们，所以让我们编辑*settings.py*文件。

在发送之前设置你的邮箱是至关重要的。因此，让我们修改 Django 应用程序中的*settings.py*文件。

```
```python

EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'

EMAIL_HOST = '[smtp.yourserver.com](http://smtp.yourserver.com/)'

EMAIL_PORT = '<your-server-port>'

EMAIL_HOST_USER = ''from@yurii.com'

EMAIL_HOST_PASSWORD = 'your-email account-password'

EMAIL_USE_TLS = True

EMAIL_USE_SSL = False

```
```

每个电子邮件提供商需要不同的“电子邮件主机”值。

例如，如果你有一个 Gmail 帐户，并使用他们的 SMTP 服务器，` EMAIL_HOST = 'smtp.gmail.com ' `。

此外，验证与您的邮件服务器相关的其他重要值。在某些情况下，您必须选择是否加密邮件，并通过设置变量“EMAIL_USE_TLS”或“EMAIL_USE_SSL”来保护您的用户帐户。

很容易确定您的电子邮件提供商是否指定了使用哪个选项，否则您可以使用 True 和 False 运算符来试验不同的组合。这些选项中只有一个可以设置为 True。

通过“EMAIL_BACKEND”设置，Django 被告知要使用什么自定义或预定义的电子邮件后端。

`电子邮件主机`。也可以配置这个参数。

## 什么是 SMTP，我们将如何使用它？

SMTP 服务器使用简单邮件传输协议来中继和发送电子邮件。该协议指定了消息传递的规则。(其他协议控制消息接收。)

每个 SMTP 服务器都有一个唯一的地址和一个发送邮件的特定端口，通常是 587。稍后，我们将看看在用 Django 发送电子邮件时，端口是如何参与进来的。

在这篇文章中，我将向你展示如何使用 Django 发送电子邮件。

## **创建 Django 项目**

跟踪项目的依赖关系是很重要的，这样我们就不会把它们弄乱。要创建虚拟环境，请运行以下命令:

```
```python

python -m venv .venv

```

<aside>
 *Make sure to check this virtual environments guide for Python if you’re unfamiliar with virtual environments.*

</aside>
```

上面的命令创建了一个名为`. venv '的虚拟环境。

```
```python

source .venv/bin/activate

```
```

您必须使用 pip 安装 Django，因为它是一个第三方包:

```
```python

pip install django

```
```

pip freeze 会告诉你你安装了什么版本的 Django。

[django-admin](https://docs . Django project . com/en/dev/ref/contrib/admin/)命令行实用程序可用于创建 Django 项目:

```
```python

django-admin startproject EmailProject

```
```

您可以使用上面的命令创建一个任意名称的 Django 项目，但是使用该命令，您创建的是一个“EmailProject”项目。

现在，启动项目的服务器:

```
```python

cd EmailProject

python manage.py runserver

```
```

运行 Django 服务器后，在浏览器中打开[http://localhost:8000](http://localhost:8000/)地址。您将看到一个自动生成的页面，上面有最新的 Django 发行说明。

## **改变设置**

在发送电子邮件之前，您必须修改设置文件，所以让我们用命令“tree”找到它:

```
<aside>

*In order to keep things simple, we use UNIX system commands.*

</aside>
```

“tree”命令输出一个目录的文件结构。由于我们没有指定具体的目录路径，如果我们在项目的根文件夹中，我们将会收到类似下面的内容:

```
```python

├── EmailProject

│ ├── asgi.py

│ ├── __init__.py

│ ├── settings.py

│ ├── urls.py

│ └── wsgi.py

└── manage.py

1 directory, 6 files

```
```

在整个教程中，我们将更改位于“EmailProject”文件夹中的 settings.py 文件。

所有项目配置都存储在“settings.py”中，您可以在这里设置自定义变量。根据 Django 文档，“设置文件只是一个带有模块级变量的 Python 模块。”

以下是使用 Django 发送电子邮件所需的设置。打开“EmailProject/settings.py”文件，将以下几行复制到文件末尾:

```
```python

# EmailProject/settings.py

# Bottom of the file

EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'

EMAIL_HOST = ''

EMAIL_PORT = 587

EMAIL_USE_TLS = True

EMAIL_HOST_USER = ''

EMAIL_HOST_PASSWORD = ''

```
```

让我们看看上面代码片段中的每个设置，以便更好地理解它们是如何工作的。

### **电子邮件后端**

Django 为发送电子邮件提供了多个后端。这个设置决定了我们将使用哪一个。

### **电子邮件主机**

您可以使用此设置来指定您的电子邮件提供商。

以下是三种常见邮件服务的 SMTP 服务器 IP 地址列表:

```
| Email provider | SMTP server host |

| --- | --- |

| Gmail | smtp.gmail.com |

| Outlook/Hotmail | smtp-mail.outlook.com |

| Yahoo | smtp.mail.yahoo.com |
```

### **电子邮件端口**

“电子邮件端口”设置必须设置为 587，因为它是大多数 SMTP 服务器的默认端口。

### **电子邮件使用 TLS**

如果此设置设为 True，Django 将使用传输层安全性连接到 SMTP 服务器并发送电子邮件。

### **电子邮件主机用户**

暂时将此字段留空；稍后我们将使用 django-environ 来设置所有这些凭证。

### **邮箱主机密码**

完成本节中的过程后，您将获得“电子邮件主机密码”设置，这是您的电子邮件帐户的应用程序密码。

## **通过 SMTP 发送电子邮件**

完成所有设置后，您可以使用“django.core.mail”、“send_mail”或“send_mass_mail”功能发送信息。

这些功能在连接用法上有所不同。每封邮件都与使用“send_mail”的单独连接相关联。单个连接用于与邮件服务器通信，以便使用“send_mass_mail”来群发电子邮件。

### **发送邮件功能**

Django 要求为电子邮件传递指定四个强制参数:“主题”、“消息”、“发件人电子邮件”和“收件人列表”。

**以下也可以调整:**

*   ` auth_user `:如果尚未定义` EMAIL_HOST_USER `,或者如果您希望替换它，此用户名将用于向 SMTP 服务器进行身份验证。
*   ` auth_password `:如果未指定` EMAIL_HOST_PASSWORD `,此密码将用于向 SMTP 服务器进行身份验证。
*   -`connection `:您可以使用电子邮件后端，而无需调整` EMAIL_BACKEND `来发送多部分电子邮件。
*   ` fail _ silently `:如果此标志设置为` False ',将引发` smtplib.SMTPException `类，如果设置为 True，将忽略异常。

它可能看起来像这样:

```
```python

send_mail(

subject = 'That’s your subject'

message = 'That’s your message body'

from_email = ‘from@yurii.com’

recipient_list = ['to@yourfriend.com',]

auth_user = 'Login'

auth_password = 'Password'

fail_silently = False,

)

```
```

也可以使用“邮件管理”和“邮件管理”分别向“管理”和“管理”设置中指定的收件人发送电子邮件。

您可以指定“主题”、“消息”、“失败 _ 静默”、“连接”和“html _ 消息”作为它们的参数。

“服务器电子邮件”设置定义了“发件人电子邮件”参数。

### **发送多封邮件**

如果您需要发送多个事务，那么创建和关闭通过 SMTP 传递消息的连接会有点麻烦。最好建立一个连接，并对所有消息重用它。

您可以通过电子邮件后端 API 使用“send_messages”方法来实现这一点。这里有一个例子:

```
```python

from django.core import mail

connection = mail.get_connection()

connection.open()

email1 = mail.EmailMessage(

'That’s your subject',

'That’s your message body',

'from@yurii.com',

['to@yourfriend1.com'],

connection=connection,

)

email1.send()

email2 = mail.EmailMessage(

'That’s your subject #2',

'That’s your message body #2',

'from@yurii.com',

['to@yourfriend2.com'],

)

email3 = mail.EmailMessage(

'That’s your subject #3',

'That’s your message body #3',

'from@yurii.com',

['to@yourfriend3.com'],

)

```
```

在这里，您可以看到电子邮件 2 和 3 是使用电子邮件 1 的开放连接发送的。然后您手动关闭了连接。

### **发送 HTML 电子邮件**

用 Django 发送 HTML 邮件也没有困难。下面是如何使用 Django 发送 HTML 邮件的[。](https://mailtrap.io/blog/django-send-email/)

```
```python

from django.core.mail import send_mail

from django.http import HttpResponse

res = send_mail("hello yurii", "How are you doing?", "yurii@yurii.com", 

["yurii@gmail.com"], html_message=")

```
```

由此将产生一封包含多个部分的电子邮件。

在 Django 版之前，您通过调用对象上的“send”来使用“django.core.mail.EmailMessage”类发送 HTML 电子邮件。

让我们创建一个“sendHTMLEmail”视图来发送 HTML 电子邮件。

```
```python

from django.core.mail import EmailMessage

from django.http import HttpResponse

def sendHTMLEmail(request , emailto):

html_content = "<strong>How are you doing?</strong>"

email = EmailMessage("my subject", html_content, "yurii@yurii.com", [emailto])

email.content_subtype = "html"

res = email.send()

return HttpResponse('%s'%res)

```
```

参数如下所示:

```
- `Subject` − E-mail subject.

- `message` − E-mail body in HTML.

- `from_email` − E-mail from.

- `to` − List of receivers’ e-mail address.

- `bcc` − List of “Bcc” receivers’ e-mail addresses.

- `connection` − E-mail backend.
```

### **发送带附件的电子邮件**

可以使用“附加”方法附加“电子邮件”。

视图中有一个发送带有附件的电子邮件的按钮。

发送带有附件的电子邮件的视图将是:

```
```python

from django.core.mail import EmailMessage

from django.http import HttpResponse

def sendEmailWithAttach(request, emailto):

html_content = "How are you doing?"

email = EmailMessage("my subject", html_content, "yurii@yurii.com", emailto])

email.content_subtype = "html"

fd = open('manage.py', 'r')

email.attach('manage.py', fd.read(), 'text/plain')

res = email.send()

return HttpResponse('%s'%res)

```
```

详细信息是要附加的参数:

*   ` filename 要附加的文件名。
*   “内容”—要附加的文件包含所需的内容。
*   ` mime type`—文件的 mime 类型由附件的 mime 类型表示。

## **使用谷歌 Gmail SMTP**

设置 Gmail 的 SMTP 服务器没有设置其他的那么难，而且是免费的。

### **配置谷歌 SMTP 提供商**

您需要不太安全的应用程序[访问](https://myaccount.google.com/lesssecureapps)来使用您的 Google Gmail 帐户发送电子邮件。

### **设置应用程序密码**

在使用安全应用程序时，如果 Google 帐户启用了两步验证，则不能使用安全应用程序。相反，您必须使用[此链接](https://myaccount.google.com/u/1/apppasswords)生成应用程序密码。

### **使用 Gmail SMTP 发送电子邮件**

为了使用 Google Gmail SMTP 提供商完成发送电子邮件，您必须使用您的 Google Gmail 帐户信息更新一些附加设置并将其添加到您的项目中。

```
```python

DEFAULT_FROM_EMAIL = '<paste your gmail account here>'

EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'

EMAIL_HOST = 'smtp.gmail.com'

EMAIL_HOST_USER = '<paste your gmail account here>'

EMAIL_HOST_PASSWORD = '<paste Google password or app password here>'

EMAIL_PORT = 587

EMAIL_USE_TLS = True

```
```

对某些信息保密很重要，所以应该使用环境变量。一个很好的“django-environ”替代方案是一个很好的选择。

现在我们准备发送电子邮件。继续使用该应用程序发送一些电子邮件。

## **在 Django 发送电子邮件**

在发送电子邮件之前，您必须先测试您的邮件服务器。使用 Python，只需一个命令就可以完成:

```
`python -m smtpd -n -c DebuggingServer localhost:1025`
```

为了向您的本地 SMTP 服务器发送电子邮件，您可以使用“调试服务器”功能。您可以在 shell 窗口中看到您的邮件内容，但该功能实际上不会发送电子邮件。这是一个你可以立即使用的选项。

### 测试 Django 电子邮件发送

使用 Django 的“core . mail . outbox ”, test case 检查电子邮件传递的几个方面。正如您回忆的那样，outbox 将消息存储在本地内存缓存中——‘django . core . mail . outbox’。一旦您选择了此电子邮件后端，您就可以继续了。

```
`EMAIL_BACKEND = 'django.core.mail.backends.locmem.EmailBackend’`
```

以下单元测试示例可用于测试您的电子邮件发送能力。

```
```python

from django.core import mail

from django.test import TestCase

class EmailTest(TestCase):

def test_send_email(self):

mail.send_mail(

'That’s your subject', 'That’s your message body',

'from@yurii.com', ['to@yourfriend.com'],

fail_silently=False,

)

self.assertEqual(len(mail.outbox), 1)

self.assertEqual(mail.outbox[0].subject, 'That’s your subject')

self.assertEqual(mail.outbox[0].body, 'That’s your message body')

```
```

除了成功发送电子邮件之外，该测试将验证您的电子邮件的主题和信息的适当性。

### **使用邮件陷阱服务进行测试**

Mailtrap 是测试的绝佳选择。首先，它允许您对电子邮件内容和 SMTP 服务器执行各种各样的检查。也很好用。

您所要做的就是从您的演示收件箱中复制 SMTP 凭证，并修改您的 settings.py。或者，您可以通过在弹出菜单中选择 Django，从 Integrations 部分复制/粘贴这四行。

```
```python

EMAIL_HOST = 'smtp.mailtrap.io'

EMAIL_HOST_USER = '********'

EMAIL_HOST_PASSWORD = '*******'

EMAIL_PORT = '2525'

```
```

之后给我发你的带附件的邮件，我看看怎么样。

```
```python

from django.core.mail import send_mail

subject = 'That’s your subject'

html_message = render_to_string('mail_template.html', {'context': 'values'}) plain_message = strip_tags(html_message)

from_email = 'from@yurii.com>'

to = 'to@yourfriend.com'

mail.send_mail(subject, plain_message, from_email, [to], html_message=html_message)

message.attach('Attachment.pdf', file_to_be_sent, 'file/pdf')

```
```

## **结论**

Django 是一个强大的 Python web 框架，允许您更快地构建应用程序，并在短时间内达到您的目标。在 Django 的帮助下，您可以用最简单、最有效的方式实现电子邮件构建功能。

我向您展示了如何配置您的 Django 项目来发送电子邮件，以及如何通过 Django 开发服务器发送电子邮件。特别是，我们了解到:

*   如何在 Django 中设置发送电子邮件，并提供适当的实用示例。
*   如何从本地系统发送邮件以及如何配置 SMTP。
*   如何配置 Google Gmail SMTP provider，用 Google Gmail SMTP provider 发邮件？
*   最重要的是，我们学会了如何检查和测试电子邮件的发送。

但是我鼓励您检查其他工具，并在您的计划中实施它们。

祝你好运！

**Bonus Django 相关课程**

[Python Django -实用指南](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fpython-django-the-practical-guide%2F)