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
- 曾经vue 用过的宏任务 微任务
 - MessageChanel 消息通道 宏任务



 # vue的响应式-2

 1. 数组
    > 通过索引的方式更改数组（不会重新渲染页面）
    > 更改长度（不会重新渲染页面）

2. 对象
    > 增删 对象（不会重新渲染页面）

- 数组（想要重新渲染页面，使用数组的变异方法）
1. 变异方法：push pop shift unshift sort reverse splice
2. vm.$set(要改谁，改什么，改成啥) 或者用 Vue.set(要改谁，改什么，改成啥)
3. vm.$delete(要删除谁，删什么)

- 对象
1. vm.$set(要改谁，改什么，改成啥) 或者用 Vue.set(要改谁，改什么，改成啥)
2. vm.$delete(要删除谁，删什么)