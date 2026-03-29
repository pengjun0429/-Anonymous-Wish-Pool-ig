# 🌌 匿名許願池系統 (Anonymous Wish Pool)

這是一個基於 **GitHub Pages** 前端介面，結合 **Google Apps Script (GAS)** 後端處理，並使用 **Google Sheets** 作為資料庫的輕量化匿名投稿系統。

---

## 🚀 核心功能
* **匿名投稿**：使用者無需登入即可投遞願望或建議。
* **自動化資料庫**：投稿即時寫入 Google 試算表，包含時間戳記與分類。
* **審核機制**：投稿預設狀態為 `待處理`，確保內容品質。
* **即時通知**：透過 Discord Webhook，管理員可在第一時間收到新投稿提醒。
* **介面美化**：暗色系視覺設計，並針對行動裝置優化字體大小。

---

## 🛠️ 技術棧 (Tech Stack)
* **Frontend**: HTML5, CSS3 (包含行動裝置字體優化), JavaScript (Fetch API)
* **Backend**: Google Apps Script (GAS)
* **Database**: Google Sheets
* **Integration**: Discord Webhook API

---

## 📖 部署指南 (全部步驟)

### 1. Google 試算表設定
1. 建立新的 Google 試算表，將工作表命名為 `SurveyData`。
2. 標題列設定：`A1:時間戳記`、`B1:許願類別`、`C1:內容`、`D1:狀態`。

### 2. 後端腳本部署 (GAS)
1. 在試算表中點擊「擴充功能」 > 「Apps Script」。
2. 貼入 `code.gs` 程式碼並更換 Discord Webhook 網址。
3. 點擊 **「部署」 > 「新部署」**：
   * **類型**：網頁應用程式
   * **誰有權限存取**：**任何人 (Anyone)**
4. 複製產生的 `.exec` 網址。

### 3. 前端網頁部署 (GitHub Pages)
1. 將 `index.html` 上傳至 GitHub。
2. 修改 `index.html` 中的 `const api` 變數，填入 GAS 網址。
3. 在 GitHub 儲存庫的 **Settings > Pages** 開啟網頁託管。

---

## 🎨 介面調整建議 (字體與視覺)

為了確保在不同裝置上的閱讀體驗，建議在 CSS 中維持以下設定：
* **標題 (h1)**：建議 `2rem` (約 32px)，醒目且具引導性。
* **內容區域 (select, textarea)**：建議 **至少 `16px`**，防止 iOS 裝置在輸入時自動縮放畫面。
* **按鈕 (button)**：建議 `1.1rem` (約 18px)，增加點擊區域的直覺性。

---


## 📝 授權協議
本專案採用 MIT 授權協議。
