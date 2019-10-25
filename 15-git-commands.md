---
layout: home
title: Git常用命令
---

## Git常用命令

### 基本操作

查看远程库连接
```
git remote -v
```
![git remote -v]({{site.baseurl}}/assets/15-remote-version.png)

切换分支
```
git checkout branch
```
![git checkout branch]({{site.baseurl}}/assets/15-switch-branch.png)

相同分支, 从远程到本地同步
```
git pull
```
![git pull]({{site.baseurl}}/assets/15-git-pull.png)

添加本地更改
```
git add -A
```

提交本地更改
```
git commit -m 'comment'
```

相同分支, 从本地同步到远程
```
git push origin branch
```
![git push origin master]({{site.baseurl}}/assets/15-git-push.png)

### 高级操作

远程覆盖本地(强制)
```
git fetch --all
git reset --hard origin/master (这里master要修改为对应的分支名)
git pull
```
本地覆盖远程(强制)
```
git push origin master --force
```

不同分支之间的同步, 用`rebase`命令将branch重新rebase到master
```
git checkout branch
git rebase master
```
![git rebase]({{site.baseurl}}/assets/15-git-rebase.png)
