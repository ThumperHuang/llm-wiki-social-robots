# 社交機器人的設計與應用：LLM Wiki

> 以 **LLM Wiki** 方法，將 6 篇 HRI 論文整理成可追溯來源的知識庫，並據此製作教學型 HTML 簡報。

## 專案簡介

- **主題**：社交機器人的設計與應用（Design and Application of Social Robots）
- **對象**：初學者
- **語言**：繁體中文，保留英文術語
- **核心原則**：
  - `raw/` 內的 PDF 為唯讀來源
  - Wiki 內容只根據 PDF 撰寫
  - 事實主張標註論文與章節
  - 推測、計畫與已驗證結果分開呈現
  - 整理者的詮釋要明確標示

## 建議閱讀順序

1. [wiki/index.md](wiki/index.md)：Wiki 首頁與導讀
2. [wiki/synthesis.md](wiki/synthesis.md)：6 篇論文的橫向比較
3. `wiki/concepts/`：5 篇概念頁
4. `wiki/papers/`：6 篇論文筆記
5. [slides.html](slides.html)：教學簡報（用瀏覽器開啟，左右鍵切換）
6. [docs/process.md](docs/process.md)：Loop／Graph 流程說明、執行紀錄與反思

## 資料夾結構

```text
my-wiki/
├── AGENTS.md          # 給 AI 的工作規範（流程圖、檢查點、格式模板）
├── README.md          # 本檔案
├── slides.html        # 教學型 HTML 簡報（單一檔案，不需網路）
├── raw/               # 原始論文 PDF（唯讀）
├── wiki/
│   ├── index.md       # 首頁與導讀
│   ├── synthesis.md   # 橫向比較
│   ├── log.md         # 操作日誌
│   ├── lint-report.md # Lint 報告
│   ├── papers/        # 6 篇論文筆記
│   └── concepts/      # 5 篇概念頁
└── docs/
    └── process.md     # 流程說明、執行與檢查紀錄、反思
```

## 納入的 6 篇論文

| 編號 | 論文 | 會議／年份 | 主題 |
|---|---|---|---|
| paper1 | A Robot Dialogue Authoring Interface with Smart Capabilities | HRI '24 Companion | 對話編寫介面 |
| paper2 | Development of a Socially Cognizant Robotic Campus Guide | HRI '24 Companion | 校園導覽機器人 |
| paper3 | Factors of Trust for Successfully Adopting Social Robots on the Campus | OZCHI '25 | 校園中的信任因素 |
| paper4 | Learning Joint Policies for Human-Robot Dialog and Co-Navigation | IROS 2023 | 對話與共同導航的聯合策略 |
| paper5 | NarraGuide: an LLM-based Narrative Mobile Robot for Remote Place Exploration | UIST '25 | LLM 敘事導覽 |
| paper6 | Co-designing a Social Robot for Newcomer Children's Cultural and Language Learning | HRI Companion '26 | 新移民兒童語言學習 |

## 5 篇概念頁

- `dialogue-interaction`：對話互動
- `navigation-co-navigation`：導航與共同導航
- `trust-transparency`：信任與透明性
- `robot-roles`：機器人角色
- `application-domains`：應用場域

## 工作流程（Loop）

1. **Ingest**：逐篇閱讀 PDF，產生論文筆記
2. **檢查點 A**：每篇完成後，對照 PDF 驗證章節、數字與用詞
3. **概念頁與整合**：建立概念頁、`synthesis.md`、`index.md`
4. **檢查點 B**：全局 Lint（死連結、無出處主張、孤立頁面）
5. **簡報**：只用 Wiki 內容產生 `slides.html`，每頁標註來源
6. **文件**：整理流程說明、檢查紀錄與反思

流程圖與逐節點說明請見 [docs/process.md](docs/process.md)。

## 品質檢查與限制

- 檢查點 A 曾發現並修正：
  - 數字過度推論
  - 把推測寫成已證實
  - 把未來工作混入研究結果
- Lint 只檢查連結、孤立頁面與出處標註格式，**不保證事實正確**。事實依靠人工對照 PDF 抽查。
- 簡報與概念頁中的整理者詮釋，皆已標示為詮釋，不是論文原文。
- 詳細紀錄見 [wiki/lint-report.md](wiki/lint-report.md) 與 [wiki/log.md](wiki/log.md)。

## 使用說明

- 閱讀 Wiki：用 VS Code、Antigravity 或任何 Markdown 預覽工具開啟 `wiki/index.md`。
- 觀看簡報：直接用 Chrome 或 Edge 開啟 `slides.html`。
  - 按 `←`、`→` 切換頁面。
