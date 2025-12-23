# Railway 部署檢查清單

## ✅ 部署前準備

### 1. 檔案準備
- [ ] app_fixed.py (主程式)
- [ ] requirements.txt (Python 套件清單)
- [ ] Procfile (啟動指令)
- [ ] runtime.txt (Python 版本)
- [ ] .streamlit/config.toml (Streamlit 設定)
- [ ] .gitignore (Git 忽略清單)
- [ ] README.md (專案說明)

### 2. Railway 設定步驟

#### 方法 A: 使用 GitHub (推薦)

1. **建立 GitHub Repository**
   - 登入 GitHub
   - 點擊右上角 "+" → "New repository"
   - 輸入 Repository 名稱 (例如: `twoption-ai`)
   - 設定為 Public 或 Private
   - 點擊 "Create repository"

2. **上傳檔案到 GitHub**
   ```bash
   # 在本地建立資料夾
   mkdir twoption-ai
   cd twoption-ai
   
   # 初始化 Git
   git init
   
   # 複製所有下載的檔案到這個資料夾
   # 然後執行:
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/你的帳號/twoption-ai.git
   git push -u origin main
   ```

3. **連接 Railway**
   - 登入 Railway (https://railway.app)
   - 點擊 "New Project"
   - 選擇 "Deploy from GitHub repo"
   - 選擇你剛建立的 Repository
   - Railway 會自動開始部署

4. **設定環境變數**
   - 部署完成後，點擊專案
   - 進入 "Variables" 頁籤
   - 點擊 "New Variable"
   - 新增以下變數:
     ```
     GEMINI_API_KEY = 你的_Gemini_金鑰
     OPENAI_API_KEY = 你的_OpenAI_金鑰
     ```
   - 儲存後 Railway 會自動重新部署

5. **設定自訂網域**
   - 進入 "Settings" 頁籤
   - 找到 "Domains" 區塊
   - 點擊 "Generate Domain" (免費子網域)
   - 或點擊 "Custom Domain" 新增自己的網域

#### 方法 B: 直接從本地部署

1. **安裝 Railway CLI**
   ```bash
   npm i -g @railway/cli
   ```

2. **登入 Railway**
   ```bash
   railway login
   ```

3. **初始化專案**
   ```bash
   cd 你的專案資料夾
   railway init
   ```

4. **部署**
   ```bash
   railway up
   ```

5. **設定環境變數**
   ```bash
   railway variables set GEMINI_API_KEY="你的金鑰"
   railway variables set OPENAI_API_KEY="你的金鑰"
   ```

### 3. 驗證部署

部署完成後，檢查以下項目:

- [ ] 網站可以正常開啟
- [ ] 數據可以正常載入
- [ ] 選擇權圖表正常顯示
- [ ] AI 分析功能可用
- [ ] 廣告代碼正確載入
- [ ] 沒有 Console 錯誤訊息

### 4. 常見問題排查

#### 問題 1: "Application failed to respond"
**解決方法:**
- 檢查 Procfile 是否正確
- 檢查 requirements.txt 所有套件都能正常安裝
- 查看 Railway 的 Deploy Logs

#### 問題 2: 模組找不到
**解決方法:**
- 確認 requirements.txt 包含所有需要的套件
- 重新部署: `railway up --detach`

#### 問題 3: 環境變數無效
**解決方法:**
- 確認變數名稱拼寫正確 (區分大小寫)
- 重新部署讓變數生效

#### 問題 4: PORT 錯誤
**解決方法:**
- 確認 Procfile 使用 `$PORT` 變數
- Railway 會自動提供 PORT 環境變數

### 5. AdSense 設定 (部署成功後)

1. **ads.txt 檔案**
   - 在專案根目錄建立 `static` 資料夾
   - 建立 `static/ads.txt` 檔案
   - 內容:
     ```
     google.com, pub-4585150092118682, DIRECT, f08c47fec0942fa0
     ```

2. **提交 AdSense 審核**
   - 確認網站可正常訪問
   - 確認廣告代碼已載入
   - 提交 Google AdSense 審核

### 6. 效能優化建議

- [ ] 啟用 Railway 的自動休眠功能 (免費方案)
- [ ] 監控 Memory 使用量
- [ ] 設定適當的 Cache TTL
- [ ] 定期檢查 Deploy Logs

---

## 🆘 需要協助?

如果遇到問題:
1. 檢查 Railway Deploy Logs
2. 確認所有設定檔案格式正確
3. 驗證環境變數已正確設定
4. 聯絡 Email: obiwang@gmail.com
