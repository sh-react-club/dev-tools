# git&github

## git 使用技巧

- [tig封装了git log](https://zhuanlan.zhihu.com/p/72554875)
- [1990-script](https://github.com/antfu/1990-script)

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