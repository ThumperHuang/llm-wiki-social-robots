---
title: "角色定位與人機互動模式 (Robot Roles & Interaction Models)"
type: concept
tags: [角色定位, 導覽員, 同儕夥伴, 自我化身, 三方互動, 社交機器人]
sources: [paper1, paper3, paper5, paper6]
date: 2026-11-22
---

# 角色定位與人機互動模式 (Robot Roles & Interaction Models)

## 1. 核心定義與在社交機器人中的重要性
角色定位定義了機器人在互動情境中的社會身分與人機權力關係。恰當的角色塑造能設定合理的使用者心理預期，並決定系統應採取完全自主、遠端遙控、或是協同代理的互動架構。

## 2. 各論文觀點與技術作法比較
- **內容編寫者與現場遙控者的角色落差** `[paper1.pdf, Section 1, 2.4.2]`：Paper 1 指出編寫長篇對話的照護者與現場遙控操作者的工作脈絡截然不同（*"fairly distinct"*），系統透過按鈕模擬預覽促進視角整合。
- **多元公共服務角色光譜** `[paper3.pdf, 4.3.1, Appendix D]`：Paper 3 歸納出 61 個應用標籤，包含學生導師機器人（student tutor）、迎賓員、迎新伴侶與實驗室助理等。
- **遠端臨場的四重動態角色** `[paper5.pdf, 5.2]`：Paper 5 透過 20 名受試者質化研究歸納出 4 種角色：專業導覽員（Guide）、學習工具與中介（Tool/Medium）、忠誠夥伴（Companion）、以及 4 位受試者認同的實體自我延伸與化身（*"extension of themselves... 'proxy' and 'eyes'"*）。
- **三方互動中的同儕夥伴** `[paper6.pdf, 3.3, 3.4.5]`：Paper 6 在課輔現場將 Maple 定位為非威權的「同儕伴侶（peer-like companion）」，在「導師–學童–機器人」三方互動中擔任「注意負載平衡器（attention load-balancer）」。

## 3. 觀點衝突、推測與已驗證結果
- **威權導師 vs 同儕夥伴的角色衝突**：Paper 6 專家明確排斥威權教師角色，主張機器人若居高臨下會令弱勢學童退縮；但 Paper 5 的博物館受試者則高度肯定機器人作為知識權威指導者（instructor）的角色。兩者源於學童輔導與大眾展館之受眾心理差異。
- **推測 vs 已驗證**：Paper 5 實證驗證了使用者會切換不同禮貌策略（politeness strategies）對待不同角色；而 Paper 6 的三方互動成效奠基於專家共同設計，兒童實地個案驗證仍屬於未來規劃（*"future work will explore several case studies... with approximately four children"*）。

## 4. 設計權衡與開放挑戰 (Trade-offs & Challenges)
核心權衡在於「機器人主導權」與「人類主體性」。若將機器人塑造成全知權威，容易引發幻覺誤導或剝奪自主性；若僅定位為被動工具，則失去社交互動與引導學習的價值。

## 5. 參考文獻對照 (References)
- [Paper 1](../papers/paper1-dialogue-authoring.md) — Section 1：*"authors currently rely on teleoperation interfaces to author content... but are not designed to do so effectively"*
- [Paper 3](../papers/paper3-campus-robot-trust.md) — 4.3.1 Ideation：*"collected all the ideas submitted by the participants and organised them into 61 unique labels"*
- [Paper 5](../papers/paper5-narrative-remote-guide.md) — 5.2.4 As a representation of self：*"Four participants (P1, 15, 16, 18) saw the robot as an extension of themselves."*
- [Paper 6](../papers/paper6-codesign-newcomer-learning.md) — 3.3 Perceived Social Role of Maple：*"experts converged on Maple as a peer-like companion rather than a teacher or authority figure."*
