---
title: Mac 终端 Git 代理
date: 2018-06-12 00:00:00
categories: 
- Git
tags:
- Git 代理
---

```shell
# 设置代理配置
git config --global http.proxy http://127.0.0.1:1080
git config --global https.proxy https://127.0.0.1:1080

git config --global http.proxy 'socks5://127.0.0.1:1080' 
git config --global https.proxy 'socks5://127.0.0.1:1080'

# 取消代理配置（如果酸酸乳关了，git 就会连接失败，用完记得关闭）
git config --global --unset http.proxy
git config --global --unset https.proxy
```
