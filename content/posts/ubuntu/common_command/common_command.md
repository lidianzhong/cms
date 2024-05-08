---
title: "Ubuntu 常用命令"
date: 2024-04-16T01:20:57+08:00
lastmod: 2024-04-16T01:20:57+08:00
keywords:
  -
categories: # 没有分类界面可以不填写
  -
tags: # 标签
  - Ubuntu
# description: "Ubuntu 常用命令汇总"
weight: 10
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
  relative: false
---

## 国内镜像源

---

### apt 清华源

配置地址：`/etc/apt/sources.list`

[ubuntu | 镜像站使用帮助 | 清华大学开源软件镜像站 | Tsinghua Open Source Mirror](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/)

<details>
<summary>快速配置镜像源</summary>

1. Ubuntu 20.04 LTS

```shell
echo "deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
deb http://security.ubuntu.com/ubuntu/ focal-security main restricted universe multiverse" > /etc/apt/sources.list
```

2. Ubuntu 22.04 LTS

```shell
echo "deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ jammy main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ jammy-updates main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ jammy-backports main restricted universe multivers
deb http://security.ubuntu.com/ubuntu/ jammy-security main restricted universe multiverse" > /etc/apt/sources.list
```

清除所有软件源

```shell
rm -rf /etc/apt/sources.list.d/*
```

</details>

apt 官方源：[Ubuntu 22.04 系统默认官方源/腾讯云源/清华源/中科大源/阿里云源](https://wph.im/213.html)

### pip 清华源

临时使用：`pip install -i https://pypi.tuna.tsinghua.edu.cn/simple some-package`

设为默认：`pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple`

[pypi | 镜像站使用帮助 | 清华大学开源软件镜像站 | Tsinghua Open Source Mirror](https://mirrors.tuna.tsinghua.edu.cn/help/pypi/)

### conda 清华镜像源

```shell
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/linux-64/
conda config --set show_channel_urls yes
```

### npm 源

npm config set registry https://registry.npmmirror.com

[npm 使用国内淘宝镜像（最新地址）\_npm 最新淘宝镜像-CSDN 博客](https://blog.csdn.net/chaoPerson/article/details/136121885)

<br>

## 进程

查看某个进程 PID 的详细信息：`ps -f -p  <PID>`

[Ubuntu 查看 GPU 进程的详细信息 - DuanYongchun - 博客园 (cnblogs.com)](https://www.cnblogs.com/dyc99/p/14597853.html)

<br>

## 其它命令

解压 tar.gz 文件：`tar -xzvf filename.tar.gz`

<br>

## 相关问题

---

apt 相关问题汇总：[apt 相关问题](/posts/ubuntu/problem/apt_problem)
