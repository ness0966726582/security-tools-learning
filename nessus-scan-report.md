# Nessus Scan Report - Vulnerability Analysis

## 🎯 實作目標
- 熟悉 Nessus 安裝與掃描流程
- 掃描一台有漏洞的測試機（如 Metasploitable2）
- 能讀懂掃描結果、風險等級與 CVE 編號
- 實作一份簡易的「風險報告摘要」

---

## 🧪 實驗環境
- 掃描器端：Kali / Windows + Nessus Essentials（免費版）
- 目標端：Metasploitable2 / DVWA / OWASP BWA

---

## 🛠️ 掃描流程紀錄
1. 安裝 Nessus Essentials 並啟用授權
2. 建立掃描任務（輸入目標 IP）
3. 選擇掃描類型：Basic Network Scan
4. 啟動掃描，等待完成
5. 匯出報告（HTML / PDF / CSV）

---

## 📊 掃描結果分析（含圖）

### 🟠 高風險項目
- Vulnerability: **OpenSSH User Enumeration Timing Attack**
- CVE: CVE-2018-15473
- 說明：透過時間差可猜測使用者帳號是否存在
- 修補建議：更新 OpenSSH 至安全版本

---

### 🟡 中風險項目
- Vulnerability: **Apache 2.2.x Multiple Vulnerabilities**
- CVE: CVE-2011-3192 等
- 問題：存在 DOS 攻擊與版本過舊問題
- 建議：升級 Web 伺服器版本

---

### 🔵 低風險項目
- Vulnerability: **FTP Banner Disclosure**
- 說明：洩露 FTP 版本資訊，可供駭客偵查使用
- 建議：隱藏 banner / 使用加密傳輸協定

---

## 📘 小知識筆記
- CVE（Common Vulnerabilities and Exposures）是什麼？
- Risk Rating（Critical / High / Medium / Low）是怎麼判的？
- Nessus 用 Plugin ID 管理漏洞偵測邏輯

---

## 📷 擷圖區
- 掃描設定畫面
- 結果總覽畫面
- 詳細漏洞說明畫面

---

## 🧠 心得與延伸
- 自動掃描雖方便，但還是要自己看懂報告
- 針對 CVE 搜尋 Exploit 會是實戰關鍵
- 如果遇到 false positive，要學會怎麼判斷真偽（補：手動驗證方式）

