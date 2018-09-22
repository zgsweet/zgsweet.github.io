<div id="topics">
	<div class="post">
		<h1 class="postTitle">
			<a id="cb_post_title_url" class="postTitle2" href="https://www.cnblogs.com/jadeboy/p/8340190.html">Npm vs Yarn 之备忘大全</a>
		</h1>
		<div class="clear"></div>
		<div class="postBody">
			<div id="cnblogs_post_body" class="blogpost-body cnblogs-markdown"><p>有则笑话，如此讲到：“老丈人爱吃核桃，昨天买了二斤陪妻子送去，老丈人年轻时练过武，用手一拍核桃就碎了，笑着对我说：你还用锤子，你看我用手就成。我嘴一抽，来了句：人和动物最大的区别就是人会使用工具。……”。撇开这样特例场景，这句话还是非常用有道理的；毕竟从远古石器时期或更早，到如今，所言之语，所穿之衣，代步之车，所学的知识，所晓的常识.....皆是工具；可以说绝大部分人之间的差异(天才级除外)，仅在于工具使用之优劣罢了。在工具的使用中，很多人极大程度上停留于会用层面，如若不遇到问题，几乎就处于停滞；这本身倒也没有问题，但可能因为没有透彻的了解，而错失了对该物可以拥有的想象力，从而错过了许多本该有的美好，如此的可惜。</p>
<p>坦白说，在从事前端方面工作，蛮长一段时间内，就因缺乏对 Npm 有足够的认知，使得后来对其诸多讯息，颇感「相见恨晚」；在本篇中，将客观陈述 Npm 与 Yarn 的各自功用，以此显出两者间的差异；同时，以比较的形式，列出「常用命令清单」，以方便使用之时，作为参考(将陆续更新以完善)；同时也欲借此，再次倡导那经典名言：<strong>「工欲善其事，必先利其器」</strong>，与诸君共勉。</p>
<blockquote>
<p>原文出处：<a href="https://jeffjade.com">晚晴幽草轩</a><br>
原文首链：<a href="https://jeffjade.com/2017/12/30/135-npm-vs-yarn-detial-memo/">Npm vs Yarn 之备忘详单</a></p>
</blockquote>
<p><img src="//upload-images.jianshu.io/upload_images/207604-66dab751cd988e3c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240" alt="NPM vs Yarn"></p>
<h2 id="什么是-npmyarn"><strong>什么是 Npm，Yarn</strong></h2>
<h3 id="什么是-npm"><strong>什么是 npm？</strong></h3>
<p><code>npm</code> 即：<a href="https://www.npmjs.com/">npm package manager</a>，是一种重用其他开发人员的代码的方法，也是一种与他人共享代码的方式，并且可以很容易地管理不同版本的代码。<code>npm</code> 开始作为 Node 包管理器，所以你会发现很多模块可以在服务器端使用。也有很多的包添加命令供您在命令行中使用。你还会发现可以在前端使用的软件包。</p>
<p><code>npm</code> 由三个不同的部分组成：网站，注册表和 CLI 。该网站是用户发现软件包的主要工具，注册表是一个关于软件包信息的大型数据库，而 CLI 则是开发者如何在注册表上发布他们的软件包或下载他们希望安装的软件包。更多详细内容，可参见 <a href="https://docs.npmjs.com/getting-started/what-is-npm">what-is-npm</a>。</p>
<h3 id="什么是-yarn"><strong>什么是 yarn？</strong></h3>
<blockquote>
<p><code>Yarn</code> 对你的代码来说是一个包管理器， 你可以通过它使用全世界开发者的代码，或者分享自己的代码。 Yarn 做这些快捷、安全、可靠，所以你不用担心什么。通过 <code>Yarn</code>，你可以使用其他开发者针对不同问题的解决方案，使自己的开发过程更简单。 使用过程中遇到问题，你可以将其上报或者贡献解决方案。一旦问题被修复，Yarn会更新保持同步。</p>
</blockquote>
<p><code>Yarn</code> 是 Facebook, Google, Exponent 和 Tilde 开发的一款新的 JavaScript 包管理工具。它并没有试图完全取代 npm。Yarn 同样是一个从 npm 注册源获取模块的新的 CLI 客户端。注册的方式不会有任何变化 —— 你同样可以正常获取与发布包。它存在的目的是解决团队在使用 <code>npm</code> 面临的少数问题。当然，在 <code>Node</code> 版本断更替中，Npm 本身也在积极更新。</p>
<h2 id="关于安装更新"><strong>关于安装/更新</strong></h2>
<h3 id="如何安装更新-npm"><strong>如何安装/更新 Npm</strong></h3>
<h4 id="如何安装-npm"><strong>如何安装 Npm</strong></h4>
<p><code>npm</code> 开始作为 Node 包管理器，所以它的安装是跟 Node.js 捆绑在一起的。至于如何安装 Node.js, Npm 官方，在 <a href="https://docs.npmjs.com/getting-started/installing-node">Installing Node.js and updating npm</a> 做了阐述。之前在不同平台尝试更新 Node.js 之时，也是遇到过各种问题，有在 <a href="http://www.jianshu.com/p/019b10b948b6">NodeJs 升级/安装折腾记</a> 一文做了记载；折腾许久，得出的结论跟官网一致：</p>
<blockquote>
<p>如果您使用的是OS X或Windows，安装Node.js的最佳方法是：使用 <a href="https://nodejs.org/en/download/">Node.js下载页面</a>中的一个安装程序。(笔者微注：如是我中国大陆用户，去<a href="https://npm.taobao.org/mirrors/node">淘宝 Node.js 镜像</a>下载，会是快速的法子)。</p>
</blockquote>
<h4 id="如何更新-npm"><strong>如何更新 Npm</strong></h4>
<ol>
<li>npm install npm@latest -g （npm install npm -g）</li>
<li>更新(重新下载) Node.js</li>
</ol>
<h4 id="如何安装-yarn"><strong>如何安装 Yarn</strong></h4>
<p>对于如何安装 <code>Yarn</code>，Yarn 官方给出了很全面的说明，详见 <a href="https://yarnpkg.com/zh-Hans/docs/install">Install Yarn</a>；涵盖 MacOs，Windows，Linux 等平台，并且还给出一些备用安装方式，譬如通过 <code>npm</code> 来安装：</p>
<pre><code class="hljs coffeescript"><span class="hljs-built_in">npm</span> install --<span class="hljs-built_in">global</span> yarn</code></pre>
<p>当然，<code>Yarn</code> 官方在 <a href="https://yarnpkg.com/zh-Hans/docs/install#alternatives-tab">Yarn 备选安装方式</a>有明确讲道：</p>
<blockquote>
<p>一般来说, 不推荐通过 <code>npm</code> 安装 <code>Yarn</code>，在用基于 Node 的包管理器安装 Yarn 时，该包未被签名， 并且只通过基本的 <code>SHA1</code> 散列进行唯一完整性检查。这在安装系统级应用时有安全风险。因为这些原因，高度推荐用你的操作系统最适合的方式来安装 Yarn。</p>
</blockquote>
<p>但在实际使用中，这倒是最为方便的方式之一，迄今倒也没遇到什么问题；当然，最好按照官方推荐的方式；如果你使用并熟悉 Mac 操作系统，用推荐方式安装 Yarn 也是很简单：<code>brew install yarn</code>(笔者注)。</p>
<h3 id="如何更新-yarn"><strong>如何更新 Yarn</strong></h3>
<p>对于如何更新 Yarn，可以结合安装时候对应命令；如果是 Mac 操作系统，使用 <code>brew</code> 安装，那么如此操作予以更新：</p>
<pre><code class="hljs nginx"><span class="hljs-attribute">brew</span> upgrade yarn</code></pre>
<p>如果 <code>Yarn</code> 通过 Debian / Ubuntu 包安装，则可以运行如下命令予以更新：</p>
<pre><code class="hljs sql">sudo apt-get <span class="hljs-keyword">update</span> &amp;&amp; sudo apt-<span class="hljs-keyword">get</span> <span class="hljs-keyword">install</span> yarn</code></pre>
<p>也可以使用 <code>yarn</code> 本身来更新自己：</p>
<pre><code class="hljs python">yarn <span class="hljs-keyword">global</span> add yarn</code></pre>
<p>如果有意了解更多如何更新 <code>yarn</code> 的方法，可参见：<a href="https://github.com/yarnpkg/yarn/issues/1139">yarn self-update should update using the same installation method originally used</a>。</p>
<h2 id="npm-与-yarn-常用命令对比"><strong>npm 与 yarn 常用命令对比</strong></h2>
<h3 id="有所区别的命令"><strong>有所区别的命令</strong></h3>
<table>
<thead>
<tr class="header">
<th style="text-align: left;">Npm</th>
<th style="text-align: left;">Yarn</th>
<th style="text-align: left;">功能描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">npm install(npm i)</td>
<td style="text-align: left;">yarn install(yarn)</td>
<td style="text-align: left;">根据 package.json 安装所有依赖</td>
</tr>
<tr class="even">
<td style="text-align: left;">npm i --save [package]</td>
<td style="text-align: left;">yarn add [package]</td>
<td style="text-align: left;">添加依赖包</td>
</tr>
<tr class="odd">
<td style="text-align: left;">npm i --save-dev [package]</td>
<td style="text-align: left;">yarn add [package] --dev</td>
<td style="text-align: left;">添加依赖包至 devDependencies</td>
</tr>
<tr class="even">
<td style="text-align: left;">npm i -g [package]</td>
<td style="text-align: left;">yarn global add [package]</td>
<td style="text-align: left;">进行全局安装依赖包</td>
</tr>
<tr class="odd">
<td style="text-align: left;">npm update --save</td>
<td style="text-align: left;">yarn upgrade [package]</td>
<td style="text-align: left;">升级依赖包</td>
</tr>
<tr class="even">
<td style="text-align: left;">npm uninstall [package]</td>
<td style="text-align: left;">yarn remove [package]</td>
<td style="text-align: left;">移除依赖包</td>
</tr>
</tbody>
</table>
<h3 id="相同操作的命令"><strong>相同操作的命令</strong></h3>
<table>
<thead>
<tr class="header">
<th style="text-align: left;">Npm</th>
<th style="text-align: left;">Yarn</th>
<th style="text-align: left;">功能描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">npm run</td>
<td style="text-align: left;">yarn run</td>
<td style="text-align: left;">运行 package.json 中预定义的脚本</td>
</tr>
<tr class="even">
<td style="text-align: left;">npm config list</td>
<td style="text-align: left;">yarn config list</td>
<td style="text-align: left;">查看配置信息</td>
</tr>
<tr class="odd">
<td style="text-align: left;">npm config set registry 仓库地址</td>
<td style="text-align: left;">yarn config set registry 仓库地址</td>
<td style="text-align: left;">更换仓库地址</td>
</tr>
<tr class="even">
<td style="text-align: left;">npm init</td>
<td style="text-align: left;">yarn init</td>
<td style="text-align: left;">互动式创建/更新 package.json 文件</td>
</tr>
<tr class="odd">
<td style="text-align: left;">npm list</td>
<td style="text-align: left;">yarn list</td>
<td style="text-align: left;">查看当前目录下已安装的node包</td>
</tr>
<tr class="even">
<td style="text-align: left;">npm login</td>
<td style="text-align: left;">yarn login</td>
<td style="text-align: left;">保存你的用户名、邮箱</td>
</tr>
<tr class="odd">
<td style="text-align: left;">npm logout</td>
<td style="text-align: left;">yarn logout</td>
<td style="text-align: left;">删除你的用户名、邮箱</td>
</tr>
<tr class="even">
<td style="text-align: left;">npm outdated</td>
<td style="text-align: left;">yarn outdated</td>
<td style="text-align: left;">检查过时的依赖包</td>
</tr>
<tr class="odd">
<td style="text-align: left;">npm link</td>
<td style="text-align: left;">yarn link</td>
<td style="text-align: left;">开发时链接依赖包，以便在其他项目中使用</td>
</tr>
<tr class="even">
<td style="text-align: left;">npm unlink</td>
<td style="text-align: left;">yarn unlink</td>
<td style="text-align: left;">取消链接依赖包</td>
</tr>
<tr class="odd">
<td style="text-align: left;">npm publish</td>
<td style="text-align: left;">yarn publish</td>
<td style="text-align: left;">将包发布到 npm</td>
</tr>
<tr class="even">
<td style="text-align: left;">npm test</td>
<td style="text-align: left;">yarn test</td>
<td style="text-align: left;">测试 = yarn run test</td>
</tr>
<tr class="odd">
<td style="text-align: left;">npm bin</td>
<td style="text-align: left;">yarn bin</td>
<td style="text-align: left;">显示 bin 文件所在的安装目录</td>
</tr>
<tr class="even">
<td style="text-align: left;">yarn info <package></package></td>
<td style="text-align: left;">yarn info <package></package></td>
<td style="text-align: left;">显示一个包的信息</td>
</tr>
</tbody>
</table>
<p>对于以上还须对于，还须做如下补充性说明：</p>
<ul>
<li>在 npm 中，可以使用 npm config set save true 设置 —-save 为默认行为，但这对多数开发者而言，并非显而易见的。而使用 yarn，在package.json 中添加（add）和移除（remove）等行为是默认的。</li>
<li><p>对于要添加或升级的包，npm 与 yarn 都可以指定具体的版本，或者 Tag；如：</p>
<blockquote>
<p>yarn add [package]@[version]<br>
yarn add [package]@[tag]</p>
</blockquote></li>
<li><p>在国内，使用 npm，最好还是替换成淘宝的镜像，如此网络影响减小到最低，这样安装依赖包的速度，可以得到蛮大的改善：</p>
<blockquote>
<p>npm config set registry http://registry.npm.taobao.org<br>
yarn config set registry http://registry.npm.taobao.org</p>
</blockquote>
<p>当然也可以设置别名 <code>cnpm</code>：</p>
<pre><code class="hljs bash"><span class="hljs-built_in">alias</span> cnpm=<span class="hljs-string">"npm --registry=http://registry.cnpmjs.org --cache=<span class="hljs-variable">$HOME</span>/.npm/.cache/cnpm"</span></code></pre></li>
</ul>
<h3 id="yarn-独有的命令"><strong>Yarn 独有的命令</strong></h3>
<ul>
<li><a href="https://yarnpkg.com/zh-Hans/docs/cli/import">yarn import</a>：依据原npm安装后的<code>node_modules</code>目录生成一份<code>yarn.lock</code>文件；</li>
<li><a href="https://yarnpkg.com/zh-Hans/docs/cli/licenses">yarn licenses</a>：列出已安装包的许可证信息；</li>
<li><a href="https://yarnpkg.com/zh-Hans/docs/cli/pack">yarn pack</a>：创建一个压缩的包依赖 gzip 档案；</li>
<li><a href="https://yarnpkg.com/zh-Hans/docs/cli/why">yarn why</a>：显示有关一个包为何被安装的信息。</li>
<li><a href="https://yarnpkg.com/zh-Hans/docs/cli/autoclean">yarn autoclean</a>：从包依赖里清除并移除不需要的文件。</li>
<li>......</li>
</ul>
<h2 id="npm-使用之额外技巧"><strong>npm 使用之额外技巧</strong></h2>
<h3 id="如何寻找适宜的-npm-包"><strong>如何寻找适宜的 npm 包</strong></h3>
<p>找到合适的软件包可能相当具有挑战性 ——，毕竟有成千上万个模块供你选择。https://npms.io/ ，这个网站的存在，让这项任务轻松很多；它显示了<strong>质量</strong>，<strong>受欢迎程度</strong>和<strong>维护</strong>等指标。这些计算是基于模块是否具有过时的依赖关系，是否配置了linters，是否包含测试或是否进行了最近的提交。</p>
<h3 id="执行-npm-包的二进制文件"><strong>执行 npm 包的二进制文件</strong></h3>
<p>显而易见，经由 <code>npm</code> 或是 <code>yarn</code> 安装，并被放置在 <code>./node_modules</code> 目录中的包，其二进制可执行文件可访问 <code>./node_modules/.bin</code>，那么该如何从项目根目录中调用它呢？以下提供了几种方式，你可以从中任意选择一种，来达到你的目的：</p>
<p>为了方便举例，这里以运行 <a href="https://github.com/nicejade/responsive-email-template">responsive-email-template</a>（制作更好的响应式邮件模板）作为示例来作说明；其中有用到 <a href="https://github.com/mjmlio/mjml">mjml</a> 这个库；此库被推荐的方式是在本地安装和使用；所以，要运行对应命令，你可以操作她，使用以下办法：</p>
<ul>
<li><strong>古老而原始的办法</strong></li>
</ul>
<p>在你安装 MJML 的文件夹中，你现在可以运行：</p>
<pre><code class="hljs delphi">./node_modules/.bin/mjml --watch src/<span class="hljs-keyword">index</span>.mjml -o dist/<span class="hljs-keyword">index</span>.html</code></pre>
<ul>
<li><strong>将 <code>./node_modules/.bin/</code> 添加至环境变量</strong></li>
</ul>
<pre><code class="hljs perl">export PATH=<span class="hljs-string">"$PATH:./node_modules/.bin"</span>
mjml --watch src/<span class="hljs-keyword">index</span>.mjml -o dist/<span class="hljs-keyword">index</span>.html</code></pre>
<ul>
<li><strong>或者使用快捷键 <code>npm bin</code></strong></li>
</ul>
<pre><code class="hljs delphi">$(npm bin)/mjml --watch src/<span class="hljs-keyword">index</span>.mjml -o dist/<span class="hljs-keyword">index</span>.html</code></pre>
<ul>
<li><strong>或者利用 npm 脚本命令</strong></li>
</ul>
<pre><code class="hljs cpp"><span class="hljs-comment">// 将命令配置在 package.json 文件，使用 scripts 字段定义脚本命令</span>
<span class="hljs-string">"scripts"</span>: {
  <span class="hljs-string">"mjml"</span>: <span class="hljs-string">"mjml --watch src/index.mjml -o dist/index.html"</span>
}

<span class="hljs-comment">// 使用之时，只需运行如下命令即可：</span>
npm run mjml</code></pre>
<ul>
<li><strong>或者通过使用 <a href="https://github.com/zkat/npx">npx</a></strong></li>
</ul>
<blockquote>
<p>注意：<a href="https://github.com/zkat/npx">npx</a> 包含在 <code>npm &gt; v5.2</code>，或可以分开安装。</p>
</blockquote>
<pre><code class="hljs perl"><span class="hljs-comment"># npm install -g npx</span>
npx mjml --watch src/<span class="hljs-keyword">index</span>.mjml -o dist/<span class="hljs-keyword">index</span>.html</code></pre>
<h2 id="强大如斯npm-脚本">强大如斯，npm 脚本</h2>
<p>npm（Yarn 亦同）允许在 <code>package.json</code> 文件里面，使用 <code>scripts</code> 字段定义脚本命令。它支持通配符、<strong>变量</strong>、钩子、外部传参、支持并发 &amp; 异步执行等等；所以，完全可以借助 <code>npm script</code>，打造属于自己的高效工作流。鉴于篇幅，这部分就不在这里多做赘述，具体使用以及运行原理等，可以参见 @阮一峰 所写的文章：<a href="http://www.ruanyifeng.com/blog/2016/10/npm_scripts.html">npm scripts 使用指南</a>。</p>
<p>具体例子来说，有些时候会有需求要删除 Git 仓库所有提交历史，而保留代码为当前状态；而删除 <code>.git</code> 文件夹可能会导致您的 git 存储库中的问题；所以可以使用另一种更为安全的办法：详见<a href="https://jeffjade.com/2014/12/22/2014-12-22-gitmemo/如何删除%20Git%20仓库所有提交历史记录">如何删除 Git 仓库所有提交历史记录</a>。但这个操作一套打下来，不免劳神费力。那么借助 <code>npm script</code>，运行如下命令，一键搞定（当然命令可自行定义）；如果你有需求执行更多，也可以在后面追加更多操作。</p>
<pre><code class="hljs cpp"><span class="hljs-string">"scripts"</span>: {
  <span class="hljs-string">"clean-commit"</span>: <span class="hljs-string">"git checkout --orphan latest_branch &amp;&amp; git add -A &amp;&amp; git commit -am 'clean past commit history 😊' &amp;&amp; git branch -D master &amp;&amp; git branch -m master &amp;&amp; git push -f origin master"</span>
}

<span class="hljs-comment">// 或者也可以将其作下拆解，譬如像这样：</span>
<span class="hljs-string">"scripts"</span>: {
  <span class="hljs-string">"recommit"</span>: <span class="hljs-string">"git add -A &amp;&amp; git commit -am 'clean past commit history 😊'"</span>,
  <span class="hljs-string">"repush"</span>: <span class="hljs-string">"git branch -D master &amp;&amp; git branch -m master &amp;&amp; git push -f origin master"</span>,
  <span class="hljs-string">"clean-commit"</span>: <span class="hljs-string">"git checkout --orphan latest_branch &amp;&amp; npm run recommit &amp;&amp; repush"</span>
}</code></pre>
<h3 id="如何探查-npm-包"><strong>如何探查 npm 包</strong></h3>
<p>一旦我们选择了我们的模块，我们应该看看文档，并检查开放的问题，以更好地了解我们将要在我们的应用程序中需要什么。不要忘记，您使用的 npm 包越多，存在易受攻击或恶意攻击的风险就越高。</p>
<p>如果你想从cli打开模块的主页，你可以这样做：</p>
<pre><code class="hljs coffeescript"><span class="hljs-built_in">npm</span> home axios</code></pre>
<p>要检查未决的问题或公开的路线图（如果有的话），你可以试试这个：</p>
<pre><code class="hljs coffeescript"><span class="hljs-built_in">npm</span> bugs axios</code></pre>
<p>另外，如果你只是想检查模块的 git 仓库，请输入：</p>
<pre><code class="hljs coffeescript"><span class="hljs-built_in">npm</span> repo axios</code></pre>
<h2 id="关于-package-lock.json-和-yarn.lock"><strong>关于 package-lock.json 和 yarn.lock</strong></h2>
<h3 id="关于-yarn.lock"><strong>关于 yarn.lock</strong></h3>
<p>有时候一个项目周期很长，在不断开发的同时，而依赖的库也会有很大改变；有时候你可能只想运行 <code>npm i</code> 更新没有下载的插件，却不想偶尔会将依赖的一些其他插件更到最新，导致各种奇葩问题；<code>package-lock.json</code> 和 <code>yarn.lock</code> 就是为解决这种问题而设定的存在。</p>
<p>使用 <code>npm</code> 或者 <code>yarn</code>，都会有 <code>pacakge.json</code> 这个文件，用以标出自己项目对 各库包的依赖。举个例子来说，你的项目中有如下依赖：</p>
<pre><code class="hljs cpp"><span class="hljs-string">"dependencies"</span>: {
    <span class="hljs-string">"jade-package"</span>: <span class="hljs-string">"^2.3.4"</span>
}</code></pre>
<p>这其中的 <strong>^</strong> 是定义了向后(新)兼容依赖；在 <code>npm&lt;5.0</code> 以前，如果 <em>jade-package</em> 的版本超过<em>2.3.4</em>，并在大版本号（2）上相同，就允许下载最新版本的 <em>jade-package</em> 库包，例如实际上可能运行<code>npm i</code>时候，下载的具体版本可能是<em>2.5.8</em>。</p>
<p>多数情况下，这种向后兼容依赖下载最新库包，是没有问题的；然而，因为 <code>npm</code> 是开源世界，各库包的版本语义可能并不相同，不是所有开发者都能严格遵守这一原则：<strong>相同大版本号的同一个库包，其接口符合兼容要求</strong>。而且，不同的库包之间也存在其他依赖。理想状态下使用语义化版本发布补丁不会包含大的变化，但不幸的是这必非真理。npm 的这种策略，有可能导致两台拥有相同 <code>package.json</code> 文件的机子，实际上安装了不同版本的包，这可能导致一些错误。有时候，相同机器稍不留神的一个 <code>npm i</code>，就可能导致 <em>node_modules</em> 中安装的实际依赖被更新，也就可能导致项目运行呈现，被面目全非。</p>
<p><code>yarn.lock</code> 就是为解决此问题而衍生的存在；为了跨机器安装得到一致的结果，Yarn 需要比你配置在 package.json 中的依赖列表更多的信息。 Yarn 需要准确存储每个安装的依赖是哪个版本；它类似于 npm 的 npm-shrinkwrap.json，并且无副作用。只是需要注意的是：</p>
<blockquote>
<p><code>yarn.lock</code> 文件是自动产生的，而且应该完全被 <code>Yarn</code> 管理。 当你用 Yarn CLI 增加／升级／删除依赖，它将自动更新你的 <code>yarn.lock</code> 文件。 不要直接编辑这个文件，那样很容易弄坏某些东西。</p>
</blockquote>
<h3 id="关于-package-lock.json"><strong>关于 package-lock.json</strong></h3>
<p>当 <code>Node.js</code> 升级之 <strong>v8.0</strong> 以后，自带的 npm 也升级到了5.0；带来速度上很大提升之外，也带来了其他很大变大；这其中就包括 <code>package-lock.json</code>：安装模块操作（改变 node_modules 文件夹内容）会生成或更新 <strong>package-lock.json</strong> 文件；<code>package-lock.json</code> 之于 <strong>npm</strong>，即是<code>yarn.lcok</code> 之于 <strong>yarn</strong> 的翻版；更多信息可参见 <a href="https://docs.npmjs.com/files/package-lock.json">npm package-lock.json</a>。</p>
<p>另外，值得一提的是，在 Github 上有人专门提供了 <a href="https://github.com/imsnif/synp">Synp</a> 工具，用以：将yarn.lock转换为package-lock.json，反之亦然（Convert yarn.lock to package-lock.json and vice versa）。</p>
<h2 id="写在文章的最后"><strong>写在文章的最后</strong></h2>
<p>相比 Npm 的默认配置，Yarn 获赞颇多。用其可以方便生成锁文件，安装依赖非常迅速，且会自动添加进 package.json，同时安装与使用 Yarn 的成本也极小，这使得 Yarn 可以完美替代 npm。yarn 之于 npm，有点像当年的 io.js 和 node.js，殊途同归，都是为了进一步解放和优善生产力；如今，在 Yarn 的影响下，npm 本身也改善不少(version &gt;= 5.0)。最后要说的是，不管用何种工具，全面了解其全貌，知其优晓其劣，方能更好驾驭它，使之为自己高效、快意的生活增姿添色。</p>
<p>@2017-12-30 于深圳.南山 Last Modify： 2018-01-02</p>
<hr>
<h3 id="您可能会感兴趣的文章">您可能会感兴趣的文章：</h3>
<ul>
<li><a href="http://www.jeffjade.com/2015/10/19/2015-10-18-chrome-vimium/">Vimium~让您的Chrome起飞</a></li>
<li><a href="http://www.jeffjade.com/2016/03/17/2016-03-17-jade-tools/">那些所倚靠的利器记载</a></li>
<li><a href="http://www.jeffjade.com/2016/03/11/2016-03-11-autohotkey/#">Win下最爱效率神器:AutoHotKey</a></li>
<li><a href="http://www.jeffjade.com/2016/01/13/2016-01-13-windows-software-cmder/">Win下必备神器之Cmder</a></li>
<li><a href="http://www.jeffjade.com/2016/03/03/2016-03-02-how-to-use-atom/">新编码神器Atom使用纪要</a></li>
<li><a href="http://www.cnblogs.com/jadeboy/p/4165449.html">sublime text 下的Markdown写作</a></li>
<li><a href="http://www.jeffjade.com/2015/08/28/2015-08-28-Write-Morkdown/">SublimeText下写作利器之MarkdownEditing</a></li>
<li><a href="http://www.jeffjade.com/2015/07/29/2015-07-29-mac-musthave-software/">Mac必备软件渐集之ZSH－终极Shell</a></li>
</ul>
</div><div id="MySignature" style="display: block;"><a href="https://nicelinks.site/?from=jadeboy-autograph" title="倾城之链 | NICE LINKS" target="_blank"><img class="width-block-wrap" style="width: 100%; max-height: 300px" src="https://image.nicelinks.site/nicelinks-popularize.png" alt="倾城之链 | NICE LINKS"> </a>
<a style="display: inline-block; margin-top: 20px" href="//click.dji.com/AEuogBLf6UXhccqUaT0NVg?pm=ad_image" title="大疆无人机" target="_blank"><img class="width-block-wrap" style="width: 100%; max-height: 250px" src="//u.djicdn.com/uploads/ad_image_file/file/992/970___250.jpg" alt="DJI Mavic Air"></a></div>
<div class="clear"></div>
<div id="blog_post_info_block">
<div id="BlogPostCategory">分类: <a href="http://www.cnblogs.com/jadeboy/category/620011.html" target="_blank">Coding工具进阶</a>,<a href="http://www.cnblogs.com/jadeboy/category/720647.html" target="_blank">web进阶篇</a></div>
<div id="EntryTag">标签: <a href="http://www.cnblogs.com/jadeboy/tag/npm/">npm</a>, <a href="http://www.cnblogs.com/jadeboy/tag/yarn/">yarn</a>, <a href="http://www.cnblogs.com/jadeboy/tag/%E5%89%8D%E7%AB%AF/">前端</a></div>
<div id="blog_post_info"><div id="green_channel">
        <a href="javascript:void(0);" id="green_channel_digg" onclick="DiggIt(8340190,cb_blogId,1);green_channel_success(this,'谢谢推荐！');">好文要顶</a>
            <a id="green_channel_follow" onclick="follow('b0a9565a-2606-e311-8d02-90b11c0b17d6');" href="javascript:void(0);">关注我</a>
    <a id="green_channel_favorite" onclick="AddToWz(cb_entryId);return false;" href="javascript:void(0);">收藏该文</a>
    <a id="green_channel_weibo" href="javascript:void(0);" title="分享至新浪微博" onclick="ShareToTsina()"><img src="//common.cnblogs.com/images/icon_weibo_24.png" alt=""></a>
    <a id="green_channel_wechat" href="javascript:void(0);" title="分享至微信" onclick="shareOnWechat()"><img src="//common.cnblogs.com/images/wechat.png" alt=""></a>
</div>
<div id="author_profile">
    <div id="author_profile_info" class="author_profile_info">
            <a href="http://home.cnblogs.com/u/jadeboy/" target="_blank"><img src="//pic.cnblogs.com/face/558479/20160314130847.png" class="author_avatar" alt=""></a>
        <div id="author_profile_detail" class="author_profile_info">
            <a href="http://home.cnblogs.com/u/jadeboy/">云轩奕鹤</a><br>
            <a href="http://home.cnblogs.com/u/jadeboy/followees">关注 - 15</a><br>
            <a href="http://home.cnblogs.com/u/jadeboy/followers">粉丝 - 194</a>
        </div>
    </div>
    <div class="clear"></div>
    <div id="author_profile_honor"></div>
    <div id="author_profile_follow">
                <a href="javascript:void(0);" onclick="follow('b0a9565a-2606-e311-8d02-90b11c0b17d6');return false;">+加关注</a>
    </div>
</div>
<div id="div_digg">
    <div class="diggit" onclick="votePost(8340190,'Digg')">
        <span class="diggnum" id="digg_count">3</span>
    </div>
    <div class="buryit" onclick="votePost(8340190,'Bury')">
        <span class="burynum" id="bury_count">0</span>
    </div>
    <div class="clear"></div>
    <div class="diggword" id="digg_tips">
    </div>
</div>
<script type="text/javascript">
    currentDiggType = 0;
</script></div>
<div class="clear"></div>
<div id="post_next_prev"><a href="http://www.cnblogs.com/jadeboy/p/7654814.html" class="p_n_p_prefix">« </a> 上一篇：<a href="http://www.cnblogs.com/jadeboy/p/7654814.html" title="发布于2017-10-12 10:14">与时俱进版前端资源教程</a><br><a href="http://www.cnblogs.com/jadeboy/p/9075003.html" class="p_n_p_prefix">» </a> 下一篇：<a href="http://www.cnblogs.com/jadeboy/p/9075003.html" title="发布于2018-05-23 08:44">高效开发 Web 单页应用解决方案</a><br></div>
</div>


		</div>
		<div class="postDesc">posted @ <span id="post-date">2018-01-24 10:05</span> <a href="http://www.cnblogs.com/jadeboy/">云轩奕鹤</a> 阅读(<span id="post_view_count">176</span>) 评论(<span id="post_comment_count">2</span>)  <a href="https://i.cnblogs.com/EditPosts.aspx?postid=8340190" rel="nofollow">编辑</a> <a href="#" onclick="AddToWz(8340190);return false;">收藏</a></div>
	</div>
	<script src="//common.cnblogs.com/highlight/9.1.0/highlight.min.js?id=20160127"></script><script>markdown_highlight();</script><script type="text/javascript">var allowComments=true,cb_blogId=160536,cb_entryId=8340190,cb_blogApp=currentBlogApp,cb_blogUserGuid='b0a9565a-2606-e311-8d02-90b11c0b17d6',cb_entryCreatedDate='2018/1/24 10:05:00';loadViewCount(cb_entryId);var cb_postType=1;</script>
	
</div>
