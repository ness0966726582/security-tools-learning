🔍 Nmap
📌 用途：主機偵測、Port 掃描、服務版本分析、OS fingerprinting

🎯 學習目標：
掃描網段中的設備與開放 Port
使用不同掃描模式（TCP SYN、UDP、Stealth）
解讀服務版本與作業系統推測結果

🧰 常用指令：
nmap -sP 192.168.1.0/24 → Ping 掃描
nmap -sS -sV 192.168.1.1 → 半開掃描 + 版本偵測
nmap -O 192.168.1.1 → OS 推測
