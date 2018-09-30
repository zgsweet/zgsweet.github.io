<div class="cnblogs_Highlighter sh-gutter">
<pre class="brush:csharp;gutter:true;">第一章. ECMAScript 6简介
(1)ECMAScript和JavaScript的关系
(2)ECMAScript的历史
(3)部署进度
(4)Babel转码器
(5)Traceur转码器
(6)ECMAScript 7
第二章.let和const命令
(1)let命令
(2)块级作用域
(3)const命令
(4)全局对象的属性
第三章.变量的解构赋值
(1)数组的解构赋值
(2)对象的解构赋值
(3)字符串的解构赋值
(4)数值和布尔值的解构赋值
(5)函数参数的解构赋值
(6)圆括号问题
(7)用途
第四章.字符串的扩展
(1)字符的Unicode表示法
(2)codePointAt()
(3)String.fromCodePoint()
(4)字符串的遍历器接口
(5)at()
(6)normalize()
(7)includes(), startsWith(), endsWith()
(8)repeat()
(9)padStart()，padEnd()
(10)模板字符串
(11)实例：模板编译
(12)标签模板
(13)String.raw()
第五章.正则的扩展
(1)RegExp构造函数
(2)字符串的正则方法
(3)u修饰符
(4)y修饰符
(5)sticky属性
(6)flags属性
(7)RegExp.escape()
(8)后行断言
第六章.数值的扩展
(1)二进制和八进制表示法
(2)Number.isFinite(), Number.isNaN()
(3)Number.parseInt(), Number.parseFloat()
(4)Number.isInteger()
(5)Number.EPSILON
(6)安全整数和Number.isSafeInteger()
(7)Math对象的扩展
(8)指数运算符
第七章.数组的扩展
(1)Array.from()
(2)Array.of()
(3)数组实例的copyWithin()
(4)数组实例的find()和findIndex()
(5)数组实例的fill()
(6)数组实例的entries()，keys()和values()
(7)数组实例的includes()
(8)数组的空位
第八章.函数的扩展
(1)函数参数的默认值
(2)rest参数
(3)扩展运算符
(4)name属性
(5)箭头函数
(6)函数绑定
(7)尾调用优化
(8)函数参数的尾逗号
第九章.对象的扩展
(1)属性的简洁表示法
(2)属性名表达式
(3)方法的name属性
(4)Object.is()
(5)Object.assign()
(6)属性的可枚举性
(7)属性的遍历
(8)proto属性，Object.setPrototypeOf()，Object.getPrototypeOf()
(9)Object.values()，Object.entries()
(10)对象的扩展运算符
(11)Object.getOwnPropertyDescriptors()
第十章.Symbol
(1)概述
(2)作为属性名的Symbol
(3)实例：消除魔术字符串
(4)属性名的遍历
(5)Symbol.for()，Symbol.keyFor()
(6)实例：模块的 Singleton 模式
(7)内置的Symbol值
第十一章.Proxy和Reflect
(1)Proxy概述
(2)Proxy实例的方法
(3)Proxy.revocable()
(4)Reflect概述
(5)Reflect对象的方法
第十二章.二进制数组
(1)ArrayBuffer对象
(2)TypedArray视图
(3)复合视图
(4)DataView视图
(5)二进制数组的应用
第十三章.Set和Map数据结构
(1)Set
(2)WeakSet
(3)Map
(4)WeakMap
第十四章.Iterator和for...of循环
(1)Iterator（遍历器）的概念
(2)数据结构的默认Iterator接口
(3)调用Iterator接口的场合
(4)字符串的Iterator接口
(5)Iterator接口与Generator函数
(6)遍历器对象的return()，throw()
(7)for...of循环
第十五章.Generator 函数
(1)简介
(2)next方法的参数
(3)for...of循环
(4)Generator.prototype.throw()
(5)Generator.prototype.return()
(6)yield*语句
(7)作为对象属性的Generator函数
(8)Generator函数的this
(9)含义
(10)应用
第十六章.Promise对象
(1)Promise的含义
(2)基本用法
(3)Promise.prototype.then()
(4)Promise.prototype.catch()
(5)Promise.all()
(6)Promise.race()
(7)Promise.resolve()
(8)Promise.reject()
(9)两个有用的附加方法
(10)应用
第十七章.异步操作和Async函数
(1)基本概念
(2)Generator函数
(3)Thunk函数
(4)co模块
(5)async函数
第十八章.Class
(1)Class基本语法
(2)Class的继承
(3)原生构造函数的继承
(4)Class的取值函数（getter）和存值函数（setter）
(5)Class的Generator方法
(6)Class的静态方法
(7)Class的静态属性和实例属性
(8)new.target属性
(9)Mixin模式的实现
第十九章.修饰器
(1)类的修饰
(2)方法的修饰
(3)为什么修饰器不能用于函数？
(4)core-decorators.js
(5)使用修饰器实现自动发布事件
(6)Mixin
(7)Trait
(8)Babel转码器的支持
第二十章.Module
(1)严格模式
(2)export命令
(3)import命令
(4)模块的整体加载
(5)export default命令
(6)模块的继承
(7)ES6模块加载的实质
(8)循环加载
(9)跨模块常量
(10)ES6模块的转码
第二十一章.编程风格
(1)块级作用域
(2)字符串
(3)解构赋值
(4)对象
(5)数组
(6)函数
(7)Map结构
(8)Class
(9)模块
(10)ESLint的使用
第二十二章.读懂 ECMAScript 规格
(1)概述
(2)相等运算符
(3)数组的空位
(4)数组的map方法
1 ECMAScript 6简介
ECMAScript 6.0（以下简称ES6）是JavaScript语言的下一代标准，已经在2015年6月正式发布了。它的目标，是使得JavaScript语言可以用来编写复
杂的大型应用程序，成为企业级开发语言。
标准的制定者有计划，以后每年发布一次标准，使用年份作为版本。因为ES6的第一个版本是在2015年发布的，所以又称ECMAScript 2015（简称
ES2015）。
2016年6月，小幅修订的《ECMAScript 2016 标准》（简称 ES2016）如期发布。由于变动非常小（只新增了数组实例的includes方法和指数运算
符），因此 ES2016 与 ES2015 基本上是同一个标准，都被看作是 ES6。根据计划，2017年6月将发布 ES2017。
1.1 ECMAScript和JavaScript的关系
一个常见的问题是，ECMAScript和JavaScript到底是什么关系？
要讲清楚这个问题，需要回顾历史。1996年11月，JavaScript的创造者Netscape公司，决定将JavaScript提交给国际标准化组织ECMA，希望这种语言
能够成为国际标准。次年，ECMA发布262号标准文件（ECMA-262）的第一版，规定了浏览器脚本语言的标准，并将这种语言称为ECMAScript，这个
版本就是1.0版。
该标准从一开始就是针对JavaScript语言制定的，但是之所以不叫JavaScript，有两个原因。一是商标，Java是Sun公司的商标，根据授权协议，只有
Netscape公司可以合法地使用JavaScript这个名字，且JavaScript本身也已经被Netscape公司注册为商标。二是想体现这门语言的制定者是ECMA，不
是Netscape，这样有利于保证这门语言的开放性和中立性。
因此，ECMAScript和JavaScript的关系是，前者是后者的规格，后者是前者的一种实现（另外的ECMAScript方言还有Jscript和ActionScript）。日常场
合，这两个词是可以互换的。
1.2 ECMAScript的历史
ES6从开始制定到最后发布，整整用了15年。
前面提到，ECMAScript 1.0是1997年发布的，接下来的两年，连续发布了ECMAScript 2.0（1998年6月）和ECMAScript 3.0（1999年12月）。3.0版
是一个巨大的成功，在业界得到广泛支持，成为通行标准，奠定了JavaScript语言的基本语法，以后的版本完全继承。直到今天，初学者一开始学习
JavaScript，其实就是在学3.0版的语法。
2000年，ECMAScript 4.0开始酝酿。这个版本最后没有通过，但是它的大部分内容被ES6继承了。因此，ES6制定的起点其实是2000年。
为什么ES4没有通过呢？因为这个版本太激进了，对ES3做了彻底升级，导致标准委员会的一些成员不愿意接受。ECMA的第39号技术专家委员会
（Technical Committee 39，简称TC39）负责制订ECMAScript标准，成员包括Microsoft、Mozilla、Google等大公司。
2007年10月，ECMAScript 4.0版草案发布，本来预计次年8月发布正式版本。但是，各方对于是否通过这个标准，发生了严重分歧。以Yahoo、
Microsoft、Google为首的大公司，反对JavaScript的大幅升级，主张小幅改动；以JavaScript创造者Brendan Eich为首的Mozilla公司，则坚持当前的草
案。
2008年7月，由于对于下一个版本应该包括哪些功能，各方分歧太大，争论过于激烈，ECMA开会决定，中止ECMAScript 4.0的开发，将其中涉及现有
功能改善的一小部分，发布为ECMAScript 3.1，而将其他激进的设想扩大范围，放入以后的版本，由于会议的气氛，该版本的项目代号起名为
Harmony（和谐）。会后不久，ECMAScript 3.1就改名为ECMAScript 5。
2009年12月，ECMAScript 5.0版正式发布。Harmony项目则一分为二，一些较为可行的设想定名为JavaScript.next继续开发，后来演变成ECMAScript
6；一些不是很成熟的设想，则被视为JavaScript.next.next，在更远的将来再考虑推出。TC39委员会的总体考虑是，ES5与ES3基本保持兼容，较大的
语法修正和新功能加入，将由JavaScript.next完成。当时，JavaScript.next指的是ES6，第六版发布以后，就指ES7。TC39的判断是，ES5会在2013年
的年中成为JavaScript开发的主流标准，并在此后五年中一直保持这个位置。
2011年6月，ECMAscript 5.1版发布，并且成为ISO国际标准（ISO/IEC 16262:2011）。
2013年3月，ECMAScript 6草案冻结，不再添加新功能。新的功能设想将被放到ECMAScript 7。
2013年12月，ECMAScript 6草案发布。然后是12个月的讨论期，听取各方反馈。
2015年6月，ECMAScript 6正式通过，成为国际标准。从2000年算起，这时已经过去了15年。
1.3 部署进度
各大浏览器的最新版本，对ES6的支持可以查看kangax.github.io/es5-compat-table/es6/。随着时间的推移，支持度已经越来越高了，ES6的大部分特
性都实现了。
Node.js是JavaScript语言的服务器运行环境，对ES6的支持度比浏览器更高。通过Node，可以体验更多ES6的特性。建议使用版本管理工具nvm，来安
装Node，因为可以自由切换版本。不过，nvm不支持Windows系统，如果你使用Windows系统，下面的操作可以改用nvmw或nvm-windows代替。
安装nvm需要打开命令行窗口，运行下面的命令。
安装nvm需要打开命令行窗口，运行下面的命令。
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/&lt;version number&gt;/install.sh | bash
上面命令的version number处，需要用版本号替换。本节写作时的版本号是v0.29.0。该命令运行后，nvm会默认安装在用户主目录的.nvm子目录。
然后，激活nvm。
$ source ~/.nvm/nvm.sh
激活以后，安装Node的最新版。
$ nvm install node
安装完成后，切换到该版本。
$ nvm use node
使用下面的命令，可以查看Node所有已经实现的ES6特性。
$ node --v8-options | grep harmony
--harmony_typeof
--harmony_scoping
--harmony_modules
--harmony_symbols
--harmony_proxies
--harmony_collections
--harmony_observation
--harmony_generators
--harmony_iteration
--harmony_numeric_literals
--harmony_strings
--harmony_arrays
--harmony_maths
--harmony
上面命令的输出结果，会因为版本的不同而有所不同。
我写了一个ES-Checker模块，用来检查各种运行环境对ES6的支持情况。访问ruanyf.github.io/es-checker，可以看到您的浏览器支持ES6的程度。运
行下面的命令，可以查看你正在使用的Node环境对ES6的支持程度。
$ npm install -g es-checker
$ es-checker
=========================================
Passes 24 feature Dectations
Your runtime supports 57% of ECMAScript 6
=========================================
1.4 Babel转码器
Babel是一个广泛使用的ES6转码器，可以将ES6代码转为ES5代码，从而在现有环境执行。这意味着，你可以用ES6的方式编写程序，又不用担心现
有环境是否支持。下面是一个例子。
// 转码前
input.map(item =&gt; item + 1);
// 转码后
input.map(function (item) {
return item + 1;
});
上面的原始代码用了箭头函数，这个特性还没有得到广泛支持，Babel将其转为普通函数，就能在现有的JavaScript环境执行了。
1.4.1 配置文件.babelrc
Babel的配置文件是.babelrc，存放在项目的根目录下。使用Babel的第一步，就是配置这个文件。
该文件用来设置转码规则和插件，基本格式如下。
{
"presets": [],
"plugins": []
}
presets字段设定转码规则，官方提供以下的规则集，你可以根据需要安装。
# ES2015转码规则
$ npm install --save-dev babel-preset-es2015
# react转码规则
$ npm install --save-dev babel-preset-react
# ES7不同阶段语法提案的转码规则（共有4个阶段），选装一个
$ npm install --save-dev babel-preset-stage-0
$ npm install --save-dev babel-preset-stage-1
$ npm install --save-dev babel-preset-stage-2
$ npm install --save-dev babel-preset-stage-3
然后，将这些规则加入.babelrc。
{
"presets": [
"es2015",
"react",
"stage-2"
],
"plugins": []
}
注意，以下所有Babel工具和模块的使用，都必须先写好.babelrc。
1.4.2 命令行转码babel-cli
Babel提供babel-cli工具，用于命令行转码。
它的安装命令如下。
$ npm install --global babel-cli
基本用法如下。
# 转码结果输出到标准输出
$ babel example.js
# 转码结果写入一个文件
# --out-file 或 -o 参数指定输出文件
$ babel example.js --out-file compiled.js
# 或者
$ babel example.js -o compiled.js
# 整个目录转码
# --out-dir 或 -d 参数指定输出目录
$ babel src --out-dir lib
# 或者
$ babel src -d lib
# -s 参数生成source map文件
$ babel src -d lib -s
上面代码是在全局环境下，进行Babel转码。这意味着，如果项目要运行，全局环境必须有Babel，也就是说项目产生了对环境的依赖。另一方面，这
样做也无法支持不同项目使用不同版本的Babel。
一个解决办法是将babel-cli安装在项目之中。
# 安装
$ npm install --save-dev babel-cli
然后，改写package.json。
{
// ...
"devDependencies": {
"babel-cli": "^6.0.0"
},
"scripts": {
"build": "babel src -d lib"
},
}
转码的时候，就执行下面的命令。
$ npm run build
1.4.3 babel-node
babel-cli工具自带一个babel-node命令，提供一个支持ES6的REPL环境。它支持Node的REPL环境的所有功能，而且可以直接运行ES6代码。
它不用单独安装，而是随babel-cli一起安装。然后，执行babel-node就进入REPL环境。
$ babel-node
&gt; (x =&gt; x * 2)(1)
2
babel-node命令可以直接运行ES6脚本。将上面的代码放入脚本文件es6.js，然后直接运行。
$ babel-node es6.js
2
babel-node也可以安装在项目中。
$ npm install --save-dev babel-cli
然后，改写package.json。
{
"scripts": {
"script-name": "babel-node script.js"
}
}
上面代码中，使用babel-node替代node，这样script.js本身就不用做任何转码处理。
1.4.4 babel-register
babel-register模块改写require命令，为它加上一个钩子。此后，每当使用require加载.js、.jsx、.es和.es6后缀名的文件，就会先用Babel进行
转码。
$ npm install --save-dev babel-register
使用时，必须首先加载babel-register。
require("babel-register");
require("./index.js");
然后，就不需要手动对index.js转码了。
需要注意的是，babel-register只会对require命令加载的文件转码，而不会对当前文件转码。另外，由于它是实时转码，所以只适合在开发环境使
用。
1.4.5 babel-core
如果某些代码需要调用Babel的API进行转码，就要使用babel-core模块。
安装命令如下。
$ npm install babel-core --save
然后，在项目中就可以调用babel-core。
var babel = require('babel-core');
// 字符串转码
babel.transform('code();', options);
// =&gt; { code, map, ast }
// 文件转码（异步）
babel.transformFile('filename.js', options, function(err, result) {
result; // =&gt; { code, map, ast }
});
// 文件转码（同步）
babel.transformFileSync('filename.js', options);
// =&gt; { code, map, ast }
// Babel AST转码
babel.transformFromAst(ast, code, options);
// =&gt; { code, map, ast }
配置对象options，可以参看官方文档http://babeljs.io/docs/usage/options/。
下面是一个例子。
var es6Code = 'let x = n =&gt; n + 1';
var es5Code = require('babel-core')
.transform(es6Code, {
presets: ['es2015']
})
.code;
// '"use strict";\n\nvar x = function x(n) {\n return n + 1;\n};'
上面代码中，transform方法的第一个参数是一个字符串，表示需要被转换的ES6代码，第二个参数是转换的配置对象。
1.4.6 babel-polyfill
Babel默认只转换新的JavaScript句法（syntax），而不转换新的API，比如Iterator、Generator、Set、Maps、Proxy、Reflect、Symbol、Promise等全
局对象，以及一些定义在全局对象上的方法（比如Object.assign）都不会转码。
举例来说，ES6在Array对象上新增了Array.from方法。Babel就不会转码这个方法。如果想让这个方法运行，必须使用babel-polyfill，为当前环境
提供一个垫片。
安装命令如下。
$ npm install --save babel-polyfill
然后，在脚本头部，加入如下一行代码。
import 'babel-polyfill';
// 或者
require('babel-polyfill');
Babel默认不转码的API非常多，详细清单可以查看babel-plugin-transform-runtime模块的definitions.js文件。
1.4.7 浏览器环境
Babel也可以用于浏览器环境。但是，从Babel 6.0开始，不再直接提供浏览器版本，而是要用构建工具构建出来。如果你没有或不想使用构建工具，可
以通过安装5.x版本的babel-core模块获取。
$ npm install babel-core@5
运行上面的命令以后，就可以在当前目录的node_modules/babel-core/子目录里面，找到babel的浏览器版本browser.js（未精简）
和browser.min.js（已精简）。
然后，将下面的代码插入网页。
&lt;script src="node_modules/babel-core/browser.js"&gt;&lt;/script&gt;
&lt;script type="text/babel"&gt;
// Your ES6 code
&lt;/script&gt;
上面代码中，browser.js是Babel提供的转换器脚本，可以在浏览器运行。用户的ES6脚本放在script标签之中，但是要注明type="text/babel"。
另一种方法是使用babel-standalone模块提供的浏览器版本，将其插入网页。
&lt;script src="https://cdnjs.cloudflare.com/ajax/libs/babel-standalone/6.4.4/babel.min.js"&gt;&lt;/script&gt;
&lt;script type="text/babel"&gt;
// Your ES6 code
&lt;/script&gt;
注意，网页中实时将ES6代码转为ES5，对性能会有影响。生产环境需要加载已经转码完成的脚本。
下面是如何将代码打包成浏览器可以使用的脚本，以Babel配合Browserify为例。首先，安装babelify模块。
$ npm install --save-dev babelify babel-preset-es2015
然后，再用命令行转换ES6脚本。
$ browserify script.js -o bundle.js \
-t [ babelify --presets [ es2015 ] ]
上面代码将ES6脚本script.js，转为bundle.js，浏览器直接加载后者就可以了。
在package.json设置下面的代码，就不用每次命令行都输入参数了。
{
"browserify": {
"transform": [["babelify", { "presets": ["es2015"] }]]
}
}
1.4.8 在线转换
Babel提供一个REPL在线编译器，可以在线将ES6代码转为ES5代码。转换后的代码，可以直接作为ES5代码插入网页运行。
1.4.9 与其他工具的配合
许多工具需要Babel进行前置转码，这里举两个例子：ESLint和Mocha。
ESLint用于静态检查代码的语法和风格，安装命令如下。
$ npm install --save-dev eslint babel-eslint
然后，在项目根目录下，新建一个配置文件.eslintrc，在其中加入parser字段。
{
"parser": "babel-eslint",
"rules": {
...
}
}
再在package.json之中，加入相应的scripts脚本。
{
"name": "my-module",
"scripts": {
"lint": "eslint my-files.js"
},
"devDependencies": {
"babel-eslint": "...",
"eslint": "..."
}
}
Mocha则是一个测试框架，如果需要执行使用ES6语法的测试脚本，可以修改package.json的scripts.test。
"scripts": {
"test": "mocha --ui qunit --compilers js:babel-core/register"
}
上面命令中，--compilers参数指定脚本的转码器，规定后缀名为js的文件，都需要使用babel-core/register先转码。
1.5 Traceur转码器
Google公司的Traceur转码器，也可以将ES6代码转为ES5代码。
1.5.1 直接插入网页
Traceur允许将ES6代码直接插入网页。首先，必须在网页头部加载Traceur库文件。
&lt;script src="https://google.github.io/traceur-compiler/bin/traceur.js"&gt;&lt;/script&gt;
&lt;script src="https://google.github.io/traceur-compiler/bin/BrowserSystem.js"&gt;&lt;/script&gt;
&lt;script src="https://google.github.io/traceur-compiler/src/bootstrap.js"&gt;&lt;/script&gt;
&lt;script type="module"&gt;
import './Greeter.js';
&lt;/script&gt;
上面代码中，一共有4个script标签。第一个是加载Traceur的库文件，第二个和第三个是将这个库文件用于浏览器环境，第四个则是加载用户脚本，
这个脚本里面可以使用ES6代码。
注意，第四个script标签的type属性的值是module，而不是text/javascript。这是Traceur编译器识别ES6代码的标志，编译器会自动将所
有type=module的代码编译为ES5，然后再交给浏览器执行。
除了引用外部ES6脚本，也可以直接在网页中放置ES6代码。
&lt;script type="module"&gt;
class Calc {
constructor(){
console.log('Calc constructor');
}
add(a, b){
return a + b;
}
}
var c = new Calc();
console.log(c.add(4,5));
&lt;/script&gt;
正常情况下，上面代码会在控制台打印出9。
如果想对Traceur的行为有精确控制，可以采用下面参数配置的写法。
&lt;script&gt;
// Create the System object
window.System = new traceur.runtime.BrowserTraceurLoader();
// Set some experimental options
var metadata = {
traceurOptions: {
experimental: true,
properTailCalls: true,
symbols: true,
arrayComprehension: true,
asyncFunctions: true,
asyncGenerators: exponentiation,
forOn: true,
generatorComprehension: true
}
};
// Load your module
System.import('./myModule.js', {metadata: metadata}).catch(function(ex) {
console.error('Import failed', ex.stack || ex);
});
&lt;/script&gt;
上面代码中，首先生成Traceur的全局对象window.System，然后System.import方法可以用来加载ES6模块。加载的时候，需要传入一个配置对
象metadata，该对象的traceurOptions属性可以配置支持ES6功能。如果设为experimental: true，就表示除了ES6以外，还支持一些实验性的新功
能。
1.5.2 在线转换
Traceur也提供一个在线编译器，可以在线将ES6代码转为ES5代码。转换后的代码，可以直接作为ES5代码插入网页运行。
上面的例子转为ES5代码运行，就是下面这个样子。
&lt;script src="https://google.github.io/traceur-compiler/bin/traceur.js"&gt;&lt;/script&gt;
&lt;script src="https://google.github.io/traceur-compiler/bin/BrowserSystem.js"&gt;&lt;/script&gt;
&lt;script src="https://google.github.io/traceur-compiler/src/bootstrap.js"&gt;&lt;/script&gt;
&lt;script&gt;
$traceurRuntime.ModuleStore.getAnonymousModule(function() {
"use strict";
var Calc = function Calc() {
console.log('Calc constructor');
};
($traceurRuntime.createClass)(Calc, {add: function(a, b) {
return a + b;
}}, {});
var c = new Calc();
console.log(c.add(4, 5));
return {};
});
&lt;/script&gt;
1.5.3 命令行转换
作为命令行工具使用时，Traceur是一个Node的模块，首先需要用Npm安装。
$ npm install -g traceur
安装成功后，就可以在命令行下使用Traceur了。
Traceur直接运行es6脚本文件，会在标准输出显示运行结果，以前面的calc.js为例。
$ traceur calc.js
Calc constructor
9
如果要将ES6脚本转为ES5保存，要采用下面的写法。
$ traceur --script calc.es6.js --out calc.es5.js
上面代码的--script选项表示指定输入文件，--out选项表示指定输出文件。
为了防止有些特性编译不成功，最好加上--experimental选项。
$ traceur --script calc.es6.js --out calc.es5.js --experimental
命令行下转换生成的文件，就可以直接放到浏览器中运行。
1.5.4 Node.js环境的用法
Traceur的Node.js用法如下（假定已安装traceur模块）。
var traceur = require('traceur');
var fs = require('fs');
// 将ES6脚本转为字符串
var contents = fs.readFileSync('es6-file.js').toString();
var result = traceur.compile(contents, {
filename: 'es6-file.js',
sourceMap: true,
// 其他设置
modules: 'commonjs'
});
if (result.error)
throw result.error;
// result对象的js属性就是转换后的ES5代码
fs.writeFileSync('out.js', result.js);
// sourceMap属性对应map文件
fs.writeFileSync('out.js.map', result.sourceMap);
1.6 ECMAScript 7
2013年3月，ES6的草案封闭，不再接受新功能了。新的功能将被加入ES7。
任何人都可以向TC39提案，从提案到变成正式标准，需要经历五个阶段。每个阶段的变动都需要由TC39委员会批准。
Stage 0 - Strawman（展示阶段）
Stage 1 - Proposal（征求意见阶段）
Stage 2 - Draft（草案阶段）
Stage 3 - Candidate（候选人阶段）
Stage 4 - Finished（定案阶段）
一个提案只要能进入Stage 2，就差不多等于肯定会包括在ES7里面。
本书的写作目标之一，是跟踪ECMAScript语言的最新进展。对于那些明确的、或者很有希望列入ES7的功能，尤其是那些Babel已经支持的功能，都将
予以介绍。
本书介绍的ES7功能清单如下。
Stage 0：
Function Bind Syntax：函数的绑定运算符
String.prototype.at：字符串的静态方法at
Stage 1：
Class and Property Decorators：Class的修饰器
Class Property Declarations：Class的属性声明
Additional export-from Statements：export的写法改进
String.prototype.{trimLeft,trimRight}：字符串删除头尾空格的方法
Stage 2：
Rest/Spread Properties：对象的Rest参数和扩展运算符
Stage 3
SIMD API：“单指令，多数据”命令集
Async Functions：async函数
Object.values/Object.entries：Object的静态方法values()和entries()
String padding：字符串长度补全
Trailing commas in function parameter lists and calls：函数参数的尾逗号
Object.getOwnPropertyDescriptors：Object的静态方法getOwnPropertyDescriptors
Stage 4：
Array.prototype.includes：数组实例的includes方法
Exponentiation Operator：指数运算符
ECMAScript当前的所有提案，可以在TC39的官方网站Github.com/tc39/ecma262查看。
Babel转码器可以通过安装和使用插件来使用各个stage的语法。
2 let和const命令
2.1 let命令
2.1.1 基本用法
ES6新增了let命令，用来声明变量。它的用法类似于var，但是所声明的变量，只在let命令所在的代码块内有效。
{
let a = 10;
var b = 1;
}
a // ReferenceError: a is not defined.
b // 1
上面代码在代码块之中，分别用let和var声明了两个变量。然后在代码块之外调用这两个变量，结果let声明的变量报错，var声明的变量返回了正确
的值。这表明，let声明的变量只在它所在的代码块有效。
for循环的计数器，就很合适使用let命令。
for (let i = 0; i &lt; arr.length; i++) {}
console.log(i);
//ReferenceError: i is not defined
上面代码的计数器i，只在for循环体内有效。
下面的代码如果使用var，最后输出的是10。
var a = [];
for (var i = 0; i &lt; 10; i++) {
a[i] = function () {
console.log(i);
};
}
a[6](); // 10
上面代码中，变量i是var声明的，在全局范围内都有效。所以每一次循环，新的i值都会覆盖旧值，导致最后输出的是最后一轮的i的值。
如果使用let，声明的变量仅在块级作用域内有效，最后输出的是6。
var a = [];
for (let i = 0; i &lt; 10; i++) {
a[i] = function () {
console.log(i);
};
}
a[6](); // 6
上面代码中，变量i是let声明的，当前的i只在本轮循环有效，所以每一次循环的i其实都是一个新的变量，所以最后输出的是6。
2.1.2 不存在变量提升
let不像var那样会发生“变量提升”现象。所以，变量一定要在声明后使用，否则报错。
console.log(foo); // 输出undefined
console.log(bar); // 报错ReferenceError
var foo = 2;
let bar = 2;
上面代码中，变量foo用var命令声明，会发生变量提升，即脚本开始运行时，变量foo已经存在了，但是没有值，所以会输出undefined。变
量bar用let命令声明，不会发生变量提升。这表示在声明它之前，变量bar是不存在的，这时如果用到它，就会抛出一个错误。
2.1.3 暂时性死区
只要块级作用域内存在let命令，它所声明的变量就“绑定”（binding）这个区域，不再受外部的影响。
var tmp = 123;
if (true) {
tmp = 'abc'; // ReferenceError
let tmp;
}
上面代码中，存在全局变量tmp，但是块级作用域内let又声明了一个局部变量tmp，导致后者绑定这个块级作用域，所以在let声明变量前，对tmp赋
值会报错。
ES6明确规定，如果区块中存在let和const命令，这个区块对这些命令声明的变量，从一开始就形成了封闭作用域。凡是在声明之前就使用这些变
量，就会报错。
总之，在代码块内，使用let命令声明变量之前，该变量都是不可用的。这在语法上，称为“暂时性死区”（temporal dead zone，简称TDZ）。
if (true) {
// TDZ开始
tmp = 'abc'; // ReferenceError
console.log(tmp); // ReferenceError
let tmp; // TDZ结束
console.log(tmp); // undefined
tmp = 123;
console.log(tmp); // 123
}
上面代码中，在let命令声明变量tmp之前，都属于变量tmp的“死区”。
“暂时性死区”也意味着typeof不再是一个百分之百安全的操作。
typeof x; // ReferenceError
let x;
上面代码中，变量x使用let命令声明，所以在声明之前，都属于x的“死区”，只要用到该变量就会报错。因此，typeof运行时就会抛出一
个ReferenceError。
作为比较，如果一个变量根本没有被声明，使用typeof反而不会报错。
typeof undeclared_variable // "undefined"
上面代码中，undeclared_variable是一个不存在的变量名，结果返回“undefined”。所以，在没有let之前，typeof运算符是百分之百安全的，永远不
会报错。现在这一点不成立了。这样的设计是为了让大家养成良好的编程习惯，变量一定要在声明之后使用，否则就报错。
有些“死区”比较隐蔽，不太容易发现。
function bar(x = y, y = 2) {
return [x, y];
}
bar(); // 报错
上面代码中，调用bar函数之所以报错（某些实现可能不报错），是因为参数x默认值等于另一个参数y，而此时y还没有声明，属于”死区“。如果y的默
认值是x，就不会报错，因为此时x已经声明了。
function bar(x = 2, y = x) {
return [x, y];
}
bar(); // [2, 2]
ES6规定暂时性死区和let、const语句不出现变量提升，主要是为了减少运行时错误，防止在变量声明前就使用这个变量，从而导致意料之外的行
为。这样的错误在ES5是很常见的，现在有了这种规定，避免此类错误就很容易了。
总之，暂时性死区的本质就是，只要一进入当前作用域，所要使用的变量就已经存在了，但是不可获取，只有等到声明变量的那一行代码出现，才可
以获取和使用该变量。
2.1.4 不允许重复声明
let不允许在相同作用域内，重复声明同一个变量。
// 报错
function () {
let a = 10;
var a = 1;
}
// 报错
// 报错
function () {
let a = 10;
let a = 1;
}
因此，不能在函数内部重新声明参数。
function func(arg) {
let arg; // 报错
}
function func(arg) {
{
let arg; // 不报错
}
}
2.2 块级作用域
2.2.1 为什么需要块级作用域？
ES5只有全局作用域和函数作用域，没有块级作用域，这带来很多不合理的场景。
第一种场景，内层变量可能会覆盖外层变量。
var tmp = new Date();
function f() {
console.log(tmp);
if (false) {
var tmp = "hello world";
}
}
f(); // undefined
上面代码中，函数f执行后，输出结果为undefined，原因在于变量提升，导致内层的tmp变量覆盖了外层的tmp变量。
第二种场景，用来计数的循环变量泄露为全局变量。
var s = 'hello';
for (var i = 0; i &lt; s.length; i++) {
console.log(s[i]);
}
console.log(i); // 5
上面代码中，变量i只用来控制循环，但是循环结束后，它并没有消失，泄露成了全局变量。
2.2.2 ES6的块级作用域
let实际上为JavaScript新增了块级作用域。
function f1() {
let n = 5;
if (true) {
let n = 10;
}
console.log(n); // 5
}
上面的函数有两个代码块，都声明了变量n，运行后输出5。这表示外层代码块不受内层代码块的影响。如果使用var定义变量n，最后输出的值就是
10。
ES6允许块级作用域的任意嵌套。
{{{{{let insane = 'Hello World'}}}}};
上面代码使用了一个五层的块级作用域。外层作用域无法读取内层作用域的变量。
{{{{
{let insane = 'Hello World'}
console.log(insane); // 报错
}}}};
内层作用域可以定义外层作用域的同名变量。
{{{{
let insane = 'Hello World';
{let insane = 'Hello World'}
}}}};
块级作用域的出现，实际上使得获得广泛应用的立即执行匿名函数（IIFE）不再必要了。
// IIFE写法
(function () {
var tmp = ...;
...
}());
// 块级作用域写法
{
let tmp = ...;
...
}
2.2.3 块级作用域与函数声明
函数能不能在块级作用域之中声明，是一个相当令人混淆的问题。
ES5规定，函数只能在顶层作用域和函数作用域之中声明，不能在块级作用域声明。
// 情况一
if (true) {
function f() {}
}
// 情况二
try {
function f() {}
} catch(e) {
}
上面代码的两种函数声明，根据ES5的规定都是非法的。
但是，浏览器没有遵守这个规定，还是支持在块级作用域之中声明函数，因此上面两种情况实际都能运行，不会报错。不过，“严格模式”下还是会报
错。
// ES5严格模式
'use strict';
if (true) {
function f() {}
}
// 报错
ES6引入了块级作用域，明确允许在块级作用域之中声明函数。
// ES6严格模式
'use strict';
if (true) {
function f() {}
}
// 不报错
并且ES6规定，块级作用域之中，函数声明语句的行为类似于let，在块级作用域之外不可引用。
function f() { console.log('I am outside!'); }
(function () {
if (false) {
// 重复声明一次函数f
function f() { console.log('I am inside!'); }
}
f();
}());
上面代码在ES5中运行，会得到“I am inside!”，因为在if内声明的函数f会被提升到函数头部，实际运行的代码如下。
// ES5版本
function f() { console.log('I am outside!'); }
(function () {
function f() { console.log('I am inside!'); }
if (false) {
}
f();
}());
ES6的运行结果就完全不一样了，会得到“I am outside!”。因为块级作用域内声明的函数类似于let，对作用域之外没有影响，实际运行的代码如下。
// ES6版本
function f() { console.log('I am outside!'); }
(function () {
f();
}());
很显然，这种行为差异会对老代码产生很大影响。为了减轻因此产生的不兼容问题，ES6在附录B里面规定，浏览器的实现可以不遵守上面的规定，有
自己的行为方式。
允许在块级作用域内声明函数。
函数声明类似于var，即会提升到全局作用域或函数作用域的头部。
同时，函数声明还会提升到所在的块级作用域的头部。
注意，上面三条规则只对ES6的浏览器实现有效，其他环境的实现不用遵守，还是将块级作用域的函数声明当作let处理。
前面那段代码，在Chrome环境下运行会报错。
// ES6的浏览器环境
function f() { console.log('I am outside!'); }
(function () {
if (false) {
// 重复声明一次函数f
function f() { console.log('I am inside!'); }
}
f();
}());
// Uncaught TypeError: f is not a function
上面的代码报错，是因为实际运行的是下面的代码。
// ES6的浏览器环境
function f() { console.log('I am outside!'); }
(function () {
var f = undefined;
if (false) {
function f() { console.log('I am inside!'); }
}
f();
}());
// Uncaught TypeError: f is not a function
考虑到环境导致的行为差异太大，应该避免在块级作用域内声明函数。如果确实需要，也应该写成函数表达式，而不是函数声明语句。
// 函数声明语句
{
let a = 'secret';
function f() {
return a;
}
}
// 函数表达式
{
let a = 'secret';
let f = function () {
return a;
};
}
另外，还有一个需要注意的地方。ES6的块级作用域允许声明函数的规则，只在使用大括号的情况下成立，如果没有使用大括号，就会报错。
// 不报错
'use strict';
if (true) {
function f() {}
}
// 报错
'use strict';
if (true)
function f() {}
2.3 const命令
const声明一个只读的常量。一旦声明，常量的值就不能改变。
const PI = 3.1415;
PI // 3.1415
PI = 3;
// TypeError: Assignment to constant variable.
上面代码表明改变常量的值会报错。
const声明的变量不得改变值，这意味着，const一旦声明变量，就必须立即初始化，不能留到以后赋值。
const foo;
// SyntaxError: Missing initializer in const declaration
上面代码表示，对于const来说，只声明不赋值，就会报错。
const的作用域与let命令相同：只在声明所在的块级作用域内有效。
if (true) {
const MAX = 5;
}
MAX // Uncaught ReferenceError: MAX is not defined
const命令声明的常量也是不提升，同样存在暂时性死区，只能在声明的位置后面使用。
if (true) {
console.log(MAX); // ReferenceError
const MAX = 5;
}
上面代码在常量MAX声明之前就调用，结果报错。
const声明的常量，也与let一样不可重复声明。
var message = "Hello!";
let age = 25;
// 以下两行都会报错
const message = "Goodbye!";
const age = 30;
对于复合类型的变量，变量名不指向数据，而是指向数据所在的地址。const命令只是保证变量名指向的地址不变，并不保证该地址的数据不变，所以
将一个对象声明为常量必须非常小心。
const foo = {};
foo.prop = 123;
foo.prop
// 123
foo = {}; // TypeError: "foo" is read-only
上面代码中，常量foo储存的是一个地址，这个地址指向一个对象。不可变的只是这个地址，即不能把foo指向另一个地址，但对象本身是可变的，所
以依然可以为其添加新属性。
下面是另一个例子。
const a = [];
a.push('Hello'); // 可执行
a.length = 0; // 可执行
a = ['Dave']; // 报错
上面代码中，常量a是一个数组，这个数组本身是可写的，但是如果将另一个数组赋值给a，就会报错。
如果真的想将对象冻结，应该使用Object.freeze方法。
const foo = Object.freeze({});
// 常规模式时，下面一行不起作用；
// 严格模式时，该行会报错
foo.prop = 123;
上面代码中，常量foo指向一个冻结的对象，所以添加新属性不起作用，严格模式时还会报错。
除了将对象本身冻结，对象的属性也应该冻结。下面是一个将对象彻底冻结的函数。
var constantize = (obj) =&gt; {
Object.freeze(obj);
Object.keys(obj).forEach( (key, value) =&gt; {
if ( typeof obj[key] === 'object' ) {
constantize( obj[key] );
}
});
};
ES5只有两种声明变量的方法：var命令和function命令。ES6除了添加let和const命令，后面章节还会提到，另外两种声明变量的方法：import命令
和class命令。所以，ES6一共有6种声明变量的方法。
2.4 全局对象的属性
全局对象是最顶层的对象，在浏览器环境指的是window对象，在Node.js指的是global对象。ES5之中，全局对象的属性与全局变量是等价的。
window.a = 1;
a // 1
a = 2;
window.a // 2
上面代码中，全局对象的属性赋值与全局变量的赋值，是同一件事。（对于Node来说，这一条只对REPL环境适用，模块环境之中，全局变量必须显式
声明成global对象的属性。）
未声明的全局变量，自动成为全局对象window的属性，这被认为是JavaScript语言最大的设计败笔之一。这样的设计带来了两个很大的问题，首先是没
法在编译时就报出变量未声明的错误，只有运行时才能知道，其次程序员很容易不知不觉地就创建了全局变量（比如打字出错）。另一方面，从语义
上讲，语言的顶层对象是一个有实体含义的对象，也是不合适的。
ES6为了改变这一点，一方面规定，为了保持兼容性，var命令和function命令声明的全局变量，依旧是全局对象的属性；另一方面规定，let命
令、const命令、class命令声明的全局变量，不属于全局对象的属性。也就是说，从ES6开始，全局变量将逐步与全局对象的属性脱钩。
var a = 1;
// 如果在Node的REPL环境，可以写成global.a
// 或者采用通用方法，写成this.a
window.a // 1
let b = 1;
window.b // undefined
上面代码中，全局变量a由var命令声明，所以它是全局对象的属性；全局变量b由let命令声明，所以它不是全局对象的属性，返回undefined。
3 变量的解构赋值
3.1 数组的解构赋值
3.1.1 基本用法
ES6允许按照一定模式，从数组和对象中提取值，对变量进行赋值，这被称为解构（Destructuring）。
以前，为变量赋值，只能直接指定值。
var a = 1;
var b = 2;
var c = 3;
ES6允许写成下面这样。
var [a, b, c] = [1, 2, 3];
上面代码表示，可以从数组中提取值，按照对应位置，对变量赋值。
本质上，这种写法属于“模式匹配”，只要等号两边的模式相同，左边的变量就会被赋予对应的值。下面是一些使用嵌套数组进行解构的例子。
let [foo, [[bar], baz]] = [1, [[2], 3]];
foo // 1
foo // 1
bar // 2
baz // 3
let [ , , third] = ["foo", "bar", "baz"];
third // "baz"
let [x, , y] = [1, 2, 3];
x // 1
y // 3
let [head, ...tail] = [1, 2, 3, 4];
head // 1
tail // [2, 3, 4]
let [x, y, ...z] = ['a'];
x // "a"
y // undefined
z // []
如果解构不成功，变量的值就等于undefined。
var [foo] = [];
var [bar, foo] = [1];
以上两种情况都属于解构不成功，foo的值都会等于undefined。
另一种情况是不完全解构，即等号左边的模式，只匹配一部分的等号右边的数组。这种情况下，解构依然可以成功。
let [x, y] = [1, 2, 3];
x // 1
y // 2
let [a, [b], d] = [1, [2, 3], 4];
a // 1
b // 2
d // 4
上面两个例子，都属于不完全解构，但是可以成功。
如果等号的右边不是数组（或者严格地说，不是可遍历的结构，参见《Iterator》一章），那么将会报错。
// 报错
let [foo] = 1;
let [foo] = false;
let [foo] = NaN;
let [foo] = undefined;
let [foo] = null;
let [foo] = {};
上面的表达式都会报错，因为等号右边的值，要么转为对象以后不具备Iterator接口（前五个表达式），要么本身就不具备Iterator接口（最后一个表达
式）。
解构赋值不仅适用于var命令，也适用于let和const命令。
var [v1, v2, ..., vN ] = array;
let [v1, v2, ..., vN ] = array;
const [v1, v2, ..., vN ] = array;
对于Set结构，也可以使用数组的解构赋值。
let [x, y, z] = new Set(["a", "b", "c"]);
x // "a"
事实上，只要某种数据结构具有Iterator接口，都可以采用数组形式的解构赋值。
function* fibs() {
var a = 0;
var b = 1;
while (true) {
yield a;
[a, b] = [b, a + b];
}
}
var [first, second, third, fourth, fifth, sixth] = fibs();
sixth // 5
上面代码中，fibs是一个Generator函数，原生具有Iterator接口。解构赋值会依次从这个接口获取值。
3.1.2 默认值
解构赋值允许指定默认值。
var [foo = true] = [];
foo // true
[x, y = 'b'] = ['a']; // x='a', y='b'
[x, y = 'b'] = ['a', undefined]; // x='a', y='b'
注意，ES6内部使用严格相等运算符（===），判断一个位置是否有值。所以，如果一个数组成员不严格等于undefined，默认值是不会生效的。
var [x = 1] = [undefined];
x // 1
var [x = 1] = [null];
x // null
上面代码中，如果一个数组成员是null，默认值就不会生效，因为null不严格等于undefined。
如果默认值是一个表达式，那么这个表达式是惰性求值的，即只有在用到的时候，才会求值。
function f() {
console.log('aaa');
}
let [x = f()] = [1];
上面代码中，因为x能取到值，所以函数f根本不会执行。上面的代码其实等价于下面的代码。
let x;
if ([1][0] === undefined) {
x = f();
} else {
x = [1][0];
}
默认值可以引用解构赋值的其他变量，但该变量必须已经声明。
let [x = 1, y = x] = []; // x=1; y=1
let [x = 1, y = x] = [2]; // x=2; y=2
let [x = 1, y = x] = [1, 2]; // x=1; y=2
let [x = y, y = 1] = []; // ReferenceError
上面最后一个表达式之所以会报错，是因为x用到默认值y时，y还没有声明。
3.2 对象的解构赋值
解构不仅可以用于数组，还可以用于对象。
var { foo, bar } = { foo: "aaa", bar: "bbb" };
foo // "aaa"
bar // "bbb"
对象的解构与数组有一个重要的不同。数组的元素是按次序排列的，变量的取值由它的位置决定；而对象的属性没有次序，变量必须与属性同名，才
能取到正确的值。
var { bar, foo } = { foo: "aaa", bar: "bbb" };
foo // "aaa"
bar // "bbb"
var { baz } = { foo: "aaa", bar: "bbb" };
baz // undefined
上面代码的第一个例子，等号左边的两个变量的次序，与等号右边两个同名属性的次序不一致，但是对取值完全没有影响。第二个例子的变量没有对
应的同名属性，导致取不到值，最后等于undefined。
如果变量名与属性名不一致，必须写成下面这样。
var { foo: baz } = { foo: 'aaa', bar: 'bbb' };
baz // "aaa"
let obj = { first: 'hello', last: 'world' };
let { first: f, last: l } = obj;
f // 'hello'
l // 'world'
这实际上说明，对象的解构赋值是下面形式的简写（参见《对象的扩展》一章）。
var { foo: foo, bar: bar } = { foo: "aaa", bar: "bbb" };
也就是说，对象的解构赋值的内部机制，是先找到同名属性，然后再赋给对应的变量。真正被赋值的是后者，而不是前者。
var { foo: baz } = { foo: "aaa", bar: "bbb" };
baz // "aaa"
foo // error: foo is not defined
上面代码中，真正被赋值的是变量baz，而不是模式foo。
注意，采用这种写法时，变量的声明和赋值是一体的。对于let和const来说，变量不能重新声明，所以一旦赋值的变量以前声明过，就会报错。
let foo;
let {foo} = {foo: 1}; // SyntaxError: Duplicate declaration "foo"
let baz;
let {bar: baz} = {bar: 1}; // SyntaxError: Duplicate declaration "baz"
上面代码中，解构赋值的变量都会重新声明，所以报错了。不过，因为var命令允许重新声明，所以这个错误只会在使用let和const命令时出现。如果
没有第二个let命令，上面的代码就不会报错。
let foo;
({foo} = {foo: 1}); // 成功
let baz;
({bar: baz} = {bar: 1}); // 成功
上面代码中，let命令下面一行的圆括号是必须的，否则会报错。因为解析器会将起首的大括号，理解成一个代码块，而不是赋值语句。
和数组一样，解构也可以用于嵌套结构的对象。
var obj = {
p: [
'Hello',
{ y: 'World' }
]
};
var { p: [x, { y }] } = obj;
x // "Hello"
y // "World"
注意，这时p是模式，不是变量，因此不会被赋值。
var node = {
loc: {
start: {
line: 1,
column: 5
}
}
};
var { loc: { start: { line }} } = node;
line // 1
loc // error: loc is undefined
start // error: start is undefined
上面代码中，只有line是变量，loc和start都是模式，不会被赋值。
下面是嵌套赋值的例子。
let obj = {};
let arr = [];
({ foo: obj.prop, bar: arr[0] } = { foo: 123, bar: true });
obj // {prop:123}
arr // [true]
对象的解构也可以指定默认值。
var {x = 3} = {};
x // 3
var {x, y = 5} = {x: 1};
x // 1
y // 5
var {x:y = 3} = {};
y // 3
var {x:y = 3} = {x: 5};
y // 5
var { message: msg = 'Something went wrong' } = {};
msg // "Something went wrong"
默认值生效的条件是，对象的属性值严格等于undefined。
var {x = 3} = {x: undefined};
x // 3
var {x = 3} = {x: null};
x // null
上面代码中，如果x属性等于null，就不严格相等于undefined，导致默认值不会生效。
如果解构失败，变量的值等于undefined。
var {foo} = {bar: 'baz'};
foo // undefined
如果解构模式是嵌套的对象，而且子对象所在的父属性不存在，那么将会报错。
// 报错
var {foo: {bar}} = {baz: 'baz'};
上面代码中，等号左边对象的foo属性，对应一个子对象。该子对象的bar属性，解构时会报错。原因很简单，因为foo这时等于undefined，再取子属
性就会报错，请看下面的代码。
var _tmp = {baz: 'baz'};
_tmp.foo.bar // 报错
如果要将一个已经声明的变量用于解构赋值，必须非常小心。
// 错误的写法
var x;
{x} = {x: 1};
// SyntaxError: syntax error
上面代码的写法会报错，因为JavaScript引擎会将{x}理解成一个代码块，从而发生语法错误。只有不将大括号写在行首，避免JavaScript将其解释为代
码块，才能解决这个问题。
// 正确的写法
({x} = {x: 1});
上面代码将整个解构赋值语句，放在一个圆括号里面，就可以正确执行。关于圆括号与解构赋值的关系，参见下文。
解构赋值允许，等号左边的模式之中，不放置任何变量名。因此，可以写出非常古怪的赋值表达式。
({} = [true, false]);
({} = 'abc');
({} = []);
上面的表达式虽然毫无意义，但是语法是合法的，可以执行。
对象的解构赋值，可以很方便地将现有对象的方法，赋值到某个变量。
let { log, sin, cos } = Math;
上面代码将Math对象的对数、正弦、余弦三个方法，赋值到对应的变量上，使用起来就会方便很多。
由于数组本质是特殊的对象，因此可以对数组进行对象属性的解构。
var arr = [1, 2, 3];
var {0 : first, [arr.length - 1] : last} = arr;
first // 1
last // 3
上面代码对数组进行对象结构。数组arr的0键对应的值是1，[arr.length - 1]就是2键，对应的值是3。方括号这种写法，属于“属性名表达式”，参
见《对象的扩展》一章。
3.3 字符串的解构赋值
字符串也可以解构赋值。这是因为此时，字符串被转换成了一个类似数组的对象。
const [a, b, c, d, e] = 'hello';
a // "h"
b // "e"
c // "l"
d // "l"
e // "o"
类似数组的对象都有一个length属性，因此还可以对这个属性解构赋值。
let {length : len} = 'hello';
len // 5
3.4 数值和布尔值的解构赋值
解构赋值时，如果等号右边是数值和布尔值，则会先转为对象。
let {toString: s} = 123;
s === Number.prototype.toString // true
let {toString: s} = true;
s === Boolean.prototype.toString // true
上面代码中，数值和布尔值的包装对象都有toString属性，因此变量s都能取到值。
解构赋值的规则是，只要等号右边的值不是对象，就先将其转为对象。由于undefined和null无法转为对象，所以对它们进行解构赋值，都会报错。
let { prop: x } = undefined; // TypeError
let { prop: y } = null; // TypeError
3.5 函数参数的解构赋值
函数的参数也可以使用解构赋值。
function add([x, y]){
return x + y;
}
add([1, 2]); // 3
上面代码中，函数add的参数表面上是一个数组，但在传入参数的那一刻，数组参数就被解构成变量x和y。对于函数内部的代码来说，它们能感受到的
参数就是x和y。
下面是另一个例子。
[[1, 2], [3, 4]].map(([a, b]) =&gt; a + b);
// [ 3, 7 ]
函数参数的解构也可以使用默认值。
function move({x = 0, y = 0} = {}) {
return [x, y];
}
move({x: 3, y: 8}); // [3, 8]
move({x: 3}); // [3, 0]
move({}); // [0, 0]
move(); // [0, 0]
上面代码中，函数move的参数是一个对象，通过对这个对象进行解构，得到变量x和y的值。如果解构失败，x和y等于默认值。
注意，下面的写法会得到不一样的结果。
function move({x, y} = { x: 0, y: 0 }) {
return [x, y];
}
move({x: 3, y: 8}); // [3, 8]
move({x: 3}); // [3, undefined]
move({}); // [undefined, undefined]
move(); // [0, 0]
上面代码是为函数move的参数指定默认值，而不是为变量x和y指定默认值，所以会得到与前一种写法不同的结果。
undefined就会触发函数参数的默认值。
[1, undefined, 3].map((x = 'yes') =&gt; x);
// [ 1, 'yes', 3 ]
3.6 圆括号问题
解构赋值虽然很方便，但是解析起来并不容易。对于编译器来说，一个式子到底是模式，还是表达式，没有办法从一开始就知道，必须解析到（或解
析不到）等号才能知道。
由此带来的问题是，如果模式中出现圆括号怎么处理。ES6的规则是，只要有可能导致解构的歧义，就不得使用圆括号。
但是，这条规则实际上不那么容易辨别，处理起来相当麻烦。因此，建议只要有可能，就不要在模式中放置圆括号。
3.6.1 不能使用圆括号的情况
以下三种解构赋值不得使用圆括号。
（1）变量声明语句中，不能带有圆括号。
// 全部报错
var [(a)] = [1];
var {x: (c)} = {};
var ({x: c}) = {};
var {(x: c)} = {};
var {(x): c} = {};
var { o: ({ p: p }) } = { o: { p: 2 } };
上面三个语句都会报错，因为它们都是变量声明语句，模式不能使用圆括号。
（2）函数参数中，模式不能带有圆括号。
函数参数也属于变量声明，因此不能带有圆括号。
// 报错
function f([(z)]) { return z; }
（3）赋值语句中，不能将整个模式，或嵌套模式中的一层，放在圆括号之中。
// 全部报错
({ p: a }) = { p: 42 };
([a]) = [5];
上面代码将整个模式放在圆括号之中，导致报错。
// 报错
[({ p: a }), { x: c }] = [{}, {}];
上面代码将嵌套模式的一层，放在圆括号之中，导致报错。
3.6.2 可以使用圆括号的情况
可以使用圆括号的情况只有一种：赋值语句的非模式部分，可以使用圆括号。
[(b)] = [3]; // 正确
({ p: (d) } = {}); // 正确
[(parseInt.prop)] = [3]; // 正确
上面三行语句都可以正确执行，因为首先它们都是赋值语句，而不是声明语句；其次它们的圆括号都不属于模式的一部分。第一行语句中，模式是取
数组的第一个成员，跟圆括号无关；第二行语句中，模式是p，而不是d；第三行语句与第一行语句的性质一致。
3.7 用途
变量的解构赋值用途很多。
（1）交换变量的值
[x, y] = [y, x];
上面代码交换变量x和y的值，这样的写法不仅简洁，而且易读，语义非常清晰。
（2）从函数返回多个值
函数只能返回一个值，如果要返回多个值，只能将它们放在数组或对象里返回。有了解构赋值，取出这些值就非常方便。
// 返回一个数组
function example() {
return [1, 2, 3];
}
var [a, b, c] = example();
// 返回一个对象
function example() {
return {
foo: 1,
bar: 2
};
}
var { foo, bar } = example();
（3）函数参数的定义
解构赋值可以方便地将一组参数与变量名对应起来。
// 参数是一组有次序的值
function f([x, y, z]) { ... }
f([1, 2, 3]);
// 参数是一组无次序的值
function f({x, y, z}) { ... }
f({z: 3, y: 2, x: 1});
（4）提取JSON数据
解构赋值对提取JSON对象中的数据，尤其有用。
var jsonData = {
id: 42,
status: "OK",
data: [867, 5309]
};
let { id, status, data: number } = jsonData;
console.log(id, status, number);
// 42, "OK", [867, 5309]
上面代码可以快速提取JSON数据的值。
（5）函数参数的默认值
jQuery.ajax = function (url, {
async = true,
beforeSend = function () {},
cache = true,
complete = function () {},
crossDomain = false,
global = true,
// ... more config
}) {
// ... do stuff
};
指定参数的默认值，就避免了在函数体内部再写var foo = config.foo || 'default foo';这样的语句。
（6）遍历Map结构
任何部署了Iterator接口的对象，都可以用for...of循环遍历。Map结构原生支持Iterator接口，配合变量的解构赋值，获取键名和键值就非常方便。
var map = new Map();
map.set('first', 'hello');
map.set('second', 'world');
for (let [key, value] of map) {
console.log(key + " is " + value);
}
// first is hello
// second is world
如果只想获取键名，或者只想获取键值，可以写成下面这样。
// 获取键名
for (let [key] of map) {
// ...
}
// 获取键值
for (let [,value] of map) {
// ...
}
（7）输入模块的指定方法
加载模块时，往往需要指定输入那些方法。解构赋值使得输入语句非常清晰。
const { SourceMapConsumer, SourceNode } = require("source-map");
4 字符串的扩展
ES6加强了对Unicode的支持，并且扩展了字符串对象。
4.1字符的Unicode表示法
JavaScript允许采用\uxxxx形式表示一个字符，其中“xxxx”表示字符的码点。
"\u0061"
// "a"
但是，这种表示法只限于\u0000——\uFFFF之间的字符。超出这个范围的字符，必须用两个双字节的形式表达。
"\uD842\uDFB7"
// ""
"\u20BB7"
// " 7"
上面代码表示，如果直接在“\u”后面跟上超过0xFFFF的数值（比如\u20BB7），JavaScript会理解成“\u20BB+7”。由于\u20BB是一个不可打印字符，所
以只会显示一个空格，后面跟着一个7。
ES6对这一点做出了改进，只要将码点放入大括号，就能正确解读该字符。
"\u{20BB7}"
// ""
"\u{41}\u{42}\u{43}"
// "ABC"
let hello = 123;
hell\u{6F} // 123
'\u{1F680}' === '\uD83D\uDE80'
// true
上面代码中，最后一个例子表明，大括号表示法与四字节的UTF-16编码是等价的。
有了这种表示法之后，JavaScript共有6种方法可以表示一个字符。
'\z' === 'z' // true
'\172' === 'z' // true
'\x7A' === 'z' // true
'\u007A' === 'z' // true
'\u{7A}' === 'z' // true
4.2 codePointAt()
JavaScript内部，字符以UTF-16的格式储存，每个字符固定为2个字节。对于那些需要4个字节储存的字符（Unicode码点大于0xFFFF的字
符），JavaScript会认为它们是两个字符。
var s = "";
s.length // 2
s.charAt(0) // ''
s.charAt(1) // ''
s.charCodeAt(0) // 55362
s.charCodeAt(1) // 57271
上面代码中，汉字“”的码点是0x20BB7，UTF-16编码为0xD842 0xDFB7（十进制为55362 57271），需要4个字节储存。对于这种4个字节的字
符，JavaScript不能正确处理，字符串长度会误判为2，而且charAt方法无法读取整个字符，charCodeAt方法只能分别返回前两个字节和后两个字节的
值。
ES6提供了codePointAt方法，能够正确处理4个字节储存的字符，返回一个字符的码点。
var s = 'a';
s.codePointAt(0) // 134071
s.codePointAt(1) // 57271
s.charCodeAt(2) // 97
codePointAt方法的参数，是字符在字符串中的位置（从0开始）。上面代码中，JavaScript将“a”视为三个字符，codePointAt方法在第一个字符上，
正确地识别了“”，返回了它的十进制码点134071（即十六进制的20BB7）。在第二个字符（即“”的后两个字节）和第三个字
符“a”上，codePointAt方法的结果与charCodeAt方法相同。
总之，codePointAt方法会正确返回32位的UTF-16字符的码点。对于那些两个字节储存的常规字符，它的返回结果与charCodeAt方法相同。
codePointAt方法返回的是码点的十进制值，如果想要十六进制的值，可以使用toString方法转换一下。
var s = 'a';
s.codePointAt(0).toString(16) // "20bb7"
s.charCodeAt(2).toString(16) // "61"
你可能注意到了，codePointAt方法的参数，仍然是不正确的。比如，上面代码中，字符a在字符串s的正确位置序号应该是1，但是必须
向charCodeAt方法传入2。解决这个问题的一个办法是使用for...of循环，因为它会正确识别32位的UTF-16字符。
var s = 'a';
for (let ch of s) {
console.log(ch.codePointAt(0).toString(16));
}
// 20bb7
// 61
codePointAt方法是测试一个字符由两个字节还是由四个字节组成的最简单方法。
function is32Bit(c) {
return c.codePointAt(0) &gt; 0xFFFF;
}
is32Bit("") // true
is32Bit("a") // false
4.3 String.fromCodePoint()
ES5提供String.fromCharCode方法，用于从码点返回对应字符，但是这个方法不能识别32位的UTF-16字符（Unicode编号大于0xFFFF）。
String.fromCharCode(0x20BB7)
// "ஷ"
上面代码中，String.fromCharCode不能识别大于0xFFFF的码点，所以0x20BB7就发生了溢出，最高位2被舍弃了，最后返回码点U+0BB7对应的字符，
而不是码点U+20BB7对应的字符。
ES6提供了String.fromCodePoint方法，可以识别0xFFFF的字符，弥补了String.fromCharCode方法的不足。在作用上，正好与codePointAt方法相
反。
String.fromCodePoint(0x20BB7)
// ""
String.fromCodePoint(0x78, 0x1f680, 0x79) === 'x\uD83D\uDE80y'
// true
上面代码中，如果String.fromCodePoint方法有多个参数，则它们会被合并成一个字符串返回。
注意，fromCodePoint方法定义在String对象上，而codePointAt方法定义在字符串的实例对象上。
4.4 字符串的遍历器接口
ES6为字符串添加了遍历器接口（详见《Iterator》一章），使得字符串可以被for...of循环遍历。
for (let codePoint of 'foo') {
console.log(codePoint)
}
// "f"
// "o"
// "o"
除了遍历字符串，这个遍历器最大的优点是可以识别大于0xFFFF的码点，传统的for循环无法识别这样的码点。
var text = String.fromCodePoint(0x20BB7);
for (let i = 0; i &lt; text.length; i++) {
console.log(text[i]);
}
// " "
// " "
for (let i of text) {
console.log(i);
}
// ""
上面代码中，字符串text只有一个字符，但是for循环会认为它包含两个字符（都不可打印），而for...of循环会正确识别出这一个字符。
4.5 at()
ES5对字符串对象提供charAt方法，返回字符串给定位置的字符。该方法不能识别码点大于0xFFFF的字符。
'abc'.charAt(0) // "a"
''.charAt(0) // "\uD842"
上面代码中，charAt方法返回的是UTF-16编码的第一个字节，实际上是无法显示的。
目前，有一个提案，提出字符串实例的at方法，可以识别Unicode编号大于0xFFFF的字符，返回正确的字符。
'abc'.at(0) // "a"
''.at(0) // ""
这个方法可以通过垫片库实现。
4.6 normalize()
许多欧洲语言有语调符号和重音符号。为了表示它们，Unicode提供了两种方法。一种是直接提供带重音符号的字符，比如Ǒ（\u01D1）。另一种是提
供合成符号（combining character），即原字符与重音符号的合成，两个字符合成一个字符，比如O（\u004F）和ˇ（\u030C）合
成Ǒ（\u004F\u030C）。
这两种表示方法，在视觉和语义上都等价，但是JavaScript不能识别。
'\u01D1'==='\u004F\u030C' //false
'\u01D1'.length // 1
'\u004F\u030C'.length // 2
上面代码表示，JavaScript将合成字符视为两个字符，导致两种表示方法不相等。
ES6提供字符串实例的normalize()方法，用来将字符的不同表示方法统一为同样的形式，这称为Unicode正规化。
'\u01D1'.normalize() === '\u004F\u030C'.normalize()
// true
normalize方法可以接受一个参数来指定normalize的方式，参数的四个可选值如下。
NFC，默认参数，表示“标准等价合成”（Normalization Form Canonical Composition），返回多个简单字符的合成字符。所谓“标准等价”指的是视
觉和语义上的等价。
NFD，表示“标准等价分解”（Normalization Form Canonical Decomposition），即在标准等价的前提下，返回合成字符分解的多个简单字符。
NFKC，表示“兼容等价合成”（Normalization Form Compatibility Composition），返回合成字符。所谓“兼容等价”指的是语义上存在等价，但视觉
上不等价，比如“囍”和“喜喜”。（这只是用来举例，normalize方法不能识别中文。）
NFKD，表示“兼容等价分解”（Normalization Form Compatibility Decomposition），即在兼容等价的前提下，返回合成字符分解的多个简单字符。
'\u004F\u030C'.normalize('NFC').length // 1
'\u004F\u030C'.normalize('NFD').length // 2
上面代码表示，NFC参数返回字符的合成形式，NFD参数返回字符的分解形式。
不过，normalize方法目前不能识别三个或三个以上字符的合成。这种情况下，还是只能使用正则表达式，通过Unicode编号区间判断。
4.7 includes(), startsWith(), endsWith()
传统上，JavaScript只有indexOf方法，可以用来确定一个字符串是否包含在另一个字符串中。ES6又提供了三种新方法。
includes()：返回布尔值，表示是否找到了参数字符串。
startsWith()：返回布尔值，表示参数字符串是否在源字符串的头部。
endsWith()：返回布尔值，表示参数字符串是否在源字符串的尾部。
var s = 'Hello world!';
s.startsWith('Hello') // true
s.endsWith('!') // true
s.includes('o') // true
这三个方法都支持第二个参数，表示开始搜索的位置。
var s = 'Hello world!';
s.startsWith('world', 6) // true
s.endsWith('Hello', 5) // true
s.includes('Hello', 6) // false
上面代码表示，使用第二个参数n时，endsWith的行为与其他两个方法有所不同。它针对前n个字符，而其他两个方法针对从第n个位置直到字符串结
束。
4.8 repeat()
repeat方法返回一个新字符串，表示将原字符串重复n次。
'x'.repeat(3) // "xxx"
'hello'.repeat(2) // "hellohello"
'na'.repeat(0) // ""
参数如果是小数，会被取整。
'na'.repeat(2.9) // "nana"
如果repeat的参数是负数或者Infinity，会报错。
'na'.repeat(Infinity)
// RangeError
'na'.repeat(-1)
// RangeError
但是，如果参数是0到-1之间的小数，则等同于0，这是因为会先进行取整运算。0到-1之间的小数，取整以后等于-0，repeat视同为0。
'na'.repeat(-0.9) // ""
参数NaN等同于0。
'na'.repeat(NaN) // ""
如果repeat的参数是字符串，则会先转换成数字。
'na'.repeat('na') // ""
'na'.repeat('3') // "nanana"
4.9 padStart()，padEnd()
ES7推出了字符串补全长度的功能。如果某个字符串不够指定长度，会在头部或尾部补全。padStart用于头部补全，padEnd用于尾部补全。
'x'.padStart(5, 'ab') // 'ababx'
'x'.padStart(4, 'ab') // 'abax'
'x'.padEnd(5, 'ab') // 'xabab'
'x'.padEnd(4, 'ab') // 'xaba'
上面代码中，padStart和padEnd一共接受两个参数，第一个参数用来指定字符串的最小长度，第二个参数是用来补全的字符串。
如果原字符串的长度，等于或大于指定的最小长度，则返回原字符串。
'xxx'.padStart(2, 'ab') // 'xxx'
'xxx'.padEnd(2, 'ab') // 'xxx'
如果用来补全的字符串与原字符串，两者的长度之和超过了指定的最小长度，则会截去超出位数的补全字符串。
'abc'.padStart(10, '0123456789')
// '0123456abc'
如果省略第二个参数，则会用空格补全长度。
'x'.padStart(4) // ' x'
'x'.padEnd(4) // 'x '
padStart的常见用途是为数值补全指定位数。下面代码生成10位的数值字符串。
'1'.padStart(10, '0') // "0000000001"
'12'.padStart(10, '0') // "0000000012"
'123456'.padStart(10, '0') // "0000123456"
另一个用途是提示字符串格式。
'12'.padStart(10, 'YYYY-MM-DD') // "YYYY-MM-12"
'09-12'.padStart(10, 'YYYY-MM-DD') // "YYYY-09-12"
4.10 模板字符串
传统的JavaScript语言，输出模板通常是这样写的。
$('#result').append(
'There are &lt;b&gt;' + basket.count + '&lt;/b&gt; ' +
'items in your basket, ' +
'&lt;em&gt;' + basket.onSale +
'&lt;/em&gt; are on sale!'
);
上面这种写法相当繁琐不方便，ES6引入了模板字符串解决这个问题。
$('#result').append(`
There are &lt;b&gt;${basket.count}&lt;/b&gt; items
in your basket, &lt;em&gt;${basket.onSale}&lt;/em&gt;
are on sale!
`);
模板字符串（template string）是增强版的字符串，用反引号（`）标识。它可以当作普通字符串使用，也可以用来定义多行字符串，或者在字符串中
嵌入变量。
// 普通字符串
`In JavaScript '\n' is a line-feed.`
// 多行字符串
`In JavaScript this is
not legal.`
console.log(`string text line 1
string text line 2`);
// 字符串中嵌入变量
var name = "Bob", time = "today";
`Hello ${name}, how are you ${time}?`
上面代码中的模板字符串，都是用反引号表示。如果在模板字符串中需要使用反引号，则前面要用反斜杠转义。
var greeting = `\`Yo\` World!`;
如果使用模板字符串表示多行字符串，所有的空格和缩进都会被保留在输出之中。
$('#list').html(`
&lt;ul&gt;
&lt;li&gt;first&lt;/li&gt;
&lt;li&gt;second&lt;/li&gt;
&lt;/ul&gt;
`);
上面代码中，所有模板字符串的空格和换行，都是被保留的，比如&lt;ul&gt;标签前面会有一个换行。如果你不想要这个换行，可以使用trim方法消除它。
$('#list').html(`
&lt;ul&gt;
&lt;li&gt;first&lt;/li&gt;
&lt;li&gt;second&lt;/li&gt;
&lt;/ul&gt;
`.trim());
模板字符串中嵌入变量，需要将变量名写在${}之中。
function authorize(user, action) {
if (!user.hasPrivilege(action)) {
throw new Error(
// 传统写法为
// 'User '
// + user.name
// + ' is not authorized to do '
// + action
// + '.'
`User ${user.name} is not authorized to do ${action}.`);
}
}
大括号内部可以放入任意的JavaScript表达式，可以进行运算，以及引用对象属性。
var x = 1;
var y = 2;
`${x} + ${y} = ${x + y}`
// "1 + 2 = 3"
`${x} + ${y * 2} = ${x + y * 2}`
// "1 + 4 = 5"
var obj = {x: 1, y: 2};
`${obj.x + obj.y}`
// 3
模板字符串之中还能调用函数。
function fn() {
return "Hello World";
}
`foo ${fn()} bar`
// foo Hello World bar
如果大括号中的值不是字符串，将按照一般的规则转为字符串。比如，大括号中是一个对象，将默认调用对象的toString方法。
如果模板字符串中的变量没有声明，将报错。
// 变量place没有声明
var msg = `Hello, ${place}`;
// 报错
由于模板字符串的大括号内部，就是执行JavaScript代码，因此如果大括号内部是一个字符串，将会原样输出。
`Hello ${'World'}`
// "Hello World"
模板字符串甚至还能嵌套。
const tmpl = addrs =&gt; `
&lt;table&gt;
${addrs.map(addr =&gt; `
&lt;tr&gt;&lt;td&gt;${addr.first}&lt;/td&gt;&lt;/tr&gt;
&lt;tr&gt;&lt;td&gt;${addr.last}&lt;/td&gt;&lt;/tr&gt;
`).join('')}
&lt;/table&gt;
`;
上面代码中，模板字符串的变量之中，又嵌入了另一个模板字符串，使用方法如下。
const data = [
{ first: '&lt;Jane&gt;', last: 'Bond' },
{ first: 'Lars', last: '&lt;Croft&gt;' },
];
console.log(tmpl(data));
// &lt;table&gt;
//
// &lt;tr&gt;&lt;td&gt;&lt;Jane&gt;&lt;/td&gt;&lt;/tr&gt;
// &lt;tr&gt;&lt;td&gt;Bond&lt;/td&gt;&lt;/tr&gt;
//
// &lt;tr&gt;&lt;td&gt;Lars&lt;/td&gt;&lt;/tr&gt;
// &lt;tr&gt;&lt;td&gt;&lt;Croft&gt;&lt;/td&gt;&lt;/tr&gt;
//
// &lt;/table&gt;
如果需要引用模板字符串本身，在需要时执行，可以像下面这样写。
// 写法一
let str = 'return ' + '`Hello ${name}!`';
let func = new Function('name', str);
func('Jack') // "Hello Jack!"
// 写法二
let str = '(name) =&gt; `Hello ${name}!`';
let func = eval.call(null, str);
func('Jack') // "Hello Jack!"
4.11 实例：模板编译
下面，我们来看一个通过模板字符串，生成正式模板的实例。
var template = `
&lt;ul&gt;
&lt;% for(var i=0; i &lt; data.supplies.length; i++) { %&gt;
&lt;li&gt;&lt;%= data.supplies[i] %&gt;&lt;/li&gt;
&lt;% } %&gt;
&lt;/ul&gt;
`;
上面代码在模板字符串之中，放置了一个常规模板。该模板使用&lt;%...%&gt;放置JavaScript代码，使用&lt;%= ... %&gt;输出JavaScript表达式。
怎么编译这个模板字符串呢？
一种思路是将其转换为JavaScript表达式字符串。
echo('&lt;ul&gt;');
for(var i=0; i &lt; data.supplies.length; i++) {
echo('&lt;li&gt;');
echo(data.supplies[i]);
echo('&lt;/li&gt;');
};
echo('&lt;/ul&gt;');
这个转换使用正则表达式就行了。
var evalExpr = /&lt;%=(.+?)%&gt;/g;
var expr = /&lt;%([\s\S]+?)%&gt;/g;
template = template
.replace(evalExpr, '`); \n echo( $1 ); \n echo(`')
.replace(expr, '`); \n $1 \n echo(`');
template = 'echo(`' + template + '`);';
然后，将template封装在一个函数里面返回，就可以了。
var script =
`(function parse(data){
var output = "";
function echo(html){
output += html;
}
${ template }
return output;
})`;
return script;
将上面的内容拼装成一个模板编译函数compile。
function compile(template){
var evalExpr = /&lt;%=(.+?)%&gt;/g;
var expr = /&lt;%([\s\S]+?)%&gt;/g;
template = template
.replace(evalExpr, '`); \n echo( $1 ); \n echo(`')
.replace(expr, '`); \n $1 \n echo(`');
template = 'echo(`' + template + '`);';
var script =
`(function parse(data){
var output = "";
function echo(html){
output += html;
}
${ template }
return output;
})`;
return script;
}
compile函数的用法如下。
var parse = eval(compile(template));
div.innerHTML = parse({ supplies: [ "broom", "mop", "cleaner" ] });
// &lt;ul&gt;
// &lt;li&gt;broom&lt;/li&gt;
// &lt;li&gt;mop&lt;/li&gt;
// &lt;li&gt;cleaner&lt;/li&gt;
// &lt;/ul&gt;
4.12 标签模板
模板字符串的功能，不仅仅是上面这些。它可以紧跟在一个函数名后面，该函数将被调用来处理这个模板字符串。这被称为“标签模板”功能（tagged
template）。
alert`123`
// 等同于
alert(123)
标签模板其实不是模板，而是函数调用的一种特殊形式。“标签”指的就是函数，紧跟在后面的模板字符串就是它的参数。
但是，如果模板字符里面有变量，就不是简单的调用了，而是会将模板字符串先处理成多个参数，再调用函数。
var a = 5;
var b = 10;
tag`Hello ${ a + b } world ${ a * b }`;
// 等同于
tag(['Hello ', ' world ', ''], 15, 50);
上面代码中，模板字符串前面有一个标识名tag，它是一个函数。整个表达式的返回值，就是tag函数处理模板字符串后的返回值。
函数tag依次会接收到多个参数。
function tag(stringArr, value1, value2){
// ...
}
// 等同于
function tag(stringArr, ...values){
// ...
}
tag函数的第一个参数是一个数组，该数组的成员是模板字符串中那些没有变量替换的部分，也就是说，变量替换只发生在数组的第一个成员与第二个
成员之间、第二个成员与第三个成员之间，以此类推。
tag函数的其他参数，都是模板字符串各个变量被替换后的值。由于本例中，模板字符串含有两个变量，因此tag会接受到value1和value2两个参数。
tag函数所有参数的实际值如下。
第一个参数：['Hello ', ' world ', '']
第二个参数: 15
第三个参数：50
也就是说，tag函数实际上以下面的形式调用。
tag(['Hello ', ' world ', ''], 15, 50)
我们可以按照需要编写tag函数的代码。下面是tag函数的一种写法，以及运行结果。
var a = 5;
var b = 10;
function tag(s, v1, v2) {
console.log(s[0]);
console.log(s[1]);
console.log(s[2]);
console.log(v1);
console.log(v2);
return "OK";
}
tag`Hello ${ a + b } world ${ a * b}`;
// "Hello "
// " world "
// ""
// 15
// 50
// "OK"
下面是一个更复杂的例子。
var total = 30;
var msg = passthru`The total is ${total} (${total*1.05} with tax)`;
function passthru(literals) {
var result = '';
var i = 0;
while (i &lt; literals.length) {
result += literals[i++];
if (i &lt; arguments.length) {
result += arguments[i];
}
}
return result;
}
msg // "The total is 30 (31.5 with tax)"
上面这个例子展示了，如何将各个参数按照原来的位置拼合回去。
passthru函数采用rest参数的写法如下。
function passthru(literals, ...values) {
var output = "";
for (var index = 0; index &lt; values.length; index++) {
output += literals[index] + values[index];
}
output += literals[index]
return output;
}
“标签模板”的一个重要应用，就是过滤HTML字符串，防止用户输入恶意内容。
var message =
SaferHTML`&lt;p&gt;${sender} has sent you a message.&lt;/p&gt;`;
function SaferHTML(templateData) {
var s = templateData[0];
for (var i = 1; i &lt; arguments.length; i++) {
var arg = String(arguments[i]);
// Escape special characters in the substitution.
s += arg.replace(/&amp;/g, "&amp;")
.replace(/&lt;/g, "&lt;")
.replace(/&gt;/g, "&gt;");
// Don't escape special characters in the template.
s += templateData[i];
}
return s;
}
上面代码中，sender变量往往是用户提供的，经过SaferHTML函数处理，里面的特殊字符都会被转义。
var sender = '&lt;script&gt;alert("abc")&lt;/script&gt;'; // 恶意代码
var message = SaferHTML`&lt;p&gt;${sender} has sent you a message.&lt;/p&gt;`;
message
// &lt;p&gt;&lt;script&gt;alert("abc")&lt;/script&gt; has sent you a message.&lt;/p&gt;
标签模板的另一个应用，就是多语言转换（国际化处理）。
i18n`Welcome to ${siteName}, you are visitor number ${visitorNumber}!`
// "欢迎访问xxx，您是第xxxx位访问者！"
模板字符串本身并不能取代Mustache之类的模板库，因为没有条件判断和循环处理功能，但是通过标签函数，你可以自己添加这些功能。
// 下面的hashTemplate函数
// 是一个自定义的模板处理函数
var libraryHtml = hashTemplate`
&lt;ul&gt;
#for book in ${myBooks}
&lt;li&gt;&lt;i&gt;#{book.title}&lt;/i&gt; by #{book.author}&lt;/li&gt;
#end
&lt;/ul&gt;
`;
除此之外，你甚至可以使用标签模板，在JavaScript语言之中嵌入其他语言。
jsx`
&lt;div&gt;
&lt;input
ref='input'
onChange='${this.handleChange}'
defaultValue='${this.state.value}' /&gt;
${this.state.value}
&lt;/div&gt;
`
上面的代码通过jsx函数，将一个DOM字符串转为React对象。你可以在Github找到jsx函数的具体实现。
下面则是一个假想的例子，通过java函数，在JavaScript代码之中运行Java代码。
java`
class HelloWorldApp {
public static void main(String[] args) {
System.out.println(“Hello World!”); // Display the string.
}
}
`
HelloWorldApp.main();
模板处理函数的第一个参数（模板字符串数组），还有一个raw属性。
tag`First line\nSecond line`
function tag(strings) {
console.log(strings.raw[0]);
// "First line\\nSecond line"
}
上面代码中，tag函数的第一个参数strings，有一个raw属性，也指向一个数组。该数组的成员与strings数组完全一致。比如，strings数组
是["First line\nSecond line"]，那么strings.raw数组就是["First line\\nSecond line"]。两者唯一的区别，就是字符串里面的斜杠都被转义
了。比如，strings.raw数组会将\n视为\和n两个字符，而不是换行符。这是为了方便取得转义之前的原始模板而设计的。
4.13 String.raw()
ES6还为原生的String对象，提供了一个raw方法。
String.raw方法，往往用来充当模板字符串的处理函数，返回一个斜杠都被转义（即斜杠前面再加一个斜杠）的字符串，对应于替换变量后的模板字
符串。
String.raw`Hi\n${2+3}!`;
// "Hi\\n5!"
String.raw`Hi\u000A!`;
// 'Hi\\u000A!'
如果原字符串的斜杠已经转义，那么String.raw不会做任何处理。
String.raw`Hi\\n`
// "Hi\\n"
String.raw的代码基本如下。
String.raw = function (strings, ...values) {
var output = "";
for (var index = 0; index &lt; values.length; index++) {
output += strings.raw[index] + values[index];
}
output += strings.raw[index]
return output;
}
String.raw方法可以作为处理模板字符串的基本方法，它会将所有变量替换，而且对斜杠进行转义，方便下一步作为字符串来使用。
String.raw方法也可以作为正常的函数使用。这时，它的第一个参数，应该是一个具有raw属性的对象，且raw属性的值应该是一个数组。
String.raw({ raw: 'test' }, 0, 1, 2);
// 't0e1s2t'
// 等同于
String.raw({ raw: ['t','e','s','t'] }, 0, 1, 2);
5 正则的扩展
5.1 RegExp构造函数
在ES5中，RegExp构造函数的参数有两种情况。
第一种情况是，参数是字符串，这时第二个参数表示正则表达式的修饰符（flag）。
var regex = new RegExp('xyz', 'i');
// 等价于
var regex = /xyz/i;
第二种情况是，参数是一个正则表示式，这时会返回一个原有正则表达式的拷贝。
var regex = new RegExp(/xyz/i);
// 等价于
var regex = /xyz/i;
但是，ES5不允许此时使用第二个参数，添加修饰符，否则会报错。
var regex = new RegExp(/xyz/, 'i');
// Uncaught TypeError: Cannot supply flags when constructing one RegExp from another
ES6改变了这种行为。如果RegExp构造函数第一个参数是一个正则对象，那么可以使用第二个参数指定修饰符。而且，返回的正则表达式会忽略原有
的正则表达式的修饰符，只使用新指定的修饰符。
new RegExp(/abc/ig, 'i').flags
// "i"
上面代码中，原有正则对象的修饰符是ig，它会被第二个参数i覆盖。
5.2 字符串的正则方法
字符串对象共有4个方法，可以使用正则表达式：match()、replace()、search()和split()。
ES6将这4个方法，在语言内部全部调用RegExp的实例方法，从而做到所有与正则相关的方法，全都定义在RegExp对象上。
String.prototype.match 调用 RegExp.prototype[Symbol.match]
String.prototype.replace 调用 RegExp.prototype[Symbol.replace]
String.prototype.search 调用 RegExp.prototype[Symbol.search]
String.prototype.split 调用 RegExp.prototype[Symbol.split]
5.3 u修饰符
ES6对正则表达式添加了u修饰符，含义为“Unicode模式”，用来正确处理大于\uFFFF的Unicode字符。也就是说，会正确处理四个字节的UTF-16编
码。
/^\uD83D/u.test('\uD83D\uDC2A')
// false
/^\uD83D/.test('\uD83D\uDC2A')
// true
上面代码中，\uD83D\uDC2A是一个四个字节的UTF-16编码，代表一个字符。但是，ES5不支持四个字节的UTF-16编码，会将其识别为两个字符，导致
第二行代码结果为true。加了u修饰符以后，ES6就会识别其为一个字符，所以第一行代码结果为false。
一旦加上u修饰符号，就会修改下面这些正则表达式的行为。
（1）点字符
点（.）字符在正则表达式中，含义是除了换行符以外的任意单个字符。对于码点大于0xFFFF的Unicode字符，点字符不能识别，必须加上u修饰符。
var s = '';
/^.$/.test(s) // false
/^.$/u.test(s) // true
上面代码表示，如果不添加u修饰符，正则表达式就会认为字符串为两个字符，从而匹配失败。
（2）Unicode字符表示法
ES6新增了使用大括号表示Unicode字符，这种表示法在正则表达式中必须加上u修饰符，才能识别。
/\u{61}/.test('a') // false
/\u{61}/u.test('a') // true
/\u{20BB7}/u.test('') // true
上面代码表示，如果不加u修饰符，正则表达式无法识别\u{61}这种表示法，只会认为这匹配61个连续的u。
（3）量词
使用u修饰符后，所有量词都会正确识别码点大于0xFFFF的Unicode字符。
/a{2}/.test('aa') // true
/a{2}/u.test('aa') // true
/{2}/.test('') // false
/{2}/u.test('') // true
另外，只有在使用u修饰符的情况下，Unicode表达式当中的大括号才会被正确解读，否则会被解读为量词。
/^\u{3}$/.test('uuu') // true
上面代码中，由于正则表达式没有u修饰符，所以大括号被解读为量词。加上u修饰符，就会被解读为Unicode表达式。
（4）预定义模式
u修饰符也影响到预定义模式，能否正确识别码点大于0xFFFF的Unicode字符。
/^\S$/.test('') // false
/^\S$/u.test('') // true
上面代码的\S是预定义模式，匹配所有不是空格的字符。只有加了u修饰符，它才能正确匹配码点大于0xFFFF的Unicode字符。
利用这一点，可以写出一个正确返回字符串长度的函数。
function codePointLength(text) {
var result = text.match(/[\s\S]/gu);
return result ? result.length : 0;
}
var s = '';
s.length // 4
codePointLength(s) // 2
（5）i修饰符
有些Unicode字符的编码不同，但是字型很相近，比如，\u004B与\u212A都是大写的K。
/[a-z]/i.test('\u212A') // false
/[a-z]/iu.test('\u212A') // true
上面代码中，不加u修饰符，就无法识别非规范的K字符。
5.4 y修饰符
除了u修饰符，ES6还为正则表达式添加了y修饰符，叫做“粘连”（sticky）修饰符。
y修饰符的作用与g修饰符类似，也是全局匹配，后一次匹配都从上一次匹配成功的下一个位置开始。不同之处在于，g修饰符只要剩余位置中存在匹配
就可，而y修饰符确保匹配必须从剩余的第一个位置开始，这也就是“粘连”的涵义。
var s = 'aaa_aa_a';
var r1 = /a+/g;
var r2 = /a+/y;
r1.exec(s) // ["aaa"]
r2.exec(s) // ["aaa"]
r1.exec(s) // ["aa"]
r2.exec(s) // null
上面代码有两个正则表达式，一个使用g修饰符，另一个使用y修饰符。这两个正则表达式各执行了两次，第一次执行的时候，两者行为相同，剩余字
符串都是_aa_a。由于g修饰没有位置要求，所以第二次执行会返回结果，而y修饰符要求匹配必须从头部开始，所以返回null。
如果改一下正则表达式，保证每次都能头部匹配，y修饰符就会返回结果了。
var s = 'aaa_aa_a';
var r = /a+_/y;
r.exec(s) // ["aaa_"]
r.exec(s) // ["aa_"]
上面代码每次匹配，都是从剩余字符串的头部开始。
使用lastIndex属性，可以更好地说明y修饰符。
const REGEX = /a/g;
// 指定从2号位置（y）开始匹配
REGEX.lastIndex = 2;
// 匹配成功
const match = REGEX.exec('xaya');
// 在3号位置匹配成功
match.index // 3
// 下一次匹配从4号位开始
REGEX.lastIndex // 4
// 4号位开始匹配失败
REGEX.exec('xaxa') // null
上面代码中，lastIndex属性指定每次搜索的开始位置，g修饰符从这个位置开始向后搜索，直到发现匹配为止。
y修饰符同样遵守lastIndex属性，但是要求必须在lastIndex指定的位置发现匹配。
const REGEX = /a/y;
// 指定从2号位置开始匹配
REGEX.lastIndex = 2;
// 不是粘连，匹配失败
REGEX.exec('xaya') // null
// 指定从3号位置开始匹配
REGEX.lastIndex = 3;
// 3号位置是粘连，匹配成功
const match = REGEX.exec('xaxa');
match.index // 3
REGEX.lastIndex // 4
进一步说，y修饰符号隐含了头部匹配的标志^。
/b/y.exec('aba')
// null
上面代码由于不能保证头部匹配，所以返回null。y修饰符的设计本意，就是让头部匹配的标志^在全局匹配中都有效。
在split方法中使用y修饰符，原字符串必须以分隔符开头。这也意味着，只要匹配成功，数组的第一个成员肯定是空字符串。
// 没有找到匹配
'x##'.split(/#/y)
// [ 'x##' ]
// 找到两个匹配
'##x'.split(/#/y)
// [ '', '', 'x' ]
后续的分隔符只有紧跟前面的分隔符，才会被识别。
'#x#'.split(/#/y)
// [ '', 'x#' ]
'##'.split(/#/y)
// [ '', '', '' ]
下面是字符串对象的replace方法的例子。
const REGEX = /a/gy;
'aaxa'.replace(REGEX, '-') // '--xa'
上面代码中，最后一个a因为不是出现下一次匹配的头部，所以不会被替换。
单单一个y修饰符对match方法，只能返回第一个匹配，必须与g修饰符联用，才能返回所有匹配。
'a1a2a3'.match(/a\d/y) // ["a1"]
'a1a2a3'.match(/a\d/gy) // ["a1", "a2", "a3"]
y修饰符的一个应用，是从字符串提取token（词元），y修饰符确保了匹配之间不会有漏掉的字符。
const TOKEN_Y = /\s*(\+|[0-9]+)\s*/y;
const TOKEN_G = /\s*(\+|[0-9]+)\s*/g;
tokenize(TOKEN_Y, '3 + 4')
// [ '3', '+', '4' ]
tokenize(TOKEN_G, '3 + 4')
// [ '3', '+', '4' ]
function tokenize(TOKEN_REGEX, str) {
let result = [];
let match;
while (match = TOKEN_REGEX.exec(str)) {
result.push(match[1]);
}
return result;
}
上面代码中，如果字符串里面没有非法字符，y修饰符与g修饰符的提取结果是一样的。但是，一旦出现非法字符，两者的行为就不一样了。
tokenize(TOKEN_Y, '3x + 4')
// [ '3' ]
tokenize(TOKEN_G, '3x + 4')
// [ '3', '+', '4' ]
上面代码中，g修饰符会忽略非法字符，而y修饰符不会，这样就很容易发现错误。
5.5 sticky属性
与y修饰符相匹配，ES6的正则对象多了sticky属性，表示是否设置了y修饰符。
var r = /hello\d/y;
r.sticky // true
5.6 flags属性
ES6为正则表达式新增了flags属性，会返回正则表达式的修饰符。
// ES5的source属性
// 返回正则表达式的正文
/abc/ig.source
// "abc"
// ES6的flags属性
// 返回正则表达式的修饰符
/abc/ig.flags
// 'gi'
5.7 RegExp.escape()
字符串必须转义，才能作为正则模式。
function escapeRegExp(str) {
return str.replace(/[\-\[\]\/\{\}\(\)\*\+\?\.\\\^\$\|]/g, '\\$&amp;');
}
let str = '/path/to/resource.html?search=query';
escapeRegExp(str)
// "\/path\/to\/resource\.html\?search=query"
上面代码中，str是一个正常字符串，必须使用反斜杠对其中的特殊字符转义，才能用来作为一个正则匹配的模式。
已经有提议将这个需求标准化，作为RegExp对象的静态方法RegExp.escape()，放入ES7。2015年7月31日，TC39认为，这个方法有安全风险，又不
愿这个方法变得过于复杂，没有同意将其列入ES7，但这不失为一个真实的需求。
RegExp.escape('The Quick Brown Fox');
// "The Quick Brown Fox"
RegExp.escape('Buy it. use it. break it. fix it.');
// "Buy it\. use it\. break it\. fix it\."
RegExp.escape('(*.*)');
// "\(\*\.\*\)"
字符串转义以后，可以使用RegExp构造函数生成正则模式。
var str = 'hello. how are you?';
var regex = new RegExp(RegExp.escape(str), 'g');
var regex = new RegExp(RegExp.escape(str), 'g');
assert.equal(String(regex), '/hello\. how are you\?/g');
目前，该方法可以用上文的escapeRegExp函数或者垫片模块regexp.escape实现。
var escape = require('regexp.escape');
escape('hi. how are you?');
// "hi\\. how are you\\?"
5.8 后行断言
JavaScript语言的正则表达式，只支持先行断言（lookahead）和先行否定断言（negative lookahead），不支持后行断言（lookbehind）和后行否定
断言（negative lookbehind）。
目前，有一个提案，在ES7加入后行断言。V8引擎4.9版已经支持，Chrome浏览器49版打开”experimental JavaScript features“开关（地址栏键
入about:flags），就可以使用这项功能。
”先行断言“指的是，x只有在y前面才匹配，必须写成/x(?=y)/。比如，只匹配百分号之前的数字，要写成/\d+(?=%)/。”先行否定断言“指的是，x只有
不在y前面才匹配，必须写成/x(?!y)/。比如，只匹配不在百分号之前的数字，要写成/\d+(?!%)/。
/\d+(?=%)/.exec('100% of US presidents have been male') // ["100"]
/\d+(?!%)/.exec('that’s all 44 of them') // ["44"]
上面两个字符串，如果互换正则表达式，就会匹配失败。另外，还可以看到，”先行断言“括号之中的部分（(?=%)），是不计入返回结果的。
"后行断言"正好与"先行断言"相反，x只有在y后面才匹配，必须写成/(?&lt;=y)x/。比如，只匹配美元符号之后的数字，要写成/(?&lt;=\$)\d+/。”后行否定
断言“则与”先行否定断言“相反，x只有不在y后面才匹配，必须写成/(?&lt;!y)x/。比如，只匹配不在美元符号后面的数字，要写成/(?&lt;!\$)\d+/。
/(?&lt;=\$)\d+/.exec('Benjamin Franklin is on the $100 bill') // ["100"]
/(?&lt;!\$)\d+/.exec('it’s is worth about €90') // ["90"]
上面的例子中，"后行断言"的括号之中的部分（(?&lt;=\$)），也是不计入返回结果。
"后行断言"的实现，需要先匹配/(?&lt;=y)x/的x，然后再回到左边，匹配y的部分。这种"先右后左"的执行顺序，与所有其他正则操作相反，导致了一些
不符合预期的行为。
首先，”后行断言“的组匹配，与正常情况下结果是不一样的。
/(?&lt;=(\d+)(\d+))$/.exec('1053') // ["", "1", "053"]
/^(\d+)(\d+)$/.exec('1053') // ["1053", "105", "3"]
上面代码中，需要捕捉两个组匹配。没有"后行断言"时，第一个括号是贪婪模式，第二个括号只能捕获一个字符，所以结果是105和3。而"后行断
言"时，由于执行顺序是从右到左，第二个括号是贪婪模式，第一个括号只能捕获一个字符，所以结果是1和053。
其次，"后行断言"的反斜杠引用，也与通常的顺序相反，必须放在对应的那个括号之前。
/(?&lt;=(o)d\1)r/.exec('hodor') // null
/(?&lt;=\1d(o))r/.exec('hodor') // ["r", "o"]
上面代码中，如果后行断言的反斜杠引用（\1）放在括号的后面，就不会得到匹配结果，必须放在前面才可以。
6 数值的扩展
6.1 二进制和八进制表示法
ES6提供了二进制和八进制数值的新的写法，分别用前缀0b（或0B）和0o（或0O）表示。
0b111110111 === 503 // true
0o767 === 503 // true
从ES5开始，在严格模式之中，八进制就不再允许使用前缀0表示，ES6进一步明确，要使用前缀0o表示。
// 非严格模式
(function(){
console.log(0o11 === 011);
})() // true
// 严格模式
(function(){
'use strict';
console.log(0o11 === 011);
})() // Uncaught SyntaxError: Octal literals are not allowed in strict mode.
如果要将0b和0o前缀的字符串数值转为十进制，要使用Number方法。
Number('0b111') // 7
Number('0o10') // 8
6.2 Number.isFinite(), Number.isNaN()
ES6在Number对象上，新提供了Number.isFinite()和Number.isNaN()两个方法。
Number.isFinite()用来检查一个数值是否为有限的（finite）。
Number.isFinite(15); // true
Number.isFinite(0.8); // true
Number.isFinite(NaN); // false
Number.isFinite(Infinity); // false
Number.isFinite(-Infinity); // false
Number.isFinite('foo'); // false
Number.isFinite('15'); // false
Number.isFinite(true); // false
ES5可以通过下面的代码，部署Number.isFinite方法。
(function (global) {
var global_isFinite = global.isFinite;
Object.defineProperty(Number, 'isFinite', {
value: function isFinite(value) {
return typeof value === 'number' &amp;&amp; global_isFinite(value);
},
configurable: true,
enumerable: false,
writable: true
});
})(this);
Number.isNaN()用来检查一个值是否为NaN。
Number.isNaN(NaN) // true
Number.isNaN(15) // false
Number.isNaN('15') // false
Number.isNaN(true) // false
Number.isNaN(9/NaN) // true
Number.isNaN('true'/0) // true
Number.isNaN('true'/'true') // true
ES5通过下面的代码，部署Number.isNaN()。
(function (global) {
var global_isNaN = global.isNaN;
Object.defineProperty(Number, 'isNaN', {
value: function isNaN(value) {
return typeof value === 'number' &amp;&amp; global_isNaN(value);
},
configurable: true,
enumerable: false,
writable: true
});
})(this);
它们与传统的全局方法isFinite()和isNaN()的区别在于，传统方法先调用Number()将非数值的值转为数值，再进行判断，而这两个新方法只对数值有
效，非数值一律返回false。
isFinite(25) // true
isFinite("25") // true
Number.isFinite(25) // true
Number.isFinite("25") // false
isNaN(NaN) // true
isNaN("NaN") // true
Number.isNaN(NaN) // true
Number.isNaN("NaN") // false
6.3 Number.parseInt(), Number.parseFloat()
ES6将全局方法parseInt()和parseFloat()，移植到Number对象上面，行为完全保持不变。
// ES5的写法
parseInt('12.34') // 12
parseFloat('123.45#') // 123.45
// ES6的写法
Number.parseInt('12.34') // 12
Number.parseFloat('123.45#') // 123.45
这样做的目的，是逐步减少全局性方法，使得语言逐步模块化。
Number.parseInt === parseInt // true
Number.parseFloat === parseFloat // true
6.4 Number.isInteger()
Number.isInteger()用来判断一个值是否为整数。需要注意的是，在JavaScript内部，整数和浮点数是同样的储存方法，所以3和3.0被视为同一个值。
Number.isInteger(25) // true
Number.isInteger(25.0) // true
Number.isInteger(25.1) // false
Number.isInteger("15") // false
Number.isInteger(true) // false
ES5可以通过下面的代码，部署Number.isInteger()。
(function (global) {
var floor = Math.floor,
isFinite = global.isFinite;
Object.defineProperty(Number, 'isInteger', {
value: function isInteger(value) {
return typeof value === 'number' &amp;&amp; isFinite(value) &amp;&amp;
value &gt; -9007199254740992 &amp;&amp; value &lt; 9007199254740992 &amp;&amp;
floor(value) === value;
},
configurable: true,
enumerable: false,
writable: true
});
})(this);
6.5 Number.EPSILON
ES6在Number对象上面，新增一个极小的常量Number.EPSILON。
Number.EPSILON
// 2.220446049250313e-16
Number.EPSILON.toFixed(20)
// '0.00000000000000022204'
引入一个这么小的量的目的，在于为浮点数计算，设置一个误差范围。我们知道浮点数计算是不精确的。
0.1 + 0.2
// 0.30000000000000004
0.1 + 0.2 - 0.3
// 5.551115123125783e-17
5.551115123125783e-17.toFixed(20)
// '0.00000000000000005551'
但是如果这个误差能够小于Number.EPSILON，我们就可以认为得到了正确结果。
5.551115123125783e-17 &lt; Number.EPSILON
// true
因此，Number.EPSILON的实质是一个可以接受的误差范围。
function withinErrorMargin (left, right) {
return Math.abs(left - right) &lt; Number.EPSILON;
}
withinErrorMargin(0.1 + 0.2, 0.3)
// true
withinErrorMargin(0.2 + 0.2, 0.3)
// false
上面的代码为浮点数运算，部署了一个误差检查函数。
6.6 安全整数和Number.isSafeInteger()
JavaScript能够准确表示的整数范围在-2^53到2^53之间（不含两个端点），超过这个范围，无法精确表示这个值。
Math.pow(2, 53) // 9007199254740992
9007199254740992 // 9007199254740992
9007199254740993 // 9007199254740992
Math.pow(2, 53) === Math.pow(2, 53) + 1
// true
上面代码中，超出2的53次方之后，一个数就不精确了。
ES6引入了Number.MAX_SAFE_INTEGER和Number.MIN_SAFE_INTEGER这两个常量，用来表示这个范围的上下限。
Number.MAX_SAFE_INTEGER === Math.pow(2, 53) - 1
// true
Number.MAX_SAFE_INTEGER === 9007199254740991
// true
Number.MIN_SAFE_INTEGER === -Number.MAX_SAFE_INTEGER
// true
Number.MIN_SAFE_INTEGER === -9007199254740991
// true
上面代码中，可以看到JavaScript能够精确表示的极限。
Number.isSafeInteger()则是用来判断一个整数是否落在这个范围之内。
Number.isSafeInteger('a') // false
Number.isSafeInteger(null) // false
Number.isSafeInteger(NaN) // false
Number.isSafeInteger(Infinity) // false
Number.isSafeInteger(-Infinity) // false
Number.isSafeInteger(3) // true
Number.isSafeInteger(1.2) // false
Number.isSafeInteger(9007199254740990) // true
Number.isSafeInteger(9007199254740992) // false
Number.isSafeInteger(Number.MIN_SAFE_INTEGER - 1) // false
Number.isSafeInteger(Number.MIN_SAFE_INTEGER) // true
Number.isSafeInteger(Number.MAX_SAFE_INTEGER) // true
Number.isSafeInteger(Number.MAX_SAFE_INTEGER + 1) // false
这个函数的实现很简单，就是跟安全整数的两个边界值比较一下。
Number.isSafeInteger = function (n) {
return (typeof n === 'number' &amp;&amp;
Math.round(n) === n &amp;&amp;
Number.MIN_SAFE_INTEGER &lt;= n &amp;&amp;
n &lt;= Number.MAX_SAFE_INTEGER);
}
实际使用这个函数时，需要注意。验证运算结果是否落在安全整数的范围内，不要只验证运算结果，而要同时验证参与运算的每个值。
Number.isSafeInteger(9007199254740993)
// false
Number.isSafeInteger(990)
// true
Number.isSafeInteger(9007199254740993 - 990)
// true
9007199254740993 - 990
// 返回结果 9007199254740002
// 正确答案应该是 9007199254740003
上面代码中，9007199254740993不是一个安全整数，但是Number.isSafeInteger会返回结果，显示计算结果是安全的。这是因为，这个数超出了精度
范围，导致在计算机内部，以9007199254740992的形式储存。
9007199254740993 === 9007199254740992
// true
所以，如果只验证运算结果是否为安全整数，很可能得到错误结果。下面的函数可以同时验证两个运算数和运算结果。
function trusty (left, right, result) {
if (
Number.isSafeInteger(left) &amp;&amp;
Number.isSafeInteger(right) &amp;&amp;
Number.isSafeInteger(result)
) {
return result;
}
throw new RangeError('Operation cannot be trusted!');
}
trusty(9007199254740993, 990, 9007199254740993 - 990)
// RangeError: Operation cannot be trusted!
trusty(1, 2, 3)
// 3
6.7 Math对象的扩展
ES6在Math对象上新增了17个与数学相关的方法。所有这些方法都是静态方法，只能在Math对象上调用。
Math.trunc()
Math.trunc方法用于去除一个数的小数部分，返回整数部分。
Math.trunc(4.1) // 4
Math.trunc(4.9) // 4
Math.trunc(-4.1) // -4
Math.trunc(-4.9) // -4
Math.trunc(-0.1234) // -0
对于非数值，Math.trunc内部使用Number方法将其先转为数值。
Math.trunc('123.456')
// 123
对于空值和无法截取整数的值，返回NaN。
Math.trunc(NaN); // NaN
Math.trunc('foo'); // NaN
Math.trunc(); // NaN
对于没有部署这个方法的环境，可以用下面的代码模拟。
Math.trunc = Math.trunc || function(x) {
return x &lt; 0 ? Math.ceil(x) : Math.floor(x);
};
6.7.1 Math.sign()
Math.sign方法用来判断一个数到底是正数、负数、还是零。
它会返回五种值。
参数为正数，返回+1；
参数为负数，返回-1；
参数为0，返回0；
参数为-0，返回-0;
其他值，返回NaN。
Math.sign(-5) // -1
Math.sign(5) // +1
Math.sign(0) // +0
Math.sign(-0) // -0
Math.sign(NaN) // NaN
Math.sign('foo'); // NaN
Math.sign(); // NaN
对于没有部署这个方法的环境，可以用下面的代码模拟。
Math.sign = Math.sign || function(x) {
x = +x; // convert to a number
if (x === 0 || isNaN(x)) {
return x;
}
return x &gt; 0 ? 1 : -1;
};
6.7.2 Math.cbrt()
Math.cbrt方法用于计算一个数的立方根。
Math.cbrt(-1) // -1
Math.cbrt(0) // 0
Math.cbrt(1) // 1
Math.cbrt(2) // 1.2599210498948734
对于非数值，Math.cbrt方法内部也是先使用Number方法将其转为数值。
Math.cbrt('8') // 2
Math.cbrt('hello') // NaN
对于没有部署这个方法的环境，可以用下面的代码模拟。
Math.cbrt = Math.cbrt || function(x) {
var y = Math.pow(Math.abs(x), 1/3);
return x &lt; 0 ? -y : y;
};
6.7.3 Math.clz32()
JavaScript的整数使用32位二进制形式表示，Math.clz32方法返回一个数的32位无符号整数形式有多少个前导0。
Math.clz32(0) // 32
Math.clz32(1) // 31
Math.clz32(1000) // 22
Math.clz32(0b01000000000000000000000000000000) // 1
Math.clz32(0b00100000000000000000000000000000) // 2
上面代码中，0的二进制形式全为0，所以有32个前导0；1的二进制形式是0b1，只占1位，所以32位之中有31个前导0；1000的二进制形式
是0b1111101000，一共有10位，所以32位之中有22个前导0。
clz32这个函数名就来自”count leading zero bits in 32-bit binary representations of a number“（计算32位整数的前导0）的缩写。
左移运算符（&lt;&lt;）与Math.clz32方法直接相关。
Math.clz32(0) // 32
Math.clz32(1) // 31
Math.clz32(1 &lt;&lt; 1) // 30
Math.clz32(1 &lt;&lt; 2) // 29
Math.clz32(1 &lt;&lt; 29) // 2
对于小数，Math.clz32方法只考虑整数部分。
Math.clz32(3.2) // 30
Math.clz32(3.9) // 30
对于空值或其他类型的值，Math.clz32方法会将它们先转为数值，然后再计算。
Math.clz32() // 32
Math.clz32(NaN) // 32
Math.clz32(Infinity) // 32
Math.clz32(null) // 32
Math.clz32('foo') // 32
Math.clz32([]) // 32
Math.clz32({}) // 32
Math.clz32(true) // 31
6.7.4 Math.imul()
Math.imul方法返回两个数以32位带符号整数形式相乘的结果，返回的也是一个32位的带符号整数。
Math.imul(2, 4) // 8
Math.imul(-1, 8) // -8
Math.imul(-2, -2) // 4
如果只考虑最后32位，大多数情况下，Math.imul(a, b)与a * b的结果是相同的，即该方法等同于(a * b)|0的效果（超过32位的部分溢出）。之所
以需要部署这个方法，是因为JavaScript有精度限制，超过2的53次方的值无法精确表示。这就是说，对于那些很大的数的乘法，低位数值往往都是不
精确的，Math.imul方法可以返回正确的低位数值。
(0x7fffffff * 0x7fffffff)|0 // 0
上面这个乘法算式，返回结果为0。但是由于这两个二进制数的最低位都是1，所以这个结果肯定是不正确的，因为根据二进制乘法，计算结果的二进
制最低位应该也是1。这个错误就是因为它们的乘积超过了2的53次方，JavaScript无法保存额外的精度，就把低位的值都变成了0。Math.imul方法可
以返回正确的值1。
Math.imul(0x7fffffff, 0x7fffffff) // 1
6.7.5 Math.fround()
Math.fround方法返回一个数的单精度浮点数形式。
Math.fround(0) // 0
Math.fround(1) // 1
Math.fround(1.337) // 1.3370000123977661
Math.fround(1.5) // 1.5
Math.fround(NaN) // NaN
对于整数来说，Math.fround方法返回结果不会有任何不同，区别主要是那些无法用64个二进制位精确表示的小数。这时，Math.fround方法会返回最
接近这个小数的单精度浮点数。
对于没有部署这个方法的环境，可以用下面的代码模拟。
Math.fround = Math.fround || function(x) {
return new Float32Array([x])[0];
};
6.7.6 Math.hypot()
Math.hypot方法返回所有参数的平方和的平方根。
Math.hypot(3, 4); // 5
Math.hypot(3, 4, 5); // 7.0710678118654755
Math.hypot(); // 0
Math.hypot(NaN); // NaN
Math.hypot(3, 4, 'foo'); // NaN
Math.hypot(3, 4, '5'); // 7.0710678118654755
Math.hypot(-3); // 3
上面代码中，3的平方加上4的平方，等于5的平方。
如果参数不是数值，Math.hypot方法会将其转为数值。只要有一个参数无法转为数值，就会返回NaN。
6.7.7 对数方法
ES6新增了4个对数相关方法。
（1） Math.expm1()
Math.expm1(x)返回e
x
- 1，即Math.exp(x) - 1。
Math.expm1(-1) // -0.6321205588285577
Math.expm1(0) // 0
Math.expm1(1) // 1.718281828459045
对于没有部署这个方法的环境，可以用下面的代码模拟。
Math.expm1 = Math.expm1 || function(x) {
return Math.exp(x) - 1;
};
（2）Math.log1p()
Math.log1p(x)方法返回1 + x的自然对数，即Math.log(1 + x)。如果x小于-1，返回NaN。
Math.log1p(1) // 0.6931471805599453
Math.log1p(0) // 0
Math.log1p(-1) // -Infinity
Math.log1p(-2) // NaN
对于没有部署这个方法的环境，可以用下面的代码模拟。
Math.log1p = Math.log1p || function(x) {
return Math.log(1 + x);
};
（3）Math.log10()
Math.log10(x)返回以10为底的x的对数。如果x小于0，则返回NaN。
Math.log10(2) // 0.3010299956639812
Math.log10(1) // 0
Math.log10(0) // -Infinity
Math.log10(-2) // NaN
Math.log10(100000) // 5
对于没有部署这个方法的环境，可以用下面的代码模拟。
Math.log10 = Math.log10 || function(x) {
return Math.log(x) / Math.LN10;
};
（4）Math.log2()
Math.log2(x)返回以2为底的x的对数。如果x小于0，则返回NaN。
Math.log2(3) // 1.584962500721156
Math.log2(2) // 1
Math.log2(1) // 0
Math.log2(0) // -Infinity
Math.log2(-2) // NaN
Math.log2(1024) // 10
Math.log2(1 &lt;&lt; 29) // 29
对于没有部署这个方法的环境，可以用下面的代码模拟。
Math.log2 = Math.log2 || function(x) {
return Math.log(x) / Math.LN2;
};
6.7.8 三角函数方法
ES6新增了6个三角函数方法。
Math.sinh(x) 返回x的双曲正弦（hyperbolic sine）
Math.cosh(x) 返回x的双曲余弦（hyperbolic cosine）
Math.tanh(x) 返回x的双曲正切（hyperbolic tangent）
Math.asinh(x) 返回x的反双曲正弦（inverse hyperbolic sine）
Math.acosh(x) 返回x的反双曲余弦（inverse hyperbolic cosine）
Math.atanh(x) 返回x的反双曲正切（inverse hyperbolic tangent）
6.8 指数运算符
ES7新增了一个指数运算符（**），目前Babel转码器已经支持。
2 ** 2 // 4
2 ** 3 // 8
指数运算符可以与等号结合，形成一个新的赋值运算符（**=）。
let a = 2;
a **= 2;
// 等同于 a = a * a;
let b = 3;
b **= 3;
// 等同于 b = b * b * b;
7 数组的扩展
7.1 Array.from()
Array.from方法用于将两类对象转为真正的数组：类似数组的对象（array-like object）和可遍历（iterable）的对象（包括ES6新增的数据结构Set和
Map）。
下面是一个类似数组的对象，Array.from将它转为真正的数组。
let arrayLike = {
'0': 'a',
'1': 'b',
'2': 'c',
length: 3
};
// ES5的写法
var arr1 = [].slice.call(arrayLike); // ['a', 'b', 'c']
// ES6的写法
let arr2 = Array.from(arrayLike); // ['a', 'b', 'c']
实际应用中，常见的类似数组的对象是DOM操作返回的NodeList集合，以及函数内部的arguments对象。Array.from都可以将它们转为真正的数组。
// NodeList对象
let ps = document.querySelectorAll('p');
Array.from(ps).forEach(function (p) {
console.log(p);
});
// arguments对象
function foo() {
var args = Array.from(arguments);
// ...
}
上面代码中，querySelectorAll方法返回的是一个类似数组的对象，只有将这个对象转为真正的数组，才能使用forEach方法。
只要是部署了Iterator接口的数据结构，Array.from都能将其转为数组。
Array.from('hello')
// ['h', 'e', 'l', 'l', 'o']
let namesSet = new Set(['a', 'b'])
Array.from(namesSet) // ['a', 'b']
上面代码中，字符串和Set结构都具有Iterator接口，因此可以被Array.from转为真正的数组。
如果参数是一个真正的数组，Array.from会返回一个一模一样的新数组。
Array.from([1, 2, 3])
// [1, 2, 3]
值得提醒的是，扩展运算符（...）也可以将某些数据结构转为数组。
// arguments对象
function foo() {
var args = [...arguments];
}
// NodeList对象
[...document.querySelectorAll('div')]
扩展运算符背后调用的是遍历器接口（Symbol.iterator），如果一个对象没有部署这个接口，就无法转换。Array.from方法则是还支持类似数组的对
象。所谓类似数组的对象，本质特征只有一点，即必须有length属性。因此，任何有length属性的对象，都可以通过Array.from方法转为数组，而此
时扩展运算符就无法转换。
Array.from({ length: 3 });
// [ undefined, undefined, undefined ]
上面代码中，Array.from返回了一个具有三个成员的数组，每个位置的值都是undefined。扩展运算符转换不了这个对象。
对于还没有部署该方法的浏览器，可以用Array.prototype.slice方法替代。
const toArray = (() =&gt;
Array.from ? Array.from : obj =&gt; [].slice.call(obj)
)();
Array.from还可以接受第二个参数，作用类似于数组的map方法，用来对每个元素进行处理，将处理后的值放入返回的数组。
Array.from(arrayLike, x =&gt; x * x);
// 等同于
Array.from(arrayLike).map(x =&gt; x * x);
Array.from([1, 2, 3], (x) =&gt; x * x)
// [1, 4, 9]
下面的例子是取出一组DOM节点的文本内容。
let spans = document.querySelectorAll('span.name');
// map()
let names1 = Array.prototype.map.call(spans, s =&gt; s.textContent);
// Array.from()
let names2 = Array.from(spans, s =&gt; s.textContent)
下面的例子将数组中布尔值为false的成员转为0。
Array.from([1, , 2, , 3], (n) =&gt; n || 0)
// [1, 0, 2, 0, 3]
另一个例子是返回各种数据的类型。
function typesOf () {
return Array.from(arguments, value =&gt; typeof value)
}
typesOf(null, [], NaN)
// ['object', 'object', 'number']
如果map函数里面用到了this关键字，还可以传入Array.from的第三个参数，用来绑定this。
Array.from()可以将各种值转为真正的数组，并且还提供map功能。这实际上意味着，只要有一个原始的数据结构，你就可以先对它的值进行处理，然
后转成规范的数组结构，进而就可以使用数量众多的数组方法。
Array.from({ length: 2 }, () =&gt; 'jack')
// ['jack', 'jack']
上面代码中，Array.from的第一个参数指定了第二个参数运行的次数。这种特性可以让该方法的用法变得非常灵活。
Array.from()的另一个应用是，将字符串转为数组，然后返回字符串的长度。因为它能正确处理各种Unicode字符，可以避免JavaScript将大
于\uFFFF的Unicode字符，算作两个字符的bug。
function countSymbols(string) {
return Array.from(string).length;
}
7.2 Array.of()
Array.of方法用于将一组值，转换为数组。
Array.of(3, 11, 8) // [3,11,8]
Array.of(3) // [3]
Array.of(3).length // 1
这个方法的主要目的，是弥补数组构造函数Array()的不足。因为参数个数的不同，会导致Array()的行为有差异。
Array() // []
Array(3) // [, , ,]
Array(3, 11, 8) // [3, 11, 8]
上面代码中，Array方法没有参数、一个参数、三个参数时，返回结果都不一样。只有当参数个数不少于2个时，Array()才会返回由参数组成的新数
组。参数个数只有一个时，实际上是指定数组的长度。
Array.of基本上可以用来替代Array()或new Array()，并且不存在由于参数不同而导致的重载。它的行为非常统一。
Array.of() // []
Array.of(undefined) // [undefined]
Array.of(1) // [1]
Array.of(1, 2) // [1, 2]
Array.of总是返回参数值组成的数组。如果没有参数，就返回一个空数组。
Array.of方法可以用下面的代码模拟实现。
function ArrayOf(){
return [].slice.call(arguments);
}
7.3 数组实例的copyWithin()
数组实例的copyWithin方法，在当前数组内部，将指定位置的成员复制到其他位置（会覆盖原有成员），然后返回当前数组。也就是说，使用这个方
法，会修改当前数组。
Array.prototype.copyWithin(target, start = 0, end = this.length)
它接受三个参数。
target（必需）：从该位置开始替换数据。
start（可选）：从该位置开始读取数据，默认为0。如果为负值，表示倒数。
end（可选）：到该位置前停止读取数据，默认等于数组长度。如果为负值，表示倒数。
这三个参数都应该是数值，如果不是，会自动转为数值。
[1, 2, 3, 4, 5].copyWithin(0, 3)
// [4, 5, 3, 4, 5]
上面代码表示将从3号位直到数组结束的成员（4和5），复制到从0号位开始的位置，结果覆盖了原来的1和2。
下面是更多例子。
// 将3号位复制到0号位
[1, 2, 3, 4, 5].copyWithin(0, 3, 4)
// [4, 2, 3, 4, 5]
// -2相当于3号位，-1相当于4号位
[1, 2, 3, 4, 5].copyWithin(0, -2, -1)
// [4, 2, 3, 4, 5]
// 将3号位复制到0号位
[].copyWithin.call({length: 5, 3: 1}, 0, 3)
// {0: 1, 3: 1, length: 5}
// 将2号位到数组结束，复制到0号位
var i32a = new Int32Array([1, 2, 3, 4, 5]);
i32a.copyWithin(0, 2);
// Int32Array [3, 4, 5, 4, 5]
// 对于没有部署TypedArray的copyWithin方法的平台
// 需要采用下面的写法
[].copyWithin.call(new Int32Array([1, 2, 3, 4, 5]), 0, 3, 4);
// Int32Array [4, 2, 3, 4, 5]
7.4 数组实例的find()和findIndex()
数组实例的find方法，用于找出第一个符合条件的数组成员。它的参数是一个回调函数，所有数组成员依次执行该回调函数，直到找出第一个返回值
为true的成员，然后返回该成员。如果没有符合条件的成员，则返回undefined。
[1, 4, -5, 10].find((n) =&gt; n &lt; 0)
// -5
上面代码找出数组中第一个小于0的成员。
[1, 5, 10, 15].find(function(value, index, arr) {
return value &gt; 9;
}) // 10
上面代码中，find方法的回调函数可以接受三个参数，依次为当前的值、当前的位置和原数组。
数组实例的findIndex方法的用法与find方法非常类似，返回第一个符合条件的数组成员的位置，如果所有成员都不符合条件，则返回-1。
[1, 5, 10, 15].findIndex(function(value, index, arr) {
return value &gt; 9;
}) // 2
这两个方法都可以接受第二个参数，用来绑定回调函数的this对象。
另外，这两个方法都可以发现NaN，弥补了数组的IndexOf方法的不足。
[NaN].indexOf(NaN)
// -1
[NaN].findIndex(y =&gt; Object.is(NaN, y))
// 0
上面代码中，indexOf方法无法识别数组的NaN成员，但是findIndex方法可以借助Object.is方法做到。
7.5 数组实例的fill()
fill方法使用给定值，填充一个数组。
['a', 'b', 'c'].fill(7)
// [7, 7, 7]
new Array(3).fill(7)
// [7, 7, 7]
上面代码表明，fill方法用于空数组的初始化非常方便。数组中已有的元素，会被全部抹去。
fill方法还可以接受第二个和第三个参数，用于指定填充的起始位置和结束位置。
['a', 'b', 'c'].fill(7, 1, 2)
// ['a', 7, 'c']
上面代码表示，fill方法从1号位开始，向原数组填充7，到2号位之前结束。
7.6 数组实例的entries()，keys()和values()
ES6提供三个新的方法——entries()，keys()和values()——用于遍历数组。它们都返回一个遍历器对象（详见《Iterator》一章），可以
用for...of循环进行遍历，唯一的区别是keys()是对键名的遍历、values()是对键值的遍历，entries()是对键值对的遍历。
for (let index of ['a', 'b'].keys()) {
console.log(index);
}
// 0
// 1
for (let elem of ['a', 'b'].values()) {
console.log(elem);
}
// 'a'
// 'b'
for (let [index, elem] of ['a', 'b'].entries()) {
console.log(index, elem);
}
// 0 "a"
// 1 "b"
如果不使用for...of循环，可以手动调用遍历器对象的next方法，进行遍历。
let letter = ['a', 'b', 'c'];
let entries = letter.entries();
console.log(entries.next().value); // [0, 'a']
console.log(entries.next().value); // [1, 'b']
console.log(entries.next().value); // [2, 'c']
7.7 数组实例的includes()
Array.prototype.includes方法返回一个布尔值，表示某个数组是否包含给定的值，与字符串的includes方法类似。该方法属于ES7，但Babel转码器
已经支持。
[1, 2, 3].includes(2); // true
[1, 2, 3].includes(4); // false
[1, 2, NaN].includes(NaN); // true
该方法的第二个参数表示搜索的起始位置，默认为0。如果第二个参数为负数，则表示倒数的位置，如果这时它大于数组长度（比如第二个参数为-4，
但数组长度为3），则会重置为从0开始。
[1, 2, 3].includes(3, 3); // false
[1, 2, 3].includes(3, -1); // true
没有该方法之前，我们通常使用数组的indexOf方法，检查是否包含某个值。
if (arr.indexOf(el) !== -1) {
// ...
}
indexOf方法有两个缺点，一是不够语义化，它的含义是找到参数值的第一个出现位置，所以要去比较是否不等于-1，表达起来不够直观。二是，它内
部使用严格相当运算符（===）进行判断，这会导致对NaN的误判。
[NaN].indexOf(NaN)
// -1
includes使用的是不一样的判断算法，就没有这个问题。
[NaN].includes(NaN)
// true
下面代码用来检查当前环境是否支持该方法，如果不支持，部署一个简易的替代版本。
const contains = (() =&gt;
Array.prototype.includes
? (arr, value) =&gt; arr.includes(value)
: (arr, value) =&gt; arr.some(el =&gt; el === value)
)();
contains(["foo", "bar"], "baz"); // =&gt; false
另外，Map和Set数据结构有一个has方法，需要注意与includes区分。
Map结构的has方法，是用来查找键名的，比
如Map.prototype.has(key)、WeakMap.prototype.has(key)、Reflect.has(target, propertyKey)。
Set结构的has方法，是用来查找值的，比如Set.prototype.has(value)、WeakSet.prototype.has(value)。
7.8 数组的空位
数组的空位指，数组的某一个位置没有任何值。比如，Array构造函数返回的数组都是空位。
Array(3) // [, , ,]
上面代码中，Array(3)返回一个具有3个空位的数组。
注意，空位不是undefined，一个位置的值等于undefined，依然是有值的。空位是没有任何值，in运算符可以说明这一点。
0 in [undefined, undefined, undefined] // true
0 in [, , ,] // false
上面代码说明，第一个数组的0号位置是有值的，第二个数组的0号位置没有值。
ES5对空位的处理，已经很不一致了，大多数情况下会忽略空位。
forEach(), filter(), every() 和some()都会跳过空位。
map()会跳过空位，但会保留这个值
join()和toString()会将空位视为undefined，而undefined和null会被处理成空字符串。
// forEach方法
[,'a'].forEach((x,i) =&gt; console.log(i)); // 1
// filter方法
['a',,'b'].filter(x =&gt; true) // ['a','b']
// every方法
[,'a'].every(x =&gt; x==='a') // true
// some方法
[,'a'].some(x =&gt; x !== 'a') // false
// map方法
[,'a'].map(x =&gt; 1) // [,1]
// join方法
[,'a',undefined,null].join('#') // "#a##"
// toString方法
[,'a',undefined,null].toString() // ",a,,"
ES6则是明确将空位转为undefined。
Array.from方法会将数组的空位，转为undefined，也就是说，这个方法不会忽略空位。
Array.from(['a',,'b'])
// [ "a", undefined, "b" ]
扩展运算符（...）也会将空位转为undefined。
[...['a',,'b']]
// [ "a", undefined, "b" ]
copyWithin()会连空位一起拷贝。
[,'a','b',,].copyWithin(2,0) // [,"a",,"a"]
fill()会将空位视为正常的数组位置。
new Array(3).fill('a') // ["a","a","a"]
for...of循环也会遍历空位。
let arr = [, ,];
for (let i of arr) {
console.log(1);
}
// 1
// 1
上面代码中，数组arr有两个空位，for...of并没有忽略它们。如果改成map方法遍历，空位是会跳过的。
entries()、keys()、values()、find()和findIndex()会将空位处理成undefined。
// entries()
[...[,'a'].entries()] // [[0,undefined], [1,"a"]]
// keys()
[...[,'a'].keys()] // [0,1]
// values()
[...[,'a'].values()] // [undefined,"a"]
// find()
[,'a'].find(x =&gt; true) // undefined
// findIndex()
[,'a'].findIndex(x =&gt; true) // 0
由于空位的处理规则非常不统一，所以建议避免出现空位。
8 函数的扩展
8.1 函数参数的默认值
8.1.1 基本用法
在ES6之前，不能直接为函数的参数指定默认值，只能采用变通的方法。
function log(x, y) {
y = y || 'World';
console.log(x, y);
}
log('Hello') // Hello World
log('Hello', 'China') // Hello China
log('Hello', '') // Hello World
上面代码检查函数log的参数y有没有赋值，如果没有，则指定默认值为World。这种写法的缺点在于，如果参数y赋值了，但是对应的布尔值
为false，则该赋值不起作用。就像上面代码的最后一行，参数y等于空字符，结果被改为默认值。
为了避免这个问题，通常需要先判断一下参数y是否被赋值，如果没有，再等于默认值。
if (typeof y === 'undefined') {
y = 'World';
}
ES6允许为函数的参数设置默认值，即直接写在参数定义的后面。
function log(x, y = 'World') {
console.log(x, y);
}
log('Hello') // Hello World
log('Hello', 'China') // Hello China
log('Hello', '') // Hello
可以看到，ES6的写法比ES5简洁许多，而且非常自然。下面是另一个例子。
function Point(x = 0, y = 0) {
this.x = x;
this.y = y;
}
var p = new Point();
p // { x: 0, y: 0 }
除了简洁，ES6的写法还有两个好处：首先，阅读代码的人，可以立刻意识到哪些参数是可以省略的，不用查看函数体或文档；其次，有利于将来的代
码优化，即使未来的版本在对外接口中，彻底拿掉这个参数，也不会导致以前的代码无法运行。
参数变量是默认声明的，所以不能用let或const再次声明。
function foo(x = 5) {
let x = 1; // error
const x = 2; // error
}
上面代码中，参数变量x是默认声明的，在函数体中，不能用let或const再次声明，否则会报错。
8.1.2 与解构赋值默认值结合使用
参数默认值可以与解构赋值的默认值，结合起来使用。
function foo({x, y = 5}) {
console.log(x, y);
}
foo({}) // undefined, 5
foo({x: 1}) // 1, 5
foo({x: 1, y: 2}) // 1, 2
foo() // TypeError: Cannot read property 'x' of undefined
上面代码使用了对象的解构赋值默认值，而没有使用函数参数的默认值。只有当函数foo的参数是一个对象时，变量x和y才会通过解构赋值而生成。如
果函数foo调用时参数不是对象，变量x和y就不会生成，从而报错。如果参数对象没有y属性，y的默认值5才会生效。
下面是另一个对象的解构赋值默认值的例子。
function fetch(url, { body = '', method = 'GET', headers = {} }) {
console.log(method);
}
fetch('http://example.com', {})
// "GET"
fetch('http://example.com')
// 报错
上面代码中，如果函数fetch的第二个参数是一个对象，就可以为它的三个属性设置默认值。
上面的写法不能省略第二个参数，如果结合函数参数的默认值，就可以省略第二个参数。这时，就出现了双重默认值。
function fetch(url, { method = 'GET' } = {}) {
console.log(method);
}
fetch('http://example.com')
// "GET"
上面代码中，函数fetch没有第二个参数时，函数参数的默认值就会生效，然后才是解构赋值的默认值生效，变量method才会取到默认值GET。
再请问下面两种写法有什么差别？
// 写法一
function m1({x = 0, y = 0} = {}) {
return [x, y];
}
// 写法二
function m2({x, y} = { x: 0, y: 0 }) {
return [x, y];
}
上面两种写法都对函数的参数设定了默认值，区别是写法一函数参数的默认值是空对象，但是设置了对象解构赋值的默认值；写法二函数参数的默认
值是一个有具体属性的对象，但是没有设置对象解构赋值的默认值。
// 函数没有参数的情况
m1() // [0, 0]
m2() // [0, 0]
// x和y都有值的情况
m1({x: 3, y: 8}) // [3, 8]
m2({x: 3, y: 8}) // [3, 8]
// x有值，y无值的情况
m1({x: 3}) // [3, 0]
m2({x: 3}) // [3, undefined]
// x和y都无值的情况
m1({}) // [0, 0];
m2({}) // [undefined, undefined]
m1({z: 3}) // [0, 0]
m2({z: 3}) // [undefined, undefined]
8.1.3 参数默认值的位置
通常情况下，定义了默认值的参数，应该是函数的尾参数。因为这样比较容易看出来，到底省略了哪些参数。如果非尾部的参数设置默认值，实际上
这个参数是没法省略的。
// 例一
function f(x = 1, y) {
return [x, y];
}
f() // [1, undefined]
f(2) // [2, undefined])
f(, 1) // 报错
f(undefined, 1) // [1, 1]
// 例二
function f(x, y = 5, z) {
return [x, y, z];
}
f() // [undefined, 5, undefined]
f(1) // [1, 5, undefined]
f(1, ,2) // 报错
f(1, undefined, 2) // [1, 5, 2]
上面代码中，有默认值的参数都不是尾参数。这时，无法只省略该参数，而不省略它后面的参数，除非显式输入undefined。
如果传入undefined，将触发该参数等于默认值，null则没有这个效果。
function foo(x = 5, y = 6) {
console.log(x, y);
}
foo(undefined, null)
// 5 null
上面代码中，x参数对应undefined，结果触发了默认值，y参数等于null，就没有触发默认值。
8.1.4 函数的length属性
指定了默认值以后，函数的length属性，将返回没有指定默认值的参数个数。也就是说，指定了默认值后，length属性将失真。
(function (a) {}).length // 1
(function (a) {}).length // 1
(function (a = 5) {}).length // 0
(function (a, b, c = 5) {}).length // 2
上面代码中，length属性的返回值，等于函数的参数个数减去指定了默认值的参数个数。比如，上面最后一个函数，定义了3个参数，其中有一个参
数c指定了默认值，因此length属性等于3减去1，最后得到2。
这是因为length属性的含义是，该函数预期传入的参数个数。某个参数指定默认值以后，预期传入的参数个数就不包括这个参数了。同理，rest参数也
不会计入length属性。
(function(...args) {}).length // 0
如果设置了默认值的参数不是尾参数，那么length属性也不再计入后面的参数了。
(function (a = 0, b, c) {}).length // 0
(function (a, b = 1, c) {}).length // 1
8.1.5 作用域
一个需要注意的地方是，如果参数默认值是一个变量，则该变量所处的作用域，与其他变量的作用域规则是一样的，即先是当前函数的作用域，然后
才是全局作用域。
var x = 1;
function f(x, y = x) {
console.log(y);
}
f(2) // 2
上面代码中，参数y的默认值等于x。调用时，由于函数作用域内部的变量x已经生成，所以y等于参数x，而不是全局变量x。
如果调用时，函数作用域内部的变量x没有生成，结果就会不一样。
let x = 1;
function f(y = x) {
let x = 2;
console.log(y);
}
f() // 1
上面代码中，函数调用时，y的默认值变量x尚未在函数内部生成，所以x指向全局变量。
如果此时，全局变量x不存在，就会报错。
function f(y = x) {
let x = 2;
console.log(y);
}
f() // ReferenceError: x is not defined
下面这样写，也会报错。
var x = 1;
function foo(x = x) {
// ...
}
foo() // ReferenceError: x is not defined
上面代码中，函数foo的参数x的默认值也是x。这时，默认值x的作用域是函数作用域，而不是全局作用域。由于在函数作用域中，存在变量x，但是
默认值在x赋值之前先执行了，所以这时属于暂时性死区（参见《let和const命令》一章），任何对x的操作都会报错。
如果参数的默认值是一个函数，该函数的作用域是其声明时所在的作用域。请看下面的例子。
let foo = 'outer';
function bar(func = x =&gt; foo) {
let foo = 'inner';
console.log(func()); // outer
}
bar();
上面代码中，函数bar的参数func的默认值是一个匿名函数，返回值为变量foo。这个匿名函数声明时，bar函数的作用域还没有形成，所以匿名函数
里面的foo指向外层作用域的foo，输出outer。
如果写成下面这样，就会报错。
function bar(func = () =&gt; foo) {
let foo = 'inner';
console.log(func());
}
bar() // ReferenceError: foo is not defined
上面代码中，匿名函数里面的foo指向函数外层，但是函数外层并没有声明foo，所以就报错了。
下面是一个更复杂的例子。
var x = 1;
function foo(x, y = function() { x = 2; }) {
var x = 3;
y();
console.log(x);
}
foo() // 3
上面代码中，函数foo的参数y的默认值是一个匿名函数。函数foo调用时，它的参数x的值为undefined，所以y函数内部的x一开始是undefined，后
来被重新赋值2。但是，函数foo内部重新声明了一个x，值为3，这两个x是不一样的，互相不产生影响，因此最后输出3。
如果将var x = 3的var去除，两个x就是一样的，最后输出的就是2。
var x = 1;
function foo(x, y = function() { x = 2; }) {
x = 3;
y();
console.log(x);
}
foo() // 2
8.1.6 应用
利用参数默认值，可以指定某一个参数不得省略，如果省略就抛出一个错误。
function throwIfMissing() {
throw new Error('Missing parameter');
}
function foo(mustBeProvided = throwIfMissing()) {
return mustBeProvided;
}
foo()
// Error: Missing parameter
上面代码的foo函数，如果调用的时候没有参数，就会调用默认值throwIfMissing函数，从而抛出一个错误。
从上面代码还可以看到，参数mustBeProvided的默认值等于throwIfMissing函数的运行结果（即函数名之后有一对圆括号），这表明参数的默认值不
是在定义时执行，而是在运行时执行（即如果参数已经赋值，默认值中的函数就不会运行），这与python语言不一样。
另外，可以将参数默认值设为undefined，表明这个参数是可以省略的。
function foo(optional = undefined) { ··· }
8.2 rest参数
ES6引入rest参数（形式为“...变量名”），用于获取函数的多余参数，这样就不需要使用arguments对象了。rest参数搭配的变量是一个数组，该变量将
多余的参数放入数组中。
function add(...values) {
let sum = 0;
for (var val of values) {
sum += val;
}
return sum;
}
add(2, 5, 3) // 10
上面代码的add函数是一个求和函数，利用rest参数，可以向该函数传入任意数目的参数。
下面是一个rest参数代替arguments变量的例子。
// arguments变量的写法
function sortNumbers() {
return Array.prototype.slice.call(arguments).sort();
}
// rest参数的写法
const sortNumbers = (...numbers) =&gt; numbers.sort();
上面代码的两种写法，比较后可以发现，rest参数的写法更自然也更简洁。
rest参数中的变量代表一个数组，所以数组特有的方法都可以用于这个变量。下面是一个利用rest参数改写数组push方法的例子。
function push(array, ...items) {
items.forEach(function(item) {
array.push(item);
console.log(item);
});
}
var a = [];
push(a, 1, 2, 3)
注意，rest参数之后不能再有其他参数（即只能是最后一个参数），否则会报错。
// 报错
function f(a, ...b, c) {
// ...
}
函数的length属性，不包括rest参数。
(function(a) {}).length // 1
(function(...a) {}).length // 0
(function(a, ...b) {}).length // 1
8.3 扩展运算符
8.3.1 含义
扩展运算符（spread）是三个点（...）。它好比rest参数的逆运算，将一个数组转为用逗号分隔的参数序列。
console.log(...[1, 2, 3])
// 1 2 3
console.log(1, ...[2, 3, 4], 5)
// 1 2 3 4 5
[...document.querySelectorAll('div')]
// [&lt;div&gt;, &lt;div&gt;, &lt;div&gt;]
该运算符主要用于函数调用。
function push(array, ...items) {
array.push(...items);
}
function add(x, y) {
return x + y;
}
var numbers = [4, 38];
add(...numbers) // 42
上面代码中，array.push(...items)和add(...numbers)这两行，都是函数的调用，它们的都使用了扩展运算符。该运算符将一个数组，变为参数序
列。
扩展运算符与正常的函数参数可以结合使用，非常灵活。
function f(v, w, x, y, z) { }
var args = [0, 1];
f(-1, ...args, 2, ...[3]);
8.3.2 替代数组的apply方法
由于扩展运算符可以展开数组，所以不再需要apply方法，将数组转为函数的参数了。
// ES5的写法
function f(x, y, z) {
// ...
}
var args = [0, 1, 2];
f.apply(null, args);
// ES6的写法
function f(x, y, z) {
// ...
}
var args = [0, 1, 2];
f(...args);
下面是扩展运算符取代apply方法的一个实际的例子，应用Math.max方法，简化求出一个数组最大元素的写法。
// ES5的写法
Math.max.apply(null, [14, 3, 77])
// ES6的写法
Math.max(...[14, 3, 77])
// 等同于
Math.max(14, 3, 77);
上面代码表示，由于JavaScript不提供求数组最大元素的函数，所以只能套用Math.max函数，将数组转为一个参数序列，然后求最大值。有了扩展运算
符以后，就可以直接用Math.max了。
另一个例子是通过push函数，将一个数组添加到另一个数组的尾部。
// ES5的写法
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
Array.prototype.push.apply(arr1, arr2);
// ES6的写法
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
arr1.push(...arr2);
上面代码的ES5写法中，push方法的参数不能是数组，所以只好通过apply方法变通使用push方法。有了扩展运算符，就可以直接将数组传入push方
法。
下面是另外一个例子。
// ES5
new (Date.bind.apply(Date, [null, 2015, 1, 1]))
// ES6
new Date(...[2015, 1, 1]);
8.3.3 扩展运算符的应用
（1）合并数组
扩展运算符提供了数组合并的新写法。
// ES5
[1, 2].concat(more)
// ES6
[1, 2, ...more]
var arr1 = ['a', 'b'];
var arr2 = ['c'];
var arr3 = ['d', 'e'];
// ES5的合并数组
arr1.concat(arr2, arr3);
// [ 'a', 'b', 'c', 'd', 'e' ]
// ES6的合并数组
[...arr1, ...arr2, ...arr3]
// [ 'a', 'b', 'c', 'd', 'e' ]
（2）与解构赋值结合
扩展运算符可以与解构赋值结合起来，用于生成数组。
// ES5
a = list[0], rest = list.slice(1)
// ES6
[a, ...rest] = list
下面是另外一些例子。
const [first, ...rest] = [1, 2, 3, 4, 5];
first // 1
rest // [2, 3, 4, 5]
const [first, ...rest] = [];
first // undefined
rest // []:
const [first, ...rest] = ["foo"];
first // "foo"
rest // []
如果将扩展运算符用于数组赋值，只能放在参数的最后一位，否则会报错。
const [...butLast, last] = [1, 2, 3, 4, 5];
// 报错
const [first, ...middle, last] = [1, 2, 3, 4, 5];
// 报错
（3）函数的返回值
JavaScript的函数只能返回一个值，如果需要返回多个值，只能返回数组或对象。扩展运算符提供了解决这个问题的一种变通方法。
var dateFields = readDateFields(database);
var d = new Date(...dateFields);
上面代码从数据库取出一行数据，通过扩展运算符，直接将其传入构造函数Date。
（4）字符串
扩展运算符还可以将字符串转为真正的数组。
[...'hello']
// [ "h", "e", "l", "l", "o" ]
上面的写法，有一个重要的好处，那就是能够正确识别32位的Unicode字符。
'x\uD83D\uDE80y'.length // 4
[...'x\uD83D\uDE80y'].length // 3
上面代码的第一种写法，JavaScript会将32位Unicode字符，识别为2个字符，采用扩展运算符就没有这个问题。因此，正确返回字符串长度的函数，
可以像下面这样写。
function length(str) {
return [...str].length;
}
length('x\uD83D\uDE80y') // 3
凡是涉及到操作32位Unicode字符的函数，都有这个问题。因此，最好都用扩展运算符改写。
let str = 'x\uD83D\uDE80y';
str.split('').reverse().join('')
// 'y\uDE80\uD83Dx'
[...str].reverse().join('')
// 'y\uD83D\uDE80x'
上面代码中，如果不用扩展运算符，字符串的reverse操作就不正确。
（5）实现了Iterator接口的对象
任何Iterator接口的对象，都可以用扩展运算符转为真正的数组。
var nodeList = document.querySelectorAll('div');
var array = [...nodeList];
上面代码中，querySelectorAll方法返回的是一个nodeList对象。它不是数组，而是一个类似数组的对象。这时，扩展运算符可以将其转为真正的数
组，原因就在于NodeList对象实现了Iterator接口。
对于那些没有部署Iterator接口的类似数组的对象，扩展运算符就无法将其转为真正的数组。
let arrayLike = {
'0': 'a',
'1': 'b',
'2': 'c',
length: 3
};
// TypeError: Cannot spread non-iterable object.
let arr = [...arrayLike];
上面代码中，arrayLike是一个类似数组的对象，但是没有部署Iterator接口，扩展运算符就会报错。这时，可以改为使用Array.from方法
将arrayLike转为真正的数组。
（6）Map和Set结构，Generator函数
扩展运算符内部调用的是数据结构的Iterator接口，因此只要具有Iterator接口的对象，都可以使用扩展运算符，比如Map结构。
let map = new Map([
[1, 'one'],
[2, 'two'],
[3, 'three'],
]);
let arr = [...map.keys()]; // [1, 2, 3]
Generator函数运行后，返回一个遍历器对象，因此也可以使用扩展运算符。
var go = function*(){
yield 1;
yield 2;
yield 3;
};
[...go()] // [1, 2, 3]
上面代码中，变量go是一个Generator函数，执行后返回的是一个遍历器对象，对这个遍历器对象执行扩展运算符，就会将内部遍历得到的值，转为一
个数组。
如果对没有iterator接口的对象，使用扩展运算符，将会报错。
var obj = {a: 1, b: 2};
let arr = [...obj]; // TypeError: Cannot spread non-iterable object
8.4 name属性
函数的name属性，返回该函数的函数名。
function foo() {}
foo.name // "foo"
这个属性早就被浏览器广泛支持，但是直到ES6，才将其写入了标准。
需要注意的是，ES6对这个属性的行为做出了一些修改。如果将一个匿名函数赋值给一个变量，ES5的name属性，会返回空字符串，而ES6的name属性
会返回实际的函数名。
var func1 = function () {};
// ES5
func1.name // ""
// ES6
func1.name // "func1"
上面代码中，变量func1等于一个匿名函数，ES5和ES6的name属性返回的值不一样。
如果将一个具名函数赋值给一个变量，则ES5和ES6的name属性都返回这个具名函数原本的名字。
const bar = function baz() {};
// ES5
bar.name // "baz"
// ES6
bar.name // "baz"
Function构造函数返回的函数实例，name属性的值为“anonymous”。
(new Function).name // "anonymous"
bind返回的函数，name属性值会加上“bound ”前缀。
function foo() {};
foo.bind({}).name // "bound foo"
(function(){}).bind({}).name // "bound "
8.5 箭头函数
8.5.1 基本用法
ES6允许使用“箭头”（=&gt;）定义函数。
var f = v =&gt; v;
上面的箭头函数等同于：
var f = function(v) {
return v;
};
如果箭头函数不需要参数或需要多个参数，就使用一个圆括号代表参数部分。
var f = () =&gt; 5;
// 等同于
var f = function () { return 5 };
var sum = (num1, num2) =&gt; num1 + num2;
// 等同于
var sum = function(num1, num2) {
return num1 + num2;
};
如果箭头函数的代码块部分多于一条语句，就要使用大括号将它们括起来，并且使用return语句返回。
var sum = (num1, num2) =&gt; { return num1 + num2; }
由于大括号被解释为代码块，所以如果箭头函数直接返回一个对象，必须在对象外面加上括号。
var getTempItem = id =&gt; ({ id: id, name: "Temp" });
箭头函数可以与变量解构结合使用。
const full = ({ first, last }) =&gt; first + ' ' + last;
// 等同于
function full(person) {
return person.first + ' ' + person.last;
}
箭头函数使得表达更加简洁。
const isEven = n =&gt; n % 2 == 0;
const square = n =&gt; n * n;
上面代码只用了两行，就定义了两个简单的工具函数。如果不用箭头函数，可能就要占用多行，而且还不如现在这样写醒目。
箭头函数的一个用处是简化回调函数。
// 正常函数写法
[1,2,3].map(function (x) {
return x * x;
});
// 箭头函数写法
[1,2,3].map(x =&gt; x * x);
另一个例子是
// 正常函数写法
var result = values.sort(function (a, b) {
return a - b;
});
// 箭头函数写法
var result = values.sort((a, b) =&gt; a - b);
下面是rest参数与箭头函数结合的例子。
const numbers = (...nums) =&gt; nums;
numbers(1, 2, 3, 4, 5)
// [1,2,3,4,5]
const headAndTail = (head, ...tail) =&gt; [head, tail];
headAndTail(1, 2, 3, 4, 5)
// [1,[2,3,4,5]]
8.5.2 使用注意点
箭头函数有几个使用注意点。
（1）函数体内的this对象，就是定义时所在的对象，而不是使用时所在的对象。
（2）不可以当作构造函数，也就是说，不可以使用new命令，否则会抛出一个错误。
（3）不可以使用arguments对象，该对象在函数体内不存在。如果要用，可以用Rest参数代替。
（4）不可以使用yield命令，因此箭头函数不能用作Generator函数。
上面四点中，第一点尤其值得注意。this对象的指向是可变的，但是在箭头函数中，它是固定的。
function foo() {
setTimeout(() =&gt; {
console.log('id:', this.id);
}, 100);
}
var id = 21;
foo.call({ id: 42 });
// id: 42
上面代码中，setTimeout的参数是一个箭头函数，这个箭头函数的定义生效是在foo函数生成时，而它的真正执行要等到100毫秒后。如果是普通函
数，执行时this应该指向全局对象window，这时应该输出21。但是，箭头函数导致this总是指向函数定义生效时所在的对象（本例是{id: 42}），所
以输出的是42。
箭头函数可以让setTimeout里面的this，绑定定义时所在的作用域，而不是指向运行时所在的作用域。下面是另一个例子。
function Timer() {
this.s1 = 0;
this.s2 = 0;
// 箭头函数
setInterval(() =&gt; this.s1++, 1000);
// 普通函数
setInterval(function () {
this.s2++;
}, 1000);
}
var timer = new Timer();
setTimeout(() =&gt; console.log('s1: ', timer.s1), 3100);
setTimeout(() =&gt; console.log('s2: ', timer.s2), 3100);
// s1: 3
// s2: 0
上面代码中，Timer函数内部设置了两个定时器，分别使用了箭头函数和普通函数。前者的this绑定定义时所在的作用域（即Timer函数），后者
的this指向运行时所在的作用域（即全局对象）。所以，3100毫秒之后，timer.s1被更新了3次，而timer.s2一次都没更新。
箭头函数可以让this指向固定化，这种特性很有利于封装回调函数。下面是一个例子，DOM事件的回调函数封装在一个对象里面。
var handler = {
id: '123456',
init: function() {
document.addEventListener('click',
event =&gt; this.doSomething(event.type), false);
},
doSomething: function(type) {
console.log('Handling ' + type + ' for ' + this.id);
}
};
上面代码的init方法中，使用了箭头函数，这导致这个箭头函数里面的this，总是指向handler对象。否则，回调函数运行时，this.doSomething这
一行会报错，因为此时this指向document对象。
this指向的固定化，并不是因为箭头函数内部有绑定this的机制，实际原因是箭头函数根本没有自己的this，导致内部的this就是外层代码块
的this。正是因为它没有this，所以也就不能用作构造函数。
所以，箭头函数转成ES5的代码如下。
// ES6
function foo() {
setTimeout(() =&gt; {
console.log('id:', this.id);
}, 100);
}
// ES5
function foo() {
var _this = this;
setTimeout(function () {
console.log('id:', _this.id);
}, 100);
}
上面代码中，转换后的ES5版本清楚地说明了，箭头函数里面根本没有自己的this，而是引用外层的this。
请问下面的代码之中有几个this？
function foo() {
return () =&gt; {
return () =&gt; {
return () =&gt; {
console.log('id:', this.id);
};
};
};
}
var f = foo.call({id: 1});
var t1 = f.call({id: 2})()(); // id: 1
var t2 = f().call({id: 3})(); // id: 1
var t3 = f()().call({id: 4}); // id: 1
上面代码之中，只有一个this，就是函数foo的this，所以t1、t2、t3都输出同样的结果。因为所有的内层函数都是箭头函数，都没有自己的this，
它们的this其实都是最外层foo函数的this。
除了this，以下三个变量在箭头函数之中也是不存在的，指向外层函数的对应变量：arguments、super、new.target。
function foo() {
setTimeout(() =&gt; {
console.log('args:', arguments);
}, 100);
}
foo(2, 4, 6, 8)
// args: [2, 4, 6, 8]
上面代码中，箭头函数内部的变量arguments，其实是函数foo的arguments变量。
另外，由于箭头函数没有自己的this，所以当然也就不能用call()、apply()、bind()这些方法去改变this的指向。
(function() {
return [
(() =&gt; this.x).bind({ x: 'inner' })()
];
}).call({ x: 'outer' });
// ['outer']
上面代码中，箭头函数没有自己的this，所以bind方法无效，内部的this指向外部的this。
长期以来，JavaScript语言的this对象一直是一个令人头痛的问题，在对象方法中使用this，必须非常小心。箭头函数”绑定”this，很大程度上解决了
这个困扰。
8.5.3 嵌套的箭头函数
箭头函数内部，还可以再使用箭头函数。下面是一个ES5语法的多重嵌套函数。
function insert(value) {
return {into: function (array) {
return {after: function (afterValue) {
array.splice(array.indexOf(afterValue) + 1, 0, value);
return array;
}};
}};
}
insert(2).into([1, 3]).after(1); //[1, 2, 3]
上面这个函数，可以使用箭头函数改写。
let insert = (value) =&gt; ({into: (array) =&gt; ({after: (afterValue) =&gt; {
array.splice(array.indexOf(afterValue) + 1, 0, value);
return array;
}})});
insert(2).into([1, 3]).after(1); //[1, 2, 3]
下面是一个部署管道机制（pipeline）的例子，即前一个函数的输出是后一个函数的输入。
const pipeline = (...funcs) =&gt;
val =&gt; funcs.reduce((a, b) =&gt; b(a), val);
const plus1 = a =&gt; a + 1;
const mult2 = a =&gt; a * 2;
const addThenMult = pipeline(plus1, mult2);
addThenMult(5)
// 12
如果觉得上面的写法可读性比较差，也可以采用下面的写法。
const plus1 = a =&gt; a + 1;
const mult2 = a =&gt; a * 2;
mult2(plus1(5))
// 12
箭头函数还有一个功能，就是可以很方便地改写λ演算。
// λ演算的写法
fix = λf.(λx.f(λv.x(x)(v)))(λx.f(λv.x(x)(v)))
// ES6的写法
var fix = f =&gt; (x =&gt; f(v =&gt; x(x)(v)))
(x =&gt; f(v =&gt; x(x)(v)));
上面两种写法，几乎是一一对应的。由于λ演算对于计算机科学非常重要，这使得我们可以用ES6作为替代工具，探索计算机科学。
8.6 函数绑定
箭头函数可以绑定this对象，大大减少了显式绑定this对象的写法（call、apply、bind）。但是，箭头函数并不适用于所有场合，所以ES7提出
了“函数绑定”（function bind）运算符，用来取代call、apply、bind调用。虽然该语法还是ES7的一个提案，但是Babel转码器已经支持。
函数绑定运算符是并排的两个双冒号（::），双冒号左边是一个对象，右边是一个函数。该运算符会自动将左边的对象，作为上下文环境（即this对
象），绑定到右边的函数上面。
foo::bar;
// 等同于
bar.bind(foo);
foo::bar(...arguments);
// 等同于
bar.apply(foo, arguments);
const hasOwnProperty = Object.prototype.hasOwnProperty;
function hasOwn(obj, key) {
return obj::hasOwnProperty(key);
}
如果双冒号左边为空，右边是一个对象的方法，则等于将该方法绑定在该对象上面。
var method = obj::obj.foo;
// 等同于
var method = ::obj.foo;
let log = ::console.log;
// 等同于
var log = console.log.bind(console);
由于双冒号运算符返回的还是原对象，因此可以采用链式写法。
// 例一
import { map, takeWhile, forEach } from "iterlib";
getPlayers()
::map(x =&gt; x.character())
::takeWhile(x =&gt; x.strength &gt; 100)
::forEach(x =&gt; console.log(x));
// 例二
let { find, html } = jake;
document.querySelectorAll("div.myClass")
::find("p")
::html("hahaha");
8.7 尾调用优化
8.7.1 什么是尾调用？
尾调用（Tail Call）是函数式编程的一个重要概念，本身非常简单，一句话就能说清楚，就是指某个函数的最后一步是调用另一个函数。
function f(x){
return g(x);
}
上面代码中，函数f的最后一步是调用函数g，这就叫尾调用。
以下三种情况，都不属于尾调用。
// 情况一
function f(x){
let y = g(x);
return y;
}
// 情况二
function f(x){
return g(x) + 1;
}
// 情况三
function f(x){
g(x);
}
上面代码中，情况一是调用函数g之后，还有赋值操作，所以不属于尾调用，即使语义完全一样。情况二也属于调用后还有操作，即使写在一行内。情
况三等同于下面的代码。
function f(x){
g(x);
return undefined;
}
尾调用不一定出现在函数尾部，只要是最后一步操作即可。
function f(x) {
if (x &gt; 0) {
return m(x)
}
return n(x);
}
上面代码中，函数m和n都属于尾调用，因为它们都是函数f的最后一步操作。
8.7.2 尾调用优化
尾调用之所以与其他调用不同，就在于它的特殊的调用位置。
我们知道，函数调用会在内存形成一个“调用记录”，又称“调用帧”（call frame），保存调用位置和内部变量等信息。如果在函数A的内部调用函数B，
那么在A的调用帧上方，还会形成一个B的调用帧。等到B运行结束，将结果返回到A，B的调用帧才会消失。如果函数B内部还调用函数C，那就还有一
个C的调用帧，以此类推。所有的调用帧，就形成一个“调用栈”（call stack）。
尾调用由于是函数的最后一步操作，所以不需要保留外层函数的调用帧，因为调用位置、内部变量等信息都不会再用到了，只要直接用内层函数的调
用帧，取代外层函数的调用帧就可以了。
function f() {
let m = 1;
let n = 2;
return g(m + n);
}
f();
// 等同于
function f() {
return g(3);
}
f();
// 等同于
g(3);
上面代码中，如果函数g不是尾调用，函数f就需要保存内部变量m和n的值、g的调用位置等信息。但由于调用g之后，函数f就结束了，所以执行到最后
一步，完全可以删除 f(x) 的调用帧，只保留 g(3) 的调用帧。
这就叫做“尾调用优化”（Tail call optimization），即只保留内层函数的调用帧。如果所有函数都是尾调用，那么完全可以做到每次执行时，调用帧只有
一项，这将大大节省内存。这就是“尾调用优化”的意义。
注意，只有不再用到外层函数的内部变量，内层函数的调用帧才会取代外层函数的调用帧，否则就无法进行“尾调用优化”。
function addOne(a){
var one = 1;
function inner(b){
return b + one;
}
return inner(a);
}
上面的函数不会进行尾调用优化，因为内层函数inner用到了外层函数addOne的内部变量one。
8.7.3 尾递归
函数调用自身，称为递归。如果尾调用自身，就称为尾递归。
递归非常耗费内存，因为需要同时保存成千上百个调用帧，很容易发生“栈溢出”错误（stack overflow）。但对于尾递归来说，由于只存在一个调用
帧，所以永远不会发生“栈溢出”错误。
function factorial(n) {
if (n === 1) return 1;
return n * factorial(n - 1);
}
factorial(5) // 120
上面代码是一个阶乘函数，计算n的阶乘，最多需要保存n个调用记录，复杂度 O(n) 。
如果改写成尾递归，只保留一个调用记录，复杂度 O(1) 。
function factorial(n, total) {
if (n === 1) return total;
return factorial(n - 1, n * total);
}
factorial(5, 1) // 120
还有一个比较著名的例子，就是计算fibonacci 数列，也能充分说明尾递归优化的重要性
如果是非尾递归的fibonacci 递归方法
function Fibonacci (n) {
if ( n &lt;= 1 ) {return 1};
return Fibonacci(n - 1) + Fibonacci(n - 2);
}
Fibonacci(10); // 89
// Fibonacci(100)
// Fibonacci(500)
// 堆栈溢出了
如果我们使用尾递归优化过的fibonacci 递归算法
function Fibonacci2 (n , ac1 = 1 , ac2 = 1) {
if( n &lt;= 1 ) {return ac2};
return Fibonacci2 (n - 1, ac2, ac1 + ac2);
}
Fibonacci2(100) // 573147844013817200000
Fibonacci2(1000) // 7.0330367711422765e+208
Fibonacci2(10000) // Infinity
由此可见，“尾调用优化”对递归操作意义重大，所以一些函数式编程语言将其写入了语言规格。ES6也是如此，第一次明确规定，所有ECMAScript的实
现，都必须部署“尾调用优化”。这就是说，在ES6中，只要使用尾递归，就不会发生栈溢出，相对节省内存。
8.7.4 递归函数的改写
尾递归的实现，往往需要改写递归函数，确保最后一步只调用自身。做到这一点的方法，就是把所有用到的内部变量改写成函数的参数。比如上面的
例子，阶乘函数 factorial 需要用到一个中间变量 total ，那就把这个中间变量改写成函数的参数。这样做的缺点就是不太直观，第一眼很难看出来，为
什么计算5的阶乘，需要传入两个参数5和1？
两个方法可以解决这个问题。方法一是在尾递归函数之外，再提供一个正常形式的函数。
function tailFactorial(n, total) {
if (n === 1) return total;
return tailFactorial(n - 1, n * total);
}
function factorial(n) {
return tailFactorial(n, 1);
}
factorial(5) // 120
上面代码通过一个正常形式的阶乘函数 factorial ，调用尾递归函数 tailFactorial ，看起来就正常多了。
函数式编程有一个概念，叫做柯里化（currying），意思是将多参数的函数转换成单参数的形式。这里也可以使用柯里化。
function currying(fn, n) {
return function (m) {
return fn.call(this, m, n);
};
}
function tailFactorial(n, total) {
if (n === 1) return total;
return tailFactorial(n - 1, n * total);
}
const factorial = currying(tailFactorial, 1);
factorial(5) // 120
上面代码通过柯里化，将尾递归函数 tailFactorial 变为只接受1个参数的 factorial 。
第二种方法就简单多了，就是采用ES6的函数默认值。
function factorial(n, total = 1) {
if (n === 1) return total;
return factorial(n - 1, n * total);
}
factorial(5) // 120
上面代码中，参数 total 有默认值1，所以调用时不用提供这个值。
总结一下，递归本质上是一种循环操作。纯粹的函数式编程语言没有循环操作命令，所有的循环都用递归实现，这就是为什么尾递归对这些语言极其
重要。对于其他支持“尾调用优化”的语言（比如Lua，ES6），只需要知道循环可以用递归代替，而一旦使用递归，就最好使用尾递归。
8.7.5 严格模式
ES6的尾调用优化只在严格模式下开启，正常模式是无效的。
这是因为在正常模式下，函数内部有两个变量，可以跟踪函数的调用栈。
func.arguments：返回调用时函数的参数。
func.caller：返回调用当前函数的那个函数。
尾调用优化发生时，函数的调用栈会改写，因此上面两个变量就会失真。严格模式禁用这两个变量，所以尾调用模式仅在严格模式下生效。
function restricted() {
"use strict";
restricted.caller; // 报错
restricted.arguments; // 报错
}
restricted();
8.7.6 尾递归优化的实现
尾递归优化只在严格模式下生效，那么正常模式下，或者那些不支持该功能的环境中，有没有办法也使用尾递归优化呢？回答是可以的，就是自己实
现尾递归优化。
它的原理非常简单。尾递归之所以需要优化，原因是调用栈太多，造成溢出，那么只要减少调用栈，就不会溢出。怎么做可以减少调用栈呢？就是采
用“循环”换掉“递归”。
下面是一个正常的递归函数。
function sum(x, y) {
if (y &gt; 0) {
return sum(x + 1, y - 1);
} else {
return x;
}
}
sum(1, 100000)
// Uncaught RangeError: Maximum call stack size exceeded(…)
上面代码中，sum是一个递归函数，参数x是需要累加的值，参数y控制递归次数。一旦指定sum递归100000次，就会报错，提示超出调用栈的最大次
数。
蹦床函数（trampoline）可以将递归执行转为循环执行。
function trampoline(f) {
while (f &amp;&amp; f instanceof Function) {
f = f();
}
return f;
}
上面就是蹦床函数的一个实现，它接受一个函数f作为参数。只要f执行后返回一个函数，就继续执行。注意，这里是返回一个函数，然后执行该函
数，而不是函数里面调用函数，这样就避免了递归执行，从而就消除了调用栈过大的问题。
然后，要做的就是将原来的递归函数，改写为每一步返回另一个函数。
function sum(x, y) {
if (y &gt; 0) {
return sum.bind(null, x + 1, y - 1);
} else {
return x;
}
}
上面代码中，sum函数的每次执行，都会返回自身的另一个版本。
现在，使用蹦床函数执行sum，就不会发生调用栈溢出。
trampoline(sum(1, 100000))
// 100001
蹦床函数并不是真正的尾递归优化，下面的实现才是。
function tco(f) {
var value;
var active = false;
var accumulated = [];
return function accumulator() {
accumulated.push(arguments);
if (!active) {
active = true;
while (accumulated.length) {
value = f.apply(this, accumulated.shift());
}
active = false;
return value;
}
};
}
var sum = tco(function(x, y) {
if (y &gt; 0) {
return sum(x + 1, y - 1)
}
else {
return x
}
});
sum(1, 100000)
// 100001
上面代码中，tco函数是尾递归优化的实现，它的奥妙就在于状态变量active。默认情况下，这个变量是不激活的。一旦进入尾递归优化的过程，这个
变量就激活了。然后，每一轮递归sum返回的都是undefined，所以就避免了递归执行；而accumulated数组存放每一轮sum执行的参数，总是有值的，
这就保证了accumulator函数内部的while循环总是会执行。这样就很巧妙地将“递归”改成了“循环”，而后一轮的参数会取代前一轮的参数，保证了调用
栈只有一层。
8.8 函数参数的尾逗号
ES7有一个提案，允许函数的最后一个参数有尾逗号（trailing comma）。
目前，函数定义和调用时，都不允许有参数的尾逗号。
function clownsEverywhere(
param1,
param2
) { /* ... */ }
clownsEverywhere(
'foo',
'bar'
);
如果以后要在函数的定义之中添加参数，就势必还要添加一个逗号。这对版本管理系统来说，就会显示，添加逗号的那一行也发生了变动。这看上去
有点冗余，因此新提案允许定义和调用时，尾部直接有一个逗号。
function clownsEverywhere(
param1,
param2,
) { /* ... */ }
clownsEverywhere(
'foo',
'bar',
);
9 对象的扩展
9.1 属性的简洁表示法
ES6允许直接写入变量和函数，作为对象的属性和方法。这样的书写更加简洁。
var foo = 'bar';
var baz = {foo};
baz // {foo: "bar"}
// 等同于
var baz = {foo: foo};
上面代码表明，ES6允许在对象之中，只写属性名，不写属性值。这时，属性值等于属性名所代表的变量。下面是另一个例子。
function f(x, y) {
return {x, y};
}
// 等同于
function f(x, y) {
return {x: x, y: y};
}
f(1, 2) // Object {x: 1, y: 2}
除了属性简写，方法也可以简写。
var o = {
method() {
return "Hello!";
}
};
// 等同于
var o = {
method: function() {
return "Hello!";
}
};
下面是一个实际的例子。
var birth = '2000/01/01';
var Person = {
name: '张三',
//等同于birth: birth
birth,
// 等同于hello: function ()...
hello() { console.log('我的名字是', this.name); }
};
这种写法用于函数的返回值，将会非常方便。
function getPoint() {
var x = 1;
var y = 10;
return {x, y};
}
getPoint()
// {x:1, y:10}
CommonJS模块输出变量，就非常合适使用简洁写法。
var ms = {};
function getItem (key) {
return key in ms ? ms[key] : null;
}
function setItem (key, value) {
ms[key] = value;
}
function clear () {
ms = {};
}
module.exports = { getItem, setItem, clear };
// 等同于
module.exports = {
getItem: getItem,
setItem: setItem,
clear: clear
};
属性的赋值器（setter）和取值器（getter），事实上也是采用这种写法。
var cart = {
_wheels: 4,
get wheels () {
return this._wheels;
},
set wheels (value) {
if (value &lt; this._wheels) {
throw new Error('数值太小了！');
}
this._wheels = value;
}
}
注意，简洁写法的属性名总是字符串，这会导致一些看上去比较奇怪的结果。
var obj = {
class () {}
};
// 等同于
var obj = {
'class': function() {}
};
上面代码中，class是字符串，所以不会因为它属于关键字，而导致语法解析报错。
如果某个方法的值是一个Generator函数，前面需要加上星号。
var obj = {
* m(){
yield 'hello world';
}
};
9.2 属性名表达式
JavaScript语言定义对象的属性，有两种方法。
// 方法一
obj.foo = true;
// 方法二
obj['a' + 'bc'] = 123;
上面代码的方法一是直接用标识符作为属性名，方法二是用表达式作为属性名，这时要将表达式放在方括号之内。
但是，如果使用字面量方式定义对象（使用大括号），在ES5中只能使用方法一（标识符）定义属性。
var obj = {
foo: true,
abc: 123
};
ES6允许字面量定义对象时，用方法二（表达式）作为对象的属性名，即把表达式放在方括号内。
let propKey = 'foo';
let obj = {
[propKey]: true,
['a' + 'bc']: 123
};
下面是另一个例子。
var lastWord = 'last word';
var a = {
'first word': 'hello',
[lastWord]: 'world'
};
a['first word'] // "hello"
a[lastWord] // "world"
a['last word'] // "world"
表达式还可以用于定义方法名。
let obj = {
['h'+'ello']() {
return 'hi';
}
};
obj.hello() // hi
注意，属性名表达式与简洁表示法，不能同时使用，会报错。
// 报错
var foo = 'bar';
var bar = 'abc';
var baz = { [foo] };
// 正确
var foo = 'bar';
var baz = { [foo]: 'abc'};
9.3 方法的name属性
函数的name属性，返回函数名。对象方法也是函数，因此也有name属性。
var person = {
sayName() {
console.log(this.name);
},
get firstName() {
return "Nicholas";
}
};
person.sayName.name // "sayName"
person.firstName.name // "get firstName"
上面代码中，方法的name属性返回函数名（即方法名）。如果使用了取值函数，则会在方法名前加上get。如果是存值函数，方法名的前面会加
上set。
有两种特殊情况：bind方法创造的函数，name属性返回“bound”加上原函数的名字；Function构造函数创造的函数，name属性返回“anonymous”。
(new Function()).name // "anonymous"
var doSomething = function() {
// ...
};
doSomething.bind().name // "bound doSomething"
如果对象的方法是一个Symbol值，那么name属性返回的是这个Symbol值的描述。
const key1 = Symbol('description');
const key2 = Symbol();
let obj = {
[key1]() {},
[key2]() {},
};
obj[key1].name // "[description]"
obj[key2].name // ""
上面代码中，key1对应的Symbol值有描述，key2没有。
9.4 Object.is()
ES5比较两个值是否相等，只有两个运算符：相等运算符（==）和严格相等运算符（===）。它们都有缺点，前者会自动转换数据类型，后者的NaN不
等于自身，以及+0等于-0。JavaScript缺乏一种运算，在所有环境中，只要两个值是一样的，它们就应该相等。
ES6提出“Same-value equality”（同值相等）算法，用来解决这个问题。Object.is就是部署这个算法的新方法。它用来比较两个值是否严格相等，与
严格比较运算符（===）的行为基本一致。
Object.is('foo', 'foo')
// true
Object.is({}, {})
// false
不同之处只有两个：一是+0不等于-0，二是NaN等于自身。
+0 === -0 //true
NaN === NaN // false
Object.is(+0, -0) // false
Object.is(NaN, NaN) // true
ES5可以通过下面的代码，部署Object.is。
Object.defineProperty(Object, 'is', {
value: function(x, y) {
if (x === y) {
// 针对+0 不等于 -0的情况
return x !== 0 || 1 / x === 1 / y;
}
// 针对NaN的情况
return x !== x &amp;&amp; y !== y;
},
configurable: true,
enumerable: false,
writable: true
});
9.5 Object.assign()
9.5.1 基本用法
Object.assign方法用于对象的合并，将源对象（source）的所有可枚举属性，复制到目标对象（target）。
var target = { a: 1 };
var source1 = { b: 2 };
var source2 = { c: 3 };
Object.assign(target, source1, source2);
target // {a:1, b:2, c:3}
Object.assign方法的第一个参数是目标对象，后面的参数都是源对象。
注意，如果目标对象与源对象有同名属性，或多个源对象有同名属性，则后面的属性会覆盖前面的属性。
var target = { a: 1, b: 1 };
var source1 = { b: 2, c: 2 };
var source2 = { c: 3 };
Object.assign(target, source1, source2);
target // {a:1, b:2, c:3}
如果只有一个参数，Object.assign会直接返回该参数。
var obj = {a: 1};
Object.assign(obj) === obj // true
如果该参数不是对象，则会先转成对象，然后返回。
typeof Object.assign(2) // "object"
由于undefined和null无法转成对象，所以如果它们作为参数，就会报错。
Object.assign(undefined) // 报错
Object.assign(null) // 报错
如果非对象参数出现在源对象的位置（即非首参数），那么处理规则有所不同。首先，这些参数都会转成对象，如果无法转成对象，就会跳过。这意
味着，如果undefined和null不在首参数，就不会报错。
let obj = {a: 1};
Object.assign(obj, undefined) === obj // true
Object.assign(obj, null) === obj // true
其他类型的值（即数值、字符串和布尔值）不在首参数，也不会报错。但是，除了字符串会以数组形式，拷贝入目标对象，其他值都不会产生效果。
var v1 = 'abc';
var v2 = true;
var v3 = 10;
var obj = Object.assign({}, v1, v2, v3);
console.log(obj); // { "0": "a", "1": "b", "2": "c" }
上面代码中，v1、v2、v3分别是字符串、布尔值和数值，结果只有字符串合入目标对象（以字符数组的形式），数值和布尔值都会被忽略。这是因为
只有字符串的包装对象，会产生可枚举属性。
Object(true) // {[[PrimitiveValue]]: true}
Object(10) // {[[PrimitiveValue]]: 10}
Object('abc') // {0: "a", 1: "b", 2: "c", length: 3, [[PrimitiveValue]]: "abc"}
上面代码中，布尔值、数值、字符串分别转成对应的包装对象，可以看到它们的原始值都在包装对象的内部属性[[PrimitiveValue]]上面，这个属性
是不会被Object.assign拷贝的。只有字符串的包装对象，会产生可枚举的实义属性，那些属性则会被拷贝。
Object.assign拷贝的属性是有限制的，只拷贝源对象的自身属性（不拷贝继承属性），也不拷贝不可枚举的属性（enumerable: false）。
Object.assign({b: 'c'},
Object.defineProperty({}, 'invisible', {
enumerable: false,
value: 'hello'
})
)
// { b: 'c' }
上面代码中，Object.assign要拷贝的对象只有一个不可枚举属性invisible，这个属性并没有被拷贝进去。
属性名为Symbol值的属性，也会被Object.assign拷贝。
Object.assign({ a: 'b' }, { [Symbol('c')]: 'd' })
// { a: 'b', Symbol(c): 'd' }
9.5.2 注意点
Object.assign方法实行的是浅拷贝，而不是深拷贝。也就是说，如果源对象某个属性的值是对象，那么目标对象拷贝得到的是这个对象的引用。
var obj1 = {a: {b: 1}};
var obj2 = Object.assign({}, obj1);
obj1.a.b = 2;
obj2.a.b // 2
上面代码中，源对象obj1的a属性的值是一个对象，Object.assign拷贝得到的是这个对象的引用。这个对象的任何变化，都会反映到目标对象上面。
对于这种嵌套的对象，一旦遇到同名属性，Object.assign的处理方法是替换，而不是添加。
var target = { a: { b: 'c', d: 'e' } }
var source = { a: { b: 'hello' } }
Object.assign(target, source)
// { a: { b: 'hello' } }
上面代码中，target对象的a属性被source对象的a属性整个替换掉了，而不会得到{ a: { b: 'hello', d: 'e' } }的结果。这通常不是开发者想要
的，需要特别小心。
有一些函数库提供Object.assign的定制版本（比如Lodash的_.defaultsDeep方法），可以解决浅拷贝的问题，得到深拷贝的合并。
注意，Object.assign可以用来处理数组，但是会把数组视为对象。
Object.assign([1, 2, 3], [4, 5])
// [4, 5, 3]
上面代码中，Object.assign把数组视为属性名为0、1、2的对象，因此目标数组的0号属性4覆盖了原数组的0号属性1。
9.5.3 常见用途
Object.assign方法有很多用处。
（1）为对象添加属性
class Point {
constructor(x, y) {
Object.assign(this, {x, y});
}
}
上面方法通过Object.assign方法，将x属性和y属性添加到Point类的对象实例。
（2）为对象添加方法
Object.assign(SomeClass.prototype, {
someMethod(arg1, arg2) {
···
},
anotherMethod() {
···
}
});
// 等同于下面的写法
SomeClass.prototype.someMethod = function (arg1, arg2) {
···
};
SomeClass.prototype.anotherMethod = function () {
···
};
上面代码使用了对象属性的简洁表示法，直接将两个函数放在大括号中，再使用assign方法添加到SomeClass.prototype之中。
（3）克隆对象
function clone(origin) {
return Object.assign({}, origin);
}
上面代码将原始对象拷贝到一个空对象，就得到了原始对象的克隆。
不过，采用这种方法克隆，只能克隆原始对象自身的值，不能克隆它继承的值。如果想要保持继承链，可以采用下面的代码。
function clone(origin) {
let originProto = Object.getPrototypeOf(origin);
return Object.assign(Object.create(originProto), origin);
}
（4）合并多个对象
将多个对象合并到某个对象。
const merge =
(target, ...sources) =&gt; Object.assign(target, ...sources);
如果希望合并后返回一个新对象，可以改写上面函数，对一个空对象合并。
const merge =
(...sources) =&gt; Object.assign({}, ...sources);
（5）为属性指定默认值
const DEFAULTS = {
logLevel: 0,
outputFormat: 'html'
};
function processContent(options) {
let options = Object.assign({}, DEFAULTS, options);
}
上面代码中，DEFAULTS对象是默认值，options对象是用户提供的参数。Object.assign方法将DEFAULTS和options合并成一个新对象，如果两者有同
名属性，则option的属性值会覆盖DEFAULTS的属性值。
注意，由于存在深拷贝的问题，DEFAULTS对象和options对象的所有属性的值，都只能是简单类型，而不能指向另一个对象。否则，将导致DEFAULTS对
象的该属性不起作用。
9.6 属性的可枚举性
对象的每个属性都有一个描述对象（Descriptor），用来控制该属性的行为。Object.getOwnPropertyDescriptor方法可以获取该属性的描述对象。
let obj = { foo: 123 };
Object.getOwnPropertyDescriptor(obj, 'foo')
// {
// value: 123,
// writable: true,
// enumerable: true,
// configurable: true
// }
描述对象的enumerable属性，称为”可枚举性“，如果该属性为false，就表示某些操作会忽略当前属性。
ES5有三个操作会忽略enumerable为false的属性。
for...in循环：只遍历对象自身的和继承的可枚举的属性
Object.keys()：返回对象自身的所有可枚举的属性的键名
JSON.stringify()：只串行化对象自身的可枚举的属性
ES6新增了一个操作Object.assign()，会忽略enumerable为false的属性，只拷贝对象自身的可枚举的属性。
这四个操作之中，只有for...in会返回继承的属性。实际上，引入enumerable的最初目的，就是让某些属性可以规避掉for...in操作。比如，对象原
型的toString方法，以及数组的length属性，就通过这种手段，不会被for...in遍历到。
Object.getOwnPropertyDescriptor(Object.prototype, 'toString').enumerable
// false
Object.getOwnPropertyDescriptor([], 'length').enumerable
// false
上面代码中，toString和length属性的enumerable都是false，因此for...in不会遍历到这两个继承自原型的属性。
另外，ES6规定，所有Class的原型的方法都是不可枚举的。
Object.getOwnPropertyDescriptor(class {foo() {}}.prototype, 'foo').enumerable
// false
总的来说，操作中引入继承的属性会让问题复杂化，大多数时候，我们只关心对象自身的属性。所以，尽量不要用for...in循环，而
用Object.keys()代替。
9.7 属性的遍历
ES6一共有5种方法可以遍历对象的属性。
（1）for...in
for...in循环遍历对象自身的和继承的可枚举属性（不含Symbol属性）。
（2）Object.keys(obj)
Object.keys返回一个数组，包括对象自身的（不含继承的）所有可枚举属性（不含Symbol属性）。
（3）Object.getOwnPropertyNames(obj)
Object.getOwnPropertyNames返回一个数组，包含对象自身的所有属性（不含Symbol属性，但是包括不可枚举属性）。
（4）Object.getOwnPropertySymbols(obj)
Object.getOwnPropertySymbols返回一个数组，包含对象自身的所有Symbol属性。
（5）Reflect.ownKeys(obj)
Reflect.ownKeys返回一个数组，包含对象自身的所有属性，不管是属性名是Symbol或字符串，也不管是否可枚举。
以上的5种方法遍历对象的属性，都遵守同样的属性遍历的次序规则。
首先遍历所有属性名为数值的属性，按照数字排序。
其次遍历所有属性名为字符串的属性，按照生成时间排序。
最后遍历所有属性名为Symbol值的属性，按照生成时间排序。
Reflect.ownKeys({ [Symbol()]:0, b:0, 10:0, 2:0, a:0 })
// ['2', '10', 'b', 'a', Symbol()]
上面代码中，Reflect.ownKeys方法返回一个数组，包含了参数对象的所有属性。这个数组的属性次序是这样的，首先是数值属性2和10，其次是字符
串属性b和a，最后是Symbol属性。
9.8 __proto__属性，Object.setPrototypeOf()，Object.getPrototypeOf()
（1）__proto__属性
__proto__属性（前后各两个下划线），用来读取或设置当前对象的prototype对象。目前，所有浏览器（包括IE11）都部署了这个属性。
// es6的写法
var obj = {
method: function() { ... }
};
obj.__proto__ = someOtherObj;
// es5的写法
var obj = Object.create(someOtherObj);
obj.method = function() { ... };
该属性没有写入ES6的正文，而是写入了附录，原因是__proto__前后的双下划线，说明它本质上是一个内部属性，而不是一个正式的对外的API，只
是由于浏览器广泛支持，才被加入了ES6。标准明确规定，只有浏览器必须部署这个属性，其他运行环境不一定需要部署，而且新的代码最好认为这个
属性是不存在的。因此，无论从语义的角度，还是从兼容性的角度，都不要使用这个属性，而是使用下面的Object.setPrototypeOf()（写操
作）、Object.getPrototypeOf()（读操作）、Object.create()（生成操作）代替。
在实现上，__proto__调用的是Object.prototype.__proto__，具体实现如下。
Object.defineProperty(Object.prototype, '__proto__', {
get() {
let _thisObj = Object(this);
return Object.getPrototypeOf(_thisObj);
},
set(proto) {
if (this === undefined || this === null) {
throw new TypeError();
}
if (!isObject(this)) {
return undefined;
}
if (!isObject(proto)) {
return undefined;
}
let status = Reflect.setPrototypeOf(this, proto);
if (!status) {
throw new TypeError();
}
},
});
function isObject(value) {
return Object(value) === value;
}
如果一个对象本身部署了__proto__属性，则该属性的值就是对象的原型。
Object.getPrototypeOf({ __proto__: null })
// null
（2）Object.setPrototypeOf()
Object.setPrototypeOf方法的作用与__proto__相同，用来设置一个对象的prototype对象。它是ES6正式推荐的设置原型对象的方法。
// 格式
Object.setPrototypeOf(object, prototype)
// 用法
var o = Object.setPrototypeOf({}, null);
该方法等同于下面的函数。
function (obj, proto) {
obj.__proto__ = proto;
return obj;
}
下面是一个例子。
let proto = {};
let obj = { x: 10 };
Object.setPrototypeOf(obj, proto);
proto.y = 20;
proto.z = 40;
obj.x // 10
obj.y // 20
obj.z // 40
上面代码将proto对象设为obj对象的原型，所以从obj对象可以读取proto对象的属性。
（3）Object.getPrototypeOf()
该方法与setPrototypeOf方法配套，用于读取一个对象的prototype对象。
Object.getPrototypeOf(obj);
下面是一个例子。
function Rectangle() {
}
var rec = new Rectangle();
Object.getPrototypeOf(rec) === Rectangle.prototype
// true
Object.setPrototypeOf(rec, Object.prototype);
Object.getPrototypeOf(rec) === Rectangle.prototype
// false
9.9 Object.values()，Object.entries()
9.9.1 Object.keys()
ES5引入了Object.keys方法，返回一个数组，成员是参数对象自身的（不含继承的）所有可遍历（enumerable）属性的键名。
var obj = { foo: "bar", baz: 42 };
Object.keys(obj)
// ["foo", "baz"]
目前，ES7有一个提案，引入了跟Object.keys配套的Object.values和Object.entries。
let {keys, values, entries} = Object;
let obj = { a: 1, b: 2, c: 3 };
for (let key of keys(obj)) {
console.log(key); // 'a', 'b', 'c'
}
for (let value of values(obj)) {
console.log(value); // 1, 2, 3
}
for (let [key, value] of entries(obj)) {
console.log([key, value]); // ['a', 1], ['b', 2], ['c', 3]
}
9.9.2 Object.values()
Object.values方法返回一个数组，成员是参数对象自身的（不含继承的）所有可遍历（enumerable）属性的键值。
var obj = { foo: "bar", baz: 42 };
Object.values(obj)
// ["bar", 42]
返回数组的成员顺序，与本章的《属性的遍历》部分介绍的排列规则一致。
var obj = { 100: 'a', 2: 'b', 7: 'c' };
Object.values(obj)
// ["b", "c", "a"]
上面代码中，属性名为数值的属性，是按照数值大小，从小到大遍历的，因此返回的顺序是b、c、a。
Object.values只返回对象自身的可遍历属性。
var obj = Object.create({}, {p: {value: 42}});
Object.values(obj) // []
上面代码中，Object.create方法的第二个参数添加的对象属性（属性p），如果不显式声明，默认是不可遍历的。Object.values不会返回这个属性。
Object.values会过滤属性名为Symbol值的属性。
Object.values({ [Symbol()]: 123, foo: 'abc' });
// ['abc']
如果Object.values方法的参数是一个字符串，会返回各个字符组成的一个数组。
Object.values('foo')
// ['f', 'o', 'o']
上面代码中，字符串会先转成一个类似数组的对象。字符串的每个字符，就是该对象的一个属性。因此，Object.values返回每个属性的键值，就是各
个字符组成的一个数组。
如果参数不是对象，Object.values会先将其转为对象。由于数值和布尔值的包装对象，都不会为实例添加非继承的属性。所以，Object.values会返
回空数组。
Object.values(42) // []
Object.values(true) // []
9.9.3 Object.entries
Object.entries方法返回一个数组，成员是参数对象自身的（不含继承的）所有可遍历（enumerable）属性的键值对数组。
var obj = { foo: 'bar', baz: 42 };
Object.entries(obj)
// [ ["foo", "bar"], ["baz", 42] ]
除了返回值不一样，该方法的行为与Object.values基本一致。
如果原对象的属性名是一个Symbol值，该属性会被省略。
Object.entries({ [Symbol()]: 123, foo: 'abc' });
// [ [ 'foo', 'abc' ] ]
上面代码中，原对象有两个属性，Object.entries只输出属性名非Symbol值的属性。将来可能会有Reflect.ownEntries()方法，返回对象自身的所有
属性。
Object.entries的基本用途是遍历对象的属性。
let obj = { one: 1, two: 2 };
for (let [k, v] of Object.entries(obj)) {
console.log(`${JSON.stringify(k)}: ${JSON.stringify(v)}`);
}
// "one": 1
// "two": 2
Object.entries方法的一个用处是，将对象转为真正的Map结构。
var obj = { foo: 'bar', baz: 42 };
var map = new Map(Object.entries(obj));
map // Map { foo: "bar", baz: 42 }
自己实现Object.entries方法，非常简单。
// Generator函数的版本
function* entries(obj) {
for (let key of Object.keys(obj)) {
yield [key, obj[key]];
}
}
// 非Generator函数的版本
function entries(obj) {
let arr = [];
for (let key of Object.keys(obj)) {
arr.push([key, obj[key]]);
}
return arr;
}
9.10 对象的扩展运算符
目前，ES7有一个提案，将Rest解构赋值/扩展运算符（...）引入对象。Babel转码器已经支持这项功能。
（1）Rest解构赋值
对象的Rest解构赋值用于从一个对象取值，相当于将所有可遍历的、但尚未被读取的属性，分配到指定的对象上面。所有的键和它们的值，都会拷贝
到新对象上面。
let { x, y, ...z } = { x: 1, y: 2, a: 3, b: 4 };
x // 1
y // 2
z // { a: 3, b: 4 }
上面代码中，变量z是Rest解构赋值所在的对象。它获取等号右边的所有尚未读取的键（a和b），将它们和它们的值拷贝过来。
由于Rest解构赋值要求等号右边是一个对象，所以如果等号右边是undefined或null，就会报错，因为它们无法转为对象。
let { x, y, ...z } = null; // 运行时错误
let { x, y, ...z } = undefined; // 运行时错误
Rest解构赋值必须是最后一个参数，否则会报错。
let { ...x, y, z } = obj; // 句法错误
let { x, ...y, ...z } = obj; // 句法错误
上面代码中，Rest解构赋值不是最后一个参数，所以会报错。
注意，Rest解构赋值的拷贝是浅拷贝，即如果一个键的值是复合类型的值（数组、对象、函数）、那么Rest解构赋值拷贝的是这个值的引用，而不是
这个值的副本。
let obj = { a: { b: 1 } };
let { ...x } = obj;
obj.a.b = 2;
x.a.b // 2
上面代码中，x是Rest解构赋值所在的对象，拷贝了对象obj的a属性。a属性引用了一个对象，修改这个对象的值，会影响到Rest解构赋值对它的引
用。
另外，Rest解构赋值不会拷贝继承自原型对象的属性。
let o1 = { a: 1 };
let o2 = { b: 2 };
o2.__proto__ = o1;
let o3 = { ...o2 };
o3 // { b: 2 }
上面代码中，对象o3是o2的拷贝，但是只复制了o2自身的属性，没有复制它的原型对象o1的属性。
下面是另一个例子。
var o = Object.create({ x: 1, y: 2 });
o.z = 3;
let { x, ...{ y, z } } = o;
x // 1
y // undefined
z // 3
上面代码中，变量x是单纯的解构赋值，所以可以读取继承的属性；Rest解构赋值产生的变量y和z，只能读取对象自身的属性，所以只有变量z可以赋
值成功。
Rest解构赋值的一个用处，是扩展某个函数的参数，引入其他操作。
function baseFunction({ a, b }) {
// ...
}
function wrapperFunction({ x, y, ...restConfig }) {
// 使用x和y参数进行操作
// 其余参数传给原始函数
return baseFunction(restConfig);
}
上面代码中，原始函数baseFunction接受a和b作为参数，函数wrapperFunction在baseFunction的基础上进行了扩展，能够接受多余的参数，并且保
留原始函数的行为。
（2）扩展运算符
扩展运算符（...）用于取出参数对象的所有可遍历属性，拷贝到当前对象之中。
let z = { a: 3, b: 4 };
let n = { ...z };
n // { a: 3, b: 4 }
这等同于使用Object.assign方法。
let aClone = { ...a };
// 等同于
let aClone = Object.assign({}, a);
扩展运算符可以用于合并两个对象。
let ab = { ...a, ...b };
// 等同于
let ab = Object.assign({}, a, b);
如果用户自定义的属性，放在扩展运算符后面，则扩展运算符内部的同名属性会被覆盖掉。
let aWithOverrides = { ...a, x: 1, y: 2 };
// 等同于
let aWithOverrides = { ...a, ...{ x: 1, y: 2 } };
// 等同于
let x = 1, y = 2, aWithOverrides = { ...a, x, y };
// 等同于
let aWithOverrides = Object.assign({}, a, { x: 1, y: 2 });
上面代码中，a对象的x属性和y属性，拷贝到新对象后会被覆盖掉。
这用来修改现有对象部分的部分属性就很方便了。
let newVersion = {
...previousVersion,
name: 'New Name' // Override the name property
};
上面代码中，newVersion对象自定义了name属性，其他属性全部复制自previousVersion对象。
如果把自定义属性放在扩展运算符前面，就变成了设置新对象的默认属性值。
let aWithDefaults = { x: 1, y: 2, ...a };
// 等同于
let aWithDefaults = Object.assign({}, { x: 1, y: 2 }, a);
// 等同于
let aWithDefaults = Object.assign({ x: 1, y: 2 }, a);
扩展运算符的参数对象之中，如果有取值函数get，这个函数是会执行的。
// 并不会抛出错误，因为x属性只是被定义，但没执行
let aWithXGetter = {
...a,
get x() {
throws new Error('not thrown yet');
}
};
// 会抛出错误，因为x属性被执行了
let runtimeError = {
...a,
...{
get x() {
throws new Error('thrown now');
}
}
};
如果扩展运算符的参数是null或undefined，这个两个值会被忽略，不会报错。
let emptyObject = { ...null, ...undefined }; // 不报错
9.11 Object.getOwnPropertyDescriptors()
ES5有一个Object.getOwnPropertyDescriptor方法，返回某个对象属性的描述对象（descriptor）。
var obj = { p: 'a' };
Object.getOwnPropertyDescriptor(obj, 'p')
// Object { value: "a",
// writable: true,
// enumerable: true,
// configurable: true
// }
ES7有一个提案，提出了Object.getOwnPropertyDescriptors方法，返回指定对象所有自身属性（非继承属性）的描述对象。
const obj = {
foo: 123,
get bar() { return 'abc' }
};
Object.getOwnPropertyDescriptors(obj)
// { foo:
// { value: 123,
// writable: true,
// enumerable: true,
// configurable: true },
// bar:
// { get: [Function: bar],
// set: undefined,
// enumerable: true,
// configurable: true } }
Object.getOwnPropertyDescriptors方法返回一个对象，所有原对象的属性名都是该对象的属性名，对应的属性值就是该属性的描述对象。
该方法的实现非常容易。
function getOwnPropertyDescriptors(obj) {
const result = {};
for (let key of Reflect.ownKeys(obj)) {
result[key] = Object.getOwnPropertyDescriptor(obj, key);
}
return result;
}
该方法的提出目的，主要是为了解决Object.assign()无法正确拷贝get属性和set属性的问题。
const source = {
set foo(value) {
console.log(value);
}
};
const target1 = {};
Object.assign(target1, source);
Object.getOwnPropertyDescriptor(target1, 'foo')
// { value: undefined,
// writable: true,
// enumerable: true,
// configurable: true }
上面代码中，source对象的foo属性的值是一个赋值函数，Object.assign方法将这个属性拷贝给target1对象，结果该属性的值变成了undefined。这
是因为Object.assign方法总是拷贝一个属性的值，而不会拷贝它背后的赋值方法或取值方法。
这时，Object.getOwnPropertyDescriptors方法配合Object.defineProperties方法，就可以实现正确拷贝。
const source = {
set foo(value) {
console.log(value);
}
};
const target2 = {};
Object.defineProperties(target2, Object.getOwnPropertyDescriptors(source));
Object.getOwnPropertyDescriptor(target2, 'foo')
// { get: undefined,
// set: [Function: foo],
// enumerable: true,
// configurable: true }
上面代码中，将两个对象合并的逻辑提炼出来，就是下面这样。
const shallowMerge = (target, source) =&gt; Object.defineProperties(
target,
Object.getOwnPropertyDescriptors(source)
);
Object.getOwnPropertyDescriptors方法的另一个用处，是配合Object.create方法，将对象属性克隆到一个新对象。这属于浅拷贝。
const clone = Object.create(Object.getPrototypeOf(obj),
Object.getOwnPropertyDescriptors(obj));
// 或者
const shallowClone = (obj) =&gt; Object.create(
Object.getPrototypeOf(obj),
Object.getOwnPropertyDescriptors(obj)
);
上面代码会克隆对象obj。
另外，Object.getOwnPropertyDescriptors方法可以实现，一个对象继承另一个对象。以前，继承另一个对象，常常写成下面这样。
const obj = {
__proto__: prot,
foo: 123,
};
ES6规定__proto__只有浏览器要部署，其他环境不用部署。如果去除__proto__，上面代码就要改成下面这样。
const obj = Object.create(prot);
obj.foo = 123;
// 或者
const obj = Object.assign(
Object.create(prot),
{
foo: 123,
}
);
有了Object.getOwnPropertyDescriptors，我们就有了另一种写法。
const obj = Object.create(
prot,
Object.getOwnPropertyDescriptors({
foo: 123,
})
);
Object.getOwnPropertyDescriptors也可以用来实现Mixin（混入）模式。
let mix = (object) =&gt; ({
with: (...mixins) =&gt; mixins.reduce(
(c, mixin) =&gt; Object.create(
c, Object.getOwnPropertyDescriptors(mixin)
), object)
});
// multiple mixins example
let a = {a: 'a'};
let b = {b: 'b'};
let c = {c: 'c'};
let d = mix(c).with(a, b);
上面代码中，对象a和b被混入了对象c。
出于完整性的考虑，Object.getOwnPropertyDescriptors进入标准以后，还会有Reflect.getOwnPropertyDescriptors方法。
10 Symbol
10.1 概述
ES5的对象属性名都是字符串，这容易造成属性名的冲突。比如，你使用了一个他人提供的对象，但又想为这个对象添加新的方法（mixin模式），新
方法的名字就有可能与现有方法产生冲突。如果有一种机制，保证每个属性的名字都是独一无二的就好了，这样就从根本上防止属性名的冲突。这就
是ES6引入Symbol的原因。
ES6引入了一种新的原始数据类型Symbol，表示独一无二的值。它是JavaScript语言的第七种数据类型，前六种是：Undefined、Null、布尔值
（Boolean）、字符串（String）、数值（Number）、对象（Object）。
Symbol值通过Symbol函数生成。这就是说，对象的属性名现在可以有两种类型，一种是原来就有的字符串，另一种就是新增的Symbol类型。凡是属性
名属于Symbol类型，就都是独一无二的，可以保证不会与其他属性名产生冲突。
let s = Symbol();
typeof s
// "symbol"
上面代码中，变量s就是一个独一无二的值。typeof运算符的结果，表明变量s是Symbol数据类型，而不是字符串之类的其他类型。
注意，Symbol函数前不能使用new命令，否则会报错。这是因为生成的Symbol是一个原始类型的值，不是对象。也就是说，由于Symbol值不是对象，
所以不能添加属性。基本上，它是一种类似于字符串的数据类型。
Symbol函数可以接受一个字符串作为参数，表示对Symbol实例的描述，主要是为了在控制台显示，或者转为字符串时，比较容易区分。
var s1 = Symbol('foo');
var s2 = Symbol('bar');
s1 // Symbol(foo)
s2 // Symbol(bar)
s1.toString() // "Symbol(foo)"
s2.toString() // "Symbol(bar)"
上面代码中，s1和s2是两个Symbol值。如果不加参数，它们在控制台的输出都是Symbol()，不利于区分。有了参数以后，就等于为它们加上了描述，
输出的时候就能够分清，到底是哪一个值。
注意，Symbol函数的参数只是表示对当前Symbol值的描述，因此相同参数的Symbol函数的返回值是不相等的。
// 没有参数的情况
var s1 = Symbol();
var s2 = Symbol();
s1 === s2 // false
// 有参数的情况
var s1 = Symbol("foo");
var s2 = Symbol("foo");
s1 === s2 // false
上面代码中，s1和s2都是Symbol函数的返回值，而且参数相同，但是它们是不相等的。
Symbol值不能与其他类型的值进行运算，会报错。
var sym = Symbol('My symbol');
"your symbol is " + sym
// TypeError: can't convert symbol to string
`your symbol is ${sym}`
// TypeError: can't convert symbol to string
但是，Symbol值可以显式转为字符串。
var sym = Symbol('My symbol');
String(sym) // 'Symbol(My symbol)'
sym.toString() // 'Symbol(My symbol)'
另外，Symbol值也可以转为布尔值，但是不能转为数值。
var sym = Symbol();
Boolean(sym) // true
!sym // false
if (sym) {
// ...
}
Number(sym) // TypeError
sym + 2 // TypeError
10.2 作为属性名的Symbol
由于每一个Symbol值都是不相等的，这意味着Symbol值可以作为标识符，用于对象的属性名，就能保证不会出现同名的属性。这对于一个对象由多个
模块构成的情况非常有用，能防止某一个键被不小心改写或覆盖。
var mySymbol = Symbol();
// 第一种写法
var a = {};
a[mySymbol] = 'Hello!';
// 第二种写法
var a = {
[mySymbol]: 'Hello!'
};
// 第三种写法
var a = {};
Object.defineProperty(a, mySymbol, { value: 'Hello!' });
// 以上写法都得到同样结果
a[mySymbol] // "Hello!"
上面代码通过方括号结构和Object.defineProperty，将对象的属性名指定为一个Symbol值。
注意，Symbol值作为对象属性名时，不能用点运算符。
var mySymbol = Symbol();
var a = {};
a.mySymbol = 'Hello!';
a[mySymbol] // undefined
a['mySymbol'] // "Hello!"
上面代码中，因为点运算符后面总是字符串，所以不会读取mySymbol作为标识名所指代的那个值，导致a的属性名实际上是一个字符串，而不是一个
Symbol值。
同理，在对象的内部，使用Symbol值定义属性时，Symbol值必须放在方括号之中。
let s = Symbol();
let obj = {
[s]: function (arg) { ... }
};
obj[s](123);
上面代码中，如果s不放在方括号中，该属性的键名就是字符串s，而不是s所代表的那个Symbol值。
采用增强的对象写法，上面代码的obj对象可以写得更简洁一些。
let obj = {
[s](arg) { ... }
};
Symbol类型还可以用于定义一组常量，保证这组常量的值都是不相等的。
Symbol类型还可以用于定义一组常量，保证这组常量的值都是不相等的。
log.levels = {
DEBUG: Symbol('debug'),
INFO: Symbol('info'),
WARN: Symbol('warn')
};
log(log.levels.DEBUG, 'debug message');
log(log.levels.INFO, 'info message');
下面是另外一个例子。
const COLOR_RED = Symbol();
const COLOR_GREEN = Symbol();
function getComplement(color) {
switch (color) {
case COLOR_RED:
return COLOR_GREEN;
case COLOR_GREEN:
return COLOR_RED;
default:
throw new Error('Undefined color');
}
}
常量使用Symbol值最大的好处，就是其他任何值都不可能有相同的值了，因此可以保证上面的switch语句会按设计的方式工作。
还有一点需要注意，Symbol值作为属性名时，该属性还是公开属性，不是私有属性。
10.3 实例：消除魔术字符串
魔术字符串指的是，在代码之中多次出现、与代码形成强耦合的某一个具体的字符串或者数值。风格良好的代码，应该尽量消除魔术字符串，该由含
义清晰的变量代替。
function getArea(shape, options) {
var area = 0;
switch (shape) {
case 'Triangle': // 魔术字符串
area = .5 * options.width * options.height;
break;
/* ... more code ... */
}
return area;
}
getArea('Triangle', { width: 100, height: 100 }); // 魔术字符串
上面代码中，字符串“Triangle”就是一个魔术字符串。它多次出现，与代码形成“强耦合”，不利于将来的修改和维护。
常用的消除魔术字符串的方法，就是把它写成一个变量。
var shapeType = {
triangle: 'Triangle'
};
function getArea(shape, options) {
var area = 0;
switch (shape) {
case shapeType.triangle:
area = .5 * options.width * options.height;
break;
}
return area;
}
getArea(shapeType.triangle, { width: 100, height: 100 });
上面代码中，我们把“Triangle”写成shapeType对象的triangle属性，这样就消除了强耦合。
如果仔细分析，可以发现shapeType.triangle等于哪个值并不重要，只要确保不会跟其他shapeType属性的值冲突即可。因此，这里就很适合改用
Symbol值。
const shapeType = {
triangle: Symbol()
};
上面代码中，除了将shapeType.triangle的值设为一个Symbol，其他地方都不用修改。
10.4 属性名的遍历
Symbol作为属性名，该属性不会出现在for...in、for...of循环中，也不会被Object.keys()、Object.getOwnPropertyNames()返回。但是，它也不
是私有属性，有一个Object.getOwnPropertySymbols方法，可以获取指定对象的所有Symbol属性名。
Object.getOwnPropertySymbols方法返回一个数组，成员是当前对象的所有用作属性名的Symbol值。
var obj = {};
var a = Symbol('a');
var b = Symbol('b');
obj[a] = 'Hello';
obj[b] = 'World';
var objectSymbols = Object.getOwnPropertySymbols(obj);
objectSymbols
// [Symbol(a), Symbol(b)]
下面是另一个例子，Object.getOwnPropertySymbols方法与for...in循环、Object.getOwnPropertyNames方法进行对比的例子。
var obj = {};
var foo = Symbol("foo");
Object.defineProperty(obj, foo, {
value: "foobar",
});
for (var i in obj) {
console.log(i); // 无输出
}
Object.getOwnPropertyNames(obj)
// []
Object.getOwnPropertySymbols(obj)
// [Symbol(foo)]
上面代码中，使用Object.getOwnPropertyNames方法得不到Symbol属性名，需要使用Object.getOwnPropertySymbols方法。
另一个新的API，Reflect.ownKeys方法可以返回所有类型的键名，包括常规键名和Symbol键名。
let obj = {
[Symbol('my_key')]: 1,
enum: 2,
nonEnum: 3
};
Reflect.ownKeys(obj)
// [Symbol(my_key), 'enum', 'nonEnum']
由于以Symbol值作为名称的属性，不会被常规方法遍历得到。我们可以利用这个特性，为对象定义一些非私有的、但又希望只用于内部的方法。
var size = Symbol('size');
class Collection {
constructor() {
this[size] = 0;
}
add(item) {
this[this[size]] = item;
this[size]++;
}
static sizeOf(instance) {
return instance[size];
}
}
var x = new Collection();
Collection.sizeOf(x) // 0
x.add('foo');
Collection.sizeOf(x) // 1
Object.keys(x) // ['0']
Object.getOwnPropertyNames(x) // ['0']
Object.getOwnPropertySymbols(x) // [Symbol(size)]
上面代码中，对象x的size属性是一个Symbol值，所以Object.keys(x)、Object.getOwnPropertyNames(x)都无法获取它。这就造成了一种非私有的内
部方法的效果。
10.5 Symbol.for()，Symbol.keyFor()
有时，我们希望重新使用同一个Symbol值，Symbol.for方法可以做到这一点。它接受一个字符串作为参数，然后搜索有没有以该参数作为名称的
Symbol值。如果有，就返回这个Symbol值，否则就新建并返回一个以该字符串为名称的Symbol值。
var s1 = Symbol.for('foo');
var s2 = Symbol.for('foo');
s1 === s2 // true
上面代码中，s1和s2都是Symbol值，但是它们都是同样参数的Symbol.for方法生成的，所以实际上是同一个值。
Symbol.for()与Symbol()这两种写法，都会生成新的Symbol。它们的区别是，前者会被登记在全局环境中供搜索，后者不会。Symbol.for()不会每次
调用就返回一个新的Symbol类型的值，而是会先检查给定的key是否已经存在，如果不存在才会新建一个值。比如，如果你调用Symbol.for("cat")30
次，每次都会返回同一个Symbol值，但是调用Symbol("cat")30次，会返回30个不同的Symbol值。
Symbol.for("bar") === Symbol.for("bar")
// true
Symbol("bar") === Symbol("bar")
// false
上面代码中，由于Symbol()写法没有登记机制，所以每次调用都会返回一个不同的值。
Symbol.keyFor方法返回一个已登记的Symbol类型值的key。
var s1 = Symbol.for("foo");
Symbol.keyFor(s1) // "foo"
var s2 = Symbol("foo");
Symbol.keyFor(s2) // undefined
上面代码中，变量s2属于未登记的Symbol值，所以返回undefined。
需要注意的是，Symbol.for为Symbol值登记的名字，是全局环境的，可以在不同的iframe或service worker中取到同一个值。
iframe = document.createElement('iframe');
iframe.src = String(window.location);
document.body.appendChild(iframe);
iframe.contentWindow.Symbol.for('foo') === Symbol.for('foo')
// true
上面代码中，iframe窗口生成的Symbol值，可以在主页面得到。
10.6 实例：模块的 Singleton 模式
Singleton模式指的是调用一个类，任何时候返回的都是同一个实例。
对于 Node 来说，模块文件可以看成是一个类。怎么保证每次执行这个模块文件，返回的都是同一个实例呢？
很容易想到，可以把实例放到顶层对象global。
// mod.js
function A() {
this.foo = 'hello';
}
if (!global._foo) {
global._foo = new A();
}
module.exports = global._foo;
然后，加载上面的mod.js。
var a = require('./mod.js');
console.log(a.foo);
上面代码中，变量a任何时候加载的都是A的同一个实例。
但是，这里有一个问题，全局变量global._foo是可写的，任何文件都可以修改。
var a = require('./mod.js');
global._foo = 123;
上面的代码，会使得别的脚本加载mod.js都失真。
为了防止这种情况出现，我们就可以使用Symbol。
// mod.js
const FOO_KEY = Symbol.for('foo');
function A() {
this.foo = 'hello';
}
if (!global[FOO_KEY]) {
global[FOO_KEY] = new A();
}
module.exports = global[FOO_KEY];
上面代码中，可以保证global[FOO_KEY]不会被其他脚本改写。
10.7 内置的Symbol值
除了定义自己使用的Symbol值以外，ES6还提供了11个内置的Symbol值，指向语言内部使用的方法。
10.7.1 Symbol.hasInstance
对象的Symbol.hasInstance属性，指向一个内部方法。当其他对象使用instanceof运算符，判断是否为该对象的实例时，会调用这个方法。比
如，foo instanceof Foo在语言内部，实际调用的是Foo[Symbol.hasInstance](foo)。
class MyClass {
[Symbol.hasInstance](foo) {
return foo instanceof Array;
}
}
[1, 2, 3] instanceof new MyClass() // true
上面代码中，MyClass是一个类，new MyClass()会返回一个实例。该实例的Symbol.hasInstance方法，会在进行instanceof运算时自动调用，判断左
侧的运算子是否为Array的实例。
下面是另一个例子。
class Even {
static [Symbol.hasInstance](obj) {
return Number(obj) % 2 === 0;
}
}
1 instanceof Even // false
2 instanceof Even // true
12345 instanceof Even // false
10.7.2 Symbol.isConcatSpreadable
对象的Symbol.isConcatSpreadable属性等于一个布尔值，表示该对象使用Array.prototype.concat()时，是否可以展开。
let arr1 = ['c', 'd'];
['a', 'b'].concat(arr1, 'e') // ['a', 'b', 'c', 'd', 'e']
arr1[Symbol.isConcatSpreadable] // undefined
let arr2 = ['c', 'd'];
arr2[Symbol.isConcatSpreadable] = false;
['a', 'b'].concat(arr2, 'e') // ['a', 'b', ['c','d'], 'e']
上面代码说明，数组的默认行为是可以展开。Symbol.isConcatSpreadable属性等于true或undefined，都有这个效果。
类似数组的对象也可以展开，但它的Symbol.isConcatSpreadable属性默认为false，必须手动打开。
let obj = {length: 2, 0: 'c', 1: 'd'};
['a', 'b'].concat(obj, 'e') // ['a', 'b', obj, 'e']
obj[Symbol.isConcatSpreadable] = true;
['a', 'b'].concat(obj, 'e') // ['a', 'b', 'c', 'd', 'e']
对于一个类来说，Symbol.isConcatSpreadable属性必须写成实例的属性。
class A1 extends Array {
constructor(args) {
super(args);
this[Symbol.isConcatSpreadable] = true;
}
}
class A2 extends Array {
constructor(args) {
super(args);
this[Symbol.isConcatSpreadable] = false;
}
}
let a1 = new A1();
a1[0] = 3;
a1[1] = 4;
let a2 = new A2();
a2[0] = 5;
a2[1] = 6;
[1, 2].concat(a1).concat(a2)
// [1, 2, 3, 4, [5, 6]]
上面代码中，类A1是可展开的，类A2是不可展开的，所以使用concat时有不一样的结果。
10.7.3 Symbol.species
对象的Symbol.species属性，指向一个方法。该对象作为构造函数创造实例时，会调用这个方法。即如果this.constructor[Symbol.species]存在，
就会使用这个属性作为构造函数，来创造新的实例对象。
Symbol.species属性默认的读取器如下。
static get [Symbol.species]() {
return this;
}
10.7.4 Symbol.match
对象的Symbol.match属性，指向一个函数。当执行str.match(myObject)时，如果该属性存在，会调用它，返回该方法的返回值。
String.prototype.match(regexp)
// 等同于
regexp[Symbol.match](this)
class MyMatcher {
[Symbol.match](string) {
return 'hello world'.indexOf(string);
}
}
'e'.match(new MyMatcher()) // 1
10.7.5 Symbol.replace
对象的Symbol.replace属性，指向一个方法，当该对象被String.prototype.replace方法调用时，会返回该方法的返回值。
String.prototype.replace(searchValue, replaceValue)
// 等同于
searchValue[Symbol.replace](this, replaceValue)
10.7.6 Symbol.search
对象的Symbol.search属性，指向一个方法，当该对象被String.prototype.search方法调用时，会返回该方法的返回值。
String.prototype.search(regexp)
// 等同于
regexp[Symbol.search](this)
class MySearch {
constructor(value) {
this.value = value;
}
[Symbol.search](string) {
return string.indexOf(this.value);
}
}
'foobar'.search(new MySearch('foo')) // 0
10.7.7 Symbol.split
对象的Symbol.split属性，指向一个方法，当该对象被String.prototype.split方法调用时，会返回该方法的返回值。
String.prototype.split(separator, limit)
// 等同于
separator[Symbol.split](this, limit)
10.7.8 Symbol.iterator
对象的Symbol.iterator属性，指向该对象的默认遍历器方法。
var myIterable = {};
myIterable[Symbol.iterator] = function* () {
yield 1;
yield 2;
yield 3;
};
[...myIterable] // [1, 2, 3]
对象进行for...of循环时，会调用Symbol.iterator方法，返回该对象的默认遍历器，详细介绍参见《Iterator和for...of循环》一章。
class Collection {
*[Symbol.iterator]() {
let i = 0;
while(this[i] !== undefined) {
yield this[i];
++i;
}
}
}
let myCollection = new Collection();
myCollection[0] = 1;
myCollection[1] = 2;
for(let value of myCollection) {
console.log(value);
}
// 1
// 2
10.7.9 Symbol.toPrimitive
对象的Symbol.toPrimitive属性，指向一个方法。该对象被转为原始类型的值时，会调用这个方法，返回该对象对应的原始类型值。
Symbol.toPrimitive被调用时，会接受一个字符串参数，表示当前运算的模式，一共有三种模式。
Number：该场合需要转成数值
String：该场合需要转成字符串
Default：该场合可以转成数值，也可以转成字符串
let obj = {
[Symbol.toPrimitive](hint) {
switch (hint) {
case 'number':
return 123;
case 'string':
return 'str';
case 'default':
return 'default';
default:
throw new Error();
}
}
};
2 * obj // 246
3 + obj // '3default'
obj == 'default' // true
String(obj) // 'str'
10.7.10 Symbol.toStringTag
对象的Symbol.toStringTag属性，指向一个方法。在该对象上面调用Object.prototype.toString方法时，如果这个属性存在，它的返回值会出现
在toString方法返回的字符串之中，表示对象的类型。也就是说，这个属性可以用来定制[object Object]或[object Array]中object后面的那个字符
串。
({[Symbol.toStringTag]: 'Foo'}.toString())
// "[object Foo]"
class Collection {
get [Symbol.toStringTag]() {
return 'xxx';
}
}
var x = new Collection();
Object.prototype.toString.call(x) // "[object xxx]"
ES6新增内置对象的Symbol.toStringTag属性值如下。
JSON[Symbol.toStringTag]：'JSON'
Math[Symbol.toStringTag]：'Math'
Module对象M[Symbol.toStringTag]：'Module'
ArrayBuffer.prototype[Symbol.toStringTag]：'ArrayBuffer'
DataView.prototype[Symbol.toStringTag]：'DataView'
Map.prototype[Symbol.toStringTag]：'Map'
Promise.prototype[Symbol.toStringTag]：'Promise'
Set.prototype[Symbol.toStringTag]：'Set'
%TypedArray%.prototype[Symbol.toStringTag]：'Uint8Array'等
WeakMap.prototype[Symbol.toStringTag]：'WeakMap'
WeakSet.prototype[Symbol.toStringTag]：'WeakSet'
%MapIteratorPrototype%[Symbol.toStringTag]：'Map Iterator'
%SetIteratorPrototype%[Symbol.toStringTag]：'Set Iterator'
%StringIteratorPrototype%[Symbol.toStringTag]：'String Iterator'
Symbol.prototype[Symbol.toStringTag]：'Symbol'
Generator.prototype[Symbol.toStringTag]：'Generator'
GeneratorFunction.prototype[Symbol.toStringTag]：'GeneratorFunction'
10.7.10 Symbol.unscopables
对象的Symbol.unscopables属性，指向一个对象。该对象指定了使用with关键字时，哪些属性会被with环境排除。
Array.prototype[Symbol.unscopables]
// {
// copyWithin: true,
// entries: true,
// fill: true,
// find: true,
// findIndex: true,
// keys: true
// }
Object.keys(Array.prototype[Symbol.unscopables])
// ['copyWithin', 'entries', 'fill', 'find', 'findIndex', 'keys']
上面代码说明，数组有6个属性，会被with命令排除。
// 没有unscopables时
class MyClass {
foo() { return 1; }
}
var foo = function () { return 2; };
with (MyClass.prototype) {
foo(); // 1
}
// 有unscopables时
class MyClass {
foo() { return 1; }
get [Symbol.unscopables]() {
return { foo: true };
}
}
var foo = function () { return 2; };
with (MyClass.prototype) {
foo(); // 2
}
11 Proxy和Reflect
11.1 Proxy概述
Proxy用于修改某些操作的默认行为，等同于在语言层面做出修改，所以属于一种“元编程”（meta programming），即对编程语言进行编程。
Proxy可以理解成，在目标对象之前架设一层“拦截”，外界对该对象的访问，都必须先通过这层拦截，因此提供了一种机制，可以对外界的访问进行过
滤和改写。Proxy这个词的原意是代理，用在这里表示由它来“代理”某些操作，可以译为“代理器”。
var obj = new Proxy({}, {
get: function (target, key, receiver) {
console.log(`getting ${key}!`);
return Reflect.get(target, key, receiver);
},
set: function (target, key, value, receiver) {
console.log(`setting ${key}!`);
return Reflect.set(target, key, value, receiver);
}
});
上面代码对一个空对象架设了一层拦截，重定义了属性的读取（get）和设置（set）行为。这里暂时先不解释具体的语法，只看运行结果。对设置了
拦截行为的对象obj，去读写它的属性，就会得到下面的结果。
obj.count = 1
// setting count!
++obj.count
// getting count!
// setting count!
// 2
上面代码说明，Proxy实际上重载（overload）了点运算符，即用自己的定义覆盖了语言的原始定义。
ES6原生提供Proxy构造函数，用来生成Proxy实例。
var proxy = new Proxy(target, handler);
Proxy对象的所有用法，都是上面这种形式，不同的只是handler参数的写法。其中，new Proxy()表示生成一个Proxy实例，target参数表示所要拦截的
目标对象，handler参数也是一个对象，用来定制拦截行为。
下面是另一个拦截读取属性行为的例子。
var proxy = new Proxy({}, {
get: function(target, property) {
return 35;
}
});
proxy.time // 35
proxy.name // 35
proxy.title // 35
上面代码中，作为构造函数，Proxy接受两个参数。第一个参数是所要代理的目标对象（上例是一个空对象），即如果没有Proxy的介入，操作原来要
访问的就是这个对象；第二个参数是一个配置对象，对于每一个被代理的操作，需要提供一个对应的处理函数，该函数将拦截对应的操作。比如，上
面代码中，配置对象有一个get方法，用来拦截对目标对象属性的访问请求。get方法的两个参数分别是目标对象和所要访问的属性。可以看到，由于
拦截函数总是返回35，所以访问任何属性都得到35。
注意，要使得Proxy起作用，必须针对Proxy实例（上例是proxy对象）进行操作，而不是针对目标对象（上例是空对象）进行操作。
如果handler没有设置任何拦截，那就等同于直接通向原对象。
var target = {};
var handler = {};
var proxy = new Proxy(target, handler);
proxy.a = 'b';
target.a // "b"
上面代码中，handler是一个空对象，没有任何拦截效果，访问handeler就等同于访问target。
一个技巧是将Proxy对象，设置到object.proxy属性，从而可以在object对象上调用。
var object = { proxy: new Proxy(target, handler) };
Proxy实例也可以作为其他对象的原型对象。
var proxy = new Proxy({}, {
get: function(target, property) {
return 35;
}
});
let obj = Object.create(proxy);
obj.time // 35
上面代码中，proxy对象是obj对象的原型，obj对象本身并没有time属性，所以根据原型链，会在proxy对象上读取该属性，导致被拦截。
同一个拦截器函数，可以设置拦截多个操作。
var handler = {
get: function(target, name) {
if (name === 'prototype') {
return Object.prototype;
}
return 'Hello, ' + name;
},
apply: function(target, thisBinding, args) {
return args[0];
},
construct: function(target, args) {
return {value: args[1]};
}
};
var fproxy = new Proxy(function(x, y) {
return x + y;
}, handler);
fproxy(1, 2) // 1
new fproxy(1,2) // {value: 2}
fproxy.prototype === Object.prototype // true
fproxy.foo // "Hello, foo"
下面是Proxy支持的拦截操作一览。
对于可以设置、但没有设置拦截的操作，则直接落在目标对象上，按照原先的方式产生结果。
（1）get(target, propKey, receiver)
拦截对象属性的读取，比如proxy.foo和proxy['foo']。
最后一个参数receiver是一个对象，可选，参见下面Reflect.get的部分。
（2）set(target, propKey, value, receiver)
拦截对象属性的设置，比如proxy.foo = v或proxy['foo'] = v，返回一个布尔值。
（3）has(target, propKey)
拦截propKey in proxy的操作，以及对象的hasOwnProperty方法，返回一个布尔值。
（4）deleteProperty(target, propKey)
拦截delete proxy[propKey]的操作，返回一个布尔值。
（5）ownKeys(target)
拦截Object.getOwnPropertyNames(proxy)、Object.getOwnPropertySymbols(proxy)、Object.keys(proxy)，返回一个数组。该方法返回对象所有自
身的属性，而Object.keys()仅返回对象可遍历的属性。
（6）getOwnPropertyDescriptor(target, propKey)
拦截Object.getOwnPropertyDescriptor(proxy, propKey)，返回属性的描述对象。
（7）defineProperty(target, propKey, propDesc)
拦截Object.defineProperty(proxy, propKey, propDesc）、Object.defineProperties(proxy, propDescs)，返回一个布尔值。
（8）preventExtensions(target)
拦截Object.preventExtensions(proxy)，返回一个布尔值。
（9）getPrototypeOf(target)
拦截Object.getPrototypeOf(proxy)，返回一个对象。
（10）isExtensible(target)
拦截Object.isExtensible(proxy)，返回一个布尔值。
（11）setPrototypeOf(target, proto)
拦截Object.setPrototypeOf(proxy, proto)，返回一个布尔值。
如果目标对象是函数，那么还有两种额外操作可以拦截。
（12）apply(target, object, args)
拦截Proxy实例作为函数调用的操作，比如proxy(...args)、proxy.call(object, ...args)、proxy.apply(...)。
（13）construct(target, args)
拦截Proxy实例作为构造函数调用的操作，比如new proxy(...args)。
11.2 Proxy实例的方法
下面是上面这些拦截方法的详细介绍。
11.2.1 get()
get方法用于拦截某个属性的读取操作。上文已经有一个例子，下面是另一个拦截读取操作的例子。
var person = {
name: "张三"
};
var proxy = new Proxy(person, {
get: function(target, property) {
if (property in target) {
return target[property];
} else {
throw new ReferenceError("Property \"" + property + "\" does not exist.");
}
}
});
proxy.name // "张三"
proxy.age // 抛出一个错误
上面代码表示，如果访问目标对象不存在的属性，会抛出一个错误。如果没有这个拦截函数，访问不存在的属性，只会返回undefined。
get方法可以继承。
let proto = new Proxy({}, {
get(target, propertyKey, receiver) {
console.log('GET '+propertyKey);
return target[propertyKey];
}
});
let obj = Object.create(proto);
obj.xxx // "GET xxx"
上面代码中，拦截操作定义在Prototype对象上面，所以如果读取obj对象继承的属性时，拦截会生效。
下面的例子使用get拦截，实现数组读取负数的索引。
function createArray(...elements) {
let handler = {
get(target, propKey, receiver) {
let index = Number(propKey);
if (index &lt; 0) {
propKey = String(target.length + index);
}
return Reflect.get(target, propKey, receiver);
}
};
let target = [];
target.push(...elements);
return new Proxy(target, handler);
}
let arr = createArray('a', 'b', 'c');
arr[-1] // c
上面代码中，数组的位置参数是-1，就会输出数组的倒数最后一个成员。
利用Proxy，可以将读取属性的操作（get），转变为执行某个函数，从而实现属性的链式操作。
var pipe = (function () {
return function (value) {
var funcStack = [];
var oproxy = new Proxy({} , {
get : function (pipeObject, fnName) {
if (fnName === 'get') {
return funcStack.reduce(function (val, fn) {
return fn(val);
},value);
}
funcStack.push(window[fnName]);
return oproxy;
}
});
return oproxy;
}
}());
var double = n =&gt; n * 2;
var pow = n =&gt; n * n;
var reverseInt = n =&gt; n.toString().split("").reverse().join("") | 0;
pipe(3).double.pow.reverseInt.get; // 63
上面代码设置Proxy以后，达到了将函数名链式使用的效果。
下面的例子则是利用get拦截，实现一个生成各种DOM节点的通用函数dom。
const dom = new Proxy({}, {
get(target, property) {
return function(attrs = {}, ...children) {
const el = document.createElement(property);
for (let prop of Object.keys(attrs)) {
el.setAttribute(prop, attrs[prop]);
}
for (let child of children) {
if (typeof child === 'string') {
child = document.createTextNode(child);
}
el.appendChild(child);
}
return el;
}
}
});
const el = dom.div({},
'Hello, my name is ',
dom.a({href: '//example.com'}, 'Mark'),
'. I like:',
dom.ul({},
dom.li({}, 'The web'),
dom.li({}, 'Food'),
dom.li({}, '…actually that\'s it')
)
);
document.body.appendChild(el);
11.2.2 set()
set方法用来拦截某个属性的赋值操作。
假定Person对象有一个age属性，该属性应该是一个不大于200的整数，那么可以使用Proxy保证age的属性值符合要求。
let validator = {
set: function(obj, prop, value) {
if (prop === 'age') {
if (!Number.isInteger(value)) {
throw new TypeError('The age is not an integer');
}
if (value &gt; 200) {
throw new RangeError('The age seems invalid');
}
}
// 对于age以外的属性，直接保存
obj[prop] = value;
}
};
let person = new Proxy({}, validator);
person.age = 100;
person.age // 100
person.age = 'young' // 报错
person.age = 300 // 报错
上面代码中，由于设置了存值函数set，任何不符合要求的age属性赋值，都会抛出一个错误。利用set方法，还可以数据绑定，即每当对象发生变化
时，会自动更新DOM。
有时，我们会在对象上面设置内部属性，属性名的第一个字符使用下划线开头，表示这些属性不应该被外部使用。结合get和set方法，就可以做到防
止这些内部属性被外部读写。
var handler = {
get (target, key) {
invariant(key, 'get');
return target[key];
},
set (target, key, value) {
invariant(key, 'set');
return true;
}
};
function invariant (key, action) {
if (key[0] === '_') {
throw new Error(`Invalid attempt to ${action} private "${key}" property`);
}
}
var target = {};
var proxy = new Proxy(target, handler);
proxy._prop
// Error: Invalid attempt to get private "_prop" property
proxy._prop = 'c'
// Error: Invalid attempt to set private "_prop" property
// Error: Invalid attempt to set private "_prop" property
上面代码中，只要读写的属性名的第一个字符是下划线，一律抛错，从而达到禁止读写内部属性的目的。
11.2.3 apply()
apply方法拦截函数的调用、call和apply操作。
var handler = {
apply (target, ctx, args) {
return Reflect.apply(...arguments);
}
};
apply方法可以接受三个参数，分别是目标对象、目标对象的上下文对象（this）和目标对象的参数数组。
下面是一个例子。
var target = function () { return 'I am the target'; };
var handler = {
apply: function () {
return 'I am the proxy';
}
};
var p = new Proxy(target, handler);
p()
// "I am the proxy"
上面代码中，变量p是Proxy的实例，当它作为函数调用时（p()），就会被apply方法拦截，返回一个字符串。
下面是另外一个例子。
var twice = {
apply (target, ctx, args) {
return Reflect.apply(...arguments) * 2;
}
};
function sum (left, right) {
return left + right;
};
var proxy = new Proxy(sum, twice);
proxy(1, 2) // 6
proxy.call(null, 5, 6) // 22
proxy.apply(null, [7, 8]) // 30
上面代码中，每当执行proxy函数（直接调用或call和apply调用），就会被apply方法拦截。
另外，直接调用Reflect.apply方法，也会被拦截。
Reflect.apply(proxy, null, [9, 10]) // 38
11.2.4 has()
has方法用来拦截HasProperty操作，即判断对象是否具有某个属性时，这个方法会生效。典型的操作就是in运算符。
下面的例子使用has方法隐藏某些属性，不被in运算符发现。
var handler = {
has (target, key) {
if (key[0] === '_') {
return false;
}
return key in target;
}
};
var target = { _prop: 'foo', prop: 'foo' };
var proxy = new Proxy(target, handler);
'_prop' in proxy // false
上面代码中，如果原对象的属性名的第一个字符是下划线，proxy.has就会返回false，从而不会被in运算符发现。
如果原对象不可配置或者禁止扩展，这时has拦截会报错。
var obj = { a: 10 };
Object.preventExtensions(obj);
var p = new Proxy(obj, {
has: function(target, prop) {
return false;
}
});
'a' in p // TypeError is thrown
上面代码中，obj对象禁止扩展，结果使用has拦截就会报错。
值得注意的是，has方法拦截的是HasProperty操作，而不是HasOwnProperty操作，即has方法不判断一个属性是对象自身的属性，还是继承的属性。
由于for...in操作内部也会用到HasProperty操作，所以has方法在for...in循环时也会生效。
let stu1 = {name: 'Owen', score: 59};
let stu2 = {name: 'Mark', score: 99};
let handler = {
has(target, prop) {
if (prop === 'score' &amp;&amp; target[prop] &lt; 60) {
console.log(`${target.name} 不及格`);
return false;
}
return prop in target;
}
}
let oproxy1 = new Proxy(stu1, handler);
let oproxy2 = new Proxy(stu2, handler);
for (let a in oproxy1) {
console.log(oproxy1[a]);
}
// Owen
// Owen 不及格
for (let b in oproxy2) {
console.log(oproxy2[b]);
}
// Mark
// Mark 99
上面代码中，for...in循环时，has拦截会生效，导致不符合要求的属性被排除在for...in循环之外。
11.2.5 construct()
construct方法用于拦截new命令，下面是拦截对象的写法。
var handler = {
construct (target, args, newTarget) {
return new target(...args);
}
};
construct方法可以接受两个参数。
target: 目标对象
args：构建函数的参数对象
下面是一个例子。
var p = new Proxy(function() {}, {
construct: function(target, args) {
console.log('called: ' + args.join(', '));
return { value: args[0] * 10 };
}
});
new p(1).value
// "called: 1"
// 10
construct方法返回的必须是一个对象，否则会报错。
var p = new Proxy(function() {}, {
construct: function(target, argumentsList) {
return 1;
}
});
new p() // 报错
11.2.6 deleteProperty()
deleteProperty方法用于拦截delete操作，如果这个方法抛出错误或者返回false，当前属性就无法被delete命令删除。
var handler = {
deleteProperty (target, key) {
invariant(key, 'delete');
return true;
}
};
function invariant (key, action) {
if (key[0] === '_') {
throw new Error(`Invalid attempt to ${action} private "${key}" property`);
}
}
var target = { _prop: 'foo' };
var proxy = new Proxy(target, handler);
delete proxy._prop
// Error: Invalid attempt to delete private "_prop" property
上面代码中，deleteProperty方法拦截了delete操作符，删除第一个字符为下划线的属性会报错。
11.2.7 defineProperty()
defineProperty方法拦截了Object.defineProperty操作。
var handler = {
defineProperty (target, key, descriptor) {
return false;
}
};
var target = {};
var proxy = new Proxy(target, handler);
proxy.foo = 'bar'
// TypeError: proxy defineProperty handler returned false for property '"foo"'
上面代码中，defineProperty方法返回false，导致添加新属性会抛出错误。
11.2.8 getOwnPropertyDescriptor()
getOwnPropertyDescriptor方法拦截Object.getOwnPropertyDescriptor，返回一个属性描述对象或者undefined。
var handler = {
getOwnPropertyDescriptor (target, key) {
if (key[0] === '_') {
return;
}
return Object.getOwnPropertyDescriptor(target, key);
}
};
var target = { _foo: 'bar', baz: 'tar' };
var proxy = new Proxy(target, handler);
Object.getOwnPropertyDescriptor(proxy, 'wat')
// undefined
Object.getOwnPropertyDescriptor(proxy, '_foo')
// undefined
Object.getOwnPropertyDescriptor(proxy, 'baz')
// { value: 'tar', writable: true, enumerable: true, configurable: true }
上面代码中，handler.getOwnPropertyDescriptor方法对于第一个字符为下划线的属性名会返回undefined。
11.2.9 getPrototypeOf()
getPrototypeOf方法主要用来拦截Object.getPrototypeOf()运算符，以及其他一些操作。
Object.prototype.__proto__
Object.prototype.isPrototypeOf()
Object.getPrototypeOf()
Reflect.getPrototypeOf()
instanceof运算符
下面是一个例子。
var proto = {};
var p = new Proxy({}, {
getPrototypeOf(target) {
return proto;
}
});
Object.getPrototypeOf(p) === proto // true
上面代码中，getPrototypeOf方法拦截Object.getPrototypeOf()，返回proto对象。
11.2.10 isExtensible()
isExtensible方法拦截Object.isExtensible操作。
var p = new Proxy({}, {
isExtensible: function(target) {
console.log("called");
return true;
}
});
Object.isExtensible(p)
// "called"
// true
上面代码设置了isExtensible方法，在调用Object.isExtensible时会输出called。
这个方法有一个强限制，如果不能满足下面的条件，就会抛出错误。
Object.isExtensible(proxy) === Object.isExtensible(target)
下面是一个例子。
var p = new Proxy({}, {
isExtensible: function(target) {
return false;
}
});
Object.isExtensible(p) // 报错
11.2.11 ownKeys()
ownKeys方法用来拦截Object.keys()操作。
let target = {};
let handler = {
ownKeys(target) {
return ['hello', 'world'];
}
};
let proxy = new Proxy(target, handler);
Object.keys(proxy)
// [ 'hello', 'world' ]
上面代码拦截了对于target对象的Object.keys()操作，返回预先设定的数组。
下面的例子是拦截第一个字符为下划线的属性名。
let target = {
_bar: 'foo',
_prop: 'bar',
prop: 'baz'
};
let handler = {
ownKeys (target) {
return Reflect.ownKeys(target).filter(key =&gt; key[0] !== '_');
}
};
let proxy = new Proxy(target, handler);
for (let key of Object.keys(proxy)) {
console.log(target[key]);
}
// "baz"
11.2.12 preventExtensions()
preventExtensions方法拦截Object.preventExtensions()。该方法必须返回一个布尔值。
这个方法有一个限制，只有当Object.isExtensible(proxy)为false（即不可扩展）时，proxy.preventExtensions才能返回true，否则会报错。
var p = new Proxy({}, {
preventExtensions: function(target) {
return true;
}
});
Object.preventExtensions(p) // 报错
上面代码中，proxy.preventExtensions方法返回true，但这时Object.isExtensible(proxy)会返回true，因此报错。
为了防止出现这个问题，通常要在proxy.preventExtensions方法里面，调用一次Object.preventExtensions。
var p = new Proxy({}, {
preventExtensions: function(target) {
console.log("called");
Object.preventExtensions(target);
return true;
}
});
Object.preventExtensions(p)
// "called"
// true
11.2.13 setPrototypeOf()
setPrototypeOf方法主要用来拦截Object.setPrototypeOf方法。
下面是一个例子。
var handler = {
setPrototypeOf (target, proto) {
throw new Error('Changing the prototype is forbidden');
}
};
var proto = {};
var target = function () {};
var proxy = new Proxy(target, handler);
proxy.setPrototypeOf(proxy, proto);
// Error: Changing the prototype is forbidden
上面代码中，只要修改target的原型对象，就会报错。
11.3 Proxy.revocable()
Proxy.revocable方法返回一个可取消的Proxy实例。
let target = {};
let handler = {};
let {proxy, revoke} = Proxy.revocable(target, handler);
proxy.foo = 123;
proxy.foo // 123
revoke();
proxy.foo // TypeError: Revoked
Proxy.revocable方法返回一个对象，该对象的proxy属性是Proxy实例，revoke属性是一个函数，可以取消Proxy实例。上面代码中，当执行revoke函
数之后，再访问Proxy实例，就会抛出一个错误。
11.4 Reflect概述
Reflect对象与Proxy对象一样，也是ES6为了操作对象而提供的新API。Reflect对象的设计目的有这样几个。
（1） 将Object对象的一些明显属于语言内部的方法（比如Object.defineProperty），放到Reflect对象上。现阶段，某些方法同时
在Object和Reflect对象上部署，未来的新方法将只部署在Reflect对象上。
（2） 修改某些Object方法的返回结果，让其变得更合理。比如，Object.defineProperty(obj, name, desc)在无法定义属性时，会抛出一个错误，
而Reflect.defineProperty(obj, name, desc)则会返回false。
// 老写法
try {
Object.defineProperty(target, property, attributes);
// success
} catch (e) {
// failure
}
// 新写法
if (Reflect.defineProperty(target, property, attributes)) {
// success
} else {
// failure
}
（3） 让Object操作都变成函数行为。某些Object操作是命令式，比如name in obj和delete obj[name]，
而Reflect.has(obj, name)和Reflect.deleteProperty(obj, name)让它们变成了函数行为。
// 老写法
'assign' in Object // true
// 新写法
Reflect.has(Object, 'assign') // true
（4）Reflect对象的方法与Proxy对象的方法一一对应，只要是Proxy对象的方法，就能在Reflect对象上找到对应的方法。这就让Proxy对象可以方便
地调用对应的Reflect方法，完成默认行为，作为修改行为的基础。也就是说，不管Proxy怎么修改默认行为，你总可以在Reflect上获取默认行为。
Proxy(target, {
set: function(target, name, value, receiver) {
var success = Reflect.set(target,name, value, receiver);
if (success) {
log('property ' + name + ' on ' + target + ' set to ' + value);
}
return success;
}
});
上面代码中，Proxy方法拦截target对象的属性赋值行为。它采用Reflect.set方法将值赋值给对象的属性，然后再部署额外的功能。
下面是另一个例子。
var loggedObj = new Proxy(obj, {
get(target, name) {
console.log('get', target, name);
return Reflect.get(target, name);
},
deleteProperty(target, name) {
console.log('delete' + name);
return Reflect.deleteProperty(target, name);
},
has(target, name) {
console.log('has' + name);
return Reflect.has(target, name);
}
});
上面代码中，每一个Proxy对象的拦截操作（get、delete、has），内部都调用对应的Reflect方法，保证原生行为能够正常执行。添加的工作，就是
将每一个操作输出一行日志。
有了Reflect对象以后，很多操作会更易读。
// 老写法
Function.prototype.apply.call(Math.floor, undefined, [1.75]) // 1
// 新写法
Reflect.apply(Math.floor, undefined, [1.75]) // 1
11.5 Reflect对象的方法
Reflect对象的方法清单如下，共13个。
Reflect.apply(target,thisArg,args)
Reflect.construct(target,args)
Reflect.get(target,name,receiver)
Reflect.set(target,name,value,receiver)
Reflect.defineProperty(target,name,desc)
Reflect.deleteProperty(target,name)
Reflect.has(target,name)
Reflect.ownKeys(target)
Reflect.isExtensible(target)
Reflect.preventExtensions(target)
Reflect.getOwnPropertyDescriptor(target, name)
Reflect.getPrototypeOf(target)
Reflect.setPrototypeOf(target, prototype)
上面这些方法的作用，大部分与Object对象的同名方法的作用都是相同的，而且它与Proxy对象的方法是一一对应的。下面是对其中几个方法的解释。
（1）Reflect.get(target, name, receiver)
查找并返回target对象的name属性，如果没有该属性，则返回undefined。
如果name属性部署了读取函数，则读取函数的this绑定receiver。
var obj = {
get foo() { return this.bar(); },
bar: function() { ... }
};
// 下面语句会让 this.bar()
// 变成调用 wrapper.bar()
Reflect.get(obj, "foo", wrapper);
（2）Reflect.set(target, name, value, receiver)
设置target对象的name属性等于value。如果name属性设置了赋值函数，则赋值函数的this绑定receiver。
（3）Reflect.has(obj, name)
等同于name in obj。
（4）Reflect.deleteProperty(obj, name)
等同于delete obj[name]。
（5）Reflect.construct(target, args)
等同于new target(...args)，这提供了一种不使用new，来调用构造函数的方法。
（6）Reflect.getPrototypeOf(obj)
读取对象的__proto__属性，对应Object.getPrototypeOf(obj)。
（7）Reflect.setPrototypeOf(obj, newProto)
设置对象的__proto__属性，对应Object.setPrototypeOf(obj, newProto)。
（8）Reflect.apply(fun,thisArg,args)
等同于Function.prototype.apply.call(fun,thisArg,args)。一般来说，如果要绑定一个函数的this对象，可以这样写fn.apply(obj, args)，但是如
果函数定义了自己的apply方法，就只能写成Function.prototype.apply.call(fn, obj, args)，采用Reflect对象可以简化这种操作。
另外，需要注意的是，Reflect.set()、Reflect.defineProperty()、Reflect.freeze()、Reflect.seal()和Reflect.preventExtensions()返回一个
布尔值，表示操作是否成功。它们对应的Object方法，失败时都会抛出错误。
// 失败时抛出错误
Object.defineProperty(obj, name, desc);
// 失败时返回false
Reflect.defineProperty(obj, name, desc);
上面代码中，Reflect.defineProperty方法的作用与Object.defineProperty是一样的，都是为对象定义一个属性。但是，Reflect.defineProperty方
法失败时，不会抛出错误，只会返回false。
12 二进制数组
二进制数组（ArrayBuffer对象、TypedArray视图和DataView视图）是JavaScript操作二进制数据的一个接口。这些对象早就存在，属于独立的规格
（2011年2月发布），ES6将它们纳入了ECMAScript规格，并且增加了新的方法。
这个接口的原始设计目的，与WebGL项目有关。所谓WebGL，就是指浏览器与显卡之间的通信接口，为了满足JavaScript与显卡之间大量的、实时的
数据交换，它们之间的数据通信必须是二进制的，而不能是传统的文本格式。文本格式传递一个32位整数，两端的JavaScript脚本与显卡都要进行格式
转化，将非常耗时。这时要是存在一种机制，可以像C语言那样，直接操作字节，将4个字节的32位整数，以二进制形式原封不动地送入显卡，脚本的
性能就会大幅提升。
二进制数组就是在这种背景下诞生的。它很像C语言的数组，允许开发者以数组下标的形式，直接操作内存，大大增强了JavaScript处理二进制数据的
能力，使得开发者有可能通过JavaScript与操作系统的原生接口进行二进制通信。
二进制数组由三类对象组成。
（1）ArrayBuffer对象：代表内存之中的一段二进制数据，可以通过“视图”进行操作。“视图”部署了数组接口，这意味着，可以用数组的方法操作内
存。
（2）TypedArray视图：共包括9种类型的视图，比如Uint8Array（无符号8位整数）数组视图, Int16Array（16位整数）数组视图,
Float32Array（32位浮点数）数组视图等等。
（3）DataView视图：可以自定义复合格式的视图，比如第一个字节是Uint8（无符号8位整数）、第二、三个字节是Int16（16位整数）、第四个字节
开始是Float32（32位浮点数）等等，此外还可以自定义字节序。
简单说，ArrayBuffer对象代表原始的二进制数据，TypedArray视图用来读写简单类型的二进制数据，DataView视图用来读写复杂类型的二进制数
据。
TypedArray视图支持的数据类型一共有9种（DataView视图支持除Uint8C以外的其他8种）。
数据类型 字节长度 含义 对应的C语言类型
Int8 1 8位带符号整数 signed char
Uint8 1 8位不带符号整数 unsigned char
Uint8C 1 8位不带符号整数（自动过滤溢出） unsigned char
Int16 2 16位带符号整数 short
Uint16 2 16位不带符号整数 unsigned short
Int32 4 32位带符号整数 int
Uint32 4 32位不带符号的整数 unsigned int
Float32 4 32位浮点数 float
Float64 8 64位浮点数 double
注意，二进制数组并不是真正的数组，而是类似数组的对象。
很多浏览器操作的API，用到了二进制数组操作二进制数据，下面是其中的几个。
File API
XMLHttpRequest
Fetch API
Canvas
WebSockets
12.1 ArrayBuffer对象
12.1.1 概述
ArrayBuffer对象代表储存二进制数据的一段内存，它不能直接读写，只能通过视图（TypedArray视图和DataView视图)来读写，视图的作用是以指定
格式解读二进制数据。
ArrayBuffer也是一个构造函数，可以分配一段可以存放数据的连续内存区域。
var buf = new ArrayBuffer(32);
上面代码生成了一段32字节的内存区域，每个字节的值默认都是0。可以看到，ArrayBuffer构造函数的参数是所需要的内存大小（单位字节）。
为了读写这段内容，需要为它指定视图。DataView视图的创建，需要提供ArrayBuffer对象实例作为参数。
var buf = new ArrayBuffer(32);
var dataView = new DataView(buf);
dataView.getUint8(0) // 0
上面代码对一段32字节的内存，建立DataView视图，然后以不带符号的8位整数格式，读取第一个元素，结果得到0，因为原始内存的ArrayBuffer对
象，默认所有位都是0。
另一种TypedArray视图，与DataView视图的一个区别是，它不是一个构造函数，而是一组构造函数，代表不同的数据格式。
var buffer = new ArrayBuffer(12);
var x1 = new Int32Array(buffer);
x1[0] = 1;
var x2 = new Uint8Array(buffer);
x2[0] = 2;
x1[0] // 2
上面代码对同一段内存，分别建立两种视图：32位带符号整数（Int32Array构造函数）和8位不带符号整数（Uint8Array构造函数）。由于两个视图
对应的是同一段内存，一个视图修改底层内存，会影响到另一个视图。
TypedArray视图的构造函数，除了接受ArrayBuffer实例作为参数，还可以接受普通数组作为参数，直接分配内存生成底层的ArrayBuffer实例，并同
时完成对这段内存的赋值。
var typedArray = new Uint8Array([0,1,2]);
typedArray.length // 3
typedArray[0] = 5;
typedArray // [5, 1, 2]
上面代码使用TypedArray视图的Uint8Array构造函数，新建一个不带符号的8位整数视图。可以看到，Uint8Array直接使用普通数组作为参数，对底
层内存的赋值同时完成。
12.1.2 ArrayBuffer.prototype.byteLength
ArrayBuffer实例的byteLength属性，返回所分配的内存区域的字节长度。
var buffer = new ArrayBuffer(32);
buffer.byteLength
// 32
如果要分配的内存区域很大，有可能分配失败（因为没有那么多的连续空余内存），所以有必要检查是否分配成功。
if (buffer.byteLength === n) {
// 成功
} else {
// 失败
}
12.1.3 ArrayBuffer.prototype.slice()
ArrayBuffer实例有一个slice方法，允许将内存区域的一部分，拷贝生成一个新的ArrayBuffer对象。
var buffer = new ArrayBuffer(8);
var newBuffer = buffer.slice(0, 3);
上面代码拷贝buffer对象的前3个字节（从0开始，到第3个字节前面结束），生成一个新的ArrayBuffer对象。slice方法其实包含两步，第一步是先
分配一段新内存，第二步是将原来那个ArrayBuffer对象拷贝过去。
slice方法接受两个参数，第一个参数表示拷贝开始的字节序号（含该字节），第二个参数表示拷贝截止的字节序号（不含该字节）。如果省略第二个
参数，则默认到原ArrayBuffer对象的结尾。
除了slice方法，ArrayBuffer对象不提供任何直接读写内存的方法，只允许在其上方建立视图，然后通过视图读写。
12.1.4 ArrayBuffer.isView()
ArrayBuffer有一个静态方法isView，返回一个布尔值，表示参数是否为ArrayBuffer的视图实例。这个方法大致相当于判断参数，是否为TypedArray
实例或DataView实例。
var buffer = new ArrayBuffer(8);
ArrayBuffer.isView(buffer) // false
var v = new Int32Array(buffer);
ArrayBuffer.isView(v) // true
12.2 TypedArray视图
12.2.1 概述
ArrayBuffer对象作为内存区域，可以存放多种类型的数据。同一段内存，不同数据有不同的解读方式，这就叫做“视图”（view）。ArrayBuffer有两种
视图，一种是TypedArray视图，另一种是DataView视图。前者的数组成员都是同一个数据类型，后者的数组成员可以是不同的数据类型。
目前，TypedArray视图一共包括9种类型，每一种视图都是一种构造函数。
Int8Array：8位有符号整数，长度1个字节。
Uint8Array：8位无符号整数，长度1个字节。
Uint8ClampedArray：8位无符号整数，长度1个字节，溢出处理不同。
Int16Array：16位有符号整数，长度2个字节。
Uint16Array：16位无符号整数，长度2个字节。
Int32Array：32位有符号整数，长度4个字节。
Uint32Array：32位无符号整数，长度4个字节。
Float32Array：32位浮点数，长度4个字节。
Float64Array：64位浮点数，长度8个字节。
这9个构造函数生成的数组，统称为TypedArray视图。它们很像普通数组，都有length属性，都能用方括号运算符（[]）获取单个元素，所有数组的
方法，在它们上面都能使用。普通数组与TypedArray数组的差异主要在以下方面。
TypedArray数组的所有成员，都是同一种类型。
TypedArray数组的成员是连续的，不会有空位。
TypedArray数组成员的默认值为0。比如，new Array(10)返回一个普通数组，里面没有任何成员，只是10个空位；new Uint8Array(10)返回一个
TypedArray数组，里面10个成员都是0。
TypedArray数组只是一层视图，本身不储存数据，它的数据都储存在底层的ArrayBuffer对象之中，要获取底层对象必须使用buffer属性。
12.2.2 构造函数
TypedArray数组提供9种构造函数，用来生成相应类型的数组实例。
构造函数有多种用法。
（1）TypedArray(buffer, byteOffset=0, length?)
同一个ArrayBuffer对象之上，可以根据不同的数据类型，建立多个视图。
// 创建一个8字节的ArrayBuffer
var b = new ArrayBuffer(8);
// 创建一个指向b的Int32视图，开始于字节0，直到缓冲区的末尾
var v1 = new Int32Array(b);
// 创建一个指向b的Uint8视图，开始于字节2，直到缓冲区的末尾
var v2 = new Uint8Array(b, 2);
// 创建一个指向b的Int16视图，开始于字节2，长度为2
var v3 = new Int16Array(b, 2, 2);
上面代码在一段长度为8个字节的内存（b）之上，生成了三个视图：v1、v2和v3。
视图的构造函数可以接受三个参数：
第一个参数（必需）：视图对应的底层ArrayBuffer对象。
第二个参数（可选）：视图开始的字节序号，默认从0开始。
第三个参数（可选）：视图包含的数据个数，默认直到本段内存区域结束。
因此，v1、v2和v3是重叠的：v1[0]是一个32位整数，指向字节0～字节3；v2[0]是一个8位无符号整数，指向字节2；v3[0]是一个16位整数，指向字
节2～字节3。只要任何一个视图对内存有所修改，就会在另外两个视图上反应出来。
注意，byteOffset必须与所要建立的数据类型一致，否则会报错。
var buffer = new ArrayBuffer(8);
var i16 = new Int16Array(buffer, 1);
// Uncaught RangeError: start offset of Int16Array should be a multiple of 2
上面代码中，新生成一个8个字节的ArrayBuffer对象，然后在这个对象的第一个字节，建立带符号的16位整数视图，结果报错。因为，带符号的16位
整数需要两个字节，所以byteOffset参数必须能够被2整除。
如果想从任意字节开始解读ArrayBuffer对象，必须使用DataView视图，因为TypedArray视图只提供9种固定的解读格式。
（2）TypedArray(length)
视图还可以不通过ArrayBuffer对象，直接分配内存而生成。
var f64a = new Float64Array(8);
f64a[0] = 10;
f64a[1] = 20;
f64a[2] = f64a[0] + f64a[1];
上面代码生成一个8个成员的Float64Array数组（共64字节），然后依次对每个成员赋值。这时，视图构造函数的参数就是成员的个数。可以看到，视
图数组的赋值操作与普通数组的操作毫无两样。
（3）TypedArray(typedArray)
TypedArray数组的构造函数，可以接受另一个TypedArray实例作为参数。
var typedArray = new Int8Array(new Uint8Array(4));
上面代码中，Int8Array构造函数接受一个Uint8Array实例作为参数。
注意，此时生成的新数组，只是复制了参数数组的值，对应的底层内存是不一样的。新数组会开辟一段新的内存储存数据，不会在原数组的内存之上
建立视图。
var x = new Int8Array([1, 1]);
var y = new Int8Array(x);
x[0] // 1
y[0] // 1
x[0] = 2;
y[0] // 1
上面代码中，数组y是以数组x为模板而生成的，当x变动的时候，y并没有变动。
如果想基于同一段内存，构造不同的视图，可以采用下面的写法。
var x = new Int8Array([1, 1]);
var y = new Int8Array(x.buffer);
x[0] // 1
y[0] // 1
x[0] = 2;
y[0] // 2
（4）TypedArray(arrayLikeObject)
构造函数的参数也可以是一个普通数组，然后直接生成TypedArray实例。
var typedArray = new Uint8Array([1, 2, 3, 4]);
注意，这时TypedArray视图会重新开辟内存，不会在原数组的内存上建立视图。
上面代码从一个普通的数组，生成一个8位无符号整数的TypedArray实例。
TypedArray数组也可以转换回普通数组。
var normalArray = Array.prototype.slice.call(typedArray);
12.2.3 数组方法
普通数组的操作方法和属性，对TypedArray数组完全适用。
TypedArray.prototype.copyWithin(target, start[, end = this.length])
TypedArray.prototype.entries()
TypedArray.prototype.every(callbackfn, thisArg?)
TypedArray.prototype.fill(value, start=0, end=this.length)
TypedArray.prototype.filter(callbackfn, thisArg?)
TypedArray.prototype.find(predicate, thisArg?)
TypedArray.prototype.findIndex(predicate, thisArg?)
TypedArray.prototype.forEach(callbackfn, thisArg?)
TypedArray.prototype.indexOf(searchElement, fromIndex=0)
TypedArray.prototype.join(separator)
TypedArray.prototype.keys()
TypedArray.prototype.lastIndexOf(searchElement, fromIndex?)
TypedArray.prototype.map(callbackfn, thisArg?)
TypedArray.prototype.reduce(callbackfn, initialValue?)
TypedArray.prototype.reduceRight(callbackfn, initialValue?)
TypedArray.prototype.reverse()
TypedArray.prototype.slice(start=0, end=this.length)
TypedArray.prototype.some(callbackfn, thisArg?)
TypedArray.prototype.sort(comparefn)
TypedArray.prototype.toLocaleString(reserved1?, reserved2?)
TypedArray.prototype.toString()
TypedArray.prototype.values()
上面所有方法的用法，请参阅数组方法的介绍，这里不再重复了。
注意，TypedArray数组没有concat方法。如果想要合并多个TypedArray数组，可以用下面这个函数。
function concatenate(resultConstructor, ...arrays) {
let totalLength = 0;
for (let arr of arrays) {
totalLength += arr.length;
}
let result = new resultConstructor(totalLength);
let offset = 0;
for (let arr of arrays) {
result.set(arr, offset);
offset += arr.length;
}
return result;
}
concatenate(Uint8Array, Uint8Array.of(1, 2), Uint8Array.of(3, 4))
// Uint8Array [1, 2, 3, 4]
另外，TypedArray数组与普通数组一样，部署了Iterator接口，所以可以被遍历。
let ui8 = Uint8Array.of(0, 1, 2);
for (let byte of ui8) {
console.log(byte);
}
// 0
// 1
// 2
12.2.4 字节序
字节序指的是数值在内存中的表示方式。
var buffer = new ArrayBuffer(16);
var int32View = new Int32Array(buffer);
for (var i = 0; i &lt; int32View.length; i++) {
int32View[i] = i * 2;
}
上面代码生成一个16字节的ArrayBuffer对象，然后在它的基础上，建立了一个32位整数的视图。由于每个32位整数占据4个字节，所以一共可以写入
4个整数，依次为0，2，4，6。
如果在这段数据上接着建立一个16位整数的视图，则可以读出完全不一样的结果。
var int16View = new Int16Array(buffer);
for (var i = 0; i &lt; int16View.length; i++) {
console.log("Entry " + i + ": " + int16View[i]);
}
// Entry 0: 0
// Entry 1: 0
// Entry 2: 2
// Entry 3: 0
// Entry 4: 4
// Entry 5: 0
// Entry 6: 6
// Entry 7: 0
由于每个16位整数占据2个字节，所以整个ArrayBuffer对象现在分成8段。然后，由于x86体系的计算机都采用小端字节序（little endian），相对重要
的字节排在后面的内存地址，相对不重要字节排在前面的内存地址，所以就得到了上面的结果。
比如，一个占据四个字节的16进制数0x12345678，决定其大小的最重要的字节是“12”，最不重要的是“78”。小端字节序将最不重要的字节排在前面，
储存顺序就是78563412；大端字节序则完全相反，将最重要的字节排在前面，储存顺序就是12345678。目前，所有个人电脑几乎都是小端字节序，所
以TypedArray数组内部也采用小端字节序读写数据，或者更准确的说，按照本机操作系统设定的字节序读写数据。
这并不意味大端字节序不重要，事实上，很多网络设备和特定的操作系统采用的是大端字节序。这就带来一个严重的问题：如果一段数据是大端字节
序，TypedArray数组将无法正确解析，因为它只能处理小端字节序！为了解决这个问题，JavaScript引入DataView对象，可以设定字节序，下文会详
细介绍。
下面是另一个例子。
// 假定某段buffer包含如下字节 [0x02, 0x01, 0x03, 0x07]
var buffer = new ArrayBuffer(4);
var v1 = new Uint8Array(buffer);
v1[0] = 2;
v1[1] = 1;
v1[2] = 3;
v1[3] = 7;
var uInt16View = new Uint16Array(buffer);
// 计算机采用小端字节序
// 所以头两个字节等于258
if (uInt16View[0] === 258) {
console.log('OK'); // "OK"
}
// 赋值运算
uInt16View[0] = 255; // 字节变为[0xFF, 0x00, 0x03, 0x07]
uInt16View[0] = 0xff05; // 字节变为[0x05, 0xFF, 0x03, 0x07]
uInt16View[1] = 0x0210; // 字节变为[0x05, 0xFF, 0x10, 0x02]
下面的函数可以用来判断，当前视图是小端字节序，还是大端字节序。
const BIG_ENDIAN = Symbol('BIG_ENDIAN');
const LITTLE_ENDIAN = Symbol('LITTLE_ENDIAN');
function getPlatformEndianness() {
let arr32 = Uint32Array.of(0x12345678);
let arr8 = new Uint8Array(arr32.buffer);
switch ((arr8[0]*0x1000000) + (arr8[1]*0x10000) + (arr8[2]*0x100) + (arr8[3])) {
case 0x12345678:
return BIG_ENDIAN;
case 0x78563412:
return LITTLE_ENDIAN;
default:
throw new Error('Unknown endianness');
}
}
总之，与普通数组相比，TypedArray数组的最大优点就是可以直接操作内存，不需要数据类型转换，所以速度快得多。
12.2.5 BYTES_PER_ELEMENT属性
每一种视图的构造函数，都有一个BYTES_PER_ELEMENT属性，表示这种数据类型占据的字节数。
Int8Array.BYTES_PER_ELEMENT // 1
Uint8Array.BYTES_PER_ELEMENT // 1
Int16Array.BYTES_PER_ELEMENT // 2
Uint16Array.BYTES_PER_ELEMENT // 2
Int32Array.BYTES_PER_ELEMENT // 4
Uint32Array.BYTES_PER_ELEMENT // 4
Float32Array.BYTES_PER_ELEMENT // 4
Float64Array.BYTES_PER_ELEMENT // 8
这个属性在TypedArray实例上也能获取，即有TypedArray.prototype.BYTES_PER_ELEMENT。
12.2.6 ArrayBuffer与字符串的互相转换
ArrayBuffer转为字符串，或者字符串转为ArrayBuffer，有一个前提，即字符串的编码方法是确定的。假定字符串采用UTF-16编码（JavaScript的内
部编码方式），可以自己编写转换函数。
// ArrayBuffer转为字符串，参数为ArrayBuffer对象
function ab2str(buf) {
return String.fromCharCode.apply(null, new Uint16Array(buf));
}
// 字符串转为ArrayBuffer对象，参数为字符串
function str2ab(str) {
var buf = new ArrayBuffer(str.length * 2); // 每个字符占用2个字节
var bufView = new Uint16Array(buf);
for (var i = 0, strLen = str.length; i &lt; strLen; i++) {
bufView[i] = str.charCodeAt(i);
}
return buf;
}
12.2.7 溢出
不同的视图类型，所能容纳的数值范围是确定的。超出这个范围，就会出现溢出。比如，8位视图只能容纳一个8位的二进制值，如果放入一个9位的
值，就会溢出。
TypedArray数组的溢出处理规则，简单来说，就是抛弃溢出的位，然后按照视图类型进行解释。
var uint8 = new Uint8Array(1);
uint8[0] = 256;
uint8[0] // 0
uint8[0] = -1;
uint8[0] // 255
上面代码中，uint8是一个8位视图，而256的二进制形式是一个9位的值100000000，这时就会发生溢出。根据规则，只会保留后8位，
即00000000。uint8视图的解释规则是无符号的8位整数，所以00000000就是0。
负数在计算机内部采用“2的补码”表示，也就是说，将对应的正数值进行否运算，然后加1。比如，-1对应的正值是1，进行否运算以后，得
到11111110，再加上1就是补码形式11111111。uint8按照无符号的8位整数解释11111111，返回结果就是255。
一个简单转换规则，可以这样表示。
正向溢出（overflow）：当输入值大于当前数据类型的最大值，结果等于当前数据类型的最小值加上余值，再减去1。
负向溢出（underflow）：当输入值小于当前数据类型的最小值，结果等于当前数据类型的最大值减去余值，再加上1。
请看下面的例子。
var int8 = new Int8Array(1);
int8[0] = 128;
int8[0] // -128
int8[0] = -129;
int8[0] // 127
上面例子中，int8是一个带符号的8位整数视图，它的最大值是127，最小值是-128。输入值为128时，相当于正向溢出1，根据“最小值加上余值，再
减去1”的规则，就会返回-128；输入值为-129时，相当于负向溢出1，根据“最大值减去余值，再加上1”的规则，就会返回127。
Uint8ClampedArray视图的溢出规则，与上面的规则不同。它规定，凡是发生正向溢出，该值一律等于当前数据类型的最大值，即255；如果发生负向
溢出，该值一律等于当前数据类型的最小值，即0。
var uint8c = new Uint8ClampedArray(1);
uint8c[0] = 256;
uint8c[0] // 255
uint8c[0] = -1;
uint8c[0] // 0
上面例子中，uint8C是一个Uint8ClampedArray视图，正向溢出时都返回255，负向溢出都返回0。
12.2.8 TypedArray.prototype.buffer
TypedArray实例的buffer属性，返回整段内存区域对应的ArrayBuffer对象。该属性为只读属性。
var a = new Float32Array(64);
var b = new Uint8Array(a.buffer);
上面代码的a视图对象和b视图对象，对应同一个ArrayBuffer对象，即同一段内存。
12.2.9 TypedArray.prototype.byteLength，TypedArray.prototype.byteOffset
byteLength属性返回TypedArray数组占据的内存长度，单位为字节。byteOffset属性返回TypedArray数组从底层ArrayBuffer对象的哪个字节开始。
这两个属性都是只读属性。
var b = new ArrayBuffer(8);
var v1 = new Int32Array(b);
var v2 = new Uint8Array(b, 2);
var v3 = new Int16Array(b, 2, 2);
v1.byteLength // 8
v2.byteLength // 6
v3.byteLength // 4
v1.byteOffset // 0
v2.byteOffset // 2
v3.byteOffset // 2
12.2.10 TypedArray.prototype.length
length属性表示TypedArray数组含有多少个成员。注意将byteLength属性和length属性区分，前者是字节长度，后者是成员长度。
var a = new Int16Array(8);
a.length // 8
a.byteLength // 16
12.2.11 TypedArray.prototype.set()
TypedArray数组的set方法用于复制数组（普通数组或TypedArray数组），也就是将一段内容完全复制到另一段内存。
var a = new Uint8Array(8);
var b = new Uint8Array(8);
b.set(a);
上面代码复制a数组的内容到b数组，它是整段内存的复制，比一个个拷贝成员的那种复制快得多。
set方法还可以接受第二个参数，表示从b对象的哪一个成员开始复制a对象。
var a = new Uint16Array(8);
var b = new Uint16Array(10);
b.set(a, 2)
上面代码的b数组比a数组多两个成员，所以从b[2]开始复制。
12.2.12 TypedArray.prototype.subarray()
subarray方法是对于TypedArray数组的一部分，再建立一个新的视图。
var a = new Uint16Array(8);
var b = a.subarray(2,3);
a.byteLength // 16
b.byteLength // 2
subarray方法的第一个参数是起始的成员序号，第二个参数是结束的成员序号（不含该成员），如果省略则包含剩余的全部成员。所以，上面代码
的a.subarray(2,3)，意味着b只包含a[2]一个成员，字节长度为2。
12.2.13 TypedArray.prototype.slice()
TypeArray实例的slice方法，可以返回一个指定位置的新的TypedArray实例。
let ui8 = Uint8Array.of(0, 1, 2);
ui8.slice(-1)
// Uint8Array [ 2 ]
上面代码中，ui8是8位无符号整数数组视图的一个实例。它的slice方法可以从当前视图之中，返回一个新的视图实例。
slice方法的参数，表示原数组的具体位置，开始生成新数组。负值表示逆向的位置，即-1为倒数第一个位置，-2表示倒数第二个位置，以此类推。
12.2.14 TypedArray.of()
TypedArray数组的所有构造函数，都有一个静态方法of，用于将参数转为一个TypedArray实例。
Float32Array.of(0.151, -8, 3.7)
// Float32Array [ 0.151, -8, 3.7 ]
下面三种方法都会生成同样一个TypedArray数组。
// 方法一
let tarr = new Uint8Array([1,2,3]);
// 方法二
let tarr = Uint8Array.of(1,2,3);
// 方法三
let tarr = new Uint8Array(3);
tarr[0] = 1;
tarr[1] = 2;
tarr[2] = 3;
12.2.15 TypedArray.from()
静态方法from接受一个可遍历的数据结构（比如数组）作为参数，返回一个基于这个结构的TypedArray实例。
Uint16Array.from([0, 1, 2])
// Uint16Array [ 0, 1, 2 ]
这个方法还可以将一种TypedArray实例，转为另一种。
var ui16 = Uint16Array.from(Uint8Array.of(0, 1, 2));
ui16 instanceof Uint16Array // true
from方法还可以接受一个函数，作为第二个参数，用来对每个元素进行遍历，功能类似map方法。
Int8Array.of(127, 126, 125).map(x =&gt; 2 * x)
// Int8Array [ -2, -4, -6 ]
Int16Array.from(Int8Array.of(127, 126, 125), x =&gt; 2 * x)
// Int16Array [ 254, 252, 250 ]
上面的例子中，from方法没有发生溢出，这说明遍历不是针对原来的8位整数数组。也就是说，from会将第一个参数指定的TypedArray数组，拷贝到
另一段内存之中，处理之后再将结果转成指定的数组格式。
12.3 复合视图
由于视图的构造函数可以指定起始位置和长度，所以在同一段内存之中，可以依次存放不同类型的数据，这叫做“复合视图”。
var buffer = new ArrayBuffer(24);
var idView = new Uint32Array(buffer, 0, 1);
var usernameView = new Uint8Array(buffer, 4, 16);
var amountDueView = new Float32Array(buffer, 20, 1);
上面代码将一个24字节长度的ArrayBuffer对象，分成三个部分：
字节0到字节3：1个32位无符号整数
字节4到字节19：16个8位整数
字节20到字节23：1个32位浮点数
这种数据结构可以用如下的C语言描述：
struct someStruct {
unsigned long id;
char username[16];
float amountDue;
};
12.4 DataView视图
如果一段数据包括多种类型（比如服务器传来的HTTP数据），这时除了建立ArrayBuffer对象的复合视图以外，还可以通过DataView视图进行操作。
DataView视图提供更多操作选项，而且支持设定字节序。本来，在设计目的上，ArrayBuffer对象的各种TypedArray视图，是用来向网卡、声卡之类
的本机设备传送数据，所以使用本机的字节序就可以了；而DataView视图的设计目的，是用来处理网络设备传来的数据，所以大端字节序或小端字节
序是可以自行设定的。
DataView视图本身也是构造函数，接受一个ArrayBuffer对象作为参数，生成视图。
DataView(ArrayBuffer buffer [, 字节起始位置 [, 长度]]);
下面是一个例子。
var buffer = new ArrayBuffer(24);
var dv = new DataView(buffer);
DataView实例有以下属性，含义与TypedArray实例的同名方法相同。
DataView.prototype.buffer：返回对应的ArrayBuffer对象
DataView.prototype.byteLength：返回占据的内存字节长度
DataView.prototype.byteOffset：返回当前视图从对应的ArrayBuffer对象的哪个字节开始
DataView实例提供8个方法读取内存。
getInt8：读取1个字节，返回一个8位整数。
getUint8：读取1个字节，返回一个无符号的8位整数。
getInt16：读取2个字节，返回一个16位整数。
getUint16：读取2个字节，返回一个无符号的16位整数。
getInt32：读取4个字节，返回一个32位整数。
getUint32：读取4个字节，返回一个无符号的32位整数。
getFloat32：读取4个字节，返回一个32位浮点数。
getFloat64：读取8个字节，返回一个64位浮点数。
这一系列get方法的参数都是一个字节序号（不能是负数，否则会报错），表示从哪个字节开始读取。
var buffer = new ArrayBuffer(24);
var dv = new DataView(buffer);
// 从第1个字节读取一个8位无符号整数
var v1 = dv.getUint8(0);
// 从第2个字节读取一个16位无符号整数
var v2 = dv.getUint16(1);
// 从第4个字节读取一个16位无符号整数
var v3 = dv.getUint16(3);
上面代码读取了ArrayBuffer对象的前5个字节，其中有一个8位整数和两个十六位整数。
如果一次读取两个或两个以上字节，就必须明确数据的存储方式，到底是小端字节序还是大端字节序。默认情况下，DataView的get方法使用大端字节
序解读数据，如果需要使用小端字节序解读，必须在get方法的第二个参数指定true。
// 小端字节序
var v1 = dv.getUint16(1, true);
// 大端字节序
var v2 = dv.getUint16(3, false);
// 大端字节序
var v3 = dv.getUint16(3);
DataView视图提供8个方法写入内存。
setInt8：写入1个字节的8位整数。
setUint8：写入1个字节的8位无符号整数。
setInt16：写入2个字节的16位整数。
setUint16：写入2个字节的16位无符号整数。
setInt32：写入4个字节的32位整数。
setUint32：写入4个字节的32位无符号整数。
setFloat32：写入4个字节的32位浮点数。
setFloat64：写入8个字节的64位浮点数。
这一系列set方法，接受两个参数，第一个参数是字节序号，表示从哪个字节开始写入，第二个参数为写入的数据。对于那些写入两个或两个以上字节
的方法，需要指定第三个参数，false或者undefined表示使用大端字节序写入，true表示使用小端字节序写入。
// 在第1个字节，以大端字节序写入值为25的32位整数
dv.setInt32(0, 25, false);
// 在第5个字节，以大端字节序写入值为25的32位整数
dv.setInt32(4, 25);
// 在第9个字节，以小端字节序写入值为2.5的32位浮点数
dv.setFloat32(8, 2.5, true);
如果不确定正在使用的计算机的字节序，可以采用下面的判断方式。
var littleEndian = (function() {
var buffer = new ArrayBuffer(2);
new DataView(buffer).setInt16(0, 256, true);
return new Int16Array(buffer)[0] === 256;
})();
如果返回true，就是小端字节序；如果返回false，就是大端字节序。
12.5 二进制数组的应用
大量的Web API用到了ArrayBuffer对象和它的视图对象。
12.5.1 AJAX
传统上，服务器通过AJAX操作只能返回文本数据，即responseType属性默认为text。XMLHttpRequest第二版XHR2允许服务器返回二进制数据，这时分
成两种情况。如果明确知道返回的二进制数据类型，可以把返回类型（responseType）设为arraybuffer；如果不知道，就设为blob。
var xhr = new XMLHttpRequest();
xhr.open('GET', someUrl);
xhr.responseType = 'arraybuffer';
xhr.onload = function () {
let arrayBuffer = xhr.response;
// ···
};
xhr.send();
如果知道传回来的是32位整数，可以像下面这样处理。
xhr.onreadystatechange = function () {
if (req.readyState === 4 ) {
var arrayResponse = xhr.response;
var dataView = new DataView(arrayResponse);
var ints = new Uint32Array(dataView.byteLength / 4);
xhrDiv.style.backgroundColor = "#00FF00";
xhrDiv.innerText = "Array is " + ints.length + "uints long";
}
}
12.5.2 Canvas
网页Canvas元素输出的二进制像素数据，就是TypedArray数组。
var canvas = document.getElementById('myCanvas');
var ctx = canvas.getContext('2d');
var imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);
var uint8ClampedArray = imageData.data;
需要注意的是，上面代码的uint8ClampedArray虽然是一个TypedArray数组，但是它的视图类型是一种针对Canvas元素的专有类
型Uint8ClampedArray。这个视图类型的特点，就是专门针对颜色，把每个字节解读为无符号的8位整数，即只能取值0～255，而且发生运算的时候自
动过滤高位溢出。这为图像处理带来了巨大的方便。
举例来说，如果把像素的颜色值设为Uint8Array类型，那么乘以一个gamma值的时候，就必须这样计算：
u8[i] = Math.min(255, Math.max(0, u8[i] * gamma));
因为Uint8Array类型对于大于255的运算结果（比如0xFF+1），会自动变为0x00，所以图像处理必须要像上面这样算。这样做很麻烦，而且影响性
能。如果将颜色值设为Uint8ClampedArray类型，计算就简化许多。
pixels[i] *= gamma;
Uint8ClampedArray类型确保将小于0的值设为0，将大于255的值设为255。注意，IE 10不支持该类型。
12.5.3 WebSocket
WebSocket可以通过ArrayBuffer，发送或接收二进制数据。
var socket = new WebSocket('ws://127.0.0.1:8081');
socket.binaryType = 'arraybuffer';
// Wait until socket is open
socket.addEventListener('open', function (event) {
// Send binary data
var typedArray = new Uint8Array(4);
socket.send(typedArray.buffer);
});
// Receive binary data
socket.addEventListener('message', function (event) {
var arrayBuffer = event.data;
// ···
});
12.5.4 Fetch API
Fetch API取回的数据，就是ArrayBuffer对象。
fetch(url)
.then(function(request){
return request.arrayBuffer()
})
.then(function(arrayBuffer){
// ...
});
12.5.5 File API
如果知道一个文件的二进制数据类型，也可以将这个文件读取为ArrayBuffer对象。
var fileInput = document.getElementById('fileInput');
var file = fileInput.files[0];
var reader = new FileReader();
reader.readAsArrayBuffer(file);
reader.onload = function () {
var arrayBuffer = reader.result;
// ···
};
下面以处理bmp文件为例。假定file变量是一个指向bmp文件的文件对象，首先读取文件。
var reader = new FileReader();
reader.addEventListener("load", processimage, false);
reader.readAsArrayBuffer(file);
然后，定义处理图像的回调函数：先在二进制数据之上建立一个DataView视图，再建立一个bitmap对象，用于存放处理后的数据，最后将图像展示
在Canvas元素之中。
function processimage(e) {
var buffer = e.target.result;
var datav = new DataView(buffer);
var bitmap = {};
// 具体的处理步骤
}
具体处理图像数据时，先处理bmp的文件头。具体每个文件头的格式和定义，请参阅有关资料。
bitmap.fileheader = {};
bitmap.fileheader.bfType = datav.getUint16(0, true);
bitmap.fileheader.bfSize = datav.getUint32(2, true);
bitmap.fileheader.bfReserved1 = datav.getUint16(6, true);
bitmap.fileheader.bfReserved2 = datav.getUint16(8, true);
bitmap.fileheader.bfOffBits = datav.getUint32(10, true);
接着处理图像元信息部分。
bitmap.infoheader = {};
bitmap.infoheader.biSize = datav.getUint32(14, true);
bitmap.infoheader.biWidth = datav.getUint32(18, true);
bitmap.infoheader.biHeight = datav.getUint32(22, true);
bitmap.infoheader.biPlanes = datav.getUint16(26, true);
bitmap.infoheader.biBitCount = datav.getUint16(28, true);
bitmap.infoheader.biCompression = datav.getUint32(30, true);
bitmap.infoheader.biSizeImage = datav.getUint32(34, true);
bitmap.infoheader.biXPelsPerMeter = datav.getUint32(38, true);
bitmap.infoheader.biYPelsPerMeter = datav.getUint32(42, true);
bitmap.infoheader.biClrUsed = datav.getUint32(46, true);
bitmap.infoheader.biClrImportant = datav.getUint32(50, true);
最后处理图像本身的像素信息。
var start = bitmap.fileheader.bfOffBits;
bitmap.pixels = new Uint8Array(buffer, start);
至此，图像文件的数据全部处理完成。下一步，可以根据需要，进行图像变形，或者转换格式，或者展示在Canvas网页元素之中。
13 Set和Map数据结构
13.1 Set
13.1.1 基本用法
ES6提供了新的数据结构Set。它类似于数组，但是成员的值都是唯一的，没有重复的值。
Set本身是一个构造函数，用来生成Set数据结构。
var s = new Set();
[2, 3, 5, 4, 5, 2, 2].map(x =&gt; s.add(x));
for (let i of s) {
console.log(i);
}
// 2 3 5 4
上面代码通过add方法向Set结构加入成员，结果表明Set结构不会添加重复的值。
Set函数可以接受一个数组（或类似数组的对象）作为参数，用来初始化。
// 例一
var set = new Set([1, 2, 3, 4, 4]);
[...set]
// [1, 2, 3, 4]
// 例二
var items = new Set([1, 2, 3, 4, 5, 5, 5, 5]);
items.size // 5
// 例三
function divs () {
return [...document.querySelectorAll('div')];
}
var set = new Set(divs());
set.size // 56
// 类似于
divs().forEach(div =&gt; set.add(div));
set.size // 56
上面代码中，例一和例二都是Set函数接受数组作为参数，例三是接受类似数组的对象作为参数。
上面代码中，也展示了一种去除数组重复成员的方法。
// 去除数组的重复成员
[...new Set(array)]
向Set加入值的时候，不会发生类型转换，所以5和"5"是两个不同的值。Set内部判断两个值是否不同，使用的算法叫做“Same-value equality”，它类
似于精确相等运算符（===），主要的区别是NaN等于自身，而精确相等运算符认为NaN不等于自身。
let set = new Set();
let a = NaN;
let b = NaN;
set.add(a);
set.add(b);
set // Set {NaN}
上面代码向Set实例添加了两个NaN，但是只能加入一个。这表明，在Set内部，两个NaN是相等。
另外，两个对象总是不相等的。
let set = new Set();
set.add({});
set.size // 1
set.add({});
set.size // 2
上面代码表示，由于两个空对象不相等，所以它们被视为两个值。
13.1.2 Set实例的属性和方法
Set结构的实例有以下属性。
Set.prototype.constructor：构造函数，默认就是Set函数。
Set.prototype.size：返回Set实例的成员总数。
Set实例的方法分为两大类：操作方法（用于操作数据）和遍历方法（用于遍历成员）。下面先介绍四个操作方法。
add(value)：添加某个值，返回Set结构本身。
delete(value)：删除某个值，返回一个布尔值，表示删除是否成功。
has(value)：返回一个布尔值，表示该值是否为Set的成员。
clear()：清除所有成员，没有返回值。
上面这些属性和方法的实例如下。
s.add(1).add(2).add(2);
// 注意2被加入了两次
s.size // 2
s.has(1) // true
s.has(2) // true
s.has(3) // false
s.delete(2);
s.has(2) // false
下面是一个对比，看看在判断是否包括一个键上面，Object结构和Set结构的写法不同。
// 对象的写法
var properties = {
'width': 1,
'height': 1
};
if (properties[someName]) {
// do something
}
// Set的写法
var properties = new Set();
properties.add('width');
properties.add('height');
if (properties.has(someName)) {
// do something
}
Array.from方法可以将Set结构转为数组。
var items = new Set([1, 2, 3, 4, 5]);
var array = Array.from(items);
这就提供了去除数组重复成员的另一种方法。
function dedupe(array) {
return Array.from(new Set(array));
}
dedupe([1, 1, 2, 3]) // [1, 2, 3]
13.1.3 遍历操作
Set结构的实例有四个遍历方法，可以用于遍历成员。
keys()：返回键名的遍历器
values()：返回键值的遍历器
entries()：返回键值对的遍历器
forEach()：使用回调函数遍历每个成员
需要特别指出的是，Set的遍历顺序就是插入顺序。这个特性有时非常有用，比如使用Set保存一个回调函数列表，调用时就能保证按照添加顺序调
用。
（1）keys()，values()，entries()
key方法、value方法、entries方法返回的都是遍历器对象（详见《Iterator对象》一章）。由于Set结构没有键名，只有键值（或者说键名和键值是同
一个值），所以key方法和value方法的行为完全一致。
let set = new Set(['red', 'green', 'blue']);
for (let item of set.keys()) {
console.log(item);
}
// red
// green
// blue
for (let item of set.values()) {
console.log(item);
}
// red
// green
// blue
for (let item of set.entries()) {
console.log(item);
}
// ["red", "red"]
// ["green", "green"]
// ["blue", "blue"]
上面代码中，entries方法返回的遍历器，同时包括键名和键值，所以每次输出一个数组，它的两个成员完全相等。
Set结构的实例默认可遍历，它的默认遍历器生成函数就是它的values方法。
Set.prototype[Symbol.iterator] === Set.prototype.values
// true
这意味着，可以省略values方法，直接用for...of循环遍历Set。
let set = new Set(['red', 'green', 'blue']);
for (let x of set) {
console.log(x);
}
// red
// green
// blue
（2）forEach()
Set结构的实例的forEach方法，用于对每个成员执行某种操作，没有返回值。
let set = new Set([1, 2, 3]);
set.forEach((value, key) =&gt; console.log(value * 2) )
// 2
// 4
// 6
上面代码说明，forEach方法的参数就是一个处理函数。该函数的参数依次为键值、键名、集合本身（上例省略了该参数）。另外，forEach方法还可
以有第二个参数，表示绑定的this对象。
（3）遍历的应用
扩展运算符（...）内部使用for...of循环，所以也可以用于Set结构。
let set = new Set(['red', 'green', 'blue']);
let arr = [...set];
// ['red', 'green', 'blue']
扩展运算符和Set结构相结合，就可以去除数组的重复成员。
let arr = [3, 5, 2, 2, 5, 5];
let unique = [...new Set(arr)];
// [3, 5, 2]
而且，数组的map和filter方法也可以用于Set了。
let set = new Set([1, 2, 3]);
set = new Set([...set].map(x =&gt; x * 2));
// 返回Set结构：{2, 4, 6}
let set = new Set([1, 2, 3, 4, 5]);
set = new Set([...set].filter(x =&gt; (x % 2) == 0));
// 返回Set结构：{2, 4}
因此使用Set可以很容易地实现并集（Union）、交集（Intersect）和差集（Difference）。
let a = new Set([1, 2, 3]);
let b = new Set([4, 3, 2]);
// 并集
let union = new Set([...a, ...b]);
// Set {1, 2, 3, 4}
// 交集
let intersect = new Set([...a].filter(x =&gt; b.has(x)));
// set {2, 3}
// 差集
let difference = new Set([...a].filter(x =&gt; !b.has(x)));
// Set {1}
如果想在遍历操作中，同步改变原来的Set结构，目前没有直接的方法，但有两种变通方法。一种是利用原Set结构映射出一个新的结构，然后赋值给
原来的Set结构；另一种是利用Array.from方法。
// 方法一
let set = new Set([1, 2, 3]);
set = new Set([...set].map(val =&gt; val * 2));
// set的值是2, 4, 6
// 方法二
let set = new Set([1, 2, 3]);
set = new Set(Array.from(set, val =&gt; val * 2));
// set的值是2, 4, 6
上面代码提供了两种方法，直接在遍历操作中改变原来的Set结构。
13.2 WeakSet
WeakSet结构与Set类似，也是不重复的值的集合。但是，它与Set有两个区别。
首先，WeakSet的成员只能是对象，而不能是其他类型的值。
其次，WeakSet中的对象都是弱引用，即垃圾回收机制不考虑WeakSet对该对象的引用，也就是说，如果其他对象都不再引用该对象，那么垃圾回收
机制会自动回收该对象所占用的内存，不考虑该对象还存在于WeakSet之中。这个特点意味着，无法引用WeakSet的成员，因此WeakSet是不可遍历
的。
var ws = new WeakSet();
ws.add(1)
// TypeError: Invalid value used in weak set
ws.add(Symbol())
// TypeError: invalid value used in weak set
上面代码试图向WeakSet添加一个数值和Symbol值，结果报错，因为WeakSet只能放置对象。
WeakSet是一个构造函数，可以使用new命令，创建WeakSet数据结构。
var ws = new WeakSet();
作为构造函数，WeakSet可以接受一个数组或类似数组的对象作为参数。（实际上，任何具有iterable接口的对象，都可以作为WeakSet的参数。）该
数组的所有成员，都会自动成为WeakSet实例对象的成员。
var a = [[1,2], [3,4]];
var ws = new WeakSet(a);
上面代码中，a是一个数组，它有两个成员，也都是数组。将a作为WeakSet构造函数的参数，a的成员会自动成为WeakSet的成员。
注意，是a数组的成员成为WeakSet的成员，而不是a数组本身。这意味着，数组的成员只能是对象。
var b = [3, 4];
var ws = new WeakSet(b);
// Uncaught TypeError: Invalid value used in weak set(…)
上面代码中，数组b的成员不是对象，加入WeaKSet就会报错。
WeakSet结构有以下三个方法。
WeakSet.prototype.add(value)：向WeakSet实例添加一个新成员。
WeakSet.prototype.delete(value)：清除WeakSet实例的指定成员。
WeakSet.prototype.has(value)：返回一个布尔值，表示某个值是否在WeakSet实例之中。
下面是一个例子。
var ws = new WeakSet();
var obj = {};
var foo = {};
ws.add(window);
ws.add(obj);
ws.has(window); // true
ws.has(foo); // false
ws.delete(window);
ws.has(window); // false
WeakSet没有size属性，没有办法遍历它的成员。
ws.size // undefined
ws.forEach // undefined
ws.forEach(function(item){ console.log('WeakSet has ' + item)})
// TypeError: undefined is not a function
上面代码试图获取size和forEach属性，结果都不能成功。
WeakSet不能遍历，是因为成员都是弱引用，随时可能消失，遍历机制无法保证成员的存在，很可能刚刚遍历结束，成员就取不到了。WeakSet的一
个用处，是储存DOM节点，而不用担心这些节点从文档移除时，会引发内存泄漏。
下面是WeakSet的另一个例子。
const foos = new WeakSet()
class Foo {
constructor() {
foos.add(this)
}
method () {
if (!foos.has(this)) {
throw new TypeError('Foo.prototype.method 只能在Foo的实例上调用！');
}
}
}
上面代码保证了Foo的实例方法，只能在Foo的实例上调用。这里使用WeakSet的好处是，foos对实例的引用，不会被计入内存回收机制，所以删除实
例的时候，不用考虑foos，也不会出现内存泄漏。
13.3 Map
13.3.1 Map结构的目的和基本用法
JavaScript的对象（Object），本质上是键值对的集合（Hash结构），但是传统上只能用字符串当作键。这给它的使用带来了很大的限制。
var data = {};
var element = document.getElementById('myDiv');
data[element] = 'metadata';
data['[object HTMLDivElement]'] // "metadata"
上面代码原意是将一个DOM节点作为对象data的键，但是由于对象只接受字符串作为键名，所以element被自动转为字符
串[object HTMLDivElement]。
为了解决这个问题，ES6提供了Map数据结构。它类似于对象，也是键值对的集合，但是“键”的范围不限于字符串，各种类型的值（包括对象）都可以
当作键。也就是说，Object结构提供了“字符串—值”的对应，Map结构提供了“值—值”的对应，是一种更完善的Hash结构实现。如果你需要“键值对”的
数据结构，Map比Object更合适。
var m = new Map();
var o = {p: 'Hello World'};
m.set(o, 'content')
m.get(o) // "content"
m.has(o) // true
m.delete(o) // true
m.has(o) // false
上面代码使用set方法，将对象o当作m的一个键，然后又使用get方法读取这个键，接着使用delete方法删除了这个键。
作为构造函数，Map也可以接受一个数组作为参数。该数组的成员是一个个表示键值对的数组。
var map = new Map([
['name', '张三'],
['title', 'Author']
]);
map.size // 2
map.has('name') // true
map.get('name') // "张三"
map.has('title') // true
map.get('title') // "Author"
上面代码在新建Map实例时，就指定了两个键name和title。
Map构造函数接受数组作为参数，实际上执行的是下面的算法。
var items = [
['name', '张三'],
['title', 'Author']
];
var map = new Map();
items.forEach(([key, value]) =&gt; map.set(key, value));
下面的例子中，字符串true和布尔值true是两个不同的键。
var m = new Map([
[true, 'foo'],
['true', 'bar']
]);
m.get(true) // 'foo'
m.get('true') // 'bar'
如果对同一个键多次赋值，后面的值将覆盖前面的值。
let map = new Map();
map
.set(1, 'aaa')
.set(1, 'bbb');
map.get(1) // "bbb"
上面代码对键1连续赋值两次，后一次的值覆盖前一次的值。
如果读取一个未知的键，则返回undefined。
new Map().get('asfddfsasadf')
// undefined
注意，只有对同一个对象的引用，Map结构才将其视为同一个键。这一点要非常小心。
var map = new Map();
map.set(['a'], 555);
map.get(['a']) // undefined
上面代码的set和get方法，表面是针对同一个键，但实际上这是两个值，内存地址是不一样的，因此get方法无法读取该键，返回undefined。
同理，同样的值的两个实例，在Map结构中被视为两个键。
var map = new Map();
var k1 = ['a'];
var k2 = ['a'];
map
.set(k1, 111)
.set(k2, 222);
map.get(k1) // 111
map.get(k2) // 222
上面代码中，变量k1和k2的值是一样的，但是它们在Map结构中被视为两个键。
由上可知，Map的键实际上是跟内存地址绑定的，只要内存地址不一样，就视为两个键。这就解决了同名属性碰撞（clash）的问题，我们扩展别人的
库的时候，如果使用对象作为键名，就不用担心自己的属性与原作者的属性同名。
如果Map的键是一个简单类型的值（数字、字符串、布尔值），则只要两个值严格相等，Map将其视为一个键，包括0和-0。另外，虽然NaN不严格相
等于自身，但Map将其视为同一个键。
let map = new Map();
map.set(NaN, 123);
map.get(NaN) // 123
map.set(-0, 123);
map.get(+0) // 123
13.3.2 实例的属性和操作方法
Map结构的实例有以下属性和操作方法。
（1）size属性
size属性返回Map结构的成员总数。
let map = new Map();
map.set('foo', true);
map.set('bar', false);
map.size // 2
（2）set(key, value)
set方法设置key所对应的键值，然后返回整个Map结构。如果key已经有值，则键值会被更新，否则就新生成该键。
var m = new Map();
m.set("edition", 6) // 键是字符串
m.set(262, "standard") // 键是数值
m.set(undefined, "nah") // 键是undefined
set方法返回的是Map本身，因此可以采用链式写法。
let map = new Map()
.set(1, 'a')
.set(2, 'b')
.set(3, 'c');
（3）get(key)
get方法读取key对应的键值，如果找不到key，返回undefined。
var m = new Map();
var hello = function() {console.log("hello");}
m.set(hello, "Hello ES6!") // 键是函数
m.get(hello) // Hello ES6!
（4）has(key)
has方法返回一个布尔值，表示某个键是否在Map数据结构中。
var m = new Map();
m.set("edition", 6);
m.set(262, "standard");
m.set(undefined, "nah");
m.has("edition") // true
m.has("years") // false
m.has(262) // true
m.has(undefined) // true
（5）delete(key)
delete方法删除某个键，返回true。如果删除失败，返回false。
var m = new Map();
m.set(undefined, "nah");
m.has(undefined) // true
m.delete(undefined)
m.has(undefined) // false
（6）clear()
clear方法清除所有成员，没有返回值。
let map = new Map();
map.set('foo', true);
map.set('bar', false);
map.size // 2
map.clear()
map.size // 0
13.3.3 遍历方法
Map原生提供三个遍历器生成函数和一个遍历方法。
keys()：返回键名的遍历器。
values()：返回键值的遍历器。
entries()：返回所有成员的遍历器。
forEach()：遍历Map的所有成员。
需要特别注意的是，Map的遍历顺序就是插入顺序。
下面是使用实例。
let map = new Map([
['F', 'no'],
['T', 'yes'],
]);
for (let key of map.keys()) {
console.log(key);
}
// "F"
// "T"
for (let value of map.values()) {
console.log(value);
}
// "no"
// "yes"
for (let item of map.entries()) {
console.log(item[0], item[1]);
}
// "F" "no"
// "T" "yes"
// 或者
for (let [key, value] of map.entries()) {
console.log(key, value);
}
// 等同于使用map.entries()
for (let [key, value] of map) {
console.log(key, value);
}
上面代码最后的那个例子，表示Map结构的默认遍历器接口（Symbol.iterator属性），就是entries方法。
map[Symbol.iterator] === map.entries
// true
Map结构转为数组结构，比较快速的方法是结合使用扩展运算符（...）。
let map = new Map([
[1, 'one'],
[2, 'two'],
[3, 'three'],
]);
[...map.keys()]
// [1, 2, 3]
[...map.values()]
// ['one', 'two', 'three']
[...map.entries()]
// [[1,'one'], [2, 'two'], [3, 'three']]
[...map]
// [[1,'one'], [2, 'two'], [3, 'three']]
结合数组的map方法、filter方法，可以实现Map的遍历和过滤（Map本身没有map和filter方法）。
let map0 = new Map()
.set(1, 'a')
.set(2, 'b')
.set(3, 'c');
let map1 = new Map(
[...map0].filter(([k, v]) =&gt; k &lt; 3)
);
// 产生Map结构 {1 =&gt; 'a', 2 =&gt; 'b'}
let map2 = new Map(
[...map0].map(([k, v]) =&gt; [k * 2, '_' + v])
);
// 产生Map结构 {2 =&gt; '_a', 4 =&gt; '_b', 6 =&gt; '_c'}
此外，Map还有一个forEach方法，与数组的forEach方法类似，也可以实现遍历。
map.forEach(function(value, key, map) {
console.log("Key: %s, Value: %s", key, value);
});
forEach方法还可以接受第二个参数，用来绑定this。
var reporter = {
report: function(key, value) {
console.log("Key: %s, Value: %s", key, value);
}
};
map.forEach(function(value, key, map) {
this.report(key, value);
}, reporter);
上面代码中，forEach方法的回调函数的this，就指向reporter。
13.3.4 与其他数据结构的互相转换
（1）Map转为数组
前面已经提过，Map转为数组最方便的方法，就是使用扩展运算符（...）。
let myMap = new Map().set(true, 7).set({foo: 3}, ['abc']);
[...myMap]
// [ [ true, 7 ], [ { foo: 3 }, [ 'abc' ] ] ]
（2）数组转为Map
将数组转入Map构造函数，就可以转为Map。
new Map([[true, 7], [{foo: 3}, ['abc']]])
// Map {true =&gt; 7, Object {foo: 3} =&gt; ['abc']}
（3）Map转为对象
如果所有Map的键都是字符串，它可以转为对象。
function strMapToObj(strMap) {
let obj = Object.create(null);
for (let [k,v] of strMap) {
obj[k] = v;
}
return obj;
}
let myMap = new Map().set('yes', true).set('no', false);
strMapToObj(myMap)
// { yes: true, no: false }
（4）对象转为Map
function objToStrMap(obj) {
let strMap = new Map();
for (let k of Object.keys(obj)) {
strMap.set(k, obj[k]);
}
return strMap;
}
objToStrMap({yes: true, no: false})
// [ [ 'yes', true ], [ 'no', false ] ]
（5）Map转为JSON
Map转为JSON要区分两种情况。一种情况是，Map的键名都是字符串，这时可以选择转为对象JSON。
function strMapToJson(strMap) {
return JSON.stringify(strMapToObj(strMap));
}
let myMap = new Map().set('yes', true).set('no', false);
strMapToJson(myMap)
// '{"yes":true,"no":false}'
另一种情况是，Map的键名有非字符串，这时可以选择转为数组JSON。
function mapToArrayJson(map) {
return JSON.stringify([...map]);
}
let myMap = new Map().set(true, 7).set({foo: 3}, ['abc']);
mapToArrayJson(myMap)
// '[[true,7],[{"foo":3},["abc"]]]'
（6）JSON转为Map
JSON转为Map，正常情况下，所有键名都是字符串。
function jsonToStrMap(jsonStr) {
return objToStrMap(JSON.parse(jsonStr));
}
jsonToStrMap('{"yes":true,"no":false}')
// Map {'yes' =&gt; true, 'no' =&gt; false}
但是，有一种特殊情况，整个JSON就是一个数组，且每个数组成员本身，又是一个有两个成员的数组。这时，它可以一一对应地转为Map。这往往是
数组转为JSON的逆操作。
function jsonToMap(jsonStr) {
return new Map(JSON.parse(jsonStr));
}
jsonToMap('[[true,7],[{"foo":3},["abc"]]]')
// Map {true =&gt; 7, Object {foo: 3} =&gt; ['abc']}
13.4 WeakMap
WeakMap结构与Map结构基本类似，唯一的区别是它只接受对象作为键名（null除外），不接受其他类型的值作为键名，而且键名所指向的对象，不计
入垃圾回收机制。
var map = new WeakMap()
map.set(1, 2)
// TypeError: 1 is not an object!
map.set(Symbol(), 2)
// TypeError: Invalid value used as weak map key
上面代码中，如果将1和Symbol作为WeakMap的键名，都会报错。
WeakMap的设计目的在于，键名是对象的弱引用（垃圾回收机制不将该引用考虑在内），所以其所对应的对象可能会被自动回收。当对象被回收
后，WeakMap自动移除对应的键值对。典型应用是，一个对应DOM元素的WeakMap结构，当某个DOM元素被清除，其所对应的WeakMap记录就会自动被
移除。基本上，WeakMap的专用场合就是，它的键所对应的对象，可能会在将来消失。WeakMap结构有助于防止内存泄漏。
下面是WeakMap结构的一个例子，可以看到用法上与Map几乎一样。
var wm = new WeakMap();
var element = document.querySelector(".element");
wm.set(element, "Original");
wm.get(element) // "Original"
element.parentNode.removeChild(element);
element = null;
wm.get(element) // undefined
上面代码中，变量wm是一个WeakMap实例，我们将一个DOM节点element作为键名，然后销毁这个节点，element对应的键就自动消失了，再引用这个键
名就返回undefined。
WeakMap与Map在API上的区别主要是两个，一是没有遍历操作（即没有key()、values()和entries()方法），也没有size属性；二是无法清空，即
不支持clear方法。这与WeakMap的键不被计入引用、被垃圾回收机制忽略有关。因此，WeakMap只有四个方法可
用：get()、set()、has()、delete()。
var wm = new WeakMap();
wm.size
// undefined
wm.forEach
// undefined
前文说过，WeakMap应用的典型场合就是DOM节点作为键名。下面是一个例子。
let myElement = document.getElementById('logo');
let myWeakmap = new WeakMap();
myWeakmap.set(myElement, {timesClicked: 0});
myElement.addEventListener('click', function() {
let logoData = myWeakmap.get(myElement);
logoData.timesClicked++;
myWeakmap.set(myElement, logoData);
}, false);
上面代码中，myElement是一个DOM节点，每当发生click事件，就更新一下状态。我们将这个状态作为键值放在WeakMap里，对应的键名就
是myElement。一旦这个DOM节点删除，该状态就会自动消失，不存在内存泄漏风险。
WeakMap的另一个用处是部署私有属性。
let _counter = new WeakMap();
let _action = new WeakMap();
class Countdown {
constructor(counter, action) {
_counter.set(this, counter);
_action.set(this, action);
}
dec() {
let counter = _counter.get(this);
if (counter &lt; 1) return;
counter--;
_counter.set(this, counter);
if (counter === 0) {
_action.get(this)();
}
}
}
let c = new Countdown(2, () =&gt; console.log('DONE'));
c.dec()
c.dec()
// DONE
上面代码中，Countdown类的两个内部属性_counter和_action，是实例的弱引用，所以如果删除实例，它们也就随之消失，不会造成内存泄漏。
14 Iterator和for...of循环
14.1 Iterator（遍历器）的概念
JavaScript原有的表示“集合”的数据结构，主要是数组（Array）和对象（Object），ES6又添加了Map和Set。这样就有了四种数据集合，用户还可以
组合使用它们，定义自己的数据结构，比如数组的成员是Map，Map的成员是对象。这样就需要一种统一的接口机制，来处理所有不同的数据结构。
遍历器（Iterator）就是这样一种机制。它是一种接口，为各种不同的数据结构提供统一的访问机制。任何数据结构只要部署Iterator接口，就可以完成
遍历操作（即依次处理该数据结构的所有成员）。
Iterator的作用有三个：一是为各种数据结构，提供一个统一的、简便的访问接口；二是使得数据结构的成员能够按某种次序排列；三是ES6创造了一
种新的遍历命令for...of循环，Iterator接口主要供for...of消费。
Iterator的遍历过程是这样的。
（1）创建一个指针对象，指向当前数据结构的起始位置。也就是说，遍历器对象本质上，就是一个指针对象。
（2）第一次调用指针对象的next方法，可以将指针指向数据结构的第一个成员。
（3）第二次调用指针对象的next方法，指针就指向数据结构的第二个成员。
（4）不断调用指针对象的next方法，直到它指向数据结构的结束位置。
每一次调用next方法，都会返回数据结构的当前成员的信息。具体来说，就是返回一个包含value和done两个属性的对象。其中，value属性是当前成
员的值，done属性是一个布尔值，表示遍历是否结束。
下面是一个模拟next方法返回值的例子。
var it = makeIterator(['a', 'b']);
it.next() // { value: "a", done: false }
it.next() // { value: "b", done: false }
it.next() // { value: undefined, done: true }
function makeIterator(array) {
var nextIndex = 0;
return {
next: function() {
return nextIndex &lt; array.length ?
{value: array[nextIndex++], done: false} :
{value: undefined, done: true};
}
};
}
上面代码定义了一个makeIterator函数，它是一个遍历器生成函数，作用就是返回一个遍历器对象。对数组['a', 'b']执行这个函数，就会返回该数
组的遍历器对象（即指针对象）it。
指针对象的next方法，用来移动指针。开始时，指针指向数组的开始位置。然后，每次调用next方法，指针就会指向数组的下一个成员。第一次调
用，指向a；第二次调用，指向b。
next方法返回一个对象，表示当前数据成员的信息。这个对象具有value和done两个属性，value属性返回当前位置的成员，done属性是一个布尔值，
表示遍历是否结束，即是否还有必要再一次调用next方法。
总之，调用指针对象的next方法，就可以遍历事先给定的数据结构。
对于遍历器对象来说，done: false和value: undefined属性都是可以省略的，因此上面的makeIterator函数可以简写成下面的形式。
function makeIterator(array) {
var nextIndex = 0;
return {
next: function() {
return nextIndex &lt; array.length ?
{value: array[nextIndex++]} :
{done: true};
}
};
}
由于Iterator只是把接口规格加到数据结构之上，所以，遍历器与它所遍历的那个数据结构，实际上是分开的，完全可以写出没有对应数据结构的遍历
器对象，或者说用遍历器对象模拟出数据结构。下面是一个无限运行的遍历器对象的例子。
var it = idMaker();
it.next().value // '0'
it.next().value // '1'
it.next().value // '2'
// ...
function idMaker() {
var index = 0;
return {
next: function() {
return {value: index++, done: false};
}
};
}
上面的例子中，遍历器生成函数idMaker，返回一个遍历器对象（即指针对象）。但是并没有对应的数据结构，或者说，遍历器对象自己描述了一个数
据结构出来。
在ES6中，有些数据结构原生具备Iterator接口（比如数组），即不用任何处理，就可以被for...of循环遍历，有些就不行（比如对象）。原因在于，
这些数据结构原生部署了Symbol.iterator属性（详见下文），另外一些数据结构没有。凡是部署了Symbol.iterator属性的数据结构，就称为部署了
遍历器接口。调用这个接口，就会返回一个遍历器对象。
如果使用TypeScript的写法，遍历器接口（Iterable）、指针对象（Iterator）和next方法返回值的规格可以描述如下。
interface Iterable {
[Symbol.iterator]() : Iterator,
}
interface Iterator {
next(value?: any) : IterationResult,
}
interface IterationResult {
value: any,
done: boolean,
}
14.2 数据结构的默认Iterator接口
Iterator接口的目的，就是为所有数据结构，提供了一种统一的访问机制，即for...of循环（详见下文）。当使用for...of循环遍历某种数据结构时，
该循环会自动去寻找Iterator接口。
ES6规定，默认的Iterator接口部署在数据结构的Symbol.iterator属性，或者说，一个数据结构只要具有Symbol.iterator属性，就可以认为是“可遍历
的”（iterable）。调用Symbol.iterator方法，就会得到当前数据结构默认的遍历器生成函数。Symbol.iterator本身是一个表达式，返回Symbol对象
的iterator属性，这是一个预定义好的、类型为Symbol的特殊值，所以要放在方括号内（请参考Symbol一章）。
在ES6中，有三类数据结构原生具备Iterator接口：数组、某些类似数组的对象、Set和Map结构。
let arr = ['a', 'b', 'c'];
let iter = arr[Symbol.iterator]();
iter.next() // { value: 'a', done: false }
iter.next() // { value: 'b', done: false }
iter.next() // { value: 'c', done: false }
iter.next() // { value: undefined, done: true }
上面代码中，变量arr是一个数组，原生就具有遍历器接口，部署在arr的Symbol.iterator属性上面。所以，调用这个属性，就得到遍历器对象。
上面提到，原生就部署Iterator接口的数据结构有三类，对于这三类数据结构，不用自己写遍历器生成函数，for...of循环会自动遍历它们。除此之
外，其他数据结构（主要是对象）的Iterator接口，都需要自己在Symbol.iterator属性上面部署，这样才会被for...of循环遍历。
对象（Object）之所以没有默认部署Iterator接口，是因为对象的哪个属性先遍历，哪个属性后遍历是不确定的，需要开发者手动指定。本质上，遍历
器是一种线性处理，对于任何非线性的数据结构，部署遍历器接口，就等于部署一种线性转换。不过，严格地说，对象部署遍历器接口并不是很必
要，因为这时对象实际上被当作Map结构使用，ES5没有Map结构，而ES6原生提供了。
一个对象如果要有可被for...of循环调用的Iterator接口，就必须在Symbol.iterator的属性上部署遍历器生成方法（原型链上的对象具有该方法也
可）。
class RangeIterator {
constructor(start, stop) {
this.value = start;
this.stop = stop;
}
[Symbol.iterator]() { return this; }
next() {
var value = this.value;
if (value &lt; this.stop) {
this.value++;
return {done: false, value: value};
} else {
return {done: true, value: undefined};
}
}
}
function range(start, stop) {
return new RangeIterator(start, stop);
}
for (var value of range(0, 3)) {
console.log(value);
}
上面代码是一个类部署Iterator接口的写法。Symbol.iterator属性对应一个函数，执行后返回当前对象的遍历器对象。
下面是通过遍历器实现指针结构的例子。
function Obj(value) {
this.value = value;
this.next = null;
}
Obj.prototype[Symbol.iterator] = function() {
var iterator = {
next: next
};
var current = this;
function next() {
if (current) {
var value = current.value;
current = current.next;
return {
done: false,
value: value
};
} else {
return {
done: true
};
}
}
return iterator;
}
var one = new Obj(1);
var two = new Obj(2);
var three = new Obj(3);
one.next = two;
two.next = three;
for (var i of one){
console.log(i);
}
// 1
// 2
// 2
// 3
上面代码首先在构造函数的原型链上部署Symbol.iterator方法，调用该方法会返回遍历器对象iterator，调用该对象的next方法，在返回一个值的同
时，自动将内部指针移到下一个实例。
下面是另一个为对象添加Iterator接口的例子。
let obj = {
data: [ 'hello', 'world' ],
[Symbol.iterator]() {
const self = this;
let index = 0;
return {
next() {
if (index &lt; self.data.length) {
return {
value: self.data[index++],
done: false
};
} else {
return { value: undefined, done: true };
}
}
};
}
};
对于类似数组的对象（存在数值键名和length属性），部署Iterator接口，有一个简便方法，就是Symbol.iterator方法直接引用数组的Iterator接口。
NodeList.prototype[Symbol.iterator] = Array.prototype[Symbol.iterator];
// 或者
NodeList.prototype[Symbol.iterator] = [][Symbol.iterator];
[...document.querySelectorAll('div')] // 可以执行了
下面是类似数组的对象调用数组的Symbol.iterator方法的例子。
let iterable = {
0: 'a',
1: 'b',
2: 'c',
length: 3,
[Symbol.iterator]: Array.prototype[Symbol.iterator]
};
for (let item of iterable) {
console.log(item); // 'a', 'b', 'c'
}
注意，普通对象部署数组的Symbol.iterator方法，并无效果。
let iterable = {
a: 'a',
b: 'b',
c: 'c',
length: 3,
[Symbol.iterator]: Array.prototype[Symbol.iterator]
};
for (let item of iterable) {
console.log(item); // undefined, undefined, undefined
}
如果Symbol.iterator方法对应的不是遍历器生成函数（即会返回一个遍历器对象），解释引擎将会报错。
var obj = {};
obj[Symbol.iterator] = () =&gt; 1;
[...obj] // TypeError: [] is not a function
上面代码中，变量obj的Symbol.iterator方法对应的不是遍历器生成函数，因此报错。
有了遍历器接口，数据结构就可以用for...of循环遍历（详见下文），也可以使用while循环遍历。
var $iterator = ITERABLE[Symbol.iterator]();
var $result = $iterator.next();
while (!$result.done) {
var x = $result.value;
// ...
$result = $iterator.next();
}
上面代码中，ITERABLE代表某种可遍历的数据结构，$iterator是它的遍历器对象。遍历器对象每次移动指针（next方法），都检查一下返回值
的done属性，如果遍历还没结束，就移动遍历器对象的指针到下一步（next方法），不断循环。
14.3 调用Iterator接口的场合
有一些场合会默认调用Iterator接口（即Symbol.iterator方法），除了下文会介绍的for...of循环，还有几个别的场合。
（1）解构赋值
对数组和Set结构进行解构赋值时，会默认调用Symbol.iterator方法。
let set = new Set().add('a').add('b').add('c');
let [x,y] = set;
// x='a'; y='b'
let [first, ...rest] = set;
// first='a'; rest=['b','c'];
（2）扩展运算符
扩展运算符（...）也会调用默认的iterator接口。
// 例一
var str = 'hello';
[...str] // ['h','e','l','l','o']
// 例二
let arr = ['b', 'c'];
['a', ...arr, 'd']
// ['a', 'b', 'c', 'd']
上面代码的扩展运算符内部就调用Iterator接口。
实际上，这提供了一种简便机制，可以将任何部署了Iterator接口的数据结构，转为数组。也就是说，只要某个数据结构部署了Iterator接口，就可以对
它使用扩展运算符，将其转为数组。
let arr = [...iterable];
（3）yield*
yield*后面跟的是一个可遍历的结构，它会调用该结构的遍历器接口。
let generator = function* () {
yield 1;
yield* [2,3,4];
yield 5;
};
var iterator = generator();
iterator.next() // { value: 1, done: false }
iterator.next() // { value: 2, done: false }
iterator.next() // { value: 3, done: false }
iterator.next() // { value: 4, done: false }
iterator.next() // { value: 5, done: false }
iterator.next() // { value: undefined, done: true }
（4）其他场合
由于数组的遍历会调用遍历器接口，所以任何接受数组作为参数的场合，其实都调用了遍历器接口。下面是一些例子。
for...of
Array.from()
Map(), Set(), WeakMap(), WeakSet()（比如new Map([['a',1],['b',2]])）
Promise.all()
Promise.race()
14.4 字符串的Iterator接口
字符串是一个类似数组的对象，也原生具有Iterator接口。
var someString = "hi";
typeof someString[Symbol.iterator]
// "function"
var iterator = someString[Symbol.iterator]();
iterator.next() // { value: "h", done: false }
iterator.next() // { value: "i", done: false }
iterator.next() // { value: undefined, done: true }
上面代码中，调用Symbol.iterator方法返回一个遍历器对象，在这个遍历器上可以调用next方法，实现对于字符串的遍历。
可以覆盖原生的Symbol.iterator方法，达到修改遍历器行为的目的。
var str = new String("hi");
[...str] // ["h", "i"]
str[Symbol.iterator] = function() {
return {
next: function() {
if (this._first) {
this._first = false;
return { value: "bye", done: false };
} else {
return { done: true };
}
},
_first: true
};
};
[...str] // ["bye"]
str // "hi"
上面代码中，字符串str的Symbol.iterator方法被修改了，所以扩展运算符（...）返回的值变成了bye，而字符串本身还是hi。
14.5 Iterator接口与Generator函数
Symbol.iterator方法的最简单实现，还是使用下一章要介绍的Generator函数。
var myIterable = {};
myIterable[Symbol.iterator] = function* () {
yield 1;
yield 2;
yield 3;
};
[...myIterable] // [1, 2, 3]
// 或者采用下面的简洁写法
let obj = {
* [Symbol.iterator]() {
yield 'hello';
yield 'world';
}
};
for (let x of obj) {
console.log(x);
}
// hello
// world
上面代码中，Symbol.iterator方法几乎不用部署任何代码，只要用yield命令给出每一步的返回值即可。
14.6 遍历器对象的return()，throw()
遍历器对象除了具有next方法，还可以具有return方法和throw方法。如果你自己写遍历器对象生成函数，那么next方法是必须部署的，return方法
和throw方法是否部署是可选的。
return方法的使用场合是，如果for...of循环提前退出（通常是因为出错，或者有break语句或continue语句），就会调用return方法。如果一个对
象在完成遍历前，需要清理或释放资源，就可以部署return方法。
function readLinesSync(file) {
return {
next() {
if (file.isAtEndOfFile()) {
file.close();
return { done: true };
}
},
return() {
file.close();
return { done: true };
},
};
}
上面代码中，函数readLinesSync接受一个文件对象作为参数，返回一个遍历器对象，其中除了next方法，还部署了return方法。下面，我们让文件的
遍历提前返回，这样就会触发执行return方法。
for (let line of readLinesSync(fileName)) {
console.log(x);
break;
}
注意，return方法必须返回一个对象，这是Generator规格决定的。
throw方法主要是配合Generator函数使用，一般的遍历器对象用不到这个方法。请参阅《Generator函数》一章。
14.7 for...of循环
ES6借鉴C++、Java、C#和Python语言，引入了for...of循环，作为遍历所有数据结构的统一的方法。一个数据结构只要部署了Symbol.iterator属
性，就被视为具有iterator接口，就可以用for...of循环遍历它的成员。也就是说，for...of循环内部调用的是数据结构的Symbol.iterator方法。
for...of循环可以使用的范围包括数组、Set和Map结构、某些类似数组的对象（比如arguments对象、DOM NodeList对象）、后文的Generator对象，
以及字符串。
14.7.1 数组
数组原生具备iterator接口，for...of循环本质上就是调用这个接口产生的遍历器，可以用下面的代码证明。
const arr = ['red', 'green', 'blue'];
let iterator = arr[Symbol.iterator]();
for(let v of arr) {
console.log(v); // red green blue
}
for(let v of iterator) {
console.log(v); // red green blue
}
上面代码的for...of循环的两种写法是等价的。
for...of循环可以代替数组实例的forEach方法。
const arr = ['red', 'green', 'blue'];
arr.forEach(function (element, index) {
console.log(element); // red green blue
console.log(index); // 0 1 2
});
JavaScript原有的for...in循环，只能获得对象的键名，不能直接获取键值。ES6提供for...of循环，允许遍历获得键值。
var arr = ['a', 'b', 'c', 'd'];
for (let a in arr) {
console.log(a); // 0 1 2 3
}
for (let a of arr) {
console.log(a); // a b c d
}
上面代码表明，for...in循环读取键名，for...of循环读取键值。如果要通过for...of循环，获取数组的索引，可以借助数组实例的entries方法
和keys方法，参见《数组的扩展》章节。
for...of循环调用遍历器接口，数组的遍历器接口只返回具有数字索引的属性。这一点跟for...in循环也不一样。
let arr = [3, 5, 7];
arr.foo = 'hello';
for (let i in arr) {
console.log(i); // "0", "1", "2", "foo"
}
for (let i of arr) {
console.log(i); // "3", "5", "7"
}
上面代码中，for...of循环不会返回数组arr的foo属性。
14.7.2 Set和Map结构
Set和Map结构也原生具有Iterator接口，可以直接使用for...of循环。
var engines = new Set(["Gecko", "Trident", "Webkit", "Webkit"]);
for (var e of engines) {
console.log(e);
}
// Gecko
// Trident
// Webkit
var es6 = new Map();
es6.set("edition", 6);
es6.set("committee", "TC39");
es6.set("standard", "ECMA-262");
for (var [name, value] of es6) {
console.log(name + ": " + value);
}
// edition: 6
// committee: TC39
// standard: ECMA-262
上面代码演示了如何遍历Set结构和Map结构。值得注意的地方有两个，首先，遍历的顺序是按照各个成员被添加进数据结构的顺序。其次，Set结构遍
历时，返回的是一个值，而Map结构遍历时，返回的是一个数组，该数组的两个成员分别为当前Map成员的键名和键值。
let map = new Map().set('a', 1).set('b', 2);
for (let pair of map) {
console.log(pair);
}
// ['a', 1]
// ['b', 2]
for (let [key, value] of map) {
console.log(key + ' : ' + value);
}
// a : 1
// b : 2
14.7.3 计算生成的数据结构
有些数据结构是在现有数据结构的基础上，计算生成的。比如，ES6的数组、Set、Map都部署了以下三个方法，调用后都返回遍历器对象。
entries() 返回一个遍历器对象，用来遍历[键名, 键值]组成的数组。对于数组，键名就是索引值；对于Set，键名与键值相同。Map结构的
iterator接口，默认就是调用entries方法。
keys() 返回一个遍历器对象，用来遍历所有的键名。
values() 返回一个遍历器对象，用来遍历所有的键值。
这三个方法调用后生成的遍历器对象，所遍历的都是计算生成的数据结构。
let arr = ['a', 'b', 'c'];
for (let pair of arr.entries()) {
console.log(pair);
}
// [0, 'a']
// [1, 'b']
// [2, 'c']
14.7.4 类似数组的对象
类似数组的对象包括好几类。下面是for...of循环用于字符串、DOM NodeList对象、arguments对象的例子。
// 字符串
let str = "hello";
for (let s of str) {
console.log(s); // h e l l o
}
// DOM NodeList对象
let paras = document.querySelectorAll("p");
for (let p of paras) {
p.classList.add("test");
}
// arguments对象
function printArgs() {
for (let x of arguments) {
console.log(x);
}
}
printArgs('a', 'b');
// 'a'
// 'b'
对于字符串来说，for...of循环还有一个特点，就是会正确识别32位UTF-16字符。
for (let x of 'a\uD83D\uDC0A') {
console.log(x);
}
// 'a'
// '\uD83D\uDC0A'
并不是所有类似数组的对象都具有iterator接口，一个简便的解决方法，就是使用Array.from方法将其转为数组。
let arrayLike = { length: 2, 0: 'a', 1: 'b' };
// 报错
for (let x of arrayLike) {
console.log(x);
}
// 正确
for (let x of Array.from(arrayLike)) {
console.log(x);
}
14.7.5 对象
对于普通的对象，for...of结构不能直接使用，会报错，必须部署了iterator接口后才能使用。但是，这样情况下，for...in循环依然可以用来遍历键
名。
var es6 = {
edition: 6,
committee: "TC39",
standard: "ECMA-262"
};
for (e in es6) {
console.log(e);
}
// edition
// committee
// standard
for (e of es6) {
console.log(e);
}
// TypeError: es6 is not iterable
上面代码表示，对于普通的对象，for...in循环可以遍历键名，for...of循环会报错。
一种解决方法是，使用Object.keys方法将对象的键名生成一个数组，然后遍历这个数组。
for (var key of Object.keys(someObject)) {
console.log(key + ": " + someObject[key]);
}
在对象上部署iterator接口的代码，参见本章前面部分。一个方便的方法是将数组的Symbol.iterator属性，直接赋值给其他对象的Symbol.iterator属
性。比如，想要让for...of环遍历jQuery对象，只要加上下面这一行就可以了。
jQuery.prototype[Symbol.iterator] =
Array.prototype[Symbol.iterator];
另一个方法是使用Generator函数将对象重新包装一下。
function* entries(obj) {
for (let key of Object.keys(obj)) {
yield [key, obj[key]];
}
}
for (let [key, value] of entries(obj)) {
console.log(key, "-&gt;", value);
}
// a -&gt; 1
// b -&gt; 2
// c -&gt; 3
14.7.6 与其他遍历语法的比较
以数组为例，JavaScript提供多种遍历语法。最原始的写法就是for循环。
for (var index = 0; index &lt; myArray.length; index++) {
console.log(myArray[index]);
}
这种写法比较麻烦，因此数组提供内置的forEach方法。
myArray.forEach(function (value) {
console.log(value);
});
这种写法的问题在于，无法中途跳出forEach循环，break命令或return命令都不能奏效。
for...in循环可以遍历数组的键名。
for (var index in myArray) {
console.log(myArray[index]);
}
for...in循环有几个缺点。
数组的键名是数字，但是for...in循环是以字符串作为键名“0”、“1”、“2”等等。
for...in循环不仅遍历数字键名，还会遍历手动添加的其他键，甚至包括原型链上的键。
某些情况下，for...in循环会以任意顺序遍历键名。
总之，for...in循环主要是为遍历对象而设计的，不适用于遍历数组。
for...of循环相比上面几种做法，有一些显著的优点。
for (let value of myArray) {
console.log(value);
}
有着同for...in一样的简洁语法，但是没有for...in那些缺点。
不同用于forEach方法，它可以与break、continue和return配合使用。
提供了遍历所有数据结构的统一操作接口。
下面是一个使用break语句，跳出for...of循环的例子。
for (var n of fibonacci) {
if (n &gt; 1000)
break;
console.log(n);
}
上面的例子，会输出斐波纳契数列小于等于1000的项。如果当前项大于1000，就会使用break语句跳出for...of循环。
15 Generator 函数
15.1 简介
15.1.1 基本概念
Generator函数是ES6提供的一种异步编程解决方案，语法行为与传统函数完全不同。本章详细介绍Generator函数的语法和API，它的异步编程应用请
看《异步操作》一章。
Generator函数有多种理解角度。从语法上，首先可以把它理解成，Generator函数是一个状态机，封装了多个内部状态。
执行Generator函数会返回一个遍历器对象，也就是说，Generator函数除了状态机，还是一个遍历器对象生成函数。返回的遍历器对象，可以依次遍
历Generator函数内部的每一个状态。
形式上，Generator函数是一个普通函数，但是有两个特征。一是，function关键字与函数名之间有一个星号；二是，函数体内部使用yield语句，定
义不同的内部状态（yield语句在英语里的意思就是“产出”）。
function* helloWorldGenerator() {
yield 'hello';
yield 'world';
return 'ending';
}
var hw = helloWorldGenerator();
上面代码定义了一个Generator函数helloWorldGenerator，它内部有两个yield语句“hello”和“world”，即该函数有三个状态：hello，world和return语
句（结束执行）。
然后，Generator函数的调用方法与普通函数一样，也是在函数名后面加上一对圆括号。不同的是，调用Generator函数后，该函数并不执行，返回的
也不是函数运行结果，而是一个指向内部状态的指针对象，也就是上一章介绍的遍历器对象（Iterator Object）。
下一步，必须调用遍历器对象的next方法，使得指针移向下一个状态。也就是说，每次调用next方法，内部指针就从函数头部或上一次停下来的地方
开始执行，直到遇到下一个yield语句（或return语句）为止。换言之，Generator函数是分段执行的，yield语句是暂停执行的标记，而next方法可
以恢复执行。
hw.next()
// { value: 'hello', done: false }
hw.next()
// { value: 'world', done: false }
hw.next()
// { value: 'ending', done: true }
hw.next()
// { value: undefined, done: true }
上面代码一共调用了四次next方法。
第一次调用，Generator函数开始执行，直到遇到第一个yield语句为止。next方法返回一个对象，它的value属性就是当前yield语句的值
hello，done属性的值false，表示遍历还没有结束。
第二次调用，Generator函数从上次yield语句停下的地方，一直执行到下一个yield语句。next方法返回的对象的value属性就是当前yield语句的值
world，done属性的值false，表示遍历还没有结束。
第三次调用，Generator函数从上次yield语句停下的地方，一直执行到return语句（如果没有return语句，就执行到函数结束）。next方法返回的对
象的value属性，就是紧跟在return语句后面的表达式的值（如果没有return语句，则value属性的值为undefined），done属性的值true，表示遍历
已经结束。
第四次调用，此时Generator函数已经运行完毕，next方法返回对象的value属性为undefined，done属性为true。以后再调用next方法，返回的都是
这个值。
总结一下，调用Generator函数，返回一个遍历器对象，代表Generator函数的内部指针。以后，每次调用遍历器对象的next方法，就会返回一个有
着value和done两个属性的对象。value属性表示当前的内部状态的值，是yield语句后面那个表达式的值；done属性是一个布尔值，表示是否遍历结
束。
ES6没有规定，function关键字与函数名之间的星号，写在哪个位置。这导致下面的写法都能通过。
function * foo(x, y) { ··· }
function *foo(x, y) { ··· }
function* foo(x, y) { ··· }
function*foo(x, y) { ··· }
由于Generator函数仍然是普通函数，所以一般的写法是上面的第三种，即星号紧跟在function关键字后面。本书也采用这种写法。
15.1.2 yield语句
由于Generator函数返回的遍历器对象，只有调用next方法才会遍历下一个内部状态，所以其实提供了一种可以暂停执行的函数。yield语句就是暂停
标志。
遍历器对象的next方法的运行逻辑如下。
（1）遇到yield语句，就暂停执行后面的操作，并将紧跟在yield后面的那个表达式的值，作为返回的对象的value属性值。
（2）下一次调用next方法时，再继续往下执行，直到遇到下一个yield语句。
（3）如果没有再遇到新的yield语句，就一直运行到函数结束，直到return语句为止，并将return语句后面的表达式的值，作为返回的对象
的value属性值。
（4）如果该函数没有return语句，则返回的对象的value属性值为undefined。
需要注意的是，yield语句后面的表达式，只有当调用next方法、内部指针指向该语句时才会执行，因此等于为JavaScript提供了手动的“惰性求
值”（Lazy Evaluation）的语法功能。
function* gen() {
yield 123 + 456;
}
上面代码中，yield后面的表达式123 + 456，不会立即求值，只会在next方法将指针移到这一句时，才会求值。
yield语句与return语句既有相似之处，也有区别。相似之处在于，都能返回紧跟在语句后面的那个表达式的值。区别在于每次遇到yield，函数暂停
执行，下一次再从该位置继续向后执行，而return语句不具备位置记忆的功能。一个函数里面，只能执行一次（或者说一个）return语句，但是可以
执行多次（或者说多个）yield语句。正常函数只能返回一个值，因为只能执行一次return；Generator函数可以返回一系列的值，因为可以有任意多
个yield。从另一个角度看，也可以说Generator生成了一系列的值，这也就是它的名称的来历（在英语中，generator这个词是“生成器”的意思）。
Generator函数可以不用yield语句，这时就变成了一个单纯的暂缓执行函数。
function* f() {
console.log('执行了！')
}
var generator = f();
setTimeout(function () {
generator.next()
}, 2000);
上面代码中，函数f如果是普通函数，在为变量generator赋值时就会执行。但是，函数f是一个Generator函数，就变成只有调用next方法时，函
数f才会执行。
另外需要注意，yield语句不能用在普通函数中，否则会报错。
(function (){
yield 1;
})()
// SyntaxError: Unexpected number
上面代码在一个普通函数中使用yield语句，结果产生一个句法错误。
下面是另外一个例子。
var arr = [1, [[2, 3], 4], [5, 6]];
var flat = function* (a) {
a.forEach(function (item) {
if (typeof item !== 'number') {
yield* flat(item);
} else {
yield item;
}
}
};
for (var f of flat(arr)){
console.log(f);
}
上面代码也会产生句法错误，因为forEach方法的参数是一个普通函数，但是在里面使用了yield语句（这个函数里面还使用了yield*语句，这里可以
不用理会，详细说明见后文）。一种修改方法是改用for循环。
var arr = [1, [[2, 3], 4], [5, 6]];
var flat = function* (a) {
var length = a.length;
for (var i = 0; i &lt; length; i++) {
var item = a[i];
if (typeof item !== 'number') {
yield* flat(item);
} else {
yield item;
}
}
};
for (var f of flat(arr)) {
console.log(f);
}
// 1, 2, 3, 4, 5, 6
另外，yield语句如果用在一个表达式之中，必须放在圆括号里面。
console.log('Hello' + yield); // SyntaxError
console.log('Hello' + yield 123); // SyntaxError
console.log('Hello' + (yield)); // OK
console.log('Hello' + (yield 123)); // OK
yield语句用作函数参数或赋值表达式的右边，可以不加括号。
foo(yield 'a', yield 'b'); // OK
let input = yield; // OK
15.1.3 与Iterator接口的关系
上一章说过，任意一个对象的Symbol.iterator方法，等于该对象的遍历器生成函数，调用该函数会返回该对象的一个遍历器对象。
由于Generator函数就是遍历器生成函数，因此可以把Generator赋值给对象的Symbol.iterator属性，从而使得该对象具有Iterator接口。
var myIterable = {};
myIterable[Symbol.iterator] = function* () {
yield 1;
yield 2;
yield 3;
};
[...myIterable] // [1, 2, 3]
上面代码中，Generator函数赋值给Symbol.iterator属性，从而使得myIterable对象具有了Iterator接口，可以被...运算符遍历了。
Generator函数执行后，返回一个遍历器对象。该对象本身也具有Symbol.iterator属性，执行后返回自身。
function* gen(){
// some code
}
var g = gen();
g[Symbol.iterator]() === g
// true
上面代码中，gen是一个Generator函数，调用它会生成一个遍历器对象g。它的Symbol.iterator属性，也是一个遍历器对象生成函数，执行后返回它
自己。
15.2 next方法的参数
yield句本身没有返回值，或者说总是返回undefined。next方法可以带一个参数，该参数就会被当作上一个yield语句的返回值。
function* f() {
for(var i=0; true; i++) {
var reset = yield i;
if(reset) { i = -1; }
}
}
var g = f();
g.next() // { value: 0, done: false }
g.next() // { value: 1, done: false }
g.next(true) // { value: 0, done: false }
上面代码先定义了一个可以无限运行的Generator函数f，如果next方法没有参数，每次运行到yield语句，变量reset的值总是undefined。当next方
法带一个参数true时，当前的变量reset就被重置为这个参数（即true），因此i会等于-1，下一轮循环就会从-1开始递增。
这个功能有很重要的语法意义。Generator函数从暂停状态到恢复运行，它的上下文状态（context）是不变的。通过next方法的参数，就有办法在
Generator函数开始运行之后，继续向函数体内部注入值。也就是说，可以在Generator函数运行的不同阶段，从外部向内部注入不同的值，从而调整
函数行为。
再看一个例子。
function* foo(x) {
var y = 2 * (yield (x + 1));
var z = yield (y / 3);
return (x + y + z);
}
var a = foo(5);
a.next() // Object{value:6, done:false}
a.next() // Object{value:NaN, done:false}
a.next() // Object{value:NaN, done:true}
var b = foo(5);
b.next() // { value:6, done:false }
b.next(12) // { value:8, done:false }
b.next(13) // { value:42, done:true }
上面代码中，第二次运行next方法的时候不带参数，导致y的值等于2 * undefined（即NaN），除以3以后还是NaN，因此返回对象的value属性也等
于NaN。第三次运行Next方法的时候不带参数，所以z等于undefined，返回对象的value属性等于5 + NaN + undefined，即NaN。
如果向next方法提供参数，返回结果就完全不一样了。上面代码第一次调用b的next方法时，返回x+1的值6；第二次调用next方法，将上一次yield语
句的值设为12，因此y等于24，返回y / 3的值8；第三次调用next方法，将上一次yield语句的值设为13，因此z等于13，这时x等于5，y等于24，所
以return语句的值等于42。
注意，由于next方法的参数表示上一个yield语句的返回值，所以第一次使用next方法时，不能带有参数。V8引擎直接忽略第一次使用next方法时的
参数，只有从第二次使用next方法开始，参数才是有效的。从语义上讲，第一个next方法用来启动遍历器对象，所以不用带有参数。
如果想要第一次调用next方法时，就能够输入值，可以在Generator函数外面再包一层。
function wrapper(generatorFunction) {
return function (...args) {
let generatorObject = generatorFunction(...args);
generatorObject.next();
return generatorObject;
};
}
const wrapped = wrapper(function* () {
console.log(`First input: ${yield}`);
return 'DONE';
});
wrapped().next('hello!')
// First input: hello!
上面代码中，Generator函数如果不用wrapper先包一层，是无法第一次调用next方法，就输入参数的。
再看一个通过next方法的参数，向Generator函数内部输入值的例子。
function* dataConsumer() {
console.log('Started');
console.log(`1. ${yield}`);
console.log(`2. ${yield}`);
return 'result';
}
let genObj = dataConsumer();
genObj.next();
// Started
genObj.next('a')
// 1. a
genObj.next('b')
// 2. b
上面代码是一个很直观的例子，每次通过next方法向Generator函数输入值，然后打印出来。
15.3 for...of循环
for...of循环可以自动遍历Generator函数时生成的Iterator对象，且此时不再需要调用next方法。
function *foo() {
yield 1;
yield 2;
yield 3;
yield 4;
yield 5;
return 6;
}
for (let v of foo()) {
console.log(v);
}
// 1 2 3 4 5
上面代码使用for...of循环，依次显示5个yield语句的值。这里需要注意，一旦next方法的返回对象的done属性为true，for...of循环就会中止，且
不包含该返回对象，所以上面代码的return语句返回的6，不包括在for...of循环之中。
下面是一个利用Generator函数和for...of循环，实现斐波那契数列的例子。
function* fibonacci() {
let [prev, curr] = [0, 1];
for (;;) {
[prev, curr] = [curr, prev + curr];
yield curr;
}
}
for (let n of fibonacci()) {
if (n &gt; 1000) break;
console.log(n);
}
从上面代码可见，使用for...of语句时不需要使用next方法。
利用for...of循环，可以写出遍历任意对象（object）的方法。原生的JavaScript对象没有遍历接口，无法使用for...of循环，通过Generator函数为
它加上这个接口，就可以用了。
function* objectEntries(obj) {
let propKeys = Reflect.ownKeys(obj);
for (let propKey of propKeys) {
yield [propKey, obj[propKey]];
}
}
let jane = { first: 'Jane', last: 'Doe' };
for (let [key, value] of objectEntries(jane)) {
console.log(`${key}: ${value}`);
}
// first: Jane
// last: Doe
上面代码中，对象jane原生不具备Iterator接口，无法用for...of遍历。这时，我们通过Generator函数objectEntries为它加上遍历器接口，就可以
用for...of遍历了。加上遍历器接口的另一种写法是，将Generator函数加到对象的Symbol.iterator属性上面。
function* objectEntries() {
let propKeys = Object.keys(this);
for (let propKey of propKeys) {
yield [propKey, this[propKey]];
}
}
let jane = { first: 'Jane', last: 'Doe' };
jane[Symbol.iterator] = objectEntries;
for (let [key, value] of jane) {
console.log(`${key}: ${value}`);
}
// first: Jane
// last: Doe
除了for...of循环以外，扩展运算符（...）、解构赋值和Array.from方法内部调用的，都是遍历器接口。这意味着，它们都可以将Generator函数返
回的Iterator对象，作为参数。
function* numbers () {
yield 1
yield 2
return 3
yield 4
}
// 扩展运算符
[...numbers()] // [1, 2]
// Array.form 方法
Array.from(numbers()) // [1, 2]
// 解构赋值
let [x, y] = numbers();
x // 1
y // 2
// for...of 循环
for (let n of numbers()) {
console.log(n)
}
// 1
// 2
15.4 Generator.prototype.throw()
Generator函数返回的遍历器对象，都有一个throw方法，可以在函数体外抛出错误，然后在Generator函数体内捕获。
var g = function* () {
try {
yield;
} catch (e) {
console.log('内部捕获', e);
}
};
var i = g();
i.next();
try {
i.throw('a');
i.throw('b');
} catch (e) {
console.log('外部捕获', e);
}
// 内部捕获 a
// 外部捕获 b
上面代码中，遍历器对象i连续抛出两个错误。第一个错误被Generator函数体内的catch语句捕获。i第二次抛出错误，由于Generator函数内部
的catch语句已经执行过了，不会再捕捉到这个错误了，所以这个错误就被抛出了Generator函数体，被函数体外的catch语句捕获。
throw方法可以接受一个参数，该参数会被catch语句接收，建议抛出Error对象的实例。
var g = function* () {
try {
yield;
} catch (e) {
console.log(e);
}
};
var i = g();
i.next();
i.throw(new Error('出错了！'));
// Error: 出错了！(…)
注意，不要混淆遍历器对象的throw方法和全局的throw命令。上面代码的错误，是用遍历器对象的throw方法抛出的，而不是用throw命令抛出的。后
者只能被函数体外的catch语句捕获。
var g = function* () {
while (true) {
try {
yield;
} catch (e) {
if (e != 'a') throw e;
console.log('内部捕获', e);
}
}
};
var i = g();
i.next();
try {
throw new Error('a');
throw new Error('b');
} catch (e) {
console.log('外部捕获', e);
}
// 外部捕获 [Error: a]
上面代码之所以只捕获了a，是因为函数体外的catch语句块，捕获了抛出的a错误以后，就不会再继续try代码块里面剩余的语句了。
如果Generator函数内部没有部署try...catch代码块，那么throw方法抛出的错误，将被外部try...catch代码块捕获。
var g = function* () {
while (true) {
yield;
console.log('内部捕获', e);
}
};
var i = g();
i.next();
try {
i.throw('a');
i.throw('b');
} catch (e) {
console.log('外部捕获', e);
}
// 外部捕获 a
上面代码中，Generator函数g内部没有部署try...catch代码块，所以抛出的错误直接被外部catch代码块捕获。
如果Generator函数内部和外部，都没有部署try...catch代码块，那么程序将报错，直接中断执行。
var gen = function* gen(){
yield console.log('hello');
yield console.log('world');
}
var g = gen();
g.next();
g.throw();
// hello
// Uncaught undefined
上面代码中，g.throw抛出错误以后，没有任何try...catch代码块可以捕获这个错误，导致程序报错，中断执行。
throw方法被捕获以后，会附带执行下一条yield语句。也就是说，会附带执行一次next方法。
var gen = function* gen(){
try {
yield console.log('a');
} catch (e) {
// ...
}
yield console.log('b');
yield console.log('c');
}
var g = gen();
g.next() // a
g.throw() // b
g.next() // c
上面代码中，g.throw方法被捕获以后，自动执行了一次next方法，所以会打印b。另外，也可以看到，只要Generator函数内部部署了try...catch代
码块，那么遍历器的throw方法抛出的错误，不影响下一次遍历。
另外，throw命令与g.throw方法是无关的，两者互不影响。
var gen = function* gen(){
yield console.log('hello');
yield console.log('world');
}
var g = gen();
g.next();
try {
throw new Error();
} catch (e) {
g.next();
}
// hello
// world
上面代码中，throw命令抛出的错误不会影响到遍历器的状态，所以两次执行next方法，都进行了正确的操作。
这种函数体内捕获错误的机制，大大方便了对错误的处理。多个yield语句，可以只用一个try...catch代码块来捕获错误。如果使用回调函数的写
法，想要捕获多个错误，就不得不为每个函数内部写一个错误处理语句，现在只在Generator函数内部写一次catch语句就可以了。
Generator函数体外抛出的错误，可以在函数体内捕获；反过来，Generator函数体内抛出的错误，也可以被函数体外的catch捕获。
function *foo() {
var x = yield 3;
var y = x.toUpperCase();
yield y;
}
var it = foo();
it.next(); // { value:3, done:false }
try {
it.next(42);
} catch (err) {
console.log(err);
}
上面代码中，第二个next方法向函数体内传入一个参数42，数值是没有toUpperCase方法的，所以会抛出一个TypeError错误，被函数体外的catch捕
获。
一旦Generator执行过程中抛出错误，且没有被内部捕获，就不会再执行下去了。如果此后还调用next方法，将返回一个value属性等
于undefined、done属性等于true的对象，即JavaScript引擎认为这个Generator已经运行结束了。
function* g() {
yield 1;
console.log('throwing an exception');
throw new Error('generator broke!');
yield 2;
yield 3;
}
function log(generator) {
var v;
console.log('starting generator');
try {
v = generator.next();
console.log('第一次运行next方法', v);
} catch (err) {
console.log('捕捉错误', v);
}
try {
v = generator.next();
console.log('第二次运行next方法', v);
} catch (err) {
console.log('捕捉错误', v);
}
try {
v = generator.next();
console.log('第三次运行next方法', v);
} catch (err) {
console.log('捕捉错误', v);
}
console.log('caller done');
}
log(g());
// starting generator
// 第一次运行next方法 { value: 1, done: false }
// throwing an exception
// 捕捉错误 { value: 1, done: false }
// 第三次运行next方法 { value: undefined, done: true }
// caller done
上面代码一共三次运行next方法，第二次运行的时候会抛出错误，然后第三次运行的时候，Generator函数就已经结束了，不再执行下去了。
15.5 Generator.prototype.return()
Generator函数返回的遍历器对象，还有一个return方法，可以返回给定的值，并且终结遍历Generator函数。
function* gen() {
yield 1;
yield 2;
yield 3;
}
var g = gen();
g.next() // { value: 1, done: false }
g.return('foo') // { value: "foo", done: true }
g.next() // { value: undefined, done: true }
上面代码中，遍历器对象g调用return方法后，返回值的value属性就是return方法的参数foo。并且，Generator函数的遍历就终止了，返回值
的done属性为true，以后再调用next方法，done属性总是返回true。
如果return方法调用时，不提供参数，则返回值的value属性为undefined。
function* gen() {
yield 1;
yield 2;
yield 3;
}
var g = gen();
g.next() // { value: 1, done: false }
g.return() // { value: undefined, done: true }
如果Generator函数内部有try...finally代码块，那么return方法会推迟到finally代码块执行完再执行。
function* numbers () {
yield 1;
try {
yield 2;
yield 3;
} finally {
yield 4;
yield 5;
}
yield 6;
}
var g = numbers()
g.next() // { done: false, value: 1 }
g.next() // { done: false, value: 2 }
g.return(7) // { done: false, value: 4 }
g.next() // { done: false, value: 5 }
g.next() // { done: true, value: 7 }
上面代码中，调用return方法后，就开始执行finally代码块，然后等到finally代码块执行完，再执行return方法。
15.6 yield*语句
如果在Generater函数内部，调用另一个Generator函数，默认情况下是没有效果的。
function* foo() {
yield 'a';
yield 'b';
}
function* bar() {
yield 'x';
foo();
yield 'y';
}
for (let v of bar()){
console.log(v);
}
// "x"
// "y"
上面代码中，foo和bar都是Generator函数，在bar里面调用foo，是不会有效果的。
这个就需要用到yield*语句，用来在一个Generator函数里面执行另一个Generator函数。
function* bar() {
yield 'x';
yield* foo();
yield 'y';
}
// 等同于
function* bar() {
yield 'x';
yield 'a';
yield 'b';
yield 'y';
}
// 等同于
function* bar() {
yield 'x';
for (let v of foo()) {
yield v;
}
yield 'y';
}
for (let v of bar()){
console.log(v);
}
// "x"
// "a"
// "b"
// "y"
再来看一个对比的例子。
function* inner() {
yield 'hello!';
}
function* outer1() {
yield 'open';
yield inner();
yield 'close';
}
var gen = outer1()
gen.next().value // "open"
gen.next().value // 返回一个遍历器对象
gen.next().value // "close"
function* outer2() {
yield 'open'
yield* inner()
yield 'close'
}
var gen = outer2()
gen.next().value // "open"
gen.next().value // "hello!"
gen.next().value // "close"
上面例子中，outer2使用了yield*，outer1没使用。结果就是，outer1返回一个遍历器对象，outer2返回该遍历器对象的内部值。
从语法角度看，如果yield命令后面跟的是一个遍历器对象，需要在yield命令后面加上星号，表明它返回的是一个遍历器对象。这被称为yield*语
句。
let delegatedIterator = (function* () {
yield 'Hello!';
yield 'Bye!';
}());
let delegatingIterator = (function* () {
yield 'Greetings!';
yield* delegatedIterator;
yield 'Ok, bye.';
}());
for(let value of delegatingIterator) {
console.log(value);
}
// "Greetings!
// "Hello!"
// "Bye!"
// "Ok, bye."
上面代码中，delegatingIterator是代理者，delegatedIterator是被代理者。由于yield* delegatedIterator语句得到的值，是一个遍历器，所以要
用星号表示。运行结果就是使用一个遍历器，遍历了多个Generator函数，有递归的效果。
yield*后面的Generator函数（没有return语句时），等同于在Generator函数内部，部署一个for...of循环。
function* concat(iter1, iter2) {
yield* iter1;
yield* iter2;
}
// 等同于
function* concat(iter1, iter2) {
for (var value of iter1) {
yield value;
}
for (var value of iter2) {
yield value;
}
}
上面代码说明，yield*后面的Generator函数（没有return语句时），不过是for...of的一种简写形式，完全可以用后者替代前者。反之，则需要
用var value = yield* iterator的形式获取return语句的值。
如果yield*后面跟着一个数组，由于数组原生支持遍历器，因此就会遍历数组成员。
function* gen(){
yield* ["a", "b", "c"];
}
gen().next() // { value:"a", done:false }
上面代码中，yield命令后面如果不加星号，返回的是整个数组，加了星号就表示返回的是数组的遍历器对象。
实际上，任何数据结构只要有Iterator接口，就可以被yield*遍历。
let read = (function* () {
yield 'hello';
yield* 'hello';
})();
read.next().value // "hello"
read.next().value // "h"
上面代码中，yield语句返回整个字符串，yield*语句返回单个字符。因为字符串具有Iterator接口，所以被yield*遍历。
如果被代理的Generator函数有return语句，那么就可以向代理它的Generator函数返回数据。
function *foo() {
yield 2;
yield 3;
return "foo";
}
function *bar() {
yield 1;
var v = yield *foo();
console.log( "v: " + v );
yield 4;
}
var it = bar();
it.next()
// {value: 1, done: false}
it.next()
// {value: 2, done: false}
it.next()
// {value: 3, done: false}
it.next();
// "v: foo"
// {value: 4, done: false}
it.next()
// {value: undefined, done: true}
上面代码在第四次调用next方法的时候，屏幕上会有输出，这是因为函数foo的return语句，向函数bar提供了返回值。
再看一个例子。
function* genFuncWithReturn() {
yield 'a';
yield 'b';
return 'The result';
}
function* logReturned(genObj) {
let result = yield* genObj;
console.log(result);
}
[...logReturned(genFuncWithReturn())]
// The result
// 值为 [ 'a', 'b' ]
上面代码中，存在两次遍历。第一次是扩展运算符遍历函数logReturned返回的遍历器对象，第二次是yield*语句遍历函数genFuncWithReturn返回的
遍历器对象。这两次遍历的效果是叠加的，最终表现为扩展运算符遍历函数genFuncWithReturn返回的遍历器对象。所以，最后的数据表达式得到的值
等于[ 'a', 'b' ]。但是，函数genFuncWithReturn的return语句的返回值The result，会返回给函数logReturned内部的result变量，因此会有终端
输出。
yield*命令可以很方便地取出嵌套数组的所有成员。
function* iterTree(tree) {
if (Array.isArray(tree)) {
for(let i=0; i &lt; tree.length; i++) {
yield* iterTree(tree[i]);
}
} else {
yield tree;
}
}
const tree = [ 'a', ['b', 'c'], ['d', 'e'] ];
for(let x of iterTree(tree)) {
console.log(x);
}
// a
// b
// c
// d
// e
下面是一个稍微复杂的例子，使用yield*语句遍历完全二叉树。
// 下面是二叉树的构造函数，
// 三个参数分别是左树、当前节点和右树
function Tree(left, label, right) {
this.left = left;
this.label = label;
this.right = right;
}
// 下面是中序（inorder）遍历函数。
// 由于返回的是一个遍历器，所以要用generator函数。
// 函数体内采用递归算法，所以左树和右树要用yield*遍历
function* inorder(t) {
if (t) {
yield* inorder(t.left);
yield t.label;
yield* inorder(t.right);
}
}
// 下面生成二叉树
function make(array) {
// 判断是否为叶节点
if (array.length == 1) return new Tree(null, array[0], null);
return new Tree(make(array[0]), array[1], make(array[2]));
}
let tree = make([[['a'], 'b', ['c']], 'd', [['e'], 'f', ['g']]]);
// 遍历二叉树
var result = [];
for (let node of inorder(tree)) {
result.push(node);
}
result
// ['a', 'b', 'c', 'd', 'e', 'f', 'g']
15.7 作为对象属性的Generator函数
如果一个对象的属性是Generator函数，可以简写成下面的形式。
let obj = {
* myGeneratorMethod() {
···
}
};
上面代码中，myGeneratorMethod属性前面有一个星号，表示这个属性是一个Generator函数。
它的完整形式如下，与上面的写法是等价的。
let obj = {
myGeneratorMethod: function* () {
// ···
}
};
15.8 Generator函数的this
Generator函数总是返回一个遍历器，ES6规定这个遍历器是Generator函数的实例，也继承了Generator函数的prototype对象上的方法。
function* g() {}
g.prototype.hello = function () {
return 'hi!';
};
let obj = g();
obj instanceof g // true
obj.hello() // 'hi!'
上面代码表明，Generator函数g返回的遍历器obj，是g的实例，而且继承了g.prototype。但是，如果把g当作普通的构造函数，并不会生效，因
为g返回的总是遍历器对象，而不是this对象。
function* g() {
this.a = 11;
}
let obj = g();
obj.a // undefined
上面代码中，Generator函数g在this对象上面添加了一个属性a，但是obj对象拿不到这个属性。
Generator函数也不能跟new命令一起用，会报错。
function* F() {
yield this.x = 2;
yield this.y = 3;
}
new F()
// TypeError: F is not a constructor
上面代码中，new命令跟构造函数F一起使用，结果报错，因为F不是构造函数。
那么，有没有办法让Generator函数返回一个正常的对象实例，既可以用next方法，又可以获得正常的this？
下面是一个变通方法。首先，生成一个空对象，使用bind方法绑定Generator函数内部的this。这样，构造函数调用以后，这个空对象就是Generator
函数的实例对象了。
function* F() {
this.a = 1;
yield this.b = 2;
yield this.c = 3;
}
var obj = {};
var f = F.call(obj);
f.next(); // Object {value: 2, done: false}
f.next(); // Object {value: 3, done: false}
f.next(); // Object {value: undefined, done: true}
obj.a // 1
obj.b // 2
obj.c // 3
上面代码中，首先是F内部的this对象绑定obj对象，然后调用它，返回一个Iterator对象。这个对象执行三次next方法（因为F内部有两个yield语
句），完成F内部所有代码的运行。这时，所有内部属性都绑定在obj对象上了，因此obj对象也就成了F的实例。
上面代码中，执行的是遍历器对象f，但是生成的对象实例是obj，有没有办法将这两个对象统一呢？
一个办法就是将obj换成F.prototype。
function* F() {
this.a = 1;
yield this.b = 2;
yield this.c = 3;
}
var f = F.call(F.prototype);
f.next(); // Object {value: 2, done: false}
f.next(); // Object {value: 3, done: false}
f.next(); // Object {value: undefined, done: true}
f.a // 1
f.b // 2
f.c // 3
再将F改成构造函数，就可以对它执行new命令了。
function* gen() {
this.a = 1;
yield this.b = 2;
yield this.c = 3;
}
function F() {
return gen.call(gen.prototype);
}
var f = new F();
f.next(); // Object {value: 2, done: false}
f.next(); // Object {value: 3, done: false}
f.next(); // Object {value: undefined, done: true}
f.a // 1
f.b // 2
f.c // 3
15.9 含义
15.9.1 Generator与状态机
Generator是实现状态机的最佳结构。比如，下面的clock函数就是一个状态机。
var ticking = true;
var clock = function() {
if (ticking)
console.log('Tick!');
else
console.log('Tock!');
ticking = !ticking;
}
上面代码的clock函数一共有两种状态（Tick和Tock），每运行一次，就改变一次状态。这个函数如果用Generator实现，就是下面这样。
var clock = function*() {
while (true) {
console.log('Tick!');
yield;
console.log('Tock!');
yield;
}
};
上面的Generator实现与ES5实现对比，可以看到少了用来保存状态的外部变量ticking，这样就更简洁，更安全（状态不会被非法篡改）、更符合函
数式编程的思想，在写法上也更优雅。Generator之所以可以不用外部变量保存状态，是因为它本身就包含了一个状态信息，即目前是否处于暂停态。
15.9.2 Generator与协程
协程（coroutine）是一种程序运行的方式，可以理解成“协作的线程”或“协作的函数”。协程既可以用单线程实现，也可以用多线程实现。前者是一种特
殊的子例程，后者是一种特殊的线程。
（1）协程与子例程的差异
传统的“子例程”（subroutine）采用堆栈式“后进先出”的执行方式，只有当调用的子函数完全执行完毕，才会结束执行父函数。协程与其不同，多个线
程（单线程情况下，即多个函数）可以并行执行，但是只有一个线程（或函数）处于正在运行的状态，其他线程（或函数）都处于暂停态
（suspended），线程（或函数）之间可以交换执行权。也就是说，一个线程（或函数）执行到一半，可以暂停执行，将执行权交给另一个线程（或
函数），等到稍后收回执行权的时候，再恢复执行。这种可以并行执行、交换执行权的线程（或函数），就称为协程。
从实现上看，在内存中，子例程只使用一个栈（stack），而协程是同时存在多个栈，但只有一个栈是在运行状态，也就是说，协程是以多占用内存为
代价，实现多任务的并行。
（2）协程与普通线程的差异
不难看出，协程适合用于多任务运行的环境。在这个意义上，它与普通的线程很相似，都有自己的执行上下文、可以分享全局变量。它们的不同之处
在于，同一时间可以有多个线程处于运行状态，但是运行的协程只能有一个，其他协程都处于暂停状态。此外，普通的线程是抢先式的，到底哪个线
程优先得到资源，必须由运行环境决定，但是协程是合作式的，执行权由协程自己分配。
由于ECMAScript是单线程语言，只能保持一个调用栈。引入协程以后，每个任务可以保持自己的调用栈。这样做的最大好处，就是抛出错误的时候，
可以找到原始的调用栈。不至于像异步操作的回调函数那样，一旦出错，原始的调用栈早就结束。
Generator函数是ECMAScript 6对协程的实现，但属于不完全实现。Generator函数被称为“半协程”（semi-coroutine），意思是只有Generator函数的
调用者，才能将程序的执行权还给Generator函数。如果是完全执行的协程，任何函数都可以让暂停的协程继续执行。
如果将Generator函数当作协程，完全可以将多个需要互相协作的任务写成Generator函数，它们之间使用yield语句交换控制权。
15.10 应用
Generator可以暂停函数执行，返回任意表达式的值。这种特点使得Generator有多种应用场景。
（1）异步操作的同步化表达
Generator函数的暂停执行的效果，意味着可以把异步操作写在yield语句里面，等到调用next方法时再往后执行。这实际上等同于不需要写回调函数
了，因为异步操作的后续操作可以放在yield语句下面，反正要等到调用next方法时再执行。所以，Generator函数的一个重要实际意义就是用来处理异
步操作，改写回调函数。
function* loadUI() {
showLoadingScreen();
yield loadUIDataAsynchronously();
hideLoadingScreen();
}
var loader = loadUI();
// 加载UI
loader.next()
// 卸载UI
loader.next()
上面代码表示，第一次调用loadUI函数时，该函数不会执行，仅返回一个遍历器。下一次对该遍历器调用next方法，则会显示Loading界面，并且异步
加载数据。等到数据加载完成，再一次使用next方法，则会隐藏Loading界面。可以看到，这种写法的好处是所有Loading界面的逻辑，都被封装在一
个函数，按部就班非常清晰。
Ajax是典型的异步操作，通过Generator函数部署Ajax操作，可以用同步的方式表达。
function* main() {
var result = yield request("http://some.url");
var resp = JSON.parse(result);
console.log(resp.value);
}
function request(url) {
makeAjaxCall(url, function(response){
it.next(response);
});
}
var it = main();
it.next();
上面代码的main函数，就是通过Ajax操作获取数据。可以看到，除了多了一个yield，它几乎与同步操作的写法完全一样。注意，makeAjaxCall函数中
的next方法，必须加上response参数，因为yield语句构成的表达式，本身是没有值的，总是等于undefined。
下面是另一个例子，通过Generator函数逐行读取文本文件。
function* numbers() {
let file = new FileReader("numbers.txt");
try {
while(!file.eof) {
yield parseInt(file.readLine(), 10);
}
} finally {
file.close();
}
}
上面代码打开文本文件，使用yield语句可以手动逐行读取文件。
（2）控制流管理
如果有一个多步操作非常耗时，采用回调函数，可能会写成下面这样。
step1(function (value1) {
step2(value1, function(value2) {
step3(value2, function(value3) {
step4(value3, function(value4) {
// Do something with value4
});
});
});
});
采用Promise改写上面的代码。
Promise.resolve(step1)
.then(step2)
.then(step3)
.then(step4)
.then(function (value4) {
// Do something with value4
}, function (error) {
// Handle any error from step1 through step4
})
.done();
上面代码已经把回调函数，改成了直线执行的形式，但是加入了大量Promise的语法。Generator函数可以进一步改善代码运行流程。
function* longRunningTask(value1) {
try {
var value2 = yield step1(value1);
var value3 = yield step2(value2);
var value4 = yield step3(value3);
var value5 = yield step4(value4);
// Do something with value4
} catch (e) {
// Handle any error from step1 through step4
}
}
然后，使用一个函数，按次序自动执行所有步骤。
scheduler(longRunningTask(initialValue));
function scheduler(task) {
var taskObj = task.next(task.value);
// 如果Generator函数未结束，就继续调用
if (!taskObj.done) {
task.value = taskObj.value
scheduler(task);
}
}
注意，上面这种做法，只适合同步操作，即所有的task都必须是同步的，不能有异步操作。因为这里的代码一得到返回值，就继续往下执行，没有判
断异步操作何时完成。如果要控制异步的操作流程，详见后面的《异步操作》一章。
下面，利用for...of循环会自动依次执行yield命令的特性，提供一种更一般的控制流管理的方法。
let steps = [step1Func, step2Func, step3Func];
function *iterateSteps(steps){
for (var i=0; i&lt; steps.length; i++){
var step = steps[i];
yield step();
}
}
上面代码中，数组steps封装了一个任务的多个步骤，Generator函数iterateSteps则是依次为这些步骤加上yield命令。
将任务分解成步骤之后，还可以将项目分解成多个依次执行的任务。
let jobs = [job1, job2, job3];
function *iterateJobs(jobs){
for (var i=0; i&lt; jobs.length; i++){
var job = jobs[i];
yield *iterateSteps(job.steps);
}
}
上面代码中，数组jobs封装了一个项目的多个任务，Generator函数iterateJobs则是依次为这些任务加上yield *命令。
最后，就可以用for...of循环一次性依次执行所有任务的所有步骤。
for (var step of iterateJobs(jobs)){
console.log(step.id);
}
再次提醒，上面的做法只能用于所有步骤都是同步操作的情况，不能有异步操作的步骤。如果想要依次执行异步的步骤，必须使用后面的《异步操
作》一章介绍的方法。
for...of的本质是一个while循环，所以上面的代码实质上执行的是下面的逻辑。
var it = iterateJobs(jobs);
var res = it.next();
while (!res.done){
var result = res.value;
// ...
res = it.next();
}
（3）部署Iterator接口
利用Generator函数，可以在任意对象上部署Iterator接口。
function* iterEntries(obj) {
let keys = Object.keys(obj);
for (let i=0; i &lt; keys.length; i++) {
let key = keys[i];
yield [key, obj[key]];
}
}
let myObj = { foo: 3, bar: 7 };
for (let [key, value] of iterEntries(myObj)) {
console.log(key, value);
}
// foo 3
// bar 7
上述代码中，myObj是一个普通对象，通过iterEntries函数，就有了Iterator接口。也就是说，可以在任意对象上部署next方法。
下面是一个对数组部署Iterator接口的例子，尽管数组原生具有这个接口。
function* makeSimpleGenerator(array){
var nextIndex = 0;
while(nextIndex &lt; array.length){
yield array[nextIndex++];
}
}
var gen = makeSimpleGenerator(['yo', 'ya']);
gen.next().value // 'yo'
gen.next().value // 'ya'
gen.next().done // true
（4）作为数据结构
Generator可以看作是数据结构，更确切地说，可以看作是一个数组结构，因为Generator函数可以返回一系列的值，这意味着它可以对任意表达式，
提供类似数组的接口。
function *doStuff() {
yield fs.readFile.bind(null, 'hello.txt');
yield fs.readFile.bind(null, 'world.txt');
yield fs.readFile.bind(null, 'and-such.txt');
}
上面代码就是依次返回三个函数，但是由于使用了Generator函数，导致可以像处理数组那样，处理这三个返回的函数。
for (task of doStuff()) {
// task是一个函数，可以像回调函数那样使用它
}
实际上，如果用ES5表达，完全可以用数组模拟Generator的这种用法。
function doStuff() {
return [
fs.readFile.bind(null, 'hello.txt'),
fs.readFile.bind(null, 'world.txt'),
fs.readFile.bind(null, 'and-such.txt')
];
}
上面的函数，可以用一模一样的for...of循环处理！两相一比较，就不难看出Generator使得数据或者操作，具备了类似数组的接口。
16 Promise对象
16.1 Promise的含义
Promise是异步编程的一种解决方案，比传统的解决方案——回调函数和事件——更合理和更强大。它由社区最早提出和实现，ES6将其写进了语言标
准，统一了用法，原生提供了Promise对象。
所谓Promise，简单说就是一个容器，里面保存着某个未来才会结束的事件（通常是一个异步操作）的结果。从语法上说，Promise是一个对象，从它
可以获取异步操作的消息。Promise提供统一的API，各种异步操作都可以用同样的方法进行处理。
Promise对象有以下两个特点。
（1）对象的状态不受外界影响。Promise对象代表一个异步操作，有三种状态：Pending（进行中）、Resolved（已完成，又称Fulfilled）
和Rejected（已失败）。只有异步操作的结果，可以决定当前是哪一种状态，任何其他操作都无法改变这个状态。这也是Promise这个名字的由来，它
的英语意思就是“承诺”，表示其他手段无法改变。
（2）一旦状态改变，就不会再变，任何时候都可以得到这个结果。Promise对象的状态改变，只有两种可能：从Pending变为Resolved和从Pending变
为Rejected。只要这两种情况发生，状态就凝固了，不会再变了，会一直保持这个结果。就算改变已经发生了，你再对Promise对象添加回调函数，也
会立即得到这个结果。这与事件（Event）完全不同，事件的特点是，如果你错过了它，再去监听，是得不到结果的。
有了Promise对象，就可以将异步操作以同步操作的流程表达出来，避免了层层嵌套的回调函数。此外，Promise对象提供统一的接口，使得控制异步
操作更加容易。
Promise也有一些缺点。首先，无法取消Promise，一旦新建它就会立即执行，无法中途取消。其次，如果不设置回调函数，Promise内部抛出的错误，
不会反应到外部。第三，当处于Pending状态时，无法得知目前进展到哪一个阶段（刚刚开始还是即将完成）。
如果某些事件不断地反复发生，一般来说，使用stream模式是比部署Promise更好的选择。
16.2 基本用法
ES6规定，Promise对象是一个构造函数，用来生成Promise实例。
下面代码创造了一个Promise实例。
var promise = new Promise(function(resolve, reject) {
// ... some code
if (/* 异步操作成功 */){
resolve(value);
} else {
reject(error);
}
});
Promise构造函数接受一个函数作为参数，该函数的两个参数分别是resolve和reject。它们是两个函数，由JavaScript引擎提供，不用自己部署。
resolve函数的作用是，将Promise对象的状态从“未完成”变为“成功”（即从Pending变为Resolved），在异步操作成功时调用，并将异步操作的结果，
作为参数传递出去；reject函数的作用是，将Promise对象的状态从“未完成”变为“失败”（即从Pending变为Rejected），在异步操作失败时调用，并将
异步操作报出的错误，作为参数传递出去。
Promise实例生成以后，可以用then方法分别指定Resolved状态和Reject状态的回调函数。
promise.then(function(value) {
// success
}, function(error) {
// failure
});
then方法可以接受两个回调函数作为参数。第一个回调函数是Promise对象的状态变为Resolved时调用，第二个回调函数是Promise对象的状态变为
Reject时调用。其中，第二个函数是可选的，不一定要提供。这两个函数都接受Promise对象传出的值作为参数。
下面是一个Promise对象的简单例子。
function timeout(ms) {
return new Promise((resolve, reject) =&gt; {
setTimeout(resolve, ms, 'done');
});
}
timeout(100).then((value) =&gt; {
console.log(value);
});
上面代码中，timeout方法返回一个Promise实例，表示一段时间以后才会发生的结果。过了指定的时间（ms参数）以后，Promise实例的状态变为
Resolved，就会触发then方法绑定的回调函数。
Promise新建后就会立即执行。
let promise = new Promise(function(resolve, reject) {
console.log('Promise');
resolve();
});
promise.then(function() {
console.log('Resolved.');
});
console.log('Hi!');
// Promise
// Hi!
// Resolved
上面代码中，Promise新建后立即执行，所以首先输出的是“Promise”。然后，then方法指定的回调函数，将在当前脚本所有同步任务执行完才会执
行，所以“Resolved”最后输出。
下面是异步加载图片的例子。
function loadImageAsync(url) {
return new Promise(function(resolve, reject) {
var image = new Image();
image.onload = function() {
resolve(image);
};
image.onerror = function() {
reject(new Error('Could not load image at ' + url));
};
image.src = url;
});
}
上面代码中，使用Promise包装了一个图片加载的异步操作。如果加载成功，就调用resolve方法，否则就调用reject方法。
下面是一个用Promise对象实现的Ajax操作的例子。
var getJSON = function(url) {
var promise = new Promise(function(resolve, reject){
var client = new XMLHttpRequest();
client.open("GET", url);
client.onreadystatechange = handler;
client.responseType = "json";
client.setRequestHeader("Accept", "application/json");
client.send();
function handler() {
if (this.readyState !== 4) {
return;
}
if (this.status === 200) {
resolve(this.response);
} else {
reject(new Error(this.statusText));
}
};
});
return promise;
};
getJSON("/posts.json").then(function(json) {
console.log('Contents: ' + json);
}, function(error) {
console.error('出错了', error);
});
上面代码中，getJSON是对XMLHttpRequest对象的封装，用于发出一个针对JSON数据的HTTP请求，并且返回一个Promise对象。需要注意的是，
在getJSON内部，resolve函数和reject函数调用时，都带有参数。
如果调用resolve函数和reject函数时带有参数，那么它们的参数会被传递给回调函数。reject函数的参数通常是Error对象的实例，表示抛出的错
误；resolve函数的参数除了正常的值以外，还可能是另一个Promise实例，表示异步操作的结果有可能是一个值，也有可能是另一个异步操作，比如
像下面这样。
var p1 = new Promise(function (resolve, reject) {
// ...
});
var p2 = new Promise(function (resolve, reject) {
// ...
resolve(p1);
})
上面代码中，p1和p2都是Promise的实例，但是p2的resolve方法将p1作为参数，即一个异步操作的结果是返回另一个异步操作。
注意，这时p1的状态就会传递给p2，也就是说，p1的状态决定了p2的状态。如果p1的状态是Pending，那么p2的回调函数就会等待p1的状态改变；如
果p1的状态已经是Resolved或者Rejected，那么p2的回调函数将会立刻执行。
var p1 = new Promise(function (resolve, reject) {
setTimeout(() =&gt; reject(new Error('fail')), 3000)
})
var p2 = new Promise(function (resolve, reject) {
setTimeout(() =&gt; resolve(p1), 1000)
})
p2
.then(result =&gt; console.log(result))
.catch(error =&gt; console.log(error))
// Error: fail
上面代码中，p1是一个Promise，3秒之后变为rejected。p2的状态在1秒之后改变，resolve方法返回的是p1。此时，由于p2返回的是另一个
Promise，所以后面的then语句都变成针对后者（p1）。又过了2秒，p1变为rejected，导致触发catch方法指定的回调函数。
16.3 Promise.prototype.then()
Promise实例具有then方法，也就是说，then方法是定义在原型对象Promise.prototype上的。它的作用是为Promise实例添加状态改变时的回调函数。
前面说过，then方法的第一个参数是Resolved状态的回调函数，第二个参数（可选）是Rejected状态的回调函数。
then方法返回的是一个新的Promise实例（注意，不是原来那个Promise实例）。因此可以采用链式写法，即then方法后面再调用另一个then方法。
getJSON("/posts.json").then(function(json) {
return json.post;
}).then(function(post) {
// ...
});
上面的代码使用then方法，依次指定了两个回调函数。第一个回调函数完成以后，会将返回结果作为参数，传入第二个回调函数。
采用链式的then，可以指定一组按照次序调用的回调函数。这时，前一个回调函数，有可能返回的还是一个Promise对象（即有异步操作），这时后一
个回调函数，就会等待该Promise对象的状态发生变化，才会被调用。
getJSON("/post/1.json").then(function(post) {
return getJSON(post.commentURL);
}).then(function funcA(comments) {
console.log("Resolved: ", comments);
}, function funcB(err){
console.log("Rejected: ", err);
});
上面代码中，第一个then方法指定的回调函数，返回的是另一个Promise对象。这时，第二个then方法指定的回调函数，就会等待这个新的Promise对
象状态发生变化。如果变为Resolved，就调用funcA，如果状态变为Rejected，就调用funcB。
如果采用箭头函数，上面的代码可以写得更简洁。
getJSON("/post/1.json").then(
post =&gt; getJSON(post.commentURL)
).then(
comments =&gt; console.log("Resolved: ", comments),
err =&gt; console.log("Rejected: ", err)
);
16.4 Promise.prototype.catch()
Promise.prototype.catch方法是.then(null, rejection)的别名，用于指定发生错误时的回调函数。
getJSON("/posts.json").then(function(posts) {
// ...
}).catch(function(error) {
// 处理 getJSON 和 前一个回调函数运行时发生的错误
console.log('发生错误！', error);
});
上面代码中，getJSON方法返回一个Promise对象，如果该对象状态变为Resolved，则会调用then方法指定的回调函数；如果异步操作抛出错误，状态
就会变为Rejected，就会调用catch方法指定的回调函数，处理这个错误。另外，then方法指定的回调函数，如果运行中抛出错误，也会被catch方法
捕获。
p.then((val) =&gt; console.log("fulfilled:", val))
.catch((err) =&gt; console.log("rejected:", err));
// 等同于
p.then((val) =&gt; console.log("fulfilled:", val))
.then(null, (err) =&gt; console.log("rejected:", err));
下面是一个例子。
var promise = new Promise(function(resolve, reject) {
throw new Error('test');
});
promise.catch(function(error) {
console.log(error);
});
// Error: test
上面代码中，promise抛出一个错误，就被catch方法指定的回调函数捕获。注意，上面的写法与下面两种写法是等价的。
// 写法一
var promise = new Promise(function(resolve, reject) {
try {
throw new Error('test');
} catch(e) {
reject(e);
}
});
promise.catch(function(error) {
console.log(error);
});
// 写法二
var promise = new Promise(function(resolve, reject) {
reject(new Error('test'));
});
promise.catch(function(error) {
console.log(error);
});
比较上面两种写法，可以发现reject方法的作用，等同于抛出错误。
如果Promise状态已经变成Resolved，再抛出错误是无效的。
var promise = new Promise(function(resolve, reject) {
resolve('ok');
throw new Error('test');
});
promise
.then(function(value) { console.log(value) })
.catch(function(error) { console.log(error) });
// ok
上面代码中，Promise在resolve语句后面，再抛出错误，不会被捕获，等于没有抛出。
Promise对象的错误具有“冒泡”性质，会一直向后传递，直到被捕获为止。也就是说，错误总是会被下一个catch语句捕获。
getJSON("/post/1.json").then(function(post) {
return getJSON(post.commentURL);
}).then(function(comments) {
// some code
}).catch(function(error) {
// 处理前面三个Promise产生的错误
});
上面代码中，一共有三个Promise对象：一个由getJSON产生，两个由then产生。它们之中任何一个抛出的错误，都会被最后一个catch捕获。
一般来说，不要在then方法里面定义Reject状态的回调函数（即then的第二个参数），总是使用catch方法。
// bad
promise
.then(function(data) {
// success
}, function(err) {
// error
});
// good
promise
.then(function(data) { //cb
// success
})
.catch(function(err) {
// error
});
上面代码中，第二种写法要好于第一种写法，理由是第二种写法可以捕获前面then方法执行中的错误，也更接近同步的写法（try/catch）。因此，建
议总是使用catch方法，而不使用then方法的第二个参数。
跟传统的try/catch代码块不同的是，如果没有使用catch方法指定错误处理的回调函数，Promise对象抛出的错误不会传递到外层代码，即不会有任何
反应。
var someAsyncThing = function() {
return new Promise(function(resolve, reject) {
// 下面一行会报错，因为x没有声明
resolve(x + 2);
});
};
someAsyncThing().then(function() {
console.log('everything is great');
});
上面代码中，someAsyncThing函数产生的Promise对象会报错，但是由于没有指定catch方法，这个错误不会被捕获，也不会传递到外层代码，导致运
行后没有任何输出。注意，Chrome浏览器不遵守这条规定，它会抛出错误“ReferenceError: x is not defined”。
var promise = new Promise(function(resolve, reject) {
resolve("ok");
setTimeout(function() { throw new Error('test') }, 0)
});
promise.then(function(value) { console.log(value) });
// ok
// Uncaught Error: test
上面代码中，Promise指定在下一轮“事件循环”再抛出错误，结果由于没有指定使用try...catch语句，就冒泡到最外层，成了未捕获的错误。因为此
时，Promise的函数体已经运行结束了，所以这个错误是在Promise函数体外抛出的。
Node.js有一个unhandledRejection事件，专门监听未捕获的reject错误。
process.on('unhandledRejection', function (err, p) {
console.error(err.stack)
});
上面代码中，unhandledRejection事件的监听函数有两个参数，第一个是错误对象，第二个是报错的Promise实例，它可以用来了解发生错误的环境信
息。。
需要注意的是，catch方法返回的还是一个Promise对象，因此后面还可以接着调用then方法。
var someAsyncThing = function() {
return new Promise(function(resolve, reject) {
// 下面一行会报错，因为x没有声明
resolve(x + 2);
});
};
someAsyncThing()
.catch(function(error) {
console.log('oh no', error);
})
.then(function() {
console.log('carry on');
});
// oh no [ReferenceError: x is not defined]
// carry on
上面代码运行完catch方法指定的回调函数，会接着运行后面那个then方法指定的回调函数。如果没有报错，则会跳过catch方法。
Promise.resolve()
.catch(function(error) {
console.log('oh no', error);
})
.then(function() {
console.log('carry on');
});
// carry on
上面的代码因为没有报错，跳过了catch方法，直接执行后面的then方法。此时，要是then方法里面报错，就与前面的catch无关了。
catch方法之中，还能再抛出错误。
var someAsyncThing = function() {
return new Promise(function(resolve, reject) {
// 下面一行会报错，因为x没有声明
resolve(x + 2);
});
};
someAsyncThing().then(function() {
return someOtherAsyncThing();
}).catch(function(error) {
console.log('oh no', error);
// 下面一行会报错，因为y没有声明
y + 2;
}).then(function() {
console.log('carry on');
});
// oh no [ReferenceError: x is not defined]
上面代码中，catch方法抛出一个错误，因为后面没有别的catch方法了，导致这个错误不会被捕获，也不会传递到外层。如果改写一下，结果就不一
样了。
someAsyncThing().then(function() {
return someOtherAsyncThing();
}).catch(function(error) {
console.log('oh no', error);
// 下面一行会报错，因为y没有声明
y + 2;
}).catch(function(error) {
console.log('carry on', error);
});
// oh no [ReferenceError: x is not defined]
// carry on [ReferenceError: y is not defined]
上面代码中，第二个catch方法用来捕获，前一个catch方法抛出的错误。
16.5 Promise.all()
Promise.all方法用于将多个Promise实例，包装成一个新的Promise实例。
var p = Promise.all([p1, p2, p3]);
上面代码中，Promise.all方法接受一个数组作为参数，p1、p2、p3都是Promise对象的实例，如果不是，就会先调用下面讲到的Promise.resolve方
法，将参数转为Promise实例，再进一步处理。（Promise.all方法的参数可以不是数组，但必须具有Iterator接口，且返回的每个成员都是Promise实
例。）
p的状态由p1、p2、p3决定，分成两种情况。
（1）只有p1、p2、p3的状态都变成fulfilled，p的状态才会变成fulfilled，此时p1、p2、p3的返回值组成一个数组，传递给p的回调函数。
（2）只要p1、p2、p3之中有一个被rejected，p的状态就变成rejected，此时第一个被reject的实例的返回值，会传递给p的回调函数。
下面是一个具体的例子。
// 生成一个Promise对象的数组
var promises = [2, 3, 5, 7, 11, 13].map(function (id) {
return getJSON("/post/" + id + ".json");
});
Promise.all(promises).then(function (posts) {
// ...
}).catch(function(reason){
// ...
});
上面代码中，promises是包含6个Promise实例的数组，只有这6个实例的状态都变成fulfilled，或者其中有一个变为rejected，才会调
用Promise.all方法后面的回调函数。
下面是另一个例子。
const databasePromise = connectDatabase();
const booksPromise = databaseProimse
.then(findAllBooks);
const userPromise = databasePromise
.then(getCurrentUser);
Promise.all([
booksPromise,
userPromise
])
.then(([books, user]) =&gt; pickTopRecommentations(books, user));
上面代码中，booksPromise和userPromise是两个异步操作，只有等到它们的结果都返回了，才会触发pickTopRecommentations这个回调函数。
16.6 Promise.race()
Promise.race方法同样是将多个Promise实例，包装成一个新的Promise实例。
var p = Promise.race([p1,p2,p3]);
上面代码中，只要p1、p2、p3之中有一个实例率先改变状态，p的状态就跟着改变。那个率先改变的Promise实例的返回值，就传递给p的回调函数。
Promise.race方法的参数与Promise.all方法一样，如果不是Promise实例，就会先调用下面讲到的Promise.resolve方法，将参数转为Promise实例，
再进一步处理。
下面是一个例子，如果指定时间内没有获得结果，就将Promise的状态变为reject，否则变为resolve。
var p = Promise.race([
fetch('/resource-that-may-take-a-while'),
new Promise(function (resolve, reject) {
setTimeout(() =&gt; reject(new Error('request timeout')), 5000)
})
])
p.then(response =&gt; console.log(response))
p.catch(error =&gt; console.log(error))
上面代码中，如果5秒之内fetch方法无法返回结果，变量p的状态就会变为rejected，从而触发catch方法指定的回调函数。
16.7 Promise.resolve()
有时需要将现有对象转为Promise对象，Promise.resolve方法就起到这个作用。
var jsPromise = Promise.resolve($.ajax('/whatever.json'));
上面代码将jQuery生成的deferred对象，转为一个新的Promise对象。
Promise.resolve等价于下面的写法。
Promise.resolve('foo')
// 等价于
new Promise(resolve =&gt; resolve('foo'))
Promise.resolve方法的参数分成四种情况。
（1）参数是一个Promise实例
如果参数是Promise实例，那么Promise.resolve将不做任何修改、原封不动地返回这个实例。
（2）参数是一个 thenable对象
thenable对象指的是具有then方法的对象，比如下面这个对象。
let thenable = {
then: function(resolve, reject) {
resolve(42);
}
};
Promise.resolve方法会将这个对象转为Promise对象，然后就立即执行thenable对象的then方法。
let thenable = {
then: function(resolve, reject) {
resolve(42);
}
};
let p1 = Promise.resolve(thenable);
p1.then(function(value) {
console.log(value); // 42
});
上面代码中，thenable对象的then方法执行后，对象p1的状态就变为resolved，从而立即执行最后那个then方法指定的回调函数，输出42。
（3）参数不是具有 then方法的对象，或根本就不是对象
如果参数是一个原始值，或者是一个不具有then方法的对象，则Promise.resolve方法返回一个新的Promise对象，状态为Resolved。
var p = Promise.resolve('Hello');
p.then(function (s){
console.log(s)
});
// Hello
上面代码生成一个新的Promise对象的实例p。由于字符串Hello不属于异步操作（判断方法是它不是具有then方法的对象），返回Promise实例的状态
从一生成就是Resolved，所以回调函数会立即执行。Promise.resolve方法的参数，会同时传给回调函数。
（4）不带有任何参数
Promise.resolve方法允许调用时不带参数，直接返回一个Resolved状态的Promise对象。
所以，如果希望得到一个Promise对象，比较方便的方法就是直接调用Promise.resolve方法。
var p = Promise.resolve();
p.then(function () {
// ...
});
上面代码的变量p就是一个Promise对象。
需要注意的是，立即resolve的Promise对象，是在本轮“事件循环”（event loop）的结束时，而不是在下一轮“事件循环”的开始时。
setTimeout(function () {
console.log('three');
}, 0);
Promise.resolve().then(function () {
console.log('two');
});
console.log('one');
// one
// two
// three
上面代码中，setTimeout(fn, 0)在下一轮“事件循环”开始时执行，Promise.resolve()在本轮“事件循环”结束时执行，console.log(’one‘)则是立即执
行，因此最先输出。
16.8 Promise.reject()
Promise.reject(reason)方法也会返回一个新的Promise实例，该实例的状态为rejected。它的参数用法与Promise.resolve方法完全一致。
var p = Promise.reject('出错了');
// 等同于
var p = new Promise((resolve, reject) =&gt; reject('出错了'))
p.then(null, function (s){
console.log(s)
});
// 出错了
上面代码生成一个Promise对象的实例p，状态为rejected，回调函数会立即执行。
16.9 两个有用的附加方法
ES6的Promise API提供的方法不是很多，有些有用的方法可以自己部署。下面介绍如何部署两个不在ES6之中、但很有用的方法。
16.9.1 done()
Promise对象的回调链，不管以then方法或catch方法结尾，要是最后一个方法抛出错误，都有可能无法捕捉到（因为Promise内部的错误不会冒泡到
全局）。因此，我们可以提供一个done方法，总是处于回调链的尾端，保证抛出任何可能出现的错误。
asyncFunc()
.then(f1)
.catch(r1)
.then(f2)
.done();
它的实现代码相当简单。
Promise.prototype.done = function (onFulfilled, onRejected) {
this.then(onFulfilled, onRejected)
.catch(function (reason) {
// 抛出一个全局错误
setTimeout(() =&gt; { throw reason }, 0);
});
};
从上面代码可见，done方法的使用，可以像then方法那样用，提供Fulfilled和Rejected状态的回调函数，也可以不提供任何参数。但不管怎
样，done都会捕捉到任何可能出现的错误，并向全局抛出。
16.9.2 finally()
finally方法用于指定不管Promise对象最后状态如何，都会执行的操作。它与done方法的最大区别，它接受一个普通的回调函数作为参数，该函数不
管怎样都必须执行。
下面是一个例子，服务器使用Promise处理请求，然后使用finally方法关掉服务器。
server.listen(0)
.then(function () {
// run test
})
.finally(server.stop);
它的实现也很简单。
Promise.prototype.finally = function (callback) {
let P = this.constructor;
return this.then(
value =&gt; P.resolve(callback()).then(() =&gt; value),
reason =&gt; P.resolve(callback()).then(() =&gt; { throw reason })
);
};
上面代码中，不管前面的Promise是fulfilled还是rejected，都会执行回调函数callback。
16.10 应用
16.10.1 加载图片
我们可以将图片的加载写成一个Promise，一旦加载完成，Promise的状态就发生变化。
const preloadImage = function (path) {
return new Promise(function (resolve, reject) {
var image = new Image();
image.onload = resolve;
image.onerror = reject;
image.src = path;
});
};
16.10.2 Generator函数与Promise的结合
使用Generator函数管理流程，遇到异步操作的时候，通常返回一个Promise对象。
function getFoo () {
return new Promise(function (resolve, reject){
resolve('foo');
});
}
var g = function* () {
try {
var foo = yield getFoo();
console.log(foo);
} catch (e) {
console.log(e);
}
};
function run (generator) {
var it = generator();
function go(result) {
if (result.done) return result.value;
return result.value.then(function (value) {
return go(it.next(value));
}, function (error) {
return go(it.throw(error));
});
}
go(it.next());
}
run(g);
上面代码的Generator函数g之中，有一个异步操作getFoo，它返回的就是一个Promise对象。函数run用来处理这个Promise对象，并调用下一
个next方法。
17 异步操作和Async函数
异步编程对JavaScript语言太重要。Javascript语言的执行环境是“单线程”的，如果没有异步编程，根本没法用，非卡死不可。
ES6诞生以前，异步编程的方法，大概有下面四种。
回调函数
事件监听
发布/订阅
Promise 对象
ES6将JavaScript异步编程带入了一个全新的阶段，ES7的Async函数更是提出了异步编程的终极解决方案。
17.1 基本概念
17.1.1 异步
所谓"异步"，简单说就是一个任务分成两段，先执行第一段，然后转而执行其他任务，等做好了准备，再回过头执行第二段。
比如，有一个任务是读取文件进行处理，任务的第一段是向操作系统发出请求，要求读取文件。然后，程序执行其他任务，等到操作系统返回文件，
再接着执行任务的第二段（处理文件）。这种不连续的执行，就叫做异步。
相应地，连续的执行就叫做同步。由于是连续执行，不能插入其他任务，所以操作系统从硬盘读取文件的这段时间，程序只能干等着。
17.1.2 回调函数
JavaScript语言对异步编程的实现，就是回调函数。所谓回调函数，就是把任务的第二段单独写在一个函数里面，等到重新执行这个任务的时候，就直
接调用这个函数。它的英语名字callback，直译过来就是"重新调用"。
读取文件进行处理，是这样写的。
fs.readFile('/etc/passwd', function (err, data) {
if (err) throw err;
console.log(data);
});
上面代码中，readFile函数的第二个参数，就是回调函数，也就是任务的第二段。等到操作系统返回了/etc/passwd这个文件以后，回调函数才会执
行。
一个有趣的问题是，为什么Node.js约定，回调函数的第一个参数，必须是错误对象err（如果没有错误，该参数就是null）？原因是执行分成两段，在
这两段之间抛出的错误，程序无法捕捉，只能当作参数，传入第二段。
17.1.3 Promise
回调函数本身并没有问题，它的问题出现在多个回调函数嵌套。假定读取A文件之后，再读取B文件，代码如下。
fs.readFile(fileA, function (err, data) {
fs.readFile(fileB, function (err, data) {
// ...
});
});
不难想象，如果依次读取多个文件，就会出现多重嵌套。代码不是纵向发展，而是横向发展，很快就会乱成一团，无法管理。这种情况就称为"回调函
数噩梦"（callback hell）。
Promise就是为了解决这个问题而提出的。它不是新的语法功能，而是一种新的写法，允许将回调函数的嵌套，改成链式调用。采用Promise，连续读
取多个文件，写法如下。
var readFile = require('fs-readfile-promise');
readFile(fileA)
.then(function(data){
console.log(data.toString());
})
.then(function(){
return readFile(fileB);
})
.then(function(data){
console.log(data.toString());
})
.catch(function(err) {
console.log(err);
});
上面代码中，我使用了fs-readfile-promise模块，它的作用就是返回一个Promise版本的readFile函数。Promise提供then方法加载回调函数，catch方法
捕捉执行过程中抛出的错误。
可以看到，Promise 的写法只是回调函数的改进，使用then方法以后，异步任务的两段执行看得更清楚了，除此以外，并无新意。
Promise 的最大问题是代码冗余，原来的任务被Promise 包装了一下，不管什么操作，一眼看去都是一堆 then，原来的语义变得很不清楚。
那么，有没有更好的写法呢？
17.2 Generator函数
17.2.1 协程
传统的编程语言，早有异步编程的解决方案（其实是多任务的解决方案）。其中有一种叫做"协程"（coroutine），意思是多个线程互相协作，完成异步
任务。
协程有点像函数，又有点像线程。它的运行流程大致如下。
第一步，协程A开始执行。
第二步，协程A执行到一半，进入暂停，执行权转移到协程B。
第三步，（一段时间后）协程B交还执行权。
第四步，协程A恢复执行。
上面流程的协程A，就是异步任务，因为它分成两段（或多段）执行。
举例来说，读取文件的协程写法如下。
function *asyncJob() {
// ...其他代码
var f = yield readFile(fileA);
// ...其他代码
}
上面代码的函数asyncJob是一个协程，它的奥妙就在其中的yield命令。它表示执行到此处，执行权将交给其他协程。也就是说，yield命令是异步两
个阶段的分界线。
协程遇到yield命令就暂停，等到执行权返回，再从暂停的地方继续往后执行。它的最大优点，就是代码的写法非常像同步操作，如果去除yield命令，
简直一模一样。
17.2.3 Generator函数的概念
Generator函数是协程在ES6的实现，最大特点就是可以交出函数的执行权（即暂停执行）。
整个Generator函数就是一个封装的异步任务，或者说是异步任务的容器。异步操作需要暂停的地方，都用yield语句注明。Generator函数的执行方法
如下。
function* gen(x){
var y = yield x + 2;
return y;
}
var g = gen(1);
g.next() // { value: 3, done: false }
g.next() // { value: undefined, done: true }
上面代码中，调用Generator函数，会返回一个内部指针（即遍历器）g 。这是Generator函数不同于普通函数的另一个地方，即执行它不会返回结
果，返回的是指针对象。调用指针g的next方法，会移动内部指针（即执行异步任务的第一段），指向第一个遇到的yield语句，上例是执行到x + 2为
止。
换言之，next方法的作用是分阶段执行Generator函数。每次调用next方法，会返回一个对象，表示当前阶段的信息（value属性和done属性）。value
属性是yield语句后面表达式的值，表示当前阶段的值；done属性是一个布尔值，表示Generator函数是否执行完毕，即是否还有下一个阶段。
17.2.4 Generator函数的数据交换和错误处理
Generator函数可以暂停执行和恢复执行，这是它能封装异步任务的根本原因。除此之外，它还有两个特性，使它可以作为异步编程的完整解决方案：
函数体内外的数据交换和错误处理机制。
next方法返回值的value属性，是Generator函数向外输出数据；next方法还可以接受参数，这是向Generator函数体内输入数据。
function* gen(x){
var y = yield x + 2;
return y;
}
var g = gen(1);
g.next() // { value: 3, done: false }
g.next(2) // { value: 2, done: true }
上面代码中，第一个next方法的value属性，返回表达式x + 2的值（3）。第二个next方法带有参数2，这个参数可以传入 Generator 函数，作为上个
阶段异步任务的返回结果，被函数体内的变量y接收。因此，这一步的 value 属性，返回的就是2（变量y的值）。
Generator 函数内部还可以部署错误处理代码，捕获函数体外抛出的错误。
function* gen(x){
try {
var y = yield x + 2;
} catch (e){
console.log(e);
}
return y;
}
var g = gen(1);
g.next();
g.throw('出错了');
// 出错了
上面代码的最后一行，Generator函数体外，使用指针对象的throw方法抛出的错误，可以被函数体内的try ...catch代码块捕获。这意味着，出错的代码
与处理错误的代码，实现了时间和空间上的分离，这对于异步编程无疑是很重要的。
17.2.5异步任务的封装
下面看看如何使用 Generator 函数，执行一个真实的异步任务。
var fetch = require('node-fetch');
function* gen(){
var url = 'https://api.github.com/users/github';
var result = yield fetch(url);
console.log(result.bio);
}
上面代码中，Generator函数封装了一个异步操作，该操作先读取一个远程接口，然后从JSON格式的数据解析信息。就像前面说过的，这段代码非常
像同步操作，除了加上了yield命令。
执行这段代码的方法如下。
var g = gen();
var result = g.next();
result.value.then(function(data){
return data.json();
}).then(function(data){
g.next(data);
});
上面代码中，首先执行Generator函数，获取遍历器对象，然后使用next 方法（第二行），执行异步任务的第一阶段。由于Fetch模块返回的是一个
Promise对象，因此要用then方法调用下一个next 方法。
可以看到，虽然 Generator 函数将异步操作表示得很简洁，但是流程管理却不方便（即何时执行第一阶段、何时执行第二阶段）。
17.3 Thunk函数
17.3.1 参数的求值策略
Thunk函数早在上个世纪60年代就诞生了。
那时，编程语言刚刚起步，计算机学家还在研究，编译器怎么写比较好。一个争论的焦点是"求值策略"，即函数的参数到底应该何时求值。
var x = 1;
function f(m){
return m * 2;
}
f(x + 5)
上面代码先定义函数f，然后向它传入表达式x + 5。请问，这个表达式应该何时求值？
一种意见是"传值调用"（call by value），即在进入函数体之前，就计算x + 5的值（等于6），再将这个值传入函数f 。C语言就采用这种策略。
f(x + 5)
// 传值调用时，等同于
f(6)
另一种意见是"传名调用"（call by name），即直接将表达式x + 5传入函数体，只在用到它的时候求值。Haskell语言采用这种策略。
f(x + 5)
// 传名调用时，等同于
(x + 5) * 2
传值调用和传名调用，哪一种比较好？回答是各有利弊。传值调用比较简单，但是对参数求值的时候，实际上还没用到这个参数，有可能造成性能损
失。
function f(a, b){
return b;
}
f(3 * x * x - 2 * x - 1, x);
上面代码中，函数f的第一个参数是一个复杂的表达式，但是函数体内根本没用到。对这个参数求值，实际上是不必要的。因此，有一些计算机学家倾
向于"传名调用"，即只在执行时求值。
17.3.2 Thunk函数的含义
编译器的"传名调用"实现，往往是将参数放到一个临时函数之中，再将这个临时函数传入函数体。这个临时函数就叫做Thunk函数。
function f(m){
return m * 2;
}
f(x + 5);
// 等同于
var thunk = function () {
return x + 5;
};
function f(thunk){
return thunk() * 2;
}
上面代码中，函数f的参数x + 5被一个函数替换了。凡是用到原参数的地方，对Thunk函数求值即可。
这就是Thunk函数的定义，它是"传名调用"的一种实现策略，用来替换某个表达式。
17.3.3 JavaScript语言的Thunk函数
JavaScript语言是传值调用，它的Thunk函数含义有所不同。在JavaScript语言中，Thunk函数替换的不是表达式，而是多参数函数，将其替换成单参
数的版本，且只接受回调函数作为参数。
// 正常版本的readFile（多参数版本）
fs.readFile(fileName, callback);
// Thunk版本的readFile（单参数版本）
var readFileThunk = Thunk(fileName);
readFileThunk(callback);
var Thunk = function (fileName){
return function (callback){
return fs.readFile(fileName, callback);
};
};
上面代码中，fs模块的readFile方法是一个多参数函数，两个参数分别为文件名和回调函数。经过转换器处理，它变成了一个单参数函数，只接受回调
函数作为参数。这个单参数版本，就叫做Thunk函数。
任何函数，只要参数有回调函数，就能写成Thunk函数的形式。下面是一个简单的Thunk函数转换器。
// ES5版本
var Thunk = function(fn){
return function (){
var args = Array.prototype.slice.call(arguments);
return function (callback){
args.push(callback);
return fn.apply(this, args);
}
};
};
// ES6版本
var Thunk = function(fn) {
return function (...args) {
return function (callback) {
return fn.call(this, ...args, callback);
}
};
};
使用上面的转换器，生成fs.readFile的Thunk函数。
var readFileThunk = Thunk(fs.readFile);
readFileThunk(fileA)(callback);
下面是另一个完整的例子。
function f(a, cb) {
cb(a);
}
let ft = Thunk(f);
let log = console.log.bind(console);
ft(1)(log) // 1
17.3.4 Thunkify模块
生产环境的转换器，建议使用Thunkify模块。
首先是安装。
$ npm install thunkify
使用方式如下。
var thunkify = require('thunkify');
var fs = require('fs');
var read = thunkify(fs.readFile);
read('package.json')(function(err, str){
// ...
});
Thunkify的源码与上一节那个简单的转换器非常像。
function thunkify(fn){
return function(){
var args = new Array(arguments.length);
var ctx = this;
for(var i = 0; i &lt; args.length; ++i) {
args[i] = arguments[i];
}
return function(done){
var called;
args.push(function(){
if (called) return;
called = true;
done.apply(null, arguments);
});
try {
fn.apply(ctx, args);
} catch (err) {
done(err);
}
}
}
};
它的源码主要多了一个检查机制，变量called确保回调函数只运行一次。这样的设计与下文的Generator函数相关。请看下面的例子。
function f(a, b, callback){
var sum = a + b;
callback(sum);
callback(sum);
}
var ft = thunkify(f);
var print = console.log.bind(console);
ft(1, 2)(print);
// 3
上面代码中，由于thunkify只允许回调函数执行一次，所以只输出一行结果。
17.3.5 Generator 函数的流程管理
你可能会问， Thunk函数有什么用？回答是以前确实没什么用，但是ES6有了Generator函数，Thunk函数现在可以用于Generator函数的自动流程管
理。
Generator函数可以自动执行。
function* gen() {
// ...
}
var g = gen();
var res = g.next();
while(!res.done){
console.log(res.value);
res = g.next();
}
上面代码中，Generator函数gen会自动执行完所有步骤。
但是，这不适合异步操作。如果必须保证前一步执行完，才能执行后一步，上面的自动执行就不可行。这时，Thunk函数就能派上用处。以读取文件为
例。下面的Generator函数封装了两个异步操作。
var fs = require('fs');
var thunkify = require('thunkify');
var readFile = thunkify(fs.readFile);
var gen = function* (){
var r1 = yield readFile('/etc/fstab');
console.log(r1.toString());
var r2 = yield readFile('/etc/shells');
console.log(r2.toString());
};
上面代码中，yield命令用于将程序的执行权移出Generator函数，那么就需要一种方法，将执行权再交还给Generator函数。
这种方法就是Thunk函数，因为它可以在回调函数里，将执行权交还给Generator函数。为了便于理解，我们先看如何手动执行上面这个Generator函
数。
var g = gen();
var r1 = g.next();
r1.value(function(err, data){
if (err) throw err;
var r2 = g.next(data);
r2.value(function(err, data){
if (err) throw err;
g.next(data);
});
});
上面代码中，变量g是Generator函数的内部指针，表示目前执行到哪一步。next方法负责将指针移动到下一步，并返回该步的信息（value属性和done
属性）。
仔细查看上面的代码，可以发现Generator函数的执行过程，其实是将同一个回调函数，反复传入next方法的value属性。这使得我们可以用递归来自动
完成这个过程。
17.3.6 Thunk函数的自动流程管理
Thunk函数真正的威力，在于可以自动执行Generator函数。下面就是一个基于Thunk函数的Generator执行器。
function run(fn) {
var gen = fn();
function next(err, data) {
var result = gen.next(data);
if (result.done) return;
result.value(next);
}
next();
}
function* g() {
// ...
}
run(g);
上面代码的run函数，就是一个Generator函数的自动执行器。内部的next函数就是Thunk的回调函数。next函数先将指针移到Generator函数的下一
步（gen.next方法），然后判断Generator函数是否结束（result.done属性），如果没结束，就将next函数再传入Thunk函数（result.value属
性），否则就直接退出。
有了这个执行器，执行Generator函数方便多了。不管内部有多少个异步操作，直接把Generator函数传入run函数即可。当然，前提是每一个异步操
作，都要是Thunk函数，也就是说，跟在yield命令后面的必须是Thunk函数。
var g = function* (){
var f1 = yield readFile('fileA');
var f2 = yield readFile('fileB');
// ...
var fn = yield readFile('fileN');
};
run(g);
上面代码中，函数g封装了n个异步的读取文件操作，只要执行run函数，这些操作就会自动完成。这样一来，异步操作不仅可以写得像同步操作，而且
一行代码就可以执行。
Thunk函数并不是Generator函数自动执行的唯一方案。因为自动执行的关键是，必须有一种机制，自动控制Generator函数的流程，接收和交还程序
的执行权。回调函数可以做到这一点，Promise 对象也可以做到这一点。
17.4 co模块
17.4.1 基本用法
co模块是著名程序员TJ Holowaychuk于2013年6月发布的一个小工具，用于Generator函数的自动执行。
比如，有一个Generator函数，用于依次读取两个文件。
var gen = function* (){
var f1 = yield readFile('/etc/fstab');
var f2 = yield readFile('/etc/shells');
console.log(f1.toString());
console.log(f2.toString());
};
co模块可以让你不用编写Generator函数的执行器。
var co = require('co');
co(gen);
上面代码中，Generator函数只要传入co函数，就会自动执行。
co函数返回一个Promise对象，因此可以用then方法添加回调函数。
co(gen).then(function (){
console.log('Generator 函数执行完成');
});
上面代码中，等到Generator函数执行结束，就会输出一行提示。
17.4.2 co模块的原理
为什么co可以自动执行Generator函数？
前面说过，Generator就是一个异步操作的容器。它的自动执行需要一种机制，当异步操作有了结果，能够自动交回执行权。
两种方法可以做到这一点。
（1）回调函数。将异步操作包装成Thunk函数，在回调函数里面交回执行权。
（2）Promise 对象。将异步操作包装成Promise对象，用then方法交回执行权。
co模块其实就是将两种自动执行器（Thunk函数和Promise对象），包装成一个模块。使用co的前提条件是，Generator函数的yield命令后面，只能是
Thunk函数或Promise对象。
上一节已经介绍了基于Thunk函数的自动执行器。下面来看，基于Promise对象的自动执行器。这是理解co模块必须的。
17.4.3 基于Promise对象的自动执行
还是沿用上面的例子。首先，把fs模块的readFile方法包装成一个Promise对象。
var fs = require('fs');
var readFile = function (fileName){
return new Promise(function (resolve, reject){
fs.readFile(fileName, function(error, data){
if (error) return reject(error);
resolve(data);
});
});
};
var gen = function* (){
var f1 = yield readFile('/etc/fstab');
var f2 = yield readFile('/etc/shells');
console.log(f1.toString());
console.log(f2.toString());
};
然后，手动执行上面的Generator函数。
var g = gen();
g.next().value.then(function(data){
g.next(data).value.then(function(data){
g.next(data);
});
});
手动执行其实就是用then方法，层层添加回调函数。理解了这一点，就可以写出一个自动执行器。
function run(gen){
var g = gen();
function next(data){
var result = g.next(data);
if (result.done) return result.value;
result.value.then(function(data){
next(data);
});
}
next();
}
run(gen);
上面代码中，只要Generator函数还没执行到最后一步，next函数就调用自身，以此实现自动执行。
17.4.4 co模块的源码
co就是上面那个自动执行器的扩展，它的源码只有几十行，非常简单。
首先，co函数接受Generator函数作为参数，返回一个 Promise 对象。
function co(gen) {
var ctx = this;
return new Promise(function(resolve, reject) {
});
}
在返回的Promise对象里面，co先检查参数gen是否为Generator函数。如果是，就执行该函数，得到一个内部指针对象；如果不是就返回，并将
Promise对象的状态改为resolved。
function co(gen) {
var ctx = this;
return new Promise(function(resolve, reject) {
if (typeof gen === 'function') gen = gen.call(ctx);
if (!gen || typeof gen.next !== 'function') return resolve(gen);
});
}
接着，co将Generator函数的内部指针对象的next方法，包装成onFulfilled函数。这主要是为了能够捕捉抛出的错误。
function co(gen) {
var ctx = this;
return new Promise(function(resolve, reject) {
if (typeof gen === 'function') gen = gen.call(ctx);
if (!gen || typeof gen.next !== 'function') return resolve(gen);
onFulfilled();
function onFulfilled(res) {
var ret;
try {
ret = gen.next(res);
} catch (e) {
return reject(e);
}
next(ret);
}
});
}
最后，就是关键的next函数，它会反复调用自身。
function next(ret) {
if (ret.done) return resolve(ret.value);
var value = toPromise.call(ctx, ret.value);
if (value &amp;&amp; isPromise(value)) return value.then(onFulfilled, onRejected);
return onRejected(new TypeError('You may only yield a function, promise, generator, array, or object, '
+ 'but the following object was passed: "' + String(ret.value) + '"'));
}
上面代码中，next 函数的内部代码，一共只有四行命令。
第一行，检查当前是否为 Generator 函数的最后一步，如果是就返回。
第二行，确保每一步的返回值，是 Promise 对象。
第三行，使用 then 方法，为返回值加上回调函数，然后通过 onFulfilled 函数再次调用 next 函数。
第四行，在参数不符合要求的情况下（参数非 Thunk 函数和 Promise 对象），将 Promise 对象的状态改为 rejected，从而终止执行。
17.4.5 处理并发的异步操作
co支持并发的异步操作，即允许某些操作同时进行，等到它们全部完成，才进行下一步。
这时，要把并发的操作都放在数组或对象里面，跟在yield语句后面。
// 数组的写法
co(function* () {
var res = yield [
Promise.resolve(1),
Promise.resolve(2)
];
console.log(res);
}).catch(onerror);
// 对象的写法
co(function* () {
var res = yield {
1: Promise.resolve(1),
2: Promise.resolve(2),
};
console.log(res);
}).catch(onerror);
下面是另一个例子。
co(function* () {
var values = [n1, n2, n3];
yield values.map(somethingAsync);
});
function* somethingAsync(x) {
// do something async
return y
}
上面的代码允许并发三个somethingAsync异步操作，等到它们全部完成，才会进行下一步。
17.5 async函数
17.5.1 含义
ES7提供了async函数，使得异步操作变得更加方便。async函数是什么？一句话，async函数就是Generator函数的语法糖。
前文有一个Generator函数，依次读取两个文件。
var fs = require('fs');
var readFile = function (fileName) {
return new Promise(function (resolve, reject) {
fs.readFile(fileName, function(error, data) {
if (error) reject(error);
resolve(data);
});
});
};
var gen = function* (){
var f1 = yield readFile('/etc/fstab');
var f2 = yield readFile('/etc/shells');
console.log(f1.toString());
console.log(f2.toString());
};
写成async函数，就是下面这样。
var asyncReadFile = async function (){
var f1 = await readFile('/etc/fstab');
var f2 = await readFile('/etc/shells');
console.log(f1.toString());
console.log(f2.toString());
};
一比较就会发现，async函数就是将Generator函数的星号（*）替换成async，将yield替换成await，仅此而已。
async函数对 Generator 函数的改进，体现在以下四点。
（1）内置执行器。Generator函数的执行必须靠执行器，所以才有了co模块，而async函数自带执行器。也就是说，async函数的执行，与普通函数一
模一样，只要一行。
var result = asyncReadFile();
上面的代码调用了asyncReadFile函数，然后它就会自动执行，输出最后结果。这完全不像Generator函数，需要调用next方法，或者用co模块，才能
得到真正执行，得到最后结果。
（2）更好的语义。async和await，比起星号和yield，语义更清楚了。async表示函数里有异步操作，await表示紧跟在后面的表达式需要等待结果。
（3）更广的适用性。 co模块约定，yield命令后面只能是Thunk函数或Promise对象，而async函数的await命令后面，可以是Promise对象和原始类
型的值（数值、字符串和布尔值，但这时等同于同步操作）。
（4）返回值是Promise。async函数的返回值是Promise对象，这比Generator函数的返回值是Iterator对象方便多了。你可以用then方法指定下一步的
操作。
进一步说，async函数完全可以看作多个异步操作，包装成的一个Promise对象，而await命令就是内部then命令的语法糖。
17.5.2 语法
async函数的语法规则总体上比较简单，难点是错误处理机制。
（1）async函数返回一个Promise对象。
async函数内部return语句返回的值，会成为then方法回调函数的参数。
async function f() {
return 'hello world';
}
f().then(v =&gt; console.log(v))
// "hello world"
上面代码中，函数f内部return命令返回的值，会被then方法回调函数接收到。
async函数内部抛出错误，会导致返回的Promise对象变为reject状态。抛出的错误对象会被catch方法回调函数接收到。
async function f() {
throw new Error('出错了');
}
f().then(
v =&gt; console.log(v),
e =&gt; console.log(e)
)
// Error: 出错了
（2）async函数返回的Promise对象，必须等到内部所有await命令的Promise对象执行完，才会发生状态改变。也就是说，只有async函数内部的异步
操作执行完，才会执行then方法指定的回调函数。
下面是一个例子。
async function getTitle(url) {
let response = await fetch(url);
let html = await response.text();
return html.match(/&lt;title&gt;([\s\S]+)&lt;\/title&gt;/i)[1];
}
getTitle('https://tc39.github.io/ecma262/').then(console.log)
// "ECMAScript 2017 Language Specification"
（3）正常情况下，await命令后面是一个Promise对象。如果不是，会被转成一个立即resolve的Promise对象。
async function f() {
return await 123;
}
f().then(v =&gt; console.log(v))
// 123
上面代码中，await命令的参数是数值123，它被转成Promise对象，并立即resolve。
await命令后面的Promise对象如果变为reject状态，则reject的参数会被catch方法的回调函数接收到。
async function f() {
await Promise.reject('出错了');
}
f()
.then(v =&gt; console.log(v))
.catch(e =&gt; console.log(e))
// 出错了
注意，上面代码中，await语句前面没有return，但是reject方法的参数依然传入了catch方法的回调函数。这里如果在await前面加上return，效果
是一样的。
只要一个await语句后面的Promise变为reject，那么整个async函数都会中断执行。
async function f() {
await Promise.reject('出错了');
await Promise.resolve('hello world'); // 不会执行
}
上面代码中，第二个await语句是不会执行的，因为第一个await语句状态变成了reject。
为了避免这个问题，可以将第一个await放在try...catch结构里面，这样第二个await就会执行。
async function f() {
try {
await Promise.reject('出错了');
} catch(e) {
}
return await Promise.resolve('hello world');
}
f()
.then(v =&gt; console.log(v))
// hello world
另一种方法是await后面的Promise对象再跟一个catch方面，处理前面可能出现的错误。
async function f() {
await Promise.reject('出错了')
.catch(e =&gt; console.log(e));
return await Promise.resolve('hello world');
}
f()
.then(v =&gt; console.log(v))
// 出错了
// hello world
如果有多个await命令，可以统一放在try...catch结构中。
async function main() {
try {
var val1 = await firstStep();
var val2 = await secondStep(val1);
var val3 = await thirdStep(val1, val2);
console.log('Final: ', val3);
}
catch (err) {
console.error(err);
}
}
（4）如果await后面的异步操作出错，那么等同于async函数返回的Promise对象被reject。
async function f() {
await new Promise(function (resolve, reject) {
throw new Error('出错了');
});
}
f()
.then(v =&gt; console.log(v))
.catch(e =&gt; console.log(e))
// Error：出错了
上面代码中，async函数f执行后，await后面的Promise对象会抛出一个错误对象，导致catch方法的回调函数被调用，它的参数就是抛出的错误对
象。具体的执行机制，可以参考后文的“async函数的实现”。
防止出错的方法，也是将其放在try...catch代码块之中。
async function f() {
try {
await new Promise(function (resolve, reject) {
throw new Error('出错了');
});
} catch(e) {
}
return await('hello world');
}
17.5.3 async函数的实现
async 函数的实现，就是将 Generator 函数和自动执行器，包装在一个函数里。
async function fn(args){
// ...
}
// 等同于
function fn(args){
return spawn(function*() {
// ...
});
}
所有的async函数都可以写成上面的第二种形式，其中的 spawn 函数就是自动执行器。
下面给出spawn函数的实现，基本就是前文自动执行器的翻版。
function spawn(genF) {
return new Promise(function(resolve, reject) {
var gen = genF();
function step(nextF) {
try {
var next = nextF();
} catch(e) {
return reject(e);
}
if(next.done) {
return resolve(next.value);
}
Promise.resolve(next.value).then(function(v) {
step(function() { return gen.next(v); });
}, function(e) {
step(function() { return gen.throw(e); });
});
}
step(function() { return gen.next(undefined); });
});
}
async函数是非常新的语法功能，新到都不属于 ES6，而是属于 ES7。目前，它仍处于提案阶段，但是转码器Babel和regenerator都已经支持，转码
后就能使用。
17.5.4 async 函数的用法
async函数返回一个Promise对象，可以使用then方法添加回调函数。当函数执行的时候，一旦遇到await就会先返回，等到触发的异步操作完成，再
接着执行函数体内后面的语句。
下面是一个例子。
async function getStockPriceByName(name) {
var symbol = await getStockSymbol(name);
var stockPrice = await getStockPrice(symbol);
return stockPrice;
}
getStockPriceByName('goog').then(function (result) {
console.log(result);
});
上面代码是一个获取股票报价的函数，函数前面的async关键字，表明该函数内部有异步操作。调用该函数时，会立即返回一个Promise对象。
下面的例子，指定多少毫秒后输出一个值。
function timeout(ms) {
return new Promise((resolve) =&gt; {
setTimeout(resolve, ms);
});
}
async function asyncPrint(value, ms) {
await timeout(ms);
console.log(value)
}
asyncPrint('hello world', 50);
上面代码指定50毫秒以后，输出"hello world"。
Async函数有多种使用形式。
// 函数声明
async function foo() {}
// 函数表达式
const foo = async function () {};
// 对象的方法
let obj = { async foo() {} };
// 箭头函数
const foo = async () =&gt; {};
17.5.5 注意点
第一点，await命令后面的Promise对象，运行结果可能是rejected，所以最好把await命令放在try...catch代码块中。
async function myFunction() {
try {
await somethingThatReturnsAPromise();
} catch (err) {
console.log(err);
}
}
// 另一种写法
async function myFunction() {
await somethingThatReturnsAPromise()
.catch(function (err) {
console.log(err);
};
}
第二点，多个await命令后面的异步操作，如果不存在继发关系，最好让它们同时触发。
let foo = await getFoo();
let bar = await getBar();
上面代码中，getFoo和getBar是两个独立的异步操作（即互不依赖），被写成继发关系。这样比较耗时，因为只有getFoo完成以后，才会执
行getBar，完全可以让它们同时触发。
// 写法一
let [foo, bar] = await Promise.all([getFoo(), getBar()]);
// 写法二
let fooPromise = getFoo();
let barPromise = getBar();
let foo = await fooPromise;
let bar = await barPromise;
上面两种写法，getFoo和getBar都是同时触发，这样就会缩短程序的执行时间。
第三点，await命令只能用在async函数之中，如果用在普通函数，就会报错。
async function dbFuc(db) {
let docs = [{}, {}, {}];
// 报错
docs.forEach(function (doc) {
await db.post(doc);
});
}
上面代码会报错，因为await用在普通函数之中了。但是，如果将forEach方法的参数改成async函数，也有问题。
async function dbFuc(db) {
let docs = [{}, {}, {}];
// 可能得到错误结果
docs.forEach(async function (doc) {
await db.post(doc);
});
}
上面代码可能不会正常工作，原因是这时三个db.post操作将是并发执行，也就是同时执行，而不是继发执行。正确的写法是采用for循环。
async function dbFuc(db) {
let docs = [{}, {}, {}];
for (let doc of docs) {
await db.post(doc);
}
}
如果确实希望多个请求并发执行，可以使用Promise.all方法。
async function dbFuc(db) {
let docs = [{}, {}, {}];
let promises = docs.map((doc) =&gt; db.post(doc));
let results = await Promise.all(promises);
console.log(results);
}
// 或者使用下面的写法
async function dbFuc(db) {
let docs = [{}, {}, {}];
let promises = docs.map((doc) =&gt; db.post(doc));
let results = [];
for (let promise of promises) {
results.push(await promise);
}
console.log(results);
}
ES6将await增加为保留字。使用这个词作为标识符，在ES5是合法的，在ES6将抛出SyntaxError。
17.5.6 与Promise、Generator的比较
我们通过一个例子，来看Async函数与Promise、Generator函数的区别。
假定某个DOM元素上面，部署了一系列的动画，前一个动画结束，才能开始后一个。如果当中有一个动画出错，就不再往下执行，返回上一个成功执
行的动画的返回值。
首先是Promise的写法。
function chainAnimationsPromise(elem, animations) {
// 变量ret用来保存上一个动画的返回值
var ret = null;
// 新建一个空的Promise
var p = Promise.resolve();
// 使用then方法，添加所有动画
for(var anim of animations) {
p = p.then(function(val) {
ret = val;
return anim(elem);
});
}
// 返回一个部署了错误捕捉机制的Promise
return p.catch(function(e) {
/* 忽略错误，继续执行 */
}).then(function() {
return ret;
});
}
虽然Promise的写法比回调函数的写法大大改进，但是一眼看上去，代码完全都是Promise的API（then、catch等等），操作本身的语义反而不容易看
出来。
接着是Generator函数的写法。
function chainAnimationsGenerator(elem, animations) {
return spawn(function*() {
var ret = null;
try {
for(var anim of animations) {
ret = yield anim(elem);
}
} catch(e) {
/* 忽略错误，继续执行 */
}
return ret;
});
}
上面代码使用Generator函数遍历了每个动画，语义比Promise写法更清晰，用户定义的操作全部都出现在spawn函数的内部。这个写法的问题在于，
必须有一个任务运行器，自动执行Generator函数，上面代码的spawn函数就是自动执行器，它返回一个Promise对象，而且必须保证yield语句后面的
表达式，必须返回一个Promise。
最后是Async函数的写法。
async function chainAnimationsAsync(elem, animations) {
var ret = null;
try {
for(var anim of animations) {
ret = await anim(elem);
}
} catch(e) {
/* 忽略错误，继续执行 */
}
return ret;
}
可以看到Async函数的实现最简洁，最符合语义，几乎没有语义不相关的代码。它将Generator写法中的自动执行器，改在语言层面提供，不暴露给用
户，因此代码量最少。如果使用Generator写法，自动执行器需要用户自己提供。
18 Class
18.1 Class基本语法
18.1.1 概述
JavaScript语言的传统方法是通过构造函数，定义并生成新对象。下面是一个例子。
function Point(x, y) {
this.x = x;
this.y = y;
}
Point.prototype.toString = function () {
return '(' + this.x + ', ' + this.y + ')';
};
var p = new Point(1, 2);
上面这种写法跟传统的面向对象语言（比如C++和Java）差异很大，很容易让新学习这门语言的程序员感到困惑。
ES6提供了更接近传统语言的写法，引入了Class（类）这个概念，作为对象的模板。通过class关键字，可以定义类。基本上，ES6的class可以看作
只是一个语法糖，它的绝大部分功能，ES5都可以做到，新的class写法只是让对象原型的写法更加清晰、更像面向对象编程的语法而已。上面的代码
用ES6的“类”改写，就是下面这样。
//定义类
class Point {
constructor(x, y) {
this.x = x;
this.y = y;
}
toString() {
return '(' + this.x + ', ' + this.y + ')';
}
}
上面代码定义了一个“类”，可以看到里面有一个constructor方法，这就是构造方法，而this关键字则代表实例对象。也就是说，ES5的构造函
数Point，对应ES6的Point类的构造方法。
Point类除了构造方法，还定义了一个toString方法。注意，定义“类”的方法的时候，前面不需要加上function这个关键字，直接把函数定义放进去了
就可以了。另外，方法之间不需要逗号分隔，加了会报错。
ES6的类，完全可以看作构造函数的另一种写法。
class Point {
// ...
}
typeof Point // "function"
Point === Point.prototype.constructor // true
上面代码表明，类的数据类型就是函数，类本身就指向构造函数。
使用的时候，也是直接对类使用new命令，跟构造函数的用法完全一致。
class Bar {
doStuff() {
console.log('stuff');
}
}
var b = new Bar();
b.doStuff() // "stuff"
构造函数的prototype属性，在ES6的“类”上面继续存在。事实上，类的所有方法都定义在类的prototype属性上面。
class Point {
constructor(){
// ...
}
toString(){
// ...
}
toValue(){
// ...
}
}
// 等同于
Point.prototype = {
toString(){},
toValue(){}
};
在类的实例上面调用方法，其实就是调用原型上的方法。
class B {}
let b = new B();
b.constructor === B.prototype.constructor // true
上面代码中，b是B类的实例，它的constructor方法就是B类原型的constructor方法。
由于类的方法都定义在prototype对象上面，所以类的新方法可以添加在prototype对象上面。Object.assign方法可以很方便地一次向类添加多个方
法。
class Point {
constructor(){
// ...
}
}
Object.assign(Point.prototype, {
toString(){},
toValue(){}
});
prototype对象的constructor属性，直接指向“类”的本身，这与ES5的行为是一致的。
Point.prototype.constructor === Point // true
另外，类的内部所有定义的方法，都是不可枚举的（non-enumerable）。
class Point {
constructor(x, y) {
// ...
}
toString() {
// ...
}
}
Object.keys(Point.prototype)
// []
Object.getOwnPropertyNames(Point.prototype)
// ["constructor","toString"]
上面代码中，toString方法是Point类内部定义的方法，它是不可枚举的。这一点与ES5的行为不一致。
var Point = function (x, y) {
// ...
};
Point.prototype.toString = function() {
// ...
};
Object.keys(Point.prototype)
// ["toString"]
Object.getOwnPropertyNames(Point.prototype)
// ["constructor","toString"]
上面代码采用ES5的写法，toString方法就是可枚举的。
类的属性名，可以采用表达式。
let methodName = "getArea";
class Square{
constructor(length) {
// ...
}
[methodName]() {
// ...
}
}
上面代码中，Square类的方法名getArea，是从表达式得到的。
18.1.2 constructor方法
constructor方法是类的默认方法，通过new命令生成对象实例时，自动调用该方法。一个类必须有constructor方法，如果没有显式定义，一个空
的constructor方法会被默认添加。
constructor() {}
constructor方法默认返回实例对象（即this），完全可以指定返回另外一个对象。
class Foo {
constructor() {
return Object.create(null);
}
}
new Foo() instanceof Foo
// false
上面代码中，constructor函数返回一个全新的对象，结果导致实例对象不是Foo类的实例。
类的构造函数，不使用new是没法调用的，会报错。这是它跟普通构造函数的一个主要区别，后者不用new也可以执行。
class Foo {
constructor() {
return Object.create(null);
}
}
Foo()
// TypeError: Class constructor Foo cannot be invoked without 'new'
18.1.3 类的实例对象
生成类的实例对象的写法，与ES5完全一样，也是使用new命令。如果忘记加上new，像函数那样调用Class，将会报错。
// 报错
var point = Point(2, 3);
// 正确
var point = new Point(2, 3);
与ES5一样，实例的属性除非显式定义在其本身（即定义在this对象上），否则都是定义在原型上（即定义在class上）。
//定义类
class Point {
constructor(x, y) {
this.x = x;
this.y = y;
}
toString() {
return '(' + this.x + ', ' + this.y + ')';
}
}
var point = new Point(2, 3);
point.toString() // (2, 3)
point.hasOwnProperty('x') // true
point.hasOwnProperty('y') // true
point.hasOwnProperty('toString') // false
point.__proto__.hasOwnProperty('toString') // true
上面代码中，x和y都是实例对象point自身的属性（因为定义在this变量上），所以hasOwnProperty方法返回true，而toString是原型对象的属性
（因为定义在Point类上），所以hasOwnProperty方法返回false。这些都与ES5的行为保持一致。
与ES5一样，类的所有实例共享一个原型对象。
var p1 = new Point(2,3);
var p2 = new Point(3,2);
p1.__proto__ === p2.__proto__
//true
上面代码中，p1和p2都是Point的实例，它们的原型都是Point，所以__proto__属性是相等的。
这也意味着，可以通过实例的__proto__属性为Class添加方法。
var p1 = new Point(2,3);
var p2 = new Point(3,2);
p1.__proto__.printName = function () { return 'Oops' };
p1.printName() // "Oops"
p2.printName() // "Oops"
var p3 = new Point(4,2);
p3.printName() // "Oops"
上面代码在p1的原型上添加了一个printName方法，由于p1的原型就是p2的原型，因此p2也可以调用这个方法。而且，此后新建的实例p3也可以调用
这个方法。这意味着，使用实例的__proto__属性改写原型，必须相当谨慎，不推荐使用，因为这会改变Class的原始定义，影响到所有实例。
18.1.4 不存在变量提升
Class不存在变量提升（hoist），这一点与ES5完全不同。
new Foo(); // ReferenceError
class Foo {}
上面代码中，Foo类使用在前，定义在后，这样会报错，因为ES6不会把类的声明提升到代码头部。这种规定的原因与下文要提到的继承有关，必须保
证子类在父类之后定义。
{
let Foo = class {};
class Bar extends Foo {
}
}
上面的代码不会报错，因为class继承Foo的时候，Foo已经有定义了。但是，如果存在class的提升，上面代码就会报错，因为class会被提升到代码
头部，而let命令是不提升的，所以导致class继承Foo的时候，Foo还没有定义。
18.1.5 Class表达式
与函数一样，类也可以使用表达式的形式定义。
const MyClass = class Me {
getClassName() {
return Me.name;
}
};
上面代码使用表达式定义了一个类。需要注意的是，这个类的名字是MyClass而不是Me，Me只在Class的内部代码可用，指代当前类。
let inst = new MyClass();
inst.getClassName() // Me
Me.name // ReferenceError: Me is not defined
上面代码表示，Me只在Class内部有定义。
如果类的内部没用到的话，可以省略Me，也就是可以写成下面的形式。
const MyClass = class { /* ... */ };
采用Class表达式，可以写出立即执行的Class。
let person = new class {
constructor(name) {
this.name = name;
}
sayName() {
console.log(this.name);
}
}('张三');
person.sayName(); // "张三"
上面代码中，person是一个立即执行的类的实例。
18.1.6 私有方法
私有方法是常见需求，但ES6不提供，只能通过变通方法模拟实现。
一种做法是在命名上加以区别。
class Widget {
// 公有方法
foo (baz) {
this._bar(baz);
}
// 私有方法
_bar(baz) {
return this.snaf = baz;
}
// ...
}
上面代码中，_bar方法前面的下划线，表示这是一个只限于内部使用的私有方法。但是，这种命名是不保险的，在类的外部，还是可以调用到这个方
法。
另一种方法就是索性将私有方法移出模块，因为模块内部的所有方法都是对外可见的。
class Widget {
foo (baz) {
bar.call(this, baz);
}
// ...
}
function bar(baz) {
return this.snaf = baz;
}
上面代码中，foo是公有方法，内部调用了bar.call(this, baz)。这使得bar实际上成为了当前模块的私有方法。
还有一种方法是利用Symbol值的唯一性，将私有方法的名字命名为一个Symbol值。
const bar = Symbol('bar');
const snaf = Symbol('snaf');
export default class myClass{
// 公有方法
foo(baz) {
this[bar](baz);
}
// 私有方法
[bar](baz) {
return this[snaf] = baz;
}
// ...
};
上面代码中，bar和snaf都是Symbol值，导致第三方无法获取到它们，因此达到了私有方法和私有属性的效果。
18.1.7 this的指向
类的方法内部如果含有this，它默认指向类的实例。但是，必须非常小心，一旦单独使用该方法，很可能报错。
class Logger {
printName(name = 'there') {
this.print(`Hello ${name}`);
}
print(text) {
console.log(text);
}
}
const logger = new Logger();
const { printName } = logger;
printName(); // TypeError: Cannot read property 'print' of undefined
上面代码中，printName方法中的this，默认指向Logger类的实例。但是，如果将这个方法提取出来单独使用，this会指向该方法运行时所在的环
境，因为找不到print方法而导致报错。
一个比较简单的解决方法是，在构造方法中绑定this，这样就不会找不到print方法了。
class Logger {
constructor() {
this.printName = this.printName.bind(this);
}
// ...
}
另一种解决方法是使用箭头函数。
class Logger {
constructor() {
this.printName = (name = 'there') =&gt; {
this.print(`Hello ${name}`);
};
}
// ...
}
还有一种解决方法是使用Proxy，获取方法的时候，自动绑定this。
function selfish (target) {
const cache = new WeakMap();
const handler = {
get (target, key) {
const value = Reflect.get(target, key);
if (typeof value !== 'function') {
return value;
}
if (!cache.has(value)) {
cache.set(value, value.bind(target));
}
return cache.get(value);
}
};
const proxy = new Proxy(target, handler);
return proxy;
}
const logger = selfish(new Logger());
18.1.8 严格模式
类和模块的内部，默认就是严格模式，所以不需要使用use strict指定运行模式。只要你的代码写在类或模块之中，就只有严格模式可用。
考虑到未来所有的代码，其实都是运行在模块之中，所以ES6实际上把整个语言升级到了严格模式。
18.1.9 name属性
由于本质上，ES6的类只是ES5的构造函数的一层包装，所以函数的许多特性都被Class继承，包括name属性。
class Point {}
Point.name // "Point"
Point.name // "Point"
name属性总是返回紧跟在class关键字后面的类名。
18.2 Class的继承
18.2.1 基本用法
Class之间可以通过extends关键字实现继承，这比ES5的通过修改原型链实现继承，要清晰和方便很多。
class ColorPoint extends Point {}
上面代码定义了一个ColorPoint类，该类通过extends关键字，继承了Point类的所有属性和方法。但是由于没有部署任何代码，所以这两个类完全一
样，等于复制了一个Point类。下面，我们在ColorPoint内部加上代码。
class ColorPoint extends Point {
constructor(x, y, color) {
super(x, y); // 调用父类的constructor(x, y)
this.color = color;
}
toString() {
return this.color + ' ' + super.toString(); // 调用父类的toString()
}
}
上面代码中，constructor方法和toString方法之中，都出现了super关键字，它在这里表示父类的构造函数，用来新建父类的this对象。
子类必须在constructor方法中调用super方法，否则新建实例时会报错。这是因为子类没有自己的this对象，而是继承父类的this对象，然后对其进
行加工。如果不调用super方法，子类就得不到this对象。
class Point { /* ... */ }
class ColorPoint extends Point {
constructor() {
}
}
let cp = new ColorPoint(); // ReferenceError
上面代码中，ColorPoint继承了父类Point，但是它的构造函数没有调用super方法，导致新建实例时报错。
ES5的继承，实质是先创造子类的实例对象this，然后再将父类的方法添加到this上面（Parent.apply(this)）。ES6的继承机制完全不同，实质是
先创造父类的实例对象this（所以必须先调用super方法），然后再用子类的构造函数修改this。
如果子类没有定义constructor方法，这个方法会被默认添加，代码如下。也就是说，不管有没有显式定义，任何一个子类都有constructor方法。
constructor(...args) {
super(...args);
}
另一个需要注意的地方是，在子类的构造函数中，只有调用super之后，才可以使用this关键字，否则会报错。这是因为子类实例的构建，是基于对父
类实例加工，只有super方法才能返回父类实例。
class Point {
constructor(x, y) {
this.x = x;
this.y = y;
}
}
class ColorPoint extends Point {
constructor(x, y, color) {
this.color = color; // ReferenceError
super(x, y);
this.color = color; // 正确
}
}
上面代码中，子类的constructor方法没有调用super之前，就使用this关键字，结果报错，而放在super方法之后就是正确的。
下面是生成子类实例的代码。
let cp = new ColorPoint(25, 8, 'green');
cp instanceof ColorPoint // true
cp instanceof Point // true
上面代码中，实例对象cp同时是ColorPoint和Point两个类的实例，这与ES5的行为完全一致。
18.2.2 类的prototype属性和__proto__属性
大多数浏览器的ES5实现之中，每一个对象都有__proto__属性，指向对应的构造函数的prototype属性。Class作为构造函数的语法糖，同时有
prototype属性和__proto__属性，因此同时存在两条继承链。
（1）子类的__proto__属性，表示构造函数的继承，总是指向父类。
（2）子类prototype属性的__proto__属性，表示方法的继承，总是指向父类的prototype属性。
class A {
}
class B extends A {
}
B.__proto__ === A // true
B.prototype.__proto__ === A.prototype // true
上面代码中，子类B的__proto__属性指向父类A，子类B的prototype属性的__proto__属性指向父类A的prototype属性。
这样的结果是因为，类的继承是按照下面的模式实现的。
class A {
}
class B {
}
// B的实例继承A的实例
Object.setPrototypeOf(B.prototype, A.prototype);
// B继承A的静态属性
Object.setPrototypeOf(B, A);
《对象的扩展》一章给出过Object.setPrototypeOf方法的实现。
Object.setPrototypeOf = function (obj, proto) {
obj.__proto__ = proto;
return obj;
}
因此，就得到了上面的结果。
Object.setPrototypeOf(B.prototype, A.prototype);
// 等同于
B.prototype.__proto__ = A.prototype;
Object.setPrototypeOf(B, A);
// 等同于
B.__proto__ = A;
这两条继承链，可以这样理解：作为一个对象，子类（B）的原型（__proto__属性）是父类（A）；作为一个构造函数，子类（B）的原型
（prototype属性）是父类的实例。
Object.create(A.prototype);
// 等同于
B.prototype.__proto__ = A.prototype;
18.2.3 Extends 的继承目标
extends关键字后面可以跟多种类型的值。
class B extends A {
}
上面代码的A，只要是一个有prototype属性的函数，就能被B继承。由于函数都有prototype属性（除了Function.prototype函数），因此A可以是任
意函数。
下面，讨论三种特殊情况。
第一种特殊情况，子类继承Object类。
class A extends Object {
}
A.__proto__ === Object // true
A.prototype.__proto__ === Object.prototype // true
这种情况下，A其实就是构造函数Object的复制，A的实例就是Object的实例。
第二种特殊情况，不存在任何继承。
class A {
}
A.__proto__ === Function.prototype // true
A.prototype.__proto__ === Object.prototype // true
这种情况下，A作为一个基类（即不存在任何继承），就是一个普通函数，所以直接继承Funciton.prototype。但是，A调用后返回一个空对象
（即Object实例），所以A.prototype.__proto__指向构造函数（Object）的prototype属性。
第三种特殊情况，子类继承null。
class A extends null {
}
A.__proto__ === Function.prototype // true
A.prototype.__proto__ === undefined // true
这种情况与第二种情况非常像。A也是一个普通函数，所以直接继承Funciton.prototype。但是，A调用后返回的对象不继承任何方法，所以它
的__proto__指向Function.prototype，即实质上执行了下面的代码。
class C extends null {
constructor() { return Object.create(null); }
}
18.2.4 Object.getPrototypeOf()
Object.getPrototypeOf方法可以用来从子类上获取父类。
Object.getPrototypeOf(ColorPoint) === Point
// true
因此，可以使用这个方法判断，一个类是否继承了另一个类。
18.2.5 super关键字
super这个关键字，有两种用法，含义不同。
（1）作为函数调用时（即super(...args)），super代表父类的构造函数。
（2）作为对象调用时（即super.prop或super.method()），super代表父类。注意，此时super即可以引用父类实例的属性和方法，也可以引用父类
的静态方法。
class B extends A {
get m() {
return this._p * super._p;
}
set m() {
throw new Error('该属性只读');
}
}
上面代码中，子类通过super关键字，调用父类实例的_p属性。
由于，对象总是继承其他对象的，所以可以在任意一个对象中，使用super关键字。
var obj = {
toString() {
return "MyObject: " + super.toString();
}
};
obj.toString(); // MyObject: [object Object]
18.2.6 实例的__proto__属性
子类实例的__proto__属性的__proto__属性，指向父类实例的__proto__属性。也就是说，子类的原型的原型，是父类的原型。
var p1 = new Point(2, 3);
var p2 = new ColorPoint(2, 3, 'red');
p2.__proto__ === p1.__proto__ // false
p2.__proto__.__proto__ === p1.__proto__ // true
上面代码中，ColorPoint继承了Point，导致前者原型的原型是后者的原型。
因此，通过子类实例的__proto__.__proto__属性，可以修改父类实例的行为。
p2.__proto__.__proto__.printName = function () {
console.log('Ha');
};
p1.printName() // "Ha"
上面代码在ColorPoint的实例p2上向Point类添加方法，结果影响到了Point的实例p1。
18.3 原生构造函数的继承
原生构造函数是指语言内置的构造函数，通常用来生成数据结构。ECMAScript的原生构造函数大致有下面这些。
Boolean()
Number()
String()
Array()
Date()
Function()
RegExp()
Error()
Object()
以前，这些原生构造函数是无法继承的，比如，不能自己定义一个Array的子类。
function MyArray() {
Array.apply(this, arguments);
}
MyArray.prototype = Object.create(Array.prototype, {
constructor: {
value: MyArray,
writable: true,
configurable: true,
enumerable: true
}
});
上面代码定义了一个继承Array的MyArray类。但是，这个类的行为与Array完全不一致。
var colors = new MyArray();
colors[0] = "red";
colors.length // 0
colors.length = 0;
colors[0] // "red"
之所以会发生这种情况，是因为子类无法获得原生构造函数的内部属性，通过Array.apply()或者分配给原型对象都不行。原生构造函数会忽
略apply方法传入的this，也就是说，原生构造函数的this无法绑定，导致拿不到内部属性。
ES5是先新建子类的实例对象this，再将父类的属性添加到子类上，由于父类的内部属性无法获取，导致无法继承原生的构造函数。比如，Array构造
函数有一个内部属性[[DefineOwnProperty]]，用来定义新属性时，更新length属性，这个内部属性无法在子类获取，导致子类的length属性行为不正
常。
下面的例子中，我们想让一个普通对象继承Error对象。
var e = {};
Object.getOwnPropertyNames(Error.call(e))
// [ 'stack' ]
Object.getOwnPropertyNames(e)
// []
上面代码中，我们想通过Error.call(e)这种写法，让普通对象e具有Error对象的实例属性。但是，Error.call()完全忽略传入的第一个参数，而是
返回一个新对象，e本身没有任何变化。这证明了Error.call(e)这种写法，无法继承原生构造函数。
ES6允许继承原生构造函数定义子类，因为ES6是先新建父类的实例对象this，然后再用子类的构造函数修饰this，使得父类的所有行为都可以继
承。下面是一个继承Array的例子。
class MyArray extends Array {
constructor(...args) {
super(...args);
}
}
var arr = new MyArray();
arr[0] = 12;
arr.length // 1
arr.length = 0;
arr[0] // undefined
上面代码定义了一个MyArray类，继承了Array构造函数，因此就可以从MyArray生成数组的实例。这意味着，ES6可以自定义原生数据结构（比如
Array、String等）的子类，这是ES5无法做到的。
上面这个例子也说明，extends关键字不仅可以用来继承类，还可以用来继承原生的构造函数。因此可以在原生数据结构的基础上，定义自己的数据结
构。下面就是定义了一个带版本功能的数组。
class VersionedArray extends Array {
constructor() {
super();
this.history = [[]];
}
commit() {
this.history.push(this.slice());
}
revert() {
this.splice(0, this.length, ...this.history[this.history.length - 1]);
}
}
var x = new VersionedArray();
x.push(1);
x.push(2);
x // [1, 2]
x.history // [[]]
x.commit();
x.history // [[], [1, 2]]
x.push(3);
x // [1, 2, 3]
x.revert();
x // [1, 2]
上面代码中，VersionedArray结构会通过commit方法，将自己的当前状态存入history属性，然后通过revert方法，可以撤销当前版本，回到上一个
版本。除此之外，VersionedArray依然是一个数组，所有原生的数组方法都可以在它上面调用。
下面是一个自定义Error子类的例子。
class ExtendableError extends Error {
constructor(message) {
super();
this.message = message;
this.stack = (new Error()).stack;
this.name = this.constructor.name;
}
}
class MyError extends ExtendableError {
constructor(m) {
super(m);
}
}
var myerror = new MyError('ll');
myerror.message // "ll"
myerror instanceof Error // true
myerror.name // "MyError"
myerror.stack
// Error
// at MyError.ExtendableError
// ...
注意，继承Object的子类，有一个行为差异。
class NewObj extends Object{
constructor(){
super(...arguments);
}
}
var o = new NewObj({attr: true});
console.log(o.attr === true); // false
上面代码中，NewObj继承了Object，但是无法通过super方法向父类Object传参。这是因为ES6改变了Object构造函数的行为，一旦发现Object方法
不是通过new Object()这种形式调用，ES6规定Object构造函数会忽略参数。
18.4 Class的取值函数（getter）和存值函数（setter）
与ES5一样，在Class内部可以使用get和set关键字，对某个属性设置存值函数和取值函数，拦截该属性的存取行为。
class MyClass {
constructor() {
// ...
}
get prop() {
return 'getter';
}
set prop(value) {
console.log('setter: '+value);
}
}
let inst = new MyClass();
inst.prop = 123;
// setter: 123
inst.prop
// 'getter'
上面代码中，prop属性有对应的存值函数和取值函数，因此赋值和读取行为都被自定义了。
存值函数和取值函数是设置在属性的descriptor对象上的。
class CustomHTMLElement {
constructor(element) {
this.element = element;
}
get html() {
return this.element.innerHTML;
}
set html(value) {
this.element.innerHTML = value;
}
}
var descriptor = Object.getOwnPropertyDescriptor(
CustomHTMLElement.prototype, "html");
"get" in descriptor // true
"set" in descriptor // true
上面代码中，存值函数和取值函数是定义在html属性的描述对象上面，这与ES5完全一致。
18.5 Class的Generator方法
如果某个方法之前加上星号（*），就表示该方法是一个Generator函数。
class Foo {
constructor(...args) {
this.args = args;
}
* [Symbol.iterator]() {
for (let arg of this.args) {
yield arg;
}
}
}
for (let x of new Foo('hello', 'world')) {
console.log(x);
}
// hello
// world
上面代码中，Foo类的Symbol.iterator方法前有一个星号，表示该方法是一个Generator函数。Symbol.iterator方法返回一个Foo类的默认遍历
器，for...of循环会自动调用这个遍历器。
18.6 Class的静态方法
类相当于实例的原型，所有在类中定义的方法，都会被实例继承。如果在一个方法前，加上static关键字，就表示该方法不会被实例继承，而是直接
通过类来调用，这就称为“静态方法”。
class Foo {
static classMethod() {
return 'hello';
}
}
Foo.classMethod() // 'hello'
var foo = new Foo();
foo.classMethod()
// TypeError: foo.classMethod is not a function
上面代码中，Foo类的classMethod方法前有static关键字，表明该方法是一个静态方法，可以直接在Foo类上调用（Foo.classMethod()），而不是
在Foo类的实例上调用。如果在实例上调用静态方法，会抛出一个错误，表示不存在该方法。
父类的静态方法，可以被子类继承。
class Foo {
static classMethod() {
return 'hello';
}
}
class Bar extends Foo {
}
Bar.classMethod(); // 'hello'
上面代码中，父类Foo有一个静态方法，子类Bar可以调用这个方法。
静态方法也是可以从super对象上调用的。
class Foo {
static classMethod() {
return 'hello';
}
}
class Bar extends Foo {
static classMethod() {
return super.classMethod() + ', too';
}
}
Bar.classMethod();
18.7 Class的静态属性和实例属性
静态属性指的是Class本身的属性，即Class.propname，而不是定义在实例对象（this）上的属性。
class Foo {
}
Foo.prop = 1;
Foo.prop // 1
上面的写法为Foo类定义了一个静态属性prop。
目前，只有这种写法可行，因为ES6明确规定，Class内部只有静态方法，没有静态属性。
// 以下两种写法都无效
class Foo {
// 写法一
prop: 2
// 写法二
static prop: 2
}
Foo.prop // undefined
ES7有一个静态属性的提案，目前Babel转码器支持。
这个提案对实例属性和静态属性，都规定了新的写法。
（1）类的实例属性
类的实例属性可以用等式，写入类的定义之中。
class MyClass {
myProp = 42;
constructor() {
console.log(this.myProp); // 42
}
}
上面代码中，myProp就是MyClass的实例属性。在MyClass的实例上，可以读取这个属性。
以前，我们定义实例属性，只能写在类的constructor方法里面。
class ReactCounter extends React.Component {
constructor(props) {
super(props);
this.state = {
count: 0
};
}
}
上面代码中，构造方法constructor里面，定义了this.state属性。
有了新的写法以后，可以不在constructor方法里面定义。
class ReactCounter extends React.Component {
state = {
count: 0
};
}
这种写法比以前更清晰。
为了可读性的目的，对于那些在constructor里面已经定义的实例属性，新写法允许直接列出。
class ReactCounter extends React.Component {
constructor(props) {
super(props);
this.state = {
count: 0
};
}
state;
}
（2）类的静态属性
类的静态属性只要在上面的实例属性写法前面，加上static关键字就可以了。
class MyClass {
static myStaticProp = 42;
constructor() {
console.log(MyClass.myProp); // 42
}
}
同样的，这个新写法大大方便了静态属性的表达。
// 老写法
class Foo {
}
Foo.prop = 1;
// 新写法
class Foo {
static prop = 1;
}
上面代码中，老写法的静态属性定义在类的外部。整个类生成以后，再生成静态属性。这样让人很容易忽略这个静态属性，也不符合相关代码应该放
在一起的代码组织原则。另外，新写法是显式声明（declarative），而不是赋值处理，语义更好。
18.8 new.target属性
new是从构造函数生成实例的命令。ES6为new命令引入了一个new.target属性，（在构造函数中）返回new命令作用于的那个构造函数。如果构造函数
不是通过new命令调用的，new.target会返回undefined，因此这个属性可以用来确定构造函数是怎么调用的。
function Person(name) {
if (new.target !== undefined) {
this.name = name;
} else {
throw new Error('必须使用new生成实例');
}
}
// 另一种写法
function Person(name) {
if (new.target === Person) {
this.name = name;
} else {
throw new Error('必须使用new生成实例');
}
}
var person = new Person('张三'); // 正确
var notAPerson = Person.call(person, '张三'); // 报错
上面代码确保构造函数只能通过new命令调用。
Class内部调用new.target，返回当前Class。
class Rectangle {
constructor(length, width) {
console.log(new.target === Rectangle);
this.length = length;
this.width = width;
}
}
var obj = new Rectangle(3, 4); // 输出 true
需要注意的是，子类继承父类时，new.target会返回子类。
class Rectangle {
constructor(length, width) {
console.log(new.target === Rectangle);
// ...
}
}
class Square extends Rectangle {
constructor(length) {
super(length, length);
}
}
var obj = new Square(3); // 输出 false
上面代码中，new.target会返回子类。
利用这个特点，可以写出不能独立使用、必须继承后才能使用的类。
class Shape {
constructor() {
if (new.target === Shape) {
throw new Error('本类不能实例化');
}
}
}
class Rectangle extends Shape {
constructor(length, width) {
super();
// ...
}
}
var x = new Shape(); // 报错
var y = new Rectangle(3, 4); // 正确
上面代码中，Shape类不能被实例化，只能用于继承。
注意，在函数外部，使用new.target会报错。
18.9 Mixin模式的实现
Mixin模式指的是，将多个类的接口“混入”（mix in）另一个类。它在ES6的实现如下。
function mix(...mixins) {
class Mix {}
for (let mixin of mixins) {
copyProperties(Mix, mixin);
copyProperties(Mix.prototype, mixin.prototype);
}
return Mix;
}
function copyProperties(target, source) {
for (let key of Reflect.ownKeys(source)) {
if ( key !== "constructor"
&amp;&amp; key !== "prototype"
&amp;&amp; key !== "name"
) {
let desc = Object.getOwnPropertyDescriptor(source, key);
Object.defineProperty(target, key, desc);
}
}
}
上面代码的mix函数，可以将多个对象合成为一个类。使用的时候，只要继承这个类即可。
class DistributedEdit extends mix(Loggable, Serializable) {
// ...
}
19 修饰器
19.1 类的修饰
修饰器（Decorator）是一个函数，用来修改类的行为。这是ES7的一个提案，目前Babel转码器已经支持。
修饰器对类的行为的改变，是代码编译时发生的，而不是在运行时。这意味着，修饰器能在编译阶段运行代码。
function testable(target) {
target.isTestable = true;
}
@testable
class MyTestableClass {}
console.log(MyTestableClass.isTestable) // true
上面代码中，@testable就是一个修饰器。它修改了MyTestableClass这个类的行为，为它加上了静态属性isTestable。
基本上，修饰器的行为就是下面这样。
@decorator
class A {}
// 等同于
class A {}
A = decorator(A) || A;
也就是说，修饰器本质就是编译时执行的函数。
修饰器函数的第一个参数，就是所要修饰的目标类。
function testable(target) {
// ...
}
上面代码中，testable函数的参数target，就是会被修饰的类。
如果觉得一个参数不够用，可以在修饰器外面再封装一层函数。
function testable(isTestable) {
return function(target) {
target.isTestable = isTestable;
}
}
@testable(true)
class MyTestableClass {}
MyTestableClass.isTestable // true
@testable(false)
class MyClass {}
MyClass.isTestable // false
上面代码中，修饰器testable可以接受参数，这就等于可以修改修饰器的行为。
前面的例子是为类添加一个静态属性，如果想添加实例属性，可以通过目标类的prototype对象操作。
function testable(target) {
target.prototype.isTestable = true;
}
@testable
class MyTestableClass {}
let obj = new MyTestableClass();
obj.isTestable // true
上面代码中，修饰器函数testable是在目标类的prototype对象上添加属性，因此就可以在实例上调用。
下面是另外一个例子。
// mixins.js
export function mixins(...list) {
return function (target) {
Object.assign(target.prototype, ...list)
}
}
// main.js
import { mixins } from './mixins'
const Foo = {
foo() { console.log('foo') }
};
@mixins(Foo)
class MyClass {}
let obj = new MyClass();
obj.foo() // 'foo'
上面代码通过修饰器mixins，把Foo类的方法添加到了MyClass的实例上面。可以用Object.assign()模拟这个功能。
const Foo = {
foo() { console.log('foo') }
};
class MyClass {}
Object.assign(MyClass.prototype, Foo);
let obj = new MyClass();
obj.foo() // 'foo'
19.2 方法的修饰
修饰器不仅可以修饰类，还可以修饰类的属性。
class Person {
@readonly
name() { return `${this.first} ${this.last}` }
}
上面代码中，修饰器readonly用来修饰“类”的name方法。
此时，修饰器函数一共可以接受三个参数，第一个参数是所要修饰的目标对象，第二个参数是所要修饰的属性名，第三个参数是该属性的描述对象。
function readonly(target, name, descriptor){
// descriptor对象原来的值如下
// {
// value: specifiedFunction,
// enumerable: false,
// configurable: true,
// writable: true
// };
descriptor.writable = false;
return descriptor;
}
readonly(Person.prototype, 'name', descriptor);
// 类似于
Object.defineProperty(Person.prototype, 'name', descriptor);
上面代码说明，修饰器（readonly）会修改属性的描述对象（descriptor），然后被修改的描述对象再用来定义属性。
下面是另一个例子，修改属性描述对象的enumerable属性，使得该属性不可遍历。
class Person {
@nonenumerable
get kidCount() { return this.children.length; }
}
function nonenumerable(target, name, descriptor) {
descriptor.enumerable = false;
return descriptor;
}
下面的@log修饰器，可以起到输出日志的作用。
class Math {
@log
add(a, b) {
return a + b;
}
}
function log(target, name, descriptor) {
var oldValue = descriptor.value;
descriptor.value = function() {
console.log(`Calling "${name}" with`, arguments);
return oldValue.apply(null, arguments);
};
return descriptor;
}
const math = new Math();
// passed parameters should get logged now
math.add(2, 4);
上面代码中，@log修饰器的作用就是在执行原始的操作之前，执行一次console.log，从而达到输出日志的目的。
修饰器有注释的作用。
@testable
class Person {
@readonly
@nonenumerable
name() { return `${this.first} ${this.last}` }
}
从上面代码中，我们一眼就能看出，Person类是可测试的，而name方法是只读和不可枚举的。
如果同一个方法有多个修饰器，会像剥洋葱一样，先从外到内进入，然后由内向外执行。
function dec(id){
console.log('evaluated', id);
return (target, property, descriptor) =&gt; console.log('executed', id);
}
class Example {
@dec(1)
@dec(2)
method(){}
}
// evaluated 1
// evaluated 2
// executed 2
// executed 1
上面代码中，外层修饰器@dec(1)先进入，但是内层修饰器@dec(2)先执行。
除了注释，修饰器还能用来类型检查。所以，对于类来说，这项功能相当有用。从长期来看，它将是JavaScript代码静态分析的重要工具。
19.3 为什么修饰器不能用于函数？
修饰器只能用于类和类的方法，不能用于函数，因为存在函数提升。
var counter = 0;
var add = function () {
counter++;
};
@add
function foo() {
}
上面的代码，意图是执行后counter等于1，但是实际上结果是counter等于0。因为函数提升，使得实际执行的代码是下面这样。
var counter;
var add;
@add
function foo() {
}
counter = 0;
add = function () {
counter++;
};
下面是另一个例子。
var readOnly = require("some-decorator");
@readOnly
function foo() {
}
上面代码也有问题，因为实际执行是下面这样。
var readOnly;
@readOnly
function foo() {
}
readOnly = require("some-decorator");
总之，由于存在函数提升，使得修饰器不能用于函数。类是不会提升的，所以就没有这方面的问题。
19.4 core-decorators.js
core-decorators.js是一个第三方模块，提供了几个常见的修饰器，通过它可以更好地理解修饰器。
（1）@autobind
autobind修饰器使得方法中的this对象，绑定原始对象。
import { autobind } from 'core-decorators';
class Person {
@autobind
getPerson() {
return this;
}
}
let person = new Person();
let getPerson = person.getPerson;
getPerson() === person;
// true
（2）@readonly
readonly修饰器使得属性或方法不可写。
import { readonly } from 'core-decorators';
class Meal {
@readonly
entree = 'steak';
}
var dinner = new Meal();
dinner.entree = 'salmon';
// Cannot assign to read only property 'entree' of [object Object]
（3）@override
override修饰器检查子类的方法，是否正确覆盖了父类的同名方法，如果不正确会报错。
import { override } from 'core-decorators';
class Parent {
speak(first, second) {}
}
class Child extends Parent {
@override
speak() {}
// SyntaxError: Child#speak() does not properly override Parent#speak(first, second)
}
// or
class Child extends Parent {
@override
speaks() {}
// SyntaxError: No descriptor matching Child#speaks() was found on the prototype chain.
//
// Did you mean "speak"?
}
（4）@deprecate (别名@deprecated)
deprecate或deprecated修饰器在控制台显示一条警告，表示该方法将废除。
import { deprecate } from 'core-decorators';
class Person {
@deprecate
facepalm() {}
@deprecate('We stopped facepalming')
facepalmHard() {}
@deprecate('We stopped facepalming', { url: 'http://knowyourmeme.com/memes/facepalm' })
facepalmHarder() {}
}
let person = new Person();
person.facepalm();
// DEPRECATION Person#facepalm: This function will be removed in future versions.
person.facepalmHard();
// DEPRECATION Person#facepalmHard: We stopped facepalming
person.facepalmHarder();
// DEPRECATION Person#facepalmHarder: We stopped facepalming
//
// See http://knowyourmeme.com/memes/facepalm for more details.
//
（5）@suppressWarnings
suppressWarnings修饰器抑制decorated修饰器导致的console.warn()调用。但是，异步代码发出的调用除外。
import { suppressWarnings } from 'core-decorators';
class Person {
@deprecated
facepalm() {}
@suppressWarnings
facepalmWithoutWarning() {
this.facepalm();
}
}
let person = new Person();
person.facepalmWithoutWarning();
// no warning is logged
19.5 使用修饰器实现自动发布事件
我们可以使用修饰器，使得对象的方法被调用时，自动发出一个事件。
import postal from "postal/lib/postal.lodash";
export default function publish(topic, channel) {
return function(target, name, descriptor) {
const fn = descriptor.value;
descriptor.value = function() {
let value = fn.apply(this, arguments);
postal.channel(channel || target.channel || "/").publish(topic, value);
};
};
}
上面代码定义了一个名为publish的修饰器，它通过改写descriptor.value，使得原方法被调用时，会自动发出一个事件。它使用的事件“发布/订阅”库
是Postal.js。
它的用法如下。
import publish from "path/to/decorators/publish";
class FooComponent {
@publish("foo.some.message", "component")
someMethod() {
return {
my: "data"
};
}
@publish("foo.some.other")
anotherMethod() {
// ...
}
}
以后，只要调用someMethod或者anotherMethod，就会自动发出一个事件。
let foo = new FooComponent();
foo.someMethod() // 在"component"频道发布"foo.some.message"事件，附带的数据是{ my: "data" }
foo.anotherMethod() // 在"/"频道发布"foo.some.other"事件，不附带数据
19.6 Mixin
在修饰器的基础上，可以实现Mixin模式。所谓Mixin模式，就是对象继承的一种替代方案，中文译为“混入”（mix in），意为在一个对象之中混入另外
一个对象的方法。
请看下面的例子。
const Foo = {
foo() { console.log('foo') }
};
class MyClass {}
Object.assign(MyClass.prototype, Foo);
let obj = new MyClass();
obj.foo() // 'foo'
上面代码之中，对象Foo有一个foo方法，通过Object.assign方法，可以将foo方法“混入”MyClass类，导致MyClass的实例obj对象都具有foo方法。这
就是“混入”模式的一个简单实现。
下面，我们部署一个通用脚本mixins.js，将mixin写成一个修饰器。
export function mixins(...list) {
return function (target) {
Object.assign(target.prototype, ...list);
};
}
然后，就可以使用上面这个修饰器，为类“混入”各种方法。
import { mixins } from './mixins';
const Foo = {
foo() { console.log('foo') }
};
@mixins(Foo)
class MyClass {}
let obj = new MyClass();
obj.foo() // "foo"
通过mixins这个修饰器，实现了在MyClass类上面“混入”Foo对象的foo方法。
不过，上面的方法会改写MyClass类的prototype对象，如果不喜欢这一点，也可以通过类的继承实现mixin。
class MyClass extends MyBaseClass {
/* ... */
}
上面代码中，MyClass继承了MyBaseClass。如果我们想在MyClass里面“混入”一个foo方法，一个办法是在MyClass和MyBaseClass之间插入一个混入
类，这个类具有foo方法，并且继承了MyBaseClass的所有方法，然后MyClass再继承这个类。
let MyMixin = (superclass) =&gt; class extends superclass {
foo() {
console.log('foo from MyMixin');
}
};
上面代码中，MyMixin是一个混入类生成器，接受superclass作为参数，然后返回一个继承superclass的子类，该子类包含一个foo方法。
接着，目标类再去继承这个混入类，就达到了“混入”foo方法的目的。
class MyClass extends MyMixin(MyBaseClass) {
/* ... */
}
let c = new MyClass();
c.foo(); // "foo from MyMixin"
如果需要“混入”多个方法，就生成多个混入类。
class MyClass extends Mixin1(Mixin2(MyBaseClass)) {
/* ... */
}
这种写法的一个好处，是可以调用super，因此可以避免在“混入”过程中覆盖父类的同名方法。
let Mixin1 = (superclass) =&gt; class extends superclass {
foo() {
console.log('foo from Mixin1');
if (super.foo) super.foo();
}
};
let Mixin2 = (superclass) =&gt; class extends superclass {
foo() {
console.log('foo from Mixin2');
if (super.foo) super.foo();
}
};
class S {
foo() {
console.log('foo from S');
}
}
class C extends Mixin1(Mixin2(S)) {
foo() {
console.log('foo from C');
super.foo();
}
}
上面代码中，每一次混入发生时，都调用了父类的super.foo方法，导致父类的同名方法没有被覆盖，行为被保留了下来。
new C().foo()
// foo from C
// foo from Mixin1
// foo from Mixin2
// foo from S
19.7 Trait
Trait也是一种修饰器，效果与Mixin类似，但是提供更多功能，比如防止同名方法的冲突、排除混入某些方法、为混入的方法起别名等等。
下面采用traits-decorator这个第三方模块作为例子。这个模块提供的traits修饰器，不仅可以接受对象，还可以接受ES6类作为参数。
import { traits } from 'traits-decorator';
class TFoo {
foo() { console.log('foo') }
}
const TBar = {
bar() { console.log('bar') }
};
@traits(TFoo, TBar)
class MyClass { }
let obj = new MyClass();
obj.foo() // foo
obj.bar() // bar
上面代码中，通过traits修饰器，在MyClass类上面“混入”了TFoo类的foo方法和TBar对象的bar方法。
Trait不允许“混入”同名方法。
import { traits } from 'traits-decorator';
class TFoo {
foo() { console.log('foo') }
}
const TBar = {
bar() { console.log('bar') },
foo() { console.log('foo') }
};
@traits(TFoo, TBar)
class MyClass { }
// 报错
// throw new Error('Method named: ' + methodName + ' is defined twice.');
// ^
// Error: Method named: foo is defined twice.
上面代码中，TFoo和TBar都有foo方法，结果traits修饰器报错。
一种解决方法是排除TBar的foo方法。
import { traits, excludes } from 'traits-decorator';
class TFoo {
foo() { console.log('foo') }
}
const TBar = {
bar() { console.log('bar') },
foo() { console.log('foo') }
};
@traits(TFoo, TBar::excludes('foo'))
class MyClass { }
let obj = new MyClass();
obj.foo() // foo
obj.bar() // bar
上面代码使用绑定运算符（::）在TBar上排除foo方法，混入时就不会报错了。
另一种方法是为TBar的foo方法起一个别名。
import { traits, alias } from 'traits-decorator';
class TFoo {
foo() { console.log('foo') }
}
const TBar = {
bar() { console.log('bar') },
foo() { console.log('foo') }
};
@traits(TFoo, TBar::alias({foo: 'aliasFoo'}))
class MyClass { }
let obj = new MyClass();
obj.foo() // foo
obj.aliasFoo() // foo
obj.bar() // bar
上面代码为TBar的foo方法起了别名aliasFoo，于是MyClass也可以混入TBar的foo方法了。
alias和excludes方法，可以结合起来使用。
@traits(TExample::excludes('foo','bar')::alias({baz:'exampleBaz'}))
class MyClass {}
上面代码排除了TExample的foo方法和bar方法，为baz方法起了别名exampleBaz。
as方法则为上面的代码提供了另一种写法。
@traits(TExample::as({excludes:['foo', 'bar'], alias: {baz: 'exampleBaz'}}))
class MyClass {}
19.8 Babel转码器的支持
目前，Babel转码器已经支持Decorator。
首先，安装babel-core和babel-plugin-transform-decorators。由于后者包括在babel-preset-stage-0之中，所以改为安
装babel-preset-stage-0亦可。
$ npm install babel-core babel-plugin-transform-decorators
然后，设置配置文件.babelrc。
{
"plugins": ["transform-decorators"]
}
这时，Babel就可以对Decorator转码了。
脚本中打开的命令如下。
babel.transform("code", {plugins: ["transform-decorators"]})
Babel的官方网站提供一个在线转码器，只要勾选Experimental，就能支持Decorator的在线转码。
20 Module
ES6的Class只是面向对象编程的语法糖，升级了ES5的构造函数的原型链继承的写法，并没有解决模块化问题。Module功能就是为了解决这个问题而
提出的。
历史上，JavaScript一直没有模块（module）体系，无法将一个大程序拆分成互相依赖的小文件，再用简单的方法拼装起来。其他语言都有这项功能，
比如Ruby的require、Python的import，甚至就连CSS都有@import，但是JavaScript任何这方面的支持都没有，这对开发大型的、复杂的项目形成了
巨大障碍。
在ES6之前，社区制定了一些模块加载方案，最主要的有CommonJS和AMD两种。前者用于服务器，后者用于浏览器。ES6在语言规格的层面上，实现
了模块功能，而且实现得相当简单，完全可以取代现有的CommonJS和AMD规范，成为浏览器和服务器通用的模块解决方案。
ES6模块的设计思想，是尽量的静态化，使得编译时就能确定模块的依赖关系，以及输入和输出的变量。CommonJS和AMD模块，都只能在运行时确
定这些东西。比如，CommonJS模块就是对象，输入时必须查找对象属性。
// CommonJS模块
let { stat, exists, readFile } = require('fs');
// 等同于
let _fs = require('fs');
let stat = _fs.stat, exists = _fs.exists, readfile = _fs.readfile;
上面代码的实质是整体加载fs模块（即加载fs的所有方法），生成一个对象（_fs），然后再从这个对象上面读取3个方法。这种加载称为“运行时加
载”，因为只有运行时才能得到这个对象，导致完全没办法在编译时做“静态优化”。
ES6模块不是对象，而是通过export命令显式指定输出的代码，输入时也采用静态命令的形式。
// ES6模块
import { stat, exists, readFile } from 'fs';
上面代码的实质是从fs模块加载3个方法，其他方法不加载。这种加载称为“编译时加载”，即ES6可以在编译时就完成模块加载，效率要比CommonJS
模块的加载方式高。当然，这也导致了没法引用ES6模块本身，因为它不是对象。
由于ES6模块是编译时加载，使得静态分析成为可能。有了它，就能进一步拓宽JavaScript的语法，比如引入宏（macro）和类型检验（type system）
这些只能靠静态分析实现的功能。
除了静态加载带来的各种好处，ES6模块还有以下好处。
不再需要UMD模块格式了，将来服务器和浏览器都会支持ES6模块格式。目前，通过各种工具库，其实已经做到了这一点。
将来浏览器的新API就能用模块格式提供，不再必要做成全局变量或者navigator对象的属性。
不再需要对象作为命名空间（比如Math对象），未来这些功能可以通过模块提供。
浏览器使用ES6模块的语法如下。
&lt;script type="module" src="foo.js"&gt;&lt;/script&gt;
上面代码在网页中插入一个模块foo.js，由于type属性设为module，所以浏览器知道这是一个ES6模块。
Node的默认模块格式是CommonJS，目前还没决定怎么支持ES6模块。所以，只能通过Babel这样的转码器，在Node里面使用ES6模块。
20.1 严格模式
ES6的模块自动采用严格模式，不管你有没有在模块头部加上"use strict";。
严格模式主要有以下限制。
变量必须声明后再使用
函数的参数不能有同名属性，否则报错
不能使用with语句
不能对只读属性赋值，否则报错
不能使用前缀0表示八进制数，否则报错
不能删除不可删除的属性，否则报错
不能删除变量delete prop，会报错，只能删除属性delete global[prop]
eval不会在它的外层作用域引入变量
eval和arguments不能被重新赋值
arguments不会自动反映函数参数的变化
不能使用arguments.callee
不能使用arguments.caller
禁止this指向全局对象
不能使用fn.caller和fn.arguments获取函数调用的堆栈
增加了保留字（比如protected、static和interface）
上面这些限制，模块都必须遵守。由于严格模式是ES5引入的，不属于ES6，所以请参阅相关ES5书籍，本书不再详细介绍了。
20.2 export命令
模块功能主要由两个命令构成：export和import。export命令用于规定模块的对外接口，import命令用于输入其他模块提供的功能。
一个模块就是一个独立的文件。该文件内部的所有变量，外部无法获取。如果你希望外部能够读取模块内部的某个变量，就必须使用export关键字输
出该变量。下面是一个JS文件，里面使用export命令输出变量。
// profile.js
export var firstName = 'Michael';
export var lastName = 'Jackson';
export var year = 1958;
上面代码是profile.js文件，保存了用户信息。ES6将其视为一个模块，里面用export命令对外部输出了三个变量。
export的写法，除了像上面这样，还有另外一种。
// profile.js
var firstName = 'Michael';
var lastName = 'Jackson';
var year = 1958;
export {firstName, lastName, year};
上面代码在export命令后面，使用大括号指定所要输出的一组变量。它与前一种写法（直接放置在var语句前）是等价的，但是应该优先考虑使用这种
写法。因为这样就可以在脚本尾部，一眼看清楚输出了哪些变量。
export命令除了输出变量，还可以输出函数或类（class）。
export function multiply(x, y) {
return x * y;
};
上面代码对外输出一个函数multiply。
通常情况下，export输出的变量就是本来的名字，但是可以使用as关键字重命名。
function v1() { ... }
function v2() { ... }
export {
v1 as streamV1,
v2 as streamV2,
v2 as streamLatestVersion
};
上面代码使用as关键字，重命名了函数v1和v2的对外接口。重命名后，v2可以用不同的名字输出两次。
需要特别注意的是，export命令规定的是对外的接口，必须与模块内部的变量建立一一对应关系。
// 报错
export 1;
// 报错
var m = 1;
export m;
上面两种写法都会报错，因为没有提供对外的接口。第一种写法直接输出1，第二种写法通过变量m，还是直接输出1。1只是一个值，不是接口。正确
的写法是下面这样。
// 写法一
export var m = 1;
// 写法二
var m = 1;
export {m};
// 写法三
var n = 1;
export {n as m};
上面三种写法都是正确的，规定了对外的接口m。其他脚本可以通过这个接口，取到值1。它们的实质是，在接口名与模块内部变量之间，建立了一一
对应的关系。
同样的，function和class的输出，也必须遵守这样的写法。
// 报错
function f() {}
export f;
// 正确
export function f() {};
// 正确
function f() {}
export {f};
另外，export语句输出的接口，与其对应的值是动态绑定关系，即通过该接口，可以取到模块内部实时的值。
export var foo = 'bar';
setTimeout(() =&gt; foo = 'baz', 500);
上面代码输出变量foo，值为bar，500毫秒之后变成baz。
这一点与CommonJS规范完全不同。CommonJS模块输出的是值的缓存，不存在动态更新，详见下文《ES6模块加载的实质》一节。
最后，export命令可以出现在模块的任何位置，只要处于模块顶层就可以。如果处于块级作用域内，就会报错，下一节的import命令也是如此。这是
因为处于条件代码块之中，就没法做静态优化了，违背了ES6模块的设计初衷。
function foo() {
export default 'bar' // SyntaxError
}
foo()
上面代码中，export语句放在函数之中，结果报错。
20.3 import命令
使用export命令定义了模块的对外接口以后，其他JS文件就可以通过import命令加载这个模块（文件）。
// main.js
import {firstName, lastName, year} from './profile';
function setName(element) {
element.textContent = firstName + ' ' + lastName;
}
上面代码的import命令，就用于加载profile.js文件，并从中输入变量。import命令接受一个对象（用大括号表示），里面指定要从其他模块导入的
变量名。大括号里面的变量名，必须与被导入模块（profile.js）对外接口的名称相同。
如果想为输入的变量重新取一个名字，import命令要使用as关键字，将输入的变量重命名。
import { lastName as surname } from './profile';
注意，import命令具有提升效果，会提升到整个模块的头部，首先执行。
foo();
import { foo } from 'my_module';
上面的代码不会报错，因为import的执行早于foo的调用。
如果在一个模块之中，先输入后输出同一个模块，import语句可以与export语句写在一起。
export { es6 as default } from './someModule';
// 等同于
import { es6 } from './someModule';
export default es6;
上面代码中，export和import语句可以结合在一起，写成一行。但是从可读性考虑，不建议采用这种写法，而应该采用标准写法。
另外，ES7有一个提案，简化先输入后输出的写法，拿掉输出时的大括号。
// 提案的写法
export v from 'mod';
// 现行的写法
export {v} from 'mod';
import语句会执行所加载的模块，因此可以有下面的写法。
import 'lodash';
上面代码仅仅执行lodash模块，但是不输入任何值。
20.4 模块的整体加载
除了指定加载某个输出值，还可以使用整体加载，即用星号（*）指定一个对象，所有输出值都加载在这个对象上面。
下面是一个circle.js文件，它输出两个方法area和circumference。
// circle.js
export function area(radius) {
return Math.PI * radius * radius;
}
export function circumference(radius) {
return 2 * Math.PI * radius;
}
现在，加载这个模块。
// main.js
import { area, circumference } from './circle';
console.log('圆面积：' + area(4));
console.log('圆周长：' + circumference(14));
上面写法是逐一指定要加载的方法，整体加载的写法如下。
import * as circle from './circle';
console.log('圆面积：' + circle.area(4));
console.log('圆周长：' + circle.circumference(14));
20.5 export default命令
从前面的例子可以看出，使用import命令的时候，用户需要知道所要加载的变量名或函数名，否则无法加载。但是，用户肯定希望快速上手，未必愿
意阅读文档，去了解模块有哪些属性和方法。
为了给用户提供方便，让他们不用阅读文档就能加载模块，就要用到export default命令，为模块指定默认输出。
// export-default.js
export default function () {
console.log('foo');
}
上面代码是一个模块文件export-default.js，它的默认输出是一个函数。
其他模块加载该模块时，import命令可以为该匿名函数指定任意名字。
// import-default.js
import customName from './export-default';
customName(); // 'foo'
上面代码的import命令，可以用任意名称指向export-default.js输出的方法，这时就不需要知道原模块输出的函数名。需要注意的是，这时import命
令后面，不使用大括号。
export default命令用在非匿名函数前，也是可以的。
// export-default.js
export default function foo() {
console.log('foo');
}
// 或者写成
function foo() {
console.log('foo');
}
export default foo;
上面代码中，foo函数的函数名foo，在模块外部是无效的。加载的时候，视同匿名函数加载。
下面比较一下默认输出和正常输出。
// 输出
export default function crc32() {
// ...
}
// 输入
import crc32 from 'crc32';
// 输出
export function crc32() {
// ...
};
// 输入
import {crc32} from 'crc32';
上面代码的两组写法，第一组是使用export default时，对应的import语句不需要使用大括号；第二组是不使用export default时，对应的import语
句需要使用大括号。
export default命令用于指定模块的默认输出。显然，一个模块只能有一个默认输出，因此export deault命令只能使用一次。所以，import命令后面
才不用加大括号，因为只可能对应一个方法。
本质上，export default就是输出一个叫做default的变量或方法，然后系统允许你为它取任意名字。所以，下面的写法是有效的。
// modules.js
function add(x, y) {
return x * y;
}
export {add as default};
// 等同于
// export default add;
// app.js
import { default as xxx } from 'modules';
// 等同于
// import xxx from 'modules';
正是因为export default命令其实只是输出一个叫做default的变量，所以它后面不能跟变量声明语句。
// 正确
export var a = 1;
// 正确
var a = 1;
export default a;
// 错误
export default var a = 1;
上面代码中，export default a的含义是将变量a的值赋给变量default。所以，最后一种写法会报错。
有了export default命令，输入模块时就非常直观了，以输入jQuery模块为例。
import $ from 'jquery';
如果想在一条import语句中，同时输入默认方法和其他变量，可以写成下面这样。
import customName, { otherMethod } from './export-default';
如果要输出默认的值，只需将值跟在export default之后即可。
export default 42;
export default也可以用来输出类。
// MyClass.js
export default class { ... }
// main.js
import MyClass from 'MyClass';
let o = new MyClass();
20.6 模块的继承
模块之间也可以继承。
假设有一个circleplus模块，继承了circle模块。
// circleplus.js
export * from 'circle';
export var e = 2.71828182846;
export default function(x) {
return Math.exp(x);
}
上面代码中的export *，表示再输出circle模块的所有属性和方法。注意，export *命令会忽略circle模块的default方法。然后，上面代码又输出
了自定义的e变量和默认方法。
这时，也可以将circle的属性或方法，改名后再输出。
// circleplus.js
export { area as circleArea } from 'circle';
上面代码表示，只输出circle模块的area方法，且将其改名为circleArea。
加载上面模块的写法如下。
// main.js
import * as math from 'circleplus';
import exp from 'circleplus';
console.log(exp(math.e));
上面代码中的import exp表示，将circleplus模块的默认方法加载为exp方法。
20.7 ES6模块加载的实质
ES6模块加载的机制，与CommonJS模块完全不同。CommonJS模块输出的是一个值的拷贝，而ES6模块输出的是值的引用。
CommonJS模块输出的是被输出值的拷贝，也就是说，一旦输出一个值，模块内部的变化就影响不到这个值。请看下面这个模块文件lib.js的例子。
// lib.js
var counter = 3;
function incCounter() {
counter++;
}
module.exports = {
counter: counter,
incCounter: incCounter,
};
上面代码输出内部变量counter和改写这个变量的内部方法incCounter。然后，在main.js里面加载这个模块。
// main.js
var mod = require('./lib');
console.log(mod.counter); // 3
mod.incCounter();
console.log(mod.counter); // 3
上面代码说明，lib.js模块加载以后，它的内部变化就影响不到输出的mod.counter了。这是因为mod.counter是一个原始类型的值，会被缓存。除非
写成一个函数，才能得到内部变动后的值。
// lib.js
var counter = 3;
function incCounter() {
counter++;
}
module.exports = {
get counter() {
return counter
},
incCounter: incCounter,
};
上面代码中，输出的counter属性实际上是一个取值器函数。现在再执行main.js，就可以正确读取内部变量counter的变动了。
$ node main.js
3
4
ES6模块的运行机制与CommonJS不一样，它遇到模块加载命令import时，不会去执行模块，而是只生成一个动态的只读引用。等到真的需要用到
时，再到模块里面去取值，换句话说，ES6的输入有点像Unix系统的“符号连接”，原始值变了，import输入的值也会跟着变。因此，ES6模块是动态引
用，并且不会缓存值，模块里面的变量绑定其所在的模块。
还是举上面的例子。
// lib.js
export let counter = 3;
export function incCounter() {
counter++;
}
// main.js
import { counter, incCounter } from './lib';
console.log(counter); // 3
incCounter();
console.log(counter); // 4
上面代码说明，ES6模块输入的变量counter是活的，完全反应其所在模块lib.js内部的变化。
再举一个出现在export一节中的例子。
// m1.js
export var foo = 'bar';
setTimeout(() =&gt; foo = 'baz', 500);
// m2.js
import {foo} from './m1.js';
console.log(foo);
setTimeout(() =&gt; console.log(foo), 500);
上面代码中，m1.js的变量foo，在刚加载时等于bar，过了500毫秒，又变为等于baz。
让我们看看，m2.js能否正确读取这个变化。
$ babel-node m2.js
bar
baz
上面代码表明，ES6模块不会缓存运行结果，而是动态地去被加载的模块取值，并且变量总是绑定其所在的模块。
由于ES6输入的模块变量，只是一个“符号连接”，所以这个变量是只读的，对它进行重新赋值会报错。
// lib.js
export let obj = {};
// main.js
import { obj } from './lib';
obj.prop = 123; // OK
obj = {}; // TypeError
上面代码中，main.js从lib.js输入变量obj，可以对obj添加属性，但是重新赋值就会报错。因为变量obj指向的地址是只读的，不能重新赋值，这就
好比main.js创造了一个名为obj的const变量。
最后，export通过接口，输出的是同一个值。不同的脚本加载这个接口，得到的都是同样的实例。
// mod.js
function C() {
this.sum = 0;
this.add = function () {
this.sum += 1;
};
this.show = function () {
console.log(this.sum);
};
}
export let c = new C();
上面的脚本mod.js，输出的是一个C的实例。不同的脚本加载这个模块，得到的都是同一个实例。
// x.js
import {c} from './mod';
c.add();
// y.js
import {c} from './mod';
c.show();
// main.js
import './x';
import './y';
现在执行main.js，输出的是1。
$ babel-node main.js
1
这就证明了x.js和y.js加载的都是C的同一个实例。
20.8 循环加载
“循环加载”（circular dependency）指的是，a脚本的执行依赖b脚本，而b脚本的执行又依赖a脚本。
// a.js
var b = require('b');
// b.js
var a = require('a');
通常，“循环加载”表示存在强耦合，如果处理不好，还可能导致递归加载，使得程序无法执行，因此应该避免出现。
但是实际上，这是很难避免的，尤其是依赖关系复杂的大项目，很容易出现a依赖b，b依赖c，c又依赖a这样的情况。这意味着，模块加载机制必须考
虑“循环加载”的情况。
对于JavaScript语言来说，目前最常见的两种模块格式CommonJS和ES6，处理“循环加载”的方法是不一样的，返回的结果也不一样。
20.8.1 CommonJS模块的加载原理
介绍ES6如何处理"循环加载"之前，先介绍目前最流行的CommonJS模块格式的加载原理。
CommonJS的一个模块，就是一个脚本文件。require命令第一次加载该脚本，就会执行整个脚本，然后在内存生成一个对象。
{
id: '...',
exports: { ... },
loaded: true,
...
}
上面代码就是Node内部加载模块后生成的一个对象。该对象的id属性是模块名，exports属性是模块输出的各个接口，loaded属性是一个布尔值，表
示该模块的脚本是否执行完毕。其他还有很多属性，这里都省略了。
以后需要用到这个模块的时候，就会到exports属性上面取值。即使再次执行require命令，也不会再次执行该模块，而是到缓存之中取值。也就是
说，CommonJS模块无论加载多少次，都只会在第一次加载时运行一次，以后再加载，就返回第一次运行的结果，除非手动清除系统缓存。
20.8.2 CommonJS模块的循环加载
CommonJS模块的重要特性是加载时执行，即脚本代码在require的时候，就会全部执行。一旦出现某个模块被"循环加载"，就只输出已经执行的部
分，还未执行的部分不会输出。
让我们来看，Node官方文档里面的例子。脚本文件a.js代码如下。
exports.done = false;
var b = require('./b.js');
console.log('在 a.js 之中，b.done = %j', b.done);
exports.done = true;
console.log('a.js 执行完毕');
上面代码之中，a.js脚本先输出一个done变量，然后加载另一个脚本文件b.js。注意，此时a.js代码就停在这里，等待b.js执行完毕，再往下执行。
再看b.js的代码。
exports.done = false;
var a = require('./a.js');
console.log('在 b.js 之中，a.done = %j', a.done);
exports.done = true;
console.log('b.js 执行完毕');
上面代码之中，b.js执行到第二行，就会去加载a.js，这时，就发生了“循环加载”。系统会去a.js模块对应对象的exports属性取值，可是因为a.js还
没有执行完，从exports属性只能取回已经执行的部分，而不是最后的值。
a.js已经执行的部分，只有一行。
exports.done = false;
因此，对于b.js来说，它从a.js只输入一个变量done，值为false。
然后，b.js接着往下执行，等到全部执行完毕，再把执行权交还给a.js。于是，a.js接着往下执行，直到执行完毕。我们写一个脚本main.js，验证
这个过程。
var a = require('./a.js');
var b = require('./b.js');
console.log('在 main.js 之中, a.done=%j, b.done=%j', a.done, b.done);
执行main.js，运行结果如下。
$ node main.js
在 b.js 之中，a.done = false
b.js 执行完毕
在 a.js 之中，b.done = true
a.js 执行完毕
在 main.js 之中, a.done=true, b.done=true
上面的代码证明了两件事。一是，在b.js之中，a.js没有执行完毕，只执行了第一行。二是，main.js执行到第二行时，不会再次执行b.js，而是输
出缓存的b.js的执行结果，即它的第四行。
exports.done = true;
总之，CommonJS输入的是被输出值的拷贝，不是引用。
另外，由于CommonJS模块遇到循环加载时，返回的是当前已经执行的部分的值，而不是代码全部执行后的值，两者可能会有差异。所以，输入变量
的时候，必须非常小心。
var a = require('a'); // 安全的写法
var foo = require('a').foo; // 危险的写法
exports.good = function (arg) {
return a.foo('good', arg); // 使用的是 a.foo 的最新值
};
exports.bad = function (arg) {
return foo('bad', arg); // 使用的是一个部分加载时的值
};
上面代码中，如果发生循环加载，require('a').foo的值很可能后面会被改写，改用require('a')会更保险一点。
20.8.3 ES6模块的循环加载
ES6处理“循环加载”与CommonJS有本质的不同。ES6模块是动态引用，如果使用import从一个模块加载变量（即import foo from 'foo'），那些变
量不会被缓存，而是成为一个指向被加载模块的引用，需要开发者自己保证，真正取值的时候能够取到值。
请看下面这个例子。
// a.js如下
import {bar} from './b.js';
console.log('a.js');
console.log(bar);
export let foo = 'foo';
// b.js
import {foo} from './a.js';
console.log('b.js');
console.log(foo);
export let bar = 'bar';
上面代码中，a.js加载b.js，b.js又加载a.js，构成循环加载。执行a.js，结果如下。
$ babel-node a.js
b.js
undefined
a.js
bar
上面代码中，由于a.js的第一行是加载b.js，所以先执行的是b.js。而b.js的第一行又是加载a.js，这时由于a.js已经开始执行了，所以不会重复执
行，而是继续往下执行b.js，所以第一行输出的是b.js。
接着，b.js要打印变量foo，这时a.js还没执行完，取不到foo的值，导致打印出来是undefined。b.js执行完，开始执行a.js，这时就一切正常了。
再看一个稍微复杂的例子（摘自 Dr. Axel Rauschmayer 的《Exploring ES6》）。
// a.js
import {bar} from './b.js';
export function foo() {
console.log('foo');
bar();
console.log('执行完毕');
}
foo();
// b.js
import {foo} from './a.js';
export function bar() {
console.log('bar');
if (Math.random() &gt; 0.5) {
foo();
}
}
按照CommonJS规范，上面的代码是没法执行的。a先加载b，然后b又加载a，这时a还没有任何执行结果，所以输出结果为null，即对于b.js来说，
变量foo的值等于null，后面的foo()就会报错。
但是，ES6可以执行上面的代码。
$ babel-node a.js
foo
bar
执行完毕
// 执行结果也有可能是
foo
bar
foo
bar
执行完毕
执行完毕
上面代码中，a.js之所以能够执行，原因就在于ES6加载的变量，都是动态引用其所在的模块。只要引用存在，代码就能执行。
下面，我们详细分析这段代码的运行过程。
// a.js
// 这一行建立一个引用，
// 从`b.js`引用`bar`
import {bar} from './b.js';
export function foo() {
// 执行时第一行输出 foo
console.log('foo');
// 到 b.js 执行 bar
bar();
console.log('执行完毕');
}
foo();
// b.js
// 建立`a.js`的`foo`引用
import {foo} from './a.js';
export function bar() {
// 执行时，第二行输出 bar
console.log('bar');
// 递归执行 foo，一旦随机数
// 小于等于0.5，就停止执行
if (Math.random() &gt; 0.5) {
foo();
}
}
我们再来看ES6模块加载器SystemJS给出的一个例子。
// even.js
import { odd } from './odd'
export var counter = 0;
export function even(n) {
counter++;
return n == 0 || odd(n - 1);
}
// odd.js
import { even } from './even';
export function odd(n) {
return n != 0 &amp;&amp; even(n - 1);
}
上面代码中，even.js里面的函数even有一个参数n，只要不等于0，就会减去1，传入加载的odd()。odd.js也会做类似操作。
运行上面这段代码，结果如下。
$ babel-node
&gt; import * as m from './even.js';
&gt; m.even(10);
true
&gt; m.counter
6
&gt; m.even(20)
true
&gt; m.counter
17
上面代码中，参数n从10变为0的过程中，even()一共会执行6次，所以变量counter等于6。第二次调用even()时，参数n从20变为0，even()一共会执
行11次，加上前面的6次，所以变量counter等于17。
这个例子要是改写成CommonJS，就根本无法执行，会报错。
// even.js
var odd = require('./odd');
var counter = 0;
exports.counter = counter;
exports.even = function(n) {
counter++;
return n == 0 || odd(n - 1);
}
// odd.js
var even = require('./even').even;
module.exports = function(n) {
return n != 0 &amp;&amp; even(n - 1);
}
上面代码中，even.js加载odd.js，而odd.js又去加载even.js，形成“循环加载”。这时，执行引擎就会输出even.js已经执行的部分（不存在任何结
果），所以在odd.js之中，变量even等于null，等到后面调用even(n-1)就会报错。
$ node
&gt; var m = require('./even');
&gt; m.even(10)
TypeError: even is not a function
20.9 跨模块常量
上面说过，const声明的常量只在当前代码块有效。如果想设置跨模块的常量（即跨多个文件），可以采用下面的写法。
// constants.js 模块
export const A = 1;
export const B = 3;
export const C = 4;
// test1.js 模块
import * as constants from './constants';
console.log(constants.A); // 1
console.log(constants.B); // 3
// test2.js 模块
import {A, B} from './constants';
console.log(A); // 1
console.log(B); // 3
20.10 ES6模块的转码
浏览器目前还不支持ES6模块，为了现在就能使用，可以将转为ES5的写法。除了Babel可以用来转码之外，还有以下两个方法，也可以用来转码。
20.10.1 ES6 module transpiler
ES6 module transpiler是square公司开源的一个转码器，可以将ES6模块转为CommonJS模块或AMD模块的写法，从而在浏览器中使用。
首先，安装这个转玛器。
$ npm install -g es6-module-transpiler
然后，使用compile-modules convert命令，将ES6模块文件转码。
$ compile-modules convert file1.js file2.js
-o参数可以指定转码后的文件名。
$ compile-modules convert -o out.js file1.js
20.10.2 SystemJS
另一种解决方法是使用SystemJS。它是一个垫片库（polyfill），可以在浏览器内加载ES6模块、AMD模块和CommonJS模块，将其转为ES5格式。它
在后台调用的是Google的Traceur转码器。
使用时，先在网页内载入system.js文件。
&lt;script src="system.js"&gt;&lt;/script&gt;
然后，使用System.import方法加载模块文件。
&lt;script&gt;
System.import('./app.js');
&lt;/script&gt;
上面代码中的./app，指的是当前目录下的app.js文件。它可以是ES6模块文件，System.import会自动将其转码。
需要注意的是，System.import使用异步加载，返回一个Promise对象，可以针对这个对象编程。下面是一个模块文件。
// app/es6-file.js:
export class q {
constructor() {
this.es6 = 'hello';
}
}
然后，在网页内加载这个模块文件。
&lt;script&gt;
System.import('app/es6-file').then(function(m) {
console.log(new m.q().es6); // hello
});
&lt;/script&gt;
上面代码中，System.import方法返回的是一个Promise对象，所以可以用then方法指定回调函数。
21 编程风格
本章探讨如何将ES6的新语法，运用到编码实践之中，与传统的JavaScript语法结合在一起，写出合理的、易于阅读和维护的代码。
多家公司和组织已经公开了它们的风格规范，具体可参阅jscs.info，下面的内容主要参考了Airbnb的JavaScript风格规范。
21.1 块级作用域
（1）let取代var
ES6提出了两个新的声明变量的命令：let和const。其中，let完全可以取代var，因为两者语义相同，而且let没有副作用。
'use strict';
if (true) {
let x = 'hello';
}
for (let i = 0; i &lt; 10; i++) {
console.log(i);
}
上面代码如果用var替代let，实际上就声明了两个全局变量，这显然不是本意。变量应该只在其声明的代码块内有效，var命令做不到这一点。
var命令存在变量提升效用，let命令没有这个问题。
'use strict';
if(true) {
console.log(x); // ReferenceError
let x = 'hello';
}
上面代码如果使用var替代let，console.log那一行就不会报错，而是会输出undefined，因为变量声明提升到代码块的头部。这违反了变量先声明后
使用的原则。
所以，建议不再使用var命令，而是使用let命令取代。
（2）全局常量和线程安全
在let和const之间，建议优先使用const，尤其是在全局环境，不应该设置变量，只应设置常量。这符合函数式编程思想，有利于将来的分布式运算。
// bad
var a = 1, b = 2, c = 3;
// good
const a = 1;
const b = 2;
const c = 3;
// best
const [a, b, c] = [1, 2, 3];
const声明常量还有两个好处，一是阅读代码的人立刻会意识到不应该修改这个值，二是防止了无意间修改变量值所导致的错误。
所有的函数都应该设置为常量。
长远来看，JavaScript可能会有多线程的实现（比如Intel的River Trail那一类的项目），这时let表示的变量，只应出现在单线程运行的代码中，不能是
多线程共享的，这样有利于保证线程安全。
21.2 字符串
静态字符串一律使用单引号或反引号，不使用双引号。动态字符串使用反引号。
// bad
const a = "foobar";
const b = 'foo' + a + 'bar';
// acceptable
const c = `foobar`;
// good
const a = 'foobar';
const b = `foo${a}bar`;
const c = 'foobar';
21.3 解构赋值
使用数组成员对变量赋值时，优先使用解构赋值。
const arr = [1, 2, 3, 4];
// bad
const first = arr[0];
const second = arr[1];
// good
const [first, second] = arr;
函数的参数如果是对象的成员，优先使用解构赋值。
// bad
function getFullName(user) {
const firstName = user.firstName;
const lastName = user.lastName;
}
// good
function getFullName(obj) {
const { firstName, lastName } = obj;
}
// best
function getFullName({ firstName, lastName }) {
}
如果函数返回多个值，优先使用对象的解构赋值，而不是数组的解构赋值。这样便于以后添加返回值，以及更改返回值的顺序。
// bad
function processInput(input) {
return [left, right, top, bottom];
}
// good
function processInput(input) {
return { left, right, top, bottom };
}
const { left, right } = processInput(input);
21.4 对象
单行定义的对象，最后一个成员不以逗号结尾。多行定义的对象，最后一个成员以逗号结尾。
// bad
const a = { k1: v1, k2: v2, };
const b = {
k1: v1,
k2: v2
};
// good
const a = { k1: v1, k2: v2 };
const b = {
k1: v1,
k2: v2,
};
对象尽量静态化，一旦定义，就不得随意添加新的属性。如果添加属性不可避免，要使用Object.assign方法。
// bad
const a = {};
a.x = 3;
// if reshape unavoidable
const a = {};
Object.assign(a, { x: 3 });
// good
const a = { x: null };
a.x = 3;
如果对象的属性名是动态的，可以在创造对象的时候，使用属性表达式定义。
// bad
const obj = {
id: 5,
name: 'San Francisco',
};
obj[getKey('enabled')] = true;
// good
const obj = {
id: 5,
name: 'San Francisco',
[getKey('enabled')]: true,
};
上面代码中，对象obj的最后一个属性名，需要计算得到。这时最好采用属性表达式，在新建obj的时候，将该属性与其他属性定义在一起。这样一
来，所有属性就在一个地方定义了。
另外，对象的属性和方法，尽量采用简洁表达法，这样易于描述和书写。
var ref = 'some value';
// bad
const atom = {
ref: ref,
value: 1,
addValue: function (value) {
return atom.value + value;
},
};
// good
const atom = {
ref,
value: 1,
addValue(value) {
return atom.value + value;
},
};
21.5 数组
使用扩展运算符（...）拷贝数组。
// bad
const len = items.length;
const itemsCopy = [];
let i;
for (i = 0; i &lt; len; i++) {
itemsCopy[i] = items[i];
}
// good
const itemsCopy = [...items];
使用Array.from方法，将类似数组的对象转为数组。
const foo = document.querySelectorAll('.foo');
const nodes = Array.from(foo);
21.6 函数
立即执行函数可以写成箭头函数的形式。
(() =&gt; {
console.log('Welcome to the Internet.');
})();
那些需要使用函数表达式的场合，尽量用箭头函数代替。因为这样更简洁，而且绑定了this。
// bad
[1, 2, 3].map(function (x) {
return x * x;
});
// good
[1, 2, 3].map((x) =&gt; {
return x * x;
});
// best
[1, 2, 3].map(x =&gt; x * x);
箭头函数取代Function.prototype.bind，不应再用self/_this/that绑定 this。
// bad
const self = this;
const boundMethod = function(...params) {
return method.apply(self, params);
}
// acceptable
const boundMethod = method.bind(this);
// best
const boundMethod = (...params) =&gt; method.apply(this, params);
简单的、单行的、不会复用的函数，建议采用箭头函数。如果函数体较为复杂，行数较多，还是应该采用传统的函数写法。
所有配置项都应该集中在一个对象，放在最后一个参数，布尔值不可以直接作为参数。
// bad
function divide(a, b, option = false ) {
}
// good
function divide(a, b, { option = false } = {}) {
}
不要在函数体内使用arguments变量，使用rest运算符（...）代替。因为rest运算符显式表明你想要获取参数，而且arguments是一个类似数组的对象，
而rest运算符可以提供一个真正的数组。
// bad
function concatenateAll() {
const args = Array.prototype.slice.call(arguments);
return args.join('');
}
// good
function concatenateAll(...args) {
return args.join('');
}
使用默认值语法设置函数参数的默认值。
// bad
function handleThings(opts) {
opts = opts || {};
}
// good
function handleThings(opts = {}) {
// ...
}
21.7 Map结构
注意区分Object和Map，只有模拟现实世界的实体对象时，才使用Object。如果只是需要key: value的数据结构，使用Map结构。因为Map有内建的遍
历机制。
let map = new Map(arr);
for (let key of map.keys()) {
console.log(key);
}
for (let value of map.values()) {
console.log(value);
}
for (let item of map.entries()) {
console.log(item[0], item[1]);
}
21.8 Class
总是用Class，取代需要prototype的操作。因为Class的写法更简洁，更易于理解。
// bad
function Queue(contents = []) {
this._queue = [...contents];
}
Queue.prototype.pop = function() {
const value = this._queue[0];
this._queue.splice(0, 1);
return value;
}
// good
class Queue {
constructor(contents = []) {
this._queue = [...contents];
}
pop() {
const value = this._queue[0];
this._queue.splice(0, 1);
return value;
}
}
使用extends实现继承，因为这样更简单，不会有破坏instanceof运算的危险。
// bad
const inherits = require('inherits');
function PeekableQueue(contents) {
Queue.apply(this, contents);
}
inherits(PeekableQueue, Queue);
PeekableQueue.prototype.peek = function() {
return this._queue[0];
}
// good
class PeekableQueue extends Queue {
peek() {
return this._queue[0];
}
}
21.9 模块
首先，Module语法是JavaScript模块的标准写法，坚持使用这种写法。使用import取代require。
// bad
const moduleA = require('moduleA');
const func1 = moduleA.func1;
const func2 = moduleA.func2;
// good
import { func1, func2 } from 'moduleA';
使用export取代module.exports。
// commonJS的写法
var React = require('react');
var Breadcrumbs = React.createClass({
render() {
return &lt;nav /&gt;;
}
});
module.exports = Breadcrumbs;
// ES6的写法
import React from 'react';
const Breadcrumbs = React.createClass({
render() {
return &lt;nav /&gt;;
}
});
export default Breadcrumbs
如果模块只有一个输出值，就使用export default，如果模块有多个输出值，就不使用export default，不要export default与普通的export同时使
用。
不要在模块输入中使用通配符。因为这样可以确保你的模块之中，有一个默认输出（export default）。
// bad
import * as myObject './importModule';
// good
import myObject from './importModule';
如果模块默认输出一个函数，函数名的首字母应该小写。
function makeStyleGuide() {
}
export default makeStyleGuide;
如果模块默认输出一个对象，对象名的首字母应该大写。
const StyleGuide = {
es6: {
}
};
export default StyleGuide;
21.10 ESLint的使用
ESLint是一个语法规则和代码风格的检查工具，可以用来保证写出语法正确、风格统一的代码。
首先，安装ESLint。
$ npm i -g eslint
然后，安装Airbnb语法规则。
$ npm i -g eslint-config-airbnb
最后，在项目的根目录下新建一个.eslintrc文件，配置ESLint。
{
"extends": "eslint-config-airbnb"
}
现在就可以检查，当前项目的代码是否符合预设的规则。
index.js文件的代码如下。
var unusued = 'I have no purpose!';
function greet() {
var message = 'Hello, World!';
alert(message);
}
greet();
使用ESLint检查这个文件。
$ eslint index.js
index.js
1:5 error unusued is defined but never used no-unused-vars
4:5 error Expected indentation of 2 characters but found 4 indent
5:5 error Expected indentation of 2 characters but found 4 indent
✖ 3 problems (3 errors, 0 warnings)
上面代码说明，原文件有三个错误，一个是定义了变量，却没有使用，另外两个是行首缩进为4个空格，而不是规定的2个空格。
22 读懂 ECMAScript 规格
22.1 概述
规格文件是计算机语言的官方标准，详细描述语法规则和实现方法。
一般来说，没有必要阅读规格，除非你要写编译器。因为规格写得非常抽象和精炼，又缺乏实例，不容易理解，而且对于解决实际的应用问题，帮助
不大。但是，如果你遇到疑难的语法问题，实在找不到答案，这时可以去查看规格文件，了解语言标准是怎么说的。规格是解决问题的“最后一招”。
这对JavaScript语言很有必要。因为它的使用场景复杂，语法规则不统一，例外很多，各种运行环境的行为不一致，导致奇怪的语法问题层出不穷，任
何语法书都不可能囊括所有情况。查看规格，不失为一种解决语法问题的最可靠、最权威的终极方法。
本章介绍如何读懂ECMAScript 6的规格文件。
ECMAScript 6的规格，可以在ECMA国际标准组织的官方网站（www.ecma-international.org/ecma-262/6.0/）免费下载和在线阅读。
这个规格文件相当庞大，一共有26章，A4打印的话，足足有545页。它的特点就是规定得非常细致，每一个语法行为、每一个函数的实现都做了详尽
的清晰的描述。基本上，编译器作者只要把每一步翻译成代码就可以了。这很大程度上，保证了所有ES6实现都有一致的行为。
ECMAScript 6规格的26章之中，第1章到第3章是对文件本身的介绍，与语言关系不大。第4章是对这门语言总体设计的描述，有兴趣的读者可以读一
下。第5章到第8章是语言宏观层面的描述。第5章是规格的名词解释和写法的介绍，第6章介绍数据类型，第7章介绍语言内部用到的抽象操作，第8章
介绍代码如何运行。第9章到第26章介绍具体的语法。
对于一般用户来说，除了第4章，其他章节都涉及某一方面的细节，不用通读，只要在用到的时候，查阅相关章节即可。下面通过一些例子，介绍如何
使用这份规格。
21.2 相等运算符
相等运算符（==）是一个很让人头痛的运算符，它的语法行为多变，不符合直觉。这个小节就看看规格怎么规定它的行为。
请看下面这个表达式，请问它的值是多少。
0 == null
如果你不确定答案，或者想知道语言内部怎么处理，就可以去查看规格，7.2.12小节是对相等运算符（==）的描述。
规格对每一种语法行为的描述，都分成两部分：先是总体的行为描述，然后是实现的算法细节。相等运算符的总体描述，只有一句话。
“The comparison x == y, where x and y are values, produces true or false.”
上面这句话的意思是，相等运算符用于比较两个值，返回true或false。
下面是算法细节。
1. ReturnIfAbrupt(x).
2. ReturnIfAbrupt(y).
3. If Type(x) is the same as Type(y), then
Return the result of performing Strict Equality Comparison x === y.
4. If x is null and y is undefined, return true.
5. If x is undefined and y is null, return true.
6. If Type(x) is Number and Type(y) is String,
return the result of the comparison x == ToNumber(y).
7. If Type(x) is String and Type(y) is Number,
return the result of the comparison ToNumber(x) == y.
8. If Type(x) is Boolean, return the result of the comparison ToNumber(x) == y.
9. If Type(y) is Boolean, return the result of the comparison x == ToNumber(y).
10. If Type(x) is either String, Number, or Symbol and Type(y) is Object, then
return the result of the comparison x == ToPrimitive(y).
11. If Type(x) is Object and Type(y) is either String, Number, or Symbol, then
return the result of the comparison ToPrimitive(x) == y.
12. Return false.
上面这段算法，一共有12步，翻译如下。
1. 如果x不是正常值（比如抛出一个错误），中断执行。
2. 如果y不是正常值，中断执行。
3. 如果Type(x)与Type(y)相同，执行严格相等运算x === y。
4. 如果x是null，y是undefined，返回true。
5. 如果x是undefined，y是null，返回true。
6. 如果Type(x)是数值，Type(y)是字符串，返回x == ToNumber(y)的结果。
7. 如果Type(x)是字符串，Type(y)是数值，返回ToNumber(x) == y的结果。
8. 如果Type(x)是布尔值，返回ToNumber(x) == y的结果。
9. 如果Type(y)是布尔值，返回x == ToNumber(y)的结果。
10. 如果Type(x)是字符串或数值或Symbol值，Type(y)是对象，返回x == ToPrimitive(y)的结果。
11. 如果Type(x)是对象，Type(y)是字符串或数值或Symbol值，返回ToPrimitive(x) == y的结果。
12. 返回false。
由于0的类型是数值，null的类型是Null（这是规格4.3.13小节的规定，是内部Type运算的结果，跟typeof运算符无关）。因此上面的前11步都得不到
结果，要到第12步才能得到false。
0 == null // false
21.3 数组的空位
下面再看另一个例子。
const a1 = [undefined, undefined, undefined];
const a2 = [, , ,];
a1.length // 3
a2.length // 3
a1[0] // undefined
a2[0] // undefined
a1[0] === a2[0] // true
上面代码中，数组a1的成员是三个undefined，数组a2的成员是三个空位。这两个数组很相似，长度都是3，每个位置的成员读取出来都
是undefined。
但是，它们实际上存在重大差异。
0 in a1 // true
0 in a2 // false
a1.hasOwnProperty(0) // true
a2.hasOwnProperty(0) // false
Object.keys(a1) // ["0", "1", "2"]
Object.keys(a2) // []
a1.map(n =&gt; 1) // [1, 1, 1]
a2.map(n =&gt; 1) // [, , ,]
上面代码一共列出了四种运算，数组a1和a2的结果都不一样。前三种运算（in运算符、数组的hasOwnProperty方法、Object.keys方法）都说明，数
组a2取不到属性名。最后一种运算（数组的map方法）说明，数组a2没有发生遍历。
为什么a1与a2成员的行为不一致？数组的成员是undefined或空位，到底有什么不同？
规格的12.2.5小节《数组的初始化》给出了答案。
“Array elements may be elided at the beginning, middle or end of the element list. Whenever a comma in the element list is not preceded by
an AssignmentExpression (i.e., a comma at the beginning or after another comma), the missing array element contributes to the length of the
Array and increases the index of subsequent elements. Elided array elements are not defined. If an element is elided at the end of an array,
that element does not contribute to the length of the Array.”
翻译如下。
"数组成员可以省略。只要逗号前面没有任何表达式，数组的length属性就会加1，并且相应增加其后成员的位置索引。被省略的成员不会被定
义。如果被省略的成员是数组最后一个成员，则不会导致数组length属性增加。”
上面的规格说得很清楚，数组的空位会反映在length属性，也就是说空位有自己的位置，但是这个位置的值是未定义，即这个值是不存在的。如果一
定要读取，结果就是undefined（因为undefined在JavaScript语言中表示不存在）。
这就解释了为什么in运算符、数组的hasOwnProperty方法、Object.keys方法，都取不到空位的属性名。因为这个属性名根本就不存在，规格里面没说
要为空位分配属性名(位置索引），只说要为下一个元素的位置索引加1。
至于为什么数组的map方法会跳过空位，请看下一节。
21.4 数组的map方法
规格的22.1.3.15小节定义了数组的map方法。该小节先是总体描述map方法的行为，里面没有提到数组空位。
后面的算法描述是这样的。
1. Let O be ToObject(this value).
2. ReturnIfAbrupt(O).
3. Let len be ToLength(Get(O, "length")).
4. ReturnIfAbrupt(len).
5. If IsCallable(callbackfn) is false, throw a TypeError exception.
6. If thisArg was supplied, let T be thisArg; else let T be undefined.
7. Let A be ArraySpeciesCreate(O, len).
8. ReturnIfAbrupt(A).
9. Let k be 0.
10. Repeat, while k &lt; len
a. Let Pk be ToString(k).
b. Let kPresent be HasProperty(O, Pk).
c. ReturnIfAbrupt(kPresent).
d. If kPresent is true, then
d-1. Let kValue be Get(O, Pk).
d-2. ReturnIfAbrupt(kValue).
d-3. Let mappedValue be Call(callbackfn, T, «kValue, k, O»).
d-4. ReturnIfAbrupt(mappedValue).
d-5. Let status be CreateDataPropertyOrThrow (A, Pk, mappedValue).
d-6. ReturnIfAbrupt(status).
e. Increase k by 1.
11. Return A.
翻译如下。
1. 得到当前数组的this对象
2. 如果报错就返回
3. 求出当前数组的length属性
4. 如果报错就返回
5. 如果map方法的参数callbackfn不可执行，就报错
6. 如果map方法的参数之中，指定了this，就让T等于该参数，否则T为undefined
7. 生成一个新的数组A，跟当前数组的length属性保持一致
8. 如果报错就返回
9. 设定k等于0
10. 只要k小于当前数组的length属性，就重复下面步骤
a. 设定Pk等于ToString(k)，即将K转为字符串
b. 设定kPresent等于HasProperty(O, Pk)，即求当前数组有没有指定属性
c. 如果报错就返回
d. 如果kPresent等于true，则进行下面步骤
d-1. 设定kValue等于Get(O, Pk)，取出当前数组的指定属性
d-2. 如果报错就返回
d-3. 设定mappedValue等于Call(callbackfn, T, «kValue, k, O»)，即执行回调函数
d-4. 如果报错就返回
d-5. 设定status等于CreateDataPropertyOrThrow (A, Pk, mappedValue)，即将回调函数的值放入A数组的指定位置
d-6. 如果报错就返回
e. k增加1
11. 返回A
仔细查看上面的算法，可以发现，当处理一个全是空位的数组时，前面步骤都没有问题。进入第10步的b时，kpresent会报错，因为空位对应的属性
名，对于数组来说是不存在的，因此就会返回，不会进行后面的步骤。
const arr = [, , ,];
arr.map(n =&gt; {
console.log(n);
return 1;
}) // [, , ,]
上面代码中，arr是一个全是空位的数组，map方法遍历成员时，发现是空位，就直接跳过，不会进入回调函数。因此，回调函数里面的console.log语
句根本不会执行，整个map方法返回一个全是空位的新数组。
V8引擎对map方法的实现如下，可以看到跟规格的算法描述完全一致。
function ArrayMap(f, receiver) {
CHECK_OBJECT_COERCIBLE(this, "Array.prototype.map");
// Pull out the length so that modifications to the length in the
// loop will not affect the looping and side effects are visible.
var array = TO_OBJECT(this);
var length = TO_LENGTH_OR_UINT32(array.length);
return InnerArrayMap(f, receiver, array, length);
}
function InnerArrayMap(f, receiver, array, length) {
if (!IS_CALLABLE(f)) throw MakeTypeError(kCalledNonCallable, f);
var accumulator = new InternalArray(length);
var is_array = IS_ARRAY(array);
var stepping = DEBUG_IS_STEPPING(f);
for (var i = 0; i &lt; length; i++) {
if (HAS_INDEX(array, i, is_array)) {
var element = array[i];
// Prepare break slots for debugger step in.
if (stepping) %DebugPrepareStepInIfStepping(f);
accumulator[i] = %_Call(f, receiver, element, i, array);
}
}
var result = new GlobalArray();
%MoveArrayContents(accumulator, result);
r
e
t
u
r
n
r
e
s
u
l
t
;
}
</pre>
</div>
