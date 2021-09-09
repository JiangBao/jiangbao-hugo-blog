---
title: "Npm 安装错误整理"
date: 2020-04-07T09:36:27+08:00
draft: true
author: "酱鲍"
authorLink: "https://github.com/JiangBao"
description: ""

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

1. 使用`npm i`安装依赖包时发现报错：`ERROR:root:code for hash md5 was not found.`  
环境：Mac OS10.15.3，[参考](https://stackoverflow.com/questions/59269208/errorrootcode-for-hash-md5-was-not-found-when-using-any-hg-mercurial-command)  
解决：更新openssl `brew upgrade openssl`  