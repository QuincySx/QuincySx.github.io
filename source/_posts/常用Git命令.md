---
title: 常用 Git 命令
date: 2020-06-13 13:47:40
categories: 
- Git
tags:
- Git
---

```
  //添加远程仓库
  git remote add origin git@github.com:xx.git
  //同步远程仓库内容
  git remote update
  
  // 删除远端分支
  git push origin --delete <branchName>
  
  // 添加 Tag
  git tag v1.0
  
  // 推送本地 Tag 到远端
  git push origin <tagname>
  
  // 删除远端 Tag
  git push origin --delete tag <tagname>
  
  // 暂存文件
  git stash
  
  // 拿出暂存文件
  git stash pop
  
  // 合并单次提交
  git cherry-pick 62ecb3
  
  // 提交代码
  // 远端没有 local_branch
  git push origin local_branch:remote_branch
  //本地有 remote_branch,远端也会相应的创建 remote_branch 分支
  git push -u origin/remote_branch
  
  // 拉取代码
  git pull origin local_branch:remote_branch
  
  // 删除本地有远端没有的分支
  git fetch -p
  
  // 查看文件 log
  git log <fileName>
  // 恢复一个文件到历史状态
  git reset <commit-id> <fileName>
  
  // 重新编辑当前提交
  git commit --amend
```

## rebase -i 高级用法
```
对于已经存在但还没有推送到远程的提交记录，我们可以使用 rebase -i 去编辑他们。假设我们想修改最近三次提交，可以输入 gri head~3，它是完整写法是：

git rebase -i head~3
这个命令会展示出最近的三次提交，最老的提交在最上面，最新的提交在最下面，这是因为 git 会按照从旧到新的顺序编辑这些提交。展示的格式如下：

pick commit_id commit_message
我们可以随意调整这三行的顺序，相当于改变提交的顺序。如果把单词 pick 改成 reword 或 r，就可以修改提交记录。

git 还支持以下关键字：

edit 或 e：编辑此次提交
drop 或 d：删除此次提交
fix 或 f：将此次提交与上次提交合并
```


![Git 速查表](http://image.smallraw.com/Git速查表.png)

