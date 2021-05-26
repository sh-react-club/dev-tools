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