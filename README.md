# learn-react-source-code
学习 react 源码  
react 源码

UI=fn(x)

Fiber

## 目录
- React API
  - createElement
    - ReactElement
      - $$typeof: REACT_ELEMENT_TYPE
    - Component
    - PureComponent
  - createRef & ref
    - stringref
    - function
    - React.createRef()
    - React.forwarRef()
  - createContext
    - childContextType
      - `getChildContext(){return {value: this.state.childContext}}`,`Parent.childContextTypes={value: PropTypes.string}`
      - `Child.contextTypes={value: PropTypes.string}`,`this.context.value`
    - createContext
      - `const {Provider, Consumer} = React.createContext('default')`
      - `<Provider value={this.state.newContext}></Provider>`
      - `<Consumer>{value => <p>new Context {value}</p>}</Consumer>`
  - JSX => JS
  - ConcurrentMode
  - Component
  - Suspense
    - lazy
  - Hooks
- React 中的更新创建
  - ReactDOM.render
  - Fiber
  - UpdateQueue
  - FiberRoot
  - Update
  - expirationTime
- Fiber Scheduler
  - scheduleWork
  - batchedUpdates
  - performWork
  - performUnitOfWork
  - requestWork
  - react scheduler
  - renderRoot
- 开始更新
  - beginWork 以及优化
  - 各类组件的更新过程
  - 调和子节点的过程
- 完成各个节点的更新
  - completeUnitOfWork
  - completeWork
  - unwindWork
  - 虚拟 DOM 对比
  - 错误捕获处理
  - 完成整棵树更新
- 提交更新
  - commitRoot 整体流程
  - 提交快照
  - 提交 DOM 更新
  - 提交所有声明周期
  - 开发时的帮助方法
  - 提交 DOM 插入
  - 提交 DOM 删除
- 各种功能的实现过程
  - context 的实现过程
  - ref 的实现过程
  - hydrate 的实现过程
  - React 的事件体系
- Suspense
  - 更新优先级的概念
  - Suspense 组件更新
  - retry 重新尝试渲染
  - 更新挂起的概念
  - timeout 处理
  - lazy 组件更新
- Hooks
  - 核心原理
  - useEffect
  - useState
  - useContext
  - 其它 Hooks API

在接触一个新事物之前最大的困难不是不理解而是不知道。

### 通读源码不是目的
- 外在
  - 提高开发能力
  - 解决问题能力
  - 提升自身价值
- 内在
  - 提升学习能力
  - 提升思考能力
  - 提升设计能力
