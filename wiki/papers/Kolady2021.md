---
type: paper
title: "Spatially Mediated Peer Effects in the Adoption of Conservation Agriculture Practices"
authors: ["Kolady, D.", "Zhang, W.", "Wang, T.", "Ulrich-Schad, J."]
year: 2021
journal: "Journal of Agricultural and Applied Economics"
doi: "10.1017/aae.2020.24"
source: "raw/papers/Spatially Mediated Peer Effects in the Adoption of Conservation Agriculture Practices.pdf"
topics: [soil-carbon, policy-economics]
methods: [peer-effects-analysis]
regions: [usa]
study_type: empirical
ingested: 2026-11-22
---

# 保育農業採用中的空間同儕效應

**原文標題**：Spatially Mediated Peer Effects in the Adoption of Conservation Agriculture Practices

## 一句話重點
在美國南達科他州東部，保育耕作與多樣化輪作的採用有統計上顯著、但幅度很小的空間同儕效應；**覆蓋作物則沒有**，影響它的主要是組織網絡與農民對環境效益的認知。

## 研究問題
在控制空間異質性（spatial heterogeneity，例如土壤、氣候、作物區）之後，鄰近農民的採用比例是否會影響自己採用三種保育農業（conservation agriculture）措施：保育耕作（conservation tillage）、覆蓋作物（cover crops）、多樣化輪作（diverse crop rotation）？

## 研究地區與資料
[[usa|美國]]南達科他州東部，以玉米–大豆為主的產區。2018 年春季以 FSA 名冊分層隨機抽樣寄發問卷，回收 708 份（回收率 30%），可地理編碼的有 518 份，進入模型的有 435 份（p. 8）。樣本年齡（56.7 歲）與州平均相近；平均經營面積 1,170 英畝（州平均 1,443 英畝）（p. 8）。採用率：保育耕作 66%、覆蓋作物 47%、多樣化輪作 24%（p. 9, Table 1）。

## 方法
[[peer-effects-analysis|同儕效應分析]]：以 15、30、50 英里半徑內鄰近農民的「採用比例」作為同儕變數，並以作物區虛擬變數控制空間異質性。採用多變量 probit 模型（multivariate probit，以 GHK 模擬），同時估計三種措施，允許它們的誤差項相關。

## 關鍵數據與結果
- **保育耕作**：15 英里與 30 英里內採用比例每增加 1 個百分點，採用機率約增加 **0.003**（p. 14–15, Table 4–5）。
- **多樣化輪作**：只有 30 英里半徑顯著（邊際效果 0.004）。距乙醇廠每遠 1 英里，採用機率增加 0.006，影響比同儕效應更大（p. 14）。
- **覆蓋作物**：同儕效應不顯著。組織網絡指數（推廣單位、NRCS、農民團體）每增加 1 單位，採用機率增加 **0.20**（p. 16）。
- 三種措施中，對環境效益的認知都有很強的正向影響，例如保育耕作的邊際效果為 1.07。
- 加入同儕變數後，其他變數（作物區、教育、面積）的係數和顯著性都改變，顯示**省略同儕效應會造成估計偏誤**。
- 覆蓋作物採用者中，47% 使用不到 3 年，屬於較新的措施；保育耕作只有 9%、多樣化輪作 19%（p. 14–15）。

## 結論
政策應依措施分開設計：
- 保育耕作與多樣化輪作：可以利用同儕網絡，在示範農場辦田間日；高採用率地區減少補貼，把資源轉往低採用率地區。
- 覆蓋作物：應透過組織網絡改變認知，並持續提供成本分攤補貼，以降低獲利風險。
- 玉米乙醇政策對作物多樣化不利。

## 限制與可質疑之處
- 橫斷面資料，無法觀察同儕效應隨時間的變化。
- 缺少田區層級的土壤與作物組合變數。
- 同儕群組的定義（半徑）會影響結果；50 英里半徑下，覆蓋作物甚至出現負向效果。
- 以郵政信箱為地址的回覆無法地理編碼，因此被排除。

## 與其他論文的關係
- 與 [[Sampson2019]] 方法相近，結論卻不同：Sampson2019 在 1 km 尺度發現明顯的同儕效應；本文因為大型農場分散，只能用 15–30 英里尺度，效果很小。
- 補充 [[soil-carbon|土壤碳匯]]：保育耕作和覆蓋作物是土壤固碳的核心措施，本文說明它們的擴散機制不同。
- 與 [[Block2024]] 呼應：兩篇都發現農民對環境效益的認知或動機，是參與與採用的重要驅力。
- 與 [[Shin2026]] 呼應：烏干達的質性資料也顯示，觀察鄰居成功與合作社組織網絡都會影響參與。

## 報告可用的引用句
- 美國南達科他州的研究顯示，鄰近農民的採用比例對保育耕作與多樣化輪作只有小幅的正向影響，對覆蓋作物則沒有顯著影響（Kolady et al., 2021）。
- 覆蓋作物的推廣較依賴推廣單位與農民組織等網絡，而不是鄰里示範（Kolady et al., 2021）。

## 書目（APA 7）
Kolady, D., Zhang, W., Wang, T., & Ulrich-Schad, J. (2021). Spatially mediated peer effects in the adoption of conservation agriculture practices. *Journal of Agricultural and Applied Economics*, *53*(1), 1–20. https://doi.org/10.1017/aae.2020.24
