🧪 Scapy
📌 用途：封包生成/改寫神器，用程式控制封包發送

🎯 學習目標：
撰寫 Python 腳本模擬 Ping flood、TCP SYN
建立自訂封包結構，理解底層運作
結合 Wireshark 驗證封包被正確送出

🧰 簡單範例：
> from scapy.all import *
send(IP(dst="192.168.1.1")/ICMP(), count=10)
