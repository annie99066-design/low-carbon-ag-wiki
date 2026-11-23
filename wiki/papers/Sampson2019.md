---
type: paper
title: "Peer effects in the diffusion of water-saving agricultural technologies"
authors: ["Sampson, G. S.", "Perry, E. D."]
year: 2019
journal: "Agricultural Economics"
doi: "10.1111/agec.12518"
source: "raw/papers/Agricultural Economics - 2019 - Sampson - Peer effects in the diffusion of water‐saving agricultural technologies.pdf"
topics: [policy-economics]
methods: [peer-effects-analysis]
regions: [usa]
study_type: empirical
ingested: 2026-11-22
---

# 節水農業技術擴散中的同儕效應

**原文標題**：Peer effects in the diffusion of water-saving agricultural technologies

## 一句話重點
美國堪薩斯州灌溉戶採用節水灌溉技術 LEPA 時，有明顯且隨距離遞減的同儕效應（peer effects）；如果沒有同儕效應，每年的採用數約少 10%。

## 研究問題
鄰近農戶已採用低能耗精準施灌（low energy precise application, LEPA），是否會提高自己採用的機率？影響範圍有多遠？

## 研究地區與資料
[[usa|美國]]堪薩斯州 High Plains 含水層地區，1990–2014 年共 25 年。資料取自州政府水權資料庫（WIMAS），以水權為分析單位，共 18,486 個水權、約 159,000 筆觀測值，並串接土壤、水文、氣候、能源價格與 EQIP 補貼資料（p. 699）。

> 💡 Agent 註：本文主題是節水，不是減碳。與低碳農業的關聯在於：LEPA 把水壓從 75 psi 降到 18 psi，可以省下抽水能源（p. 695），而且研究方法可直接套用到低碳技術的擴散分析。

## 方法
[[peer-effects-analysis|同儕效應分析]]：以「已安裝基數」（installed base，即上一期鄰近採用者的累積數）衡量同儕影響，依 0–1、1–2、2–5、5–10 km 四個同心圓分開估計。模型為 logit（離散時間風險模型），控制郡、農業區×年份等固定效果；另以水權固定效果的線性機率模型做穩健性檢驗。

## 關鍵數據與結果
- 1 km 內每多 1 個 LEPA 採用者，自己採用的機率約增加 **0.26 個百分點**（勝算比 1.043）（p. 701, Table 2, col. 4）。
- 1–2 km 的效果約為 0–1 km 的一半；2–5 km 不顯著；5–10 km 微弱，效果只有 1 km 內的約十分之一。
- 能源價格每上升 1 USD/mmbtu（約 10%），採用機率增加約 0.20 個百分點（p. 702）。
- 反事實模擬：沒有同儕效應時，2001–2014 年**每年約少 1,000–1,600 件安裝（約 10%）**（p. 703, Fig. 3）。
- 前一年種植耗水作物、灌溉面積較大、水權較資深、已使用中心樞軸（center pivot）的農戶較容易採用。
- 1997 年 EQIP 成本分攤補貼上路後，採用曲線出現明顯轉折（p. 695, Fig. 1）。

## 結論
補貼與推廣資源如果投放在農戶網絡的**中心**而不是邊緣，可以藉由同儕效應放大效果；也可以依水源（含水層、地表水）的空間組織來佈局（p. 704）。但作者提醒：LEPA 可能有**反彈效應**（rebound effect）。依 Hornbaker & Mapp（1988）的參數，同儕效應帶動的採用可省水 0.10–0.31 百萬英畝·呎；但依 Pfeiffer & Lin（2014a）的估計，採用後每英畝多用 2.5% 的水，反而可能多用約 0.09 百萬英畝·呎（p. 704）。

## 限制與可質疑之處
- 以空間距離定義同儕會有測量誤差，使估計值偏向零。
- 無法完全排除隨時間與空間變動的未觀察因素，例如推廣強度。
- 節水效果因反彈效應而不確定。

## 與其他論文的關係
- 與 [[Kolady2021]] 方法相近：兩者都以空間同儕效應解釋技術採用。本文在 1 km 尺度發現明顯效果；Kolady2021 在南達科他州 15–30 英里尺度只發現很小的效果，覆蓋作物甚至沒有效果。
- 與 [[Cacho2013]] 呼應：Cacho2013 建議用同儕監測降低交易成本，本文則顯示同儕網絡確實會影響技術擴散。

## 報告可用的引用句
- 美國堪薩斯州的證據顯示，鄰近 1 km 內每多一位採用者，農戶採用節水灌溉技術的機率約增加 0.26 個百分點，而且效果隨距離快速遞減（Sampson & Perry, 2019）。
- 推動農業新技術時，把補貼投放在農戶網絡的中心，可以透過同儕效應提高政策效果（Sampson & Perry, 2019）。

## 書目（APA 7）
Sampson, G. S., & Perry, E. D. (2019). Peer effects in the diffusion of water-saving agricultural technologies. *Agricultural Economics*, *50*(6), 693–706. https://doi.org/10.1111/agec.12518
