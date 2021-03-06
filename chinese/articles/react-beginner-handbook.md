> * 原文地址：[React for Beginners – A React.js Handbook for Front End Developers React.js 入门教程](https://www.freecodecamp.org/news/react-beginner-handbook/#howmuchjavascriptyouneedtoknowtousereact)
> * 原文作者：Flavio Copes
> * 译者：xinlei_ye@163.com
> * 校对者：

![React for Beginners – A React.js Handbook for Front End Developers](https://www.freecodecamp.org/news/content/images/size/w2000/2020/11/book-2.jpg)

React 是目前为止最受欢迎的 JavaScript 框架之一，而且我相信它也是目前最好用的开发工具之一。

这篇文章的目的在于为 React 初学者提供一些学习指导。

在学习完这篇文章后，你就可以对 React 有初步的了解：

-   什么是 React，它为什么这么受欢迎
-   如何安装 React
-   React 组件
-   React State
-   React Props
-   在 React 中处理用户事件
-   React 组件的生命周期事件

以上这些内容是你构建高级 React 应用的基础。

这篇文章是专门为刚接触 React 的 JavaScript 程序员写的。现在就让我们开始学习吧。

## 什么是 React？

React 是一个 JavaScript 库，旨在简化 UI 的开发。

2013 年，Facebook 首次向全世界发布了 React，Facebook 和 Instagram 以它为基础开发了大量的 APP，其中的一些 APP 有着最广泛的使用。

React 最初是为了使开发者可以在任意时间点都能轻松的追踪 UI 及它的状态。它通过将 UI 划分为多个组件的集合来达到这个目的。

在学习 React 的时候，你可能遇到一些小困难，但是只要解决了它们，我保证这将会是你最美好的经历。React 可以使前端开发工作变的更加简单，而且它的生态里还有很多好用的库和工具。

React 自身有一套易于使用的 API，当你开始学习的时候，需要先明白以下 4 个基本概念：

-   组件
-   JSX
-   State
-   Props

我们将在这篇指导中学习以上几个基本概念，那些高级的概念我们会留给其它的教程，我也会在文章的末尾给出深入学习 React 的资料。

你可以[免费下载 PDF / ePub / Mobi 格式的本篇指导][1]

## 学习目录

-   [学习 React 需要知道多少 JavaScript][2]
-   [为什么要学习 React][3]
-   [如何安装 React][4]
-   [React 组件][5]
-   [JSX 简介][6]
-   [使用 JSX 实现 UI][7]
-   [JSX 与 HTML 的区别][8]
-   [在 JSX 中嵌入 JavaScript][9]
-   [React 中的状态管理][10]
-   [React 组件中的 Props][11]
-   [React 应用中的数据流][12]
-   [在 React 中处理用户事件][13]
-   [React 组件中的生命周期事件][14]
-   [参考资料][15]

## 学习 React 需要了解多少 JavaScript

在真正开始学习 React 之前，你需要对 JavaScript 的核心概念有很好的理解

你不需要成为 JavaScript 专家，但是我希望你对以下内容有很好的了解：

-   [变量][16]
-   [箭头函数][17]
-   [使用扩展运算符处理对象和数组][18]
-   [对象和数组的解构][19]
-   [模板字符串][20]
-   [回调函数][21]
-   [ES 模块化][22]

如果你对这些概念不熟悉，我为你提供了一些资料来学习这些概念。

## 为什么要学习 React?

我强烈建议每一位 Web 开发者都可以对 React 有基本的了解。

那是因为以下几个原因：

1. React 十分受欢迎。作为一名开发者，你很可能在将来参与 React 项目。它们可能是目前正在进行的项目，也可能是你的团队希望你使用 React 开发的一个全新的 APP。
2. 现在很多工具都是基于 React 开发的。比如 Next.js，Gatsby 等流行框架与工具，它们在后台都使用了 React。
3. 作为一名前端工程师，很可能会在面试时遇到关于 React 的问题。

这些都是很好的理由，但是我希望你学习 React 的一个主要原因是它真的非常优秀。

React 促成了包括代码复用、组件化开发在内的几种很好的开发实践。它高效、轻量，并且使开发者关注于应用中的数据流，这种开发思想适用于很多常见的场景。

## 如何安装 React

有几种不同的方式安装 React。

在开始时，我强烈建议一种方法，那就是使用官方推荐的工具：`create-react-app`。

`create-react-app` 是一个命令行工具，旨在让你快速了解 React。

你可以从使用 `npx` 开始，这是一种不需要安装就能下载和执行 Node.js 命令的便捷方法。

> 在这里查看我的 npx 指南：[https://flaviocopes.com/npx/][23]

从 5.2 版的 `npm` 开始，增加了 `npx` 命令。如果你现在还没安装 npm，那么点击这里 [https://nodejs.org][24] 安装吧（npm 是随 Node 安装的）。

如果你不能确定你的 npm 版本号，那么执行 `npm -v` 命令来检查你是否需要更新 npm。

> 注意：如果你不熟悉终端的使用方法，请访问 [https://flaviocopes.com/macos-terminal/][25]，查看我的 OSX 终端教程。这份教程适用于 Mac 和 Linux。

当你执行 `npx create-react-app <app-name>` 命令时，`npx` 首先会 _下载_ 最新版的 `create-react-app`，然后再运行它，运行结束后会把它从你的系统中删除。

这点很不错，因为你的系统上永远不会有旧的版本，并且每次运行的时候，你都会获得最新、最全的可用版本。

让我们开始吧：

```sh
npx create-react-app todolist
```

![cra-start](https://www.freecodecamp.org/news/content/images/2020/11/cra-start.png)

运行成功后你会看到：

![create-react-app-finished](https://www.freecodecamp.org/news/content/images/2020/11/create-react-app-finished.png)

`create-react-app` 会在你指定的文件夹下创建项目的目录结构（本示例中为 `todolist`），同时将它初始化为一个 [Git][26] 仓库。

它也会在 `package.json` 文件中添加几个命令：

![cra-packagejson](https://www.freecodecamp.org/news/content/images/2020/11/cra-packagejson.png)

所以你可以即刻进入到新创建的应用目录下，运行 `npm start` 命令来启动 app。

![cra-running](https://www.freecodecamp.org/news/content/images/2020/11/cra-running.png)

默认情况下，这个命令会在你本地的 3000 端口启动 app，并打开浏览器，为你展示欢迎界面：

![cra-browser](https://www.freecodecamp.org/news/content/images/2020/11/cra-browser.png)

现在你就可以开始开发这个应用程序了！

## React 组件

在上一节课程里，我们创建了我们的第一个 React 应用。

在这个应用中，包含了一系列执行各种操作的文件，大部分文件都与配置有关，但是有一个文件十分的不同：`App.js`。

`App.js` 是你遇到的 **第一个 React 组件**。

文件中的代码如下：

```js
import React from 'react'
import logo from './logo.svg'
import './App.css'

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  )
}

```

一个使用 React 或者其他的主流前端框架，如：Vue、Svelte，创建的应用，都是由很多的组件构成的。

不过，我们还是先分析这个组件吧。我把这个组件代码简化如下：

```js
import React from 'react'
import logo from './logo.svg'
import './App.css'
function App() {
  return /* something */
}

```

现在你可以看到几件事情：我们使用 _import_ 导入了一些东西，并且 _导出_ 了一个名为 `App` 的函数。

在这段示例代码中，我们导入了一个 JavaScript 库（`react` npm 包），一个 SVG 图片，和一个 CSS 文件。

> `create-react-app`  设置了一种方法，它允许我们导入图片和 CSS，然后在 JavaScript 中使用它们。但这不是我们现在需要关心的内容，我们现在关心的是 **组件** 的概念。

`App` 是一个官方示例中的函数, 返回了一些初看之下非常怪异的内容。

它看起来很像 **HTML**，但是内嵌了一些 JavaScript。

其实这就是 **JSX**，一种我们构建组件时使用的特殊语言。我们将会在下一节讨论 JSX。

除了可以返回 JSX，组件还具有一些其他特征。

一个组件可以有它自己的 **state（状态）**，这就是说它可以封装一些其他组件无法访问的属性，除非它把这些 **state** 暴露给应用中的其他组件。

一个组件也可以接收来自其他组件的数据，我们称这些数据为 **props**。

先不要着急，我们很快就会详细学习所有的这些概念（JSX，State 和 Props）了。

## JSX 简介

要想学习 React 就必须首先了解 JSX。

在上一节中，我们创建了第一个 React 组件，即 `App`，它定义在由 `create-react-app` 构建的默认应用程序中。

它的代码如下：

```js
import React from 'react'
import logo from './logo.svg'
import './App.css'
function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  )
}

```

当时我们忽略了 `return` 语句中的所有内容，但是在本节中我们将会讨论它们。

我们将包含在组件返回语句后的括号内的所有内容称为 JSX：

```jsx
<div className="App">
  <header className="App-header">
    <img src={logo} className="App-logo" alt="logo" />
    <p>
      Edit <code>src/App.js</code> and save to reload.
    </p>
    <a
      className="App-link"
      href="https://reactjs.org"
      target="_blank"
      rel="noopener noreferrer"
    >
      Learn React
    </a>
  </header>
</div>

```

这些内容 _看起来_ 很像 HTML，但是却又不是真正的 HTML。它们之间有一些不同点。

而且将这样的代码包含在 JavaScript 文件中有点奇怪：它们看起来一点都不像 JavaScript！

在后台，React 会处理 JSX，它们会被转换为浏览器可以识别的 JavaScript。

因此，虽然我们编写了 JSX，但是最终会有一个转换的步骤，使它可以被 JavaScript 解析器所识别。

React 这样做的一个主要原因就是：**使用 JSX 能更加轻松的开发 UI 界面**。

当然了，前提是你必须非常熟悉它。

在下一节中，我们将会学习 JSX 是怎么使 UI 开发变容易的。再然后我们将会讨论它与“标准 HTML”的区别，而这些差异是你必须知道的。

## 使用 JSX 构建 UI

就像上一节中介绍的那样，JSX 的一个主要作用就是借助它可以非常容易的编写 UI。

特别的，在 React 组件中，你可以导入其他 React 组件，然后将它们嵌入当前组件以展示它们。

通常情况下，一个文件就是一个 React 组件，这是我们可以非常容易的在其它组件中复用（通过导入的方式）它们的原因。

但是同一个文件中也可以定义其它的 React 组件，这些组件只会在当前文件中用到。这里并没有明确的规则来规定一个文件中是否需要定义多个组件，选择最适合你的那种方式即可。

当一个文件中的代码行数过多时，我通常会将代码进行拆分，放到单独的文件中。

为了方便学习，我们在 `App.js` 文件中再定义一个组件。

我们计划创建一个名为 `WelcomeMessage` 的组件：

```js
function WelcomeMessage() {
  return <p>Welcome!</p>
}

```
看到了吗？ 这个组件就是一个简单的函数，它返回了一行 JSX，表示一个 `p` 标签。

我们将这个函数添加到 `App.js` 文件中。

现在，我们将 `<WelcomeMessage />` 添加到 `App` 组件的 JSX 代码中，就可以在 UI 中展示这个组件：

```js
import React from 'react'
import logo from './logo.svg'
import './App.css'
function WelcomeMessage() {
  return <p>Welcome!</p>
}
function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <WelcomeMessage />
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  )
}

```

下面是运行结果，你应该可以在屏幕中看到“Welcome!”信息。

![new-component](https://www.freecodecamp.org/news/content/images/2020/11/new-component.png)

我们称 `WelcomeMessage` 为子组件，`App` 为父组件。

我们像使用 HTML 标签一样，添加 `<WelcomeMessage />` 组件。

这就是 React 组件和 JSX 优雅的地方：我们构建应用程序组件，并且像使用 HTML 标签一样使用它们。

关于 JSX 与 THML 的区别，我们将会在下一节中学习。

## JSX 与 HTML 的区别

JSX 看起来像 HTML，但事实并不是这样。

在这节课程里，我会介绍一些在使用 JSX 时，你必须要知道的东西。

如果你仔细阅读过 `App` 组件的 JSX 代码，会发现一个很明显的不同点：组件中有一个名为 `className` 的属性。

在 HTML 中，我们使用的是 `class` 属性。出于各种原因，它可能是使用最广泛的属性，而 CSS 就是其中一个原因。`class` 属性使我们可以轻松的设置 HTML 样式，并且在设计 UI 时，Tailwind 之类的 CSS 框架就是以这个属性为核心的。 

但是这里有个问题。我们在 JavaScript 文件中编写 UI 代码，而 `class` 是 JavaScript 语言的保留字，这就意味着我们不能使用它，它有特殊的作用（定义 JavaScript 类）。由于这个原因，React 的作者们不得不选择一个其它的名称。

这就是我们为什么用 `className` 替代了 `class`。

当你将一些现有的 HTML 代码改写为 JSX 时，需要牢记这点。

React 为了保证页面能正常显示，对这种情况进行了特殊处理，但是它会在开发者工具中给出警告：

![className](https://www.freecodecamp.org/news/content/images/2020/11/className.png)

这种情况非常普遍，并不是只有 HTML 会遇到这种困扰，

JSX 与 HTML 的另一个非常大的不同点是 HTML 是很 _宽松_。当出现语法错误、标签没有正确闭合或者匹配时，浏览器会尽可能的解析 HTML，而不是中断解析过程。

这是 Web 的一个核心特点，它非常宽松。

但是 JSX 并不宽松。如果你忘记将一个标签闭合，你将会得到一条错误信息：

![jsx-error](https://www.freecodecamp.org/news/content/images/2020/11/jsx-error.png)

> React 会给出非常友好的错误信息，使你可以准确的定位问题并解决问题。

第三个 JSX 与 HTML 的不同点在于：在 JSX 中，我们可以内嵌 JavaScript。

我们会在下一节讨论这点。

## 在 JSX 嵌入 JavaScript

React 的一大特点就是我们可以非常容易的在 JSX 中嵌入 JavaScript。

其他的前端框架，如 Angular 和 Vue，有自己的特殊方法来在模板中显示 JavaScript 值，或者执行类似循环的操作。

React 并没有添加类似的新特性。React 通过使用大括号的方式，容许我们在 JSX 中嵌入 JavaScript。

我们展示的第一个示例，来自于我们之前学习过的 `App` 组件。

我们可以使用下面的方法导入 `logo` 的 SVG 文件：

```js
import logo from './logo.svg'

```

然后在 JSX 中，我们将这个 SVG 文件赋值给 `img` 标签的 `src` 属性。

```js
<img src={logo} class="App-logo" alt="logo" />

```

我们再来展示一个示例。假设 `App` 组件有一个变量，名为 `message`：

```js
function App() {
  const message = 'Hello!'
  //...
}

```

我们可以通过在 JSX 的任意位置添加 `{message}`，来在 JSX 中显示这个变量的值。

我们可以在 `{ }` 中添加任何 Javscript 表达式，但是每对大括号中只能有 _一个_ 表达式，并且这个表达式必须是可正确求值的。

如下所示，这是一个在 JSX 中非常常见的表达式。我们编写了一个三元运算符，在其中定义了一个条件语句（`message === 'Hello!'`），当条件为真时，我们输出一个值（`The message was "Hello!"`）；条件为假时，输出另一个值（当前示例中为变量 `message` 的值）：

```js
{
  message === 'Hello!' ? 'The message was "Hello!"' : message
}

```

## 在 React 中管理 state

每一个 React 组件都可以有它自己的 **state**。

那么什么是 _state_ ？state 就是 **由组件管理的状态的集合**。

例如，对于表单来说，它的每一个独立的 input 元素都管理着它自己的 state：它的输入值。

一个按钮负责处理自己是否被点击；是否获得焦点。

一个链接负责管理鼠标是否悬停在它上面。

在 React 或者其他组件化的框架、库中，我们所有的应用都是以大量使用含有 state 的组件为基础构建的。

我们使用由 React 提供的高效管理工具 `useState` 来管理 state。从技术上来说，它是个 **钩子** （尽管事实就是这样，但是现在我们还不需要知道钩子的详细信息）。

你可以使用下面的方法来从 React 中导入 `useState`：

```js
import React, { useState } from 'react'

```

通过调用 `useState()`，我们将会得到一个 state，以及一个供我们调用，用来修改 state 值的函数。

`useState()` 可以传入一个参数，用来初始化 state。它会返回一个数组，这个数组包含一个 state 和一个修改 state 值的函数。

如下所示:

```js
const [count, setCount] = useState(0)

```

这一点非常重要。我们不能直接修改 state，只能通过调用修改函数来修改它，否则，React 组件无法及时将数据的变化反映在 UI 中。

调用修改函数是一种将组件 state 的变化告知 React 的方法。

这个语法是不是看起来有点奇怪？这是因为 `useState()` 返回的是数组，所以我们使用了数组解构的方法来获取每个数组成员，就像这样：`const [count, setCount] = useState(0)`

下面是一个示例：

```js
import { useState } from 'react'
const Counter = () => {
  const [count, setCount] = useState(0)
  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  )
}

```

我们也可以调用多次调用 `useState()`，来创建多个 state：

```js
const [count, setCount] = useState(0)
const [anotherCounter, setAnotherCounter] = useState(0)

```

## React 组件中的 Props

我们称传入组件的初始值为 props。

我们之前创建了一个 `WelcomeMessage` 组件：

```js
function WelcomeMessage() {
  return <p>Welcome!</p>
}

```

我们这样使用它：

```js
<WelcomeMessage />

```

这个组件没有任何初始值，所以它没有 props。

在 JSX 中，props 可以作为属性传给组件。

```js
<WelcomeMessage myprop={'somevalue'} />

```

在组件中，我们以函数参数的形式接收 props：

```js
function WelcomeMessage(props) {
  return <p>Welcome!</p>
}

```

通常情况下，我们用对象解构的形式来获取 props 的名称：

```js
function WelcomeMessage({ myprop }) {
  return <p>Welcome!</p>
}

```

现在我们获得了 props，并可以在组件中使用它了。如下所示，我们可以在 JSX 中输出它的值：

```js
function WelcomeMessage({ myprop }) {
  return <p>{myprop}</p>
}

```

这里的大括号有多种含义。对于函数参数来说，大括号是对象解构语法的一部分。我们也可以用它来定义函数代码块；而在 JSX 中，我们用它来输出 JavaScript 值。

将 props 传递给组件是一种在应用中传递值的好方法。

一个组件既可以有自己的状态（state），也可以通过 props 来接收数据。

当将函数作为 props 时，子组件就可以调用父组件中定义的函数。

有一种被称为 `children` 的特殊 props，它代表了包含在组件的开始标签和结束标签之间的所有内容，例如：

```html
<WelcomeMessage> Here is some message </WelcomeMessage>

```

这种情况下，在 `WelcomeMessage` 中，我们可以通过使用名为 `children` 的 props 来获取 `Here is some message`。

```js
function WelcomeMessage({ children }) {
  return <p>{children}</p>
}

```

## React 应用中的数据流

在一个 React 应用中，数据通常以 props 的方式从父组件流向子组件，就像我们在上一节看到的那样：

```js
<WelcomeMessage myprop={'somevalue'} />

```

如果给子组件传递一个函数，你就可以在子组件中修改父组件的 state：

```js
const [count, setCount] = useState(0)

```

如下所示，在 Counter 组件内部，我们取得了 `setCount`，然后在适当情况下，可以调用它来修改父组件中的 `count`：

```js
function Counter({ setCount }) {
  //...
  setCount(1)

```

其实还有很多更高级的方法来管理数据，比如 Context API 和 Redux 之类的库。但是这些方法会增加复杂性，而在大约 90% 的时间里，我们刚刚介绍的两种方法都是完美的解决方案。

## 在 React 中处理用户事件

React 提供了一种简单的方法来管理从 DOM 触发的事件，如点击事件、表单事件等。

这里我们以最容易理解单击事件为例来进行说明。

你可以在任意的 JSX 元素上使用 `onClick` 属性：

```js
<button
  onClick={(event) => {
    /* handle the event /
  }}
>
  Click here
</button>

```
_每当元素被点击的时候，传递给 `onClick` 属性的函数就会被触发。_

_你也可以在 JSX 的外部定义这些函数：_

_`const handleClickEvent = (event) => {
  /`_ `handle the event */
}` 

`function App() {
  return <button onClick={handleClickEvent}>Click here</button>
}` 

当点击 button 时，就会触发 `click` 事件，此时，React 就会调用 `click` 事件的处理函数。

React 支持非常多的事件类型，如：`onKeyUp`，`onFocus`，`onChange`，`onMouseDown`，`onSubmit` 等。

## React 组件的生命周期事件

到目前为止，我们已经学习了怎么使用 `useState` 钩子来管理 state。

在本节中，我想介绍另外一个钩子：`userEffect`。

`useEffect` 钩子允许组件访问它的生命周期事件。

当你调用这个钩子时，你需要传入一个函数。在组件第一次被渲染的时候，以及在随后的每次重新渲染 / 更新时，React 都会调用这个函数。

React 首先更新 DOM，然后调用任何传递给 `useEffect()` 的函数。

所有这些都不会阻塞 UI 的渲染，即使是同步函数。

这里是一个示例：

```js
const { useEffect, useState } = React
const CounterWithNameAndSideEffect = () => {
  const [count, setCount] = useState(0)
  useEffect(() => {
    console.log(You clicked ${count} times)
  })

```

因为在随后的每次重新渲染 / 更新时，传递给 useEffect() 的函数都会被执行，所以出于性能上的考虑，我们可以告诉 React 在某些时候不要执行这个函数。为了实现这个目的，我们可以为 useEffect() 传入第二个参数，这个参数是一个数组，它的成员是需要监视的 state 变量。只有在这些 state 发生变化的时候，React 才会执行这个函数。

```js
useEffect(() => {
  console.log(Hi ${name} you clicked ${count} times)
}, [name, count])

```

类似的，你可以传入一个空数组，这会使 React 只在组件挂载的时候才执行这个函数。

```js
useEffect(() => {
  console.log(Component mounted)
}, [])

```

这是一个非常有用的技巧。

useEffect() 非常适合添加日志，访问第三方 API 等。

## 接下来做什么？

熟练掌握在这篇文章中提到主题是朝着学习 React 目标迈出的重要一步。

在这里我想给出一些指导，防止你在有关 React 教程和课程的海洋中迷失方向。

接下来该学习什么呢？

了解有关 [虚拟 DOM][31]，[编写声明式代码][32]，[单向数据流][33]，[不变性][34]，[组合][35]的更多理论。

构建一些简单的 React 应用。例如：[一个简单的计数器][36] 或者 [与公共 API 交互][37]

学习如何使用 [条件渲染][38]，如何在 [JSX 中使用循环][39]，如何使用 [React 开发者工具][40]

通过 [plain CSS][41] 或者 [Styled Components][42] 学习如何在 React 应用中使用 CSS。

学习如何使用 [Context API][43]，useContext 与 [Redux][44] 来管理 state。

学习如何与 [forms][45] 交互。

学习如何使用 [React 路由][46]。

学习 [如何测试 React 应用][47]。

了解基于 React 构建的应用程序框架，如 [Gatsby][48] 或者 [Next.js][49]。

当然，最重要的是，请确保在构建应用的过程中实践你所学习的每一个知识点。

## 结语

非常感谢阅读这篇入门指导。

我希望这篇指导可以激发你去学习更多关于 React 知识的兴趣以及了解 React 能做的每一件事。

不要忘了你可以 [免费下载 PDF / ePub / Mobi 格式的本篇指导][50]

每天我都会在我的网站 [flaviocopes.com][51] 上发布编程教程，你可以在那里看到更多类似的精彩内容。

你也可以在 Twitter 上与我交流 [@flaviocopes][52]。

[1]: https://flaviocopes.com/page/react-handbook/
[2]: https://www.freecodecamp.org/news/react-beginner-handbook/#howmuchjavascriptyouneedtoknowtousereact
[3]: https://www.freecodecamp.org/news/react-beginner-handbook/#whyshouldyoulearnreact
[4]: https://www.freecodecamp.org/news/react-beginner-handbook/#howtoinstallreact
[5]: https://www.freecodecamp.org/news/react-beginner-handbook/#reactcomponents
[6]: https://www.freecodecamp.org/news/react-beginner-handbook/#introductiontojsx
[7]: https://www.freecodecamp.org/news/react-beginner-handbook/#usingjsxtocomposeaui
[8]: https://www.freecodecamp.org/news/react-beginner-handbook/#thedifferencebetweenjsxandhtml
[9]: https://www.freecodecamp.org/news/react-beginner-handbook/#embeddingjavascriptinjsx
[10]: https://www.freecodecamp.org/news/react-beginner-handbook/#managingstateinreact
[11]: https://www.freecodecamp.org/news/react-beginner-handbook/#componentpropsinreact
[12]: https://www.freecodecamp.org/news/react-beginner-handbook/#dataflowinareactapplication
[13]: https://www.freecodecamp.org/news/react-beginner-handbook/#handlingusereventsinreact
[14]: https://www.freecodecamp.org/news/react-beginner-handbook/#lifecycleeventsinareactcomponent
[15]: https://www.freecodecamp.org/news/react-beginner-handbook/#wheretogofromhere
[16]: https://flaviocopes.com/javascript-variables/
[17]: https://flaviocopes.com/javascript-arrow-functions/
[18]: https://flaviocopes.com/javascript-rest-spread/
[19]: https://flaviocopes.com/javascript-destructuring/
[20]: https://flaviocopes.com/javascript-template-literals/
[21]: https://flaviocopes.com/javascript-callbacks/
[22]: https://flaviocopes.com/es-modules/
[23]: https://flaviocopes.com/npx/
[24]: https://nodejs.org/
[25]: https://flaviocopes.com/macos-terminal/
[26]: https://flaviocopes.com/git/
[27]: https://reactjs.org%22/
[28]: https://reactjs.org%22/
[29]: https://reactjs.org%22/
[30]: https://reactjs.org%22/
[31]: https://flaviocopes.com/react-virtual-dom/
[32]: https://flaviocopes.com/react-declarative/
[33]: https://flaviocopes.com/react-unidirectional-data-flow/
[34]: https://flaviocopes.com/react-immutability/
[35]: https://flaviocopes.com/react-composition/
[36]: https://flaviocopes.com/react-example-counter/
[37]: https://flaviocopes.com/react-example-githubusers/
[38]: https://flaviocopes.com/react-conditional-rendering/
[39]: https://flaviocopes.com/react-how-to-loop/
[40]: https://flaviocopes.com/react-developer-tools/
[41]: https://flaviocopes.com/react-css/
[42]: https://flaviocopes.com/styled-components/
[43]: https://flaviocopes.com/react-context-api/
[44]: https://flaviocopes.com/redux/
[45]: https://flaviocopes.com/react-forms/
[46]: https://flaviocopes.com/react-router/
[47]: https://flaviocopes.com/react-testing-components/
[48]: https://flaviocopes.com/gatsby/
[49]: https://flaviocopes.com/nextjs/
[50]: https://flaviocopes.com/page/react-handbook/
[51]: https://flaviocopes.com/
[52]: https://twitter.com/flaviocopes
