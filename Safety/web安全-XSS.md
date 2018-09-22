
## 1、了解XSS的定义
  XSS：跨域脚本攻击 cross-site scripting
## 2、理解XSS的原理
## 3、理解XSS的攻击方式
  ### 》反射型
    发出请求时，XSS代码出现在URL中，作为输入到服务器端，服务器端解析后相应，XSS代码随响应内容一起传回给浏览器，最后
    浏览器解析执行XSS代码，这个过程像一次反射，故叫反射型XSS。
 ### 》存储型
   存储型XSS和反射型XSS的差别仅在于，提交的代码会存储在服务端（数据库，内存，文件系统等），下次请求目标页面时不，
   不用再提交XSS代码。
   总结：反射型xss攻击代码是存在url中，存储型是存在服务端
   ### 破坏性：
    1、盗用cokkie，获取敏感信息
    2、破坏正常的页面结构，插入恶意内容
    3、利用flash，但是flash已经不常用了
    4、实现DDoS攻击效果，分布式拒绝服务攻击
    基本的DoS攻击：就是利用合理的客户端请求，占用过多的服务器资源，从而使合法的用户无法得到服务器的响应
## 4、掌握XSS的防御措施
 ### 1、编码
    不能对用户的所有输入保持原样（对用户输入的数据进行HTML Entity编码）
    ```
    " --->&quot;
    &--->&amp;
    < ---> &lt;
    > ---> &gt;
    function html_encode(str){
      var s = '';
      if(str.length==0){return ""}
      s = str.replace(/&/g,"&amp;");
      s = str.replace(/</g,"&lt;");
      s = str.replace(/>/g,"&gt;");
      s = str.replace(/\s/g,"&nbsp;");
      s = str.replace(/\'/g,"&#39;");
      s = str.replace(/\"/g,"&quot;");
      s = str.replace(/\n/g,"<br>");
      return s;
}
    ```
 ### 2、过滤
    在显示原样内容时，要过滤不应该原样显示的东西。
    移除用户上传的DOM属性，如onerror等
     移除用户上传的Style、Script、iframe节点
 ### 3、校正
   避免直接对HTML Entity解码
   使用DOM Parse转换，校正不配对的DOM标签
   
 备注：SQL注入原理：https://blog.csdn.net/stilling2006/article/details/8526458
  ## 解码
  ### 1、常用到的三方工具：
  encode.js：可以使用https://github.com/mathiasbynens/he 中的he.js
  domParse：可以用 https://github.com/blowsie/Pure-JavaScript-HTML5-Parser

  解码代码函数：
  ```
  <script src="encode.js" charset="utf-8"></script>
   <script src="domParse.js" charset="utf-8"></script>
   <script>
   var parse = function(str){
    var results='';
    try{
      HTMLParse(he.unescape(str,{strict:true}),{
      start:function(tag,attrs,unary){
       results += '<'+tag;
       for(var i=0,len=attrs.length;i<len;i++){
        results+=' '+attrs[i].name+'='+attrs[i].escaped+'"';
       }
       retuslts += (unary?"/":"")+">";
      },
      end:function(tag){
      retuslts+='</'+tag+">";
      },
      chars:function(text){
      results+=text;
      },
      comment:function(text){
        results+="<!--"+text+"-->";
      }
      
      })
    }catch(err){
      console.log(err)
    }
   
   }
   </script>
   ```
  ## 提问：
  1、为什么在服务端转义后，拿到前端后又直接转义后再过滤，直接过滤不行吗？
  答：在服务器进行转义存储，是考虑数据库服务器安全问题，前端反转义是因为要显示，然后不能直接反转义，是因为可能存在XSS攻击，所以要过滤。
  2、像我们直接评论是还会显示标签的，如<script></script>,这怎么解释？
  答：评论区会直接显示标签，可能是使用了innerText，innerText不识别不解析标签，所以也不会造成xss攻击。
