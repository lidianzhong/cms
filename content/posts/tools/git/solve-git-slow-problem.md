---

title: '解决Git同步访问慢的问题'
date: 2024-04-01T01:09:33+08:00
draft: false
tags: 
    - "Git"
    - "Bugs"
---

> 在我们想要将本地的代码提交到Github远程仓库时，会因为网络问题，拉取失败。

---

### 解决Git提交拉取时的网络问题

1. 查询以下网址对应的`DNS`服务器地址: [DNS查询工具](https://tool.chinaz.com/dns)
```shell
github.com
github.global.ssl.fastly.net
assets-cdn.github.com
```

2. 修改 `hosts` 文件
```bash
20.205.243.166 github.com
66.220.148.145 github.global.ssl.fastly.net
185.199.111.153 assets-cdn.github.com

# https://tool.chinaz.com/dns/github.com
# https://tool.chinaz.com/dns/github.global.ssl.fastly.net
# https://tool.chinaz.com/dns/assets-cdn.github.com
```

---

### 解决 Git clone 时的网络问题
1. 加个`fast`：`https://github.com/` 改为 `https://githubfast.com/`
2. 使用镜像仓库：[Github镜像仓库](https://www.sockstack.cn/github)


<br>