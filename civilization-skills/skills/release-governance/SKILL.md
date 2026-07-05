# Release Governance Skill（發布治理技能）

Status: `DRAFT`

## Purpose（目的）

防止 App、頁面、Agent workflow（工作流）或小工具在未完成驗收、未確認邊界、未處理風險前進入 production（正式生產）。

## When to Use（使用時機）

- 新功能準備上線
- 小程序準備交給外部使用者
- 需要解除 freeze（凍結）
- 涉及正式資料、正式抽籤、正式公告
- Agent 已完成但尚未驗收

## Inputs（輸入）

- Release target（發布目標）
- Current state（目前狀態）
- QA results（驗收結果）
- Known risks（已知風險）
- Rollback plan（回滾計劃）

## Outputs（輸出）

- Release Readiness Report（發布就緒報告）
- QA Summary（驗收摘要）
- Risk Register（風險清單）
- Go / No-Go Recommendation（放行 / 不放行建議）

## Agent Roles（Agent 分工）

- Zara: 定義發布邊界與裁決建議
- CC: 執行技術檢查與 sandbox validation（沙盒驗證）
- Hermes: read-only audit（唯讀稽核）
- Gina: APR（最終核定）

## Execution Steps（執行步驟）

1. 確認 release scope（發布範圍）。
2. 確認 production write（正式生產寫入）是否仍 frozen（凍結）。
3. 檢查 QA report（驗收報告）。
4. 檢查 Stop Rule（停止規則）是否被觸發。
5. 檢查 Cost Gate（成本閘門）。
6. 檢查 rollback plan（回滾方案）。
7. 輸出 Go / No-Go。

## Validation（驗收標準）

- 功能通過 sandbox test（沙盒測試）
- 使用者路徑可完成
- 無未處理 critical risk（重大風險）
- 有 rollback plan（回滾方案）
- Unknown（未確認資訊）已列出

## Non-Negotiables（不可偏離紅線）

不得跳過：

- QA Validation（驗收）
- Security Review（安全檢查）
- APR（核定）
- Rollback Plan（回滾方案）

## Lessons Learned（實戰教訓）

抽籤器事件顯示：小程序也需要 release governance（發布治理）。功能看似簡單，但 Agent 協作、QA、freeze、deadline、proxy path 等流程若未收斂，仍可能造成混亂。
