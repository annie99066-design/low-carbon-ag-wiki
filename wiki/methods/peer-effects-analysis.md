---
type: method
title: "空間同儕效應分析（spatial peer effects analysis）"
category: statistical
topics: [policy-economics, soil-carbon]
papers: [Sampson2019, Kolady2021]
updated: 2026-11-22
---

# 空間同儕效應分析（spatial peer effects analysis）

## 定義
估計「鄰近他人的採用行為」對自己採用新技術或新做法的因果影響。核心難題是 Manski（1993）的**反射問題**（reflection problem）：鄰居行為相似，可能來自真正的同儕影響，也可能只是因為共享環境，也就是脈絡效應或空間異質性。

## 適用情境
- 解釋農業技術（灌溉、保育耕作、覆蓋作物）的擴散。
- 設計補貼與推廣策略，例如把資源投在網絡中心，或在示範農場辦田間日。

## 操作步驟／關鍵參數
1. **定義同儕群組**：以距離環帶（Sampson2019：0–1、1–2、2–5、5–10 km）或半徑（Kolady2021：15、30、50 英里）定義。
2. **同儕變數**：上一期鄰近採用者的累積數（installed base，可避免同時性問題），或鄰近採用比例。
3. **控制空間異質性**：郡、農業區、作物區的固定效果，或年份×地區固定效果。
4. **模型**：logit（離散時間風險模型）、線性機率模型；若同時分析多種做法，可用多變量 probit。
5. **反事實模擬**：把同儕變數設為 0，估計同儕效應對總採用量的貢獻。

## 優點與限制
- 優點：可量化「社會乘數」，直接轉成空間化的政策建議。
- 限制：空間距離只是社會網絡的代理變數，會有測量誤差，使估計值偏向零；群組半徑的設定會影響結果；未觀察的時空因素（例如推廣強度）可能高估效果。

## 本 wiki 中使用此方法的論文
| 論文 | 應用對象 | 主要參數／設定 | 結果摘要 |
|---|---|---|---|
| [[Sampson2019]] | 堪薩斯 LEPA 節水灌溉，1990–2014 | 18,486 個水權；4 個距離環帶；logit + 固定效果 | 1 km 內每多 1 位採用者 +0.26 個百分點；若無同儕效應，每年採用約少 10% |
| [[Kolady2021]] | 南達科他州保育耕作、覆蓋作物、輪作 | N=435；15/30 英里；多變量 probit | 保育耕作 +0.003／百分點；覆蓋作物不顯著 |

> 💡 Agent 註：兩篇結果的差異可能來自尺度。Sampson2019 有精細的水權座標（約 1 km），Kolady2021 因農場大且分散，只能用 15–30 英里，同儕訊號可能被稀釋。

## 相關方法
- [[discrete-choice-experiment|離散選擇實驗]]：從陳述偏好看動機；本方法則從顯示偏好（實際採用）看擴散。

## 參考文獻
Kolady, D., Zhang, W., Wang, T., & Ulrich-Schad, J. (2021). Spatially mediated peer effects in the adoption of conservation agriculture practices. *Journal of Agricultural and Applied Economics*, *53*(1), 1–20. https://doi.org/10.1017/aae.2020.24

Sampson, G. S., & Perry, E. D. (2019). Peer effects in the diffusion of water-saving agricultural technologies. *Agricultural Economics*, *50*(6), 693–706. https://doi.org/10.1111/agec.12518
