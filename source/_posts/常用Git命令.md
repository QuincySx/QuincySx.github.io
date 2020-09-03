---
title: 常用 Git 命令
date: 2018-06-13 13:47:40
categories: 
- Git
tags:
- Git
---

```
  //添加远程仓库
  git remote add origin git@github.com:xx.git
  
  //删除远端分支
  git push origin --delete <branchName>
  
  //添加 Tag
  git tag v1.0
  
  //删除远端 Tag
  git push origin --delete tag <tagname>
  
  //暂存文件
  git stash
  
  //拿出暂存文件
  git stash pop
  
  //合并单次提交
  git cherry-pick 62ecb3
  
  //提交代码
  //远端没有 local_branch
  git push origin local_branch:remote_branch
  //本地有 remote_branch
  git push -u origin/remote_branch
  
  //拉取代码
  git pull origin local_branch:remote_branch
```


![Git 速查表](http://image.smallraw.com/Git速查表.png)

