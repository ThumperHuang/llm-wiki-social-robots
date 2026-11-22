---
title: "導航、空間感知與協同移動 (Navigation & Co-Navigation)"
type: concept
tags: [導航, 協同移動, 社交Costmap, SLAM, DRRL, 社交機器人]
sources: [paper2, paper4, paper5]
date: 2026-11-22
---

# 導航、空間感知與協同移動 (Navigation & Co-Navigation)

## 1. 核心定義與在社交機器人中的重要性
導航與空間感知賦予社交機器人自主移動與引導人類的能力。在人機互動中，導航不僅追求幾何最短路徑，更必須遵循人際距離與社交預期，並能協調人機同行（Co-Navigation）時的空間步調與共處狀態。

## 2. 各論文觀點與技術作法比較
- **動態扇形社交本地圖** `[paper2.pdf, 5 NAVIGATION MODULE]`：Paper 2 改進 ROS Costmap，將移動行人建模為圓形扇區（*"sector of a circle"*），半徑與速度成正比、張角與速度成反比。實測在 4.4 公尺內效能無顯著差異（*"within 4.4 meters of the robot"*），靜態避障達成 4/5 成功率，5 次動態模擬避障全數成功（*"avoided the moving person for each of its five trials"*）。
- **非共處狀態下的協同導航策略** `[paper4.pdf, I. INTRODUCTION, V, VI.C]`：Paper 4 指出人機並非始終共處，採用 RecurrentPPO 學習聯合策略。實驗證實 Joint Policy 能察覺人類脫隊並主動導航至共處位置，達成最高共處率與最短回合長度（*"highest proximity rate, and a shorter episode length"*）。
- **語義地圖與自主導覽姿態** `[paper5.pdf, 3.3.4 Robotic System]`：Paper 5 透過 Cartographer SLAM 與 Nav2 實現網格自主移動，並預先儲存展品最佳觀賞姿態（optimal pose）。

## 3. 觀點衝突、推測與已驗證結果
- **自主導引與使用者自主性的衝突**：Paper 5 實證指出，當機器人未經確認即主動帶路前往下一展品時，會削弱使用者自主性（*"wasn't done at a certain exhibit"* - P4）；然而 Paper 4 的策略則以任務總時效為目標，自主引導使用者移動。
- **推測 vs 已驗證**：Paper 2 在室內驗證了 9 次端到端無碰撞導航（*"successful and reliable on each of the nine trials"*）；但其即時人體速度追蹤則屬於未來改進計畫（*"Moving forward, we will continue... by developing a new person detection module that provides the velocities of people"*）。

## 4. 設計權衡與開放挑戰 (Trade-offs & Challenges)
核心權衡在於「避障保守性」與「通行效率」。過度擴大行人成本區會導致機器人在擁擠走廊動彈不得；而在遠端操控中，純口語微調轉向（如 Paper 5 受試者反映轉向 15 度困難）與網路延遲亦是開放挑戰。

## 5. 參考文獻對照 (References)
- [Paper 2](../papers/paper2-campus-guide.md) — 5 NAVIGATION MODULE：*"The velocity of the person is proportional to the radius of the sector... and inversely proportional to the angle swept by the sector"*
- [Paper 4](../papers/paper4-joint-dialog-navigation.md) — VI.C Results：*"A higher proximity rate indicates that the robot can perceive the absence of the user and correctly select a navigation action so that they are co-located."*
- [Paper 5](../papers/paper5-narrative-remote-guide.md) — 5.3.1 Dialogue for Guided Navigation：*"Robot Suggestions Impairing User Autonomy... including the lack of user confirmation"*
