---
title: "應用場景與使用者族群 (Application Domains & User Groups)"
type: concept
tags: [應用場景, 校園, 博物館, 兒童課輔, 房地產, 社交機器人]
sources: [paper1, paper2, paper3, paper4, paper5, paper6]
date: 2026-11-22
---

# 應用場景與使用者族群 (Application Domains & User Groups)

## 1. 核心定義與在社交機器人中的重要性
應用場景與目標受眾決定了社交機器人的實體外觀、感測配置、互動策略與社會規範。不同場域的物理空間特徵與利害關係人群體，深刻制約了系統的可行性與設計優先順序。

## 2. 各論文觀點與技術作法比較
- **校園生活與行政導引** `[paper2.pdf, 1 INTRODUCTION; paper3.pdf, 4.3.1]`：Paper 2 針對廣達 6,000 英畝與 900 棟建築的校園迷路新生；Paper 3 歸納出 61 個校園應用標籤，涵蓋導航、校園助理、安防、宣傳推廣、娛樂、社交輔助與身心健康 7 大類別。
- **文化場館遠端臨場** `[paper5.pdf, 3.4 System Deployment]`：Paper 5 部署於擁有 68 處展品的地質博物館，為遠端訪客提供 11 處精選展品的沉浸式導覽。
- **商業帶看與共同導航** `[paper4.pdf, IV.A Real Estate Agent Domain]`：Paper 4 模擬包含客廳、廚房與臥室 3 個區域的房地產帶看導覽。
- **弱勢學童與伴讀照護** `[paper1.pdf, Section 1; paper6.pdf, 1 Introduction]`：Paper 1 鎖定幼兒伴讀以減輕照護者負擔；Paper 6 深入社區課輔，為 5 年內抵達的新移民學童設計融入加拿大貨幣（Loonie/Toonie）與文化常規的互動故事。

## 3. 觀點衝突、推測與已驗證結果
- **現場親臨 vs 遠端代理的體驗衝突**：Paper 5 實證遠端臨場能打破地理限制，但使用者易受現場旁觀者遮擋鏡頭視野（*"annoying when his view was blocked"* - P13）且缺乏實體觸覺；相較之下 Paper 2 實體機器人能直接引導現場行人。
- **推測 vs 已驗證**：Paper 2、3、5 分別驗證了特定場域的真實限制；而 Paper 1 認為伴讀對話編寫模式可廣泛泛化至其他成人或醫療 SAR 領域則屬於待驗證推測（*"We suspect that this tool may be generalizable to all teleoperated social robot dialogue"*）。

## 4. 設計權衡與開放挑戰 (Trade-offs & Challenges)
核心權衡在於「深度客製化」與「通用泛化能力」。新移民課輔高度依賴加拿大在地文化題材，難以直接移植；而校園公共機器人則面臨如何在嘈雜動態環境中兼顧非母語口音辨識與防破壞（vandalism）考驗。

## 5. 參考文獻對照 (References)
- [Paper 1](../papers/paper1-dialogue-authoring.md) — Section 4.3：*"investigate patterns in social robot dialogue use to generalize our interface beyond dialogue for socially assistive robots for children."*
- [Paper 2](../papers/paper2-campus-guide.md) — 1 INTRODUCTION：*"Rutgers University spans over six thousand acres and consists of over nine hundred buildings"*
- [Paper 3](../papers/paper3-campus-robot-trust.md) — 4.3.1 Ideation：*"organised these labels into seven categories: Navigation, On-campus Assistant, Safety and Security, Promotion, Entertainment, Social Assistance, and Wellbeing."*
- [Paper 5](../papers/paper5-narrative-remote-guide.md) — 3.4 System Deployment：*"The geology museum has 68 exhibits in total across four areas"*
- [Paper 6](../papers/paper6-codesign-newcomer-learning.md) — 1 Introduction：*"refer to young children from immigrant or refugee backgrounds who have migrated to Canada within the past five years"*
