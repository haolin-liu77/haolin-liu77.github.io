---
layout: single
title: "博客"
permalink: /blog/
author_profile: true
---

按主题分类整理的文章。文件目录与 URL 路径对应，详见下方说明。

{% include base_path %}

## 学习笔记

### 机器学习

<ul>
{% assign found = false %}
{% for post in site.posts %}
  {% if post.categories[0] == "学习笔记" and post.categories[1] == "机器学习" %}
    {% assign found = true %}
    <li>{% include archive-single.html %}</li>
  {% endif %}
{% endfor %}
{% unless found %}<li><em>暂无文章</em></li>{% endunless %}
</ul>

### 课程

<ul>
{% assign found = false %}
{% for post in site.posts %}
  {% if post.categories[0] == "学习笔记" and post.categories[1] == "课程" %}
    {% assign found = true %}
    <li>{% include archive-single.html %}</li>
  {% endif %}
{% endfor %}
{% unless found %}<li><em>暂无文章</em></li>{% endunless %}
</ul>

### 计算机基础

<ul>
{% assign found = false %}
{% for post in site.posts %}
  {% if post.categories[0] == "学习笔记" and post.categories[1] == "计算机基础" %}
    {% assign found = true %}
    <li>{% include archive-single.html %}</li>
  {% endif %}
{% endfor %}
{% unless found %}<li><em>暂无文章</em></li>{% endunless %}
</ul>

## 项目记录

<ul>
{% assign found = false %}
{% for post in site.posts %}
  {% if post.categories[0] == "项目记录" %}
    {% assign found = true %}
    <li>{% include archive-single.html %}</li>
  {% endif %}
{% endfor %}
{% unless found %}<li><em>暂无文章</em></li>{% endunless %}
</ul>

## 随笔

<ul>
{% assign found = false %}
{% for post in site.posts %}
  {% if post.categories[0] == "随笔" %}
    {% assign found = true %}
    <li>{% include archive-single.html %}</li>
  {% endif %}
{% endfor %}
{% unless found %}<li><em>暂无文章</em></li>{% endunless %}
</ul>

---

## 怎么写一篇新文章

1. 在 `_posts/` 下对应文件夹新建 Markdown 文件，命名格式：`YYYY-MM-DD-标题.md`
2. 复制 `_drafts/post-draft.md` 里的模板，填好 `categories` 和 `permalink`
3. 用 `##` / `###` 标题写文章，右侧会自动生成**本页目录**

### 文件夹对照表

| 文件路径 | categories | URL 前缀 |
|----------|------------|----------|
| `_posts/notes/ml/` | `[学习笔记, 机器学习]` | `/blog/notes/ml/` |
| `_posts/notes/course/` | `[学习笔记, 课程]` | `/blog/notes/course/` |
| `_posts/notes/cs/` | `[学习笔记, 计算机基础]` | `/blog/notes/cs/` |
| `_posts/projects/` | `[项目记录, 子分类名]` | `/blog/projects/` |
| `_posts/misc/` | `[随笔]` | `/blog/misc/` |

新增大类时：新建文件夹 → 在本页加一节 → `categories` 第一级与目录名对应即可。
