---
layout: post
title: Vercel编译Github Page托管的Jekyll静态网站突然失败报错
categories: 经验分享
description: Vercel编译Github Page托管的Jekyll静态网站突然失败报错，It looks like you're trying to use Nokogiri as a precompiled native gem on a system with an unsupported version of glibc.
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

我的博客前几天突然无法发布新文章，本站是使用Jekyll + Github Pages搭建的静态网站，托管到Vercel，每次推送新文章都会自动进行编译，生成新的页面，已经正常工作快两年了，前几天突然写的新文章发现网站上没有发布，记录下排查过程，方便遇到类似问题的朋友能有个参考。

### 报错现象

登录Vercel查看项目编译情况，发现编译报错，报错内容如下图，“It looks like you're trying to use Nokogiri as a precompiled native gem on a system with an unsupported version of glibc.”从截图中看出现错误是因为Nokogiri这个组件引起的，可我的托管代码从来没做过任何改动，所以可以确定这个原因是因为vercel的编译环境升级引起的，从图片上面能看到Nokogiri的版本是1.18.0，于是我去查看了最后一次编译正常的版本，从中发现以前使用的Nokogiri版本是1.17.2，于是尝试编辑Github根目录的Gemfile文件，添加一行gem 'nokogiri', '~> 1.17.2'指定使用这个版本的nokogiri进行编译，代码提交后网站重新自动编译，成功通过。

![Vercel error](/images/posts/vercelerror/vercel-error.png)

### 一点感想

搞编程相关的工作就是这样，经常会遇到一些奇奇怪怪的问题，很多问题最后的解决方案可能就是一行代码或者改个数字，但是为了找到这个答案，可能需要敷出很大的精力去查原因，方法很重要，同时资料也很重要，分享这些小的精力，当其他朋友也遇到类似这种问题的时候希望能够通过搜到我的这种文档给大家提供一个思路，以便能更快的解决问题，这也便是这种记录的最大价值了。


  






