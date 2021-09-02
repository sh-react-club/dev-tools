# git&github

## git 学习

- [githowto](https://githowto.com/setup)

## git 使用技巧
- [How to learn Git slowly.](https://dev.to/samuelfaure/how-to-learn-git-slowly-38fa)
- [tig 封装了git log](https://zhuanlan.zhihu.com/p/72554875)
- [1990-script](https://github.com/antfu/1990-script)
- [Git 更安全的强制推送，--force-with-lease](https://blog.csdn.net/WPwalter/article/details/80371264)
- [如何使用 git rebase](https://zhuanlan.zhihu.com/p/145037478)

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

## git 别名

```bash
// ~/.gitconfig
[alias]
    co = checkout
    ci = commit
    st = status
    pl = pull
    ps = push
    dt = difftool
    l = log --stat
    cp = cherry-pick
    ca = commit -a
    b = branch
    pso = push origin
    plo = pull origin
    cm = commit -m
    gst = git status
    gd = git diff
    gl = git pull
    gp = git push
    glo = git pull origin
    gpo = git push origin
    gcm = git common -m
    gc = git checkout
    gcm = git checkout master
    gcd = git checkout develop
    gb = git branch
    ga = git add .

```

## git stash 用法

- git stash save 'message'
- git stash pop  弹出最近一次 stash 并且删除
- git stash apply 弹出最近一次 stash 不删除 stash
- git stash list 查看当前 stash
- git stash save -u '暂存 未被跟踪的文件'
- git stash save -a '暂存 git 工作区 所有修改的文件'
- [git stash 用法总结](https://www.cnblogs.com/tocy/p/git-stash-reference.html)
