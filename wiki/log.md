# Log

> 只能追加（append-only）。標題格式：`## [YYYY-MM-DD] <ingest|query|lint|save|slides|schema> | 標題`

## [2026-11-22] schema | 建立 wiki 架構
- 依需求訪談建立 `AGENTS.md`：課程報告用途；三大子主題（溫室氣體減量、土壤碳匯、政策與經濟）；繁中附英文術語；APA 7；批次匯入；Obsidian。
- 建立 `wiki/` 資料夾：papers、methods、regions、topics、analyses。
- 建立 `index.md`、`log.md`、`overview.md`，以及三個主題樞紐頁的骨架。
- 待匯入：`raw/papers/` 已有 6 篇 PDF。

## [2026-11-22] ingest | 批次匯入 6 篇（碳農業政策與經濟）
- 來源 PDF：
  - `Transaction costs of carbon offset projects A comparative study.pdf` → [[Cacho2013]]
  - `Farmers’ Willingness to Participate in a Carbon Sequestration.pdf` → [[Block2024]]
  - `Agricultural Economics - 2019 - Sampson - Peer effects in the diffusion of water‐saving agricultural technologies.pdf` → [[Sampson2019]]
  - `Spatially Mediated Peer Effects in the Adoption of Conservation Agriculture Practices.pdf` → [[Kolady2021]]
  - `Carbon finance as climate adaptation depends on smallholder livelihood contexts in Uganda.pdf` → [[Shin2026]]
  - `Incentive mechanisms of carbon farming contracts A systematic mapping study.pdf` → [[Raina2024]]
- 新增：6 篇論文頁；5 個方法頁（transaction-cost-analysis、discrete-choice-experiment、contingent-valuation、peer-effects-analysis、systematic-mapping）；6 個地區頁（australia、eu-cap、germany、usa、uganda、indonesia）。
- 更新：三個主題樞紐頁、overview、index。
- 記錄的矛盾：同儕效應大小（Sampson2019 對 Kolady2021）、成果導向付款的可行性（Raina2024 對 Block2024）、合約長短（Block2024 對 Cacho2013）。
- ⚠️ 待確認：Shin2026 圖 4 的說明與內文的追加出價比例不一致（200% 對 50%）。
- 缺口：溫室氣體減量只有 1 篇間接涉及；土壤碳缺少自然科學量測文獻；沒有台灣相關文獻。

## [2026-11-22] schema | 刪除子主題「溫室氣體減量」
- 依使用者要求，子主題由三個改為兩個：土壤碳匯、政策與經濟。
- `AGENTS.md`：更新範圍（非 CO₂ 溫室氣體減量技術列為範圍外，涉及碳權、合約或補貼的部分歸入政策與經濟）、資料夾說明、論文頁 topics 列舉、主題頁固定頁數、overview 與 Lint 檢查項目。
- 刪除 `wiki/topics/ghg-mitigation.md`。
- 修改：Raina2024、eu-cap 的 frontmatter（移除 ghg-mitigation）；policy-economics、soil-carbon 的相關主題連結；indonesia 的資料缺口；overview、index。

## [2026-11-22] schema | 新增簡報製作 workflow
- 新增 `.agents/workflows/make-slides.md`：10 步驟的 HTML 簡報製作流程（需求釐清 → 需求摘要🔒 → 準備 → 取材 → 大綱🔒 → 視覺設計 → 逐頁內容 → 生成 → 查核 → 檢視🔒 → 存回）。
- `AGENTS.md`：資料夾結構加入 `.agents/workflows/`、`output/`，並說明 `assets/` 子資料夾；`assets/` 規則改為「永遠不修改，製作 output 成品時可引用，後製一律用 CSS」；新增 §7.4 製作簡報（原 §7.4 Schema 演進改為 §7.5）；log 類型新增 `slides`。

## [2026-11-22] schema | 修正簡報 workflow（依參考流程圖）
- `.agents/workflows/make-slides.md` 改寫：新增覆蓋率關卡（不足即停下）、證據卡（每頁一張、可平行，存於 `output/<slug>/evidence/`）；大綱退回分為「修大綱／補檢索」；忠實度檢查移到渲染前、只退回單頁；渲染檢查獨立、退回逐頁稿；視覺設計併入渲染步驟；節點分為 AI／人工確認／檢查關卡三類。
- `AGENTS.md` §7.4 與 `output/` 規則同步更新。

## [2026-11-22] slides | 低碳農業推廣的機會與困境：證據卡完成（待確認大綱）
- 依 `.agents/workflows/make-slides.md` 執行到步驟 4。建立 `output/slides-low-carbon-promotion/`：`brief.md`、`evidence/02–18.md`。
- 覆蓋率關卡通過；第 18 頁無台灣文獻，限制為只提開放問題。
- 從 PDF 核對後補入 wiki：[[Cacho2013]]（Table 6 最小面積、尚無租賃合約）、[[Kolady2021]]（使用年數 9%／19%、平均面積）、[[Block2024]]（平均耕地）、[[Sampson2019]]（省水 0.10–0.31 與反彈 2.5%、依水源佈局）。
- 下一步：步驟 5 人工確認大綱。

## [2026-11-22] slides | 低碳農業推廣的機會與困境：大綱第二輪（待確認）
- 依使用者意見改為「困境 → 機會 → 策略」三大板塊，共 21 頁；討論題 A／B／C 分別放在三個板塊結尾。
- 證據卡重新編號為 02–20；制度端拆為機會（12）與策略（17）；新增討論題 A（08）。
- 補入 wiki：[[Raina2024]]（遙測與區塊鏈工具、MRV 複雜度壓低付款）。
- 論點與證據檢查：19 張卡的每個論點都有來源列，所引論文皆在 wiki。

## [2026-11-22] slides | 低碳農業推廣的機會與困境：HTML 簡報完成（待檢視）
- 依 workflow 完成步驟 6–9：`output/slides-low-carbon-promotion/draft.md`、`index.html`（21 頁）。
- 忠實度檢查：修正第 04 頁四捨五入、第 20 頁換算標註；其餘通過。
- 渲染檢查：無溢出、翻頁正常、圖片路徑皆存在；圖片實際效果待使用者在本機瀏覽器確認。
- workflow 補充：輸出結構加入 `draft.md`；註明內建瀏覽器無法預覽本機圖片。

## [2026-11-23] slides | 低碳農業推廣的機會與困境：依檢視意見修改（待第二輪檢視）
- 刪除討論題 A（困境篇），全份 20 頁；證據卡與逐頁稿重新編號。
- 視覺：圓形貓咪頭像、封面無貓咪、討論題改為貓咪＋對話框、導覽／總覽／參考文獻改為深色背景。
- 內容：刪除封面「從 6 篇文獻」、參考文獻標題的「（APA 7）」。
- 忠實度與渲染檢查皆重跑通過。

## [2026-11-23] slides | 交件：低碳農業推廣的機會與困境（20 頁）
- 成品：`output/slides-low-carbon-promotion/index.html`；附 `brief.md`、`draft.md`、`evidence/02–19.md`。
- 使用論文：[[Block2024]]、[[Cacho2013]]、[[Kolady2021]]、[[Raina2024]]、[[Sampson2019]]、[[Shin2026]]。
- 檢查：覆蓋率、忠實度、渲染檢查皆通過；使用者兩輪檢視後通過。
- 未執行：存回 `wiki/analyses/`（等使用者說「存起來」）。
