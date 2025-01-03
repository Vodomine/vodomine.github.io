---
layout: post
title: Clash删库始末及知识普及
categories: 机场观察
description: 2023年11月初发生了Clash删库事件，很多不知情的小白在国内媒体上参与讨论传播，都上了热搜了，这种东西拿出来讨论也是无知，吓的所有这些软件的关联作者都删除了网上的下载链接，很多人不能区分Clash for windows和Clash内核，以及他们买的代理节点订阅之间的关系，本篇文章给大家说明一下相关内容
keywords: Clash删库
mermaid: false
sequence: false
flow: false
mathjax: false
mindmap: false
mindmap2: false
topmost: false
permalink: /:title/
---
2023年11月初发生了Clash删库事件，很多不知情的小白在国内媒体上参与讨论传播，都上了热搜了，这种东西拿出来讨论也是无知，吓的所有这些软件的关联作者都删除了网上的下载链接，很多人不能区分Clash for windows和Clash内核，以及他们买的代理节点订阅之间的关系，本篇文章给大家说明一下相关内容。

### 名词解释

* Clash for window --简称CFW,这是个套了Clash内核的UI,可以理解成是一个皮，引发整个事件第一个删库的作者就是他。   

* Clash Core --Clash核心，这个才是软件的根本，套上不同的UI就是不同平台的的不同软件，Clash for windows,clash for android,Clash verge,ClashX都是基于它的UI，这个内核是另一个作者。  

* 节点订阅 --用户们花钱在机场买的是它，不是Clash,没了Clash还可用其他代理软件，比如V2Ray等，售卖给用户的卖家也跟前面Clash内核和CFW的作者完全无关。

* Clash库和Clash for windows等程序 --作者只是把Github官网上的源代码还有程序下载链接都删除了，但是用户已经下载下来的程序是可以继续用的，这个毫不影响，除非代理协议有大的变更或者有重大漏洞，这些软件不更新就不支持了或者无法修复漏洞了，实际上代理协议能用很久，软件只要没漏洞也没必要去更新，稳定在用个几年可能都没问题，后面自然会有新的工具出现来替代。

### 删库始末

* 第一天，11/2号下午3点，clash for windows作者Fndroid发出公告：“停止更新了，江湖再见吧😅”，原因未知，网上很多谣言，但能确认的是作者没有被控制，人身自由。当天有微博大V在墙内微博转发。

* 第二天，11/3号，随着国内大V转发以及不明真相的网友热议，迅速成为热门新闻，进入微博热搜和抖音热门，看网友讨论里面净是笑话，好多人在骂刚买了白花钱了，这些人希望能有机会看到我上面的名词解释，一些清醒的用户在评论中劝阻大家停止讨论，别把事情搞大，可是已经晚了，一些无知或者无良大V，自媒体号为了凑热度仍然在疯狂发布相关话题，然后就是Clash社区当天全部内容相关作者为了避免风险都删库了，clash 内核，ClashForAndroid，OpenWrt helloword插件，Gui.For.Clash，Clash.Meta，clash-verge，ClashMetaForAndroid，tuic，Fclash，shellclash，有一个算一个，有影响力的都删了。请注意：这些Ui作者都好好的，都不是被抓了或者被控制了，请不要传播谣言！

### Clash文件备份

Clash系列备份：[需科学访问https://mega.nz/folder/orkzRYbR#bHhSjy9r_9AJayIgqtZTag](https://mega.nz/folder/orkzRYbR#bHhSjy9r_9AJayIgqtZTag)
包括：
* Clash for Windows 0.20.29版本
* Clash for Android 2.5.12和3.0.3版本
* ClashMetaForAndroid 2.9.0版本
* ClashX 1.118.0版本
* ClashX Pro 1.118.1版本
* lashX meta 1.3.7 版本
* metacubexd 1.129.0版本
* Open Clash 0.45.141版本
* clash verge 1.3.8版本

以及clash核心
* clash 1.18.0版本
* clash Core Premium
* clash meta 1.16.0 和alpha版本
* OpenClash-core master和dev

### 删库停更有什么影响？

* 1.clash删库停更不代表clash不能用，都可以正常使用，停止维护对大家影响其实不大，只要不爆出大漏洞正常使用即可。毕竟现在机场都是ss协议为主，而且clash.meta是开源的，大家都可以接手维护。clash社区作者们暂时停更主要是为了避风头，过了这段时间应该就好了，CFA一年没更新，安卓手机绝大部分都还正常用着它，最大影响可能是未来出现的新协议新特性，无法在这些停更软件上使用，但那时会有新的软件。

* 2.clash删库停更是否还安全？目前没有漏洞都是安全的，都可以正常使用。有些人担心clash for windows作者被控制了，担心留有后门，电脑被监控。担心纯属多余，如果是留有后门，那应该是继续更新继续加后门而不是停更。再说作者也没有被控制。

* 3.clash删库停更代理软件停更不影响你的节点使用，这个前面第一部分名词解释已经说了，你花的钱付费购买的不是clash。

* 4.只是clash for windows一直会停止更新。因为目前大部分作者只是避风头，已经归档的客户端后续应该还是会继续开发。clash meta是开源项目，不用担心没有人维护，其它ui客户端还是会继续更新，比如clash verge,

* 5.谨言慎行，不要在墙内传播科学上网相关的新闻，此次clash for windows删库上微博热门导致clash内核也跟着删库，最后导致整个clash社区都删库。就是因为有博主在微博讨论这事，为了流量，啥都发。而且墙内媒体讨论会暴露你翻墙的事实，有可能引起网警注意到你。

### 机场推荐

**可付费购买可稳定使用的机场，可参考我的另一篇总结，**🔥[*自用机场记录*](https://www.openwayz.com/jichang/) 

都是个人实际体验用过的6 7家服务商，包含专线及大带宽中转机场，价格从10￥到20￥，包月套餐及不限时流量套餐都有，可提供很好的使用体验。

