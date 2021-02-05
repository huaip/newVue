# Vue的响应式-1
- 数据变化，页面会重新渲染
> Object.defineProperty 实现数据劫持
>
> 以下两点，不会重新渲染页面
- 未经声名的
- 未使用的
> 
>
>
- 更改数据后，页面会重新渲染吗
> 不会的,页面渲染的操作是异步执行的
> 同步执行栈，异步队列(宏任务、微任务，event loop 事件环)
> 宏任务：setTimeout、 setImmediate
> 微任务 Promise.resolve.then() 、MutationObserve 突变观察

> vm.$el 内部的this指向vue实例
> vm.$nextTick() 内部的this指向window
> 区别？