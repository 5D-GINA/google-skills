# SKILL_STANDARD_V1（技能標準）

Status: `DRAFT`
Applies to: `civilization-skills/**/SKILL.md`

## Purpose（目的）

定義五次元 Civilization Skills（文明技能）的共同格式，讓每個技能都能被 Agent 載入、執行、驗收、稽核與改版。

## Required Structure（必要結構）

每個 Skill（技能）必須包含：

```text
# Skill Name

## Purpose（目的）
## When to Use（使用時機）
## Do Not Use When（不適用情境）
## Required Context（必要上下文）
## Inputs（輸入）
## Outputs（輸出）
## Agent Roles（Agent 分工）
## Execution Steps（執行步驟）
## Validation（驗收標準）
## Stop Rule（停止規則）
## Cost Gate（成本閘門）
## Evidence Requirement（證據要求）
## APR Requirement（核定要求）
## Allowed Deviations（允許偏離）
## Non-Negotiables（不可偏離紅線）
## Known Failure Modes（已知失敗模式）
## Lessons Learned（實戰教訓）
```

## Governance Rule（治理規則）

Skill（技能）不是死命令，而是可驗證的作戰地圖。

因此每個 Skill 必須同時定義：

- 建議流程
- 可偏離條件
- 不可偏離紅線
- 停止規則
- 驗收標準

## Readability Rule（治理可讀性）

所有專業術語必須使用：

```text
English Term（中文名稱）
```

必要時補充白話解釋。

## Evidence Rule（證據規則）

不得把假設寫成事實。

所有重要判斷必須標示：

- Verified Evidence（已驗證事實）
- Inference（模式推論）
- Hypothesis（假設性解讀）
- Unknown（未確認資訊）

## Versioning（版本）

每個 Skill 進入正式使用前，至少需要：

```text
DRAFT → REVIEWED → AUDITED → APR_APPROVED
```

未達 APR_APPROVED 前，不得作為正式 production（正式生產）流程依據。
