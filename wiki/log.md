# 操作紀錄 (Wiki Maintenance Log)

本文件依據 `AGENTS.md` 規範記錄知識庫之所有 Ingest、Lint、修正與生成歷程。

| 日期 | 操作 | 影響檔案 | 備註 |
| :--- | :--- | :--- | :--- |
| 2026-11-21 | Init | AGENTS.md | 建立初始 LLM Wiki 維護規範與目錄架構 |
| 2026-11-22 | Config | AGENTS.md | 調整 5.1 節批次彈性、目錄架構、模板連結、Ingest/Lint 規則與檢查點定義 |
| 2026-11-22 | Ingest | wiki/papers/paper1-dialogue-authoring.md, wiki/index.md, wiki/concepts/dialogue-interaction.md, wiki/concepts/robot-roles.md, wiki/concepts/application-domains.md, wiki/log.md | 完成 Paper 1 文獻吸納，更新 index.md 與相關概念頁，通過單篇檢查點 A |
| 2026-11-22 | Fix (Checkpoint A) | wiki/papers/paper1-dialogue-authoring.md, wiki/concepts/dialogue-interaction.md, wiki/lint-report.md, wiki/log.md | 依人工審閱（檢查點 A 查核）修正 Paper 1：更正斷句未給具體數值、修正推論用詞、明確標註 Section 4 為 FUTURE WORK、標記第 6 節為整理者詮釋並移除未出現之詞彙 |
| 2026-11-22 | Ingest | wiki/papers/paper2-campus-guide.md, wiki/index.md, wiki/concepts/navigation-co-navigation.md, wiki/log.md | 完成 Paper 2 文獻吸納，更新 index.md 與導航概念頁，具體數值皆附原文短句，通過單篇檢查點 A |
| 2026-11-22 | Ingest | wiki/papers/paper3-campus-robot-trust.md, wiki/index.md, wiki/concepts/trust-transparency.md, wiki/log.md | 完成 Paper 3 文獻吸納，更新 index.md 與信任概念頁，所有受試者數據皆附原文短句，通過單篇檢查點 A |
| 2026-11-22 | Ingest | wiki/papers/paper4-joint-dialog-navigation.md, wiki/index.md, wiki/concepts/navigation-co-navigation.md, wiki/concepts/dialogue-interaction.md, wiki/log.md | 完成 Paper 4 文獻吸納，更新 index.md 與導航／對話概念頁，所有模擬與網路參數皆附原文短句，通過單篇檢查點 A |
| 2026-11-22 | Ingest | wiki/papers/paper5-narrative-remote-guide.md, wiki/index.md, wiki/concepts/dialogue-interaction.md, wiki/concepts/trust-transparency.md, wiki/concepts/robot-roles.md, wiki/log.md | 完成 Paper 5 文獻吸納，更新 index.md 與相關概念頁，所有受試者數據與統計檢定皆附原文短句，通過單篇檢查點 A |
| 2026-11-22 | Ingest | wiki/papers/paper6-codesign-newcomer-learning.md, wiki/index.md, wiki/concepts/robot-roles.md, wiki/concepts/application-domains.md, wiki/log.md | 完成 Paper 6 文獻吸納，更新 index.md 與相關概念頁，專家資歷與共同設計參數皆附原文短句，通過單篇檢查點 A |
| 2026-11-22 | Audit (Lint) | wiki/lint-report.md, wiki/log.md | 執行 Paper 2～6 深度數字與出處全面核對，驗證 raw/paper3.pdf 與 raw/paper5.pdf 論文原始性，產出數值清單與 TL;DR 語氣詞佐證表 |
| 2026-11-22 | Synthesize (Concepts) | wiki/concepts/*.md, wiki/log.md | 依 AGENTS.md 6.2 節重構 5 篇核心概念專頁（各篇 300–500 字，含出處章節、原文短句、衝突觀點並列與推測/實證區分） |
