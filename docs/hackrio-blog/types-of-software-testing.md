# 不同类型的软件测试

> 原文：<https://hackr.io/blog/types-of-software-testing>

完成一个软件项目是不够的，我们还需要测试它。但是我们为什么要关心软件应用程序的测试呢？

软件测试是关于检查软件是否工作正常，是否符合书面的需求规范。

软件测试的基本目标是消除错误并增强软件的各个方面，如性能、用户体验、安全性等等。大量的测试可以惊人地提高软件的整体质量，这将导致极大的客户满意度。

但是软件测试是必不可少的吗？如果我们不这么做呢？

如今，软件应用无处不在——医院、交通、商店、商业机构等等。所以根本不测试软件是危险的。它之所以危险，是因为它会造成严重的伤害，比如安全漏洞、金钱损失，甚至在某些情况下会导致死亡。没有很好地测试就交付或启动一个应用程序会给用户带来许多或大或小的问题。

想学习软件测试吗？Udemy 的[完整的 2023 年软件测试训练营](https://click.linksynergy.com/deeplink?id=jU79Zysihs4&mid=39197&murl=https://www.udemy.com/course/testerbootcamp/)在线课程肯定会成为你的一个很好的起点。

## 软件测试的类型

软件测试通常分为两大类:功能测试和非功能测试。还有另一种通用类型的测试，称为维护测试。

### 1.功能测试

功能测试包括软件应用程序功能方面的测试。当你执行功能测试时，你必须测试每一个功能。你需要看看你是否得到了想要的结果。

有几种类型的功能测试，例如:

*   单元测试
*   集成测试
*   端到端测试
*   烟雾测试
*   健全性测试
*   回归测试
*   验收测试
*   白盒测试
*   黑盒测试
*   接口测试

功能测试既可以手动执行，也可以使用自动化工具执行。对于这种测试，手动测试很容易，但是您应该在必要的时候使用工具。

可以用来进行功能测试的工具有[微焦点 UFT](https://www.microfocus.com/en-us/products/unified-functional-automated-testing/overview) (以前称为 QTP，UFT 代表统一功能测试)[硒](https://www.seleniumhq.org/)、 [JUnit](https://junit.org/junit5/) 、 [soapUI](https://www.soapui.org/) 、 [Watir](http://watir.com/) 等。

### 2.非功能测试

非功能测试是对应用程序的非功能方面的测试，比如性能、可靠性、可用性、安全性等等。非功能性测试在功能性测试之后进行。

通过非功能测试，你可以在很大程度上提高你的软件质量。功能测试也提高了质量，但是通过非功能测试，你有机会让你的软件变得更好。非功能测试允许你润色软件。这种测试不是关于软件是否工作。相反，它是关于软件运行得有多好，以及其他许多事情。

非功能性测试通常不会手动运行。事实上，手工执行这种测试是很困难的。所以这些测试通常使用工具来执行。

有几种类型的非功能性测试，例如:

*   性能试验
*   安全测试
*   负载测试
*   故障转移测试
*   兼容性测试
*   可用性测试
*   可扩展性测试
*   容量测试
*   压力测试
*   可维护性测试
*   符合性测试
*   效率测试
*   可靠性测试
*   耐久性测试
*   灾难恢复测试
*   本地化测试
*   国际化测试

注意，解释所有类型的软件测试超出了本文的范围。

## 不同类型的软件测试

本文只解释了一些最常见的软件测试类型。

### 1.单元测试

测试软件项目的每个组件或模块被称为单元测试。要执行这种测试，编程知识是必要的。所以只有程序员做这种测试，而不是测试人员。

你必须做大量的单元测试，因为你应该测试项目中的每一个代码单元。

### 2.集成测试

集成模块后，您需要查看组合的模块是否能一起工作。这种类型的测试被称为集成测试。您需要执行的集成测试比单元测试少。

一些好的单元和集成测试工具有 [Jasmine](https://jasmine.github.io/) 、 [Mocha](https://mochajs.org/) 等。

### 3.端到端测试

端到端测试是对整个软件系统的功能测试。当您测试完整的软件系统时，这样的测试被称为端到端测试。与集成测试相比，您需要执行更少的端到端测试。

[黄瓜](https://cucumber.io/)、[量角器](https://www.protractortest.org/)、[茉莉](https://jasmine.github.io/)、[因缘](https://karma-runner.github.io/1.0/index.html)、 [SpecFlow、](https://specflow.org/community/talking-about-specflow/)等。是一些很棒的端到端测试工具。

### 4.用户界面测试

用户界面测试包括应用程序用户界面的测试。UI 测试的目的是检查用户界面是否是根据需求规格文档中描述的内容开发的。

通过运行 UI 测试，您可以使应用程序的用户界面更友好，更吸引人。

一些很棒的自动化用户界面测试工具有【Android 猴子测试、 [Saucelabs](https://saucelabs.com/) 和[量角器](http://www.protractortest.org/#/)。

### 5.可访问性测试

测试你的软件对残疾人是否可访问被称为可访问测试。对于这种类型的测试，您需要检查残疾人(如色盲、失明和失聪的人)是否可以使用您的应用程序。

需要选择正确的颜色和对比度，让色盲的人也能使用你的软件。

### 6.阿尔法测试

Alpha 测试是一种寻找整个软件中所有错误和问题的测试。这种测试是在应用程序开发的最后阶段进行的，在产品发布或交付给客户之前，由开发人员执行，以确保用户/客户获得无错误的软件应用程序。

Alpha 测试在 beta 测试之前运行，这意味着在执行 alpha 测试之后，您需要运行 beta 测试。

Alpha 测试不在真实环境中执行。相反，这种测试是通过创建一个类似真实环境的虚拟环境来完成的。

### 7.Beta 测试

如前所述，beta 测试发生在 alpha 测试之后。Beta 测试在产品发布前完成。它是由有限数量的实际客户或用户在真实用户环境中执行的，目的是确保软件完全没有错误并且运行顺畅。在从这些用户那里收集反馈和建设性的批评之后，进行一些修改来使软件变得更好。

因此，当软件处于测试阶段时，它被称为软件的测试版。测试完成后，软件将向公众发布。

### 8.临时测试

顾名思义，临时测试是一种以临时方式执行的测试，不使用任何测试用例、计划、文档或系统。与所有其他类型的测试不同，这种测试不是以系统的方式进行的。

虽然不使用测试用例很难发现错误，但是有一些技术问题很容易通过特别测试发现，但是通过使用测试用例的其他测试方法很难发现。

这种非正式类型的软件测试可以由参与项目的任何人来执行。

### 9.兼容性测试

兼容性测试包括软件与不同操作系统、网络浏览器、网络环境、硬件等的兼容性检查。它检查开发的软件应用程序在不同的配置下是否工作良好。

举几个例子，如果软件是 Windows 的 app，就要检查是否兼容不同版本的 Windows 操作系统。如果它是一个网络应用程序，测试该应用程序是否可以从广泛使用的网络浏览器的不同版本中轻松访问。而如果是安卓的 app，就要检查一下是否能很好的兼容所有常用版本的安卓操作系统。

### 10.向后兼容性测试

执行向后兼容性测试是为了测试应用程序的全新或更新版本是否与运行该软件的环境的先前版本(例如操作系统和 web 浏览器)兼容。有时，某些应用程序会进行专门更新，以符合更新、更现代的环境的标准和风格。在这种情况下，支持向后兼容性是必要的。

向后兼容性测试可以确保所有在特定环境中使用旧版本的人都可以使用您的软件。

### 11.浏览器兼容性测试

顾名思义，浏览器兼容性测试检查 web 应用程序的浏览器兼容性。更具体地说，测试 web 应用程序是否可以从所有版本的主要 web 浏览器轻松访问。

它是兼容性测试的一种特定形式，而兼容性测试检查一般的兼容性。

一些流行的检查浏览器兼容性的工具有[CrossBrowserTesting.com](https://crossbrowsertesting.com/)，LamdaTest， [Browsershots](http://browsershots.org/) ， [Experitest](https://experitest.com/) ， [Turbo 浏览器沙箱](https://turbo.net/browsers)， [Ranorex Studio](https://www.ranorex.com/cross-browser-testing-tools/) ， [Browsera](http://www.browsera.com/) 等。

### 12.性能试验

运行性能测试来检查软件的性能是否良好。有一些性能测试工具可以分析你的应用程序的性能，并向你展示性能问题。通过修复这些问题，您将能够提高软件应用程序的性能。

web 应用程序的一些优秀的性能测试工具，也称为负载测试工具，有 [WebLOAD](https://www.radview.com/) 、 [LoadView](https://www.loadview-testing.com/) 、 [NeoLoad](https://www.neotys.com/) 、 [LoadNinja](https://loadninja.com/) 、[appadvance](https://www.appvance.ai/)、 [LoadRunner](https://www.microfocus.com/en-us/products/loadrunner-load-testing/overview) 、 [Apache JMeter](https://jmeter.apache.org/) 、 [Loadster](https://loadster.app/) 、 [LoadImpact](https://loadimpact.com/) 、[随处测试](https://testanywhere.co/)、[smart](https://www.smartmeter.io/)

### 13.负载测试

负载测试是一种性能测试，测试在软件性能开始下降之前系统可以承受多少负载。通过运行负载测试，我们可以了解系统的负载承受能力。

您可以使用类似于 [LoadRunner](https://www.microfocus.com/en-us/products/loadrunner-load-testing/overview) 、 [WebLoad](https://www.radview.com/) 、 [JMeter](https://jmeter.apache.org/) 等工具来运行负载测试。

### 14.恢复测试

恢复测试包括检查应用程序是否可以从崩溃中恢复，以及恢复得如何。在这种测试中，测试人员观察软件如何回到正常的执行流程。崩溃随时可能发生。即使你的软件质量非常好，崩溃也可能发生。你不知道它们什么时候会发生，并使用户烦恼。

因此，您必须实现能够快速恢复软件应用程序并使应用程序再次平稳运行的机制。

### 15.回归测试

如果您需要对任何组件、模块或功能进行更改，您必须查看在这些修改之后整个系统是否正常运行。在这样的修改之后对整个系统的测试被称为回归测试。

### 16.敏捷测试

由 QA 团队执行的敏捷测试是一种根据敏捷方法的规则进行的测试。这种测试是从实际客户的角度进行的。

你可以用来进行敏捷测试的一些有用的工具有 [JIRA](https://www.atlassian.com/software/jira) 、[practist](https://www.practitest.com/)、[junone](https://juno.one/)、 [VersionOne](https://www.versionone.com/versionone-vs-atlassian-jira-agile/) 、 [TestRail](https://www.gurock.com/testrail) 、 [SoapUI](https://www.soapui.org/) 等等。

### 17.API 测试

就像单元测试一样，API 测试也是代码级的测试类型。单元测试和 API 测试的基本区别在于单元测试是由开发团队执行的，而 API 测试是由 QA 团队处理的。

### 18.黑盒测试

由公司的 QA 团队执行的黑盒测试是一种测试技术，它涉及在没有任何应用程序技术知识的情况下检查应用程序的功能，如代码逻辑知识、代码如何工作、内部结构知识等。

### 19.白盒测试

由开发团队执行的白盒测试是一种需要很好地理解应用程序代码的测试方法。这需要对应用程序的内部逻辑有深入的了解。

### 20.安全测试

执行安全性测试是为了确保您的应用程序的安全性，以防止安全漏洞。安全专家运行这种测试，看看你的软件在多大程度上免受攻击，并找到安全问题，以便加强应用程序的安全性。

[顶级网站安全测试工具](https://hackr.io/blog/top-10-open-source-security-testing-tools-for-web-applications)包括 Grabber、 [Arachni](http://www.arachni-scanner.com/) 、[铁黄蜂](https://ironwasp.org/)、 [Nogotofail](https://security.googleblog.com/2014/11/introducing-nogotofaila-network-traffic.html) 、 [SQLMap](http://sqlmap.org/) 、 [W3af](http://w3af.org/) 、 [Wapiti](http://wapiti.sourceforge.net/) 、 [Wfuzz](http://www.edge-security.com/wfuzz.php) 、 [Zed 攻击代理](https://www.zaproxy.org/)等。

### 21.可用性测试

测试应用程序的用户友好性被称为可用性测试。它包括检查应用程序的可用性或用户友好性。测试的是有没有用户可以轻松使用你的软件而不卡顿。

测试软件可用性的最好方法之一是邀请一些人来使用你的软件。看看他们是否能在不需要你的任何帮助的情况下在你的应用中做某些事情。

看看这些有用的可用性测试工具:[优化](https://www.optimizely.com/)、 [Qualaroo](https://qualaroo.com/) 、[疯狂彩蛋](https://www.crazyegg.com/)、 [Usabilla](https://usabilla.com/) 、 [Clicktale](https://www.clicktale.com/default.aspx) 、[五秒测试](http://fivesecondtest.com/)、[粉笔记号](https://www.optimalworkshop.com/chalkmark)、 [UXtweak](https://www.uxtweak.com/) 。

### 22.可扩展性测试

可伸缩性测试验证软件是否是可伸缩的。换句话说，当用户数量、数据量或交易数量显著增加时，它会检查您的应用程序是否表现良好。不可扩展的软件应用程序可能会导致巨大的业务损失。

### 23.可靠性测试

可靠性测试是一种验证软件是否可靠的软件测试。换句话说，它检查软件运行是否没有错误，是否可以信赖。

例如，如果用户存储在软件数据库中的重要信息在几个月后因为代码中的一些错误而被突然删除，我们可以说该软件不可靠。

### 24.验收测试

将购买您的软件的客户将执行验收测试(也称为用户验收测试)，通过检查您的软件是否满足客户的所有要求和偏好来确定软件是否可以被接受。如果你的软件不符合所有的要求，或者如果你的客户不喜欢应用程序中的某些东西，他们可能会要求你在接受项目之前进行更改。

**遗言**

## 本文解释了几种类型的软件测试。请记住，您不需要为您的软件项目执行本文中提到的所有测试。你应该运行什么样的测试取决于你正在构建的软件类型和其他因素。

除了执行测试之外，测量测试的有效性也很重要，测试覆盖率告诉你测试的有效性。伊斯坦布尔是一个测量测试覆盖率的好工具，用于 JavaScript 软件项目。

即使在你的应用程序启动后，也可能存在未被发现的错误，这将会使用户烦恼，并给他们带来问题。实时错误检查工具如[哨兵](https://sentry.io/welcome/)和 [Newrelic](https://newrelic.com/) 会自动发现错误并通知你，所以你不需要告诉你的用户报告 bug。

您也可以使用自动化代码分级工具。像[sonar cube](https://www.sonarqube.org/)和 [codebeat](https://codebeat.co/) 这样的自动化代码分级工具通过显示应用程序中的问题，帮助你惊人地提高代码质量。这些工具将帮助你在更短的时间内修复错误。在分析您的代码之后，这些工具会为您提供有用的报告，其中包含代码质量增强所需的有价值的信息。

您可以使用名为 linters 的程序来检查软件项目的代码是否符合指定的编码约定规则。linter 实际上为您节省了大量时间，因为手动检查几个开发人员编写的代码是一个非常耗时的过程。

您可以找到几乎任何编程语言的 linters。看看这些流行的 linter:[TypeScript ts lint，](https://www.npmjs.com/package/tslint) [JavaScript ESLint](http://eslint.org/) ， [Sass/SCSS sass-lint](http://sass-lang.com/) ，[Python pylint](https://www.pylint.org/)/[flake 8](http://flake8.pycqa.org/en/latest/)， [Bash ShellCheck](https://www.shellcheck.net/) ， [Go golang lint](https://github.com/golang/lint) 等。代码编辑器(如 Visual Studio 代码)允许您配置林挺。

**人也在读:**

**People are also reading:**