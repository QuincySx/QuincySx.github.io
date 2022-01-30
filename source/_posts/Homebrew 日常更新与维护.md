---
title: Homebrew 日常更新与维护
date: 2018-10-12 00:00:00
categories: 
- Homebrew
tags:
- Homebrew
---

```
brew update //更新 Homebrew

brew install #name //安装软件

brew outdated //查看那些软件可更新

brew upgrade //更新所有软件

brew upgrade #name //更新指定软件

brew cleanup //清理旧版本软件

brew cleanup #name //清理指定软件的旧版本

brew cleanup -n //查看可清理的软件

brew autoremove // 清理没有使用的依赖


// 卸载依赖的库
brew tap beeftornado/rmtree

brew rmtree git // 卸载依赖
```

