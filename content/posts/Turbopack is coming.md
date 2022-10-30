---
title: "Turbopack Is Coming"
date: 2022-10-28T14:35:56+08:00
draft: false
author: "酱鲍"
authorLink: "https://github.com/JiangBao"
description: ""

tags: ["Turbopack"]
categories: ["技术"]
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
{{<figure src="https://vercel.com/_next/image?url=https%3A%2F%2Fimages.ctfassets.net%2Fe5382hct74si%2F5xISJZLpC7OKEDNRII3r8T%2F491842a26bbc8ed1a976393dc42e2755%2FFrame_427319031.png&w=3840&q=75">}}
<!--more-->

最近 Vercel 开源了新一代打包工具 [Turbopack](https://vercel.com/blog/turbopack)

## 简单使用
### 从现有脚手架创建项目
通过 `create-next-app` 脚手架新建一个 `Next.js` 项目，安装 `turbo` 依赖后，项目根目录添加 `turbo.json` 配置文件即可开始 `turbopack` 打包：
```json
{
  "pipeline": {
    "build": {
      "outputs": [".next/**"]
    },
    "lint": {
      "outputs": []
    }
  }
}
```
不改变源文件场景时，重复打包两次，可以体会到缓存带来的快速打包体验：
```
 Tasks:    2 successful, 2 total
Cached:    2 cached, 2 total
  Time:    297ms >>> FULL TURBO
```
{{< admonition type=tip title="cache miss 问题" details=false >}}
按照[官方文档说明](https://turbo.build/repo/docs/getting-started/add-to-project)操作，出现了 `cache miss` 问题，重复打包一直没使用缓存，后来发现是新建项目后习惯性使用了 `yarn` 安装依赖，但测试时依然使用 `npx turbo build lint` 命令导致
{{< /admonition >}}

### 新建 Monorepo
