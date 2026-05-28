# Security Policy / 安全政策

本儲存庫是一個以 [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) 建置的
**靜態文件網站**，發布於 <https://volunteer.ocf.tw/>。這裡沒有後端服務或資料庫，因此回報範圍
主要為網站內容、建置流程與相依套件相關的問題。

This repository is a **static documentation site** built with
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) and published at
<https://volunteer.ocf.tw/>. There is no backend service or database, so reports mainly concern the
site content, the build pipeline, and dependencies.

## 回報方式 / Reporting

請勿在公開的 Issue 中揭露安全性問題。請改以下列方式私下通報：

Please do not disclose security issues in public Issues. Report them privately instead:

- Email：[volunteer@ocf.tw](mailto:volunteer@ocf.tw)
- 或使用 GitHub 的 [私密漏洞回報 (Private vulnerability reporting)](https://github.com/ocftw/volunteer/security/advisories/new) 功能。
  You may also use GitHub's [private vulnerability reporting](https://github.com/ocftw/volunteer/security/advisories/new).

我們會盡快回覆並與您協調修復與揭露時程。

We will respond as soon as possible and coordinate a fix and disclosure timeline with you.

## 範圍 / Scope

- 受支援的版本：`main` 分支（即線上網站當前內容）。
  Supported version: the `main` branch (the content currently live on the site).
- `zh-TW/verify.md` 內的 PGP 公鑰為**刻意公開**的簽署金鑰，用於驗證志工數位時數證明，並非洩漏的密鑰。
  The PGP public key in `zh-TW/verify.md` is an **intentionally public** signing key used to verify
  volunteer service-hour certificates; it is not a leaked secret.
