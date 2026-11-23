---
type: method
title: "離散選擇實驗（discrete choice experiment, DCE）"
category: economic-valuation
topics: [policy-economics, soil-carbon]
papers: [Block2024]
updated: 2026-11-22
---

# 離散選擇實驗（discrete choice experiment, DCE）

## 定義
一種陳述性偏好（stated preference）方法：讓受訪者在多組由不同「屬性 × 水準」組成的假設方案中做選擇，藉此推估各屬性的效用，以及受償意願（willingness to accept, WTA）或願付價格（willingness to pay, WTP）。

## 適用情境
- 方案還沒上市或參與者很少，無法觀察真實行為時。例如碳農業計畫的設計，見 [[Block2024]]。
- 想知道「哪一項合約條款最影響參與」，以及「要多付多少錢才能抵銷不受歡迎的條款」。

## 操作步驟／關鍵參數
以 [[Block2024]] 為例：
1. 依現有計畫、專家意見與前測（15 位農民）選定屬性與水準：基準值類型、檢驗時點、最低增量、基本獎金、額外獎金／回收機制。
2. 以 D-efficient 貝氏設計（Ngene）把 46,656 種組合縮減為 12 組選擇題，每組都附「不參加」選項。
3. 以混合 logit（mixed logit）估計，處理偏好異質性，並加入交互項（動機、補貼導向、畜牧密度、面積、風險態度）。
4. 以 WTA = −β_屬性 / β_價格 計算受償意願，並用 Krinsky-Robb 法求信賴區間。

## 優點與限制
- 優點：可以拆解每一項合約條款的貨幣價值；設計彈性大。
- 限制：屬於假設情境，可能有假設性偏誤；受訪者負擔重，例如平均 34 分鐘；農民樣本通常很小（N≈50–170）。

## 本 wiki 中使用此方法的論文
| 論文 | 應用對象 | 主要參數／設定 | 結果摘要 |
|---|---|---|---|
| [[Block2024]] | 德國農民的腐植質計畫 | N=150；5 個屬性；12 組選擇題；mixed logit | 最低增量每提高 0.1%，獎金須多 323.76 €/ha；回收機制須多付 18.10 €/ha |

## 相關方法
- [[contingent-valuation|條件評估法]]：同樣估計受償意願，但只問「接不接受某個金額」，不拆解屬性。

## 參考文獻
Block, J. B., Danne, M., & Mußhoff, O. (2024). Farmers' willingness to participate in a carbon sequestration program – A discrete choice experiment. *Environmental Management*, *74*, 332–349. https://doi.org/10.1007/s00267-024-01963-9
