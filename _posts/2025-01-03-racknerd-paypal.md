---
layout: post
title: Racknerd如何用Paypal支付
categories: VPS
description: Racknerd突然不能用Paypal支付了,以前我都是用Paypal支付，突然今天的续费账单不能用了，查找了些资料，也咨询了客服，最终成功支付了，把解决方法整理出来供大家参考，Racknerd用的是第三方支付渠道FastSpring，这应该是FastSpring增加了相关的风控检测手段所以才导致的这个问题
keywords: Racknerd
mermaid: false
sequence: false
flow: false
mathjax: false
mindmap: false
mindmap2: false
topmost: false
permalink: /:title/
---

昨天在Racknerd续费机器突然不能用Paypal支付了,以前都是用Paypal支付，突然今天的续费账单不能用了，查找了些资料，也咨询了客服，客服反馈这是第三方支付上的风控行为，他们无法干预，折腾了两个小时，最终成功支付了，把解决方法整理出来供大家参考，Racknerd用的是第三方支付渠道FastSpring，这应该是FastSpring增加了相关的风控检测手段所以才导致的这个问题。

### 问题现象

支付订单时支付方式选择了Paypal,但是跳转进去后弹出如下提示，“订单无法被接受”试用多次后即使不开代理直连都是一样的问题，网上论坛查了下一些网友的经验，大部分人反馈国区paypal已经不能使用了，可我的这个是美区Paypal,后来看到一个网友给的经验说是修改Racknerd个人资料把地址改成美国的就可以，尝试后确实有效，但是有个问题，随便改成美国地址后支付会收税，我15$的机器收8%，还是挺高的，想必应该是美国有些洲就是收税的，于是找了找美国的免税州地址，我用的是美国俄勒冈州，使用了地址生成器，[https://www.meiguodizhi.com/usa-address/oregon](https://www.meiguodizhi.com/usa-address/oregon)，更改个人资料后重新下单，订单已经没有税了，成功支付。  

![Racknerd Paypal](/images/posts/racknerd/racknerd-paypal.png)

### Racknerd介绍

Racknerd是一个主要经营美国VPS和独立服务器的商家，有中国团队参与运营，在美国众多的商家之中，他算是很便宜的商家，2015年成立，刚开始的时候，用户都担心是灵车，说不定什么时候就跑路了，但经营几年下来，稳定性可用性都不错，口碑日渐提升，产品性价比很高，数据中心包含洛杉矶，圣何塞，西雅图，新泽西，纽约，达拉斯，芝加哥，阿什本，亚特兰大，荷兰，部分热门地区机器存在超售，不过胜在价格便宜，每年的黑五，新年都会推出很多闪购，年付活动。目前最新的活动是2024年黑五和2025年新年，这些机器基本上在2025年全年都可购买。

### 2024年黑五套餐

| 处理器CPU | 内存RAM | SSD硬盘容量 | 流量/月 | 价格/年 | 购买链接 |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 1核 | 1GB | 20GB | 1.5T | 10.99美元 | [racknerd购买](https://my.racknerd.com/aff.php?aff=9815&pid=879) |
| 2核 | 2.5GB | 40GB | 3 | 18.93美元 | [racknerd购买](https://my.racknerd.com/aff.php?aff=9815&pid=880) |
| 2核 | 3.5GB | 650B | 5.5T | 27.89美元 | [racknerd购买](https://my.racknerd.com/aff.php?aff=9815&pid=881) |
| 3核 | 4.5GB | 100GB | 8.5T | 39.88美元 | [racknerd购买](https://my.racknerd.com/aff.php?aff=9815&pid=882) |
| 4核 | 5GB | 130GB | 12T | 55.93美元 | [racknerd购买](https://my.racknerd.com/aff.php?aff=9815&pid=883) |

### 2025年New Year套餐

| 处理器CPU | 内存RAM | SSD硬盘容量 | 流量/月 | 价格/年 | 购买链接 |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 1核 | 1GB | 24GB | 2T | 11.29美元 | [racknerd购买](https://my.racknerd.com/aff.php?aff=9815&pid=903) |
| 1核 | 2GB | 40GB | 3.5 | 18.29美元 | [racknerd购买](https://my.racknerd.com/aff.php?aff=9815&pid=904) |
| 2核 | 3.5GB | 65GB | 7T | 32.49美元 | [racknerd购买](https://my.racknerd.com/aff.php?aff=9815&pid=905) |
| 3核 | 4GB | 105GB | 9T | 43.88美元 | [racknerd购买](https://my.racknerd.com/aff.php?aff=9815&pid=906) |
| 4核 | 6GB | 140GB | 12T | 59.99美元 | [racknerd购买](https://my.racknerd.com/aff.php?aff=9815&pid=907) |

  






