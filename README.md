# What-Is-React-Native
React-Native introduction in doodles/用涂鸦让你认识React-Native

## 在阅读之前
### 1. 起源
偶然间在知乎专栏读到一篇翻译的国外文章[图解React](https://zhuanlan.zhihu.com/p/39658720?utm_source=wechat_session&utm_medium=social&wechatShare=1#showWechatShareTip)文章，觉得写的/翻译的非常不错，生动形象；在原文链接中发现还有React-Native系列文章，自己对React-Native比较认可和感兴趣，便决定翻译一下这篇文章。希望能让更多的新手了解和上手React-Native。建议先阅读[图解React](https://zhuanlan.zhihu.com/p/39658720?utm_source=wechat_session&utm_medium=social&wechatShare=1#showWechatShareTip)。

### 2. 原文系列 in English
> [原博地址](https://learnreact.design/blog)


## 正文
系列博文： 涂鸦教你学习React
* [What is React(中文)](https://zhuanlan.zhihu.com/p/39658720?utm_source=wechat_session&utm_medium=social&wechatShare=1#showWechatShareTip)
* What is React Native(本文)
* Components,Props and State
* Props and State Re-explained
* React Native vs. Cordova, PhoneGap, Ionic etc.

***
在[上一篇文章中](https://zhuanlan.zhihu.com/p/39658720?utm_source=wechat_session&utm_medium=social&wechatShare=1#showWechatShareTip)，我们了解到了什么是React和React的特别之处。这一次让我们来进一步学习React Native: 它是干嘛用的，它是什么来头，它与React有何不同之处，以及我们为何要重视它。


### 学习目标
在阅读这篇文章之后我希望你回到这里可以清晰明白的回答如下问题：
* React Native是什么鬼？为啥名字带有Native？
* 为什么React Native如此之叼？
* 我们可以用React/React Native来做点什么东西？
* ReactDom是什么来头？它能做什么？
* React Renderer有什么作用？
* React Sketch.app的工作原理？
* ReactVR的工作原理？
* ReactJS和React.js是什么？

### 不仅仅应用于Web
到目前为止，你应该已经对React有了如下的认识：
![React Feature](https://learnreact.design/static/1-react-summary-28be1df2fed9962a09c159ded7e14881-d47ca.png)

React是一个非常牛b的工具来帮助我们在Web程序中搭建用户界面。借助React，我们可以直接通过描述我们想要的样式来更新UI，而不是手动更新UI（reactive UI），创建可以复用的组件和高性能的UI，而不用担心DOM操作缓慢的问题（virtual DOM）。越来越多的Web开发者开始投入到React的怀抱，因为他们可以专注于整体的设计而不用纠结于各种小细节的操作。We call this way of building the UI React paradigm. A paradigm is basically the way how you think about a problem and how you describe it and its solution2。我们称这种方式为React UI 构建范式，一个你如何去思考、描述以及解决问题的范式。

这对Web应用程序来说非常棒。那像其他的平台呢，例如iOS和Android？如果我们可以直接使用React 范式来开发移动应用那岂不是碉堡了吗？

在某种程度上，移动平台和Web平台的工作方式是有些类似的。都有一个模型(树人)和有一个可以根据模型来生成可见元素的角色(画家)。毫无疑问的是，构建移动端UI比较传统的方式是直接操纵树模型去渲染和更新(直接和树人进行对话)。这和在Web浏览器中直接操作DOM有类似的缺点。React在这方面可以大展拳脚。

抛开这些相同点，移动端平台与Web平台又是有很大区别的，并且移动平台之间也不尽相同。以前，开发者必须去学习特定的编程语言和工具链来去为特定的平台编写App。

这种感觉就像是和一个异国的工作室里的员工进行沟通，并且他们还说不同的语言。你必须去学习他们的语言以便和他们进行沟通。这听起来并不是一件很轻松的事情。

![exotic studios](https://learnreact.design/static/2-ios-android-9937949ca76a9fd81237721a60e48023-fb8a0.png)

因此，如果你想同时为iOS和Android开发一款App，你就必须去学习两种完全不同的代码。同一个业务逻辑不得不去实现两次。用这样的方式去开发一款App不仅很苦难、而且成本很高，更不用说以后的维护工作了。

这就是React Native诞生的原因。接下来让我们看看它是如果让这一切变得简单起来的。

### React Native

#### Renderers And The New React



