# cwl02716.github.io

個人部落格原始碼，使用 [Hugo](https://gohugo.io/)（extended）+ [Stack](https://github.com/CaiJimmy/hugo-theme-stack) 主題（以 Hugo Module 引入）。
推送到 `master` 後，GitHub Actions 會自動建置並部署到 GitHub Pages。

## 結構

```
content/
  post/     技術文章、面試心得（每篇一個資料夾，圖片和 index.md 放一起）
  notes/    學習筆記
  page/     關於、封存、搜尋頁
  categories/  分類的顏色與說明
config/_default/  網站設定（標題、側邊欄、選單等）
assets/img/avatar.png  頭像
```

## 常用指令

```bash
hugo new content post/my-post/index.md     # 新文章
hugo new content notes/my-note/index.md    # 新筆記
hugo server -D                             # 本機預覽（含草稿） http://localhost:1313
hugo mod get -u                            # 更新主題
```

新文章預設是 `draft: true`，要發布時改成 `false` 再 push。

## 寫作慣例（方便日後換框架）

- front matter 用 YAML（`---`），只用 `title / description / slug / date / categories / tags / image` 等通用欄位
- 盡量用標準 Markdown，少用 Hugo shortcode
- 分類：`技術文章`、`學習筆記`、`面試心得`

## 開啟留言（選用）

1. 在此 repo 開啟 Discussions，安裝 [giscus app](https://github.com/apps/giscus)
2. 到 https://giscus.app 產生設定
3. 在 `config/_default/params.yaml` 的 `comments` 下設 `enabled: true` 並加入 `giscus:` 設定
