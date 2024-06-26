---
title: "Representation Learning"
date: 2024-04-22T03:18:36+08:00
lastmod: 2024-04-22T03:18:36+08:00
keywords:
  -
categories: # 没有分类界面可以不填写
  -
tags: # 标签
  -
description: ""
weight:
draft: true # 是否为草稿
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

## 什么是 Representation Learning（表征学习）

机器学习算法的 work 与否不仅仅取决于算法的正确选用，也取决于数据的质量和有效的表示（representation）。针对不同类型的数据（text，image，video），不同的表示可能会导致有效信息的缺失或是曝露，这决定了算法能否有效地解决问题。表征学习的目的是对复杂的原始数据化繁为简，把原始数据的无效的或者冗余的信息剔除，把有效信息进行提炼，形成特征（feature）。

特征提取可以人为地手工处理，也可以借助特定的算法自动提取。Roughly Speaking， 前者为特征工程，后者为表征学习（Representation Learning）。如果数据量较小，我们可以根据自身的经验和先验知识，人为地设计出合适的特征，用作下游的任务，比如表征学习同样在人工智能领域有着相当重要的地位。 我们已经知道人类的信息处理过程与长期记忆和短期记忆密切相关。短期记忆是短期存储的记忆，长期记忆就是我们大脑中长期存储的知识，就像在图书馆中存储的海量文献。根据这个简单的信息处理模型，再加上计算机更快的计算速度和海量的存储空间，人工智能应该比人类更为强大才是。但至少到目前，我们看到的情况并非如此。这其中一个重要的原因就是我们还未能破解人类大脑究竟是如何对数据进行编码，和对知识进行存储的。处理外界信息的第一步就是要将其编码，投影到某一空间。比如说，当人类仅需要几个例子就可以区分猫和狗的不同，而机器却需要大量数据训练时，我们不由得想要探寻：人类是如何对图像进行编码的？他提取了哪些特征可以通过少量样本进行学习？为什么人类学习的知识更灵活，可以在更多方面应用，而机器学习的模型通用性往往很差？这正是表征学习探索的目标：寻找对数据更好的表示方式。（机器学习的目的就是学习物质的有限个特征，而这些特征都要从数据里来。数据如何更够更好地反应我们需要的特征，让数据能够更多更准确地得到物质的特征，这个工作可以由人工处理完成，也可以通过自动化的表征学习来完成）。

一般来说，数据该如何进行表示能收到更好的效果，是各个数据更加独立？还是其它？

在单个任务中，选用什么样的数据表示更好，比如在图像中，设计的 HSV 就比 RGB 一般效果要好
