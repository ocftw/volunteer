# Contributing / 貢獻指南

感謝您願意協助改善 OCF 志工團隊網站！本文件說明如何在本機預覽、新增內容，以及送出貢獻。

Thanks for helping improve the OCF Volunteer site! This guide covers local preview, adding
content, and submitting changes.

請先閱讀我們的 [行為準則 (Code of Conduct)](CODE_OF_CONDUCT.md)。
Please also read our [Code of Conduct](CODE_OF_CONDUCT.md) first.

---

## 開始之前 / Getting started

本專案使用 [`uv`](https://docs.astral.sh/uv/)（Python 3.12+）。
This project uses [`uv`](https://docs.astral.sh/uv/) (Python 3.12+).

```bash
uv sync                  # 安裝相依套件 / install dependencies
uv run mkdocs serve      # 本機預覽 / live preview at http://127.0.0.1:8000/
uv run mkdocs build      # 建置 / build into site/
```

內容位於 `zh-TW/` 目錄。修改後請以 `mkdocs serve` 在瀏覽器確認排版與連結正常。
Content lives under `zh-TW/`. After editing, verify rendering and links in the browser via
`mkdocs serve`.

## 如何貢獻 / How to contribute

1. Fork 並建立分支（feature branch）。Fork the repo and create a feature branch.
2. 進行修改並於本機預覽確認。Make your changes and preview locally.
3. 送出 Pull Request，於描述中說明變更內容與動機。Open a Pull Request describing what and why.

小幅的錯字／連結修正可直接送 PR；較大的內容調整建議先開 Issue 討論。
Small typo/link fixes can go straight to a PR; for larger content changes, please open an Issue
to discuss first.

> 本專案的提交慣例採用 **Signed-off-by**（`git commit -s`）。
> Commits in this project use **Signed-off-by** (`git commit -s`).

## 新增一般頁面 / Adding a page

1. 在 `zh-TW/` 新增 `.md` 檔，檔案開頭加入 front-matter（`title`、`icon` 等）。
2. 若希望出現在主導覽列，於 `mkdocs.yml` 的 `nav` 加入該頁。

Create a `.md` file under `zh-TW/` with front-matter (`title`, `icon`, …). To show it in the main
navigation, add it to `nav` in `mkdocs.yml`.

## 新增公告／部落格文章 / Adding a blog post

在 `zh-TW/blog/posts/` 新增 `.md` 檔，依下列格式撰寫 front-matter（參考既有文章
`zh-TW/blog/posts/recruitment-202506.md`）：

Create a `.md` file under `zh-TW/blog/posts/` using the front-matter below (see the existing
`zh-TW/blog/posts/recruitment-202506.md`):

```markdown
---
date: 2025-06-04
authors:
    - ocf-volunteer
categories:
    - 任務
slug: my-post-slug
image: "assets/images/my-cover.png"
summary: "一句話摘要 / one-line summary"
description: "用於 SEO 與分享的描述 / description for SEO and sharing"
---
# 文章標題 Post title

![封面 alt 文字](./assets/images/my-cover.png)

前言段落（會顯示在文章列表）。Intro paragraph (shown in the post list).

<!-- more -->

正文其餘內容。The rest of the post body.
```

重點 / Notes:

- `authors` 對應 `zh-TW/blog/.authors.yml` 中定義的作者鍵（如 `ocf-volunteer`）。若需新增作者，
  請先在該檔加入。
  `authors` must match a key defined in `zh-TW/blog/.authors.yml` (e.g. `ocf-volunteer`); add a new
  author there first if needed.
- `<!-- more -->` 標記文章摘要的分隔點，之前的內容會出現在文章列表。
  `<!-- more -->` marks the excerpt cut-off shown on the post list.
- `slug` 決定文章網址；`date` 決定發布時間與 RSS。
  `slug` sets the URL; `date` drives publish time and RSS.

## 圖片與資源 / Images & assets

- 一般頁面圖片：`zh-TW/assets/images/`
- 部落格文章圖片：`zh-TW/blog/posts/assets/images/`
- 請使用最佳化過的格式（如 `.webp`、`.png`、`.svg`），並避免過大的檔案。
  Use optimized formats (`.webp`, `.png`, `.svg`) and avoid oversized files.

## 授權 / Licensing of contributions

送出貢獻即表示您同意：程式碼／設定以 [MIT](LICENSE) 授權，`zh-TW/` 內的文件內容以
[CC BY 4.0](LICENSE-CONTENT.md) 授權。請僅提交您有權釋出的內容，第三方素材（如照片）須具備相容
授權並標示來源。

By contributing you agree that code/config is licensed under [MIT](LICENSE) and documentation
content under `zh-TW/` under [CC BY 4.0](LICENSE-CONTENT.md). Only submit material you have the
right to release; third-party assets (e.g. photos) must be compatibly licensed and properly
attributed.

## 有問題嗎？ / Questions?

歡迎開 Issue，或來信 [volunteer@ocf.tw](mailto:volunteer@ocf.tw)。
Open an Issue or email [volunteer@ocf.tw](mailto:volunteer@ocf.tw).
