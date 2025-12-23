# 台指選擇權籌碼分析 - 莊家思維

## 📋 專案說明

這是一個台灣期貨選擇權市場的即時數據分析平台，結合 AI 技術提供莊家控盤分析。

## 🚀 Railway 部署指南

### 1. 環境變數設定

在 Railway Dashboard 中設定以下環境變數：

```
GEMINI_API_KEY=你的_Gemini_API_金鑰
OPENAI_API_KEY=你的_OpenAI_API_金鑰
```

### 2. 檔案結構

```
專案目錄/
├── app_fixed.py          # 主程式
├── requirements.txt      # Python 套件清單
├── Procfile             # Railway 啟動指令
├── runtime.txt          # Python 版本指定
├── .streamlit/
│   └── config.toml      # Streamlit 設定
└── .gitignore           # Git 忽略清單
```

### 3. 部署步驟

1. 將所有檔案上傳到 GitHub Repository
2. 在 Railway 中連接你的 GitHub Repository
3. Railway 會自動偵測 Procfile 並部署
4. 在 Railway Settings → Variables 中新增環境變數
5. 等待部署完成

### 4. 自訂網域設定

1. 在 Railway Dashboard → Settings → Domains
2. 點擊 "Generate Domain" 或 "Custom Domain"
3. 如果使用自訂網域，需要在 DNS 設定 CNAME 記錄

## 🔧 技術棧

- **前端框架**: Streamlit
- **資料處理**: Pandas, NumPy
- **視覺化**: Plotly
- **AI 整合**: Google Gemini, OpenAI GPT
- **數據來源**: 台灣期貨交易所 (TAIFEX)

## 📊 核心功能

- 📈 即時選擇權未平倉分析
- 🏦 三大法人籌碼追蹤
- 🤖 AI 莊家控盤預測
- 📉 Dealer Gamma Exposure (GEX) 分析
- 💰 Google AdSense 廣告整合
- 📱 PWA (Progressive Web App) 支援

## ⚠️ 免責聲明

本網站提供的資訊僅供參考，不構成投資建議。所有投資決策應由您自行判斷，本站不負任何盈虧責任。

## 📧 聯絡方式

Email: obiwang@gmail.com

---

© 2025 台指選擇權籌碼分析. All rights reserved.
