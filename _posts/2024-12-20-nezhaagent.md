---
layout: post
title: 哪吒监控如何修改agent的配置，不监控进程数和连接数，禁止自动升级
categories: 经验分享
description: 哪吒监控迁移面板并且修改agent的配置，不监控进程数和连接数，禁止自动升级
keywords: 哪吒监控
mermaid: false
sequence: false
flow: false
mathjax: false
mindmap: false
mindmap2: false
topmost: false
permalink: /:title/
---

如果你手里有很多VPS，那肯定需要一个工具来监控和管理这些服务器，俗称探针，而哪吒监控就是广泛在被使用的一个项目，在玩服务器VPS的圈子里大家都是很熟悉的，它是一款轻量化的服务器监控和运维工具，提供实时性能监控与告警通知，能让我们方便的管理自己拥有的服务器，直观的看到服务器数量，以及CPU,内存，硬盘，网络等情况的资源占用，及时处理服务器离线，资源超载等情况，面板截图如下。

![nezha](/images/posts/nezha/nezha.png)

### 哪吒监控的使用

哪吒监控是个开源项目，作者提供了比较详细的文档来指导用户安装使用，有很易用的一键安装脚本，基本就算你不懂也可以傻瓜化的一键安装，[哪吒官网使用文档地址](https://nezha.wiki/guide/dashboard.html)  

虽然可以很简单的安装，但是有时候因为我们的机器状况和项目不同会需要对监控项做一些自定义设置，这时需要去修改agent(被监控的服务器)的配置，比如我用的服务器资源比较有限，而且并发连接数高，服务器还需要能长期稳定工作，所以我希望能设置不监控连接数和进程数，同时禁用哪吒监控的自动升级（这一点需要吐槽，哪吒的升级比较频繁，很担心哪一个版本别有什么不完善的地方，升级后让整个服务器挂掉），最近正好用到，简单整理一下分享出来。

### 如何修改Agent配置

```nano /etc/systemd/system/nezha-agent.service```

编辑/etc/systemd/system/nezha-agent.service，

nezha-agent.service这文件中有一行
```ExecStart=/opt/nezha/agent/nezha-agent -s xxx.xxx.xxx:5555 -p xxxxxxxxxxx```
在 ExecStart= 这一行的末尾加上

```ExecStart=/opt/nezha/agent/nezha-agent -s xxx.xxx.xxx:5555 -p xxxxxxxxxxx --skip-conn --skip-procs --disable-auto-update```

就可以起到不监控连接数，进程数，禁用自动升级的功能。

还可以加入其他配置项，如下：
--report-delay 系统信息上报的间隔，默认为 1 秒，可以设置为 3 来进一步降低 agent 端系统资源占用（配置区间 1-4）
--skip-conn 不监控连接数，机场/连接密集型机器推荐设置，不然比较占 CPU(shirou/gopsutil/issues#220)
--skip-procs 不监控进程数，也可以降低 agent 占用
--disable-auto-update 禁止 自动更新 Agent（安全特性）
--disable-force-update 禁止 强制更新 Agent（安全特性）
--disable-command-execute 禁止在 Agent 机器上执行定时任务、打开在线终端（安全特性）
--tls 启用 SSL/TLS 加密（使用 nginx 反向代理 Agent 的 grpc 连接，并且 nginx 开启 SSL/TLS 时，需要启用该项配置）


修改完后执行命令Ctrl+O，Ctrl+O，保存，退出nano编辑器。

然后执行命令
```systemctl daemon-reload && systemctl restart nezha-agent```

就可以让配置生效了，后面即使VPS重启也可以保持修改后的配置生效。






