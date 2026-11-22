---
title: "A Robot Dialogue Authoring Interface with Smart Capabilities"
type: paper
paper_id: paper1
venue: "HRI '24 Companion (Companion of the 2024 ACM/IEEE International Conference on Human-Robot Interaction)"
authors: "Saad Elbeleidy, Michelle Lieng, Tom Williams"
tags: [社交機器人, HRI, 社交輔助機器人, SAR, 對話編寫, 遠端遙控, 終端使用者開發]
date: 2026-11-22
---

# A Robot Dialogue Authoring Interface with Smart Capabilities

- **出處資訊**：發表於 HRI '24 Companion (March 11–14, 2024, Boulder, CO, USA)，作者 Saad Elbeleidy, Michelle Lieng, Tom Williams（Colorado School of Mines / Peerbots）
- **DOI**：`10.1145/3610978.3640555`
- **原始檔案**：`raw/paper1.pdf`

---

## 1. 核心摘要 (TL;DR)
本研究針對照護者在社交輔助機器人（Socially Assistive Robots, SARs）應用中編寫童書伴讀對話的繁重負擔，開發了一款具備智慧自動化功能的對話編寫專用介面。系統透過自然語言處理技術自動拆分長句、自動補全破冰問候與反饋語句，並提供遙控模擬預覽，旨在減輕照護者開發對話內容的技術門檻與無形勞動負擔。

## 2. 研究背景與痛點 (Problem Statement)
- **社交輔助機器人的內容生成瓶頸** `[paper1.pdf, Section 1 INTRODUCTION]`：  
  SAR 在兒童教育與治療、高齡陪伴等領域潛力巨大，但廣泛落地的關鍵障礙之一在於「輔助內容的開發」。照護者視輔助內容為使用機器人的先決條件，然而目前內容產出多仰賴「無形勞動（invisible labor）」：
  > 原文短句引用：*"Caregivers using SARs to deliver care have suggested that the assistive content itself is a central component of using SARs... However, this content is often authored through invisible labor"*
- **現行工具不匹配** `[paper1.pdf, Section 1 INTRODUCTION]`：  
  現有創作者通常被迫直接在機器人遙控介面中邊做邊寫、依賴拼湊的試算表軟體（Spreadsheets），或仰賴工程師將內容寫死（hard-code），缺乏專為對話內容編寫設計的友善介面。
- **遙控操作與編寫情境的差異** `[paper1.pdf, Section 1 INTRODUCTION]`：  
  遙控者需要配合對話節奏發出簡短語句，並具備破冰建立關係（rapport building）、回饋（feedback）及未知應答（ignorance statements）等對話模組，編寫介面必須反映這些典型 SAR 對話架構。

## 3. 系統架構與技術方法 (Methodology & Architecture)
本系統針對結合 Peerbots 遙控軟體（用於控制 Misty 機器人或虛擬代理）與兒童伴讀情境設計，包含四大核心功能：

1. **單一文本輸入介面 (Simple Author Input)** `[paper1.pdf, Section 2.1 Simple Author Input]`：  
   作者僅需在單一文字框內貼入未處理的童書故事文本，點擊送出即可自動轉換為機器人對話動作，將底層遙控通訊與技術細節完全抽象化。
2. **三項自動化輔助功能 (Automated Capabilities)** `[paper1.pdf, Section 2.2 Automated Capabilities]`：
   - **自動插入破冰與結尾對話** `[paper1.pdf, Section 2.2.1]`：系統在對話開頭與結尾自動從預設庫中隨機選取並插入建立關係（rapport-building）的語句（如打招呼與道別）。
   - **長語句自動斷句 (Long Dialogue Utterance Splitting)** `[paper1.pdf, Section 2.2.2]`：使用 `spaCy` NLP 函式庫分析文字結構，遇到標點符號、換行或超過字數／詞數上限（論文未給具體數值）時切分，並在「從屬連接詞（subordinating conjunctions）」處進行智慧斷句，確保每句長度適當，避免機器人發話過長導致遙控者無法靈活應對插話。
   - **問句自動配對反饋與未知語句** `[paper1.pdf, Section 2.2.3]`：偵測到文字中的問號（`?`）時，系統自動附加 3 個對話動作選項：（1）正向反饋（Positive feedback）、（2）建設性反饋（Constructive feedback）、（3）表示不知道的未知回應（Ignorance response）。
3. **客製化覆寫功能 (Customizability)** `[paper1.pdf, Section 2.3 Customizability]`：  
   作者可自訂各類預設清單（問候、反饋、未知句庫），並可在進階設定中微調斷句的最大字數與詞數限制。
4. **雙模式預覽 (Preview Capabilities)** `[paper1.pdf, Section 2.4 Preview Capabilities]`：
   - **表格預覽 (Table Preview)** `[paper1.pdf, Section 2.4.1]`：展示將匯入 Peerbots 的 CSV 格式對話與標籤元數據。
   - **遙控介面模擬預覽 (Teleoperation Interface Preview)** `[paper1.pdf, Section 2.4.2]`：直接以 Peerbots 按鈕介面的複製品呈現，讓編寫者能夠「換位思考」，代入現場遙控者的視角評估對話節奏。

## 4. 使用者研究與實驗設計 (User Study & Evaluation)
- **實證評估狀態** `[paper1.pdf, Section 4 FUTURE WORK, Section 4.1 Experimental Evaluation, Section 5 CONCLUSION]`：  
  本篇為 Short Paper，**尚未進行正式受試者實驗**。論文在 `Section 4 FUTURE WORK` 標題下的 `Section 4.1 Experimental Evaluation` 中提出了未來的實驗評估規劃：
  > 原文短句引用：*"We plan to experimentally evaluate the authoring interface’s performance compared to other interfaces. Specifically, we think it is important to evaluate the interface compared to the teleoperation interface and compared to spreadsheet-based interfaces that authors may use. We suspect that using a dedicated authoring interface... would be rated higher by authors... and would be faster at creating the same dialogue."*
- **預計評估指標** `[paper1.pdf, Section 4.1, Section 5]`：  
  未來實驗規劃比較（1）專用編寫介面、（2）現有遙控介面與（3）試算表軟體在「內容編寫時間（time taken to author content）」與「作者主觀易用度（author-reported usability）」上的表現。

## 5. 主要發現與研究限制 (Key Findings & Limitations)
- **兩大核心實作挑戰 (Key Challenges)** `[paper1.pdf, Section 3 KEY CHALLENGES]`：
  1. **缺乏通用標準對話格式 (Standard Robot Dialogue Format)** `[paper1.pdf, Section 3.1]`：目前各家 SAR 遙控系統格式封閉且碎片化，本介面僅適配 Peerbots CSV 格式，內容難以跨平台移植，呼籲學界建立共享對話標準。
  2. **獨立編寫介面與遙控現場之割裂 (Integrating with Teleoperation Interface)** `[paper1.pdf, Section 3.2]`：作者指出獨立專用介面雖便於專注編寫，但依據自身使用經驗（"based on our personal use"），發現這會拉開編寫者與遙控者現場體驗的距離；儘管加入了按鈕模擬預覽，但若面對更複雜的遙控介面將難以複製，因此建議編寫介面應與遙控系統直接整合。
- **未來工作與改進方向 (Future Work & Recommendations)** `[paper1.pdf, Section 4 FUTURE WORK]`：
  - *語境感知生成* `[paper1.pdf, Section 4.2 Additional Features]`：目前自動生成的問候與反饋語句為「語境無關（context-agnostic）」的隨機抽取，未來建議研究語境感知演算法以提升自動推薦品質。
  - *行內編輯支援* `[paper1.pdf, Section 4.2 Additional Features]`：作者建議（"We recommend"）未來介面應支援對自動生成內容的行內編輯（inline editing）。
  - *領域泛化* `[paper1.pdf, Section 4.3 Generalizing To Other Domains]`：目前系統僅針對幼兒伴讀情境，未來需研究其他 SAR 領域的對話模式以評估泛化性。

## 6. 課堂報告亮點與啟發 (Takeaways for Presentation)
> ⚠️ **註：以下內容為整理者之教學詮釋與報告建議，非論文原文主張。**

1. **「無形勞動（Invisible Labor）」的設計視角**：  
   社交輔助機器人研究常聚焦於現場互動效果，但實際落地時，背後龐大的「對話內容編寫成本」常落在照護者身上。簡化非技術專業人員的編寫負擔，是推動 SAR 走出研究場域的實務關鍵。
2. **人機協同架構（Human-in-the-Loop 模式）**：  
   在醫療與兒童教育等敏感場景中，維持遠端遙控可確保安全；利用 NLP 自動化（智慧斷句、從預設清單隨機選取）輔助編寫，提供了一種以自動化工具支援遙控操作者的可行途徑。
3. **編寫者與遙控者的視角整合**：  
   論文指出編寫者與現場遙控者的工作情境與需求不同，在介面中整合「遙控按鈕視圖預覽」有助於編寫者以遙控者的角度檢視對話節奏。

## 7. 相關概念雙向連結 (Related Concepts)
- [對話與語言互動機制](../concepts/dialogue-interaction.md)
- [角色定位與人機互動模式](../concepts/robot-roles.md)
- [應用場景與使用者族群](../concepts/application-domains.md)
