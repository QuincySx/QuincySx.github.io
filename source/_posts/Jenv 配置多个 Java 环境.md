---
title: Jenv 配置多个 Java 环境
date: 2019-04-12 00:00:00
categories: 
- Ubuntu
tags:
- Jenv 配置
---

```shell
// 安装
brew install jenv

// 配置文件配置
export PATH=$HOME/.jenv/bin:$PATH
eval "$(jenv init -)"

// 显示全部版本
jenv versions

// 添加新版本
jenv add /Library/Java/JavaVirtualMachines/jdk1.8.0_211.jdk/Contents/Home/

// 删除版本
jenv remove 1.6

// 显示当前版本
jenv version

// 设置本地应用
jenv local 1.8.0.25

// 设置全局应用
jenv global 1.8.0.25

// 设置终端应用
jenv shell 1.8.0.25

// 显示路径
jenv which java

// 设置 JAVA_HOME，运行后需要重启
jenv enable-plugin export
```
