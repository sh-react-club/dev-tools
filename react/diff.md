# 我理解的 react diff 

传统的 diff 算法是递归比较 时间复杂度 on3 次方 , 性能比较低

react diff 算法做了优化 时间复杂度 on 

## 如果做到的 

三个策略

- web 中的 dom 一般不会跨层级移动
- 相同的组件会生成相同的树形接口
- 同一层级的子节点会有相同的 key 

分三层比较 

root 根节点比较 如果不一样 那么直接删除 重新创建
component 组件比较
元素比较
    类型有 删除 移动 更新



## 参考资料

[不可思议的 react diff](https://zhuanlan.zhihu.com/p/20346379)