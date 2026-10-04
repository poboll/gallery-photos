# 傍晚的月亮 — 照片存储仓

[gallery.caiths.com](https://gallery.caiths.com/) 的照片存储后端，供 [Afilmory](https://github.com/Afilmory/afilmory) 构建器以 GitHub 存储源方式读取。

> 本仓库为**公开仓库**：仓库内照片与 [gallery.caiths.com](https://gallery.caiths.com/) 一样对所有人可见。这是当前架构的设计前提，介意请勿上传未公开的照片。

## 目录结构

| 路径 | 说明 | 谁在写 |
|---|---|---|
| `photos/` | 照片原图（HEIC / JPEG / Live Photo 成对 HEIC+MOV） | 人（网页拖拽上传） |
| `thumbnails/` | 构建器自动生成的缩略图与转码副本 | 🤖 构建器（勿手改） |
| `photos-manifest.json` | 构建产物清单（照片元数据 + URL） | 🤖 构建器（勿手改） |

## 如何添加照片

1. 打开本仓库的 `photos` 文件夹 → **Add file → Upload files**
2. 拖入照片（iPhone 高效格式 HEIC 直接传；Live Photo 请把同名 `.HEIC` + `.MOV` 成对上传）
3. Commit —— 构建管线会自动：转码 HEIC、生成缩略图、更新 [gallery.caiths.com](https://gallery.caiths.com/)

## 隐私与边界

- 公开仓库 = 照片公开。涉及他人肖像、未公开行程的照片请勿上传
- 原图的下载直链（raw）同样公开；介意批量抓取可随时转私有仓（需同步改造画廊的鉴权代理，见 Afilmory#219 的讨论）

## 相关

- 画廊前台：[gallery.caiths.com](https://gallery.caiths.com/)
- 构建器：[Afilmory](https://github.com/Afilmory/afilmory)（MIT 开源，本仓库为其 GitHub 存储源）
- 博客：[blog.caiths.com](https://blog.caiths.com/)
