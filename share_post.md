## 短版（LINE、群組）

你的 AI 紅隊報告寫「攻擊成功率 0%」，那是誰擋下的？

OWASP《GenAI Red Teaming Manual》1.0 的主線很清楚：提示指令、模型拒答、分類器只算縱深防禦，能強制的邊界要設在模型改寫不了的服務裡。

我把這份 144 頁的手冊整理成三份給台灣讀者的資料：
・導讀：照這條主線重排，附 5 張手冊表格與 5 張自製概念圖
・全文中譯：144 頁逐頁標頁碼，機器翻譯、AI 逐頁審校，非官方譯本，以原文為準
・資安用語對照：250 條台灣譯法

導讀 https://lushinshang.github.io/owasp-genai-red-teaming-guide/
全文中譯 https://lushinshang.github.io/owasp-genai-red-teaming-guide/manual-zh.html
用語對照 https://lushinshang.github.io/owasp-genai-red-teaming-guide/glossary.html

## 長版（Facebook、LinkedIn、社群貼文）

你的 AI 紅隊報告寫「攻擊成功率 0%」，那是誰擋下的？是模型自己拒絕，還是模型以外的服務擋住？這一百次測試，到底能證明什麼？

OWASP 在 2026 年 10 月發布《GenAI Red Teaming Manual》1.0，共 144 頁。讀完最值得帶走的一句話：提示指令、模型拒答、模型式分類器都只算縱深防禦，真正能強制的邊界，必須落在模型繞不過、改寫不了的服務裡。紅隊要做的，是用可重現、有分母的證據，證明這道邊界守不守得住。

我做了三份東西，給台灣的資安從業者，以及正把大型語言模型與 AI 代理接進業務系統的工程團隊：

1. 導讀：不照八個階段逐章摘要，順著上面那條主線重排；演練前要先寫下「不測什麼」、信任邊界怎麼畫、入侵為什麼不會隨對話結束、「沒打穿」為什麼不等於安全。內附 5 張手冊表格與 5 張導讀者自製的概念圖。
2. 全文中譯：144 頁逐頁標示頁碼，導讀裡每個 `（p.N）` 都能點到對應頁。這是機器翻譯，再由 AI 審校代理對照原文檢查 143 頁，沒有人工逐字校對，不是官方譯本，有出入請以原文為準。
3. 資安用語對照：250 條，列出台灣常用譯法與建議避免的用語，頁碼同樣連到全文中譯。

導讀 https://lushinshang.github.io/owasp-genai-red-teaming-guide/
全文中譯 https://lushinshang.github.io/owasp-genai-red-teaming-guide/manual-zh.html
用語對照 https://lushinshang.github.io/owasp-genai-red-teaming-guide/glossary.html

原作：OWASP GenAI Security Project《GenAI Red Teaming Manual》Version 1.0，CC BY-SA 4.0。本專案為衍生作品，已作修改，沿用同一授權，不代表 OWASP 的立場。
