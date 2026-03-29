🌌 匿名許願池系統 (Anonymous Wish Pool)
這是一個基於 GitHub Pages 前端介面，結合 Google Apps Script (GAS) 作為後端處理，並使用 Google Sheets 作為資料庫的輕量化匿名投稿系統。系統具備 Discord Webhook 即時通知功能，並預設所有投稿為「待處理」狀態，方便管理員進行審核。

🚀 核心功能
匿名投稿：使用者無需登入即可投遞願望或建議。

自動化資料庫：所有投稿即時寫入 Google 試算表，包含時間戳記與分類。

審核機制：投稿預設狀態為 待處理，確保內容品質。

即時通知：透過 Discord Webhook，管理員可在第一時間收到新投稿提醒。

極簡介面：符合 Z 世代審美的暗色系與霓虹發光視覺設計。

🛠️ 技術棧 (Tech Stack)
Frontend: HTML5, CSS3, JavaScript (Fetch API)

Backend: Google Apps Script (GAS)

Database: Google Sheets

Integration: Discord Webhook API

📖 部署指南 (全部步驟)
1. Google 試算表設定
建立新的 Google 試算表，並將工作表命名為 SurveyData。

標題列設定：A1:時間戳記、B1:許願類別、C1:內容、D1:狀態。

2. 後端腳本部署 (GAS)
在試算表中點擊「擴充功能」 > 「Apps Script」。

貼入專案提供的 code.gs 程式碼。

替換代碼中的 discordUrl 為使用者的 Webhook 網址。

點擊 「部署」 > 「新部署」：

類型：網頁應用程式

誰有權限存取：任何人 (Anyone)

複製產生的 .exec 網址。

3. 前端網頁部署 (GitHub Pages)
將 index.html 上傳至本儲存庫。

修改 index.html 中的 const api 變數，填入上一步複製的 GAS 網址。

前往 GitHub 儲存庫的 Settings > Pages，選擇 main 分支並儲存。

📝 授權協議
本專案採用 MIT 授權協議。
