# PicReview

A lightweight image review tool for small teams who are tired of chasing feedback. Upload, approve, reject, and leave comments — all in one tab :)

**Live site:** https://willowding.github.io/picreview/

---

## Features

- **Project-based organization** — group images into projects (e.g. 造句图片, 英语单词卡片, 英语绘本 L1–L6)
- **Two roles** — switch between "上传" (upload / delete / replace) and "审核" (approve / reject / comment)
- **Four review states** — 待审核 / 已通过 / 已认领 / 已打回, with quick-filter tabs
- **Tag library** — one-click rejection tags: 有描边 / 风格问题 / 剧情问题 / 形象/场景问题 / 色彩/文字问题
- **Claim & rework** — designers can claim a rejected image and upload a replacement directly in the modal
- **Two views** — 🖼 card grid for quick browsing, 📊 table for status overview
- **Custom tables** — upload a CSV per project to map IDs → keywords → sentences; the table view renders from your data
- **Bulk actions** — multi-select to batch download or delete
- **Realtime sync** — all changes propagate instantly to anyone with the page open
- **Upload notifications** — automatic toast when a teammate uploads a batch
- **Smart matching** — English word card images auto-match by 4-digit ID prefix or keyword fallback
- **Copy IDs** — one click to copy all visible row IDs (space-separated) to clipboard

## Tech Stack

- **Frontend:** single-file `index.html` (HTML + CSS + vanilla JS, no build step)
- **Database & realtime:** [Supabase](https://supabase.com/) (PostgreSQL + realtime subscriptions)
- **Image storage:** [Cloudinary](https://cloudinary.com/)
- **Hosting:** GitHub Pages

## Repository Files

| File | Purpose |
|---|---|
| `index.html` | The entire application |
| `README.md` | This file |

## Deployment

The app is served directly from `main` branch root via GitHub Pages. Any change pushed to `index.html` goes live in 1–2 minutes after a hard refresh.

## Acknowledgements

This is my very first complete project from idea to deployment. Huge thanks to Claude :)
