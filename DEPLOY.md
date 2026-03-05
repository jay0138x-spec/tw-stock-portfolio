# 🚀 GitHub Pages 部署指南

## 快速部署步驟（3 分鐘完成）

### 方法一：GitHub 網頁上傳（推薦初學者）

1. **登入 GitHub**：開啟 https://github.com/login

2. **建立新 Repository**：
   - 點擊右上角 "+" → "New repository"
   - Repository name: `tw-stock-portfolio`
   - 選擇 "Public"（公開）
   - 點擊 "Create repository"

3. **上傳檔案**：
   - 在新頁面點擊 "uploading an existing file"
   - 將這個資料夾的所有檔案拖曳到上傳區：
     - `index.html`
     - `README.md`
     - `LICENSE`
     - `package.json`
     - `.github/workflows/deploy.yml`
   - 點擊 "Commit changes"

4. **啟用 GitHub Pages**：
   - 進入 repository 的 "Settings"
   - 左側選單點擊 "Pages"
   - "Source" 選擇 "GitHub Actions"
   - 等待約 2-3 分鐘

5. **完成**！
   - 網站網址會顯示在 Pages 設定頁
   - 通常是 `https://你的帳號名稱.github.io/tw-stock-portfolio`

---

### 方法二：使用 Git 指令（推薦有經驗者）

```bash
# 在這個資料夾內執行
cd /Users/chou/.openclaw/workspace-sysop2/tw-stock-portfolio-site

# 設定 GitHub 帳號（只需要做一次）
git config user.email "你的email@gmail.com"
git config user.name "你的名字"

# 加入所有檔案
git add .

# 提交
git commit -m "Initial commit: 台股投資組合網站"

# 連結到 GitHub（建立 repository 後）
git remote add origin https://github.com/你的帳號名稱/tw-stock-portfolio.git

# 上傳
git push -u origin main
```

---

## 📱 使用說明

部署完成後，你可以：

1. **手機存取**：直接開啟 GitHub Pages 網址
2. **加入主畫面**：在手機瀏覽器選擇「加入主畫面」，像 App 一樣使用
3. **分享給朋友**：直接分享網址

---

## 🔧 自訂設定

### 修改網站標題
編輯 `index.html` 第 7 行：
```html
<title>你的自訂標題</title>
```

### 修改封鎖的股票
編輯 `index.html` 搜尋 `BLOCKED_STOCKS`，加入想封鎖的代碼

### 修改預設產業 Beta 值
編輯 `index.html` 搜尋 `SECTOR_BETA_MAP`

---

## 🆘 常見問題

### Q: FinMind API 無法連線？
A: 這是正常的，GitHub Pages 有時候會被 FinMind 限制。網站會自動使用本地資料庫（包含 20+ 檔常用台股）。其他股票可以手動輸入。

### Q: 如何更新網站？
A: 修改檔案後重新上傳到 GitHub，GitHub Actions 會自動重新部署。

### Q: 部署後網頁沒更新？
A: 瀏覽器快取問題，按 Ctrl+F5 (Windows) 或 Cmd+Shift+R (Mac) 強制重新整理。

---

## 📞 需要幫助？

如果有問題，可以：
1. 檢查 GitHub Pages 設定是否正確
2. 查看 GitHub Actions 的執行紀錄（repository 的 Actions 分頁）
3. 確認檔案都已正確上傳
