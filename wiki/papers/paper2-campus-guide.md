---
title: "Development of a Socially Cognizant Robotic Campus Guide"
type: paper
paper_id: paper2
venue: "HRI '24 Companion (Companion of the 2024 ACM/IEEE International Conference on Human-Robot Interaction)"
authors: "Benjamin Greenberg, Daniel Nakhimovich, Richard Magnotti, Hriday Purohit, Sanskar Shah, Aniket Satish Kulkarni, Uriel Gonzalez-Bravo, Noah R. Carver"
tags: [社交機器人, HRI, 校園導覽, 社會認知導航, 語音互動, YOLOv5, Costmap]
date: 2026-11-22
---

# Development of a Socially Cognizant Robotic Campus Guide

- **出處資訊**：發表於 HRI '24 Companion (March 11–14, 2024, Boulder, CO, USA)，作者來自 Rutgers University
- **DOI**：`10.1145/3610978.3641263`
- **原始檔案**：`raw/paper2.pdf`

---

## 實際章節標題列表 (Section Headings)
1. `1 INTRODUCTION`
2. `2 DESIGN CONTEXT`
   - `2.1 Socially Cognizant Design`
   - `2.2 Stakeholder Engagement`
3. `3 SYSTEM OVERVIEW`
4. `4 SPEECH MODULE`
5. `5 NAVIGATION MODULE`
6. `6 PERSON DETECTION MODULE`
7. `7 EVALUATION AND RESULTS`
8. `8 CONCLUSION AND FUTURE WORK`

---

## 1. 核心摘要 (TL;DR)
本研究設計並實作了一款具備社會意識（Socially Cognizant）的自主校園導覽機器人，旨在協助迷路學生導引方向。系統採用跨領域與利害關係人共同設計方法，整合語音與觸控互動、改進型動態扇形成本地圖（Social Costmap）以及深度相機行人偵測，並在室內環境完成了獨立與整合的系統模組評估（evaluation in isolation and in concert）。

## 2. 研究背景與痛點 (Problem Statement)
- **校園迷路問題** `[paper2.pdf, 1 INTRODUCTION, 2 DESIGN CONTEXT]`：  
  大學校園幅員遼闊且建築眾多（例如 Rutgers 大學佔地超過 6,000 英畝、擁有超過 900 棟建築），新生或訪客極易迷路（例如誤以為 PH-111 在物理系館，實則在藥學院），造成遲到與困擾。
- **公共場所機器人的社會可接受性挑戰** `[paper2.pdf, 1 INTRODUCTION]`：  
  移動機器人走入公共場合時，其行為必須符合社會接受度（socially acceptable），需在設計初期便考量機器人與使用者、旁觀者之間的互動動態。
- **利害關係人洞察** `[paper2.pdf, 2.2 Stakeholder Engagement]`：  
  團隊與學生迎新與轉銜計畫辦公室（RUDSOTP）討論，利害關係人指出部分學生會對向陌生人問路感到退縮，因而歡迎自動化系統；但同時也提出機器人可能缺乏人情味（human touch）、以及在擁擠區域可能造成困擾等顧慮。

## 3. 系統架構與技術方法 (Methodology & Architecture)
- **硬體平台** `[paper2.pdf, 3 SYSTEM OVERVIEW]`：  
  採用 LoCoBot WX250S 作為基礎移動平台，搭載觸控螢幕、麥克風、揚聲器與 Intel RealSense D435 RGB-D 相機。
- **語音模組 (Speech Module)** `[paper2.pdf, 4 SPEECH MODULE]`：  
  當麥克風音量超過分貝閾值時開始聆聽，支援雙模式：
  1. *導引模式 (Guidance mode)*：由關鍵字（如 "take", "guide", "bring"）觸發，確認資料庫有該地點後直接移動導航帶路。
  2. *指示模式 (Instruction mode)*：預設模式，由問句觸發（如 "How do I get to..."），調用 OpenAI API（GPT 模型），結合預先建立的環境文字描述生成導航文字並朗讀。
- **改進型社交導航模組 (Navigation Module)** `[paper2.pdf, 5 NAVIGATION MODULE]`：  
  基於 ROS Navigation stack 與 2D Costmap。原本的社會導航層（Pablo de Olavide 大學插件）對移動中的人僅建立圓角長條型成本區，假定人只會直線前進；本研究將移動者的成本區改進為**圓形扇區（sector of a circle）**：
  > 原文短句引用：*"The velocity of the person is proportional to the radius of the sector (faster people cover more distance), and inversely proportional to the angle swept by the sector (faster people are less likely to change direction quickly)."*  
  （扇形半徑與人移動速度成正比，扇形張角與人移動速度成反比）。
- **行人偵測模組 (Person Detection Module)** `[paper2.pdf, 6 PERSON DETECTION MODULE]`：  
  使用 Intel RealSense D435 相機搭配 YOLOv5 偵測行人邊界框（Bounding box），並取邊界框內的深度數據以計算行人 3D 空間位置：
  > 原文短句引用：*"the most reliable method we found was to take the 25th percentile depth point in the bounding box."*  
  （取邊界框內第 25 百分位數深度點）。

## 4. 使用者研究與實驗設計 (User Study & Evaluation)
- **實驗環境** `[paper2.pdf, 7 EVALUATION AND RESULTS]`：  
  由於機器人移動能力限制，評估在一處具代表性的室內空間進行，分別對各模組及整合系統進行測試。
- **具體量化數據與原文出處** `[paper2.pdf, 7 EVALUATION AND RESULTS]`：
  1. *行人偵測距離限制*：  
     > 原文短句引用：*"We found that there were no significant differences between the performance of these systems when a person was within 4.4 meters of the robot. Our system’s performance degraded beyond that point."*  
     （與 LIDAR 比較，在 4.4 公尺內偵測效能無顯著差異，超過 4.4 公尺效能下降）。
  2. *語音模組測試*：  
     > 原文短句引用：*"The speech detection module successfully understood the utterances of users for all of the conditions tested. However, it was observed to have difficulty understanding some non-American accents."*  
     （所有測試條件下皆成功辨識，但觀察到對某些非美式口音理解有困難）。
  3. *靜態避障導航成功率*：  
     > 原文短句引用：*"The navigation module successfully planned and executed motion to the desired location in four out of five trials. The robot was able to avoid collisions with static people in the environment."*  
     （靜態人體環境下，5 次試驗中有 4 次成功規劃並導航至目標，成功率 4/5）。
  4. *動態避障導航模擬測試*：  
     因目前視覺偵測尚無法直接估算行人速度，團隊透過模擬輸入速度評估扇形 Costmap：  
     > 原文短句引用：*"Because our person detection system does not provide velocities of people, we had to simulate this input to evaluate the changes we made to the navigation module. We found that the robot successfully avoided the moving person for each of its five trials."*  
     （在 5 次模擬試驗中，機器人每次均成功避開移動中的行人，共 5 次試驗）。
  5. *端到端整合測試 (End-to-End Trials)*：  
     > 原文短句引用：*"The end-to-end process from speech or touch command to collision-free guidance to the desired destination was shown to be successful and reliable on each of the nine trials."*  
     （從語音／觸控指令到無碰撞導引的完整流程，在全部 9 次試驗中皆成功）。

## 5. 主要發現與研究限制 (Key Findings & Limitations)
- **主要發現** `[paper2.pdf, 7 EVALUATION AND RESULTS, 8 CONCLUSION AND FUTURE WORK]`：  
  社會認知導航扇區設計能兼顧行人動向的不確定性；語音與觸控雙模態互動能提供靈活求助途徑。
- **研究限制與未來工作 (Future Work)** `[paper2.pdf, 6 PERSON DETECTION MODULE, 8 CONCLUSION AND FUTURE WORK]`：
  - *速度估算缺失*：目前視覺系統因缺乏個體追蹤（lack of individuation of people），無法直接估算行人即時速度（velocities），導致動態扇形 Costmap 僅能先以模擬速度驗證。作者計畫在未來改進偵測模組以支援真實世界測試（*"Moving forward, we will continue improving the robotic campus guide by developing a new person detection module that provides the velocities of people."*）。
  - *社會接受度尚未評估*：作者明確表示尚未在真實社群進行廣泛社會接受度與滿意度評估，列為未來工作計畫（*"Future work includes... evaluating social acceptance."*、*"We also plan to get feedback from community members..."*）。
  - *未實作功能 (Not Implemented)*：利害關係人會議中提及的遠端視訊通話功能、多語言切換功能、以及面向使用者的鏡頭仰角互動等，論文均明確標註「尚未實作（has not been implemented）」。

## 6. 課堂報告亮點與啟發 (Takeaways for Presentation)
> ⚠️ **註：以下內容為整理者之教學詮釋與報告建議，非論文原文主張。**

1. **跨領域與利害關係人前期參與的重要性**：  
   在開發公共服務機器人時，納入社會科學人員與校園行政單位（RUDSOTP）能在硬體成型前釐清非技術需求（例如學生害怕與真人交談 vs 缺乏人情味的兩難），並提示了 QR code 等備案設計。
2. **「非社交」到「社交」導航演進的代表範例**：  
   論文清楚示範了如何將傳統僅考慮幾何障礙物的「反社交（antisocial）」ROS Navigation 疊加動態扇形 Costmap，將人類運動速度與轉向不確定性數學化，是非常直觀且具體的演算法教學案例。
3. **實驗限制的誠實揭露**：  
   論文誠實區分了「真實感測（靜態 4.4 米內有效）」與「模擬輸入（動態行人速度需先以模擬測試）」，展現了雛形系統迭代研發中的典型技術瓶頸與驗證策略。

## 7. 相關概念雙向連結 (Related Concepts)
- [導航、空間感知與協同移動](../concepts/navigation-co-navigation.md)
- [對話與語言互動機制](../concepts/dialogue-interaction.md)
- [應用場景與使用者族群](../concepts/application-domains.md)
- [角色定位與人機互動模式](../concepts/robot-roles.md)
