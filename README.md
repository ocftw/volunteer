# OCF Volunteer 志工團隊

> 投入志工行列、豐富開源生態！ — Join us as a volunteer and enrich the open-source ecosystem!

本儲存庫是 **[財團法人開放文化基金會 (Open Culture Foundation, OCF)](https://ocf.tw/)
志工團隊網站**的原始碼。網站使用 [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
建置，內容位於 [`zh-TW/`](zh-TW/) 目錄，並發布於：

This repository contains the source of the **OCF Volunteer team website**, built with
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/). Content lives under
[`zh-TW/`](zh-TW/) and is published at:

**🌐 <https://volunteer.ocf.tw/>**

---

## 中文

### 這個專案是什麼？

OCF 志工團隊網站提供志工申請與登錄、數位時數證明驗證說明，以及近期招募與活動公告。歡迎參與我們在
開放原始碼、開放資料、開放政府、網路自由與數位人權等領域的推廣與倡議。

### 在本機開發

本專案使用 [`uv`](https://docs.astral.sh/uv/) 管理 Python 環境與相依套件，需要 Python 3.12 以上。

```bash
# 安裝相依套件
uv sync

# 啟動本機預覽伺服器（http://127.0.0.1:8000/）
uv run mkdocs serve

# 建置靜態網站到 site/
uv run mkdocs build
```

> `mkdocs.yml` 的 `docs_dir` 預設為 `zh-TW`（透過 `DOCS_DIR` 環境變數可覆寫），因此上述指令會
> 直接使用 `zh-TW/` 內的內容。

### 專案結構

```
.
├── zh-TW/              # 網站內容（Markdown 頁面、部落格文章、圖片）
│   ├── index.md        # 首頁
│   ├── apply.md        # 志工申請與登錄
│   ├── verify.md       # 志工數位證明
│   ├── blog/           # 公告／部落格（posts/ 內為文章）
│   └── assets/         # 圖片等靜態資源
├── overrides/          # Material 主題的自訂 partial
├── mkdocs.yml          # MkDocs 設定
└── pyproject.toml      # 專案與相依套件設定（uv）
```

### 新增內容

- **新增一般頁面**：在 `zh-TW/` 新增 `.md` 檔，並視需要加入 `mkdocs.yml` 的 `nav`。
- **新增公告／部落格文章**：在 `zh-TW/blog/posts/` 新增 `.md` 檔。
  詳細的 front-matter 格式與慣例請見 [CONTRIBUTING.md](CONTRIBUTING.md)。

### 部署

合併到 `main` 分支後，會由 GitHub Actions 自動建置並部署到 GitHub Pages
（網域 `volunteer.ocf.tw`）。Pull Request 則只會執行建置驗證。

---

## English

### What is this?

The OCF Volunteer site explains how to apply and register as a volunteer, how the digital
service-hour certificates are signed and verified, and posts recruitment / event announcements.
We welcome participation in open source, open data, open government, internet freedom, and
digital rights advocacy.

### Local development

This project uses [`uv`](https://docs.astral.sh/uv/) to manage the Python environment and
dependencies. Python 3.12+ is required.

```bash
uv sync                  # install dependencies
uv run mkdocs serve      # live preview at http://127.0.0.1:8000/
uv run mkdocs build      # build the static site into site/
```

> `docs_dir` defaults to `zh-TW` in `mkdocs.yml` (overridable via the `DOCS_DIR` env var), so the
> commands above operate on the content in `zh-TW/`.

### Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to add a page or a blog post and for local
preview steps. Please also read our [Code of Conduct](CODE_OF_CONDUCT.md).

### Deployment

Merges to `main` are automatically built and deployed to GitHub Pages (custom domain
`volunteer.ocf.tw`) via GitHub Actions. Pull requests run a build-only validation.

---

## License / 授權

This repository is dual-licensed / 本儲存庫採雙重授權：

- **Code & configuration** (`mkdocs.yml`, theme overrides, stylesheets, CI workflows) —
  [MIT License](LICENSE).
  **程式碼與設定** — [MIT 授權](LICENSE)。
- **Documentation content** under `zh-TW/` —
  [Creative Commons Attribution 4.0 (CC BY 4.0)](LICENSE-CONTENT.md).
  **`zh-TW/` 文件內容** — [創用 CC 姓名標示 4.0（CC BY 4.0）](LICENSE-CONTENT.md)。

## Contact / 聯絡

Email: [volunteer@ocf.tw](mailto:volunteer@ocf.tw) · Web: <https://ocf.tw/>
