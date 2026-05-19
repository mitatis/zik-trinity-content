# ZIK Trinity Content

这是 `ZIK Trinity` 的独立内容仓库。网站代码仓库只负责 Astro 模板、样式、组件和构建流程；本仓库只负责 Markdown 内容与 Obsidian 内容管理配置。

## 目录约定

```text
blog/     # 博客文章，供网站的 blog 内容集合读取
poetry/   # 诗歌内容，供网站的 poetry 内容集合读取
```

网站仓库构建前会克隆本仓库到 `.content/`，再同步到 `src/content/blog` 与 `src/content/poetry`，让 Astro 内容集合正常生成静态页面。

## Frontmatter

当前网站没有为内容集合设置严格 schema，页面会读取以下常用字段：

```yaml
---
title: 标题
description: 摘要
pubDate: 2026-05-19
updatedDate: 2026-05-19
heroImage: /path/to/image.jpg
image: /path/to/card-image.jpg
readingTime: 3 min read
tags:
  - 标签
draft: false
---
```

新增内容时请尽量补齐 `title`、`description`、`pubDate` 和 `tags`。需要暂不发布的内容可设置 `draft: true`。
