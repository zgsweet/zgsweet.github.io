<div id="cnblogs_post_body" class="blogpost-body"><p><span style="font-family: 'Microsoft YaHei';">整理网上流传的若干份面试题目，突发奇想，总结关于CSS面试题目的考察点，发现问题大多围绕几个属性和几种题目，水平有限，仅供参考。</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;</span></p>
<p><span style="font-family: 'Microsoft YaHei';"><strong>纠正前端开发中容易出错知识点</strong><a href="http://www.cnblogs.com/0603ljx/p/4354656.html" target="_blank">&nbsp;http://www.cnblogs.com/0603ljx/p/4354656.html</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;</span></p>
<p><span style="color: #000080; font-size: 16px;"><strong><span style="font-family: 'Microsoft YaHei';">1，&nbsp; 多元素水平居中</span></strong></span></p>
<p><span style="font-family: 'Microsoft YaHei';">实现一下效果：&nbsp;</span></p>
<p><span style="font-family: 'Microsoft YaHei';"><img src="https://images0.cnblogs.com/blog2015/601481/201504/200009392602364.png" alt=""></span></p>
<p><span style="font-family: 'Microsoft YaHei';">平常人看见题目，最初感觉实现图片中的效果不难，设置小黑框的宽高边距，字体水平垂直居中即可。其实，题目应该实际上是考察多元素水平居中，即无论元素（小黑框）基数为多少，它们都能作为一个整体，水平居中。</span></p>
<p><span style="font-family: 'Microsoft YaHei';">在网站布局中，很多时候，子元素中使用行内元素如span或块元素li标签且标签个数不定，而我们又想让这一块不管个数有多少个(子元素的总体宽度不定)，始终都能居中显示。这就需要设置子元素display:inline-block。同时，根据display:inline-block的属性，子元素本身具备inline的特性，因此父元素需要设置text-align：center，来实现子元素作为一个整体在父元素中水平居中。</span></p>
<div class="cnblogs_code"><div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div>
<pre><span style="font-family: 'Microsoft YaHei';"><span style="color: #800000;">main</span>{<span style="color: #ff0000;">
  text-align</span>:<span style="color: #0000ff;">center</span>;
}<span style="color: #800000;">

div</span>{<span style="color: #ff0000;">
  display</span>:<span style="color: #0000ff;">inline-block</span>;<span style="color: #ff0000;">
  *display</span>:<span style="color: #0000ff;">inline</span>;<span style="color: #008000;">/*</span><span style="color: #008000;">hack IE</span><span style="color: #008000;">*/</span><span style="color: #ff0000;">
  *zoom</span>:<span style="color: #0000ff;">1</span>;<span style="color: #008000;">/*</span><span style="color: #008000;">hack IE</span><span style="color: #008000;">*/</span>
}</span></pre>
<div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div></div>
<p><span style="font-family: 'Microsoft YaHei';">使用display:inline-block属性，可以使<strong>行内元素或块元素</strong>能够不加float属性就可以定义自身的宽、高，同时又能使该元素在父元素居中显示。</span></p>
<p><span style="font-family: 'Microsoft YaHei';">在内联元素上定义display:inline-block属性，发现IE6、IE7中的显示效果同其它浏览器一致，但事实是ie7及更低版本的ie浏览器不支持display:inline-block这个属性。&nbsp;</span></p>
<p><span style="font-family: 'Microsoft YaHei';">在IE下，display: inline-block只是触发了元素的layout。比如将display: inline-block设置到div上，只能保证这个div拥有块元素的特征（可以设置宽度，高度等），但还是会产生换行。接下来要设置display: inline，使其不产生换行。将display:inline-block;*display:inline;写在同一个样式上，inline-block属性是不会触发元素的layout的，因此我们还要额外加上 *zoom:1来触发layout。</span></p>
<p><span style="font-family: 'Microsoft YaHei';">除了以上所提到的有效方法之外，还有<strong>另外一种方法</strong>：</span></p>
<p><span style="font-family: 'Microsoft YaHei';">先使用 display:inline-block 属性触发块元素，然后再定义 display:inline，让块元素呈递为内联对象（两个display 要先后放在两个 CSS 样式声明中才有效果，这是 IE 的一个经典 bug&nbsp;，如果先定义了 display:inline-block，然后再将 display 设回 inline 或 block，layout 不会消失）。</span></p>
<p><span style="font-family: 'Microsoft YaHei';">div {display:inline-block;...}div {*display:inline;}</span></p>
<p><span style="font-family: 'Microsoft YaHei';">但是要注意的是，<span style="line-height: 1.5;">display:inline-block元素间会产生多余空白（本题没有涉及）。解决方法：父元素定义font-size:0 去掉行内块元素水平方向空白；子元素定义vertical-align 属性去掉行内块元素垂直方向空白。</span></span></p>
<p>&nbsp;<a href="http://codepen.io/floralam/pen/XJwWZJ?editors=110">http://codepen.io/floralam/pen/XJwWZJ?editors=110</a></p>
<p>&nbsp;</p>
<p><span style="color: #000080; font-size: 16px; font-family: 'Microsoft YaHei';"><strong>实现多元素水平垂直居中</strong></span></p>
<p><span style="font-family: 'Microsoft YaHei';">使用flexbox</span></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/MwKmGP" target="_blank">http://codepen.io/floralam/pen/MwKmGP</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">具体解析，可查看<a href="http://www.w3cplus.com/css3/designing-css-layout-with-flexbox.html" target="_blank">《</a><a href="http://www.w3cplus.com/css3/designing-css-layout-with-flexbox.html" target="_blank">Flexbox制作CSS布局易如反掌》</a></span></p>
<p>&nbsp;</p>
<p><span style="font-size: 16px;"><strong><span style="font-family: 'Microsoft YaHei'; color: #000080;">2，&nbsp; 栏栅化布局</span></strong></span></p>
<p><span style="font-family: 'Microsoft YaHei';">实现一下布局：&nbsp;</span></p>
<p><span style="font-family: 'Microsoft YaHei';"><img src="https://images0.cnblogs.com/blog2015/601481/201504/200009494798342.png" alt="" width="386" height="259"></span></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/OPYyEE">http://codepen.io/floralam/pen/OPYyEE</a></span></p>
<div class="cnblogs_code"><div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div>
<pre><span style="color: #800000;">.parent</span>{<span style="color: #ff0000;">
    display</span>:<span style="color: #0000ff;"> flex</span>;<span style="color: #ff0000;">
    flex-direction</span>:<span style="color: #0000ff;"> column</span>;<span style="color: #ff0000;">//上面两行等同于flex-flow：colomn
    flex-wrap</span>:<span style="color: #0000ff;"> wrap</span>;<span style="color: #ff0000;">// 显示 wrap一行显示不完的时候换行
    height</span>:<span style="color: #0000ff;"> 440px</span>;<span style="color: #ff0000;">
    width</span>:<span style="color: #0000ff;"> 660px</span>;
}</pre>
<div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div></div>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;</span></p>
<p><span style="font-family: 'Microsoft YaHei';">一个Flexbox布局是由一个<span style="text-decoration: underline;">伸缩容器</span>(flex containers)和在这个容器里的<span style="text-decoration: underline;">伸缩项目</span>(flex items)组成。</span></p>
<p><span style="font-family: 'Microsoft YaHei';"><strong>伸缩方向与换行(flex-flow)</strong></span></p>
<p><span style="font-family: 'Microsoft YaHei';">伸缩容器有一个CSS属性“flex-flow”用来决定<span style="text-decoration: underline;">伸缩项目的布局方式</span>。</span></p>
<p><span style="font-family: 'Microsoft YaHei';">如果伸缩容器设置了“flex-flow”值为“row”，伸缩项目排列由左向右排列。</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;<img src="https://images0.cnblogs.com/blog2015/601481/201504/200009122295256.jpg" alt=""></span></p>
<p><span style="font-family: 'Microsoft YaHei';">如果“flex-flow”值设置为“column”，伸缩项目排列由上至下排列。</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;<img src="https://images0.cnblogs.com/blog2015/601481/201504/200009248239075.jpg" alt=""></span></p>
<p><span style="font-family: 'Microsoft YaHei';"><strong><span style="color: #000080;">制作一个20%、60%、20%网格布局</span></strong></span></p>
<div class="cnblogs_code"><div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div>
<pre><span style="color: #800000;">.main-content </span>{<span style="color: #ff0000;">
      width</span>:<span style="color: #0000ff;"> 60%</span>;
}<span style="color: #800000;">

.main-nav,.main-sidebar </span>{<span style="color: #ff0000;">
     -webkit-box-flex</span>:<span style="color: #0000ff;"> 1</span>;      <span style="color: #008000;">/*</span><span style="color: #008000;"> OLD - iOS 6-, Safari 3.1-6 </span><span style="color: #008000;">*/</span><span style="color: #ff0000;">
      -moz-box-flex</span>:<span style="color: #0000ff;"> 1</span>;         <span style="color: #008000;">/*</span><span style="color: #008000;"> OLD - Firefox 19- </span><span style="color: #008000;">*/</span><span style="color: #ff0000;">
      width</span>:<span style="color: #0000ff;"> 20%</span>;               <span style="color: #008000;">/*</span><span style="color: #008000;"> For old syntax, otherwise collapses. </span><span style="color: #008000;">*/</span><span style="color: #ff0000;">
      -webkit-flex</span>:<span style="color: #0000ff;"> 1</span>;          <span style="color: #008000;">/*</span><span style="color: #008000;"> Chrome </span><span style="color: #008000;">*/</span><span style="color: #ff0000;">
      -ms-flex</span>:<span style="color: #0000ff;"> 1</span>;              <span style="color: #008000;">/*</span><span style="color: #008000;"> IE 10 </span><span style="color: #008000;">*/</span><span style="color: #ff0000;">
      flex</span>:<span style="color: #0000ff;"> 1</span>;                  <span style="color: #008000;">/*</span><span style="color: #008000;"> NEW, Spec - Opera 12.1, Firefox 20+ </span><span style="color: #008000;">*/</span>
}</pre>
<div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div></div>
<p>&nbsp;</p>
<p><span style="font-size: 16px;"><strong><span style="font-family: 'Microsoft YaHei'; color: #000080;">3，&nbsp; 未知高度多行文本垂直居中</span></strong></span></p>
<p><span style="font-family: 'Microsoft YaHei';"><strong>方法一，使用display：inline-block+伪元素：</strong><a href="http://codepen.io/floralam/pen/WbBrwV?editors=110">http://codepen.io/floralam/pen/WbBrwV?editors=110</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;<img src="https://images0.cnblogs.com/blog2015/601481/201505/091702269072903.png" alt=""></span></p>
<div class="cnblogs_code"><div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div>
<pre><span style="color: #800000;">.container</span>{<span style="color: #ff0000;">
   position</span>:<span style="color: #0000ff;"> fixed</span>;<span style="color: #ff0000;">
    left</span>:<span style="color: #0000ff;"> 0</span>;<span style="color: #ff0000;">
    top</span>:<span style="color: #0000ff;">0</span>;<span style="color: #ff0000;">
    height</span>:<span style="color: #0000ff;"> 100%</span>;<span style="color: #ff0000;">
    width</span>:<span style="color: #0000ff;"> 100%</span>;<span style="color: #ff0000;">
    text-align</span>:<span style="color: #0000ff;"> center</span>;
}<span style="color: #800000;">

.mask:after</span>{<span style="color: #ff0000;">
    content</span>:<span style="color: #0000ff;"> " "</span>;<span style="color: #ff0000;">
    display</span>:<span style="color: #0000ff;"> inline-block</span>;<span style="color: #ff0000;">
    vertical-align</span>:<span style="color: #0000ff;"> middle</span>;<span style="color: #ff0000;">
    height</span>:<span style="color: #0000ff;"> 100%
</span>}<span style="color: #800000;">

.dialog</span>{<span style="color: #ff0000;">
    display</span>:<span style="color: #0000ff;"> inline-block</span>;<span style="color: #ff0000;">
    border</span>:<span style="color: #0000ff;"> 3px solid lightblue</span>;
}</pre>
<div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div></div>
<p><span style="font-family: 'Microsoft YaHei';">box 容器通过 after或者before 生成一个高度 100% 的「备胎」，他的高度和容器的高度是一致的，相对于「备胎」垂直居中，在视觉上表现出来也就是相对于容器垂直居中了</span></p>
<p><strong><span style="font-family: 'Microsoft YaHei';">&nbsp;方法二（感谢超级课程表胡晋哥哥的提示），使用display：table-cell：</span></strong></p>
<p><a href="http://codepen.io/floralam/pen/yNeMPg" target="_blank"><span style="font-family: 'Microsoft YaHei';">http://codepen.io/floralam/pen/yNeMPg</span></a></p>
<p><span style="font-family: 'Microsoft YaHei';">通过display转化成为表格的形式，再采用垂直居中的方法得到需要的结果。</span></p>
<p><span style="font-family: 'Microsoft YaHei';">display:table &nbsp; &nbsp;此元素会作为块级表格来显示（类似 &lt;table&gt;），表格前后带有换行符。 &nbsp; &nbsp;</span></p>
<p><span style="font-family: 'Microsoft YaHei';">display:table-cell 此元素会作为一个表格单元格显示（类似 &lt;td&gt; 和 &lt;th&gt;）</span></p>
<p><strong><span style="font-family: 'Microsoft YaHei';">方法三（感谢超级课程表胡晋哥哥的提示），flexbox布局：</span></strong></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/yNeMvM" target="_blank">http://codepen.io/floralam/pen/yNeMvM</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">flexbox属性：</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;伸缩容器：一个设有“display:flex”或“display:inline-flex”的元素<br>&nbsp;伸缩项目：伸缩容器的子元素<br>&nbsp;主轴、主轴方向：用户代理沿着一个伸缩容器的主轴配置伸缩项目，主轴是主轴方向的延伸。<br>&nbsp;主轴起点、主轴终点：伸缩项目的配置从容器的主轴起点边开始，往主轴终点边结束。<br>&nbsp;主轴长度、主轴长度属性：伸缩项目的在主轴方向的宽度或高度就是项目的主轴长度，伸缩项目的主轴长度属性是width或height属性，由哪一个对着主轴方向决定。<br>&nbsp;侧轴、侧轴方向：与主轴垂直的轴称作侧轴，是侧轴方向的延伸。<br>&nbsp;侧轴起点、侧轴终点：填满项目的伸缩行的配置从容器的侧轴起点边开始，往侧轴终点边结束。<br>&nbsp;侧轴长度、侧轴长度属性：伸缩项目的在侧轴方向的宽度或高度就是项目的侧轴长度，伸缩项目的侧轴长度属性是「width」或「height」属性，由哪一个对着侧轴方向决定。</span></p>
<p><strong><span style="font-family: 'Microsoft YaHei';">另外，对于单行文本，设置line-height=height代码更加简洁:</span></strong></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/eNJvyE" target="_blank">http://codepen.io/floralam/pen/eNJvyE</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">父元素设置宽度高度，然后设置属性</span></p>
<p><span style="font-family: 'Microsoft YaHei';">text-align:center; /* 水平居中 */<br>line-height: 300px; /* line-height = height */</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;</span></p>
<p><span style="font-size: 16px;"><strong><span style="font-family: 'Microsoft YaHei'; color: #000080;">4，&nbsp; 多栏自适应布局</span></strong></span></p>
<p><span style="font-family: 'Microsoft YaHei';">对于移动设备浏览器：<a href="http://codepen.io/floralam/pen/NPVwgz?editors=110">http://codepen.io/floralam/pen/NPVwgz?editors=110</a></span></p>
<div class="cnblogs_code"><div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div>
<pre><span style="color: #800000;">.container</span>{<span style="color: #ff0000;">
  display</span>:<span style="color: #0000ff;">-webkit-box</span>;
}<span style="color: #800000;">

.left</span>{<span style="color: #ff0000;">
  -webkit-box-flex</span>:<span style="color: #0000ff;">1</span>;
}<span style="color: #800000;">

.right</span>{<span style="color: #ff0000;">
  -webkit-box-flex</span>:<span style="color: #0000ff;">1</span>;
}</pre>
<div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div></div>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;实现左右两侧元素，右侧元素的文字不会溢出到左侧位置。</span></p>
<p><span style="font-family: 'Microsoft YaHei';"><img src="https://images0.cnblogs.com/blog2015/601481/201504/200919594964579.png" alt="" width="396" height="148"></span></p>
<p><strong><span style="font-family: 'Microsoft YaHei';">1）让左边的图片左浮动或者绝对定位，</span></strong></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/wBbPPj">http://codepen.io/floralam/pen/wBbPPj</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">.right{</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;&nbsp;&nbsp; margin-left: 150px;</span></p>
<p><span style="font-family: 'Microsoft YaHei';">}</span></p>
<p><strong><span style="font-family: 'Microsoft YaHei';">2）让左边的图片左浮动或者绝对定位，</span></strong></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/gbJogQ">http://codepen.io/floralam/pen/gbJogQ</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">.right{</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp; overflow:hidden;/*让右侧文字和左侧图片自动分栏*/</span></p>
<p><span style="font-family: 'Microsoft YaHei';">}</span></p>
<p><strong><span style="font-family: 'Microsoft YaHei';">3）左侧图片设置为左浮动，</span></strong></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/bNyaaX?editors=110">http://codepen.io/floralam/pen/bNyaaX?editors=110</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">.right{</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp; display: table-cell;/*让右侧文字和左侧图片自动分栏*/</span></p>
<p><span style="font-family: 'Microsoft YaHei';">}</span></p>
<p><span style="font-family: 'Microsoft YaHei';"><strong>两栏或多栏自适应布局的通用类语句是（block</strong><strong>水平标签，需配合浮动）：</strong></span></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/vEwpjV">http://codepen.io/floralam/pen/vEwpjV</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">.cell{</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp; padding-right:10px;</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp; display: table-cell;</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp; *display: inline-block;</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp; *width: auto;</span></p>
<p><span style="font-family: 'Microsoft YaHei';">}</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;</span><img style="font-family: 'Microsoft YaHei'; line-height: 1.5;" src="https://images0.cnblogs.com/blog2015/601481/201504/200008338396085.png" alt="" width="368" height="254"></p>
<p>&nbsp;</p>
<p><span style="font-size: 16px;"><strong><span style="font-family: 'Microsoft YaHei'; color: #000080;">5，&nbsp; 强制不换行</span></strong></span></p>
<div class="cnblogs_code">
<pre><span style="color: #800000;">div</span>{<span style="color: #ff0000;">
    white-space</span>:<span style="color: #0000ff;">nowrap</span>;
}</pre>
</div>
<p><span style="font-family: 'Microsoft YaHei';">自动换行</span></p>
<div class="cnblogs_code">
<pre><span style="color: #800000;">div</span>{<span style="color: #ff0000;">
　　word-wrap</span>:<span style="color: #0000ff;"> break-word</span>;<span style="color: #ff0000;"> //性允许长单词或 URL 地址换行到下一行
　　word-break</span>:<span style="color: #0000ff;"> normal</span>;<span style="color: #ff0000;"> //让浏览器实现在任意位置的换行
</span>}</pre>
</div>
<p>&nbsp;</p>
<p><span style="font-family: 'Microsoft YaHei';">word-wrap是控制换行的。break-word是控制是否断词的。</span></p>
<p><span style="font-family: 'Microsoft YaHei';">强制英文单词断行</span></p>
<p><span style="font-family: 'Microsoft YaHei';">div{</span></p>
<p><span style="font-family: 'Microsoft YaHei';">　　word-break:break-all;</span></p>
<p><span style="font-family: 'Microsoft YaHei';">}</span></p>
<p>&nbsp;</p>
<p><span style="font-size: 16px;"><strong><span style="font-family: 'Microsoft YaHei'; color: #000080;">6，&nbsp; li超过一定长度，以省略号显示</span></strong></span></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/zxQjrK">http://codepen.io/floralam/pen/zxQjrK</a></span></p>
<div class="cnblogs_code">
<pre><span style="color: #800000;">.nowrap li</span>{<span style="color: #ff0000;">
   white-space</span>:<span style="color: #0000ff;">nowrap</span>;<span style="color: #ff0000;">
   width</span>:<span style="color: #0000ff;">100px</span>;<span style="color: #ff0000;">
   overflow</span>:<span style="color: #0000ff;">hidden</span>;<span style="color: #ff0000;">
   text-overflow</span>:<span style="color: #0000ff;"> ellipsis</span>;
}</pre>
</div>
<p>&nbsp;</p>
<p><span style="font-size: 16px;"><strong><span style="font-family: 'Microsoft YaHei'; color: #000080;">7，&nbsp; 左侧导航</span></strong></span></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/ogrbXW?editors=110">http://codepen.io/floralam/pen/ogrbXW?editors=110</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;<img src="https://images0.cnblogs.com/blog2015/601481/201504/200008074483147.png" alt=""></span></p>
<div class="cnblogs_code"><div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div>
<pre><span style="color: #800000;">.nav</span>{<br><span style="color: #ff0000;">　　position</span>:<span style="color: #0000ff;">relative</span>;<br><span style="color: #ff0000;">　　float</span>:<span style="color: #0000ff;">left</span>;<span style="color: #ff0000;">width</span>:<span style="color: #0000ff;">190px</span>;<br><span style="color: #ff0000;">　　margin-right</span>:<span style="color: #0000ff;">-190px</span>;<br><span style="color: #ff0000;">　　background</span>:<span style="color: #0000ff;">lightblue</span>;<br>}<span style="color: #800000;">
.container</span>{<br><span style="color: #ff0000;">　　float</span>:<span style="color: #0000ff;">right</span>;<br><span style="color: #ff0000;">　　width</span>:<span style="color: #0000ff;">100%</span>;<br><span style="color: #ff0000;">　　background</span>:<span style="color: #0000ff;">pink</span>;<br>}<span style="color: #800000;">
.content</span>{<br><span style="color: #ff0000;">　　margin-left</span>:<span style="color: #0000ff;">200px</span>;<br>}</pre>
<div class="cnblogs_code_toolbar"><span class="cnblogs_code_copy"><a href="javascript:void(0);" onclick="copyCnblogsCode(this)" title="复制代码"><img src="//common.cnblogs.com/images/copycode.gif" alt="复制代码"></a></span></div></div>
<p>&nbsp;</p>
<p><span style="font-size: 16px;"><strong><span style="font-family: 'Microsoft YaHei'; color: #000080;">8，&nbsp; css3文字分栏</span></strong></span></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/ZYdOmN?editors=110">http://codepen.io/floralam/pen/ZYdOmN?editors=110</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;</span></p>
<p><span style="font-size: 16px;"><strong><span style="font-family: 'Microsoft YaHei'; color: #000080;">9，&nbsp; 修复侧边栏</span></strong></span></p>
<p><span style="font-family: 'Microsoft YaHei';">在外容器的添加导航和主内容，当导航和主内容的宽度加上内外边距的数值大于外容器的宽度减去内边距的值，会导致导航和主内容（其中一个，html代码排后面的元素）被挤下。<br></span></p>
<p><span style="font-family: 'Microsoft YaHei';"><img src="https://images0.cnblogs.com/blog2015/601481/201504/200007466048247.jpg" alt=""></span></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/XJLRYq?editors=110">http://codepen.io/floralam/pen/XJLRYq?editors=110</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;解决方案：</span></p>
<p><span style="font-family: 'Microsoft YaHei';">1)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Section元素上使用box-sizing:border-box;模拟IE6中，使得内元素的宽度为width的值，而非width加上padding和margin的值。</span></p>
<p><span style="font-family: 'Microsoft YaHei';">2)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; width:-moz-calc(75% -1rem * 2);width:-webkit-calc(75% - 1rem * 2); width: calc(75% - 1rem * 2); width属性中减去padding值</span></p>
<p><span style="font-family: 'Microsoft YaHei';">3)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <a href="http://codepen.io/floralam/pen/yydPOE">http://codepen.io/floralam/pen/yydPOE</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">在元素内部增加一个额外的容器，并将padding放在这个新增的内部容器中，这是一种修复方法，而且得到众多浏览器支持。</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;</span></p>
<p><strong><span style="font-family: 'Microsoft YaHei'; color: #000080; font-size: 16px;">10， css描绘三角形</span></strong></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/azgGmZ">http://codepen.io/floralam/pen/azgGmZ</a></span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;很多关于使用css3来描绘特定图像，使用代码而非图片实现（多座小山包，返回顶部）的题目，都离不开描绘三角形。</span></p>
<p>&nbsp;</p>
<p><span style="font-size: 16px;"><strong><span style="font-family: 'Microsoft YaHei'; color: #000080;">11， 清除浮动的技巧</span></strong></span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;</span></p>
<p><span style="font-family: 'Microsoft YaHei';">&nbsp;<img src="https://images0.cnblogs.com/blog2015/601481/201504/200007168235113.png" alt=""></span></p>
<p><span style="font-family: 'Microsoft YaHei';">在非IE浏览器（如Firefox）下，当容器的高度为auto，且容器的内容中有浮动（float为left或right）的元素，在这种情况下，<span style="text-decoration: underline;">容器的高度不能自动伸长以适应内容的高度，使得内容溢出到容器外面而影响（甚至破坏）布局的现象</span>。这个现象叫浮动溢出，为了防止这个现象的出现而进行的CSS处理，就叫CSS清除浮动。</span></p>
<p><span style="font-family: 'Microsoft YaHei';">1)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 添加最后一个元素&lt;div style ="clear:both"&gt;&lt;/div&gt;</span></p>
<p><span style="font-family: 'Microsoft YaHei';">2)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 父元素设置overflow: hidden;</span></p>
<p><span style="font-family: 'Microsoft YaHei';">3)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 使用CSS的:after伪元素</span></p>
<p><span style="font-family: 'Microsoft YaHei';">通过CSS伪元素在容器的内部元素最后添加了一个看不见的空格"020"或点"."，并且赋予clear属性来清除浮动。需要注意的是为了IE6和IE7浏览器，要给clearfix这个class添加一条zoom:1;触发haslayout。</span></p>
<p><span style="font-family: 'Microsoft YaHei';"><a href="http://codepen.io/floralam/pen/xboPXK?editors=110">http://codepen.io/floralam/pen/xboPXK?editors=110</a></span></p></div>
