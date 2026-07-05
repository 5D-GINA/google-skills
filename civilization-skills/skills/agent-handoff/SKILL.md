# Agent Handoff Skill（Agent 交接技能）

Status: `DRAFT`

## Purpose（目的）

避免換視窗、換 Agent、跨工具或跨階段時失去上下文，讓下一位 Agent 能快速接手，不需 Gina 反覆搬運。

## When to Use（使用時機）

- 換 ChatGPT 視窗
- 從 Zara 交給 CC
- 從 CC 交給 Hermes
- 從 Lovable / 亮亮交給 Zara
- 任務進入下一階段
- 長任務暫停後恢復

## Required Handoff（必要交接內容）

```text
Task（任務）:
Current Status（目前狀態）:
Done（已完成）:
Not Done（未完成）:
Blocking Issues（阻塞事項）:
Files / URLs（檔案或連結）:
Evidence（證據）:
Unknown（未知）:
Next Agent（下一位 Agent）:
Next Action（下一步）:
Stop Rule Status（停止規則狀態）:
APR Needed（是否需要核定）:
```

## File Handoff Rule（檔案交接規則）

重要任務不得只靠對話交接，必須產出 Markdown 交接檔：

```text
handoff.md
qa-report.md
lessons-learned.md
```

## Non-Negotiables（不可偏離紅線）

不得只說：

```text
已完成，請下一位繼續。
```

必須說清楚完成範圍、未完成範圍、證據與未知。

## Lessons Learned（實戰教訓）

抽籤器事件顯示：Agent 團隊若只靠聊天接力，容易出現上下文遺失、需求變形、QA 漏檢與重複修正。
