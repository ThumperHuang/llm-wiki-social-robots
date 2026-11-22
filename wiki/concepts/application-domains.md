---
title: "應用場景與使用者族群 (Application Domains & User Groups)"
type: concept
tags: [應用場景, 兒童教育, 伴讀, 照護輔助]
sources: [paper1]
date: 2026-11-22
---

# 應用場景與使用者族群 (Application Domains & User Groups)

## 1. 核心定義與在社交機器人中的重要性
應用場景與目標使用者族群決定了社交機器人的物理外觀、互動模態、語言複雜度與安全規範。不同場域（如醫院、家庭、學校、博物館、校園）對機器人的社會行為、耐用性與文化包容度具有截然不同的脈絡要求，是評估社交機器人系統是否具備實用落地價值的決定性維度。

## 2. 各論文觀點與技術作法比較
- **兒童教育與伴讀輔助場景** `[paper1.pdf, Section 1 INTRODUCTION, Section 2 THE AUTHORING INTERFACE]`：  
  Paper 1 鎖定「童書共讀（reading a book with a child）」此一特定社交輔助場景。目標使用者包含幼兒以及負責照料的照護者（Caregivers）。
- **非技術人員在特定場域的進入門檻** `[paper1.pdf, Section 1 INTRODUCTION]`：  
  Paper 1 指出在教育與醫療照護等特定場景中，照護人員通常不具備程式設計技能。若要讓機器人真正走入日常照護，系統設計必須降低專業門檻，提供極簡化的內容導入途徑。
- *(其他論文待 Ingest 後持續補充)*

## 3. 設計權衡與開放挑戰 (Trade-offs & Challenges)
特定場域客製化與通用性之間的衝突顯著。如 Paper 1 所提及 `[paper1.pdf, Section 4.3 Generalizing To Other Domains]`，針對幼兒伴讀所優化的對話模式與斷句邏輯，能否順利遷移至高齡照護或其他成人教育領域，仍受限於場域情境的高度異質性。

## 4. 參考文獻對照 (References)
- [A Robot Dialogue Authoring Interface with Smart Capabilities](../papers/paper1-dialogue-authoring.md) — Section 1：*"SARs have been used with children in education settings and therapeutic settings. Elderly folks have also benefited from SARs as companions or to support their cognitive abilities."*
