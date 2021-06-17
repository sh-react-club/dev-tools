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