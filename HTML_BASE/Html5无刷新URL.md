# Html5无刷新URL
发现一个可以改变地址栏，而不导致页面刷新的东东。 Chrome, FF测试通过，不支持IE.
一、实现目标
1.  页面的跳转（前进后退，点击等）不重新请求页面
2.  页面URL与页面展现内容一致（符合人们对传统网页的认识）
3.  在不支持的浏览器下降级成传统网页的方式

二、使用到的API
1、history.state
当前URL下对应的状态信息。如果当前URL不是通过pushState或者replaceState产生的，那么history.state是null。

2、history.pushState(state, title, url)
将当前URL和history.state加入到history中，并用新的state和URL替换当前。不会造成页面刷新。
state：与要跳转到的URL对应的状态信息。
title：不知道干啥用，传空字符串就行了。
url：要跳转到的URL地址，不能跨域。

3、history.replaceState
用新的state和URL替换当前。不会造成页面刷新。
state：与要跳转到的URL对应的状态信息。
title：不知道干啥用，传空字符串就行了。
url：要跳转到的URL地址，不能跨域。

4、window.onpopstate
history.go和history.back（包括用户按浏览器历史前进后退按钮）触发，并且页面无刷的时候（由于使用pushState修改了history）
会触发popstate事件，事件发生时浏览器会从history中取出URL和对应的state对象替换当前的URL和history.state。
通过event.state也可以获取history.state。
5、支持性判断
if ('pushState' in history) {...}

三、实现思路
用户通过“点击触发”，“操作历史”，“直接访问URL”的方式修改当前URL。这三种触发方式会使浏览器做出不同的行为。如果页面做无刷跳转，
那么页面具体显示什么内容需要js来控制，js则需要根据一些信息来知道当前应该显示什么内容，这个信息就是history.state。
这样我们只要保持URL和history.state一一对应，就能保证URL和内容一一对应。大部分情况下URL和history.state都是一一对应的，
但通过直接URL访问页面的方式进入页面，history.state是null，所以我们需要把URL转换成对应的history.state写入。
我们不能直接写入history.state，需要通过replaceState的方式写入。对于不支持pushstate的浏览器，一律修改href跳转页面，
等同于直接访问URL。示意图如下。
 
实例一、通过pushState修改URL
DEMO http://www.qttc.net/static/demo/html5_20130320/test.html
通过这句代码可以无刷新改变URL
window.history.pushState({},0,url);
DEMO代码：
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>HTML5无刷修改url - 琼台博客</title>
        <script type="text/javascript">
            function changeURL(){
                var url = document.getElementById('url').value;
                window.history.pushState({},0,'http://'+window.location.host+'/'+url);      
            }
 
        </script> 
    </head>
    <body>
        <h1>html5无刷新改变url</h1>
        <div id="info" style="margin:30px 0;">
            页面真实地址:
            <span style="color:red;"><script type="text/javascript">document.write(window.location.href);</script></span>
        </div>
        <div>
        请输入要改变地URL字符串：<input id='url' type="text" />
        <button onclick="changeURL();">点击无刷改变url</button>
        </div>
        <div style="color:red;margin-top:30px;">请使用支持html5的浏览器访问</div>
        <div style="margin-top:30px;"><a href="http://www.qttc.net/201303292.html" target="_blank">《html5无刷新改变URL》</a> - 琼台博客</div>
    </body>
 
</html>
截图：
 
在input输入框内输入haha.html点击“点击无刷新改变url”按钮即可实现
 
实例二、利用ajax配合pushState翻页无刷新的动作
主要在ajax发起数据请求，在数据页面响应后利用pushState修改分页参数，达到模拟真实翻页效果，并且写入历史表达到后退时能恢复上一页的数据
DEMO http://www.qttc.net/static/demo/html5_20130320/demo-page.html
demo-page.html代码：
<!DOCTYPE html>
<html>
    <head>
    <meta charset="utf-8" />
    <title>HTML5无刷修改url - 琼台博客</title>
    <script type="text/javascript">
    var changeURL = function(){
         
        if(location.href.indexOf("?") > -1){
            var arr = location.href.split('?');
            var urlbase = arr[0];
            var pageObj = arr[1].match(/page=(\d+)/);
            var page = Number(pageObj[1]) || 1;
        }else{
            var urlbase = location.href;
            var page = 1;
        }
 
        load = false;
        var content = document.getElementById("content");   
        var ajax = new XMLHttpRequest();
 
        // 调用数据回掉函数
        var ajaxCallback = function(){
            if(ajax.readyState == 4){
                load = false;
                result = eval('('+ajax.responseText+')');
                content.innerHTML = result.data;
                next.href = urlbase + "?page=" + (page + 1);
 
                // push到历史记录里，可以在点击后退时从历史记录里恢复内容
                // 并且无刷修改url地址
                window.history.pushState({content:content.innerHTML,page:page},page,urlbase + "?page=" + page);
            }
        };
 
        // 点击事件
        document.getElementById('next').onclick = function(event){
            if(!load){
                load = true;
                content.innerHTML = '加载中数据中...(注意看数据返回后url改变)';
                page++;
                ajax.open('GET','shuju.php?page='+page, true);
                ajax.onreadystatechange = ajaxCallback;
                ajax.send('');
                return false;
            }
        };
 
 
        // 记录到历史里，当点击后退按钮还退回上次页面请求前的页面内容
        window.onpopstate = function(){
            content.innerHTML = history.state.content;
            page = history.state.page;              
        }
 
        // 修改当前页面在 history 中的记录
        window.history.replaceState({content:content.innerHTML,page:page},page,urlbase + (page > 1 ? '?page=' + page : '' ));
    };
 
    // 检测是否支持
    try{
        //监听事件
        window.addEventListener('DOMContentLoaded', changeURL, false);
    }catch(e){
        alert('浏览器不支持，请使用支持html5的浏览器'); 
    }
 
    </script>
    </head>
    <body>
        <div id="content" style="width:300px;height:100px;border:1px solid #999;">第1页的内容</div>
        <div><a id="next" href="?page=2">下一页</a></div>
         
        <div style="color:red; margin-top:30px;">请使用支持html5的浏览器测试</div>
        <div><a href="http://www.qttc.net">xxx</a></div>
    </body>
</html>
shuju.php代码：
<?php
sleep(3);
echo json_encode(array('data'=>'第'.$_GET['page'].'内容'));
DEMO贴图：
 
没有点击之前
 
点击后，发起ajax请求page=2数据
 
ajax返回后通过pushState修改URL，请看截图地址栏已经是page=2，页面没有刷新，因为firebug控制台中的ajax请求记录还在
点击后退箭头，恢复上一页的数据

最后
虽说这两个html5新加api能实现无刷新修改URL，但js毕竟是前端，为了安全是不能跨域的。比如本例中的demo域是在www.qttc.net下，
不能修改到www.xxx.com域下。有不少人说这个特性解决了ajax局部刷新区域不容易被蜘蛛人抓取的问题，本人没有亲自验证，但却有可行之势，
感兴趣的童鞋可以尝试下。
