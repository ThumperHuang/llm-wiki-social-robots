---
title: "信任度、透明性與倫理接受度 (Trust, Transparency & Ethics)"
type: concept
tags: [信任度, 運作透明度, 營運者透明度, 隱私, 幻覺, 社交機器人]
sources: [paper1, paper3, paper5, paper6]
date: 2026-11-22
---

# 信任度、透明性與倫理接受度 (Trust, Transparency & Ethics)

## 1. 核心定義與在社交機器人中的重要性
信任度是使用者接納社交機器人並與之互動的關鍵基石。在公共環境中，信任不僅取決於機器人的功能表現，更深植於機器人如何向大眾揭示其內部運作機理與背後權責歸屬。

## 2. 各論文觀點與技術作法比較
- **雙重視角的透明度架構** `[paper3.pdf, 4.2.1, 5.2]`：Paper 3 調查 59 位師生（*"59 participants"*），提出兩大透明度維度：（1）*運作透明度（Operational Transparency）*：明確溝通功能、能力極限與出錯可能性；（2）*營運者透明度（Operator Transparency）*：公開營運主體與資料管理責任（*"who is behind her"*）。
- **擴充信任因素模型** `[paper3.pdf, 4.2, 4.2.4]`：Paper 3 擴充 Hancock 信任模型（加入程式透明度、資料安全、營運者身分與透明度），並將透明度與安全性列為 Baraka 特徵架構第 8 項關鍵特徵（*"eighth key characteristic"*）。
- **生成式 AI 的幻覺信任危機** `[paper5.pdf, 5.3.3]`：Paper 5 實地研究揭露，當非專業使用者面對表現專業的機器人時，即使機器人產生幻覺編造資訊，使用者仍全盤採信（*"it feels like right"* - P18），凸顯事實查核的倫理急迫性。

## 3. 觀點衝突、推測與已驗證結果
- **營運主體身分 vs 流程透明度的衝突**：Paper 3 顯示受試者觀點分歧。部分受試者認為校方背書即足以保證信任（*"if the robots are all university-sponsored, I don’t think anybody will wonder about the trustworthiness"* - P43）；另一派則堅持必須公開資料處理細節。
- **容錯性與隱私態度的衝突**：Paper 3 發現有人認為出錯不可容忍，有人則認為校園內出錯無實質危害；有人強烈要求面部去識別化，有人則持消極態度認為數位世界本無隱私（*"there’s no privacy at all"* - I8）。
- **推測 vs 已驗證**：Paper 3 實證驗證了性別在機器人熟悉度上的顯著差異（男 M=2.61 vs 女 M=1.90, p < .05）；而在敏感照護領域中遠端遙控優於完全自主則屬於學界倡議觀點 `[paper1.pdf, Section 1]`。

## 4. 設計權衡與開放挑戰 (Trade-offs & Challenges)
核心權衡在於「資料蒐集深度」與「隱私保護」。如 Paper 5 受試者不想在公共展館螢幕露臉以防路人指點（P8, 15, 18, 20），提出虛擬頭像（avatar）折衷方案；而系統如何在不犧牲流暢體驗下向使用者即時預警 LLM 幻覺，仍是艱鉅挑戰。

## 5. 參考文獻對照 (References)
- [Paper 1](../papers/paper1-dialogue-authoring.md) — Section 1：*"in domains where socially assistive robots are used, there ought to be a human in the loop"*
- [Paper 3](../papers/paper3-campus-robot-trust.md) — 5.2 Transparency in Practice：*"Operational transparency relates to how clear the robot’s functions... Operator transparency concerns the clarity about... who is responsible for data management"*
- [Paper 5](../papers/paper5-narrative-remote-guide.md) — 5.3.3 Dialogue for Location-aware Narratives：*"participants still expressed their trust towards the robot when hallucinations occurred."*
