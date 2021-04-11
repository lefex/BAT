# vue 相关的面试题

- 聊聊 Vue 的双向数据绑定，Model 如何改变 View，View 又是如何改变 Model 的
- 聊聊 Redux 和 Vuex 的设计思想
- React 和 Vue 的 diff 时间复杂度从 O(n^3) 优化到 O(n) ，那么 O(n^3) 和 O(n) 是如何计算出来的？
- vue 在 v-for 时给每项元素绑定事件需要用事件代理吗？为什么？
- react-router 里的 <Link> 标签和 <a> 标签有什么区别
- Vue 的父组件和子组件生命周期钩子执行顺序是什么
- 为什么普通 for 循环的性能远远高于 forEach 的性能，请解释其中的原因。
- redux 为什么要把 reducer 设计成纯函数
- Vue 的响应式原理中 Object.defineProperty 有什么缺陷？为什么在 Vue3.0 采用了 Proxy，抛弃了 Object.defineProperty？
- 双向绑定和 vuex 是否冲突
- 在 Vue 中，子组件为何不可以修改父组件传递的 Prop。如果修改了，Vue 是如何监控到属性的修改并给出警告的。
- 为什么 Vuex 的 mutation 和 Redux 的 reducer 中不能做异步操作？
- Virtual DOM 真的比操作原生 DOM 快吗？谈谈你的想法。
- vue数据绑定的实现原理
- vue computed具体在什么阶段进行的依赖收集，具体的过程详细描述
- vue的生命周期
- vue父子组件通信的方式
- vue eventbus的原理
- vue中可以对对象进行数据监听，如果对于数组中的某个元素能否监听，是如何做到的
- 什么事虚拟dom
- 动态给Vue实例增加属性， this.a = 2 a之前未定义，如何监听a的变化
- 在 vue 中根据索引值修改的数据变动的，是否可以检测到，为什么？如果有这样的场景你怎么处理
- Vue中nextTick 的实现原理 与 node 中的 process.nextTick 的区别


为何组件要从直接产出 html 变成产出 Virtual DOM 呢？其原因是 Virtual DOM 带来了 分层设计，它对渲染过程的抽象，使得框架可以渲染到 web(浏览器) 以外的平台，以及能够实现 SSR 等。

http://hcysun.me/vue-design/zh/essence-of-comp.html#%E7%BB%84%E4%BB%B6%E7%9A%84%E4%BA%A7%E5%87%BA%E6%98%AF%E4%BB%80%E4%B9%88

VNode 是真实 DOM 的描述，比如我们可以用如下对象描述一个 div 标签：

vnode：虚拟 DOM
container：真实 DOM 节点