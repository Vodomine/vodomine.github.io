---
layout: post
title: Clash for Windows下载、使用教程
categories: 代理设置教程
description: Clash for windows使用设置教程,参照此篇教程可下载，并且快速应用订阅实现上网
keywords: 机场,Clash,免费,订阅
mermaid: false
sequence: false
flow: false
mathjax: false
mindmap: false
mindmap2: false
permalink: /:title/
---
Clash是一个开源、免费的网络连接代理内核，其原理是通过预先定义的规则，对网络连接进行转发，用于无限制上网。        

最大得优点是可以根据节点延时**自动选择最快节点**，从而实现以最快的速度来访问不同的网站。  


### 1、下载地址  

> **注意!**安装版或者解压缩版都不能有中文目录！   

[Clash for Windows 0.20.39解压缩版代理下载](https://ghproxy.com/https://github.com/BoyceLig/Clash_Chinese_Patch/releases/download/0.20.39/Clash.for.Windows-0.20.39-win.7z)

### 2、配置使用教程 

- 1、首先需要注册一个机场，选择机场可以参考我的另一篇笔记🔥[**自用过的机场记录推荐**](https://vodomine.github.io/2023/08/21/Aircraft-used/)，注册机场后进入主页，如下图操作，其他机场界面可能不一致，但基本大同小异，其中都有一键订阅部分  
    
    ![机场订阅](/images/posts/Clash/001.png)
    ![机场订阅](/images/posts/Clash/002.png)

**(可选)**若上面的一键订阅失败，可尝试点击"复制订阅地址"，手动粘贴到Clash For Windows客户端中  
    ![机场订阅](/images/posts/Clash/003.png)
    
- 2、通过订阅链接下载配置文件，在(Profiles)配置文件一栏里面，复制你购买订阅的链接 URL，然后点击 download（下载）按钮下载订阅文件  
    
    ![机场订阅](/images/posts/Clash/004.png)
    
- 3、切换到 proxies一栏，上面选择**Rule(符合规则国外网址的走代理，国内网址直连不消耗流量)**，**Global(就是所有网址都走代理，一般不选择这个)**，列表中会看到很多节点，单击无线图标可以查看延迟。用鼠标点下即可选择你想要的节点。推荐直接使用**自动选择**，除非是想用某个地址的特定代理使用某种业务，比如使用ChatGPT,那就得一般选择美国节点比较好，其他不懂的不要动。
    
    ![机场订阅](/images/posts/Clash/clash-sub2.webp)
    
- 4、点击常规,打开系统代理和开机启动两项即可。其实只打开系统代理就可以使用，但是关机前要关闭这里的系统代理，不然下次开机，如果没有开Clash,浏览器就不能上网了。  
    
    ![使用Clash](/images/posts/Clash/005.png)


### 3、代理模式解释 

- 全局（Global）：所有请求直接发往代理服务器    
- 规则（Rule）：所有请求根据配置文件规则进行分流    
- 直连（ Direct ）：所有请求直接发往目的地    

## 至此，可以无阻碍顺利上网了。   