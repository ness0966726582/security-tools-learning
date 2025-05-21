# Burp Suite Walkthrough - Web Pentest Lab

## 🎯 實作目標
- 安裝與設定 Burp Suite（免費版）
- 攔截並觀察網站的 HTTP 請求與回應
- 修改表單參數、cookie、header 並觀察效果
- 嘗試模擬簡單漏洞測試（如弱密碼登入）

---

## 🧪 實驗環境
- 測試站：DVWA（Damn Vulnerable Web App） / PortSwigger Labs
- 瀏覽器：Firefox + Burp Proxy 設定（127.0.0.1:8080）

---

## 🛠️ 操作任務列表

### 1. 攔截登入請求
- 操作：打開 DVWA 登入頁 → 輸入 admin / admin → 攔截送出
- 分析內容：username, password 參數 → Request/Response headers
- 學習：HTTP POST 請求格式長怎樣？

---

### 2. 修改登入參數
- 在 Intercept 中修改 username → `admin' or '1'='1`
- 嘗試 SQL Injection（初階）
- 結果觀察：是否繞過驗證？有錯誤訊息？

---

### 3. 分析 Cookie 與 Session 機制
- 登入後觀察 Set-Cookie headers
- 改 Cookie 值 → 看是否能繞過權限
- 分析常見：`PHPSESSID`、JWT

---

### 4. 使用 Repeater 重送請求
- 把一筆請求丟進 Repeater
- 嘗試改參數做暴力測試（ex: 密碼字典爆破）
- 學習：怎麼從觀察變成主動攻擊（安全前提下）

---

## 📷 截圖與標註
- 攔截畫面 + 改參數前後對比
- Repeater 使用流程 + 結果畫面
- Cookie before/after 畫面對照

---

## 🔍 小技巧筆記
- 如何快速導入 Proxy 設定（用 burp cert 匯入）
- 攔截 HTTPS 請求時的注意事項
- 快捷鍵與 Repeater 節奏最佳化

---

## 🧠 心得與補充
- 攔截請求後才知道前端畫面只是假的
- Repeater 讓我更理解參數怎麼被伺服器解讀
- 如果網站回應「403 Forbidden」，該怎麼繞？

---

## 🚀 Bonus 延伸
- 結合字典檔做簡單爆破
- 安裝 Burp 插件如 Active Scan++ / Logger++
