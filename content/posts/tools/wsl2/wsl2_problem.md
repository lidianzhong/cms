+++
title = 'WSL 问题汇总'
date = 2024-04-03
draft = false
tags = ["WSL2", "BUGS"]
+++



## 安装问题

1. 无法解析的服务器名称，`Error code: Wsl/WININET_E_NAME_NOT_RESOLVED`

```shell
PS C:\Users\DianzhongLi> wsl --list --online
无法从“https://raw.githubusercontent.com/microsoft/WSL/master/distributions/DistributionInfo.json”中提取列表分发。无法解析服务器的名称或地址
Error code: Wsl/WININET_E_NAME_NOT_RESOLVED
```

解决方法：
1. 使用代理或者VPN
1. 在 `hosts` 中指定 `raw.githubusercontent.com`  的对应ip

[安装 WSL 报错 Error code: Wsl/WININET_E_NAME_NOT_RESOLVED 问题解决-CSDN博客](https://blog.csdn.net/u013737132/article/details/136280824)



