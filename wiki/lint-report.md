# Lint 檢查報告 (Wiki Lint Report)

本文件依據 `AGENTS.md` 規範記錄所有單篇驗證（檢查點 A）與全局檢查（檢查點 B）之檢查日期、發現問題與修正紀錄。

---

## 檢查紀錄

### 2026-11-22 | 檢查點 A：人工對照 PDF 審查與問題修正 (Paper 1)
- **檢查檔案**：`wiki/papers/paper1-dialogue-authoring.md`、`wiki/concepts/dialogue-interaction.md`
- **發現問題**：
  1. 數值過度推斷：原筆記將圖表範例數值「5 詞／90 字元」寫為「預設」，但正文未給出具體數值。
  2. 推論與實證混淆：TL;DR 將推測性陳述寫為確定成效（「大幅降低」應為「旨在減輕」）。
  3. 出處與情境誤植：第 4 節將 Section 3.2 針對遙控者距離感的個人使用經驗誤寫為系統評估的驗證基礎。
  4. 章節性質標示不清：未明確標示 Section 4 為「FUTURE WORK」，且「行內編輯」未標記為作者建議（"We recommend"）。
  5. 課堂詮釋未清楚標示：第 6 節未標明為整理者詮釋，並出現論文未使用的詞彙（如「過度聚焦於自主性」、「雙贏」、「Cognitive Distance」、「範本推薦」）。
- **修正動作**：
  1. 刪除數值，修正為「（論文未給具體數值）」，並同步更新概念頁。
  2. TL;DR 調整為「旨在減輕照護者開發對話內容的技術門檻與無形勞動負擔」。
  3. 第 4 節刪除不合情境之描述，標註 Section 4 為 FUTURE WORK（4.1 屬未來實驗規劃）。
  4. 第 5 節澄清論文無獨立 Limitations 章節，主要挑戰列於 Section 3，未來工作列於 Section 4，並將行內編輯標為作者建議。
  5. 第 6 節頂部追加「以下為整理者詮釋，非論文原文」警語，刪除未出現名詞，「範本推薦」更正為「從預設清單隨機選取」。
  6. 更新 `wiki/log.md` 紀錄。檢查點 A 複驗通過。

### 2026-11-22 | 檢查點 A：單篇出處與格式驗證 (Paper 2)
- **檢查檔案**：`wiki/papers/paper2-campus-guide.md`
- **核對項目**：
  1. 章節出處忠實性：確認嚴格使用 PDF 實際標題（如 1 INTRODUCTION, 2.1, 2.2, 3, 4, 5, 6, 7, 8），無自行臆測。
  2. 數值與原文短句：感測距離（4.4 meters）、演算法參數（25th percentile）、實驗次數（4 out of 5, 5, 9 trials）均附完整英文短句引用。
  3. 未實作功能明確標註：視訊通話、多語言切換等均如實標註為 "has not been implemented"。
  4. 課堂詮釋警語：第 6 節開頭清楚標註整理者詮釋警語，未使用論文未出現之杜撰術語。
- **檢查結果**：通過。

### 2026-11-22 | 檢查點 A：單篇出處與格式驗證 (Paper 3)
- **檢查檔案**：`wiki/papers/paper3-campus-robot-trust.md`
- **核對項目**：
  1. 章節出處忠實性：確認嚴格使用 PDF 實際標題（如 1 Introduction, 2.1-2.4, 3.1-3.4, 4.1, 4.2.1-4.2.4, 4.3.1-4.3.2, 5.1-5.2, 6, 7）。
  2. 數值與原文短句：受試者規模（59 participants, 44 questionnaire, 17 interview, 2 both）、性別年齡（67% male / 33% female, median 29 SD=4.9）、熟悉度統計檢定（p < .05, M=2.61 vs 1.90）、標籤統計（61 labels, 7 categories）均附完整英文短句引用。
  3. 課堂詮釋警語：第 6 節開頭清楚標註整理者詮釋警語。
- **檢查結果**：通過。

### 2026-11-22 | 檢查點 A：單篇出處與格式驗證 (Paper 4)
- **檢查檔案**：`wiki/papers/paper4-joint-dialog-navigation.md`
- **核對項目**：
  1. 章節出處忠實性：確認嚴格使用 PDF 實際標題（如 I. INTRODUCTION, II, III, IV.A-B, V, VI.A-D, VII）。
  2. 數值與原文短句：模擬環境（10 house instances, 3 domains, 4 feature slots）、獎勵噪聲（Rmax=1.0, R=-0.01, noise 0.1, 0.05）、神經網路參數（MLP 64, LSTM 256, 5,000,000 timesteps, batch 4096）均附完整英文短句引用。
  3. 課堂詮釋警語：第 6 節開頭清楚標註整理者詮釋警語。
- **檢查結果**：通過。

### 2026-11-22 | 檢查點 A：單篇出處與格式驗證 (Paper 5)
- **檢查檔案**：`wiki/papers/paper5-narrative-remote-guide.md`
- **核對項目**：
  1. 章節出處忠實性：確認嚴格使用 PDF 實際標題（如 1 Introduction, 2.1-2.3, 3.1-3.4, 4.1-4.3, 5.1-5.4, 6.1-6.2, 7）。
  2. 數值與原文短句：展品分佈（68 exhibits, 23 across 3 zones, 11 selected）、計時閾值（45-second period of silence）、受試者人口統計（20 participants, 8 women 12 men, age 19-77, $15 USD）、成對 t 檢定數據（t(19)=4.06, p=0.0007）均附完整英文短句引用。
  3. 課堂詮釋警語：第 6 節開頭清楚標註整理者詮釋警語。
- **檢查結果**：通過。

### 2026-11-22 | 檢查點 A：單篇出處與格式驗證 (Paper 6)
- **檢查檔案**：`wiki/papers/paper6-codesign-newcomer-learning.md`
- **核對項目**：
  1. 章節出處忠實性：確認嚴格使用 PDF 實際標題（如 1 Introduction, 2.1-2.3, 3.1-3.4, 4 Discussion and Future Work, 5 Conclusion）。
  2. 數值與原文短句：專家參與者（4 participants: 2 L2 tutors with 7 and 2.5 years, 2 HRI researchers）、會議時長（one 60-minute online meeting）、缺課比例（three out of eight sessions）、學童定義（past five years）、未來規劃（children aged 5-10, approx 4 children）均附完整英文短句引用。
  3. 實驗狀態忠實性：明確標註為專家共同設計報告，尚未進行長程兒童實驗（4 Discussion and Future Work 屬未來規劃）。
  4. 課堂詮釋警語：第 6 節開頭清楚標註整理者詮釋警語。
- **檢查結果**：通過。

---

### 2026-11-22 | 深度查核：Paper 2 至 Paper 6 數字、出處、TL;DR 語氣詞與 PDF 驗證

#### 1. 原始論文 PDF 驗證（paper3.pdf 與 paper5.pdf）
- **`raw/paper3.pdf`**：
  - **ACM 官方版權頁與封面**：第 1 頁具備 ACM Digital Library 官方下載封面頁（DOI: 10.1145/3764687.3764717，收錄於 OZCHI '25，ISBN: 9798400720161）；第 2 頁（正文第 176 頁）具備標準 ACM 版權許可宣告區塊（Creative Commons Attribution 4.0 International License, OZCHI '25, Sydney, Australia）。
  - **參考文獻完整性**：正文第 10~11 頁（刊物頁碼 184~185）完整列出 47 篇學術參考文獻（[1] Andy Alorwu... 至 [47] James E. Young...），並附有 Appendix A~E。
  - **結論**：確認為標準原始學術研討會論文 PDF。
- **`raw/paper5.pdf`**：
  - **ACM 官方版權頁與封面**：第 1 頁具備 ACM Digital Library 官方下載封面頁（DOI: 10.1145/3746059.3747697，收錄於 UIST '25，ISBN: 9798400720376）；第 2 頁具備標準 ACM 版權宣告區塊（UIST '25, Busan, Republic of Korea, ACM ISBN 979-8-4007-2037-6/25/09）。
  - **參考文獻完整性**：正文第 15~16 頁完整列出 69 篇學術參考文獻（[1] Josh Achiam... 至 [69] Paul T, ot, a...）。
  - **結論**：確認為標準原始學術研討會論文 PDF。

#### 2. Paper 2 至 Paper 6 具體數字與 PDF 出處完整核對表

| 論文編號 | Wiki 所在小節 | 具體數字／量化項目 | PDF 實際章節標題 | PDF 頁碼 | PDF 英文原文短句 (Exact Short Quote) | 驗證狀態 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Paper 2** | 2. 研究背景與痛點 | 6,000 英畝 (acres) | `1 INTRODUCTION` | p. 1229 | *"Rutgers University spans over six thousand acres"* | ✅ 驗證核可 |
| **Paper 2** | 2. 研究背景與痛點 | 900 棟建築 (buildings) | `1 INTRODUCTION` | p. 1229-1230 | *"and consists of over nine hundred buildings [1]."* | ✅ 驗證核可 |
| **Paper 2** | 2. 研究背景與痛點 | PH-111 演講廳編號 | `2 DESIGN CONTEXT` | p. 1230 | *"the lecture hall named PH-111 is in the Physics Building... in the Pharmacy Building"* | ✅ 驗證核可 |
| **Paper 2** | 3. 系統架構與技術方法 | WX250S 底座型號 | `3 SYSTEM OVERVIEW` | p. 1231 | *"leveraged a LoCoBot WX250S robot as the base platform."* | ✅ 驗證核可 |
| **Paper 2** | 3. 系統架構與技術方法 | D435 相機型號 | `6 PERSON DETECTION MODULE` | p. 1232 | *"used the Intel Realsense D435 camera at our disposal"* | ✅ 驗證核可 |
| **Paper 2** | 3. 系統架構與技術方法 | 第 25 百分位數 (25th percentile) | `6 PERSON DETECTION MODULE` | p. 1232 | *"take the 25th percentile depth point in the bounding box."* | ✅ 驗證核可 |
| **Paper 2** | 4. 使用者研究與實驗設計 | 4.4 公尺感測極限 | `7 EVALUATION AND RESULTS` | p. 1232 | *"when a person was within 4.4 meters of the robot. Our system’s performance degraded beyond that point."* | ✅ 驗證核可 |
| **Paper 2** | 4. 使用者研究與實驗設計 | 5 次試驗中成功 4 次 (4/5) | `7 EVALUATION AND RESULTS` | p. 1232 | *"planned and executed motion to the desired location in four out of five trials."* | ✅ 驗證核可 |
| **Paper 2** | 4. 使用者研究與實驗設計 | 5 次模擬動態避障試驗 | `7 EVALUATION AND RESULTS` | p. 1232 | *"avoided the moving person for each of its five trials."* | ✅ 驗證核可 |
| **Paper 2** | 4. 使用者研究與實驗設計 | 9 次端到端完整測試 | `7 EVALUATION AND RESULTS` | p. 1232 | *"guidance to the desired destination was shown to be successful and reliable on each of the nine trials."* | ✅ 驗證核可 |
| **Paper 3** | 1. 核心摘要 (TL;DR) | 59 位師生受試者 | `4 Results` | p. 179 | *"collected data from 59 participants, of whom 44 answered the questionnaires and 17 attended the interview sessions (two participants did both)."* | ✅ 驗證核可 |
| **Paper 3** | 3. 系統架構與技術方法 | 1.2 公尺高 (1.2-meter-tall) | `3 Study Design` | p. 178 | *"employed Pepper, a 1.2-meter-tall, wheeled, programmable humanoid social robot."* | ✅ 驗證核可 |
| **Paper 3** | 3. 系統架構與技術方法 | 60 分鐘訪談時長 | `3.3 Interviews` | p. 179 | *"series of 60-minute, semi-structured interviews."* | ✅ 驗證核可 |
| **Paper 3** | 4. 使用者研究與實驗設計 | 44 名問卷、17 名訪談、2 名重疊 | `4 Results` | p. 179 | *"44 answered the questionnaires and 17 attended the interview sessions (two participants did both)."* | ✅ 驗證核可 |
| **Paper 3** | 4. 使用者研究與實驗設計 | 訪談性別：男 67% (N=10), 女 33% (N=5) | `4.1 Demographics...` | p. 179 | *"Within the interview group, 67% (N = 10) identified as male and 33% (N = 5) as female, with no participants identifying as non-binary."* | ✅ 驗證核可 |
| **Paper 3** | 4. 使用者研究與實驗設計 | 問卷性別：男 61% (N=27), 女 36% (N=16), 非二元 2% (N=1) | `4.1 Demographics...` | p. 179 | *"Questionnaire participants comprised 61% male (N = 27), 36% female (N = 16), and 2% non-binary (N = 1)."* | ✅ 驗證核可 |
| **Paper 3** | 4. 使用者研究與實驗設計 | 年齡中位數：訪談 29 歲 (SD=4.9), 問卷 28 歲 (SD=5.9) | `4.1 Demographics...` | p. 179 | *"The median age for interview participants was 29 years (SD = 4.9), and 28 years for the other group (SD = 5.9)."* | ✅ 驗證核可 |
| **Paper 3** | 4. 使用者研究與實驗設計 | 學生佔比：訪談 67% (N=10), 問卷 66% (N=29) | `4.1 Demographics...` | p. 179 | *"67% (N = 10) of interview participants were students and 33% (N = 5) were non-students. Similarly, among questionnaire participants, 66% (N = 29) were students and 34% (N = 15) were non-students."* | ✅ 驗證核可 |
| **Paper 3** | 4. 使用者研究與實驗設計 | 科技背景：訪談 47% (N=7), 問卷 64% (N=28) | `4.1 Demographics...` | p. 179 | *"47% (N = 7) of interview participants were in tech-related areas, 47% (N = 7) were outside of tech, and 7% (N = 1) unclear, whereas for questionnaire participants, 64% (N = 28) were in tech-related areas and 36% (N = 16) outside tech."* | ✅ 驗證核可 |
| **Paper 3** | 4. 使用者研究與實驗設計 | 國籍比例：訪談亞洲 60% (N=9)、問卷亞洲 41% (N=18) 等 | `4.1 Demographics...` | p. 180 | *"predominantly from Asia (60%, N = 9), followed by Europe (13%, N = 2)... Questionnaire participants showed... Asia (41%, N = 18)"* | ✅ 驗證核可 |
| **Paper 3** | 4. 使用者研究與實驗設計 | 熟悉度均值 2.3；性別檢定：男 M=2.61 vs 女 M=1.90, p < .05 | `4.1 Demographics...` | p. 180 | *"averaging 2.3 (SD = 1.0 and SD = 1.1 respectively)... male participants overall (M = 2.61, SD = 1.10) reporting higher familiarity than female participants (M = 1.90, SD = 0.91), p < .05."* | ✅ 驗證核可 |
| **Paper 3** | 4. 使用者研究與實驗設計 | 報酬價值：約 20 歐元、約 10 歐元 | `3.2 Questionnaires` | p. 179 | *"valued at around 20 EUR. For the second questionnaire, participants were rewarded a prize valued at around 10 EUR"* | ✅ 驗證核可 |
| **Paper 3** | 4. 使用者研究與實驗設計 | 發想標籤：61 個獨立標籤，7 大類別 | `4.3.1 Ideation...` | p. 181 | *"collected all the ideas submitted by the participants and organised them into 61 unique labels... organised these labels into seven categories"* | ✅ 驗證核可 |
| **Paper 3** | 5. 主要發現與研究限制 | 第 8 個特徵 (eighth key characteristic) | `4.2.4 Characterisation...` | p. 181 | *"extension of the framework with an eighth key characteristic, transparency and security."* | ✅ 驗證核可 |
| **Paper 4** | 3. 系統架構與技術方法 | MLP 64 單元, LSTM 256 單元 | `VI.B Experiment Settings` | p. 7897 | *"first two layers have an MLP layer of 64 units with tanh activation as a hidden layer. The output of the second layer is fed into the LSTM layer with 256 units."* | ✅ 驗證核可 |
| **Paper 4** | 4. 使用者研究與實驗設計 | 10 個房屋實例, 3 個區域, 4 個槽位 | `VI.A Simulator Design` | p. 7896 | *"consists of 10 house instances. Each house instance has three domains (“livingroom”, “kitchen”, and “bedroom”), each with 4 feature slots."* | ✅ 驗證核可 |
| **Paper 4** | 4. 使用者研究與實驗設計 | 獎勵參數：Rmax = 1.0, 負獎勵 R = -0.01 | `VI.A Simulator Design` | p. 7897 | *"returns a positive reward Rmax = 1.0 when all user requirements are satisfied and a negative reward R = −0.01 otherwise."* | ✅ 驗證核可 |
| **Paper 4** | 4. 使用者研究與實驗設計 | 噪聲機率：回饋反向 0.1, 機器導航 0.9, 人類走偏 0.05 | `VI.A Simulator Design` | p. 7897 | *"noise with a 0.1 probability of being opposite... navigate to its goal location in 0.9 probability. The user follows the robot in presence of a 0.05 probability noise"* | ✅ 驗證核可 |
| **Paper 4** | 4. 使用者研究與實驗設計 | 5,000,000 訓練步數, batch 4096, γ=0.99, α=0.002, ϵ=0.1 | `VI.B Experiment Settings` | p. 7897 | *"spends 5, 000, 000 timesteps for each run to learn a joint policy... batch size of 4096. The discounting factor γ is 0.99, the learning rate α is 0.002, and clip size ϵ is 0.1."* | ✅ 驗證核可 |
| **Paper 4** | 4. 使用者研究與實驗設計 | 每 100,000 步評估 100 回合 | `VI.B Experiment Settings` | p. 7897 | *"for 100 independent episodes every 100, 000 timestep"* | ✅ 驗證核可 |
| **Paper 4** | 4. 使用者研究與實驗設計 | 真實環境包含 3 個房間 | `VI.D Demonstration...` | p. 7897 | *"traversing an environment where three rooms exist."* | ✅ 驗證核可 |
| **Paper 4** | 5. 主要發現與研究限制 | 100 次運行評估 | `VI.C Results` | p. 7897 | *"agent’s success rate and episode length over 100 runs."* | ✅ 驗證核可 |
| **Paper 4** | 5. 主要發現與研究限制 | 約 95% 任務完成率 | `VI.C Results`, `Fig. 3a` | p. 7897 | *"Joint Policy could achieve the highest success rate"*（註：95% 係依據 Fig. 3a 柱狀圖高度估計，正文未列小數值） | ✅ 圖表可驗證 |
| **Paper 4** | 5. 主要發現與研究限制 | 平均約 28 步 vs 基線 35~50 步 | `VI.C Results`, `Fig. 3b` | p. 7897 | *"and a shorter episode length"*（註：28 步與 35~50 步係依據 Fig. 3b 箱型圖中位數估計，正文未列小數值） | ✅ 圖表可驗證 |
| **Paper 4** | 5. 主要發現與研究限制 | 共處率接近 0.98 | `VI.C Results`, `Fig. 3c` | p. 7897 | *"Joint Policy has the highest proximity rate"*（註：0.98 係依據 Fig. 3c 柱狀圖高度估計，正文未列小數值） | ✅ 圖表可驗證 |
| **Paper 5** | 1. 核心摘要 (TL;DR) | 20 名受試者實地研究 | `4 User Study`, `4.1` | p. 7-8 | *"We recruited 20 participants (P1–20; eight women, twelve men)"* | ✅ 驗證核可 |
| **Paper 5** | 3. 系統架構與技術方法 | 全館 68 展品, 取 3 區 23 展品, 精選 11 展品 | `3.4 System Deployment` | p. 7 | *"68 exhibits in total across four areas... comprising 23 exhibits across three zones... selection of 11 exhibits"* | ✅ 驗證核可 |
| **Paper 5** | 3. 系統架構與技術方法 | 45 秒靜默主動發話計時閾值 | `3.3.3 Dialogue System` | p. 6 | *"initiates a social chat after a 45-second period of silence. The 45-second time-lapse is selected based on experimental results from pilot tests"* | ✅ 驗證核可 |
| **Paper 5** | 4. 使用者研究與實驗設計 | 20 名受試者：8 女、12 男, 19–77 歲, M=29, SD=13.57 | `4.1 Participants` | p. 8 | *"recruited 20 participants (P1–20; eight women, twelve men) aged 19–77 (M = 29, SD = 13.57)"* | ✅ 驗證核可 |
| **Paper 5** | 4. 使用者研究與實驗設計 | 11 位先前曾造訪該博物館 | `4.1 Participants` | p. 8 | *"Among the 20 participants, 11 have been to the geology museum before the study."* | ✅ 驗證核可 |
| **Paper 5** | 4. 使用者研究與實驗設計 | 15 美元受試者報酬 | `4.1 Participants` | p. 8 | *"Each participant was compensated with $15 USD for their participation."* | ✅ 驗證核可 |
| **Paper 5** | 4. 使用者研究與實驗設計 | 參觀 20 分鐘，至少 5 個展品 | `4.2 Task and Procedure` | p. 8 | *"explore the museum for 20 minutes and visit at least five exhibits."* | ✅ 驗證核可 |
| **Paper 5** | 4. 使用者研究與實驗設計 | 3 位受試者僅體驗 10 分鐘，2 位遭遇重複規劃 | `5 Findings` | p. 9 | *"three participants (P2, 4, 13) experienced only 10 minutes of the tour... issues of the robot planner with two participants (P6, 7)"* | ✅ 驗證核可 |
| **Paper 5** | 4. 使用者研究與實驗設計 | 推薦接受 M=2.90 (STD=2.32) vs 拒絕 M=0.9 (STD=0.99), t(19)=4.06, p=0.0007 | `5.1 Quantitative Results` | p. 9 | *"significantly more acceptance (M = 2.90 times, STD = 2.32 times) than rejections (M = 0.9 times, STD = 0.99 times) in responding to the robot suggestions [t(19) = 4.06, p = 0.0007]."* | ✅ 驗證核可 |
| **Paper 5** | 4. 使用者研究與實驗設計 | 高階指令 M=7.90 (STD=4.17) vs 低階 M=7.35 (STD=7.26), t(19)=0.32, p=0.75 | `5.1 Quantitative Results` | p. 9 | *"no statistically significant result was found for the difference between the usage of high-level instructions (M = 7.90 times, STD = 4.17 times) and low-level instructions (M = 7.35 times, STD = 7.26 times) when controlling the robot [t(19) = 0.32, p = 0.75]."* | ✅ 驗證核可 |
| **Paper 5** | 4. 使用者研究與實驗設計 | 展品詢問 M=14.65 (STD=9.41) vs 控制 M=15.50 (STD=9.36), t(19)=-0.25, p=0.80 | `5.1 Quantitative Results` | p. 9 | *"not significantly different between the amount of museum inquiry speeches (M = 14.65 times, STD = 9.41 times) and robot control commands (M = 15.50 times, STD = 9.36 times) [t(19) = −0.25, p = 0.80]."* | ✅ 驗證核可 |
| **Paper 5** | 5. 主要發現與研究限制 | 自我延伸化身受試者 4 位 (P1, 15, 16, 18) | `5.2.4 As a representation of self` | p. 9 | *"Four participants (P1, 15, 16, 18) saw the robot as an extension of themselves."* | ✅ 驗證核可 |
| **Paper 5** | 5. 主要發現與研究限制 | 自主掌控感分佈：7 位高、8 位混合、5 位低 | `5.3.2 Dialogue for Robot Control` | p. 10 | *"Seven participants (P1, 3, 4, 7, 11, 14, 17) highlighted the sense of autonomy... eight participants (P5, 8, 9, 10, 12, 13, 15, 20) reported a mixed sense... five participants (P2, 6, 16, 18, 19) reported low sense of control"* | ✅ 驗證核可 |
| **Paper 5** | 5. 主要發現與研究限制 | 偏好遇到旁觀者受試者 7 位 (P10, 12, 15, 16, 18–20) | `5.4.2 Favoring Bystander...` | p. 12 | *"Encountering bystanders was favorable for seven participants (P10, 12, 15, 16, 18–20)"* | ✅ 驗證核可 |
| **Paper 6** | 2. 研究背景與痛點 | 過去 5 年內抵達之新移民兒童 | `1 Introduction` | p. 36 | *"migrated to Canada within the past five years and are in the process of learning English as an additional language"* | ✅ 驗證核可 |
| **Paper 6** | 2. 研究背景與痛點 | 8 次課程中僅出席 3 次 | `3.1.1 Language Barriers...` | p. 37 | *"some children attend as few as three out of eight sessions... irregular attendance makes it difficult"* | ✅ 驗證核可 |
| **Paper 6** | 3. 系統架構與技術方法 | ROBOTIS Engineer Kit 1 組裝平台 | `2.2 Robotic System Overview` | p. 37 | *"assembled from the ROBOTIS Engineer Kit 1"* | ✅ 驗證核可 |
| **Paper 6** | 3. 系統架構與技術方法 | 4 位專家參與者 (2 導師, 2 研究者) | `2.1 Co-designers` | p. 37 | *"design team comprised four participants: two expert second-language (L2) tutors from UFL... and two Human–Robot Interaction (HRI) researchers"* | ✅ 驗證核可 |
| **Paper 6** | 3. 系統架構與技術方法 | 導師資歷：7 年 與 2.5 年 | `2.1 Co-designers` | p. 37 | *"One L2 expert was a regional manager... with seven years of experience, and the other L2 expert was a Program Support Staff... for two and a half years"* | ✅ 驗證核可 |
| **Paper 6** | 3. 系統架構與技術方法 | 60 分鐘線上共同設計會議 | `2.3 Procedure and Analysis` | p. 37 | *"conducted one 60-minute online co-design meeting with the participants as a group over Microsoft Teams."* | ✅ 驗證核可 |
| **Paper 6** | 4. 使用者研究與實驗設計 | 未來規劃：約 4 名 5–10 歲學童 | `4 Discussion and Future Work` | p. 39 | *"children aged between 5-10 years old and would be coordinated with UFL... interaction, that will have approximately four children."* | ✅ 驗證核可 |
| **Paper 6** | 5. 主要發現與設計準則 | 5 項初步設計準則 (Guideline 1~5) | `3.4 Preliminary Design Guidelines` | p. 38-39 | *"outline a set of preliminary design guidelines for a peer SAR robot (3.4.1 Guideline 1 to 3.4.5 Guideline 5)"* | ✅ 驗證核可 |

#### 3. 各篇 TL;DR 強語氣詞之原文依據查核表

| 論文編號 | TL;DR 使用之強語氣詞彙 | PDF 原文詞彙與出處章節 | 刊物頁碼 | 原文短句佐證與說明 |
| :--- | :--- | :--- | :--- | :--- |
| **Paper 2** | 「實證評估」 | `7 EVALUATION AND RESULTS` | p. 1232 | *"System modules were evaluated independently, as well as in concert... The end-to-end process from speech or touch command to collision-free guidance... was shown to be successful and reliable on each of the nine trials."*（論文第 7 節專門進行評估實驗，用語有據）。 |
| **Paper 2** | 「共同設計」 | `2.2 Stakeholder Engagement` | p. 1230 | *"crucial to identify and engage with as many stakeholders as possible... RUDSOTP... provided valuable input during our design process."*（論文透過利益相關者會議進行需求探討，符合共同設計參與原則）。 |
| **Paper 3** | 「核心基石」 | `1 Introduction`, `5.2 Transparency...` | p. 176, 183 | *"we highlight operational and operator transparency as keys for gaining users’ trust in on-campus social robots."* 及 *"We identified transparency as a critical aspect influencing users’ trust"*（原文使用 "keys" 與 "critical aspect"，以「核心基石」詮釋合乎原文意旨）。 |
| **Paper 3** | 「擴充」 | `1 Introduction`, `4.2.4` | p. 177, 181 | *"we put forward extensions to Hancock et al.’s Factors of Trust [15] and to Baraka et al.’s social robot characterisation framework [2]."*（原文直接使用 "extensions" 與 "extension of the framework"，完全吻合）。 |
| **Paper 4** | 「顯著優於」 | `Abstract`, `I. INTRODUCTION`, `VI.C` | p. 7893, 7897 | *"We show that our approach outperforms baselines from the literature in task completion rate and execution time"* 及 *"Both figures demonstrate that our approach outperforms the baselines."*（原文使用 "outperforms"，表意直接且經 100 次運行數據支持）。 |
| **Paper 4** | 「真實世界機器人驗證」 | `VI.D Demonstration in the Real World` | p. 7897 | *"We have demonstrated our approach using a real robot. We deployed our joint policy model on a segway-based mobile robot. The robot interacts with a human while traversing an environment where three rooms exist."*（章節標題即為 "Demonstration in the Real World"，具實體機實驗支援）。 |
| **Paper 5** | 「實地研究」 | `Abstract`, `1 Introduction` | p. 2, 3 | *"We deployed our prototype in a geology museum, where remote participants (n = 20) used the robot to tour the museum."* 及 *"Conducted field studies in a genuine geology museum"*（原文明確使用 "field studies in a genuine geology museum"，實地部署無誤）。 |
| **Paper 6** | 「共同設計 (Co-design)」 | `論文標題`, `Abstract`, `1 Introduction` | p. 36 | 標題為 *"Co-designing a Social Robot..."*，內文 *"This research presents a co-design study with program tutors and coordinators... conducted a co-design meeting"*（原文核心方法即為 co-design）。 |
| **Paper 6** | 「資深」 | `2.1 Co-designers`, `1 Introduction` | p. 36, 37 | *"two expert second-language (L2) tutors from UFL... with seven years of experience"* 及 *"expert-grounded insights"*（原文使用 "expert" 且導師具備 7 年與 2.5 年資歷，以「資深專家導師」表述合乎事實）。 |

