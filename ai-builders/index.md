---
layout: default
title: AI Builders Digest
---

# AI Builders Digest

追踪 AI 领域真正在做事的人（builders，而非搬运 influencers）：每天从 X/Twitter 上的 builder 动态、官方博客与播客中提炼的中英双语简报。每日北京时间约 15:10 自动更新。

## 往期简报

<ul>
  {% assign ai_pages = site.pages | where: "dir", "/ai-builders/" | where_exp: "p", "p.name != 'index.md'" | sort: "date" | reverse %}
  {% for p in ai_pages limit:100 %}
    <li>
      <a href="{{ p.url | relative_url }}">{{ p.date | date: "%Y-%m-%d" }} — {{ p.title }}</a>
    </li>
  {% else %}
    <li><em>暂无内容 / No digests yet</em></li>
  {% endfor %}
</ul>

<a href="{{ '/' | relative_url }}">← 返回 Horizon 首页</a>
