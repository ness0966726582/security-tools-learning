# Wireshark Demo - Packet Analysis Practice

## 🎯 實作目標
- 學會擷取封包（本機、目標機）
- 用 Filter 鎖定特定協定（HTTP、TCP、DNS、ICMP）
- 分析簡單的請求與回應封包
- 理解封包內容結構（Header、Payload）

---

## 🧪 實驗環境
- 攔截目標：用瀏覽器開網站、ping、登入 DVWA
- 工具：Wireshark + Firefox / ping / curl

---

## 🔍 分析任務

### 1. HTTP 封包解析
- 瀏覽 `http://testphp.vulnweb.com`（非 HTTPS）
- 觀察 GET / POST 封包
- 目標：找出 cookie、User-Agent、URL path

---

### 2. DNS 查詢封包
- 執行：`nslookup google.com`
- 觀察 DNS Request / Response 封包  
- 解釋：Query Type / Response Code / IP 回應

---

### 3. ICMP 封包（Ping）
- 執行：`ping 8.8.8.8`
- 找出 Echo Request / Echo Reply
- 說明：封包格式、TTL、Checksum

---

### 4. TCP 三次握手流程
- 開啟任意網站（如 `curl http://example.com`）
- 找出 SYN → SYN/ACK → ACK
- 標註封包號碼，畫出連線建立順序

---

## 📷 擷取截圖 + 解說
- 每個任務貼出 Wireshark 畫面
- 標記 Header 欄位（如 Source IP、Dest Port、Flags）

---

## 🧠 小技巧 & 常用 Filter
- `http.request`
- `tcp.flags.syn == 1`
- `dns`
- `icmp`
- `ip.addr == 192.168.1.100`

---

## 💡 實作心得
- 有時 HTTP 太快抓不到？用 `curl` 慢慢跑
- 避免 HTTPS 網站（因為封包加密看不到）
- 過濾條件記不起來就先存好 `.pcap` 重看！

