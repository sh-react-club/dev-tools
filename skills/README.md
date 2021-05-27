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

## 本地仓库关联远程

```bash
echo "# my-test" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:BestDingSheng/my-test.git
git push -u origin main
#
git remote add origin git@github.com:BestDingSheng/my-test.git
git branch -M main
git push -u origin main
```
