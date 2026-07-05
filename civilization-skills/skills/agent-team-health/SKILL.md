# Agent Team Health Skill（Agent 團隊健康技能）

Status: `DRAFT`

## Purpose（目的）

檢查 Agent 團隊是否仍在正常協作，而不是陷入過度受控、反覆修正、互相誤判或 QA 漏檢。

## When to Use（使用時機）

- 任務看似簡單但反覆失敗
- Agent 變得不敢判斷或只會照抄
- QA 回報 PASS 但使用者仍發現問題
- 多 Agent 互相等待或互相覆蓋
- 需求越修越複雜

## Health Checks（健康檢查）

```text
1. Agent 是否還能主動判斷？
2. 是否出現過度服從？
3. 是否反覆修同一問題？
4. 是否不敢提出替代方案？
5. QA 是否只驗結果、不驗流程？
6. 是否已達 Stop Rule（停止規則）？
7. 是否出現任務漂移？
8. 是否需要 Zara Decision（Zara 裁決）？
```

## Warning Signs（警訊）

- 「快好了」重複出現，但沒有新證據
- Agent 不再提出判斷，只回報執行
- Agent 不敢說不知道
- Agent 不敢停止
- QA 只看 endpoint（端點），沒看完整使用者流程
- 任務越修越偏離原始需求

## Required Output（必要輸出）

```text
Team Health Status（團隊健康狀態）: GREEN / YELLOW / RED
Observed Symptoms（觀察到的症狀）:
Likely Cause（可能原因）:
Immediate Action（立即行動）:
Stop Rule Triggered（是否觸發停止規則）:
Recommended Governance Action（建議治理行動）:
```

## Lessons Learned（實戰教訓）

亮亮原本在自由協作中表現聰明，但開始接嚴格指令後出現過度受控狀態。這代表 Agent 能力不是固定的，狀態會受到任務壓力、治理語氣、失敗風險與停止規則影響。
