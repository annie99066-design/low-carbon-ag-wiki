---
type: method
title: "交易成本分析（transaction cost analysis）"
category: economic-valuation
topics: [policy-economics]
papers: [Cacho2013]
updated: 2026-11-22
---

# 交易成本分析（transaction cost analysis）

## 定義
交易成本（transaction costs）是把減碳成果轉成可交易商品的過程中，除了減量成本（abatement cost，即機會成本）以外的所有成本。例如搜尋與協商、核准、專案管理、監測，以及執行與保險（[[Cacho2013|Cacho et al., 2013]]）。

## 適用情境
- 評估碳抵換、生態系服務付費（payment for ecosystem services, PES）或碳農業專案能否成立。
- 比較不同合約設計（購買型或租賃型、個別或集體）的成本結構。

## 操作步驟／關鍵參數
以 [[Cacho2013]] 的模型為例：
1. 把交易成本依單位分類：一次性固定成本（$）、每年固定成本（$/y）、依農戶計（$/farm）、依面積計（$/ha/y）、依碳信用計（credit/y）。
2. 分別列出買方（彙整者）與賣方（農民）的成本。
3. 設定買賣雙方都可行的條件（碳收入 − 減量成本 ≥ 交易成本），求出**專案可行性邊界**（project feasibility frontier, PFF），也就是各碳價下的最小可行面積或合約數。
4. 以彈性分析與蒙地卡羅模擬檢驗哪一類成本最關鍵。

## 優點與限制
- 優點：能找出「規模經濟」的門檻與最關鍵的成本項目，可以直接轉成政策建議。
- 限制：參數多半來自二手資料；通常假設農戶同質。

## 本 wiki 中使用此方法的論文
| 論文 | 應用對象 | 主要參數／設定 | 結果摘要 |
|---|---|---|---|
| [[Cacho2013]] | 印尼小農農林複合、澳洲家庭農場造林 | 15 項交易成本；CER 價格 14–50 USD | 年度固定成本彈性 0.89–0.95；租賃型合約的最小規模可達購買型的 2 倍 |

> 💡 Agent 註：[[Raina2024]] 與 [[Shin2026]] 雖然沒有用這套模型，但都提供了交易成本的描述性證據，例如 MRV 占碳收入的 20–40%。

## 相關方法
- [[contingent-valuation|條件評估法]]、[[discrete-choice-experiment|離散選擇實驗]]：從農民端估計受償意願，可與交易成本模型互補。

## 參考文獻
Cacho, O. J., Lipper, L., & Moss, J. (2013). Transaction costs of carbon offset projects: A comparative study. *Ecological Economics*, *88*, 232–243. https://doi.org/10.1016/j.ecolecon.2012.12.008

Raina, N., Zavalloni, M., & Viaggi, D. (2024). Incentive mechanisms of carbon farming contracts: A systematic mapping study. *Journal of Environmental Management*, *352*, Article 120126. https://doi.org/10.1016/j.jenvman.2024.120126

Shin, S., Okello, O., Otim, J., Lehmann, J., Fiorella, K., Waldman, K., & Liao, C. (2026). Carbon finance as climate adaptation depends on smallholder livelihood contexts in Uganda. *Communications Sustainability*, *1*, Article 145. https://doi.org/10.1038/s44458-026-00151-6
