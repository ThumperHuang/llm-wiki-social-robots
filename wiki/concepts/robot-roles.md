---
title: "角色定位與人機互動模式 (Robot Roles & Interaction Models)"
type: concept
tags: [角色定位, 遙控操作, 照護輔助, 終端使用者開發]
sources: [paper1]
date: 2026-11-22
---

# 角色定位與人機互動模式 (Robot Roles & Interaction Models)

## 1. 核心定義與在社交機器人中的重要性
角色定位定義了社交機器人在互動場景中被賦予的社會身份、功能定位及其與人類互動者之間的權力與從屬關係。社交機器人的角色並非單一固定，而是涵蓋了導覽員、照護助手、同儕夥伴乃至遠端操作者的實體化身。清晰的角色定義有助於設定使用者的心理預期，並決定了底層人機協同架構（如自主控制、遠端遙控或半自主輔助）。

## 2. 各論文觀點與技術作法比較
- **照護者與遙控操作之共存角色** `[paper1.pdf, Section 1 INTRODUCTION]`：  
  Paper 1 探討社交輔助機器人（SAR）在醫療照護與童書伴讀中的角色定位。研究指出，在此類高敏感場景下，機器人更適合維持「人在迴路中（Human-in-the-loop）」的遠端遙控模式（Teleoperation），以確保安全與即時應變能力。
- **內容作者與現場遙控者的角色認知分離** `[paper1.pdf, Section 1 INTRODUCTION, Section 2.4.2]`：  
  Paper 1 深刻分析了「內容編寫者（Author）」與「現場遙控者（Teleoperator）」之間的認知差異。編寫者聚焦於長篇教學內容，而遙控者需要按鈕化的即時應答工具。系統透過「按鈕視圖模擬」幫助作者代入遙控者角色，縮短兩者間的心智模型差距。
- *(其他論文待 Ingest 後持續補充)*

## 3. 設計權衡與開放挑戰 (Trade-offs & Challenges)
在遙控輔助機器人角色設計中，核心權衡在於「完全自主」與「人工遙控」的邊界劃分。如 Paper 1 所述，過度依賴遙控會衍生龐大的「無形勞動（invisible labor）」；但完全自主在當前照護倫理與安全標準下仍難以落實，因此如何利用智慧介面減輕人類負擔成為關鍵折衷。

## 4. 參考文獻對照 (References)
- [A Robot Dialogue Authoring Interface with Smart Capabilities](../papers/paper1-dialogue-authoring.md) — Section 1：*"While a caregiver may perform both tasks of authoring content and teleoperating robots, the context in which they do so, and their needs in accomplishing each are fairly distinct"*
