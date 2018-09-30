## # promise是什么 # ##
- 主要用于异步计算
- 可以将异步操作队列化，按照期望的顺序执行，返回符合预期的结果
- 可以在对象之间传递，帮我们处理队列

1. promise是一个代理对象，它和原先要进行的操作并无关系
2. 它通过引入一个回调，避免更多的回调
3. promise有3个状态
	- pending 初始
	- fulfilled 操作成功
	- rejected 失败
![](https://i.imgur.com/LMpEjPk.jpg)
  ![](https://i.imgur.com/Txo8xZ9.jpg)uhjnmjillksaz
## 为什么会出现promise ##
- js检查表单而生，操作DOM，异步操作能够避免窗格的冻结
- 创造它的首要目标是操作DOM
- javascript的操作大多数是异步的
- 异步主要是事件的侦听与响应，回调函数，ajax代码
- 浏览器中的javascript是一部操作以事件为主
- node.js是无阻塞或高并发，异步操作上其保障，大量操作依赖回调函数
## 异步回调的问题 ##
- 回调地狱：嵌套层次很深，难以维护
- 无法正常使用return和throw
- 多个回调之间难以建立联系
- 无法正常检索堆栈信息
- 异步回调函数会在一个新的栈中运行
1. 异步回调函数与前面的函数不处于同一个栈，所以不适用try/cath等上层检查机制，全局变量的污染问题
## 方法 ##
一、.then()里有.then()的情况：一个响应函数中又有链式调用

1、因为.then()返回的还是promise实例。

2、会等里面的.then()执行完，在执行外面的。

3、对于我们来说，此时最好将其展开，会更好读。
一、

promise队列的重要特性，在任何地方生成了一个promise队列之后，我们可以把它作为一个变量传递到其他地方，如果我们的操作是队列的状态，即先进先出的状态，就可以在后面追加任意多的then，不管之前的队列是完成还是没有完成，队列都会按照顺序完成。

二、

let promise = new Promise(resolve => {
  setTimeout(() => {
    console.log('the promise fulfilled');
    resolve('hello');
  }, 1000);
});
setTimeout(() => {
  promise.then(value => {
    console.log(value);
  })
})
一、错误处理

1、promise会自动捕获内部异常，并交给rejected响应函数处理。

2、promise试图在现有的语言框架中解决异步回调带来的问题。在栈的语言基层运行池相关的问题就无法处理了，我们能捕获到的是异步完成回调之后的这部分栈信息，仍然无法确定是哪里导致的错误。

3、promise执行器如果发生错误，执行器状态就会被置为rejected，fulfilled状态就不会被执
一、.catch()之后.then()

catch也会返回一个promise实例，如果没有抛出错误，也会是fulfilled状态，会执行后面的then()。

二、强烈建议在所有队列最后都加上.catch()，以避免漏掉错误处理造成意想不到的问题。
## promise.all()：批量执行 ##

1、Promise.all([p1, p2, p3,  …])用于将多个promise实例，包装成一个新的promise实例。

2、返回的实例就是普通promise

3、它接收一个数组作为参数。

4、数组里可以是promise对象，也可以是别的值，只有promise对象会等待状态改变。

5、当所有子promise都完成，该promise完成，返回值是全部值的数组。
## 实现队列 ##

1、forEach()

（1）

function queue(things) {
  let promise = Promise.resolve();
  things.forEach(thing => {
    promise = promise.then(() => {
      return new Promise(resolve => {
        doThing(thing, () => {
          resolve();
        });
      });
    });
  });
  return promise;
}
queue(['lots', 'of', 'things', ....]);
（2）常见错误：没有把.then()产生的新的promise实例赋给then,没有生成队列。

2、reduce()，数组的一端遍历到另一端。

（1）

function queue(things) {
  return things.reduce((promise, things) => {
    return promise.then(() => {
      return new Promise(resolve => {
        doThing(thing, () => {
          resolve();
        });
      });
    });
  }), Promise.resolve();
}
queue(['lots', 'of', 'things', ....]);
（2）常见错误：Promise实例创建之后，会立刻执行执行器代码，所以这个也无法达成队列的效果。
## promise.resolve() ##

1、返回一个fulfilled的promise实例，或原始promise实例。

（1）参数为空，返回一个状态为fulfilled的promise实例

（2）参数是一个跟promise无关的值，同上，不过fulfilled响应函数会得到这个参数。

（3）参数为promise实例，则返回该实例，不做任何修改。

（4）参数为thenable，立刻执行它的.then()函数

## promise.reject() ##

1、返回一个rejected的promise实例，或原始promise实例。

（1）参数为空，返回一个状态为rejected的promise实例

（2）参数是一个跟promise无关的值，同上，不过rejected响应函数会得到这个参数。

（3）参数为promise实例，则返回该实例，不做任何修改。

（4）与promise.resolve相比，不认thenable。
## promise.race() ##

1、类似promise.all(),区别在于它有任意一个完成就算完成。

2、常见用法

（1）把异步操作和定时器放在一起

（2）如果定时器先触发，就认为超时，告知用户。
## 把任何异步操作包装成promise ##

1、假设需求：

（1）用户点击按钮，弹出确认窗体。

（2）用户确认和取消有不同的处理。

let confirm = popupManager.confirm('您确定么');
confirm.promise
  .then(() => {
    // do confirm staff
  })
  .catch(() => {
    // do cancel staff
  })

// 窗体的构造函数
class Confirm{
  constructor() {
    this.promise = new Promise((resolve, reject) => {
      this.confirmButton.onClick = resolve;
      this.cancelButton.onclick = reject;
    })
  }
}

一、如果你需要在ie使用promise，有两个选择：

1、只想实现异步队列：jQuery.defered

2、需要兼容所有平台：Bluebird、 Promise polyfill

二、fetch api

1、fetch api是XMLHttpRequest的现代化替代方案。

（1）更强大，也更友好。
一、async/ await：es2017新增运算符，新的语言元素。

1、赋予javascript以顺序手法编写异步脚本的能力。

2、既保留异步运算的无阻塞特性，还继续使用同步写法。

3、还能正常使用return/ try/ catch。

4、async/ await 仍然需要promise。