---
title: "ros 相关的安装"
date: 2024-04-10
lastmod: 2024-04-19T17:06:23+08:00
keywords: 
- 
categories: # 没有分类界面可以不填写
- 
tags: # 标签
- 安装
- ros
description: ""
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



## 安装

### `ros2 control` 安装

安装 ros2 control，`humble` 替换为你使用的版本

```shell
sudo apt install ros-humble-ros2-control
sudo apt install ros-humble-ros2-controllers
```

---

### 使用 RosTeamWS ROS工作区模板

能够快速地创建特定 ros 功能包，提供模板功能

https://rtw.stoglrobotics.de/master/index.html

---

### ros2 安装

```shell
sudo apt install ros-humble-desktop
```

https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html

---

### ignition gazebo 安装

ignition 为新一代的模拟题，替换了之前使用的 gazebo

```shell
sudo wget https://packages.osrfoundation.org/gazebo.gpg -O /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg] http://packages.osrfoundation.org/gazebo/ubuntu-stable $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/gazebo-stable.list > /dev/null
sudo apt-get update
sudo apt-get install gz-harmonic
```

https://staging.gazebosim.org/docs/harmonic/install_ubuntu

---

### 安装 python2 版本和 python3 版本的numpy

```shell
sudo apt-get install python-numpy  # python2 numpy
sudo apt-get install python3-numpy  # python3 numpy
```



