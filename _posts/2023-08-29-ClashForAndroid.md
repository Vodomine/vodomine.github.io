---
layout: post
title: Clash for Android下载、使用教程
categories: 代理设置教程
description: ClashforAndroid使用设置教程,机场推荐
keywords: 机场,Clash,免费,订阅
mermaid: false
sequence: false
flow: false
mathjax: false
mindmap: false
mindmap2: false
permalink: /:title/
---
ClashforAndroid使用clash内核，其原理是通过预先定义的规则，对网络连接进行转发，用于科学上网（翻墙）。      

最大得优点是可以根据节点延时**自动选择最快节点**，从而实现以最快的速度来访问不同的网站。  


### 1、下载地址  

[Clash for Android加速直接下载版本2.5.12](https://ghproxy.com/https://github.com/Kr328/ClashForAndroid/releases/download/v2.5.12/cfa-2.5.12-premium-armeabi-v7a-release.apk)

[Clash for Android Github下载页面](https://github.com/Kr328/ClashForAndroid/releases)，请下载版本号标记为“*Latest*”的版本 

关于下载页各版本说明：
* armeabiv-v7a: 第7代及以上的 ARM 处理器。2011年5月以后的生产的大部分Android设备都使用它.（通常下载这个就可以）
* arm64-v8a: 第8代、64位ARM处理器，现在已经是主流版本，三星 Galaxy S6是其中之一。
* armeabi: 第5代、第6代的ARM处理器，早期的手机用的比较多。
* x86: 平板、模拟器用得比较多。
* x86_64: 64位的平板。

如果已经安装了google商店，可以直接搜索Clash For Android安装使用。 


### 2、界面预览

<img src="/images/posts/Clashforandroid/main.png" width="50%" alt="Clashforandroid主界面" />

1）主界面点击配置进入配置界面

<img src="/images/posts/Clashforandroid/peizhi.png" width="50%" alt="Clashforandroid配置页面" /><img src="/images/posts/Clashforandroid/daoru.png" width="50%" alt="Clashforandroid导入" />

2）点击软件右上角的 ➕ 键，添加配置文件，有两种添加配置文件的方式,通常选择从URL导入,即从订阅连接获取配置

### 3、订阅地址获取 

首先需要注册一个机场，选择机场可以参考我的另一篇笔记[**自用过的机场记录推荐**](https://www.openwayz.com/jichang/)，注册机场后进入主页，获取订阅地址，可点击一键导入Clash配置，如果失败可复制订阅地址，使用以下步骤： 

* 把订阅地址填入下图URL处，右上角点保存
* 选中相应的机场配置，返回主界面
* 开启连接，点击启动，如果是第一次使用会提示你开启VPN连接，点击确定即可
* 检查手机状态栏右上角，是否有一个 VPN(钥匙) 图标

<img src="/images/posts/Clashforandroid/001.png" width="50%" alt="机场订阅]" /><img src="/images/posts/Clashforandroid/002.png" width="50%" alt="机场订阅]" /><img src="/images/posts/Clashforandroid/003.png" width="50%" alt="机场订阅]" /><img src="/images/posts/Clashforandroid/004.png" width="50%" alt="机场订阅]" />
  
### 3、代理模式
当按钮呈蓝色并且显示"运行中"时表示 Clash 目前正在运行中，我们可以点击"代理"来进行节点的选择以及代理模式的更改，  

## 至此，可以无阻碍使用Androids手机顺利上网了。   