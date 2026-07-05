# AGENT_STOP_RULE_V1（Agent 停止規則）

Status: `DRAFT`

## Purpose（目的）

防止 Agent 在任務失控時持續消耗時間、成本與上下文，尤其避免「快好了」但反覆修不完的情況。

## Default Stop Conditions（預設停止條件）

任務符合任一條件，必須停止並回報：

1. 同一任務連續 3 輪未通過驗收。
2. 同一問題被修正 2 次後仍重現。
3. Agent 無法說明目前阻塞原因。
4. Agent 無法提出可驗證的下一步。
5. QA（驗收）與實際使用者觀察不一致。
6. 任務開始新增原本未授權的功能。
7. 任務需要 production write（正式生產寫入）但未取得 APR。

## Required Stop Report（停止回報格式）

```text
Status（狀態）:
Task（任務）:
Completed（已完成）:
Failed（未完成）:
Repeated Failure（重複失敗）:
Evidence（證據）:
Unknown（未知）:
Recommended Decision（建議裁決）:
```

## Non-Negotiables（不可偏離紅線）

Agent 不得以「即將完成」為理由繼續繞過停止規則。

若 Stop Rule（停止規則）觸發，必須交由：

```text
Zara Decision → Gina APR（必要時）
```

## Lesson Learned（實戰教訓）

抽籤器事件顯示：若沒有明確 Stop Rule（停止規則），多 Agent 團隊可能在小程序上持續修正、持續驗收、持續失控，直到人工強制收斂。
