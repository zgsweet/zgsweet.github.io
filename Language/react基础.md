1、react.JS是facebook推出的前端页面UI库，类似MVC中的view,简单说就是将页面分成一个个小块，每一个小块都是一个组件，组件之间可以组合、嵌套，就成了页面。<br/>
2、JSX 原理:每个DOM元素都可以用javascript对象结构来表示，一个 DOM 元素包含的信息其实只有三个：标签名，属性，子元素。HTML 的信息和 JavaScript 所包含的结构和信息其实是一样的，我们可以用 JavaScript 对象来描述所有能用 HTML 表示的 UI 信息。但是用 JavaScript 写起来太长了，结构看起来又不清晰，用 HTML 的方式写起来就方便很多了，于是 React.js 就把 JavaScript 的语法扩展了一下，让 JavaScript 语言能够支持这种直接在 JavaScript 代码里面编写类似 HTML 标签结构的语法，这样写起来就方便很多了。编译的过程会把类似 HTML 的 JSX 结构转换成 JavaScript 的对象结构。所谓的 JSX 其实就是 JavaScript 对象，ReactDOM.render 功能就是把组件渲染并且构造 DOM 树，然后插入到页面上某个特定的元素上。<br/>
3、 JSX 到页面到底经过了什么样的过程：<br/>
  jsx--babel编译+react.js构造-->javascript对象结构---ReactDOM.render--->Dom元素-->插入页面。<br/>为什么不直接从 JSX 直接渲染构造 DOM 结构，而是要经过中间这么一层呢？<br/>第一个原因是，当我们拿到一个表示 UI 的结构和信息的对象以后，不一定会把元素渲染到浏览器的普通页面上，我们有可能把这个结构渲染到 canvas 上，或者是手机 App 上。所以这也是为什么会要把 react-dom 单独抽离出来的原因，可以想象有一个叫 react-canvas 可以帮我们把 UI 渲染到 canvas 上，或者是有一个叫 react-app 可以帮我们把它转换成原生的 App（实际上这玩意叫 ReactNative）。<br/>

第二个原因是，有了这样一个对象。当数据变化，需要更新组件的时候，就可以用比较快的算法操作这个 JavaScript 对象，而不用直接操作页面上的 DOM，这样可以尽量少的减少浏览器重排，极大地优化性能。这个在以后的章节中我们会提到。<br/>
4、jsx总结：<br/>
JSX 是 JavaScript 语言的一种语法扩展，长得像 HTML，但并不是 HTML。<br/>
React.js 可以用 JSX 来描述你的组件长什么样的。<br/>
JSX 在编译的时候会变成相应的 JavaScript 对象描述。<br/>
react-dom 负责把这个用来描述 UI 信息的 JavaScript 对象变成 DOM 元素，并且渲染到页面上。<br/>
5、没有经过特殊处理的话，这些 on* 的事件监听只能用在普通的 HTML 的标签上，而不能用在组件标签上。也就是说，<Header onClick={…} /> 这样的写法不会有什么效果的。这一点要注意，但是有办法可以做到这样的绑定，以后我们会提及。现在只要记住一点就可以了：这些 on* 的事件监听只能用在普通的 HTML 的标签上，而不能用在组件标签上。<br/>
5、传入的并不意味着由 props 决定的显示形态不能被修改。组件的使用者可以主动地通过重新渲染的方式把新的 props 传入组件当中，这样这个组件中由 props 决定的显示形态也会得到相应的改变。
6、props总结：<br/>
为了使得组件的可定制性更强，在使用组件的时候，可以在标签上加属性来传入配置参数。<br/>
组件可以在内部通过 this.props 获取到配置参数，组件可以根据 props 的不同来确定自己的显示形态，达到可配置的效果。<br/>
可以通过给组件添加类属性 defaultProps 来配置默认参数。<br/>
props 一旦传入，你就不可以在组件内部对它进行修改。但是你可以通过父组件主动重新渲染的方式来传入新的 props，从而达到更新的效果。<br/>
7、state vs props总结：<br/>
state 的主要作用是用于组件保存、控制、修改自己的可变状态。state 在组件内部初始化，可以被组件自身修改，而外部不能访问也不能修改。你可以认为 state 是一个局部的、只能被组件自身控制的数据源。state 中状态可以通过 this.setState 方法进行更新，setState 会导致组件的重新渲染。<br/>

props 的主要作用是让使用该组件的父组件可以传入参数来配置该组件。它是外部传进来的配置参数，组件内部无法控制也无法修改。除非外部组件主动传入新的 props，否则组件的 props 永远保持不变。<br/>

state 和 props 有着千丝万缕的关系。它们都可以决定组件的行为和显示形态。一个组件的 state 中的数据可以通过 props 传给子组件，一个组件可以使用外部传入的 props 来初始化自己的 state。但是它们的职责其实非常明晰分明：state 是让组件控制自己的状态，props 是让外部对组件自己进行配置。<br/>

如果你觉得还是搞不清 state 和 props 的使用场景，那么请记住一个简单的规则：尽量少地用 state，尽量多地用 props。<br/>

没有 state 的组件叫无状态组件（stateless component），设置了 state 的叫做有状态组件（stateful component）。因为状态会带来管理的复杂性，我们尽量多地写无状态组件，尽量少地写有状态的组件。这样会降低代码维护的难度，也会在一定程度上增强组件的可复用性。前端应用状态管理是一个复杂的问题<br/>

React 16 中关于服务端渲染的新特性

快速介绍React 16 服务端渲染的新特性，包括数组、性能、流等

React 16 终于来了！������

React 16 中有许多令人激动的新特性（最著名的是Fiber的重写），但是对我个人而言，最兴奋的还是React 16 对服务器端渲染所做的许多改进。

让我们深入了解一下在React 16 中使用新的、不同的SSR，我希望你能像我一样兴奋！

如何在React 15 中运行SSR

首先，让我们复习一下如何在React 15 中使用SSR。为了实现SSR，通常需要运行一个基于Node的web服务器，例如Express、Hapi或Koa，可以调用renderToString方法将根组件渲染为字符串，然后写入响应：
// using Express
import { **renderToString** } from "react-dom/server"
import MyPage from "./MyPage"

app.get("/", (req, res) => {
  res.write("<!DOCTYPE html><html><head><title>My Page</title></head><body>");
  res.write("<div id='content'>");  
  **res.write(renderToString(<MyPage/>));**
  res.write("</div></body></html>");
  res.end();
});


然后，在客户端启动代码中，通知客户端使用render()渲染在服务端生成的HTML，这与客户端渲染应用程序的方法一致：
import { render } from "react-dom"
import MyPage from "./MyPage"

render(<MyPage/>, document.getElementById("content"));


如果你的做法正确，客户端渲染器可以使用现有的服务器生成的HTML进行渲染，不需要更新DOM。

那么，在React 16 中，如何实现SSR呢？

React 16 向后兼容

React小组深刻承诺向后兼容，所以如果你的代码在React 15 中运行没有任何问题，那么，在React 16 仍然可正常运行。上一小节中的示例代码在React 15 和 React 16 中都可以正常运行。

万一在你的应用程序中使用React 16 却发现问题，请提交issue！将有助于核心团队清除React 16 版本的缺陷。

render() 变成 hydrate()

如果你将SSR从React 15 升级到React 16，在浏览器中将会看见如下警告：



这是一个有益的React警告。render() 已变成 hydrate()。

在React 16中，有两种不同的方法实现客户端渲染：render()仅用于渲染客户端内容，hydrate用于渲染服务器端标记。由于React是向下兼容的，在React 16中使用render()渲染服务端生成的标记仍旧有效，但是需要使用hydrate()方法来消除警告，为React 17做好准备。前文的代码片段应改写为：
import { **hydrate** } from "react-dom"
import MyPage from "./MyPage"

**hydrate**(<MyPage/>, document.getElementById("content"));


React 16 可以处理数组、字符串和数字

在React 15中，组件的render方法必须返回一个简单的React元素。而在React 16中，客户端渲染的render方法允许组件返回字符串、数字或一组元素组成的数组。显然，React 16服务端渲染方法hydrate方法也支持该特性。

因此，可以使用如下方式编写组件：
class MyArrayComponent extends React.Component {
  render() {
    return [
      <div key="1">first element</div>, 
      <div key="2">second element</div>
    ];
  }
}

class MyStringComponent extends React.Component {
  render() {
    return "hey there";
  }
}

class MyNumberComponent extends React.Component {
  render() {
    return 2;
  }
}


甚至可以在顶层renderToString方法中传入字符串、数字、组件数组：
res.write(renderToString([
      <div key="1">first element</div>, 
      <div key="2">second element</div>
    ]));

// it’s not entirely clear why you would do this, but it works!
res.write(renderToString("hey there"));
res.write(renderToString(2));


这种方式有助于消除用于包裹React组件的div或span，有助于减小HTML文件体积。

React 16 生成更有效的HTML

说到减小HTML文件体积，React 16也从根本上减小SSR在创建HTML上的开销。在React 15中，SSR文件中的每个HTML元素都有一个data-reactid属性，其值即是简单的递增的ID，text节点也含有react-text和ID。查看一下代码片段看效果：
renderToString(
  <div>
    This is some <span>server-generated</span> <span>HTML.</span>
  </div>
);


在React 15中，该片段生成的HTML如下（注释便于阅读）：
<div data-reactroot="" data-reactid="1" 
    data-react-checksum="122239856">
  <!-- react-text: 2 -->This is some <!-- /react-text -->
  <span data-reactid="3">server-generated</span>
  <!-- react-text: 4--> <!-- /react-text -->
  <span data-reactid="5">HTML.</span>
</div>


而在React 16中，所有的ID都从节点中移除了，HTML看起来简单很多：
<div data-reactroot="">
  This is some <span>server-generated</span> <span>HTML.</span>
</div>


不仅简洁便于阅读，而且显著地减小HTML文件体积。棒！

React 16 允许使用非标准DOM属性

在React 15中，DOM渲染严格限制HTML元素，并且移除非标准HTML属性。而在React 16中，客户端和服务端渲染均允许在HTML元素上使用非标准属性。了解更多该特性的内容，请查阅 Dan Abramov’s post on the React blog

React 16 SSR不支持的错误边界和Portal

React 16 客户端渲染有两个新特性是服务端不支持的：错误边界和Portal。了解更多内容请查询Dan Abramovd 的一篇文章 excellent post on the React blog，但是至少必须了解的是服务端不会捕获错误边界。关于Portal我目前没有查到相应的解释性的文章，但是Portal 的 API依赖DOM节点，因此无法在服务端使用。

React 16 执行不太严格的客户端检查

在React 15中，当重新渲染节点时，ReactDOM.render()方法执行与服务端生成的字符挨个比对。如果一旦有不匹配的，不论什么原因，React在开发模式下会发出警告，替换整个服务端的节点数。

在React 16中，客户端渲染使用差异算法检查服务端生成的节点的准确性。相比于React 15更宽松；例如，不要求服务端生成的节点属性与客户端顺序完全一致。当React 16的客户端渲染器检测到节点不匹配，仅仅是尝试修改不匹配的HTML子树，而不是修改整个HTML树。

通常，这种变化对用户不会有影响，调用**ReactDOM.render()/hydrate()**时React 16不会修改SSR生成的不匹配HTML。这一项性能优化意味着你需要额外确保修复在开发模式下的所有警告。

React 16 不需要通过编译获得最佳性能

在React 15中，如果直接使用SSR，即使在生产模式下性能也不是最优的。这是因为有大量的开发人员警告和提示，并且每个警告都类似于：
if (process.env.NODE_ENV !== "production") {
  // check some stuff and output great developer
  // warnings here.
}


不幸的是，process.env不是一个普通的JavaScript对象，从中取值非常消耗性能。因此即使NODE_ENV被设置为production，仅仅检测环境变量常常增加了大量的服务器渲染时间。

为了解决React 15中的这种问题，你需要编译SSR代码移除process.env，可以使用Webpack Environment Plugin或Babeltransform-inline-environment-variables 插件。从经验来看，许多开发同学未编译服务端代码，结果SSR性能明显下降。

在React 16中，该问题已解。在React 16中只会在开始时调用一次process.env.NODE_ENV，因此不需要编译SSR代码就可以获得最佳性能。

React 16更快

说到性能，使用React做服务端渲染的同学经常抱怨说即使使用最佳实践，大文件渲染依旧缓慢。

因此，我非常高兴地公布性能测试报告，不同Node版本上React 16性能均有大幅提升：



React 16服务端渲染比React 15快。

与React 15相比，process.env编译后，在Node 4上大约提升2.4倍，Node 6中提升3倍，Node8.4 release版本提升3.8倍。对比未编译的情况，React 16大幅提升性能。

为什么React 16服务端渲染比React 15快这么多？在React 15中，服务端和客户端渲染基本是相同的代码。意味着数据结构需要维持一个虚拟DOM，尽管调用renderToString后vDOM很快被废弃。也就是说服务端渲染非常浪费。

在React 16，核心团队重新编写服务端渲染引擎，不会创建vDOM，因此会快很多。

警告：我的测试是通过生成巨大的DOM树，使用一个非常简单的递归响应组件。这意味着它是一个非常综合的基准，几乎肯定不能反映真实的使用情况。如果你的组件中有一大堆复杂的“渲染”方法占用了大量的CPU周期，那么React 16可能没那么快。所以，我绝对希望看到React 16 SSR得到明显改善，真实的应用可能改进不到3倍。据传，我听过一些早期采用者的看法关于 1.3x 性能提升。在你的应用程序中测试实验并找出最好的方法！

React 16 支持流

最后但并非最不重要的是，React 16现在支持直接渲染节点流。

渲染流可以减小第一个字节(TTFB)渲染时间，在文档的下一个部分生成之前，将文档的开头向下发送到浏览器。所有主流浏览器都会在服务器以这种方式流出内容时开始解析和呈现文档。

从呈现流中获得的另一个很棒的东西是响应backpressure的能力。这意味着，在实践中如果网络支持，不能接受更多的字节，渲染得到的信号与停顿渲染到堵塞清理。这意味着服务器使用更少的内存，对I/O条件更敏感，这两种情况都可以帮助服务器在充满挑战的条件下保持正常工作。

使用React 16渲染流，需要调用两个方法：renderToNodeStream 或 renderToStaticNodeStream，与renderToString 和 renderToStaticMarkup相对应。新方法返回Readable。

当收到renderTo(Static)NodeStream方法返回Readable流，它处于暂停模式，并且还没有渲染。当调用read或pipeWritable时开始渲染，大部分Node web框架从Writable继承响应对象，因此，一般来说，只要将Readable发送到响应。

举个例子，从上面的例子可以用流式重写：
// using Express
import { **renderToNodeStream** } from "react-dom/server"
import MyPage from "./MyPage"

app.get("/", (req, res) => {
  res.write("<!DOCTYPE html><html><head><title>My Page</title></head><body>");
  res.write("<div id='content'>"); **const stream = renderToNodeStream(<MyPage/>);
  stream.pipe(res, { end: false });
  stream.on('end', () => {**
    res.write("</div></body></html>");
    res.end();
  **});**
});


注意，当我们管的响应对象，我们必须包括可选参数{ end: false }告诉流不自动结束响应当渲染完成。这允许我们完成HTML主体，并在流完全写入响应后结束响应。

流有一些陷阱

虽然在大多数场景中，对流的渲染应该是一种升级，但目前有一些流媒体模式不能很好地工作。

一般来说，任何使用服务器呈现模式的模式都会产生标记，需要将这些标记添加到文档中，然后才可以与流媒体基本上不兼容。其中一些示例是动态决定在前面添加到页面中的CSS的框架向文档添加元素的标记或框架。如果你使用这些类型的框架，可能不得不使用字符串渲染。

另一种尚未在React 16中发挥作用的模式是嵌入调用renderToNodeStream。在React 15是相当典型的使用rendertostaticmarkup生成的页面模板和嵌入调用rendertostring产生动态的内容，如：
res.write("<!DOCTYPE html>");
res.write(renderToStaticMarkup(
  <html>
    <head>
      <title>My Page</title>
    </head>
    <body>
      <div id="content">
        { renderToString(<MyPage/>) }
      </div>
    </body>
  </html>);


但是，如果用流式对等体替换这些呈现调用，该代码将停止工作，因为它是不可能的一Readable流（rendertonodestream返回的）是嵌入在一个组件的元件。我希望在后续会增加！

