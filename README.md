# 台股 AI 智慧投資組合與風險分析系統

🔗 **線上體驗**: https://yourusername.github.io/tw-stock-portfolio

![台股投資組合](screenshot.png)

## ✨ 功能特色

- 📊 **投資組合管理**：新增、刪除、編輯台股持股
- 🤖 **AI 投資報告**：整合 Kimi AI 生成專業投資分析
- 📈 **風險分析**：基於 Beta 係數的風險評估
- 🏭 **產業板塊**：視覺化產業集中度分析
- 📱 **響應式設計**：支援手機、平板、桌機

## 🚀 快速開始

### 1. 本地測試
```bash
# 方法一：使用 Python
python3 -m http.server 8080

# 方法二：使用 Node.js
npx http-server -p 8080

# 方法三：使用 VS Code Live Server 插件
```

### 2. 訪問網站
開啟瀏覽器訪問 `http://localhost:8080`

## 📖 使用說明

### 新增持股
1. 輸入股票代碼（如：2330）
2. 系統會自動帶入股票名稱和產業類別
3. 輸入持有股數和成本價
4. 點擊確認加入

### AI 報告
1. 切換到「AI 投資報告」頁面
2. 貼上你的 Kimi API 金鑰（sk-...）
3. 點擊「呼喚 Kimi 生成專業報告」
4. 等待 AI 分析完成

> 💡 **提示**：Kimi API 金鑰可以在 [Moonshot AI](https://platform.moonshot.cn/) 申請

## 🔧 技術架構

- **前端**：原生 HTML5 + Tailwind CSS
- **圖表**：Chart.js
- **Markdown 渲染**：Marked.js
- **資料來源**：FinMind API（台股資料）
- **AI 服務**：Moonshot AI (Kimi)

## 🌐 部署到 GitHub Pages

### 方法一：自動部署
1. Fork 這個 repository
2. 進入 Settings → Pages
3. Source 選擇 "Deploy from a branch"
4. Branch 選擇 "main"，資料夾選擇 "/ (root)"
5. 點擊 Save，等待幾分鐘即可

### 方法二：手動上傳
1. 下載所有檔案
2. 建立新的 GitHub repository
3. 上傳檔案到 repository
4. 啟用 GitHub Pages（Settings → Pages）

## ⚠️ 注意事項

- API 金鑰僅儲存在本地瀏覽器，不會上傳到任何伺服器
- FinMind API 免費版有請求限制，如遇到連線問題可手動輸入股票資訊
- 建議使用現代瀏覽器（Chrome、Firefox、Safari、Edge）

## 📝 更新日誌

### v1.0.0 (2026-03-06)
- 🎉 初始版本發布
- ✅ 投資組合管理功能
- ✅ AI 投資報告生成
- ✅ 風險分析與產業板塊視覺化
- ✅ 響應式設計

## 📄 授權

MIT License - 詳見 [LICENSE](LICENSE) 檔案

## 🙏 致謝

- [FinMind](https://finmindtrade.com/) - 台股資料 API
- [Moonshot AI](https://moonshot.cn/) - Kimi AI 服務
- [Tailwind CSS](https://tailwindcss.com/) - CSS 框架
- [Chart.js](https://www.chartjs.org/) - 圖表函式庫
 
