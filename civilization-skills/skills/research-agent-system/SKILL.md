# Research Agent System Skill（研究型多 Agent 技能）

Status: `DRAFT`

## Purpose（目的）

把一個研究題目拆成多個專家 Agent，透過檔案交接、引用標註、交叉審核，產出可用於簡報、論文、課程或治理決策的深度報告。

## When to Use（使用時機）

- AI 共智課程研究
- TED / 論文蒸餾
- 全人健康 / 神經科學 / 意識研究
- 產學合作報告
- AI 工具或模型深度評估
- 嘉年華會復盤報告

## Agent Roles（Agent 分工）

```text
1. Research PM（研究專案經理）
2. Literature Agent（文獻智能體）
3. Data Agent（資料智能體）
4. Technology Agent（技術分析智能體）
5. Market / Application Agent（市場與應用智能體）
6. Risk Agent（風險智能體）
7. Synthesis Agent（整合智能體）
8. QA Agent（交叉審核智能體）
9. Executive Writer（高層報告撰寫智能體）
```

## File Handoff Rule（檔案交接規則）

研究任務必須產出中間檔：

```text
outputs/phase-1-literature.md
outputs/phase-2-analysis.md
outputs/phase-3-risk.md
outputs/phase-4-synthesis.md
outputs/final-report.md
outputs/references.md
outputs/gaps-and-unknowns.md
outputs/lessons-learned.md
```

## Source Rule（來源規則）

重要結論必須標示來源類型：

- Academic Paper（學術論文）
- Official Documentation（官方文件）
- Company Blog（公司技術部落格）
- Industry Report（產業報告）
- News（新聞）
- Unknown（未確認）

## QA Gate（品質閘門）

最終報告前必須檢查：

- 引用完整性
- 資料衝突
- 未知資訊
- 事實與推論分離
- 非技術讀者可讀性
- 是否可進入課程資料庫

## Outputs（輸出）

```text
Final Report（最終報告）
Executive Summary（高層摘要）
References（參考來源）
Gaps and Unknowns（缺口與未知）
Lessons Learned（經驗總結）
Reusable Skill Update（可複用技能更新建議）
```

## Lessons Learned（實戰教訓）

深度研究不應只靠單一 AI 長篇回答。高品質研究需要角色分工、檔案交接、來源標註、交叉審核與經驗總結。
