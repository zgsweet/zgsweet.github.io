1、一个 history 知道如何去监听浏览器地址栏的变化， 并解析这个 URL 转化为 location 对象， 然后 router 使用它匹配到路由，最后正确地渲染对应的组件。
  hashHistory;  // /#/user/id
  browserHistory; // /user/id
  createMemoryHistory;
  官方推荐使用browserHistory
 
2、区别
 
 hashHistory由于存在#，所以浏览器不会发送request请求，router自己根据URL去render相应的模块
 browserHistory从/到/USER/ID，浏览器会向server发送request，所以要做特殊请求处理，
 
 browserHistory其实使用的是HTML5的history的API，浏览器提供相应的接口来修改浏览器的历史记录，而hashHistory是通过改变地址后面的hash来改变浏览器的历史记录
 history API提供了pushState（）和replaceState（）方法来增加或替换历史记录，而hashHistory没有响应的方法，所以并没有替换历史记录的功能
 
