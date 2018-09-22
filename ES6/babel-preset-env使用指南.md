<div class="postBody">
			<div id="cnblogs_post_body" class="blogpost-body cnblogs-markdown"><h2 id="文章概览">文章概览</h2>
<p>babel-preset-env是非常重要且常用的一个插件预设，掌握它的用法以及实现原理非常有必要。</p>
<p>本文主要内容包括：babel-preset-env是什么、入门实例、如何配置以支持特定版本的 node/浏览器、实现原理等。</p>
<p>本文所有例子可以在 <a href="https://github.com/chyingp/blog/tree/master/demo/2018.06.02-babel-preset-env">笔者的github</a> 找到。</p>
<h2 id="babel-preset-env简介">babel-preset-env简介</h2>
<p>首先，介绍下历史背景，对了解和学习 babel-preset-env 有帮助。</p>
<p>最初，为了让开发者能够尽早用上新的JS特性，babel团队开发了babel-preset-latest。这个preset比较特殊，它是多个preset的集合(es2015+)，并且随着ECMA规范的更新更增加它的内容。</p>
<p>比如，当前(2018.06.02)，它包含的preset包括：es2017、es1016、es2015。</p>
<p>到了明年，可能它包含的preset就包括：es2018、es2017、es2016、es2015。</p>
<p>随着时间的推移，babel-preset-latest 包含的插件越来越多，这带来了如下问题：</p>
<ol>
<li>加载的插件越来越多，编译速度会越来越慢；</li>
<li>随着用户浏览器的升级，ECMA规范的支持逐步完善，编译至低版本规范的必要性在减少（比如ES6 -&gt; ES5），多余的转换不单降低执行效率，还浪费带宽。</li>
</ol>
<p>因为上述问题的存在，babel官方推出了babel-preset-env插件。它可以根据开发者的配置，按需加载插件。配置项大致包括：</p>
<ol>
<li>需要支持的平台：比如node、浏览器等。</li>
<li>需要支持的平台的版本：<a href="mailto:比如支持node@6.1等">比如支持node@6.1等</a>。</li>
</ol>
<p>默认配置的情况下，它跟 babel-preset-latest 是等同的，会加载从es2015开始的所有preset。</p>
<h2 id="入门例子">入门例子</h2>
<p>首先，安装依赖。</p>
<div class="sourceCode"><pre class="sourceCode bash"><code class="sourceCode bash"><span class="kw">npm</span> install babel-cli --save-dev
<span class="kw">npm</span> install babel-preset-env --save-dev</code></pre></div>
<p>创建 index.js。</p>
<div class="sourceCode"><pre class="sourceCode javascript"><code class="sourceCode javascript"><span class="kw">let</span> foo <span class="op">=</span> () <span class="op">=&gt;</span> <span class="st">'foo'</span><span class="op">;</span></code></pre></div>
<p>配置文件 .babelrc 如下，当前为默认配置。</p>
<div class="sourceCode"><pre class="sourceCode json"><code class="sourceCode json"><span class="fu">{</span>
  <span class="dt">"presets"</span><span class="fu">:</span> <span class="ot">[</span> <span class="st">"env"</span> <span class="ot">]</span>
<span class="fu">}</span></code></pre></div>
<p>运行转换命令</p>
<div class="sourceCode"><pre class="sourceCode bash"><code class="sourceCode bash"><span class="kw">`npm</span> bin<span class="kw">`/babel</span> index.js</code></pre></div>
<p>转换结果如下：</p>
<div class="sourceCode"><pre class="sourceCode javascript"><code class="sourceCode javascript"><span class="st">'use strict'</span><span class="op">;</span>

<span class="kw">var</span> foo <span class="op">=</span> <span class="kw">function</span> <span class="at">foo</span>() <span class="op">{</span>
  <span class="cf">return</span> <span class="st">'foo'</span><span class="op">;</span>
<span class="op">};</span></code></pre></div>
<h2 id="针对node版本的配置">针对node版本的配置</h2>
<p>前面提到，babel-preset-env 提供了更精细化的配置，以提升编译速度，同时减少代码冗余。</p>
<p>我们看下实际例子。假设当前有如下代码：</p>
<pre><code>// index.js
async function foo () {}</code></pre>
<p>采用 babel-preset-env，默认配置下，输出的转换结果如下（具体内容不用关心，知道很长就行了）。</p>
<div class="sourceCode"><pre class="sourceCode javascript"><code class="sourceCode javascript"><span class="st">"use strict"</span><span class="op">;</span>

<span class="kw">var</span> foo <span class="op">=</span> <span class="kw">function</span> () <span class="op">{</span>
  <span class="kw">var</span> _ref <span class="op">=</span> <span class="at">_asyncToGenerator</span>( <span class="co">/*#__PURE__*/</span><span class="va">regeneratorRuntime</span>.<span class="at">mark</span>(<span class="kw">function</span> <span class="at">_callee</span>() <span class="op">{</span>
    <span class="cf">return</span> <span class="va">regeneratorRuntime</span>.<span class="at">wrap</span>(<span class="kw">function</span> <span class="at">_callee$</span>(_context) <span class="op">{</span>
      <span class="cf">while</span> (<span class="dv">1</span>) <span class="op">{</span>
        <span class="cf">switch</span> (<span class="va">_context</span>.<span class="at">prev</span> <span class="op">=</span> <span class="va">_context</span>.<span class="at">next</span>) <span class="op">{</span>
          <span class="cf">case</span> <span class="dv">0</span><span class="op">:</span>
          <span class="cf">case</span> <span class="st">"end"</span><span class="op">:</span>
            <span class="cf">return</span> <span class="va">_context</span>.<span class="at">stop</span>()<span class="op">;</span>
        <span class="op">}</span>
      <span class="op">}</span>
    <span class="op">},</span> _callee<span class="op">,</span> <span class="kw">this</span>)<span class="op">;</span>
  <span class="op">}</span>))<span class="op">;</span>

  <span class="cf">return</span> <span class="kw">function</span> <span class="at">foo</span>() <span class="op">{</span>
    <span class="cf">return</span> <span class="va">_ref</span>.<span class="at">apply</span>(<span class="kw">this</span><span class="op">,</span> arguments)<span class="op">;</span>
  <span class="op">};</span>
<span class="op">}</span>()<span class="op">;</span>

<span class="kw">function</span> <span class="at">_asyncToGenerator</span>(fn) <span class="op">{</span> <span class="cf">return</span> <span class="kw">function</span> () <span class="op">{</span> <span class="kw">var</span> gen <span class="op">=</span> <span class="va">fn</span>.<span class="at">apply</span>(<span class="kw">this</span><span class="op">,</span> arguments)<span class="op">;</span> <span class="cf">return</span> <span class="kw">new</span> <span class="at">Promise</span>(<span class="kw">function</span> (resolve<span class="op">,</span> reject) <span class="op">{</span> <span class="kw">function</span> <span class="at">step</span>(key<span class="op">,</span> arg) <span class="op">{</span> <span class="cf">try</span> <span class="op">{</span> <span class="kw">var</span> info <span class="op">=</span> gen[key](arg)<span class="op">;</span> <span class="kw">var</span> value <span class="op">=</span> <span class="va">info</span>.<span class="at">value</span><span class="op">;</span> <span class="op">}</span> <span class="cf">catch</span> (error) <span class="op">{</span> <span class="at">reject</span>(error)<span class="op">;</span> <span class="cf">return</span><span class="op">;</span> <span class="op">}</span> <span class="cf">if</span> (<span class="va">info</span>.<span class="at">done</span>) <span class="op">{</span> <span class="at">resolve</span>(value)<span class="op">;</span> <span class="op">}</span> <span class="cf">else</span> <span class="op">{</span> <span class="cf">return</span> <span class="va">Promise</span>.<span class="at">resolve</span>(value).<span class="at">then</span>(<span class="kw">function</span> (value) <span class="op">{</span> <span class="at">step</span>(<span class="st">"next"</span><span class="op">,</span> value)<span class="op">;</span> <span class="op">},</span> <span class="kw">function</span> (err) <span class="op">{</span> <span class="at">step</span>(<span class="st">"throw"</span><span class="op">,</span> err)<span class="op">;</span> <span class="op">}</span>)<span class="op">;</span> <span class="op">}</span> <span class="op">}</span> <span class="cf">return</span> <span class="at">step</span>(<span class="st">"next"</span>)<span class="op">;</span> <span class="op">}</span>)<span class="op">;</span> <span class="op">};</span> <span class="op">}</span></code></pre></div>
<p><a href="mailto:如果我们的代码是打算跑在node@8.9.3版本上">如果我们的代码是打算跑在node@8.9.3版本上</a>，那上面的兼容代码就有点多余了，<a href="mailto:因为node@8.9.3已经支持了async/await">因为node@8.9.3已经支持了async/await</a>。</p>
<p>修改下 .babelrc，加上配置参数"target"，它表示我们需要支持哪些平台+哪些版本。这里声明我们要支持的是node版本为8.9.3。</p>
<div class="sourceCode"><pre class="sourceCode json"><code class="sourceCode json"><span class="fu">{</span>
  <span class="dt">"presets"</span><span class="fu">:</span> <span class="ot">[</span>
    <span class="ot">[</span><span class="st">"env"</span><span class="ot">,</span> <span class="fu">{</span>
      <span class="dt">"targets"</span><span class="fu">:</span> <span class="fu">{</span>
        <span class="dt">"node"</span><span class="fu">:</span> <span class="st">"8.9.3"</span>
      <span class="fu">}</span>      
    <span class="fu">}</span><span class="ot">]</span>
  <span class="ot">]</span>
<span class="fu">}</span></code></pre></div>
<p>再次进行转码，结果如下。几乎没有变化，因为node最新版本支持 async/await，因此不需要额外的兼容代码。</p>
<div class="sourceCode"><pre class="sourceCode javascript"><code class="sourceCode javascript"><span class="st">"use strict"</span><span class="op">;</span>

async <span class="kw">function</span> <span class="at">foo</span>() <span class="op">{}</span></code></pre></div>
<h2 id="针对浏览器版本的配置">针对浏览器版本的配置</h2>
<p>babel-preset-env 同样提供了对浏览器版本的配置能力。</p>
<h3 id="支持特定版本的浏览器">支持特定版本的浏览器</h3>
<p>假设我们的代码如下：</p>
<div class="sourceCode"><pre class="sourceCode javascript"><code class="sourceCode javascript"><span class="kw">let</span> nick <span class="op">=</span> <span class="st">'程序猿小卡'</span><span class="op">;</span>
<span class="kw">let</span> desc <span class="op">=</span> <span class="vs">`你好 </span><span class="sc">${</span>nick<span class="sc">}</span><span class="vs">`</span><span class="op">;</span></code></pre></div>
<p>如果只需要支持 IE11，那么可以这样配置。</p>
<div class="sourceCode"><pre class="sourceCode json"><code class="sourceCode json"><span class="fu">{</span>
  <span class="dt">"presets"</span><span class="fu">:</span> <span class="ot">[</span>
    <span class="ot">[</span><span class="st">"env"</span><span class="ot">,</span> <span class="fu">{</span>
      <span class="dt">"targets"</span><span class="fu">:</span> <span class="fu">{</span>
        <span class="dt">"browsers"</span><span class="fu">:</span> <span class="st">"ie 11"</span>
      <span class="fu">}</span>      
    <span class="fu">}</span><span class="ot">]</span>
  <span class="ot">]</span>
<span class="fu">}</span></code></pre></div>
<p>如果只需要支持支持 Edge 16，那么可以这样配置</p>
<div class="sourceCode"><pre class="sourceCode json"><code class="sourceCode json"><span class="fu">{</span>
  <span class="dt">"presets"</span><span class="fu">:</span> <span class="ot">[</span>
    <span class="ot">[</span><span class="st">"env"</span><span class="ot">,</span> <span class="fu">{</span>
      <span class="dt">"targets"</span><span class="fu">:</span> <span class="fu">{</span>
        <span class="dt">"browsers"</span><span class="fu">:</span> <span class="st">"edge 16"</span>
      <span class="fu">}</span>      
    <span class="fu">}</span><span class="ot">]</span>
  <span class="ot">]</span>
<span class="fu">}</span></code></pre></div>
<p>因为 IE 11 不支持模板字面量，而 Edge 16支持模板字面量，因此上面配置的转码结果是不同的，读者可以自行尝试。</p>
<h3 id="支持特定版本范围的浏览器">支持特定版本范围的浏览器</h3>
<p>大部分时候，我们要针对的都是特定范围的浏览器，比如 IE8+，那么，逐个指定是不现实的。好在 babel-preset-env 支持要支持的版本范围。</p>
<p>比如，我们需要支持 IE8+、chrome62+，那么可以这样配置：</p>
<div class="sourceCode"><pre class="sourceCode json"><code class="sourceCode json"><span class="fu">{</span>
  <span class="dt">"presets"</span><span class="fu">:</span> <span class="ot">[</span>
    <span class="ot">[</span><span class="st">"env"</span><span class="ot">,</span> <span class="fu">{</span>
      <span class="dt">"targets"</span><span class="fu">:</span> <span class="fu">{</span>
        <span class="dt">"browsers"</span><span class="fu">:</span> <span class="ot">[</span> <span class="st">"ie &gt;= 8"</span><span class="ot">,</span> <span class="st">"chrome &gt;= 62"</span> <span class="ot">]</span>
      <span class="fu">}</span>      
    <span class="fu">}</span><span class="ot">]</span>
  <span class="ot">]</span>
<span class="fu">}</span></code></pre></div>
<p>看下前面声明的范围涵盖了哪些浏览器。</p>
<div class="sourceCode"><pre class="sourceCode bash"><code class="sourceCode bash">$ <span class="kw">`npm</span> bin<span class="kw">`/browserslist</span> <span class="st">"ie &gt;= 8, chrome &gt;= 62"</span>
<span class="kw">chrome</span> 66
<span class="kw">chrome</span> 65
<span class="kw">chrome</span> 64
<span class="kw">chrome</span> 63
<span class="kw">chrome</span> 62
<span class="kw">ie</span> 11
<span class="kw">ie</span> 10
<span class="kw">ie</span> 9
<span class="kw">ie</span> 8</code></pre></div>
<p>对浏览器版本范围的配置，babel-preset-env 借助了 <a href="https://github.com/browserslist/browserslist" title="browserslist">browserslist</a> 这个库，还有更多的配置方式，可以自行探究。</p>
<h2 id="babel-preset-env实现原理">babel-preset-env实现原理</h2>
<p>实现原理很简单。官方文档写的挺简洁的，挑重点大致翻译下。</p>
<p>1、首先，检测浏览器对JS特性的支持程度，比如通过通过 <a href="https://github.com/kangax/compat-table" title="compat-table">compat-table</a> 这样的外部数据。</p>
<p><img src="https://www.chyingp.com/wp-content/uploads/2018/06/fe1fe66055df7efde0355429452744f7.png"></p>
<p>2、将 JS特性 跟 特定的babel插件 建立映射，映射关系可以参考 <a href="https://github.com/babel/babel-preset-env/blob/master/data/plugin-features.js">这里</a>。</p>
<p>3、stage-x 的插件不包括在内。</p>
<p>4、根据开发者的配置项，确定至少需要包含哪些插件。比如声明了需要支持 IE8+、chrome62+，那么，所有IE8+需要的插件都会被包含进去。</p>
<h2 id="相关链接">相关链接</h2>
<p><a href="https://babeljs.io/docs/plugins/preset-env/#how-it-works" class="uri" title="https://babeljs.io/docs/plugins/preset-env/#how-it-works">https://babeljs.io/docs/plugins/preset-env/#how-it-works</a></p>
</div><div id="MySignature" style="display: block;"><br>
github博客：<a href="https://github.com/chyingp/blog" target="_blank">https://github.com/chyingp/blog</a>
<br>
新浪微博：<a href="http://weibo.com/chyingp" target="_blank">http://weibo.com/chyingp</a>
<br>
站酷主页：<a href="http://www.zcool.com.cn/u/346408/" target="_blank">http://www.zcool.com.cn/u/346408/</a></div>
<div class="clear"></div>
<div id="blog_post_info_block">
<div id="BlogPostCategory">分类: <a href="http://www.cnblogs.com/chyingp/category/560724.html" target="_blank">前端工具</a></div>
<div id="EntryTag">标签: <a href="http://www.cnblogs.com/chyingp/tag/babel/">babel</a>, <a href="http://www.cnblogs.com/chyingp/tag/babel-plugin/">babel-plugin</a>, <a href="http://www.cnblogs.com/chyingp/tag/babel-preset-env/">babel-preset-env</a></div>
<div id="blog_post_info"><div id="green_channel">
        <a href="javascript:void(0);" id="green_channel_digg" onclick="DiggIt(9137849,cb_blogId,1);green_channel_success(this,'谢谢推荐！');">好文要顶</a>
            <a id="green_channel_follow" onclick="follow('46ff3810-43ac-df11-8eb9-001cf0cd104b');" href="javascript:void(0);">关注我</a>
    <a id="green_channel_favorite" onclick="AddToWz(cb_entryId);return false;" href="javascript:void(0);">收藏该文</a>
    <a id="green_channel_weibo" href="javascript:void(0);" title="分享至新浪微博" onclick="ShareToTsina()"><img src="//common.cnblogs.com/images/icon_weibo_24.png" alt=""></a>
    <a id="green_channel_wechat" href="javascript:void(0);" title="分享至微信" onclick="shareOnWechat()"><img src="//common.cnblogs.com/images/wechat.png" alt=""></a>
</div>
<div id="author_profile">
    <div id="author_profile_info" class="author_profile_info">
            <a href="http://home.cnblogs.com/u/chyingp/" target="_blank"><img src="//pic.cnblogs.com/face/154088/20140304010315.png" class="author_avatar" alt=""></a>
        <div id="author_profile_detail" class="author_profile_info">
            <a href="http://home.cnblogs.com/u/chyingp/">程序猿小卡</a><br>
            <a href="http://home.cnblogs.com/u/chyingp/followees">关注 - 22</a><br>
            <a href="http://home.cnblogs.com/u/chyingp/followers">粉丝 - 962</a>
        </div>
    </div>
    <div class="clear"></div>
    <div id="author_profile_honor">荣誉：<a href="http://www.cnblogs.com/expert/" target="_blank">推荐博客</a></div>
    <div id="author_profile_follow">
                <a href="javascript:void(0);" onclick="follow('46ff3810-43ac-df11-8eb9-001cf0cd104b');return false;">+加关注</a>
    </div>
</div>
<div id="div_digg">
    <div class="diggit" onclick="votePost(9137849,'Digg')">
        <span class="diggnum" id="digg_count">1</span>
    </div>
    <div class="buryit" onclick="votePost(9137849,'Bury')">
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
<div id="post_next_prev"><a href="http://www.cnblogs.com/chyingp/p/how-to-write-a-babel-plugin.html" class="p_n_p_prefix">« </a> 上一篇：<a href="http://www.cnblogs.com/chyingp/p/how-to-write-a-babel-plugin.html" title="发布于2018-06-04 08:16">Babel插件开发入门指南</a><br><a href="http://www.cnblogs.com/chyingp/p/nodejs-learning-guide-github-got-1000-stars.html" class="p_n_p_prefix">» </a> 下一篇：<a href="http://www.cnblogs.com/chyingp/p/nodejs-learning-guide-github-got-1000-stars.html" title="发布于2018-06-06 07:35">一点感悟：《Node.js学习笔记》star数突破1000+</a><br></div>
</div>


		</div>
