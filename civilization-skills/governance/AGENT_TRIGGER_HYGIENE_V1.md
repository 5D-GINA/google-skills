# AGENT_TRIGGER_HYGIENE_V1（Agent 觸發衛生規則）

Status: `DRAFT`

## Purpose（目的）

避免因 Agent 名稱錯置、任務 ID 錯誤、Issue 錯位或未定義代稱，造成觸發失敗或誤判自動化失效。

白話：
先確認喊對人，再判斷人有沒有來。

## Canonical Names（標準名稱）

AI Office（AI 辦公室）中的 Agent 必須使用固定稱呼：

```text
Gina（司令官）
Zara（參謀總長）
Hermes（H先生）
CC（Codex）
JOES（文書）
亮亮（Lovable）
```

## Trigger Rule（觸發規則）

每次觸發 Agent 任務時，指令必須包含：

```text
Task ID（任務 ID）:
Target Agent（目標 Agent）:
Canonical Name（標準名稱）:
Target Repo（目標倉庫）:
Target Issue / PR（目標 Issue / PR）:
Required Output（必要回報）:
Non-Authorization（非授權事項）:
```

## Name Hygiene（名稱衛生）

不得使用未定義代稱，例如：

```text
G先生
那位稽核員
剛剛那個 Agent
他
她
```

若需使用暱稱，必須同時附標準名稱：

```text
Hermes（H先生）
亮亮（Lovable）
```

## Failure Diagnosis（觸發失敗診斷）

若 Agent 未回應，不得立即推論為自動化失效。

必須先檢查：

1. Agent 名稱是否正確。
2. Issue / PR 是否正確。
3. Repo 是否正確。
4. Task ID 是否唯一。
5. 指令是否明確要求回覆位置。
6. 是否誤寫未定義代稱。
7. 是否有 Dashboard Visibility（儀表板可見性）欄位。

## Correction Rule（更正规則）

若發現觸發名稱錯誤，必須：

1. 修正原留言或新增更正留言。
2. 標示 `TRIGGER_CORRECTED`。
3. 重新記錄測試起點。
4. 不得使用錯誤留言作為觸發失敗證據。

## Required Report（必要回報格式）

```text
Trigger Status（觸發狀態）: PASS / FAIL / CORRECTED / UNKNOWN
Target Agent（目標 Agent）:
Canonical Name（標準名稱）:
Issue / PR（觸發位置）:
Correction Needed（是否需更正）:
Verified Evidence（已驗證事實）:
Unknown（未確認資訊）:
```

## Lessons Learned（實戰教訓）

一次將 Hermes（H先生）誤寫為 G先生，可能導致 Agent 無法被正確點名，進而讓團隊誤判觸發失敗。Agent Swarm（Agent 編隊）必須治理「名字漂移」，否則小錯字會造成大排查。
