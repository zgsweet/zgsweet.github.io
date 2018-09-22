###  什么是类
javascript语言基于函数和原型链继承机制的方式构建可重用的组件，这对于面向对象编程来说显得比较笨拙，下一代提供了基于class base的
面向对象的设计方式。
类似面向对象编程的核心基础，是属于和方法的集合，类不能直接编写程序时引用，必须实例化后才能使用。
构造函数是一种特殊的方法，主要用来在创建对象时初始化对象，即为对象成员变量赋初始值，总与new运算符一起使用中创建对象的语句中。
### 选择node.js有哪些优势
1、性能：相对于多线程，异步I/O没有了线程间的上下文切换开销，由此带来可观的性能提升是选择它的主要原因。
2、成本：由于性能的提升，相同的硬件可以发挥更大的作用，变相的降低了运营成本，由于node.js采用javascript作为开发语言，而javascript的使用已经非常广泛，所以降低了node.js的学习成本。
3、效率：node.js采用javascript作为开发语言，使前后端开发语言统一，不需要切换开发语言，使开发效率更高，加之javascript使用者众多，使得node.js迅速的流行起来。

### 高阶函数
1、高级函数与普通函数不同的是高价函数可以把函数作为参数，或者将函数作为返回值
2、函数作为参数；函数作为返回值；
### 什么是偏函数
假设有一个参数或变量已经预置的函数A，我们通过调用A来产生一个新的函数B，函数B就是我们说的偏函数
```js
var isType = function(type){
  return function(obj){
    return toString.call(obj)=='[object '+type+']';
  }
};
var isString = isType('String') // isString就是偏函数
```
总之：1、一个创建函数的工厂函数；2、通过指定部分参数，定制新的函数；

### async流程控制库：
```
npm install async
var async = require('async');
```
1、series(tasks,callback);【作用是串行执行，一个函数数组中的每个函数，每一个函数执行完成之后才能执行下一个函数】
```
async.series({
    one: function(callback){
        callback(null, 1);
    },
    two: function(callback){
        callback(null, 2);
    }
},function(err, results) {
});
```
series函数的第一个参数可以是一个数组也可以是一个JSON对象，参数类型不同，影响的是返回数据的格式
