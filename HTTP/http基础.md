1、网络模型：
  应用层:http协议   
  传输层 tcp/ip
  网络层
  数据链路层
  物理层
  
2、http://user:pass@host.com:80/path?query=param@hash<br/>
3、http缓存cache-Control<br/>
  到期设置有：[max-age |s-maxage | max-stale]=seconds<br/>
  可缓存性：[public|private|no-cache]<br/>
  重新验证:[must-revalidate | proxy-revalidate]<br/>
  res.writeHead(200,{<br/>
    'Content-Type':'text/javascript',<br/>
    'Cache-Control':'max-age=20,no-cache<br/>
    ' last-modified':'123' // 配置代表在下次再发请求的时候通过传回的if-modified-since带回的上次设置的日期参数123来判断是否文件做了修改，没有修改返回 304,<br/>'Etag':'xxx' //配置代表实体标签签名，在下次再请求时传回if-none-Match参数带回xxx参数值，来判断是否和上次的签名一致
  })<br/>
 
  no-cache:代表每次发送请求后都要先向服务端发请求做验证是否需要读取缓存内容，忽略返回的请求主体内容<br/>
 no-store:代表不设置任何缓存内容,每次都要发出请求


1、内容安全测试CSP(content-security-policy):https://developer.mozilla.org/zh-CN/docs/Web/HTTP/CSP
内容安全策略   (CSP) 是一个额外的安全层，用于检测并削弱某些特定类型的攻击，包括跨站脚本 (XSS) 和数据注入攻击等。无论是数据盗取、网站内容污染还是散发恶意软件，这些攻击都是主要的手段
客户端：
<meta http-equiv="Content-Security-Policy" content="default-src 'self'; img-src https://*; child-src 'none';">
服务端：
res.writeHead(200,{
'Conent-type:'text/html',
'Content-Security-policy':'default-src \'self\''
})
