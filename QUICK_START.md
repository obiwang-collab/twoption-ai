# 🚀 快速開始指南

## 📦 檔案說明

你已經下載了以下檔案：

1. **app_fixed.py** - 主程式（已修正所有錯誤）
2. **requirements.txt** - Python 套件清單
3. **Procfile** - Railway 啟動指令
4. **runtime.txt** - Python 版本指定
5. **.streamlit/config.toml** - Streamlit 設定檔
6. **.gitignore** - Git 忽略清單
7. **README.md** - 專案說明
8. **DEPLOYMENT_CHECKLIST.md** - 詳細部署檢查清單

## ⚡ 3 分鐘快速部署

### 方法 1: 使用 GitHub (最簡單！)

#### Step 1: 建立 GitHub Repository
1. 登入 https://github.com
2. 點擊右上角 ➕ → "New repository"
3. Repository 名稱: `twoption-ai`
4. 選擇 Public
5. 點擊 "Create repository"

#### Step 2: 上傳檔案
1. 在新建的 Repository 頁面，點擊 "uploading an existing file"
2. 將下載的所有檔案拖曳上傳（包含 .streamlit 資料夾）
3. 點擊 "Commit changes"

#### Step 3: 連接 Railway
1. 登入 https://railway.app
2. 點擊 "New Project"
3. 選擇 "Deploy from GitHub repo"
4. 選擇 `twoption-ai`
5. 等待自動部署（約 2-3 分鐘）

#### Step 4: 設定環境變數
1. 部署完成後，點擊你的專案
2. 點擊 "Variables" 頁籤
3. 點擊 "New Variable" 新增：
   ```
   GEMINI_API_KEY
   值: 你的 Gemini API 金鑰
   ```
4. 再次點擊 "New Variable" 新增：
   ```
   OPENAI_API_KEY
   值: 你的 OpenAI API 金鑰
   ```
5. 儲存後會自動重新部署

#### Step 5: 取得網址
1. 進入 "Settings" 頁籤
2. 找到 "Domains" 區塊
3. 點擊 "Generate Domain"
4. 複製產生的網址，例如: `https://你的專案.up.railway.app`

### 方法 2: 使用 Railway CLI

如果你熟悉命令列，這個方法更快：

```bash
# 1. 安裝 Railway CLI
npm i -g @railway/cli

# 2. 登入
railway login

# 3. 進入專案資料夾
cd 下載檔案的資料夾

# 4. 初始化 Railway 專案
railway init

# 5. 部署
railway up

# 6. 設定環境變數
railway variables set GEMINI_API_KEY="你的金鑰"
railway variables set OPENAI_API_KEY="你的金鑰"

# 7. 開啟網站
railway open
```

## ✅ 驗證部署成功

開啟網站後，檢查：
- ✅ 頁面正常載入
- ✅ 可以選擇合約
- ✅ 圖表正常顯示
- ✅ AI 分析可以使用

## 🔧 設定自訂網域 (選填)

如果你有自己的網域 (例如: www.twoption-ai.com)：

1. 在 Railway Settings → Domains
2. 點擊 "Custom Domain"
3. 輸入你的網域
4. 在你的 DNS 服務商（例如 Cloudflare）新增 CNAME 記錄：
   ```
   Type: CNAME
   Name: www
   Value: 你的專案.up.railway.app
   ```

## 📊 AdSense 設定 (等審核通過後)

部署成功後，進行 AdSense 設定：

### 1. 建立 ads.txt
在專案根目錄建立 `static` 資料夾，新增 `static/ads.txt`：
```
google.com, pub-4585150092118682, DIRECT, f08c47fec0942fa0
```

### 2. 提交審核
- 確認網站已經上線且可訪問
- 到 AdSense 後台提交網站審核
- 通常需要 1-2 週審核時間

## ❓ 常見問題

### Q1: 部署失敗怎麼辦？
A: 
1. 檢查 Railway 的 "Deployments" 頁籤查看錯誤訊息
2. 確認 Procfile 檔名正確（沒有副檔名）
3. 確認所有檔案都已上傳

### Q2: 網站顯示 "Application failed to respond"
A:
1. 檢查環境變數是否設定正確
2. 查看 Deploy Logs 找出錯誤
3. 確認 Procfile 內容正確

### Q3: 如何查看錯誤訊息？
A: Railway Dashboard → 你的專案 → Deployments → 點擊最新的部署 → View Logs

### Q4: 可以免費使用嗎？
A: Railway 提供每月 $5 免費額度，通常足夠小型專案使用

## 🆘 需要幫助？

- 📧 Email: obiwang@gmail.com
- 📖 詳細檢查清單: 查看 DEPLOYMENT_CHECKLIST.md
- 🐛 發現 Bug: 請回報問題描述

---

## 🎉 恭喜！

如果一切順利，你的台指選擇權分析系統現在已經上線了！

下一步：
1. ✅ 測試所有功能
2. ✅ 提交 Google AdSense 審核
3. ✅ 分享給朋友使用
4. ✅ 持續優化改進

祝你使用愉快！🚀
