---
title: "Ubuntu 常用命令汇总"
date: 2024-04-16T01:20:57+08:00
lastmod: 2024-04-16T01:20:57+08:00
keywords: 
- 
categories: # 没有分类界面可以不填写
- 
tags: # 标签
- Ubuntu
# description: "Ubuntu 常用命令汇总"
weight:
draft: false # 是否为草稿
comments: true # 本页面是否显示评论
reward: false # 打赏
mermaid: true #是否开启mermaid
showToc: true # 显示目录
TocOpen: true # 自动展开目录
hidemeta: false # 是否隐藏文章的元信息，如发布日期、作者等
disableShare: true # 底部不显示分享栏
showbreadcrumbs: true #顶部显示路径
cover:
    image: "" #图片路径例如：posts/tech/123/123.png
    zoom: # 图片大小，例如填写 50% 表示原图像的一半大小
    caption: "" #图片底部描述
    alt: ""
    relative: false
---

### apt 清华源

配置地址：`/etc/apt/sources.list`

[ubuntu | 镜像站使用帮助 | 清华大学开源软件镜像站 | Tsinghua Open Source Mirror](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/)

### 解压 tar.gz 文件

```shell
tar -xzvf filename.tar.gz
```

### 清华 conda 镜像

```shell
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/linux-64/
conda config --set show_channel_urls yes
```

### pip 清华源

临时使用：`pip install -i https://pypi.tuna.tsinghua.edu.cn/simple some-package`

设为默认：`pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple`

[pypi | 镜像站使用帮助 | 清华大学开源软件镜像站 | Tsinghua Open Source Mirror](https://mirrors.tuna.tsinghua.edu.cn/help/pypi/)
