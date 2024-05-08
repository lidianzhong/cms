---
title: "局域网访问WSL2服务"
date: 2024-04-20T02:32:28+08:00
lastmod: 2024-04-20T02:32:28+08:00
keywords:
  -
categories: # 没有分类界面可以不填写
  -
tags: # 标签
  - Network
description: ""
weight:
draft: false # 是否为草稿
comments: true # 本页面是否显示评论
reward: false # 打赏
mermaid: true #是否开启mermaid
showToc: true # 显示目录
TocOpen: false # 自动展开目录
hidemeta: false # 是否隐藏文章的元信息，如发布日期、作者等
disableShare: true # 底部不显示分享栏
showbreadcrumbs: false #顶部显示路径
cover:
  image: "" #图片路径例如：posts/tech/123/123.png
  zoom: # 图片大小，例如填写 50% 表示原图像的一半大小
  caption: "" #图片底部描述
  alt: ""
  relative: falser
---

> 在 WSL2 中运行的有 http://localhost:1188/ 的服务，如何通过 Windows 宿主机进行访问？

无需任何操作，直接在 Windows 中使用 http://localhost:1188/ 即可访问。

这种情况只针对于使用的是 localhost

[使用 WSL 访问网络应用程序 | Microsoft Learn](https://learn.microsoft.com/zh-cn/windows/wsl/networking)
