---
title: '四足机器人概述'
date: 2024-04-02
draft: false
tags: ["robot", "overview"]
keywords: 
- 
categories: 
- 
description: ""
weight: 10
slug: ""
draft: false # 是否为草稿
comments: true
reward: false # 打赏
mermaid: false #是否开启mermaid
showToc: true # 显示目录
TocOpen: false # 自动展开目录
hidemeta: false # 是否隐藏文章的元信息，如发布日期、作者等
disableShare: true # 底部不显示分享栏
showbreadcrumbs: false #顶部显示路径
cover:
    image: "" #图片路径例如：posts/tech/123/123.png
    caption: "" #图片底部描述
    alt: ""
    relative: false

---

> 介绍目前全球知名的四足机器人研究组织和相关的机器人和四足机器人总体概述

---

### 四足机器人发展现状

1. **波士顿动力公司（Boston Dynamics）**

相关机器人：Altas、Stretch、Spot

2. **麻省理工学院 Biomimetic Robotics Lab**

相关机器人：MIT Cheetah、MIT Mini Cheetah

3. **苏黎世联邦理工学院（ETH Zurich）**

相关机器人：ANYmal

4. **宇树科技（Unitree Robotics）（国内）**

相关机器人：Laikago、Aliengo、A1、Go1、Go2

---

### 四足机器人的组成

**动力系统 + 控制系统 + 通信系统 + 能源系统**

动力系统：核心是机器人关节电机，需要能够对关节力矩和角度进行精确控制。

控制系统： 重点是控制算法，比如规划器和运动控制器，能够根据目标路径计算出各个关节需要执行的命令

通信系统：各个关节电机、传感器、遥控手柄的通信

能源系统：使用电池或者外部直流电源进行供电
