# 在 ChatGPT 使用：建立自訂 GPT

需要 ChatGPT 付費方案（可建立 GPT 的帳號）。

1. 打開 ChatGPT → 左側 **GPTs** → **Create**（建立）→ 切到 **Configure**（設定）分頁。
2. 依下表填寫：

| 欄位 | 填入內容 |
|---|---|
| Name | 決策三問思考教練 |
| Description | 用蘇格拉底式提問，帶你以決策三問想清楚轉職、團隊方向與產品策略（不處理投資與政治）。 |
| Instructions | 複製 [`../system-prompt.md`](../system-prompt.md) 的**全部內容**貼上 |
| Conversation starters | 我在考慮要不要轉職／團隊下季該先做哪個方向？／這個產品功能該不該砍？／用決策三問幫我想一個決定 |
| Knowledge | 上傳 `skills/decision3q-mrsbao/references/` 裡的 `knowledge-base.md` 和 `decision-matrix-template.md` |
| Capabilities | 全部可關閉（不需要網頁搜尋、圖片生成、程式碼） |

3. 右上角 **Create** → 選擇分享範圍（只有我／有連結的人／GPT 商店）。

> Instructions 欄位有字數上限（約 8,000 字元），`system-prompt.md` 已控制在範圍內；知識內容請放在 Knowledge 檔案，不要貼進 Instructions。
