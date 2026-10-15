---
layout: default
title: Home
---

# Horizon

<div id="lang-zh" class="lang-section" markdown="1">

欢迎来到 [Horizon](https://github.com/thysrael/Horizon)，一个 AI 驱动的信息聚合系统。

## 文档

- [配置指南](configuration) — AI 提供商、信息源、过滤规则与环境变量替换
- [信息源采集器](scrapers) — Horizon 如何从 GitHub、Hacker News、RSS、Reddit 采集内容
- [评分系统](scoring) — 基于 AI 的内容分析与 0-10 评分体系

## 每日速递 <a class="rss-icon" href="{{ '/feed-zh.xml' | relative_url }}" aria-label="订阅中文"><svg viewBox="0 0 448 512" xmlns="http://www.w3.org/2000/svg"><path fill="currentColor" d="M128.081 415.959c0 35.369-28.672 64.041-64.041 64.041S0 451.328 0 415.959s28.672-64.041 64.041-64.041 64.04 28.673 64.04 64.041zm175.66 47.25c-8.354-154.6-132.185-278.587-286.95-286.95C7.656 175.765 0 183.105 0 192.253v48.069c0 8.415 6.49 15.472 14.887 16.018 111.832 7.284 201.473 96.702 208.772 208.772.547 8.397 7.604 14.887 16.018 16.018h48.069c9.149.001 16.489-7.655 15.995-16.79zm144.249.288C439.596 229.677 251.465 40.445 16.503 32.01 7.473 31.686 0 38.981 0 48.016v48.068c0 8.625 6.835 15.645 15.453 15.999 191.179 7.839 344.627 161.316 352.465 352.465.353 8.618 7.373 15.453 15.999 15.453h48.068c9.034-.001 16.329-7.474 16.005-16.504z"/></svg></a>

<ul>
  {% assign daily_pages = site.pages | where: "dir", "/daily/" | where_exp: "p", "p.name != 'index.md'" | sort: "date" | reverse %}
  {% assign zh_posts = site.posts | where: "lang", "zh" %}
  {% capture covered_dates_str %}{% for p in daily_pages %}{{ p.date | date: "%Y-%m-%d" }},{% endfor %}{% endcapture %}
  {% assign covered_dates = covered_dates_str | split: "," %}
  {% assign shown = 0 %}
  {% for p in daily_pages %}
    {% if shown >= 5 %}{% break %}{% endif %}
    <li>
      <a href="{{ p.url | relative_url }}">{{ p.date | date: "%Y-%m-%d" }}</a>
    </li>
    {% assign shown = shown | plus: 1 %}
  {% else %}
    <li><em>暂无内容</em></li>
  {% endfor %}
  {% for post in zh_posts %}
    {% assign pd = post.date | date: "%Y-%m-%d" %}
    {% unless covered_dates contains pd or shown >= 5 %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ pd }}</a>
      </li>
      {% assign shown = shown | plus: 1 %}
    {% endunless %}
  {% endfor %}
</ul>

<a href="{{ '/daily/' | relative_url }}">整合版日报存档 →</a>

## AI Builders Digest

追踪 AI 领域真正在做事的人（builders）的中英双语每日简报：

<ul>
  {% assign ai_pages = site.pages | where: "dir", "/ai-builders/" | where_exp: "p", "p.name != 'index.md'" | sort: "date" | reverse %}
  {% for p in ai_pages limit:5 %}
    <li>
      <a href="{{ p.url | relative_url }}">{{ p.date | date: "%Y-%m-%d" }}</a>
    </li>
  {% else %}
    <li><em>暂无内容</em></li>
  {% endfor %}
</ul>

<a href="{{ '/ai-builders/' | relative_url }}">查看全部 →</a>

</div>

<div id="lang-en" class="lang-section" markdown="1">

Welcome to [Horizon](https://github.com/thysrael/Horizon), an AI-driven information aggregation system.

## Documentation

- [Configuration Guide](configuration) — AI providers, information sources, filtering, and environment variable substitution
- [Source Scrapers](scrapers) — How Horizon collects content from GitHub, Hacker News, RSS, and Reddit
- [Scoring System](scoring) — AI-based content analysis and the 0-10 scoring scale

## Daily Digest <a class="rss-icon" href="{{ '/feed-en.xml' | relative_url }}" aria-label="Subscribe English"><svg viewBox="0 0 448 512" xmlns="http://www.w3.org/2000/svg"><path fill="currentColor" d="M128.081 415.959c0 35.369-28.672 64.041-64.041 64.041S0 451.328 0 415.959s28.672-64.041 64.041-64.041 64.04 28.673 64.04 64.041zm175.66 47.25c-8.354-154.6-132.185-278.587-286.95-286.95C7.656 175.765 0 183.105 0 192.253v48.069c0 8.415 6.49 15.472 14.887 16.018 111.832 7.284 201.473 96.702 208.772 208.772.547 8.397 7.604 14.887 16.018 16.018h48.069c9.149.001 16.489-7.655 15.995-16.79zm144.249.288C439.596 229.677 251.465 40.445 16.503 32.01 7.473 31.686 0 38.981 0 48.016v48.068c0 8.625 6.835 15.645 15.453 15.999 191.179 7.839 344.627 161.316 352.465 352.465.353 8.618 7.373 15.453 15.999 15.453h48.068c9.034-.001 16.329-7.474 16.005-16.504z"/></svg></a>

<ul>
  {% assign daily_pages_en = site.pages | where: "dir", "/daily/" | where_exp: "p", "p.name != 'index.md'" | sort: "date" | reverse %}
  {% assign en_posts = site.posts | where: "lang", "en" %}
  {% capture covered_dates_str_en %}{% for p in daily_pages_en %}{{ p.date | date: "%Y-%m-%d" }},{% endfor %}{% endcapture %}
  {% assign covered_dates_en = covered_dates_str_en | split: "," %}
  {% assign shown_en = 0 %}
  {% for p in daily_pages_en %}
    {% if shown_en >= 5 %}{% break %}{% endif %}
    <li>
      <a href="{{ p.url | relative_url }}">{{ p.date | date: "%Y-%m-%d" }}</a>
    </li>
    {% assign shown_en = shown_en | plus: 1 %}
  {% else %}
    <li><em>No reports yet</em></li>
  {% endfor %}
  {% for post in en_posts %}
    {% assign pd = post.date | date: "%Y-%m-%d" %}
    {% unless covered_dates_en contains pd or shown_en >= 5 %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ pd }}</a>
      </li>
      {% assign shown_en = shown_en | plus: 1 %}
    {% endunless %}
  {% endfor %}
</ul>

<a href="{{ '/daily/' | relative_url }}">Curated report archive →</a>

## AI Builders Digest

A bilingual daily digest tracking the people who actually build AI:

<ul>
  {% assign ai_pages_en = site.pages | where: "dir", "/ai-builders/" | where_exp: "p", "p.name != 'index.md'" | sort: "date" | reverse %}
  {% for p in ai_pages_en limit:5 %}
    <li>
      <a href="{{ p.url | relative_url }}">{{ p.date | date: "%Y-%m-%d" }}</a>
    </li>
  {% else %}
    <li><em>No digests yet</em></li>
  {% endfor %}
</ul>

<a href="{{ '/ai-builders/' | relative_url }}">View all →</a>

</div>
