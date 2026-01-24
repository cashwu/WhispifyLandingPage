# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Whispify 官方網站與 Landing Page。Whispify 是一款本地端影片字幕轉錄與翻譯工具，支援 macOS 與 Windows。

## Tech Stack

- 純靜態 HTML 網站，無 build system、無 npm dependencies
- **CSS**: Tailwind CSS (CDN)
- **JS**: Vanilla JavaScript (inline `<script>`)
- **部署**: Firebase Hosting
- **語言**: 繁體中文為主，品牌名與技術術語使用英文

## Site Structure

| 檔案 | 用途 |
|------|------|
| `index.html` | 首頁（功能介紹、定價、平台支援） |
| `download.html` | 下載與安裝指南 |
| `releases.html` | 版本更新歷史 |
| `faq.html` | 常見問題 |
| `privacy.html` | 隱私權政策 |

圖片資源（`.webp`）直接放在根目錄。

## Architecture Patterns

### Platform Tabs

`download.html` 與 `releases.html` 使用相同的 platform tab 機制：
- 兩組 content div：`platform-macos` / `platform-windows`（download）或 `releases-macos` / `releases-windows`（releases）
- Tab 按鈕使用 `.platform-tab-btn` class，透過 `active` class 控制狀態
- 預設顯示 macOS，Windows 內容加 `hidden` class

### URL Hash Navigation

- `releases.html#v1.0.8` → macOS 版本，滾動到對應 `<details>` 並展開
- `releases.html#win-v1.0.0` → 切換到 Windows tab 並滾動到對應元素
- `download.html#win` → 切換到 Windows 安裝指南

Windows 版本的 hash 統一使用 `win-` 前綴來判斷平台。

### Scroll Animations

使用 Intersection Observer API 實現滾動觸發動畫，搭配 `.animate-in` class 與 `delay-*` 變體控制入場時序。

### Design System

- 深色主題：背景 `#050208` 到 `#241832` 漸層
- 強調色：Violet (`#7C3AED`)、Cyan (`#06B6D4`)、Amber (`#F59E0B`)
- 毛玻璃卡片效果（glassmorphism）
- 漸層邊框與發光效果

## Conventions

### Release Notes

macOS 與 Windows 版本號獨立，各自有自己的 latest version。發佈新版本時需同時更新兩個頁面：

**`releases.html`**：
1. 將目前的 latest card 內容搬到 previous releases 區塊（用 `<details>` 包裹）
2. 更新 latest card 為新版本內容
3. macOS latest card 有 `id="v{version}"`，Windows latest card 有 `id="win-v{version}"`
4. Previous releases 的 `<details>` 使用相同 id 規則
5. Previous releases 區塊 id 為 `releases-macos-prev` / `releases-windows-prev`

**`download.html`**：
1. 更新對應平台的下載連結與版本號

### Commit Messages

使用 `feat:` / `fix:` / `chore:` 前綴，英文撰寫。

## Deployment

靜態檔案直接部署到 Firebase Hosting，無需 build 步驟。域名為 `whispifyapp.com`。
