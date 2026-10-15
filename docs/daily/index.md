---
layout: default
title: 每日日报
---

# 每日日报

<div id="lang-zh" class="lang-section" markdown="1">

晨间自动化整理的每日要闻与深读（Horizon 新闻雷达），中英双语：

## 往期日报

<ul>
  {% assign daily_pages = site.pages | where: "dir", "/daily/" | where_exp: "p", "p.name != 'index.md'" | sort: "date" | reverse %}
  {% for p in daily_pages limit:100 %}
    <li>
      <a href="{{ p.url | relative_url }}">{{ p.date | date: "%Y-%m-%d" }}</a>
    </li>
  {% else %}
    <li><em>暂无内容</em></li>
  {% endfor %}
</ul>

</div>

<div id="lang-en" class="lang-section" markdown="1">

An automated morning digest of top stories and deep dives (Horizon News Radar), in Chinese and English:

## Past Reports

<ul>
  {% assign daily_pages_en = site.pages | where: "dir", "/daily/" | where_exp: "p", "p.name != 'index.md'" | sort: "date" | reverse %}
  {% for p in daily_pages_en limit:100 %}
    <li>
      <a href="{{ p.url | relative_url }}">{{ p.date | date: "%Y-%m-%d" }}</a>
    </li>
  {% else %}
    <li><em>No reports yet</em></li>
  {% endfor %}
</ul>

</div>

<a href="{{ '/' | relative_url }}">← 返回 Horizon 首页 / Back to Horizon Home</a>
