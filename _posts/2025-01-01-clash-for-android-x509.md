---
layout: post
title: 解决导入订阅报错x509 certificate signed by unknown authority
categories: 经验分享
description: 有些安卓手机用户的用户使用clash for android代理软件来做梯子，但是导入机场订阅的时候会报错，failed to verify certificate:x509:certificate signed by unknown authority,这种问题该如何解决呢？本文介绍一下产生该问题的原因以及解决方案
keywords: X509
mermaid: false
sequence: false
flow: false
mathjax: false
mindmap: false
mindmap2: false
topmost: false
permalink: /:title/
---

有些安卓手机用户的用户使用clash for android代理软件来做梯子，但是导入机场订阅链接的时候会报错，x509 certificate signed by unknown authority，很多用于遇到这种问题会不知道怎么回事，无法使用，以为是被骗了。  

### 问题原因

在使用代理软件的过程中，我们经常会遇到一些奇奇怪怪的小问题导致无法使用，其实只要根据软件的报错信息，借助搜索引擎查一下就可以很轻松的解决这些问题failed to verify certificate:x509:certificate signed by unknown authority从这个报错中就可以看出是因为订阅链接的SSL证书有问题，大部分订阅网址使用的证书都是Let's Encrypt免费签发的，2015年的时候，所有主流浏览器和操作系统都无法信任Let’s Encrypt的根证书， 新的根证书需要数年时间才能通过所有安全审核和规定，于是Let’s Encrypt 使用第三方根证书IdenTrust DST Root X3证书，但IdenTrust根证书于2021年9月30日到期，这给Let’s Encrypt的用户带来了兼容性问题，尤其是安卓用户，因为clash for android这个软件的验证机制问题，较老的安卓手机会无法通过证书验证，系统内置的 DST Root CA X3 证书在 2021 年 9 月 30 日过期了，所以就会报这个X509错误，而Clash for Android这个软件也早就无人维护了，所以这个问题也就一直存在了。

### 解决办法

解决方法也很简单，机场的订阅只是个加密的线路规则文件而已，代理软件都是通用的，Clash for Android不能用，我们就换个其他比较新的正在维护的软件即可Surfboard或者clash meta for android等，推荐使用Surfboard,在安卓系统上Surfboard 的界面相比Clash 更为美观、直观，可以在主界面很方便地查看网络速度、代理规则，公网IP等等信息，Surfboard的官方下载地址在Github上，下载链接[https://github.com/getsurfboard/surfboard/releases](https://github.com/getsurfboard/surfboard/releases)
使用方式也很简单，都是通用的，复制链接，导入订阅，选择规则模式，开启代理开关就可以用了。

![surfboard](/images/posts/surfboard/surfboard.png)

  






