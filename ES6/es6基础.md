1、let、const 分别是变量和常量；块级作用域；不能重复定义，不能覆盖；不存在变量提升
var 存在变量提升/可以重复定义，并且后者覆盖前者
2、箭头函数：参数=>表达式/语句；没有独立作用域是继承外层作用域、不能用作构造函数（new）、没有prototype属性
表达式:double=x=>2*x;语句 treble=x>{return 3* x}
3、promise对象，是解决异步调用层层回调问题，它实现链式调用，便于阅读 resolve,reject表示异步回调的成功和失败,then,all
new Promise((resolve,reject)=>{
fech({url}).then((data)=>{
resolve(data)
}).catch((err)=>{
reject(err)
})
}).then((success)=>{

},(fail)=>{

})
  
