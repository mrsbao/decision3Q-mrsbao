# decision3Q-mrsbao｜決策三問思考教練

決策三問思考教練：基於陳伶志老師在天下學習〈啟動 AI 外掛大腦 〉課程核心與寶太太觀課心得，實作「寶太太版本的決策三問思考教練」
不直接給答案，而是透過「釐清目標、評估代價、反思風險」三大視角進行深度提問，幫助你擺脫思維盲點，做出條理分明、高品質的關鍵決策。一個 AI 思考教練：用蘇格拉底式提問，帶你以「決策三問」（影響規模、風險與可逆性、隱性脈絡）想清楚決策（如：公司發展、團隊方向、專案與產品策略與個人發展等）。

**支援 Claude、ChatGPT、Gemini。**

- 不直接給答案，而是一次問 1～2 個關鍵問題，讓你自己做決定
- 結尾整理成「決策評估矩陣」與最小可行驗證（MVP）
- **不處理投資理財與政治相關議題**

## 目錄結構

```
decision3Q-mrsbao/
├── README.md
├── LICENSE
├── skills/
│   └── decision3q-mrsbao/                 # Claude Skill（Agent Skills 格式）
│       ├── SKILL.md
│       └── references/
│           ├── knowledge-base.md          # 決策三問整理後的知識文件
│           └── decision-matrix-template.md
└── platforms/
    ├── system-prompt.md                   # ChatGPT／Gemini 共用指令
    ├── chatgpt/README.md                  # 建立自訂 GPT 步驟
    └── gemini/README.md                   # 建立 Gem 步驟
```

## 下載

點本頁右上角 **Code → Download ZIP**，或：

```bash
git clone https://github.com/mrsbao/decision3Q-mrsbao.git
```

## 依平台安裝

| 平台 | 方式 | 說明 |
|---|---|---|
| Claude.ai／Claude 桌面版（含 Cowork） | 上傳 Skill | 見下方 |
| Claude Code | 複製資料夾 | 見下方 |
| ChatGPT | 建立自訂 GPT | [platforms/chatgpt](platforms/chatgpt/README.md) |
| Gemini | 建立 Gem | [platforms/gemini](platforms/gemini/README.md) |
| 其他支援 Agent Skills 格式的工具（如 OpenAI Codex、Gemini CLI） | 複製資料夾 | 把 `skills/decision3q-mrsbao` 放進該工具的 skills 目錄，路徑以各工具官方文件為準 |

### Claude.ai／Claude 桌面版（含 Cowork）
1. 到本 repo 的 **[Releases](https://github.com/mrsbao/decision3Q-mrsbao/releases)** 下載 `decision3q-mrsbao-skill.zip`。
   - 或自行把 `skills/decision3q-mrsbao` 資料夾壓縮成 zip（zip 第一層要是 `decision3q-mrsbao/`，裡面有 `SKILL.md`）。
2. 進入 **Settings → Capabilities → Skills**（需開啟 Code execution），點 **Upload skill**，選擇該 zip。
3. 在對話中說「用決策三問幫我想一下要不要轉職」即可觸發。

### Claude Code
```bash
cp -r skills/decision3q-mrsbao ~/.claude/skills/              # 個人全域
cp -r skills/decision3q-mrsbao <你的專案>/.claude/skills/      # 單一專案
```

## 放入知識庫（重要）

教練會優先依據 `skills/decision3q-mrsbao/references/knowledge-base.md` 引用講者案例與檢查清單。
`knowledge-base.md` 是**整理過的知識文件**（理論重點、三問定義、案例摘要、檢查清單），不是逐字稿原文。請依檔案內的章節格式整理後填入：Claude 版重新打包上傳；ChatGPT／Gemini 版在 Knowledge 區上傳這個檔案。

> 整理時請用自己的話摘要，不要大段照抄原始講稿；若涉及他人著作，公開分享前請先取得授權。

## 修改指令時

Claude 版的指令在 `SKILL.md`，ChatGPT／Gemini 版在 `platforms/system-prompt.md`。兩份內容相同，改一份時請同步改另一份。

## 使用範例

> 我在考慮從現在的公司跳到新創當產品經理，但不確定時機對不對。

教練會先確認你的困境，接著依序引導三問，每次回應結尾附上 **【教練思考提問】**。

## 關於名稱

專案名稱為 **decision3Q-mrsbao**。Skill 規格只接受小寫英文、數字與連字號，所以 `SKILL.md` 的 `name` 與資料夾名稱使用小寫的 `decision3q-mrsbao`，兩者指的是同一個 skill。

## 授權

MIT License，詳見 [LICENSE](LICENSE)。
