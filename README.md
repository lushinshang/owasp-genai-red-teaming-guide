# 模型說「不」不算數：OWASP 紅隊手冊要你證明的，是模型以外那道牆

OWASP GenAI Security Project 在 2026 年 10 月發布《GenAI Red Teaming Manual》1.0 版（144 頁）。本導讀不照八個階段逐章摘要，而是順著手冊反覆出現的一條主張重新編排：可強制的安全邊界必須落在模型無法改寫的服務裡，紅隊的工作是用可重現、有分母的證據，證明這條邊界守不守得住。全文附 PDF 頁碼方便回原文核對，手冊的主張與導讀者的判斷分開標示。另附一份台灣資訊資安用語對照表（250 條）、手冊全文的繁體中文譯本，並把手冊內 9 張圖翻成繁體中文；導讀內另有 5 張重排的手冊表格與 5 張導讀者自製概念圖。

網頁版：https://lushinshang.github.io/owasp-genai-red-teaming-guide/
術語對照：https://lushinshang.github.io/owasp-genai-red-teaming-guide/glossary.html
手冊全文中譯：https://lushinshang.github.io/owasp-genai-red-teaming-guide/manual-zh.html

## 200字介紹

多數 AI 紅隊報告寫「攻擊成功率 0%」，卻沒說拒絕是模型自己決定的，還是模型以外的服務擋下的；也沒說這一百次測試到底能證明什麼。這份導讀依手冊整理出一條主線：信任邊界必須在模型之外強制執行，提示指令、模型拒答與分類器只算縱深防禦。順著這條線，文章談演練前要寫下「不測什麼」、怎麼畫資料流與信任邊界、每類攻擊證明了哪一層失守、入侵為何不會隨對話結束、影響要照最壞的可達後果計算，以及「沒打穿」為什麼不等於安全，並帶讀者看手冊如何用判定準則、分母與信賴上限讓數字可信。文中只談概念、判準與防禦結論，不轉述攻擊操作細節。

## 檔案說明

| 檔案 | 說明 |
|------|------|
| `index.html` | 導讀網頁（單檔，瀏覽器直接開啟） |
| `manual-zh.html` | 《GenAI Red Teaming Manual》1.0 全文繁體中文譯本（144 頁逐頁標示頁碼，單檔） |
| `glossary.html` | 台灣資訊資安用語對照網頁（250 條，可搜尋、分類篩選） |
| `owasp-genai-red-teaming-guide.md` | 導讀正文（Markdown） |
| `glossary.tsv` | 用語對照原始資料（Tab 分隔，UTF-8） |
| `images/` | 手冊內 9 張圖的繁體中文翻譯與導讀者自製的 5 張概念圖（WebP） |
| `README.md` | 本檔 |
| `share_post.md` | 社群分享文 |
| `.gitignore` | 忽略本機 QA 截圖與暫存檔 |

## 原始素材

- 原作：《GenAI Red Teaming Manual Version 1.0》，OWASP GenAI Security Project，2026 年 10 月，https://genai.owasp.org/resource/genai-red-teaming-manual-version-1-0/
- 授權：原作為 CC BY-SA 4.0（見手冊 p.2）。

## 授權與修改說明

本導讀、術語對照與全文中譯為原作的衍生作品，內容包含摘要、重組、評論、用語對照、全文翻譯、表格重排與圖片翻譯，已作修改；以 [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) 授權釋出。本專案不代表原作者或 OWASP 的立場，也未經其背書；與原文有出入時，以原文為準。全文中譯由機器翻譯產生，再由 AI 審校代理（不是人工）對照原文逐頁檢查（涵蓋 143／144 頁，未審的 p.40 是圖頁），沒有人工逐字校對，非官方譯本。

## 查證來源

- 手冊全文（PDF）：https://genai.owasp.org/download/58204/
- 文中事實逐條對照手冊 PDF 頁面（以 PDF 頁碼標示），公開案例與統計數字只轉述手冊成稿時的描述，現況請自行查證。
- 術語譯法參考 Microsoft Learn 繁體中文文件、趨勢科技繁體中文頁面、iThome 與 Google Cloud 繁體中文文件；OWASP LLM／Agentic 十大風險 2026 的中文名稱為本專案擬定（尚未見官方繁中版）。
