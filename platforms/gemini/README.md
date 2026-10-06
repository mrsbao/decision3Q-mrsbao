# 在 Gemini 使用：建立 Gem

1. 打開 [gemini.google.com](https://gemini.google.com) → 左側 **探索 Gem（Explore Gems）** → **新增 Gem（New Gem）**。
2. 依下表填寫：

| 欄位 | 填入內容 |
|---|---|
| 名稱 | 決策三問思考教練 |
| 說明 | 用蘇格拉底式提問，帶你以決策三問想清楚轉職、團隊方向與產品策略（不處理投資與政治）。 |
| 指示（Instructions） | 複製 [`../system-prompt.md`](../system-prompt.md) 的**全部內容**貼上 |
| 知識（Knowledge） | 上傳 `skills/decision3q-mrsbao/references/` 裡的 `knowledge-base.md` 和 `decision-matrix-template.md` |

3. 先在右側預覽區測試一輪對話，確認會一次只問 1～2 個問題、結尾有【教練思考提問】，再按 **儲存（Save）**。
4. 若要給別人用，在 Gem 管理頁點 **分享**，取得連結。

> 不要按「使用 Gemini 改寫指示」，它可能改掉排除投資／政治等規則。
