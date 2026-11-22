---
title: "Learning Joint Policies for Human-Robot Dialog and Co-Navigation"
type: paper
paper_id: paper4
venue: "IROS 2023 (IEEE/RSJ International Conference on Intelligent Robots and Systems)"
authors: "Yohei Hayamizu, Zhou Yu, Shiqi Zhang"
tags: [社交機器人, HRI, 協同導航, DRRL, POMDP, 對話狀態追蹤, 強化學習]
date: 2026-11-22
---

# Learning Joint Policies for Human-Robot Dialog and Co-Navigation

- **出處資訊**：發表於 IROS 2023 (October 1–5, 2023, Detroit, USA)，作者來自紐約州立大學賓漢頓分校（SUNY Binghamton）與哥倫比亞大學（Columbia University）
- **DOI**：`10.1109/IROS55552.2023.10341663`
- **原始檔案**：`raw/paper4.pdf`

---

## 實際章節標題列表 (Section Headings)
1. `I. INTRODUCTION`
2. `II. RELATED WORK`
3. `III. DEEP RECURRENT REINFORCEMENT LEARNING`
4. `IV. PROBLEM STATEMENT`
   - `A. Real Estate Agent Domain`
   - `B. Real Estate Agent Problem`
5. `V. PROPOSED APPROACH`
6. `VI. EXPERIMENT`
   - `A. Simulator Design`
   - `B. Experiment Settings`
   - `C. Results`
   - `D. Demonstration in the Real World`
7. `VII. CONCLUSION AND FUTURE WORK`
- `ACKNOWLEDGMENTS`
- `REFERENCES`

---

## 1. 核心摘要 (TL;DR)
本研究針對服務型機器人與人類同行移動時的「對話導航（dialog navigation）」複合難題，提出基於深度循環強化學習（Deep Recurrent Reinforcement Learning, DRRL）的聯合策略學習框架。系統能同時根據對話歷史與人機空間位置，聯合決策下一步應採取對話動作還是導航動作，在房地產導覽模擬環境與真實世界機器人驗證中，顯著優於傳統交替式規則與分離式基線模型。

## 2. 研究背景與痛點 (Problem Statement)
- **同行移動中對話與導航的交互影響** `[paper4.pdf, I. INTRODUCTION]`：  
  傳統機器人研究通常將移動導航與對話系統割裂處理，對話多發生在導航之前或固定單一地點。然而在房仲帶看、導覽等真實場景中，機器人需要與人類同行移動（Co-Navigation）並同時進行多輪對話：
  > 原文短句引用：*"Dialog capabilities enable the robot to estimate the human’s belief state, and accordingly select the next navigation goal; navigation capabilities help change the human-robot system’s location to facilitate the next few turns of the ongoing dialog."*
- **非共處（Not Co-located）與部分可觀測性** `[paper4.pdf, I. INTRODUCTION, IV. PROBLEM STATEMENT]`：  
  在協同移動過程中，人類可能不會隨時跟隨在機器人身旁（人機並非始終共處）。當人類不在同一房間時，機器人若逕自陳述房間特徵將無法被接收，且使用者回饋存在噪聲，因此系統面臨高度不確定性與部分可觀測馬可夫決策過程（POMDP）挑戰。

## 3. 系統架構與技術方法 (Methodology & Architecture)
- **聯合策略學習框架 (Joint Policy Learning Framework)** `[paper4.pdf, V. PROPOSED APPROACH]`：  
  將空間位置資訊與對話狀態追蹤（Dialog State Tracking, DST）統一整合，利用槽位填充（slot-filling）表徵任務進度。狀態包含：機器人位置、使用者位置、各屬性槽位狀態與前一動作。
- **深度循環強化學習模型 (DRRL with RecurrentPPO)** `[paper4.pdf, III, V, VI.B]`：  
  為處理因導航動作缺乏立即回饋而需要長程記憶的特性，模型採用結合長短期記憶網路（LSTM）的 Proximal Policy Optimization（RecurrentPPO）。Actor 與 Critic 網路皆包含：
  > 原文短句引用：*"The first two layers have an MLP layer of 64 units with tanh activation as a hidden layer. The output of the second layer is fed into the LSTM layer with 256 units."*  
  （前兩層為 64 單元具 tanh 激活函數的 MLP，輸出接入 256 單元的 LSTM 層）。
- **動作空間統一表徵** `[paper4.pdf, IV.B, VI.A]`：  
  動作空間 $A = A^D \cup A^N$，包含對話動作（inform, guidance, report）與導航動作（stay, goto），採用類似 MultiWOZ-2.1 的四元組語義表徵 `[意圖, 領域, 槽位, 值]`。

## 4. 使用者研究與實驗設計 (User Study & Evaluation)
- **模擬器參數與設定** `[paper4.pdf, VI.A Simulator Design, VI.B Experiment Settings]`：
  1. *環境規模*：  
     > 原文短句引用：*"The simulator consists of 10 house instances. Each house instance has three domains (“livingroom”, “kitchen”, and “bedroom”), each with 4 feature slots."*  
     （10 個房屋實例，每實例 3 個區域：客廳、廚房、臥室，各含 4 個特徵槽位）。
  2. *獎勵函數*：  
     > 原文短句引用：*"The environment returns a positive reward Rmax = 1.0 when all user requirements are satisfied and a negative reward R = −0.01 otherwise."*  
     （滿足所有需求時給予 +1.0 正向獎勵，否則每步給予 -0.01 負向生活成本獎勵）。
  3. *環境噪聲與轉移機率*：  
     > 原文短句引用：*"User feedback has noise with a 0.1 probability of being opposite. Robot and user movements are controlled with transition probabilities. The robot can successfully navigate to its goal location in 0.9 probability. The user follows the robot in presence of a 0.05 probability noise"*  
     （使用者回饋有 0.1 機率出現反向噪聲；機器人有 0.9 機率成功抵達目標；人類跟隨伴隨 0.05 機率走向其他位置）。
  4. *訓練步數與超參數*：  
     > 原文短句引用：*"The robot spends 5, 000, 000 timesteps for each run to learn a joint policy... batch size of 4096. The discounting factor γ is 0.99, the learning rate α is 0.002, and clip size ϵ is 0.1."*  
     （每輪訓練花費 5,000,000 步；向量化環境維度 32；批次大小 4096；折扣因子 0.99；學習率 0.002；裁剪值 0.1）。
  5. *評估規模*：  
     > 原文短句引用：*"We evaluate the agent’s performance of those policies for 100 independent episodes every 100, 000 timestep by using a deterministic policy and select the best policy model to compare the performance"*  
     （每 100,000 步評估 100 個獨立回合）。
- **真實世界機器人驗證** `[paper4.pdf, VI.D Demonstration in the Real World]`：  
  > 原文短句引用：*"We deployed our joint policy model on a segway-based mobile robot. The robot interacts with a human while traversing an environment where three rooms exist. We use YOLO V3 for ROS to realize real-time object detection and Google Dialogflow for a natural language understanding component."*  
  （部署於 Segway 輪式移動機器人，穿梭於 3 個房間中與真人互動，結合 YOLO V3 與 Google Dialogflow）。

## 5. 主要發現與研究限制 (Key Findings & Limitations)
- **主要發現** `[paper4.pdf, VI.C Results, Fig. 3]`：  
  在 100 次運行評估中，聯合策略模型（Joint Policy）全面超越三種基線（DP+P 分離策略、RD+P 最快完成規則、RD+P 高成功率規則）：
  1. *成功率最高*：在人類有偏離機率與回饋噪聲下，Joint Policy 達成最高任務完成率（約 95%）。
  2. *回合長度最短*：兼顧資訊傳遞與導航效率，平均所需步數最短（約 28 步，基線需 35~50 步）。
  3. *共處率（Proximity Rate, PR）最高*：  
     > 原文短句引用：*"Joint Policy has the highest proximity rate, and DP+P and RD+Ps have a lower proximity rate. This indicates that the DP+P tries to inform entities without considering the user’s location to minimize the episode length, resulting in a lower success rate than Joint Policy."*  
     （Joint Policy 共處率接近 0.98，證明模型學會在說出資訊前主動確認或導航至與人類共處）。
- **研究限制與未來工作 (Future Work)** `[paper4.pdf, VII. CONCLUSION AND FUTURE WORK]`：
  - *樣本效率偏低*：作者明確指出強化學習面臨樣本效率低的問題（"the low sample efficiency issue can be addressed to increase the cardinality of slots"），限制了目前特徵槽位的擴展規模。
  - *非端到端架構*：目前視覺感知（YOLO）、自然語言理解（Dialogflow）與策略學習為分離模組，作者計畫未來進一步將語言理解與視覺感知融入迴路中實現端到端學習（*"Another direction is to enable end-to-end learning by further incorporating language understanding and perception into the loop."*）。

## 6. 課堂報告亮點與啟發 (Takeaways for Presentation)
> ⚠️ **註：以下內容為整理者之教學詮釋與報告建議，非論文原文主張。**

1. **空間狀態與對話狀態的緊密耦合**：  
   本篇精準解決了實體機器人與純虛擬助理的最大差異：在實體世界中，「在哪裡說話」與「說什麼話」同等重要。未確認人類同行便逕自發話，會導致資訊傳遞失敗。
2. **POMDP 與 LSTM 在長程人機互動中的應用**：  
   移動需要時間且中途沒有對話反饋，LSTM 成功充當了信念狀態（belief state）的近似器，解決了純反應式策略容易遺忘對話進度的痛點。
3. **從模擬器到實體機器的遷移展示**：  
   透過在模擬環境中注入隨機噪聲（人類走失機率 0.05、回饋相反機率 0.1），使策略具備對現實世界感測與人類行為不確定性的容錯韌性，並成功於 Segway 實體機落地。

## 7. 相關概念雙向連結 (Related Concepts)
- [導航、空間感知與協同移動](../concepts/navigation-co-navigation.md)
- [對話與語言互動機制](../concepts/dialogue-interaction.md)
- [角色定位與人機互動模式](../concepts/robot-roles.md)
- [應用場景與使用者族群](../concepts/application-domains.md)
