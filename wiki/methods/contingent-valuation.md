---
type: method
title: "條件評估法：雙界二分選擇（contingent valuation, DBDC）"
category: economic-valuation
topics: [policy-economics]
papers: [Shin2026]
updated: 2026-11-22
---

# 條件評估法：雙界二分選擇（contingent valuation, DBDC）

## 定義
條件評估法（contingent valuation method, CVM）直接詢問受訪者是否接受某個金額。雙界二分選擇（double-bounded dichotomous choice, DBDC）會連續問兩次：先給一個起始出價；接受就降價再問，拒絕就加價再問。受訪者的真實受償意願（WTA）因此被夾在一個較窄的區間內。

## 適用情境
- 估計參與生態系服務付費（PES）或碳專案所需的最低補償。
- 受訪者教育程度不高、無法負擔複雜的選擇實驗時，題目較簡單。

## 操作步驟／關鍵參數
以 [[Shin2026]] 為例：
1. 以焦點團體決定在地可理解的出價範圍：起始出價為每英畝每年 20,000–200,000 UGX，隨機指派。
2. 接受起始出價就問 50% 的金額，拒絕就問 200% 的金額。
3. 以第二次出價的接受機率 × 金額加總，直接計算平均 WTA（無母數）。
4. 以雙變量 probit（bivariate probit）分析兩次回答的決定因素。
5. 做起始出價敏感度診斷：共變數平衡、同額一致性、區間設限的等分配檢定。

## 優點與限制
- 優點：題目簡單；比單界設計更有統計效率。
- 限制：**起始點偏誤**（starting-point bias／錨定效應）。Shin2026 的區間設限檢定拒絕了「各起始出價組有共同的 WTA 分配」（χ²(4)=27.62, p<0.01），所以 WTA 只能當作情境特定的基準。

## 本 wiki 中使用此方法的論文
| 論文 | 應用對象 | 主要參數／設定 | 結果摘要 |
|---|---|---|---|
| [[Shin2026]] | 烏干達小農的農林複合碳專案 | n≈296；5 個起始出價；DBDC + 雙變量 probit | WTA 約 54 USD/ha/年；補償每多 1 美元，參與機率 +1% |

## 相關方法
- [[discrete-choice-experiment|離散選擇實驗]]：可以同時評估多個合約屬性。
- 質性方法（訪談、焦點團體）：Shin2026 以永續生計架構（SLF）結合兩者，屬於混合方法。

## 參考文獻
Shin, S., Okello, O., Otim, J., Lehmann, J., Fiorella, K., Waldman, K., & Liao, C. (2026). Carbon finance as climate adaptation depends on smallholder livelihood contexts in Uganda. *Communications Sustainability*, *1*, Article 145. https://doi.org/10.1038/s44458-026-00151-6
