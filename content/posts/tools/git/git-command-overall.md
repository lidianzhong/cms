+++
title = 'Git 命令汇总'
date = 2024-04-01T01:09:33+08:00
draft = false
tags = ["Git"]
+++

## Git 命令汇总

### 1. 分支相关

1.1 查看当前分支

``` bash
git branch
```

1.2 创建一个新分支并切换到这个分支

```bash
git checkout -b dev		  # 创建新分支 dev 并切换到它
```

1.3 切换到某个分支

```bash
git checkout test		 # 切换到 test 分支
```

1.4 删除分支

```bash
git branch -d test		# 删除 test 分支，如果分支没有被合并，使用 -D 参数强制删除
```


### 2. 撤销相关

2.1 撤销最近的一次提交

``` bash
git reset --hard HEAD~1		# 撤销最近的一次提交
```





