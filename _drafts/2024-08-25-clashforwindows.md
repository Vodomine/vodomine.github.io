---
layout: post
title: Clash for Windows下载、使用教程
categories: 代理设置教程
description: Clash for windows使用设置教程,参照此篇教程可下载，并且快速应用订阅实现上网，Clash号称小猫咪，基本大家都知道这是干吗用的，有的人可能不知道机场，但是知道clash是干嘛用的，其实clash只是个内核，上面加了一层皮肤，界面不一样就衍生出了现在的很多版本，什么clash for windows,clash verge等等
keywords: Clash
mermaid: false
sequence: false
flow: false
mathjax: false
mindmap: false
mindmap2: false
permalink: /:title/
---
Clash号称小猫咪，基本大家都知道这是干吗用的，有的人可能不知道机场，但是知道clash是干嘛用的，其实clash只是个内核，上面加了一层皮肤，界面不一样就衍生出了现在的很多版本，什么clash for windows,clash verge等等，不过只是界面不一样，功能基本都是一样的，windows下推荐用clash for windows。        

比起V2rayN这些软件，它的界面更加简介，最大得优点是可以根据节点延时**自动选择最快节点**，从而实现以最快的速度来访问不同的网站，这个对于小白用户相当之友好，最早我还是小白的时候就是因为这个功能选择用它。  


### 1、下载地址  

> **注意!** 

[Clash for Windows 0.20.39地址](hhttps://mirror.ghproxy.com/https://raw.githubusercontent.com/OpenWayz/OpenWayz.github.io/main/Clash.for.Windows-0.20.39-win.7z)

### 2、配置使用教程 

- 1、首先需要注册一个机场，这就不用说了，clash相当于我们用的手机，买的机场相当于是个手机卡，不买手机卡那就不能上网，选择机场可以参考我的另一篇笔记🔥[**自用过的机场记录推荐**](https://www.openwayz.com/jichang/)，如下图操作，一键订阅  
    
    ![机场订阅](/images/posts/Clash/001.png)
    ![机场订阅](/images/posts/Clash/002.png)

**(也可以手动导入)**点击"复制订阅地址"，手动粘贴到Clash For Windows中导入
    ![机场订阅](/images/posts/Clash/003.png)
    
- 2、通过订阅链接就可以下载配置文件，在(Profiles)配置文件一栏里面，粘贴订阅链接，然后点击 download按钮即可  
    
    ![机场订阅](/images/posts/Clash/004.png)
    
- 3、切换到 代理模式proxies一栏，上面选择**Rule(符合规则国外网址的走代理，国内网址直连不消耗流量)**，**Global(就是所有网址都走代理，一般不选择这个)**，列表中会看到很多节点，单击无线图标可以查看延迟。用鼠标点下即可选择你想要的节点。可点击选择使用**自动选择**，也可以手动选择自己想用的节点，如果网速慢的话也可以切换节点。

    ![机场订阅](/images/posts/Clash/clash-sub2.webp)
    
- 4、点击常规,打开系统代理和开机启动两项即可。只打开系统代理就可以使用，但是关机前要关闭这里的系统代理，不然下次开机，如果没有开Clash,浏览器就不能上网了。  
    
    ![使用Clash](/images/posts/Clash/005.png)


### 3、代理模式解释 

- 全局（Global）：就是所有网址都走代理，用个微信都走流量    
- 规则（Rule）：国外网址的走代理，国内网址直连不消耗流量    
- 直连（ Direct ）：和不用梯子一个作用    

## 设置完成就可以无阻碍顺利上网了。   
