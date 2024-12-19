---
layout: post
title: 网站突然在必应Bing无法被搜索到，索引全部没了
categories: 经验分享
description: 突然发现我的博客在Bing搜索引擎上的流量锐减，几乎跌到了零，使用bing搜索我的网站，提示搜多不到相关结果，疑似被拉黑了
keywords: Bing索引消失
mermaid: false
sequence: false
flow: false
mathjax: false
mindmap: false
mindmap2: false
topmost: false
permalink: /:title/
---
2024/12/13日突然发现我的博客在Bing搜索引擎上的流量锐减，几乎跌到了零，于是我使用bing搜索我的网站，发现没有任何文章能搜到，搜索site:www.openwayz.com提示没有与此相关的结果，似乎整个网站被bing拉黑除名了，但是在其他搜索引擎上的索引确实正常的，可以确定是单方面的可能是触发了bing的什么机制导致了这种问题。

![noindex](/images/posts/bing/noindex.png)

### 问题出在哪里呢

意识到肯定是哪里出问题了，但我的博客已经正常运行一年多了，之前一直都是正常的，最近我也没做什么更改，为什么突然这样了？很疑惑也很苦恼，毕竟一年多的心血，好不容易有点流量，如果网站就这么没了实在不甘心，于是我登陆Bing Webmaster tools后台查看是否有什么相关通知，遗憾的是没有任何通知，我只能去查看相关的报表已经URL检查。

### 查看点击量

从网站的搜索性能中能发现点击量和印象锐减至0。

![click](/images/posts/bing/click.png)

### 查看网址索引量

发现数据是正常的，以往发布的文章还是索引的状态，看下图绿色的横线，也就是说不是把我所有索引的URL取消了，索引的网址都还在。

![crawl](/images/posts/bing/crawl.png)

### 查看Recommendations

这里是Bing给网站的一些建议，我吃惊的发现这里有大量的错误，大多是跟SEO相关的,竟然有如此之多的错误，进一步去排查网站的代码，发现是因为我用的SEO插件冲突，产生了两份seo内容，无论是不是因为这个问题导致的，先行修复这个问题，然后进行实时URL检查，确认修复该问题。

![Recommendations](/images/posts/bing/Recommendations.png)

### 后续工作

问题修复后，我重新提交了网站的sitemap,期待网站能被重新爬取后检测到我修复了这个问题能给恢复索引，不过遗憾的是12/14号提交，至本文章编写时12/16号，提交的sitemap一直是待处理状态，似乎爬虫都不来了，很像网站已经被拉入了垃圾站黑名单，网上查了些信息，这种情况可能很难自行恢复了，于是我给bing发了请求工单邮件，不过看网上一些人的经验，这种邮件很大可能会石沉大海，没有回复，不过目前也没有其他办法，只能等待，后续我再更新一下进展，给后来人能有一个参考。




