# 下载 React 原生备忘单 PDF 以供快速参考

> 原文：<https://hackr.io/blog/react-native-cheat-sheet>

React Native 是一个支持开发基于移动设备的应用程序的框架。它有很多特性和种类来帮助你创建用户界面。与主要面向网络浏览器的 React 不同，React Native 主要专注于移动应用。

该软件的*一次编写，随处运行*使其比同类软件更受欢迎。这意味着你可以编写代码，然后重用它在其他平台上创建应用程序。

随着 React Native 的广泛流行，许多组织都在采用它来最大化和提升 IoS 和 Android 应用程序的用户体验。如今，学习这种技能对于赚钱的职业来说是一项很好的技能。

准备 React 本地面试还是练习移动开发？使用这个方便的 React 本机备忘单作为快速参考！

我们将讨论风格、组件、布局和命令行。在我们的 React Native 风格备忘单结束时，您将可以轻松地执行任何 React Native 任务。丰厚的奖金？您可以下载我们的 React 原生备忘单 PDF，并在需要时随时离线访问。

**点击下载 React 原生备忘单 PDF [。](https://drive.google.com/file/d/1V0WFIveNraZkvqpax4BmOh3AMum6E1jM/view?usp=sharing)**

## **React 原生备忘单**

在我们进入备忘单的本质之前，让我们快速回顾一下使用 React Native 的先决条件。

### **先决条件**

以下是在您的系统上使用 React Native 所需的内容:

1.  安装 **Visual Studio 代码**(或者你选择的代码编辑器)。
2.  安装**安卓工作室**。默认情况下，Android Studio 将可能是最新的 Android SDK。React Native 需要 Android 6.0(棉花糖)SDK 或更高版本。我们建议您使用最新的 SDK。
3.  为 **Java SDK** 和 **Android SDK** 环境变量创建路由:

a.在 Windows 搜索菜单中输入“编辑系统环境变量”以启动系统属性窗口。

b.在用户变量下，选择环境变量...然后新的…

c.填写变量路径的名称和值。以下是 Java 和 Android SDKs 的默认目录。

ANDROID HOME:C:UsersusernameAppDataLocalAndroidSdk JAVA HOME:C:Program files androidandroid Studiojrebin ANDROID HOME:C:UsersusernameAppDataLocalAndroidSdk

通过这些课程学习 React Native！
[![](img/385a271194b246b326175b1c6e161970.png)](https://click.linksynergy.com/deeplink?id=Qouy7GhEEFU&mid=39197&murl=https://www.udemy.com/topic/react-native/)

## **React 原生命令行**

希望学习不同的命令来创建项目，运行 Android 或 iOS 应用程序，链接库，以及升级 React 本机和 NPM 软件包？

你可以用所有这些反应原生命令。让我们开始吧。

#### **创建项目**

若要开始一个新项目，请打开“终端”应用程序并键入以下命令:

```
react-native init AppName;

cd AppName;
```

#### **在 iOS 模拟器中运行 App**

在终端中使用以下命令在 iOS 模拟器上运行您的程序:

```
react-native run-ios;
```

#### **在 Android 模拟器中运行应用**

使用这些命令在 Android 模拟器上运行您的程序:

```
cd AppName;

react-native run-android;
```

#### **指定模拟器设备**

此命令将帮助您在 iPhone 7 Plus 上启动模拟器:

```
react-native run-ios --simulator "iPhone 7 Plus"
```

要列出可用设备，请执行:

```
xcrun simctl list devices
```

#### **链接依赖关系**

有时，您需要连接第三方库依赖项。假设您安装了 react-native-vector-icons 库。要将图标字体添加到项目中，您需要执行以下操作:

```
react-native link
```

#### **链接库**

如果你在 IOS 上使用链接或推送通知这样的库，你必须包含标题搜索路径。也可以参考 React 原生文档。

下面是如何添加 React Native 附带的库的路径:

1.  在 iOS 文件夹中，打开 **AppName.xcodeproj.**
2.  点击左侧面板中的 **AppName** 。
3.  在**目标**部分，点击 **AppName** 。
4.  点击**构建设置。**
5.  在搜索路径部分中，查找**标题搜索路径**行。
6.  查找术语“标题”在搜索中的路径行的 AppName 列中双击一条**路线**。
7.  点击弹出窗口左下角的+按钮。
8.  粘贴 *$(SRCROOT)/../node _ modules/react-native/Libraries*拖动到第一列，并从第二列的下拉菜单中选择 recursive。

#### **升级 React Native**

要将 React Native 更新到最新版本，请运行以下命令:

```
npm install --save react-native@latest;
```

要升级项目文件，请执行:

```
react-native upgrade;
```

#### **升级 NPM 包**

要列出所有过期的软件包，请执行:

```
npm outdated
```

要将软件包更新到最新版本，请执行:

```
npm install --save package-name@latest;
```

### **开发流程**

#### **启用热重装**

启用热重载会在您更改代码时更新模拟器中的应用程序。

要启用热重装，请在模拟器中运行您的应用程序。一旦启动，选择**启用热重装**。如果您使用的是 iOS 模拟器，请按下⌘d；如果您使用的是 Android 模拟器，请按下⌘M。

#### **启用远程调试**

当启用远程调试时，Chrome 中会出现一个新标签，指示如何启动开发人员工具。这将显示调试信息，如问题和警告。您还可以在应用程序代码中使用 console.log('Debug '，object)来输出自定义数据，如字符串、变量、对象、组件等。

要启用远程调试，您必须首先在模拟器中运行您的应用程序。一旦启动，如果你使用的是 iOS 模拟器，按下⌘D，或者如果你使用的是 Android 模拟器，按下⌘M，选择远程调试 JS。

### [![](img/220bebb5e58c7258fdcac387f350d4ba.png)](https://click.linksynergy.com/deeplink?id=Qouy7GhEEFU&mid=39197&murl=https://www.udemy.com/course/the-complete-react-native-and-redux-course/)

### **代码片段**

让我们用这些代码片段来探索 React 本机布局命令。

#### **检测屏幕尺寸**

你可能需要知道你的应用程序运行的设备的屏幕大小，以便改变你的应用程序的布局、文本大小和其他方面。

*我*

```
mport { Dimensions } from 'react-native';

const { width, height } = Dimensions.get('window');

alert(Screen size: ${width}x${height});
```

以下是各种屏幕尺寸供您参考:

*   iPhone 5: 320 x 568
*   **iPhone 6:** 375 x 667
*   **iPhone 6 Plus:** 414 x 736

#### **转换文本**

使用字符串变量的 toUpperCase()函数将文本转换为大写:

```
<Text>{this.props.title.toUpperCase()}</Text>
```

使用字符串变量的 toLowerCase()方法将文本转换为小写:

```
<Text>{this.props.title.toLowerCase()}</Text>
```

#### **限制文本组件的行数**

numberOfLines 属性帮助您限制文本组件显示的行数，并剪切不适合的文本:

```
<Text numberOfLines={2}>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam tincidunt eu neque non varius. Phasellus id arcu in enim sodales sodales. Vestibulum maximus hendrerit feugiat. Maecenas nec risus metus. Nam ullamcorper et mauris sit amet placerat. Cras elementum nunc a lorem auctor accumsan. Nam dapibus tristique tempor. Aenean nec augue viverra, tincidunt magna ac, varius leo. Nunc condimentum tristique placerat. Donec ullamcorper nibh vel lacinia pharetra. Praesent a scelerisque tellus. Fusce aliquet porta scelerisque. Suspendisse convallis urna eu arcu finibus ullamcorper. Etiam commodo faucibus ligula, ac consectetur mauris gravida id. Quisque lacus tortor, pellentesque sed eleifend nec, pellentesque vitae diam.

</Text>
```

### **组件**

现在，我们将介绍如何使用各种 React 本机组件来开发应用程序:

#### **组件样板文件**

```
You can use this boilerplate to create new components:

import React, { Component } from 'react';

import {

StyleSheet,

Text,

View

} from 'react-native';

export default class Component extends Component {

render() {

return (

<View style={styles.container}>

<Text>Component</Text>

</View>

);

}

}

const styles = StyleSheet.create({

container: {

flex: 1,

},

});
```

#### **默认属性值**

使用 defaultProps 属性设置组件的默认属性值。

通过为组件 JSX 表达式提供自定义值，您可以随时覆盖默认值。

例如，如果您使用

，标题值将从默认更改为我的标题:

```
import React, { Component } from 'react';

import {

StyleSheet,

Text,

View

} from 'react-native';

export default class Header extends Component {

static defaultProps = {

title: 'Default Header'

}

render() {

return (

<View >

<Text style={styles.header}>

{this.props.title.toUpperCase()}

</Text>

</View>

);

}

}

const styles = StyleSheet.create({

header: {

fontFamily: 'Avenir',

fontSize: 40,

fontWeight: 'bold',

textAlign: 'center',

},

});
```

#### **传播属性**

您可以使用 spread 运算符在 JSX 将道具作为对象发送:

```
render() {

const props = {

title: 'My Title',

size: 20,

};

return <Header {...props} />;

}

This code is essentially the same as follows:

render() {

return <Header title="My Title" size={20} />;

} 
```

#### **从对象中提取属性**

您可以使用 const { prop1，prop1，...rest } =对象符号:

```
render() {

const { title, size, ...rest } = this.props;

return (

<View>

<Text style={[styles.header, { fontSize: size }]} {...rest}>

{title.toUpperCase()}

</Text>

</View>

);

}
```

#### **使用 ES7 装饰器**

要使用 ES7 decorators，你应该先安装 babel-plugin-transform-decorators-legacy:

*npm 安装-保存-开发巴别塔-插件-转换-装饰者-遗留*

然后，编辑。包含 transform-decorator-legacy 插件的 babelrc 文件:

```
{

"presets": [

"react-native"

],

"plugins": [

"transform-decorators-legacy"

]

}
```

在下面的例子中，我们可以使用 react-redux 包中的@connect 装饰器:

```
import { connect } from 'react-redux';

import { bindActionCreators } from 'redux';

@connect(

(state) => {

const { user, data } = state;

return {

user,

data

};},

(dispatch) => ({

actions: { ...bindActionCreators({ actionA, actionB }, dispatch) }

})

)

export default class App extends Component {

render({ user } = this.props) {

return (

<View >

<Text style={styles.header}>

Hello {user.name}

</Text>

</View>

);

}

} 
```

### **React 原生样式表备忘单**

准备好设计你的组件了吗？继续读！

#### **对一个组件应用多种样式**

您可以使用数组将多个样式传递给一个组件:

```
<View style={[styles.generic, styles.specific, { color: 'blue' }]} />
```

### **直列造型**

顾名思义，将样式放在 HTML 元素中。假设我们想在我们的住所周围放置一个边框。颜色变量决定边框颜色:

```
function House() {

const [color, setColor] = useState("red");

return (

<div>

<h2 style={{"border":`1px solid ${color}`}}>This is a {color} house</h2>

</div>

);

}
```

或者，您可以创建一个样式对象，并在样式属性中传递它，如下所示:

```
function House() {

const [color, setColor] = useState("red");

//style obj contains the css

const style={

"border":`1px solid ${color}`

}

return (

<div>

<h2 style={style}>This is a {color} house</h2>

</div>

);

}
```

#### **做一个圆**

诀窍是使用你的圆的宽度/高度的一半作为边框半径:

```
<View style={{

width: 90,

height: 90,

borderRadius: 90 / 2,

backgroundColor: '#2196F3'

}}/>
```

#### **将图像放入柔性容器**

假设您有一个灵活的容器，并希望在其中放置一张居中的图片，以填充整个容器:

这是如何做到的:

```
<View style={{

backgroundColor: '#dddddd',

flex: 1,

}}>

<Image source={{ uri: 'https://placekitten.com/g/800/600' }} style={{

position: 'absolute',

top: 0,

left: 0,

bottom: 0,

right: 0,

}} />

</View>
```

### **柔性盒**

Flexbox 的主要目的是布局组件的子组件。现在，让我们更多地谈谈布局。

#### **主轴和副轴**

主轴总是与副轴相反。如果主轴是列，副轴将是行。反之亦然。

#### **调整内容**

子元素在主轴上的分布由组件样式的内容决定。您还有几种选择:

**1。弹性开始(默认)-在开始时分配子节点。**

```
container: {

flexDirection: 'row',

justifyContent: 'flex-start'

}
```

**2。居中—子对象居中。**

```
container: {

flexDirection: 'row',

justifyContent: 'center'

}
```

**3。柔性末端—末端分布的子节点。**

```
container: {

flexDirection: 'row',

justifyContent: 'flex-end'

},
```

**4。周围空间——孩子以相等的空间分布在周围。**

![](img/afa07a5f577b602304dc7ac4d7d80b38.png)

```
container: {

flexDirection: 'row',

justifyContent: 'space-around'

}
```

**5。间距-均匀分布的子代。**

![](img/ef4f8a969b7c25da8132df0f0a779424.png)

```
container: {

flexDirection: 'row',

justifyContent: 'space-between'

}
```

#### **对齐项目**

该命令设置子对象沿次轴的对齐方式。你可以这样做:

**1。flex-start-子节点在起点对齐。**

![](img/885d56f73a10765773e37c7f51d38f60.png)

```
container: {

flexDirection: 'row',

justifyContent: 'space-between',

alignItems: 'flex-start'

}
```

**2。居中-子对象居中对齐。**

![](img/18de0c75dd449e8a3ea50331608b6ca3.png)

```
container: {

flexDirection: 'row',

justifyContent: 'space-between',

alignItems: 'center'

}
```

**3。flex-end-末端对齐的子项。**

![](img/85c5112b92df4192d0260925af283009.png)

```
container: {

flexDirection: 'row',

justifyContent: 'space-between',

alignItems: 'flex-end'

}
```

**4。拉伸(默认)** —子元素被拉伸以填满所有空间。此选项不适用于沿辅助轴具有固定尺寸的子对象。

### **CSS 模块**

React 本机样式的另一个选项是创建一个. css 文件并将其导入到组件中。

我创建了一个基本的 styles.css 文件，样式如下:

```
h2 {

font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;

padding: 10px 5px;

border-radius: 10px;

}
```

然后，在我的房子组件文件中，导入文件，如下所示:

```
import React, { useState } from "react";

import ReactDOM from "react-dom";

import "./style.css"; //import here

//keep everything else the same

function House() {

const [color, setColor] = useState("red");

const style={

border: `1px solid ${color}`

};

return (

<div>

<h2 style={style}>This is a {color} house</h2>

</div>

);

}
```

### **反应道具**

您可以使用 props——在 React Native 中，props 相当于函数的参数，而 HTML 属性相当于 HTML。

想象一下，我们在一个房子里有很多门组件。我们如何区分一扇门和另一扇门？为什么不给每个门一个标题道具？

为此，只需向门组件添加一个标题，如下所示。

```
<Door title="front" />
```

有点类似于 [HTML](https://hackr.io/blog/how-to-create-a-website-using-html) 属性，对吧？然后在门组件中，我们可以打印出它的道具:

```
function Door(props) {

return (

<div>

<h3>This is the {props.title} door</h3> 

</div>

);

}
```

结果呢？我们的应用程序会像预期的那样打印出标题。

现在，我们可以在房子内部添加许多门组件，并有一个标题来区分它们。

```
function House() {

return (

<div>

<h2>This is a house</h2>

<Door title="front"/>

<Door title="back"/>

<Door title="kitchen"/>

<Door title="bedroom"/>

</div>

);

}
```

### **反应状态**

React 中的状态是存储变量的对象。您只能在其组件中访问这些变量，除非您使用一些状态管理工具，如 [Redux](https://hackr.io/tutorials/learn-redux) 。

让我们给我们的 House 类组件添加一些状态，使它更有趣:

```
class House extends React.Component {

constructor(props) {

super(props);

this.state = {

color: "white",

rooms: 4

};

}

render() {

return (

<div>

<h2>This is a {this.state.color} house with {this.state.rooms} rooms.</h2>

</div>

)

}

}
```

### **useEffect()**

useEffect 钩子是你将遇到的下一个最有用的钩子。当一个定义的状态改变时，这个钩子执行一个函数。

回到我们的 Home 组件，我们添加一个名为“door”的变量来监控房子的其他门。我们在它的使用状态钩子中将它设置为 0。

然后，我们添加一个按钮，单击该按钮时，门的值增加 1。最后，每次门的值被更新时，我们有一个 useEffect 钩子来打印家里的门的数量。

代码如下:

```
function House() {

const [color, setColor] = useState("white");

const [door, setDoor] = useState(0); //initialize door as 0

//add 1 to the current value of door on every button click

const addDoor = () => {

setDoor(door + 1);

};

 useEffect(() => {

console.log(`Door count: ${door}`)

}, [door]);

return (

<div>

<h2>This is a {color} house</h2>

<button onClick={addDoor}>Add a Door</button>

</div>

);

}
```

## **结论**

学习 React Native 是一项了不起的职业发展，但有效地使用它同样重要。从长远来看，React Native cheat sheet 将使您的项目流程更容易，并节省您的时间。

如果你有兴趣寻找其他的小抄，我们会帮你找到。

[访问 Golang 备忘单](https://hackr.io/blog/golang-cheat-sheet)

**人也在读:**