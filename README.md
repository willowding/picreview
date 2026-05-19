# PicReview — 多人在线图片审核系统
# PicReview — Collaborative Image Review System

**在线地址 / Live URL：** https://willowding.github.io/picreview/

---

## 简介 / About

PicReview 是一个面向小团队的在线图片审核工具，支持多人实时协作，适用于 AI 生成图片的人工审核流程。  
PicReview is an online image review tool for small teams, supporting real-time multi-user collaboration, designed for human review of AI-generated images.

---

## 功能 / Features

### 通用 / General
- 多人实时同步，任意用户的操作立即对所有人可见  
  Real-time sync — any action is instantly visible to all users
- 按文件名降序排列图片  
  Images sorted by filename in descending order
- 弹窗左右导航，支持键盘方向键  
  Modal navigation with left/right arrows and keyboard shortcuts
- 重复检测：相同内容自动跳过，同名图片自动替换  
  Duplicate detection: same content (hash) is skipped; same filename is replaced

### 文件夹 / Folders
- 按项目建立文件夹，支持搜索框实时过滤  
  Organize images into project folders with real-time search
- 文件夹名含 L1–L6 自动显示彩色级别标签（红/橙/黄/绿/蓝/紫）  
  Folders containing L1–L6 in their name automatically display a color-coded level tag
- 级别按钮一键筛选，可与搜索框叠加使用  
  Level filter buttons (L1–L6) can be combined with text search
- 打开绘本弹窗时显示对应关键词与造句  
  Modal shows the matching keyword and sentence from the content sheet
- 英语绘本文件夹内图片自动按 Level（L1→L6）→ 书名（A-Z）→ 分镜编号升序排列  
  Inside the 英语绘本 folder, images are auto-sorted by level (L1→L6), then book title (A–Z), then scene number ascending
- 文件名规范：`L1_《Look, Look, Colors!》_分镜1`  
  Filename convention: `L1_《Look, Look, Colors!》_分镜1`
- 打开任意文件夹后显示文件名搜索框；英语绘本文件夹内额外显示 L1–L6 快速筛选按钮  
  A filename search bar appears inside any folder; L1–L6 filter buttons appear only inside 英语绘本

### 上传方 / Uploader
- 拖拽或点击批量上传图片（JPG / PNG / WEBP）  
  Drag-and-drop or click to batch upload images (JPG / PNG / WEBP)
- 多选、批量下载（ZIP）、批量删除  
  Multi-select, batch download as ZIP, batch delete
- 对已打回的图片可直接在弹窗内上传替换图  
  Replace rejected images directly from the modal

### 审核员 / Reviewer
- 对图片标注「通过」或「打回」，并附评论  
  Approve or reject images with comments
- 可选标签：有描边 / 豆豆眼 / 风格问题 / 形象或场景问题 / 色彩或文字问题  
  Predefined tags: outlined style / dot eyes / style issue / character or scene issue / color or text issue
- 标注「我来改！」认领打回图片；其他审核员可「抢夺认领」  
  Claim a rejected image with "我来改！"; other reviewers can take over the claim
- 已认领状态单独筛选，与「已打回」区分显示  
  Claimed images have their own filter tab, separate from plain rejected images

---

## 审核标准 / Review Criteria

1. 图案圆润，无尖锐形状 / Rounded shapes, no sharp edges
2. 形象可爱，无恐怖表情 / Cute characters, no scary expressions
3. 动物符合真实形态 / Animals anatomically accurate
4. 场景与道具符合现实逻辑 / Scenes and props follow real-world logic
5. 颜色柔和，不刺眼 / Soft, non-jarring colors
6. 文字清晰，大小适当 / Clear and appropriately sized text
7. 无敏感元素，无侵权风险 / No sensitive content, no copyright risk
8. 整套风格统一 / Consistent style throughout the set
9. 适合 3–6 岁儿童认知 / Appropriate for children aged 3–6
10. 场景和角色均无描边 / No outlines on scenes or characters
11. 角色需有眼白，不得为豆豆眼 / Characters must have visible eye whites, no dot eyes

---

## 技术架构 / Tech Stack

| 层级 | 技术 |
|------|------|
| 前端 / Frontend | 纯 HTML + CSS + JavaScript（无框架）|
| 数据库 / Database | Supabase（PostgreSQL + Realtime）|
| 图片存储 / Image Storage | Cloudinary（缩略图自动压缩）|
| 部署 / Hosting | GitHub Pages |

---

## 使用说明 / How to Use

1. 打开在线地址，输入姓名，选择「上传」或「审核」角色  
   Open the URL, enter your name, choose Uploader or Reviewer role
2. 点击文件夹进入，或使用搜索框 / 级别按钮快速定位  
   Click a folder, or use the search bar / level buttons to find it quickly
3. 上传方拖拽图片上传；审核员点开图片进行审核  
   Uploaders drag images to upload; reviewers click images to review
4. 审核员点「打回」需选择标签或填写原因  
   Reviewers must select a tag or enter a reason when rejecting
5. 打回的图片可由审核员认领（「我来改！」），上传方看到后上传替换图  
   Rejected images can be claimed by a reviewer; the uploader then replaces them

## 致谢 / Acknowledgement

这是我第一次从零完成一个完整的程序，感谢 Claude 耐心陪跑。

This is my first complete program built from scratch. Thanks to Claude for the patient guidance throughout.
