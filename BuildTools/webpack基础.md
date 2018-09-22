## 1. 导语

###  1.1 什么叫做webpack
> webpack is a module bundler. 
> webpack takes modules with dependencies and generates static assets representing those modules.

简单的概括就是：webpack是一个模块打包工具，处理模块之间的依赖同时生成对应模块的静态资源。

### 1.2 webpack可以做一些什么事情
![这里写图片描述](http://img.blog.csdn.net/20160723105504240)

图中已经很清楚的反应了几个信息：

 - webpack把项目中所有的静态文件都看作一个模块
 - 模快之间存在着一些列的依赖
 - 多页面的静态资源生成(打包之后生成多个静态文件，涉及到代码拆分)

## 2. webpack安装

- 全局安装(供全局调用：如`webpack --config webpack.config.js`)

```javascript
npm install -g webpack
```
- 项目安装

```javascript
npm install webpack

// 处理类似如下调用
import webpack from "webpack";
var webpack = require("webpack");
```

建议安装淘宝的npm镜像，这样下载npm包会快上很多，具体做法：

```javascript
// 方式一
npm install xx --registry=https://registry.npm.taobao.org/

// 方式二:安装淘宝提供的npm工具
npm install -g cnpm
cnpm install xx

// 方式三
// 在用户主目录下，找到.npmrc文件，加上下面这段配置
registry=https://registry.npm.taobao.org/
```

## 3. webpack的基本配置
创建配置文件(`webpack.config.js`，执行webpack命令的时候，默认会执行这个文件)
```javascript
module.export = {
	entry : 'app.js',
	output : {
		path : 'assets/',
		filename : '[name].bundle.js'
	},
	module : {
		loaders : [
			// 使用babel-loader解析js或者jsx模块
			{ test : /\.js|\.jsx$/, loader : 'babel' },
			// 使用css-loader解析css模块
			{ test : /\.css$/, loader : 'style!css' },
			// or another way
			{ test : /\.css$/, loader : ['style', 'css'] }
		]
	}
};
```
说明一： `webpack.config.js`默认输出一个`webpack`的配置文件，与`CLI`方式调用相同，只是更加简便

说明二： 执行`webpack`命令即可以运行配置，先决条件，全局安装`webpack`，项目安装各模块`loader`

说明三： `entry`对应需要打包的入口`js`文件，`output`对应输出的目录以及文件名，`module`中的`loaders`对应解析各个模块时需要的加载器

**一个简单的例子**

`basic/app.js`
```javascript
require('./app.css');
document.getElementById('container').textContent = 'APP';
```

---------
`basic/app.css`
```css
* {
    margin: 0;
    padding: 0;
}
#container {
    margin: 50px auto;
    width: 50%;
    height: 200px;
    line-height: 200px;
    border-radius: 5px;
    box-shadow: 0 0 .5em #000;
    text-align: center;
    font-size: 40px;
    font-weight: bold;
}
```

--------
`basic/webpack.config.js`
```javascript
/**
 * webpack打包配置文件
 */

module.exports = {
	// 如果你有多个入口js,需要打包在一个文件中,那么你可以这么写 
	// entry : ['./app1.js', './app2.js']
    entry : './app.js',
    output : {
        path : './assets/',
        filename : '[name].bundle.js'
    },
    module : {
        loaders : [
            { test : /\.js$/, loader : 'babel' },
            { test : /\.css$/, loader : 'style!css' }
        ]
    }
};
```

-----------
`basic/index.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>basic webpack</title>
</head>
<body>
    <div id="container"></div>
    <script src="./assets/main.bundle.js"></script>
</body>
</html>
```

在`basic`文件夹执行`webpack`，打包信息如下

![这里写图片描述](http://img.blog.csdn.net/20160723115842221)

生成`main.bundle.js`文件，`chunk`名称为`main`，也是`webpack`默认生成的`chunk`名

## 4. webapck常用到的各点拆分
---------------

### 4.1 entry相关
--------------
 **4.1.1`webpack`的多入口配置**

上例的简单配置中，只有一个入口文件，那么如果对应于一个页面需要加载多个打包文件或者多个页面想同时引入对应的打包文件的时候，应该怎么做？
```javascript
entry : {
	app1 : './app1.js',
	app2 : './app2.js'
}
```
在`multi-entry`文件夹执行`webpack`，打包信息如下

![这里写图片描述](http://img.blog.csdn.net/20160723122445540)

可见生成了两个入口文件，以及各自对应的`chunk`名

----------
### 4.2 output相关
------------
**4.2.1 `output.publicPath`**
```javascript
output: {
    path: "/home/proj/cdn/assets/[hash]",
    publicPath: "http://cdn.example.com/assets/[hash]/"
}
```

引用一段官网的话：
> The publicPath specifies the public URL address of the output files when referenced in a browser. For loaders that embed `<script>` or `<link>` tags or reference assets like images, publicPath is used as the href or url() to the file when it’s different then their location on disk (as specified by path). 

大致意思就是：`publicPath`指定了你在浏览器中用什么地址来引用你的静态文件，它会包括你的图片、脚本以及样式加载的地址，一般用于线上发布以及CDN部署的时候使用。

比如有下面一段配置：
```javascript
var path = require('path');
var HtmlWebpackPlugin =  require('html-webpack-plugin');

module.exports = {
    entry : './app.js',
    output : {
        path : './assets/',
        filename : '[name].bundle.js',
        publicPath : 'http://rynxiao.com/assets/'
    },
    module : {
        loaders : [
            { test : /\.js$/, loader : 'babel' },
            { test : /\.css$/, loader : 'style!css' }
        ]
    },
    plugins : [
        new HtmlWebpackPlugin({
            filename: './index-release.html',
            template: path.resolve('index.template'),
            inject: 'body'
        })
    ]
};
```
其中我将`publicPath`设置成了`http://rynxiao.com/assets/`，其中设置到了插件的一些东西，这点下面会讲到，总之这个插件的作用是生成了上线发布时候的首页文件，其中`script`中引用的路径将会被替换。如下图：

![这里写图片描述](http://img.blog.csdn.net/20160723132645470)

----------------
**4.2.2 `output.chunkFilename`**

各个文件除了主模块以外，还可能生成许多额外附加的块，比如在模块中采用代码分割就会出现这样的情况。其中`chunkFilename`中包含以下的文件生成规则：

[id] 会被对应块的id替换.

[name] 会被对应块的name替换（或者被id替换，如果这个块没有name）.

[hash] 会被文件hash替换.

[chunkhash] 会被块文件hash替换.

例如，我在output中如下设置：
```javascript
output : {
    path : './assets/',
    filename : '[name].[hash].bundle.js',
    chunkFilename: "chunk/[chunkhash].chunk.js"
}
```
同时我修改了一下`basic/app.js`中的文件
```javascript
require('./app.css');

require.ensure('./main.js', function(require) {
    require('./chunk.js');
});

document.getElementById("container").textContent = "APP";
```
其中对应的`chunk.js`就会生成带有`chunkhash`的`chunk`文件，如下图：

![这里写图片描述](http://img.blog.csdn.net/20160723135002158)

*这在做给文件打版本号的时候特别有用，当时如何进行`hash`替换，下面会讲到*

-----------
**4.2.3 `output.library`**

这个配置作为库发布的时候会用到，配置的名字即为库的名字，通常可以搭配`libraryTarget`进行使用。例如我给`basic/webpack.config.js`加上这样的配置：
```javascript
output : {
	// ...
	library : 'testLibrary'
	// ...
}
```
那么实际上生成出来的`main.bundle.js`中会默认带上以下代码：
```javascript
var testLibrary = (//....以前的打包生成的代码);
// 这样在直接引入这个库的时候，就可以直接使用`testLibrary`这个变量
```
![这里写图片描述](http://img.blog.csdn.net/20160723142057926)

------------
**4.2.4 `output.libraryTarget`**

规定了以哪一种方式输出你的库，比如：amd/cmd/或者直接变量，具体包括如下

`"var"` - 以直接变量输出(默认library方式) `var Library = xxx (default)`

`"this"` - 通过设置`this`的属性输出 `this["Library"] = xxx`

`"commonjs"` - 通过设置`exports`的属性输出 `exports["Library"] = xxx`

`"commonjs2"` - 通过设置`module.exports`的属性输出 `module.exports = xxx`

`"amd"` - 以amd方式输出

`"umd"` - 结合commonjs2/amd/root

例如我以`umd`方式输出，如图：

![这里写图片描述](http://img.blog.csdn.net/20160723142325583)

-------------

### 4.3 module相关
--------

#### 4.3.1 `loader`中`!`代表的含义
> `require("!style!css!less!bootstrap/less/bootstrap.less");`
// => the file "bootstrap.less" in the folder "less" in the "bootstrap"
//    module (that is installed from github to "node_modules") is
//    transformed by the "less-loader". The result is transformed by the
//    "css-loader" and then by the "style-loader".
//    If configuration has some transforms bound to the file, they will not be applied.

代表加载器的流式调用，例如：
```javascript
{ test : /\.css|\.less$/, loader : 'style!css!less' }
```
就代表了先使用less加载器来解释less文件，然后使用css加载器来解析less解析后的文件，依次类推

--------
#### 4.3.2 `loaders`中的`include`与`exclude`
`include`表示必须要包含的文件或者目录，而`exclude`的表示需要排除的目录

比如我们在配置中一般要排除`node_modules`目录，就可以这样写
```javascript
{ 
	test : /\.js$/, 
	loader : 'babel',
	exclude : nodeModuleDir 
}
```
官方建议：优先采用include，并且include最好是文件目录

---------
#### 4.3.3 `module.noParse`
使用了`noParse`的模块将不会被`loaders`解析，所以当我们使用的库如果太大，并且其中不包含`require`、`define`或者类似的关键字的时候(因为这些模块加载并不会被解析，所以就会报错)，我们就可以使用这项配置来提升性能。

例如下面的例子：在`basic/`目录中新增`no-parse.js`
```javascript
var cheerio = require('cheerio');

module.exports = function() {
    console.log(cheerio);
}
```
`webpack.config.js`中新增如下配置：
```javascript
module : {
    loaders : [
        { test : /\.js$/, loader : 'babel' },
        { test : /\.css$/, loader : 'style!css' }
    ],
    noParse : /no-parse.js/
}
```
当执行打包后，在浏览器中打开`index.html`时，就会报错`require is not defined`

![这里写图片描述](http://img.blog.csdn.net/20160723152744481)

### 4.4 resolve相关

#### 4.4.1 `resolve.alias`
为模块设置别名，能够让开发者指定一些模块的引用路径。对一些经常要被import或者require的库，如react,我们最好可以直接指定它们的位置，这样webpack可以省下不少搜索硬盘的时间。
例如我们修改`basic/app.js`中的相关内容：
```javascript
var moment = require("moment");

document.getElementById("container").textContent = moment().locale('zh-cn').format('LLLL');
```
加载一个操作时间的类库，让它显示当前的时间。使用`webpack --profile --colors --display-modules`执行配置文件，得到如下结果：

![这里写图片描述](http://img.blog.csdn.net/20160723162934423)

其中会发现，打包总共生成了104个隐藏文件，其中一半的时间都在处理关于`moment`类库相关的事情，比如寻找`moment`依赖的一些类库等等。

在`basic/webpack.config.js`加入如下配置，然后执行配置文件
```javascript
resolve : {
    alias : {
        moment : 'moment/min/moment-with-locales.min.js'
    }
}
```
![这里写图片描述](http://img.blog.csdn.net/20160723163439259)

有没有发现打包的时间已经被大大缩短，并且也只产生了两个隐藏文件。

**配合`module.noParse`使用**

`module.noParse`参看上面的解释
```javascript
noParse: [/moment-with-locales/]
```
执行打包后，效果如下：

![这里写图片描述](http://img.blog.csdn.net/20160723163819826)

是不是发现打包的时间进一步缩短了。

**配合`externals`使用**

`externals`参看下面的解释
>Webpack 是如此的强大，用其打包的脚本可以运行在多种环境下，Web 环境只是其默认的一种，也是最常用的一种。考虑到 Web 上有很多的公用 CDN 服务，那么 怎么将 Webpack 和公用的 CDN 结合使用呢？方法是使用 externals 声明一个外部依赖。
```javascript
externals: {
    moment: true
}
```
当然了 HTML 代码里需要加上一行
```javascript
<script src="//apps.bdimg.com/libs/moment/2.8.3/moment-with-locales.min.js"></script>
```
执行打包后，效果如下：

![这里写图片描述](http://img.blog.csdn.net/20160723170548257)

---------
#### 4.4.2 `resolve.extensions`

```javascript
resolve : {
    extensions: ["", ".webpack.js", ".web.js", ".js", ".less"]
}
```
这项配置的作用是自动加上文件的扩展名，比如你有如下代码：
```javascript
require('style.less');

var app = require('./app.js');
```
那么加上这项配置之后，你可以写成：
```javascript
require('style');

var app = require('./app');
```
------------
### 4.5 externals

当我们想在项目中require一些其他的类库或者API，而又不想让这些类库的源码被构建到运行时文件中，这在实际开发中很有必要。此时我们就可以通过配置externals参数来解决这个问题：
```javascript
//webpack.config.js
module.exports = {
    externals: {
      'react': 'React'
    },
    //...
}
```
externals对象的key是给require时用的，比如require('react')，对象的value表示的是如何在global（即window）中访问到该对象，这里是window.React。

同理jquery的话就可以这样写：'jquery': 'jQuery'，那么require('jquery')即可。

HTML中注意引入顺序即可：
```javascript
<script src="react.min.js" />
<script src="bundle.js" />
```

----------------------
### 4.6 devtool
提供了一些方式来使得代码调试更加方便，因为打包之后的代码是合并以后的代码，不利于排错和定位。其中有如下几种方式，参见官网[devtool](http://webpack.github.io/docs/configuration.html#devtool)

例如，我在`basic/app.js`中增加如下配置：
```javascript
require('./app.css');

// 新增hello.js，显然在文件夹中是不会存在hello.js文件的，这里会报错
require('./hello.js');

document.getElementById("container").textContent = "APP";
```
执行文件，之后运行`index.html`，报错结果如下：

![这里写图片描述](http://img.blog.csdn.net/20160723172740677)

给出的提示实在main.bundle.js第48行，点进去看其中的报错如下：

![这里写图片描述](http://img.blog.csdn.net/20160723172852054)

从这里你完全看不出到底你程序的哪个地方出错了，并且这里的行数还算少，当一个文件出现了上千行的时候，你定位`bug`的时间将会更长。

增加`devtool`文件配置，如下：
```javascript
module.exports = {
	devtool: 'eval-source-map',
	// ....
};
```
执行文件，之后运行`index.html`，报错结果如下：

![这里写图片描述](http://img.blog.csdn.net/20160723173217887)

这里发现直接定位到了`app.js`，并且报出了在第二行出错，点击去看其中的报错如下：

![这里写图片描述](http://img.blog.csdn.net/20160723173402869)

发现问题定位一目了然。

## 5. webpack常用技巧

### 5.1 代码块划分
------------
**5.1.1 Commonjs采用`require.ensure`来产生`chunk`块**
```javascript
require.ensure(dependencies, callback);

//static imports
import _ from 'lodash'

// dynamic imports
require.ensure([], function(require) {
  let contacts = require('./contacts')
})
```
这一点在`output.chunkFileName`中已经做过演示，可以去查看

----------------------------
**5.1.2 AMD采用`require`来产生`chunk`块**
```javascript
require(["module-a", "module-b"], function(a, b) {
    // ...
});
```

---------------------
**5.1.3 将项目APP代码与公共库文件单独打包**

我们在`basic/app.js`中添加如下代码
```javascript
var $ = require('juqery'),
	_ = require('underscore');

//.....
```
然后我们在配置文件中添加`vendor`，以及运用代码分离的插件对生成的`vendor`块重新命名
```javascript
var webpack = require("webpack");

module.exports = {
	entry: {
		app: "./app.js",
		vendor: ["jquery", "underscore", ...],
	},
	output: {
		filename: "bundle.js"
	},
	plugins: [
		new webpack.optimize.CommonsChunkPlugin(/* chunkName= */"vendor", /* filename= */"vendor.bundle.js")
	]
};
```
运行配置文件，效果如下：

![这里写图片描述](http://img.blog.csdn.net/20160723191116598)

------------------
**5.1.4 抽取多入口文件的公共部分**

我们重新建立一个文件夹叫做`common`，有如下文件：
```javascript
// common/app1.js

console.log("APP1");
```
```javascript
// common/app2.js

console.log("APP2");
```
打包之后生成的`app1.bundle.js`、`app2.bundle.js`中会存在许多公共代码，我们可以将它提取出来。
```javascript
// common/webpack.config.js

/**
 * webpack打包配置文件
 * 抽取公共部分js
 */

var webpack = require('webpack');

module.exports = {
    entry : {
        app1 : './app1.js',
        app2 : './app2.js'
    },
    output : {
        path : './assets/',
        filename : '[name].bundle.js'
    },
    module : {
        loaders : [
            { test : /\.js$/, loader : 'babel' },
            { test : /\.css$/, loader : 'style!css' }
        ]
    },
    plugins : [
        new webpack.optimize.CommonsChunkPlugin("common.js")
    ]
};
```
抽取出的公共js为`common.js`,如图

![这里写图片描述](http://img.blog.csdn.net/20160723192023883)

查看`app1.bundle.js`，发现打包的内容基本是我们在模块中所写的代码，公共部分已经被提出到`common.js`中去了

![这里写图片描述](http://img.blog.csdn.net/20160723192454683)

**5.1.5 抽取css文件，打包成css bundle**

默认情况下以`require('style.css')`情况下导入样式文件，会直接在`index.html`的`<head>`中生成`<style>`标签，属于内联。如果我们想将这些css文件提取出来，可以按照下面的配置去做。
```javascript
// extract-css/app1.js
require('./app1.css');
document.getElementById("container").textContent = "APP";

// extract-css/app2.js
require('./app2.css');
document.getElementById("container").textContent = "APP1 APP2";

// extract-css/app1.css
* {
    margin: 0;
    padding: 0;
}
#container {
    margin: 50px auto;
    width: 50%;
    height: 200px;
    line-height: 200px;
    border-radius: 5px;
    box-shadow: 0 0 .5em #000;
    text-align: center;
    font-size: 40px;
    font-weight: bold;
}

// extract-css/app2.css
#container {
    background-color: #f0f0f0;
}

// extract-css/webpack.config.js
/**
 * webpack打包配置文件
 * 抽取公共样式(没有chunk)
 */

var webpack = require('webpack');
var ExtractTextPlugin = require("extract-text-webpack-plugin");

module.exports = {
    entry : {
        app1 : './app1.js',
        app2 : './app1.js'
    },
    output : {
        path : './assets/',
        filename : '[name].bundle.js'
    },
    module : {
        loaders : [
            { test : /\.js$/, loader : 'babel' },
            { test : /\.css$/, loader : ExtractTextPlugin.extract("style-loader", "css-loader") }
        ]
    },
    plugins : [
        new ExtractTextPlugin("[name].css")
    ]
};
```
得到的效果如下图：

![这里写图片描述](http://img.blog.csdn.net/20160723193957752)

如果包含chunk文件，并且chunk文件中也因为了样式文件，那么样式文件会嵌入到js中

**css合并到一个文件**
```javascript
// ...
module.exports = {
    // ...
    plugins: [
        new ExtractTextPlugin("style.css", {
            allChunks: true
        })
    ]
}
```
效果如图：

![这里写图片描述](http://img.blog.csdn.net/20160723194749005)

如果包含chunk文件，并且chunk文件中也因为了样式文件，样式文件不会嵌入到js中，而是直接输出到`style.css`

**配合CommonsChunkPlugin一起使用**
```javascript
// ...
module.exports = {
    // ...
    plugins: [
        new webpack.optimize.CommonsChunkPlugin("commons", "commons.js"),
        new ExtractTextPlugin("[name].css")
    ]
}
```
效果图如下：

![这里写图片描述](http://img.blog.csdn.net/20160723200356707)

-------------------
### 5.2 如何给文件打版本

线上发布时为了防止浏览器缓存静态资源而改变文件版本，这里提供两种做法：

**5.2.1 使用`HtmlWebpackPlugin`插件**
```javascript
// version/webpack.config.js

/**
 * webpack打包配置文件
 * 文件打版本，线上发布
 */

var path = require('path');
var HtmlWebpackPlugin =  require('html-webpack-plugin');

module.exports = {
    entry : './app.js',
    output : {
        path : './assets/',
        filename : '[name].[hash].bundle.js',
        publicPath : 'http://rynxiao.com/assets/'
    },
    module : {
        loaders : [
            { test : /\.js$/, loader : 'babel' },
            { test : /\.css$/, loader : 'style!css' }
        ]
    },
    plugins : [
        new HtmlWebpackPlugin({
            filename: './index-release.html',
            template: path.resolve('index.template'),
            inject: 'body'
        })
    ]
};
```
生成的效果如下：

![这里写图片描述](http://img.blog.csdn.net/20160723201203843)

每次打包之后都会生成文件hash，这样就做到了版本控制

----------------
**5.2.2 自定义插件给文件添加版本**
```javascript
// version/webpack.config.version.js

/**
 * webpack打包配置文件
 * 文件打版本，线上发布，自定义插件方式
 */

var path = require('path');
var fs = require('fs');
var cheerio = require('cheerio');

module.exports = {
    entry : './app.js',
    output : {
        path : './assets/',
        filename : '[name].[hash].bundle.js',
        publicPath : 'http://rynxiao.com/assets/'
    },
    module : {
        loaders : [
            { test : /\.js$/, loader : 'babel' },
            { test : /\.css$/, loader : 'style!css' }
        ]
    },
    plugins : [
        function() {
            this.plugin("done", function(stats) {
                fs.writeFileSync(
                    path.join(__dirname, "stats.json"),
                    JSON.stringify(stats.toJson())
                );
                fs.readFile('./index.html', function(err, data) {
                    var $ = cheerio.load(data.toString());
                   $('script[src*=assets]').attr('src','http://rynxiao.com/assets/main.' 
		                    + stats.hash +'.bundle.js');
                    fs.writeFile('./index.html', $.html(), function(err) {
                        !err && console.log('Set has success: '+ stats.hash)
                    })
                })
            });
        }
    ]
};
```

效果如图：

![这里写图片描述](http://img.blog.csdn.net/20160723203654971)

可以达到同样的效果，但是stats暂时只能拿到hash值，因为我们只能考虑在hash上做版本控制，比如我们可以建hash目录等等

----------------
### 5.3 shim
比如有如下场景：我们用到 Pen 这个模块, 这个模块对依赖一个 window.jQuery, 可我手头的 jQuery 是 CommonJS 语法的，而 Pen 对象又是生成好了绑在全局的, 可是我又需要通过 require('pen') 获取变量。 最终的写法就是做 Shim 处理直接提供支持:

**做法一：**
```javascript
{test: require.resolve('jquery'), loader: 'expose?jQuery'}, // 输出jQuery到全局
{test: require.resolve('pen'), loader: 'exports?window.Pen'}    // 将Pen作为一个模块引入
```

**做法二：**
```javascript
new webpack.ProvidePlugin({
    $: "jquery",
    jQuery: "jquery",
    "window.jQuery": "jquery"
})
```
>This plugin makes a module available as variable in every module. 
>The module is required only if you use the variable.
>Example: Make $ and jQuery available in every module without writing require("jquery").

--------------------
### 5.4 怎样写一个loader

> Loader 是支持链式执行的，如处理 sass 文件的 loader，可以由 sass-loader、css-loader、style-loader 组成，由 compiler 对其由右向左执行，第一个 Loader 将会拿到需处理的原内容，上一个 Loader 处理后的结果回传给下一个接着处理，最后的 Loader 将处理后的结果以 String 或 Buffer 的形式返回给 compiler。固然也是希望每个 loader **只做该做的事，纯粹的事**，而不希望一箩筐的功能都集成到一个 Loader 中。

官网给出了两种写法：

```javascript
// Identity loader
module.exports = function(source) {
  return source;
};
```

```javascript
// Identity loader with SourceMap support
module.exports = function(source, map) {
  this.callback(null, source, map);
};
```
第一种为基础的写法，采用`return`返回， 是因为是同步类的 Loader 且返回的内容唯一。如果你写loader有依赖的话，同样的你也可以在头部进行引用，比如：
```javascript
// Module dependencies.
var fs = require("fs");
module.exports = function(source) {
  return source;
};
```
而第二种则是希望多个`loader`之间链式调用，将上一个`loader`返回的结果传递给下一个`loader`。

**案例**

比如我想开发一个es6-loader,专门用来做以`.es6`文件名结尾的文件处理，那么我们可以这么写
```javascript
// loader/es6-loader.js
// 当然如果我这里不想将这个loader所返回的东西传递给下一个laoder，那么我
// 可以在最后直接返回return source
// 这里改变之后，我直接可以扔给babel-loader进行处理
module.exports = function(source, map) {
	// 接收es6结尾文件，进行source改变
    source = "console.log('I changed in loader');"
    // 打印传递进来的参数
    console.log("param", this.query);
    // ... 我们还可以做一些其他的逻辑处理
    this.callback(null, source, map);
};

// loader/loader1.es6
let a = 1;
console.log(a);

// loader/app.js
// 向loader中传递参数
require('./es6-loader?param1=p1!./loader1.es6');
document.getElementById("container").textContent = "APP";
```
执行webpack打包命令，在控制台会打印出param的值，如图：

![这里写图片描述](http://img.blog.csdn.net/20160723221900665)

在执行完成之后，打开`index.html`，在控制台打印出“I changed in loader”，而不是1

![这里写图片描述](http://img.blog.csdn.net/20160723222056334)

**进阶**

可以去阅读以下这篇文章 [如何开发一个 Webpack loader](http://web.jobbole.com/84851/)

--------------------
### 5.4 怎样写一个plugin

插件基本的结构

插件是可以实例化的对象，在它的prototype上必须绑定一个`apply`方法。这个方法会在插件安装的时候被`Webpack compiler`进行调用。

```javascript
function HelloWorldPlugin(options) {
	// Setup the plugin instance with options...
}

HelloWorldPlugin.prototype.apply = function(compiler) {
	compiler.plugin('done', function() {
	    console.log('Hello World!'); 
	});
};

module.exports = HelloWorldPlugin;
```

安装一个插件，将其添加到配置中的`plugins`数组中。

```javascript
var HelloWorldPlugin = require('hello-world');

var webpackConfig = {
// ... config settings here ...
	plugins: [
		new HelloWorldPlugin({options: true})
	]
};
```
执行效果如图：

![这里写图片描述](http://img.blog.csdn.net/20160723223746845)

这里只作简单的引入，平常一般都不需要自己写插件，如果想进一步了解，可以去看官网例子

### 5.5 布置一个本地服务器
```javascript
// 1.全局安装webpack-dev-server
cnpm install -g webpack-dev-server

// 2. 设置一个文件启动目录，运行
webpack-dev-server --content-base basic/

// 3. 在浏览器输入localhost:8080
```

------------------
### 5.6 热替换
```javascript
// auto-refresh/app.js
document.getElementById("container").textContent = "APP APP HOT ";
console.log("OK");

// auto-refresh/server.js
var webpack = require('webpack');
var config = require('./webpack.config.js');
var WebpackDevServer = require("webpack-dev-server");

var compiler = webpack(config);
new WebpackDevServer(webpack(config), {
    publicPath: config.output.publicPath,
    hot: true,
    noInfo: false,
    historyApiFallback: true
}).listen(8080, 'localhost', function (err, result) {
    if (err) {
        console.log(err);
    }
    console.log('Listening at localhost:3000');
});

// auto-refresh/webpack.config.js
/**
 * webpack打包配置文件
 */

var webpack = require('webpack');

module.exports = {
    entry : [
        'webpack-dev-server/client?http://127.0.0.1:8080', // WebpackDevServer host and port
        'webpack/hot/only-dev-server',
        './app.js'
    ],
    output : {
        path : './assets/',
        filename : '[name].bundle.js',
        publicPath : './assets/'
    },
    module : {
        loaders : [
            { test : /\.js$/, loader : 'react-hot!babel' },
            { test : /\.css$/, loader : 'style!css' }
        ]
    },
    plugins : [
        new webpack.HotModuleReplacementPlugin(),
        new webpack.NoErrorsPlugin(),
        new webpack.DefinePlugin({
            'process.env.NODE_ENV': '"development"'
        }),
    ]
};

// auto-refresh/index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>basic webpack</title>
</head>
<body>
    <div id="container"></div>
    <script src="./assets/main.bundle.js"></script>
</body>
</html>

// 运行
node server.js

// 浏览器输入：localhost:8080
```

----------------------------
### 5.7 让wepack.config.js支持es6写法
```javascript
// 1. 安装babel-core、babel-preset-es2015以及babel-loader

// 2. 项目根目录下配置.babelrc文件
{
  "presets": ["es2015"]
}

// 3. 将webpack.config.js重新命名为webpack.config.babel.js

// 4.运行webpack --config webpack.config.babel.js

// 说明node 版本5.0以上，babel-core版本6以上需要如此配置
```
>这是一个 Webpack 支持，但文档里完全没有提到的特性  （应该马上就会加上）。只要你把配置文件命名成 webpack.config.[loader].js ，Webpack 就会用相应的 loader 去转换一遍配置文件。所以要使用这个方法，你需要安装 babel-loader 和 babel-core 两个包。记住你不需要完整的 babel 包。

**其他办法(未成功)**

```javascript
1.在上述的方案中，其实不需要重新命名就可以直接运行webpack，但是今天试了一直不成功
2.{ 
	test : /\.js|jsx$/, 
	loader : 'babel',
	query: {
          //添加两个presents 使用这两种presets处理js或者jsx文件
          presets: ['es2015', 'react']
    } 
}
```


## 6.相关链接
[webpack官方网站](http://webpack.github.io/docs/)

[用 ES6 编写 Webpack 的配置文件](http://cnodejs.org/topic/56346ee43ef9ce60493b0c96)

[一小时包教会 —— webpack 入门指南](http://www.cnblogs.com/vajoy/p/4650467.html)

[Webpack傻瓜式指南（一）](https://zhuanlan.zhihu.com/p/20367175)

[前端模块化工具-webpack](http://www.cnblogs.com/Leo_wl/p/4862714.html)

[如何开发一个 Webpack Loader ( 一 )](http://web.jobbole.com/84851/)

[关于externals解释](https://segmentfault.com/q/1010000002720840)

[webpack使用优化](http://www.open-open.com/lib/view/open1452487103323.html)

[http://webpack.github.io/docs/installation.html](http://webpack.github.io/docs/installation.html)

[https://github.com/petehunt/webpack-howto](https://github.com/petehunt/webpack-howto)

https://github.com/Rynxiao/webpack-tutorial


Webpack 1 / 2 / 3 的 区别
一、 Webpack2 VS Webpack1
新增了许多新特性，需要处理配置语法兼容

1. 增加对 ES6 模块的原生支持
2. 可以混用 ES2015 和 AMD 和 CommonJS
3. 支持 tree-shaking（减少打包后的体积）
4. 新增更多的 CLI 参数项
-p 指定当前的编译环境为生产环境，即设置 process.env.NODE_ENV 为 production

5. 配置选项语法有较大改动，且不向下兼容
5.1 配置项 - resolve（解析）
取消了 extensions 空字符串（表示导入文件无后缀名）

Webpack1
resolve: {
    extensions: ['', '.js', '.css'],
    modulesDirectories: ['node_modules', 'src']
}
Webpack2
resolve: {
    extensions: ['.js', '.css'],
    modules: [
        path.resolve(__dirname, 'node_modules'),
        path.join(__dirname, './src')
    ]
}
5.2 配置项 - module（模块）
外层 loaders 改为 rules
内层 loader 改为 use
所有插件必须加上 -loader，不再允许缩写
不再支持使用!连接插件，改为数组形式
json-loader 模块移除，不再需要手动添加，webpack2 会自动处理

Webpack1
module: {
    loaders: [{
        test: /\.(less|css)$/,
        loader: "style!css!less!postcss"
    }, {
        test: /\.json$/,
        loader: 'json'
    }]
}
Webpack2
module: {
    rules: [{
        test: /\.(less|css)$/,
        use: [
            "style-loader", 
            "css-loader", 
            "less-loader", 
            "postcss-loader"
        ]
    }]
};
5.3 配置项 - plugins（插件）
移除了 OccurenceOrderPlugin 模块（已内置）、NoErrorsPlugin 模块（已内置）
二、 Webpack3 VS Webpack2
两个版本几乎完全兼容，新增部分新特性

1. 加入 Scope Hoisting（作用域提升）
之前版本将每个依赖都分别封装在一个闭包函数中来独立作用域。这些包装函数闭包函数降低了浏览器 JS 引擎解析速度
Webpack 团队参考 Closure Compiler 和 Rollup JS，将有联系的模块放到同一闭包函数中，从而减少闭包函数数量，使文件大小的少量精简，提高 JS 执行效率
在 Webpack3 配置中加入 ModuleConcatenationPlugin 插件来启用作用域提升
module.exports = {
    plugins: [
        new webpack.optimize.ModuleConcatenationPlugin()
    ]
};
2. 加入 Magic Comments（魔法注解）
在 Webpack2 中引入了 Code Splitting-Async 的新方法 import()，用于动态引入 ES Module，Webpack 将传入 import 方法的模块打包到一个单独的代码块（chunk），但是却不能像 require.ensure 一样，为生成的 chunk 指定 chunkName。因此在 Webpack3 中提出了 Magic Comment 用于解决该问题
import(/* webpackChunkName: "my-chunk-name" */ 'module');

### 选择合适的 Devtool 版本[https://www.cnblogs.com/powertoolsteam/p/Webpack.html]
​webpack 的 devtool 配置，决定了在构建过程中怎样生成 sourceMap 文件。通常来说eval的性能最高，但是不能生成的 sourceMap 文件解析出来的代码，和源代码差异较大。 source-map 的性能较差，但是可以生成原始版本的代码。 在大多数 Development 场景下 cheap-module-eval-source-map 是最佳的选择。
### Build Cache
Webpack 和一些 Plugin/Loader 都有 Cache 选项。开启 Cache 选项，有利用提高构建性能。
​比如：使用 babel-loader 的时候开启 cacheDirectory 选项，会较为明显的提升构建速度
```
module: {
    rules: [{
        test: /\.js$/,
        use: ['babel-loader?cacheDirectory'],
        include: path.join(__dirname, 'app')
    }]
 }
 ```
 ### 减少代码体积
 使用 CommonsChunksPlugin 提取多个 chunk 之间的通用模块，减少总体的代码体积
把部分依赖转移到 CDN 上，避免在每次编译过程中都由 Webpack 处理
对于支持局部引入的类库，在开发的过程中使用局部引入的方式，避免引入无用的文件
比如 lodash 就支持部分引入：
```
import isArray from 'lodash/isArray';
```
参考： [Don't import whole lodash] (https://github.com/lodash/lodash/issues/3450)

<div id="cnblogs_post_body" class="blogpost-body"><p align="left">&nbsp;</p>
<blockquote>
<p>本文由博客园-葡萄城技术团队首发</p>
<p>转载请注明出自：<a href="https://www.grapecity.com.cn/" target="_blank">葡萄城官网</a>，葡萄城为开发者提供专业的开发工具、解决方案和服务，赋能开发者。</p>
</blockquote>
<p align="left">&nbsp;</p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;"><a href="https://github.com/webpack">Webpack</a>&nbsp;作为目前最流行的前端构建工具之一，在 vue/react 等 Framework 的生态圈中都占据重要地位。在开发现代 Web 应用的过程中，Webpack 和我们的开发过程和发布过程都息息相关，如何改善 Webpack 构建打包的性能也关系到我们开发和发布部署的效率。</span></p>
<p align="left">&nbsp;</p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">以下是一些关于优化 Webpack 构建性能的几点建议：</span></p>
<h1><span style="font-family: 'Microsoft YaHei'; font-size: 18px;">一、选择合适的 Devtool 版本</span></h1>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">&#8203;webpack 的 devtool 配置，决定了在构建过程中怎样生成 sourceMap 文件。通常来说eval的性能最高，但是不能生成的 sourceMap 文件解析出来的代码，和源代码差异较大。&nbsp;source-map 的性能较差，但是可以生成原始版本的代码。 在大多数 Development 场景下 cheap-module-eval-source-map 是最佳的选择。</span></p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">下图是各个 Devtool 配置的对比（+号越多，代表速度越快，-号越多，代表速度越慢, o代表中等速度）</span></p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">&nbsp;<img src="https://images2017.cnblogs.com/blog/139239/201712/139239-20171225115729928-51931115.png" alt=""></span></p>
<p><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">注意* ： 在 production 配置中，如果需要生成 sourceMap 文件来进行异常分析， 应该使用 hidden-source-map 或者 nosources-source-map,&nbsp;source-map 等配置。并且不要把 sourceMap 文件也放在部署目录下。</span></p>
<p>&nbsp;</p>
<h1><span style="font-family: 'Microsoft YaHei'; font-size: 18px;">二、Build Cache</span></h1>
<p><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">Webpack 和一些 Plugin/Loader 都有 Cache 选项。开启 Cache 选项，有利用提高构建性能。</span></p>
<p><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">&#8203;比如：使用 babel-loader 的时候开启 cacheDirectory 选项，会较为明显的提升构建速度</span></p>
<div class="cnblogs_code"><div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div>
<pre><span style="color: #000000;"> module: {
    rules: [{
        test: </span>/\.js$/<span style="color: #000000;">,
        use: [</span><span style="color: #800000;">'</span><span style="color: #800000;">babel-loader?cacheDirectory</span><span style="color: #800000;">'</span><span style="color: #000000;">],
        include: path.join(__dirname, </span><span style="color: #800000;">'</span><span style="color: #800000;">app</span><span style="color: #800000;">'</span><span style="color: #000000;">)
    }]
 }</span></pre>
<div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div></div>
<p>&nbsp;</p>
<h1><span style="font-family: 'Microsoft YaHei'; font-size: 18px;">三、减少代码体积</span></h1>
<ul>
<li><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">使用 CommonsChunksPlugin&nbsp;提取多个 chunk 之间的通用模块，减少总体的代码体积</span></li>
<li><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">把部分依赖转移到 CDN 上，避免在每次编译过程中都由 Webpack 处理</span></li>
<li><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">对于支持局部引入的类库，在开发的过程中使用局部引入的方式，避免引入无用的文件</span></li>
</ul>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">比如 lodash 就支持部分引入：</span></p>
<div class="cnblogs_code">
<pre>import isArray <span style="color: #0000ff;">from</span> <span style="color: #800000;">'</span><span style="color: #800000;">lodash/isArray</span><span style="color: #800000;">'</span>;</pre>
</div>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">参考： [Don't import whole lodash] (<a href="https://github.com/lodash/lodash/issues/3450" target="_blank">https://github.com/lodash/lodash/issues/3450</a>)</span></p>
<p align="left">&nbsp;</p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">&#8203;在进行这一优化手段的时候，可以借助可视化工具进行 chunk 体积和内容的分析。方便进一步调整 webpack 的配置。主要有以下两种方法：</span></p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">1. 使用 webpack 的 profile 命令生成 JSON 文件，并且把 JSON 上传到相应的在线网站进行可视化分析。</span></p>
<div class="cnblogs_code">
<pre><span style="color: #000000;">```bash
webpack </span>--profile --json &gt;<span style="color: #000000;"> stat.json
```</span></pre>
</div>
<p><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">使用&nbsp;<a href="https://chrisbateman.github.io/webpack-visualizer/">webpack-visualizer</a>&nbsp;进行分析：</span></p>
<p><span style="font-family: 'Microsoft YaHei'; font-size: 16px;"><img src="https://images2017.cnblogs.com/blog/139239/201712/139239-20171226100105712-1272621604.png" alt="" width="658" height="613"></span></p>
<p><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">2. 使用第三方 plugin，在编译过程中进行体积分析，并且以图表方式输出：</span></p>
<p><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">推荐使用&nbsp;<a href="https://www.npmjs.com/package/webpack-bundle-analyzer">webpack-bundle-analyzer</a>:</span></p>
<p><span style="font-family: 'Microsoft YaHei'; font-size: 16px;"><img src="https://images2017.cnblogs.com/blog/139239/201712/139239-20171226100142478-364491911.gif" alt="" width="694" height="418"></span></p>
<h1><span style="font-family: 'Microsoft YaHei'; font-size: 18px;">四、减少目录检索范围</span></h1>
<p><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">在使用 loader 的时候，通过指定 exclude 和 incude 选项，减少 loader 遍历的目录范围，从而加快 Webpack 编译速度。</span></p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">比如指定 babel-loader 只处理业务代码：</span></p>
<div class="cnblogs_code">
<pre><span style="color: #000000;">{
   test: </span>/\.js$/<span style="color: #000000;">,
   use: [</span><span style="color: #800000;">'</span><span style="color: #800000;">babel-loader</span><span style="color: #800000;">'</span><span style="color: #000000;">],
   include: path.join(__dirname, </span><span style="color: #800000;">'</span><span style="color: #800000;">app</span><span style="color: #800000;">'</span><span style="color: #000000;">)
}</span></pre>
</div>
<p>&nbsp;</p>
<h1><span style="font-family: 'Microsoft YaHei'; font-size: 18px;">五、减少检索路径</span></h1>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">resolve.alias 可以配置 webpack 模块解析的别名，对于比较深的解析路径，可以对其配置 alias. 可以提升 webpack 的构建速度。</span></p>
<div class="cnblogs_code">
<pre><span style="color: #000000;">alias: {
  Utilities: path.resolve(__dirname, </span><span style="color: #800000;">'</span><span style="color: #800000;">src/utilities/</span><span style="color: #800000;">'</span><span style="color: #000000;">),
  Templates: path.resolve(__dirname, </span><span style="color: #800000;">'</span><span style="color: #800000;">src/templates/</span><span style="color: #800000;">'</span><span style="color: #000000;">)
}</span></pre>
</div>
<p>&nbsp;</p>
<h1><span style="font-family: 'Microsoft YaHei'; font-size: 18px;">六、使用 DllPlugin/DllReferencePlugin 进行预先构建</span></h1>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">&#8203;Webpack 的 DllPlugin 和 DllReferencePlugin 是在新版本中推出的 Plugin，其思路就是把改变频率比较小的第三方库等依赖单独打包构建，在打包整个项目的时候，如果解析到了通过 Dll 形式进行打包的依赖，会在正常的打包过程中跳过，同时把对这些依赖的引入导入到 Dll 模块上去。 这样会大大提升在对业务代码进行打包时候的速度。</span></p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">1. 新建一个单独的 webpack 配置文件，比如 webpack.dll.config.js</span></p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">2. 在这个配置文件中，使用 webpack DllPlugin 生成 manifest.json 文件和 Dll 模块文件。也可以引入诸如 uglifyPlugin 对第三方依赖进行压缩等处理。</span></p>
<div class="cnblogs_code"><div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div>
<pre>import path <span style="color: #0000ff;">from</span> <span style="color: #800000;">'</span><span style="color: #800000;">path</span><span style="color: #800000;">'</span><span style="color: #000000;">;
import pkg </span><span style="color: #0000ff;">from</span> <span style="color: #800000;">'</span><span style="color: #800000;">./package.json</span><span style="color: #800000;">'</span><span style="color: #000000;">;
import webpack </span><span style="color: #0000ff;">from</span> <span style="color: #800000;">'</span><span style="color: #800000;">webpack</span><span style="color: #800000;">'</span><span style="color: #000000;">;
</span><span style="color: #0000ff;">var</span> vendorPackages =<span style="color: #000000;"> Object.keys(pkg.dependencies);
</span><span style="color: #0000ff;">const</span> config =<span style="color: #000000;"> {
entry: {
     vendor: vendorPackages
     },
output: {
     filename: </span><span style="color: #800000;">'</span><span style="color: #800000;">dll.[name].js</span><span style="color: #800000;">'</span><span style="color: #000000;">,
     path: path.resolve(__dirname, </span><span style="color: #800000;">'</span><span style="color: #800000;">build</span><span style="color: #800000;">'</span>, <span style="color: #800000;">'</span><span style="color: #800000;">dll</span><span style="color: #800000;">'</span><span style="color: #000000;">),
     library: </span><span style="color: #800000;">'</span><span style="color: #800000;">[name]</span><span style="color: #800000;">'</span><span style="color: #000000;">
      },
plugins: [
     </span><span style="color: #0000ff;">new</span><span style="color: #000000;"> webpack.DllPlugin({
           context: __dirname,
           name: </span><span style="color: #800000;">"</span><span style="color: #800000;">[name]_[hash]</span><span style="color: #800000;">"</span><span style="color: #000000;">,
           path: path.join(__dirname, </span><span style="color: #800000;">"</span><span style="color: #800000;">manifest.json</span><span style="color: #800000;">"</span><span style="color: #000000;">),
     }),
     </span><span style="color: #0000ff;">new</span><span style="color: #000000;"> webpack.optimize.UglifyJsPlugin({
           sourceMap: </span><span style="color: #0000ff;">true</span><span style="color: #000000;">,
           minimize: </span><span style="color: #0000ff;">true</span><span style="color: #000000;">,
           cache: </span><span style="color: #0000ff;">true</span><span style="color: #000000;">,
           parallel: </span><span style="color: #0000ff;">true</span><span style="color: #000000;">
       }),
     ]
}
&#8203;   export </span><span style="color: #0000ff;">default</span> config;</pre>
<div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div></div>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">3. 在正常的 webpack 配置文件中，使用 webpack DllReferencePlugin 解析上一步生成的 manifest.json</span></p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">new</span><span style="color: #000000;"> webpack.DllReferencePlugin({
        context: path.join(__dirname),
        manifest: require(</span><span style="color: #800000;">'</span><span style="color: #800000;">./manifest.json</span><span style="color: #800000;">'</span><span style="color: #000000;">)
})</span></pre>
</div>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">在具体的使用过成中， 在 Dll 中包含的依赖没有变化的场景下，可以先执行单次 webpack --config webpack.dll.config.js。然后可以多次执行业务代码的构建过程。由于把第三方依赖进行了剥离，业务代码的构建会快很多。</span></p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">以下是一些关于 Webpack 构建性能的文章：</span></p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">1)：<a href="http://engineering.invisionapp.com/post/optimizing-webpack/">使用 DllPlugin 提升性能</a></span></p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">2）:&nbsp;<a href="https://stackoverflow.com/questions/32923085/how-to-optimize-webpacks-build-time-using-prefetchplugin-analyse-tool/33415019#33415019">PrefetchPlugin 的使用</a></span></p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">3）:&nbsp;<a href="https://zhuanlan.zhihu.com/p/25212283">webpack 打包分析与性能优化</a></span></p>
<p align="left"><span style="font-family: 'Microsoft YaHei'; font-size: 16px;">4）:&nbsp;<a href="http://www.alloyteam.com/2016/01/webpack-use-optimization/">webpack 使用优化</a></span></p>
<p align="left"><span style="color: #000000; font-family: 'Microsoft YaHei'; font-size: 16px;">转载请注明出自：葡萄城控件</span></p>
<p align="left">&nbsp;</p>
<p align="left"><span style="font-size: 16px; font-family: 'Microsoft YaHei';" data-mce-=""><strong>相关阅读：</strong></span></p>
<p><a href="http://www.cnblogs.com/powertoolsteam/p/low-code-platform.html" target="_blank"><span style="font-size: 16px; font-family: 'Microsoft YaHei';">基于低代码平台（Low Code Platform）开发中小企业信息化项目</span></a><br><a href="http://www.cnblogs.com/powertoolsteam/p/soapui.html" target="_blank"><span style="font-size: 16px; font-family: 'Microsoft YaHei';">SoapUI实践：自动化测试、压力测试、持续集成</span></a><br><a href="http://www.cnblogs.com/powertoolsteam/p/chart_graph.html" target="_blank"><span style="font-size: 16px; font-family: 'Microsoft YaHei';">图表（Chart &amp; Graph）你真的用对了吗？</span></a></p>
<p align="left">&nbsp;</p></div>
