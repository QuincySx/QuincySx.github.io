---
title: Ubuntu 管理多个会话
date: 2018-07-12 00:00:00
categories: 
- Ubuntu
tags:
- Screen
---

```
#创建新的会话
screen -S name 

#保存会话
按ctrl+a后再按d 

#恢复会话
screen -r name 

#查看会话列表
screen --list
screen -ls

#detach 某个 session
screen -d 会话名称

#kill 某个 session
screen -S 会话名称 -X quit
```
