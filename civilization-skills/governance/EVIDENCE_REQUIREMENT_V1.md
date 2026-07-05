# EVIDENCE_REQUIREMENT_V1（證據要求）

Status: `DRAFT`

## Purpose（目的）

確保 Agent 輸出不把未驗證資訊包裝成確定事實，讓治理判斷可以追溯。

## Required Labels（必要標籤）

### Verified Evidence（已驗證事實）

已經由檔案、測試、來源、工具輸出或可查證紀錄支持的資訊。

### Inference（模式推論）

根據已驗證事實推導出的合理判斷，但不是直接證據。

### Hypothesis（假設性解讀）

可能成立、值得探索，但目前證據不足的解讀。

### Unknown（未確認資訊）

目前無法確認、未找到來源、資料衝突或尚未驗證的資訊。

## Report Rule（回報規則）

每份 QA Report（驗收報告）、Research Report（研究報告）、Audit Report（稽核報告）至少要包含：

```text
Verified Evidence（已驗證事實）:
Inference（模式推論）:
Hypothesis（假設性解讀）:
Unknown（未確認資訊）:
```

## Conflict Rule（資料衝突規則）

若來源互相矛盾，必須標示：

```text
Conflict Detected（資料衝突）
Source A:
Source B:
Current Judgment:
Unknown:
```

不得自行選擇看起來比較順的資料寫成確定事實。

## APR Rule（核定規則）

進入 APR（核定）前，Unknown（未確認資訊）必須清楚列出。

若 Unknown 涉及安全、正式發布、使用者權益、金流或個資，不得核定正式上線。
