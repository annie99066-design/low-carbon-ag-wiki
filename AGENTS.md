# AGENTS.md — 低碳／永續農業論文 LLM Wiki

本檔案是這個知識庫的「規則書」。任何 LLM agent（Claude Code、Codex 等）在這個資料夾工作前，都必須先讀完本檔，並嚴格遵守。
人類使用者負責：挑選論文、提問、決定重點。Agent 負責：閱讀、摘要、交叉連結、維護一致性與記錄。

---

## 1. 專案目的與範圍

- **用途**：支援課程報告與簡報——快速查到「哪篇論文、用什麼方法、在哪裡、得到什麼數字」，並能直接引用（APA 7）。
- **兩大聚焦子主題**（所有內容都應盡量掛到其中至少一個）：
  1. **土壤碳匯**（soil carbon sequestration）：土壤有機碳（SOC）、生物炭、覆蓋作物、不整地等
  2. **政策與經濟**（policy & economics）：碳權／碳信用、碳費、補貼、合約誘因、交易成本、農民採用行為
- 範圍外的內容（例如純作物育種，以及稻田甲烷、氮肥 N₂O、畜牧排放等非 CO₂ 溫室氣體減量技術）若出現在論文中，只在論文頁簡短記錄，不另建頁面。若這些內容涉及碳權、合約或補貼，歸入「政策與經濟」。

---

## 2. 資料夾結構

```
W10 LLM wiki/
├── AGENTS.md              ← 本檔（規則書）
├── .agents/
│   └── workflows/         ← 可重複使用的工作流程（例如 make-slides.md）
├── raw/                   ← 原始來源層：唯讀，不可修改、改名、移動或刪除
│   └── papers/            ← 論文 PDF 放這裡；匯入後 PDF 仍留在原地
├── assets/                ← 使用者的簡報模板、底圖與角色圖；唯讀，只可引用
│   ├── template/          ← 簡報模板與底圖（bg*.png、底圖*.png）
│   └── icons/             ← 角色圖（1.jpg 圍巾貓、2.jpg 蜜蜂貓）
├── output/                ← 由 wiki 產生的成品，例如 HTML 簡報；一個成品一個子資料夾
└── wiki/                  ← Agent 全權維護的知識層
    ├── index.md           ← 全站目錄（每頁一行摘要）
    ├── log.md             ← 時間序紀錄（append-only）
    ├── overview.md        ← 兩大子主題的總覽與目前綜合觀點
    ├── papers/            ← 一篇論文一頁
    ├── methods/           ← 方法／指標頁
    ├── regions/           ← 地區／政策頁
    ├── topics/            ← 兩大子主題的樞紐頁
    └── analyses/          ← 使用者要求「存起來」的問答分析
```

### 鐵則
- **`raw/` 永遠唯讀。** 包括 `raw/papers/README.md`。
- **`assets/` 不屬於 wiki，且永遠不修改。** 製作 `output/` 成品（例如簡報）時可以讀取並以相對路徑引用；需要後製（濾鏡、透明度、色調）時一律用 CSS 處理，不修改原檔，也不另存處理後的圖檔。其他情況除非使用者明確要求，否則不讀取。
- **`output/`** 存放由 wiki 產生的成品。成品的內容只能來自 wiki；每個成品子資料夾附一份 `brief.md`（需求摘要與大綱）；簡報另附 `evidence/` 證據卡，一頁一張。
- `wiki/` 內所有檔案由 agent 撰寫，使用者原則上不手動編輯；若使用者改過，以使用者版本為準並保留。

---

## 3. 語言與寫作慣例

- **繁體中文為主，專業術語第一次出現時附英文（與縮寫）**，例如：土壤有機碳（soil organic carbon, SOC）、生命週期評估（life cycle assessment, LCA）、願付價格（willingness to pay, WTP）。同一頁之後可直接用縮寫。
- 數字保留原文單位，例如 `t CO₂e ha⁻¹ yr⁻¹`、`Mg C ha⁻¹`、`USD/t CO₂e`。不要自行換算；需要換算時，標明「（換算）」並附公式。
- 區分**論文作者的主張**和 **agent 的推論**：agent 的推論一律以 `> 💡 Agent 註：` 開頭的引言區塊呈現。
- 不確定或 PDF 讀不清楚的內容，標記 `⚠️ 待確認`，不要猜。
- 檔名：英數字與連字號（`-`），不用空白和中文，以確保 Obsidian 連結穩定。頁面標題（H1 與 frontmatter `title`）可用中文。

---

## 4. 連結與引用

### 4.1 Wiki 內部連結（Obsidian）
- 使用 `[[檔名]]` 或 `[[檔名|顯示文字]]`，不加 `.md`。
- 每頁至少要有 **2 個向外連結**（通常是：所屬 topic + 相關 method/region/paper）。
- 提到 wiki 中已有頁面的概念時就連結；提到值得建頁但還沒有頁面的概念時，也可以先寫 `[[未建頁面]]`（Obsidian 會顯示為未解析連結，Lint 時再處理）。

### 4.2 APA 7 引用
- **文中引用**：`（Sampson & Perry, 2019）`、`（Smith et al., 2023）`，並連結論文頁：`[[Sampson2019|Sampson & Perry, 2019]]`。
- **論文頁**的「書目」區塊放完整 APA 7 參考文獻（含 DOI，格式 `https://doi.org/...`）。
- **topic、method、region、analysis 頁**的最下方要有 `## 參考文獻`，列出該頁引用過的所有論文（APA 7，依第一作者姓氏字母排序）。
- 書目資訊以 PDF 首頁／版權頁為準；缺漏的欄位標 `⚠️ 待確認`，不要自行編造 DOI 或頁碼。

### 4.3 論文 ID（檔名）規則
- 格式：`第一作者姓氏 + 年份`，例如 `Sampson2019`。
- 同一作者同一年有多篇時，加 `a`、`b`：`Smith2023a`、`Smith2023b`。
- 第一作者是機構時用簡寫，例如 `FAO2021`、`IPCC2019`。

---

## 5. 頁面類型與模板

所有頁面都以 YAML frontmatter 開頭（方便 Obsidian Dataview 查詢）。日期格式一律為 `YYYY-MM-DD`。

### 5.1 論文頁 `wiki/papers/<PaperID>.md`

篇幅：**正文約 300–600 字**（不含 frontmatter 與書目）。

```markdown
---
type: paper
title: "論文原文標題"
authors: ["Sampson, G. S.", "Perry, E. D."]
year: 2019
journal: "Agricultural Economics"
doi: "10.xxxx/xxxx"
source: "raw/papers/<原始 PDF 檔名>.pdf"
topics: [policy-economics]          # soil-carbon | policy-economics
methods: [spatial-econometrics]     # 對應 wiki/methods/ 的檔名
regions: [usa-kansas]               # 對應 wiki/regions/ 的檔名
study_type: empirical               # empirical | review | modelling | experiment | meta-analysis | case-study
ingested: 2026-11-22
---

# 中文意譯標題

**原文標題**：…

## 一句話重點
（一句話說明這篇論文的核心發現）

## 研究問題
## 研究地區與資料
## 方法
## 關鍵數據與結果
（條列；保留原文數字與單位，附頁碼或表號，例如「(p. 7, Table 3)」）
## 結論
## 限制與可質疑之處
## 與其他論文的關係
（呼應、矛盾或補充哪些論文；用 [[連結]]）
## 報告可用的引用句
（1–3 句可以直接寫進報告的中文敘述，附 APA 文中引用）

## 書目（APA 7）
Sampson, G. S., & Perry, E. D. (2019). Title. *Journal*, *vol*(issue), pages. https://doi.org/...
```

### 5.2 方法／指標頁 `wiki/methods/<method-name>.md`

例如：`lca.md`、`static-chamber.md`、`emission-factor.md`、`choice-experiment.md`、`spatial-econometrics.md`、`systematic-mapping.md`。

```markdown
---
type: method
title: "方法中文名（English, 縮寫）"
category: measurement            # measurement | modelling | economic-valuation | statistical | review
topics: [...]
papers: [PaperID, ...]
updated: 2026-11-22
---

# 方法中文名（English, 縮寫）

## 定義
## 適用情境
## 操作步驟／關鍵參數
## 優點與限制
## 本 wiki 中使用此方法的論文
| 論文 | 應用對象 | 主要參數／設定 | 結果摘要 |
|---|---|---|---|
## 相關方法
## 參考文獻
```

### 5.3 地區／政策頁 `wiki/regions/<region-or-policy>.md`

例如：`taiwan.md`、`eu-cap.md`、`usa-kansas.md`、`sub-saharan-africa.md`、`china.md`。地區與該地區的政策寫在同一頁；跨國政策工具（例如自願性碳市場）則放在 topics 頁討論。

```markdown
---
type: region
title: "地區或政策名稱"
scope: country                   # country | subnational | supranational | policy-programme
topics: [...]
papers: [PaperID, ...]
updated: 2026-11-22
---

# 地區或政策名稱

## 背景（農業結構、排放概況）
## 相關政策與制度
## 研究發現彙整
（依論文條列，附 APA 引用）
## 與其他地區的比較
## 資料缺口
## 參考文獻
```

### 5.4 主題樞紐頁 `wiki/topics/<topic>.md`

固定兩頁：`soil-carbon.md`、`policy-economics.md`。

```markdown
---
type: topic
title: "主題名稱"
papers: [PaperID, ...]
updated: 2026-11-22
---

# 主題名稱

## 主題概述
## 目前的共識
## 爭議與矛盾
（不同論文說法不一致的地方，並列雙方證據）
## 子議題
（連到 methods / regions / papers）
## 研究缺口與值得找的文獻
## 參考文獻
```

### 5.5 分析頁 `wiki/analyses/<YYYY-MM-DD>-<short-slug>.md`

**只有在使用者說「存起來」或類似指示時才建立。**

```markdown
---
type: analysis
title: "問題或分析標題"
question: "使用者原本的問題"
papers: [PaperID, ...]
created: 2026-11-22
---

# 標題

（回答內容；可包含比較表）

## 參考文獻
```

---

## 6. 特殊檔案

### `wiki/index.md`
- 依類別分區：主題、論文、方法／指標、地區／政策、分析。
- 每頁一行：`- [[檔名|標題]] — 一句話摘要（論文加上年份與 study_type）`。
- 每次匯入或新增頁面都要更新。

### `wiki/log.md`
- **只能追加（append-only）**，新的紀錄加在檔案最後。
- 每筆紀錄的標題格式固定：`## [YYYY-MM-DD] <ingest|query|lint|save|slides|schema> | 標題`
- 內容條列：處理了哪些來源、新增／修改了哪些頁面、發現的矛盾或待辦。
- `ingest` 紀錄必須寫出原始 PDF 檔名，作為「已匯入」的依據。

### `wiki/overview.md`
- 用 1–2 頁的篇幅，總結兩大子主題的整體圖像與目前的綜合觀點。
- 每次批次匯入後檢視是否需要修訂，並在頁首的 `updated` 更新日期。

---

## 7. 工作流程

### 7.1 Ingest（批次匯入）— 使用者說「匯入」「ingest」「處理新論文」時

1. **找出新論文**：列出 `raw/papers/*.pdf`，與 `wiki/papers/*.md` frontmatter 的 `source` 欄位比對，沒有對應論文頁的就是新論文。PDF 留在原地，不移動。
2. **逐篇閱讀**：完整讀完每篇 PDF（長文分段讀）。記下書目、方法、地區、關鍵數字（附頁碼／表號）。
3. **建立論文頁**：依 §5.1 模板。
4. **更新相關頁面**：
   - 對應的 `topics/` 樞紐頁（加入論文、更新共識與爭議）
   - 用到的 `methods/` 頁（沒有就新建）
   - 涉及的 `regions/` 頁（沒有就新建）
   - 有呼應或矛盾關係的其他論文頁的「與其他論文的關係」區塊
5. **處理矛盾**：新資料與既有內容衝突時，**不要覆蓋舊說法**，在兩邊頁面與 topic 頁的「爭議與矛盾」區塊並列，並註明來源。
6. **更新 `index.md`、`overview.md`**，並在 `log.md` 追加一筆 `ingest` 紀錄。
7. **批次結束後回報使用者**（全部處理完才回報，中途不停下來詢問，除非 PDF 無法讀取）：
   - 新增的頁面清單、修改的頁面清單
   - 每篇論文的一句話重點
   - 發現的矛盾與 `⚠️ 待確認` 項目
   - 建議接下來可以補充的文獻方向

### 7.2 Query（提問）

1. 先讀 `wiki/index.md` 找相關頁面，再深入閱讀相關頁面；必要時回到 `raw/papers/` 的 PDF 核對細節。
2. 以繁體中文回答，附 APA 7 文中引用與 `[[連結]]`；比較型問題優先用表格呈現。
3. 明確區分「wiki 中有證據支持的」和「agent 的推論或 wiki 沒有涵蓋的」。
4. **不主動存檔。** 使用者說「存起來」時，依 §5.5 建立分析頁，更新 `index.md`，並在 `log.md` 追加 `save` 紀錄。
5. 一般提問不需要寫進 log。

### 7.3 Lint（健檢）— 使用者說「健檢」「lint」時

檢查並回報以下項目，再詢問使用者要修哪些（**簡單的機械性修正**，例如補 index 條目、修壞掉的連結，可以直接修）：

- [ ] 頁面之間的矛盾說法，以及尚未記錄到「爭議與矛盾」區塊的矛盾
- [ ] 孤立頁面（沒有任何其他頁面連進來）
- [ ] 未解析連結 `[[...]]`（被提到但還沒有頁面），判斷是否值得建頁
- [ ] `raw/papers/` 中尚未匯入的 PDF
- [ ] frontmatter 缺欄位、`papers` 清單與實際引用不一致
- [ ] `index.md` 漏列或多列的頁面
- [ ] 參考文獻缺漏，或 APA 格式錯誤
- [ ] 殘留的 `⚠️ 待確認`
- [ ] 兩大子主題中證據薄弱的地方，以及建議補充的文獻或搜尋關鍵字

完成後在 `log.md` 追加一筆 `lint` 紀錄。

### 7.4 製作簡報 — 使用者說「做簡報」「製作 HTML 簡報」「slides」時
- 依照 `.agents/workflows/make-slides.md` 執行。
- 流程：需求 → 檢索 wiki → **覆蓋率關卡** → 證據卡（每頁一張，可平行）→ 大綱 → 人工確認 → 逐頁稿 → **忠實度檢查** → 渲染 HTML → **渲染檢查** → 使用者檢視 → 交件。
- 重點：
  - 需求訪談一次一題；需求摘要、大綱與成品檢視都要等使用者確認。
  - 覆蓋率不足就**停下**回報，不可寫出沒有證據的頁面。
  - 忠實度檢查在渲染**之前**，逐頁比對證據卡；不通過只退回那一頁。
  - 渲染檢查只看畫面（路徑、可讀性、翻頁）；內容或版面問題退回逐頁稿。
  - 使用者說「存起來」時，才把大綱存成 `wiki/analyses/` 的分析頁。
- 成品放在 `output/<slug>/`（`brief.md`、`evidence/`、`index.html`），並在 `wiki/log.md` 追加一筆 `slides` 紀錄。

### 7.5 Schema 演進
- 使用者要求修改規則時，更新本檔並在 `log.md` 追加 `schema` 紀錄。
- Agent 發現規則不合用時，可以**提出**修改建議，但要經使用者同意才修改本檔。

---

## 8. 品質守則（摘要）

1. 不編造：書目、數字、DOI 一律以 PDF 為準；不確定就標 `⚠️ 待確認`。
2. 數字附出處（頁碼或表號）。
3. 矛盾並列，不覆蓋。
4. 每次修改都同步更新 index 與 log。
5. `raw/` 和 `assets/` 永遠不修改；`assets/` 只在製作 `output/` 成品時引用。
