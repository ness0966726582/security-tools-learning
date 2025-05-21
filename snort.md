🔔 Snort
📌 用途：網路入侵偵測（IDS），可自訂告警規則

🎯 學習目標：
撰寫自定義規則：如偵測 ping、login 字串
學會規則語法（協定 / port / content / msg / sid）
在終端機觀察即時告警

🧰 範例規則：
> alert icmp any any -> any any (msg:"Ping detected"; sid:1000001;)
