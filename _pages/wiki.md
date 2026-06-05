---
layout: single
title: "Wiki"
permalink: /wiki/
author_profile: true
---

个人知识库，按编号目录组织。点击进入各章，再进入子目录阅读具体条目。

{% include base_path %}

| 目录 | 说明 |
|------|------|
| [00 导论](/wiki/00-导论/) | 总览与说明 |
| [01 数学](/wiki/01-数学/) | 数学基础 |
| [02 感知](/wiki/02-感知/) | 感知相关 |
| [03 运动控制](/wiki/03-运动控制/) | 运动控制（含机械臂、仿真等） |

### 03 运动控制 · 子目录

{% include wiki-subsections.html section="03-运动控制" %}

---

## 如何新增条目

1. 在 `_wiki/` 对应文件夹下新建 `.md` 文件（无需日期前缀）
2. 复制 `_drafts/wiki-draft.md` 作为模板
3. 子目录新建：建文件夹 + 放一个 `index.md` 作为目录页

```
_wiki/
├── 00-导论/
├── 01-数学/
├── 02-感知/
└── 03-运动控制/
    ├── index.md
    ├── 机械臂/
    │   ├── index.md
    │   └── 某篇文章.md
    └── 仿真/
        └── index.md
```
