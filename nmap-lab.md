# Nmap Lab - Network Scanning Practice

## 🎯 實作目標
- 掌握基本的 Nmap 掃描語法與選項
- 能分辨主機存活、開放 Port 與 OS fingerprinting
- 熟悉實際使用情境（資安測試 or 偵察前置）

## 🧪 實驗環境
- 測試機：Kali Linux / Parrot OS / 自建 VM
- 目標機：Metasploitable2 / DVWA / 本機網段裝置

## 🛠️ 常用掃描指令 + 結果解析

### 1. 主機掃描（Ping sweep）
```bash
nmap -sn 192.168.1.0/24
說明：列出這個網段裡「活著的主機」。
→ 結果範例 + 解釋 ICMP 的作用。

### 2. Port 掃描
```bash
nmap -sS 192.168.1.100
說明：半開掃描（SYN），比 TCP connect 快又 stealth。
→ 解釋常見 port 結果（如 22, 80, 443）

### 3. OS 探測 & Banner 抓取
```bash
nmap -sV -O 192.168.1.100
→ 看到服務版本、可能的作業系統
→ 解釋結果可信度 & OS fingerprint 是怎麼判的
