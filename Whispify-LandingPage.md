請幫我建立一個簡潔現代的 landing page，用於展示一個 macOS 應用程式：

### 產品資訊

**產品名稱：** Whispify

**一句話描述：** Mac 原生影片字幕轉錄與翻譯工具

**核心價值主張：**
將任何影片轉換成精準字幕，支援 AI 翻譯 — 完全在你的 Mac 上本地處理，保護隱私。

---

### 品牌配色（參考 App Icon）

App Icon 設計：白色圓角方形背景，紫色聲波圖形漸變至右側的文字線條，象徵「聲音轉文字」

**主色調：**
- 主要紫色：#7C3AED (Violet 600)
- 深紫色：#6D28D9 (Violet 700) - 用於 hover、強調
- 淺紫色：#A78BFA (Violet 400) - 用於漸層、次要元素
- 極淺紫：#EDE9FE (Violet 100) - 用於背景區塊

**背景：**
- 主背景：深色 #0F0A1A（帶紫調的深黑色）或 #1A1025
- 卡片背景：#1E1529 或半透明白色

**漸層方案：**
- 主要漸層：from-violet-600 to-purple-500
- 背景漸層：subtle radial gradient 帶紫色光暈

**文字：**
- 主要文字：白色 #FFFFFF
- 次要文字：#A1A1AA（灰色）

---

### 頁面結構

#### 1. Hero Section
- 產品名稱「Whispify」（大標題）
- 標語：「影片字幕轉錄與翻譯工具」
- 副標語：「完全本地處理，保護你的隱私」
- 主視覺：可放 App Icon 或 app 截圖 mockup
- CTA 按鈕：「了解更多」（滾動到功能區）
- Badge：「隱私優先」、「本地處理」

#### 2. Features Section
6 個主要功能卡片（深色卡片帶紫色邊框或 glow）：

1. **本地語音辨識**
   - Icon：waveform 或 cpu
   - 說明：使用 WhisperKit (Apple CoreML) 在本機進行語音轉文字，不需上傳影片到雲端

2. **多語言支援**
   - Icon：globe
   - 說明：支援英文、日文、中文等多種語言的語音辨識

3. **AI 智慧翻譯**
   - Icon：language 或 translate
   - 說明：整合 OpenAI 相容 API，一鍵將字幕翻譯成繁體中文

4. **彈性模型選擇**
   - Icon：slider 或 layers
   - 說明：從輕量 Tiny 到高精度 Large，依需求選擇 Whisper 模型

5. **SRT 匯出**
   - Icon：document-arrow-down
   - 說明：支援原文、翻譯、雙語三種字幕格式匯出

6. **自動佇列處理**
   - Icon：queue-list
   - 說明：批次匯入影片，自動排隊轉錄

#### 3. How it Works Section
3 步驟流程（水平排列，有連接線或箭頭）：

1. **匯入影片**
   - Icon：film 或 folder-open
   - 說明：拖放或選擇影片檔案

2. **選擇模型轉錄**
   - Icon：waveform 或 play
   - 說明：選擇 Whisper 模型，開始語音辨識

3. **翻譯匯出**
   - Icon：document-check
   - 說明：一鍵翻譯並匯出 SRT 字幕檔

#### 4. Platform Section（平台支援）
標題：「支援平台」

兩個平台卡片並排：

1. **macOS**
   - Icon：Apple logo
   - 狀態 Badge：「✓ 已推出」（綠色或紫色實心 badge）
   - 系統需求：macOS 14.0 (Sonoma) 或以上

2. **Windows**
   - Icon：Windows logo
   - 狀態 Badge：「開發中」（灰色或虛線邊框 badge）
   - 說明：敬請期待

下方文案：「想要 Windows 版？追蹤社群獲得最新開發進度！」

#### 5. CTA Section（社群追蹤）
- 標題：「對這個工具有興趣？」
- 副標題：「追蹤我的社群帳號，第一時間獲得發布通知」
- 兩個社群按鈕並排：
  1. **Threads 按鈕**
     - 連結：https://www.threads.com/@cashwugeek
     - 圖示：Threads logo
     - 文案：「追蹤 Threads」
  2. **X (Twitter) 按鈕**
     - 連結：https://x.com/cashwugeek
     - 圖示：X logo
     - 文案：「追蹤 X」
- 下方顯示 handle：@cashwugeek

#### 6. Footer
- 版權資訊：© 2025 Whispify
- 可選：簡單的連結（隱私政策 placeholder）

---

### 設計風格

- 簡潔現代，符合 Apple 設計美學
- 深色主題搭配紫色調漸層
- 微妙的紫色光暈效果（glow）增加科技感
- 卡片元素有輕微的 glassmorphism 效果
- Hero 區塊可加入聲波動畫元素，呼應 App Icon 設計
- 單頁式設計，smooth scroll

### 按鈕樣式

**主要 CTA 按鈕：**
- 紫色漸層背景 (violet-600 → purple-500)
- 圓角、適當 padding
- hover 時加深或加 glow 效果

**社群按鈕：**
- 深色背景 + 紫色邊框
- 或使用各平台品牌色
- hover 時有微妙的 lift 效果

**狀態 Badge：**
- 「已推出」：綠色或紫色實心背景
- 「開發中」：灰色背景或虛線邊框

---

### 技術需求

- 響應式設計（支援桌機、平板、手機）
- 使用 Tailwind CSS
- 純前端 HTML/CSS/JS（或 React/Next.js 單頁）
- 可部署到 GitHub Pages、Vercel、Netlify 等靜態託管
- 不需要後端
- 社群連結在新分頁開啟（target="_blank"）

---

### 目標用戶（供文案參考）

- 影片創作者 / YouTuber
- 語言學習者
- 需要為外語影片加字幕的使用者
- 重視隱私、不想上傳影片到雲端的人

---

### 額外細節

- 所有文案使用繁體中文
- 強調「本地處理」和「隱私優先」的賣點
- 可加入簡單的入場動畫（fade in、slide up）
- Platform Section 的「開發中」卡片可以稍微降低透明度，表示尚未推出
