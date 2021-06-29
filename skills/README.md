# 整理开发中经常碰到的一些问题

## 后端返回 \n 前端怎么自动换行

``` jsx
<div style={{ whiteSpace: 'pre-line' }}>{value}</div>
```

## antd 组件渲染到父节点上

```jsx
getPopupContainer={triggerNode => triggerNode.parentElement}
```

## https 协议下无法下载 http协议文件

可以根据当前协议重新拼接 url

```js
const url = new URL(url) 
```

## antd Table 组件设置 scroll col 中渲染 Select 组件展示问题 

- 如果设置挂载容器 那么会撑开 table 
- 不设置会 随着滚动态条 滚动
- 解决方案 在 table 外面包裹一个 div 把 select 渲染到 这个 div 下面 
- [点我查看](https://codesandbox.io/s/table-zhong-render-select-wenti-tbz73)

## 子组件延迟渲染

今天碰到个问题, 父组件请求了几个接口后 过了好几秒子组件又重新 render , 导致用户在 input 上输入的值 被覆盖了， 最后的解决方案是 对子组件做了优化 如果 value 相同那么就不重复 render , 根本原因还是根 react 渲染机制有关 这个还得在深入学习

## 如何不自动闭合空标签

今天同事问了个问题, 空标签会自动闭合 如何解决, 这个问题主要是 eslint 导致的 只要把自动闭合的规则 禁用就行了

```json
"rules": {
    "react/self-closing-comp": 0,
  }
```

```html
<div></div>
<!-- 格式化后会成 -->
<div />
```
## antd 3 升级到 4 的一些总

table 组件 

- DataSource 必须要有一个唯一 key , 没有的 DataSource 有值组件不会显示
- 增删修改了 DataSource 必须返回一个新的 DataSource , 不然组件认为你没有修改 页面上不会更新

superfrom 组件

- 需要拷贝一分传进去， 不然会报不能修改的错误 