---
title: 部落格開張
description: 從 Hexo 搬到 Hugo + Stack，紀錄一下這個網站怎麼運作
slug: hello-world
date: 2026-09-28
categories: [技術文章]
tags: [Hugo, GitHub Pages]
---

這是新網站的第一篇文章。以後會在這裡寫技術文章、學習筆記和面試心得。

## 這個網站怎麼運作

- 用 [Hugo](https://gohugo.io/) 產生靜態網頁，主題是 [Stack](https://github.com/CaiJimmy/hugo-theme-stack)。
- 原始碼放在 GitHub，每次推送後 GitHub Actions 會自動建置、部署到 GitHub Pages。

## 寫一篇新文章

```bash
hugo new content post/my-first-post/index.md
```

寫完後把 front matter 裡的 `draft: true` 改成 `false`（或刪掉這行），commit 並 push 就會上線。

本機預覽：

```bash
hugo server -D
```
