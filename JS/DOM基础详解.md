## DOM 文档对象模型
### DOM的级别：
    1、DOM1级主要定义HTML和XML文档的底层结构，在DOM1中，DOM由两个模块组成：DOM Core（DOM核心）和DOM HTML,
    其中DOM Core规定了基于XML的文档结构标准，通过这个标准简化了对文档中任意部分的房屋和操作，DOM HTML则在
    DOM核心基础上加以扩展，添加了针对HTML的对象和方法，如javascript中的Document对象。<br/>
    2、DOM2级在原来的DOM的基础上又扩充了鼠标、用户界面事件、范围、遍历等细分模块，而且通过对象
    接口增加了对CSS的支持。在DOM2中引入了一下模块，在模块包含了众多新类型和新接口：<br/>
      》、DOM视图(DOM Views):定义了跟踪不同文档视图的接口<br/>
      》、DOM事件（DOM Events）:定义了事件和事件处理的接口<br/>
      》、DOM样式(DOM Style):定义了基于CSS为元素应用样式的接口<br/>
      》、DOM遍历和范围：定义了遍历和操作文档树的接口<br/>
    3、DOM3级进一步扩展了DOM，在DOM3中引入了以下模块：<br/>
      》、DOM加载和保持模块(DOM Load and Save)：引入了以统一方式加载和保存文档方法<br/>
      》、DOM验证模块(DOM Validation)：定义了验证文档的方法<br/>
      》、DOM核心的扩展(DOM Style)：支持XML1.0规范、涉及XML Infoset、XPath和XML Base

### DHTML (Dynamic HTML)指动态HTML 不是W3C标准，不是由万维网联盟(W3C)规定的标准，是一个营销术语，被网景公司
和微软公司用来描述4.X代浏览器应当支持的新技术。
## 文档的类型
通用标记语言（1969年 GML）-->标准通用标记语言(1985年 SGML)-->超文本标记语言(1993年 HTML)-->可扩展标记语言(1998年 XML)
1、超文本标记语言：HTML(Help Text Markup Language)W3C万维网联盟维护，用来显示数据，重点是如何显示数据；使用定义的标准标签，HTML标签作为根元素.<br>
2、可扩展标记语言：XML(Extensable Markup Language)，用来描述数据，重点是什么是数据，如何存放数据
备注：XHTML（早期 HTML与xml合并作用）
## 节点类型：
节点类型   字符常量     数值常量<br/>
元素节点  ELEMENT_NODE   1     （拥有子节点和文本，是唯一能拥有属性的节点类型）<br/>
属性节点  ATTRIBUTE_NODE 2 （元素中的属性，是附属于元素的，是包含他的元素节点的一部分，不属于文档树的一部分）<br/>
文本节点  TEXT_NODE      3 <br/>
注释节点  COMMENT_NODE   8  <br/>
文档节点  DOCUMENT_NODE  9   <br/>
文档类型节点  DOCUMENT_TYPE_NODE  10 <br/>
***
文档片段节点，DocumentFragment。
作为一个占位节点，并不具有特殊定义。类似于一个未定义的容器，通过:
var frag = document.createDocumentFragment();
创建这个容器，再往这个容器里添加要添加的element:
frag.appendChild("li");
然后利用这个容器frag，把里面装的元素添加到document文档流中：
***
```
判断这个位置是否为元素节点：
<body>
<div id="container">
<script>
var divNode = document.getElementById("container");
/* if(divNode.nodeType==Node.ELEMENT_NODE){alert("Node is an element.");}* /
if (divNode.nodeType == 1){
alert("Node is an element.");
}
</script>
</div>
</body>

IE浏览器没有内置node的对象，不能判断nodetype的值是否等于Node.ELEMENT_NODE，不能通过“字符常量”判断，但可以通过“数值常量”来判断。

通过数值常量来判断一个节点类型是所有的浏览器都兼容的。
```
## DOM Ready:
    > 浏览器通过渲染引擎将html解析为dom节点
    > 页面上所有html都转换为节点以后叫做dom树构建完毕，简称dom ready
    > 渲染引擎职责将请求的内容显示到浏览器屏幕上，默认情况下，可以显示html、xml、图片，通过插件扩展可以显示其他类型的文档
### 渲染引擎的渲染过程
    解析html、构建dom树(将标签转化为节点)
    构建渲染树（解析样式信息）(外部css文件、style标签)
    布局渲染树（布局dom节点）(确定每个节点在屏幕上的确切坐标)
    绘制渲染树（绘制dom节点）(遍历渲染树，使用UI后端层绘制每个节点)
    扩展阅读：http://kb.cnblogs.com/page/129756
### DOMReady实现策略
    在页面的DOM树创建完成后（也就是HTML解析地一步完成）即出发，而无需等待其他资源的加载，即DOMReady实现策略
    支持DOMConentLoaded事件的就是DOMConentLoaded事件
    不支持的，就用来自Diego Perini发现的著名Hack兼容。兼容原理大概就是，通过IE中的document.documentElement.doScroll("left")来判断DOM树是否创建完毕。
    说明：window.onload事件：浏览器绘制完dom节点，在加载页面上的所有资源以后才执行我们自己定义的代码。也就是说在文档解析渲染、资源价在完成之前不让js脚本执行，但当资源过多是便出现短板，并不实用。
    domReady的实现：
    ```
    function myReady(fn){
        // 对于现代浏览器，对DOMContentLoaded事件的处理采用标准的事件绑定方式
        if(document.addEventListener){
            document.addEventListener("DOMContentLoaded", fn, false); // 在冒泡阶段捕获
        } else {
            IEContentLoaded(fn);
        }

        // IE模拟DOMContentLoaded
        function IEContentLoaded(fn){
            var d = window.document;
            var done = false;
        // 只执行一次的用户回调函数init()
        var init = function(){
            if(!done){
                done = true;
                fn();
            }
        }

        (function(){
            try{
            // DOM树未创建之前调用doScroll会抛出错误
            d.documentElement.doScroll('left');
            } catch(e){
            // 延迟再试一次，调用函数自身的事件
            setTimeout(arguments.callee, 50);
            return;
            }
            // 没有错误就表示DOM树创建完毕，然后立马执行用户回调
            init();
        })();

        // 监听document的加载状态
        d.onreadystatechange = function(){
            // 如果用户是在domReady之后绑定的函数，就立马执行
            if(d.readyState == 'complete') {
                d.onreadtstatechange = null;
                init();
            }
           }
        }
    }
```
    DOM文档加载的步骤为
    1.解析HTML结构
    2.加载外部脚本和样式文件
    3.解析并执行脚本文件
    4。DOM树构建完成  会触发DOMcontentLoaded事件
    5.加载图片等外部文件
   备注： 对于渲染引擎的工作流程的了解，有助于写出更好用户体验的代码。onload事件是要在所有请求都完成之后才执行，而domReady利用hack技术，在加载完dom树之后就能执行，所以domReady比onload执行时间更早，建议采用domReady。同时也可以去了解各大js框架，例如jquery，ext等，他们的domReady的实现机制
   
## 元素节点的判断
```
    元素节点类型判断
    /*isElement*/
    var testDiv = document.createElement('div');
    var isElement = function(obj){
        if(obj && obj.nodeType === 1){
            if (window.Node && (obj instanceof Node)) {
                return true;
            }
            try{
                testDiv.appendChild(obj);
                testDiv.removeChild(obj);
            } catch(e) {
                return false;
            }
            return false;
        }
        return false;
    }
    /*isXML*/
    var isXML = function (document) {
        return (!!document.xmlVersion) || (!!docuemnt.xml) || (toString.call(document) == '[object XMLDocument]') || ( document.nodeType == 9 && document.documentElement.nodeName != 'HTML');
    }
    /*2*/
    var isXML = function(doc){
        return doc.createElement('p').nodeName != doc.createElement('P').nodeName;
    }
    /*isHTML*/
    var isHTML = function(doc){
        return doc.createElement('p').nodeName === doc.createElement('P').nodeName;
    }
    /*自定义方法来判断结点之间的包含关系，兼容所有浏览器*/
    function fixContains (pNode, cNode) {
        try{
            while(cNode = cNode.parentNode){
                if(cNode === pNode){
                    return true;
                }
            }
            return false;
        }catch(e){
            return false;
        }
    }
```
来判断是否是 XML 文档：判断节点名是否是区分大小写的，HTML文档节点名不区分大小写判断XML和HTML的方法：
先使用isElememt判断是否为元素节点，再用creatElement判断元素名大写小写是否都等同，大小写不等同为XML，等同为HTML
```
var isXML = function(doc){
return doc.createElement('div').nodeName !== doc.createElement('DIV').nodeName;
}
判断包涵关系contains的方法 各浏览器通用的: 参考代码：
<div id="p-node">
		<div id="c-node">子节点内容</div>
	</div>
<script type="text/javascript">
	function fixContains(a, b) {
		try{
			while ((b = b.parentNode)){
				if (b ===a){
					return true;
				}
			}
			return false;
		} catch (e){
			return false;
		}
	}
	var pNode = document.getElementById("p-node");
	var cNode = document.getElementById("c-node").childNodes[0];
	alert(pNode.contains(cNode));
	</script>
```
### DOM节点继承层次
dom节点继承层次多，dom操作耗费性能，故将dom操作转交框架内部，精细化操作，虚拟dom，mvvm框架；dom节点十分复杂，
dom操作十分耗性能
react 提出虚拟dom，合并且屏蔽了无效的dom，大大提高了性能
备注：关于MVVM模式的前端框架，请移步：http://avalonjs.github.io/
### HTML嵌套规则：
块状元素与内联元素嵌套规则<br>
1，块状元素可以包含内联元素或 某些 块元素，但内联元素却不能包含块元素，它只能包含其他的内联元素。<br>
2，块级元素不能放在<p>里面。<br>
3，有几个特殊的块级元素只能包含內联元素，不能再包含块级元素，这几个特殊的标签：h1-h6,p,dt。<br>
4,li内可以包含div标签。（两者都是装载内容的容器，没有级别之分，同理，li内可以容纳ul/ol）<br>
5,块级元素与块级元素并列，内联元素与内联元素并列。<br>
<div><h2></h2><span></span></div>不提倡

对于<a>元素：

同时属于Flow content 、 Phrasing content、Interactive content、Palpable content分类
父元素必须是那些子元素为段落式元素的元素
允许的子元素是以它的父元素允许的子元素为准，但不能包含交互式元素
这样看<a>元素还是挺有意思的，允许的子元素要看它的父元素所能包含的子元素。

a元素里不可以嵌套交互式元素(<a>、<button>、<select>等)
<p>里面不可以嵌套<div>、<h1>~<h6>、<p>、<ul>/<ol>/<li>、<dl>/<dt>/<dd>、<form>
