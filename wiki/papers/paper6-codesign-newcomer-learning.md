---
title: "Co-designing a Social Robot for Newcomer Children’s Cultural and Language Learning"
type: paper
paper_id: paper6
venue: "HRI Companion '26 (21st ACM/IEEE International Conference on Human-Robot Interaction)"
authors: "Neil Fernandes, Tehniyat Shahbaz, Emily Davies-Robinson, Yue Hu, Kerstin Dautenhahn"
tags: [社交機器人, HRI, 共同設計, 新移民兒童, 語言學習, 文化適應, 三方互動, Maple]
date: 2026-11-22
---

# Co-designing a Social Robot for Newcomer Children’s Cultural and Language Learning

- **出處資訊**：發表於 HRI Companion '26 (March 16–19, 2026, Edinburgh, Scotland, UK)，作者來自滑鐵盧大學（University of Waterloo）與非營利讀寫教育組織 United for Literacy (UFL)
- **DOI**：`10.1145/3776734.3794350`
- **原始檔案**：`raw/paper6.pdf`

---

## 實際章節標題列表 (Section Headings)
1. `1 Introduction`
2. `2 Methods and Procedures`
   - `2.1 Co-designers`
   - `2.2 Robotic System Overview`
   - `2.3 Procedure and Analysis`
3. `3 Preliminary Results`
   - `3.1 Challenges`
     - `3.1.1 Language Barriers and Skill Levels`
     - `3.1.2 Lack of Motivation and Attention`
     - `3.1.3 Absence of Formal Proficiency Baselines`
     - `3.1.4 Lack of One-on-One Attention and Support`
   - `3.2 Cultural Orientation and Community Belonging`
   - `3.3 Perceived Social Role of Maple`
   - `3.4 Preliminary Design Guidelines`
     - `3.4.1 Guideline 1: Provide multi-modal and multilingual scaffolding for language barriers`
     - `3.4.2 Guideline 2: Use short, story-based activities to support attention and motivation`
     - `3.4.3 Guideline 3: Learn a second language through cultural orientation`
     - `3.4.4 Guideline 4: Embed formal assessments into playful interactions`
     - `3.4.5 Guideline 5: Support one-on-one attention within a triadic setup`
4. `4 Discussion and Future Work`
5. `5 Conclusion`
- `Acknowledgments`
- `References`

---

## 1. 核心摘要 (TL;DR)
本研究透過與加拿大非營利讀寫組織（UFL）之第二語言專家導師（expert L2 tutors）共同設計（Co-design），探討桌上型社交輔助機器人 Maple 如何協助新移民兒童進行英語學習與在地文化融入。研究識別出社區課輔現場的四大教學瓶頸，將機器人定位為非威脅性的「同儕伴侶（Peer-like companion）」與「注意負載平衡器」，並提出基於「導師–學童–機器人」三方互動模式的五項初步設計準則。

## 2. 研究背景與痛點 (Problem Statement)
- **新移民兒童的雙重挑戰** `[paper6.pdf, 1 Introduction]`：  
  新移民兒童（過去 5 年內移民或難民背景之學童）在適應全新學校體系與文化規範的同時，面臨嚴峻的語言習得挑戰。
- **社區輔導計畫的四大實務瓶頸** `[paper6.pdf, 3.1 Challenges]`：
  1. *語言障礙與技能懸殊* `[paper6.pdf, 3.1.1]`：學童英文程度落差極大（部分甚至完全不會說英文），且出勤極不穩定：
     > 原文短句引用：*"some children attend as few as three out of eight sessions... This irregular attendance makes it difficult to implement new approaches consistently."*  
     （部分學童在 8 次課程中僅出席 3 次，難以持續實施教學介入）。
  2. *動機與注意力缺乏* `[paper6.pdf, 3.1.2]`：傳統紙本學習單枯燥，學童在全日學校作息後易感到疲倦分心，或受 ADHD/ASD 等未診斷症狀影響。
  3. *缺乏正式語言能力基準* `[paper6.pdf, 3.1.3]`：開放式入學機制缺乏前期程度測驗，導師無從掌握個別起點進行差異化教學。
  4. *師資短缺與一對一支援不足* `[paper6.pdf, 3.1.4]`：師生比例低，導師必須在教室巡迴走動（"float around"），無法提供個別化持續指導。

## 3. 系統架構與技術方法 (Methodology & Architecture)
- **Maple 機器人雛形平台** `[paper6.pdf, 2.2 Robotic System Overview]`：  
  由 ROBOTIS Engineer Kit 1 組裝而成之小型桌上型人形機器人（compact table-top humanoid），配備多個 DYNAMIXEL 伺服馬達實現上半身手勢與頭部轉動；頭部安裝智慧型手機作為臉部螢幕，呈現動畫眼睛與嘴型表情。
- **軟體與控制架構** `[paper6.pdf, 2.2 Robotic System Overview]`：  
  基於 ROS Noetic（Ninjemys 發行版），整合運動控制、音訊輸出、臉部動畫（PyLips 套件實現唇形同步）與行為樹（Behavior Tree）；對話與動作調度遵循 RoboSync 原則；提供以 React 開發之平板網頁介面，透過 ROS bridge 讓導師無需撰寫程式碼即可編輯故事活動與測驗。
- **共同設計流程與參與專家** `[paper6.pdf, 2.1 Co-designers, 2.3 Procedure and Analysis]`：  
  > 原文短句引用：*"Our design team comprised four participants: two expert second-language (L2) tutors from UFL that delivers literacy programs and two Human–Robot Interaction (HRI) researchers (one professor and one graduate student)... We conducted one 60-minute online co-design meeting with the participants as a group over Microsoft Teams."*  
  （共 4 位參與者：2 位 UFL 第二語言專家導師，分別具 7 年與 2.5 年資歷；2 位 HRI 研究者，包含 1 位教授與 1 位研究生；進行 60 分鐘線上會議與錄音轉錄分析）。

## 4. 使用者研究與實驗設計 (User Study & Evaluation)
- **實證評估狀態** `[paper6.pdf, 4 Discussion and Future Work, 5 Conclusion]`：  
  本篇為 Late-Breaking Report（晚期突破報告），目前核心成果奠基於**導師共同設計工作坊**所產出之洞察與設計原則。作者明確標註尚未進行兒童實地長程評估，並詳細載明未來規劃：
- **未來實證實驗規劃細節** `[paper6.pdf, 4 Discussion and Future Work]`：  
  > 原文短句引用：*"Since this work solely relied on expert perspectives, future work will explore several case studies, in which children read stories that embed target words... These sessions would include children aged between 5-10 years old and would be coordinated with UFL... run with a one-to-one, tutor-mediated interaction, that will have approximately four children. We also will be running several play-testing sessions, using the think aloud approach and interviews with tutors"*  
  （未來將與 UFL 合作進行個案研究，招募約 4 名 5–10 歲學童進行伴讀測試與放聲思考測試）。

## 5. 主要發現與設計準則 (Key Findings & Design Guidelines)
- **社交角色：同儕伴侶而非威權教師** `[paper6.pdf, 3.3 Perceived Social Role of Maple]`：  
  專家一致認為 Maple 應定位為平易近人的「同儕（peer-like companion）」，而非嚴肅權威的教師。機器人在「導師–學童–機器人」三方架構中充當注意力負載平衡器（"attention load-balancer"），陪伴單一學童閱讀，複雜概念則交由巡迴的真人導師介入。
- **文化適應與社區認同 (Cultural Orientation)** `[paper6.pdf, 3.2]`：  
  語言學習必須根植於當地文化常規。例如將加拿大文化象徵（Loonie 與 Toonie 貨幣、浣熊與麋鹿等動物）融入情境故事，並藉由故事角色扮演（如遇到公車司機或老師該如何打招呼）讓學童理解文化禮貌規範。
- **五大初步設計準則 (Preliminary Design Guidelines)** `[paper6.pdf, 3.4 Preliminary Design Guidelines]`：
  1. *多模態與多語言鷹架 (Multi-modal & multilingual scaffolding)* `[paper6.pdf, 3.4.1]`：數位故事同時顯示英語與母語單字，結合語音與肢體手勢指向圖片，降低初學者門檻。
  2. *短篇故事化活動維持專注 (Short, story-based activities)* `[paper6.pdf, 3.4.2]`：以短篇輪流對話遊戲打破沉悶學習單，在學童分心時利用揮手等動作重新吸引注意。
  3. *以文化適應促進第二語言習得 (Cultural orientation)* `[paper6.pdf, 3.4.3]`：透過日常場景角色扮演（role-play）實踐語言社會化。
  4. *在遊戲互動中嵌入正式評量 (Embed formal assessments)* `[paper6.pdf, 3.4.4]`：在遊戲與故事中暗中記錄學童朗讀或點擊答題表現，免除正式考試壓力並為導師建立能力基準。
  5. *支援三方架構下的一對一專注 (Triadic setup support)* `[paper6.pdf, 3.4.5]`：在導師巡視多位學童時，機器人維持單一學童的一對一陪伴，兼顧公平性與個別關注。

## 6. 課堂報告亮點與啟發 (Takeaways for Presentation)
> ⚠️ **註：以下內容為整理者之教學詮釋與報告建議，非論文原文主張。**

1. **「三方互動（Triadic Interaction）」顛覆傳統二元人機架構**：  
   在教育場景中，機器人不應是取代人類教師的「獨立教學者」，而是扮演學童與教師之間的「輔助同儕（Peer）」。這種「導師–學童–機器人」三方協同架構，有效解決了師資比例不足與學童不敢向真人提問的矛盾。
2. **機器人作為「文化轉譯橋樑（Cultural Bridge）」**：  
   語言習得無法脫離文化脈絡。透過將在地俚語、貨幣與禮節嵌入機器人故事互動，使社交機器人不僅傳授文法，更能協助脆弱族群（移民家庭）融入在地社區。
3. **無痛隱蔽評量（Stealth Micro-Assessment）**：  
   利用機器人互動過程自動記錄辨識學童朗讀與選擇反應，在不增加學童考試壓力的情況下為教學者提供量化能力指標，展現了極佳的教育輔助設計典範。

## 7. 相關概念雙向連結 (Related Concepts)
- [角色定位與人機互動模式](../concepts/robot-roles.md)
- [應用場景與使用者族群](../concepts/application-domains.md)
- [對話與語言互動機制](../concepts/dialogue-interaction.md)
- [信任度、透明性與倫理接受度](../concepts/trust-transparency.md)
