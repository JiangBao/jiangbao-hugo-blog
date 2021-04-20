---
title: "Node Process Fail Due to Out of Memory"
date: 2021-04-20T11:25:50+08:00
draft: false
author: "酱鲍"
authorLink: "https://github.com/JiangBao"
description: "mac m1 下 Node.js 程序错误"

tags: ["工具"]
categories: ["问题归档"]
hiddenFromHomePage: false

featuredImage: ""
featuredImagePreview: ""

toc: false
autoCollapseToc: true
math: false
lightgallery: true
linkToMarkdown: false
share:
  enable: false
comment: false
---

<!--more-->

最近换了新的`MacBook M1`开发，一个旧项目运行出现了`out of memory`的错误：
![node out of memory](https://jiangbao-1258001083.cos.ap-shanghai.myqcloud.com/node-out-of-memory.png)

> 环境
> * Node.js: v14.16.1
> * OS: macOS Big Sur with an M1 chip

找了一下，貌似还是`M1`芯片下比较常见的问题，参考[此处](https://github.com/TypeStrong/typedoc/issues/1491)，升级至`Node.js v15`解决了此问题。