---
layout: categories
title: Categories文章分类目录
description: 本站文章分类页面，包含了所有标签的分类目录，在这里，可以对本站所有的文章类别一览无遗，更快的找到您需要的部分内容，是本站最核心的页面，包含机场推荐，机场知识，经验分享，海外银行卡，加密货币出入金等相关信息，通过点击目录，可以快速找到相关的内容
keywords: 分类
comments: false
menu: 分类
permalink: /categories/
---

<section class="container posts-content">
{% assign sorted_categories = site.categories | sort %}
{% for category in sorted_categories %}
<h3 id="{{ category[0] }}">{{ category | first }}</h3>
<ol class="posts-list">
{% for post in category.last %}
<li class="posts-list-item">
<span class="posts-list-meta">{{ post.date | date:"%Y-%m-%d" }}</span>
<a class="posts-list-name" href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
</li>
{% endfor %}
</ol>
{% endfor %}
</section>
<!-- /section.content -->
