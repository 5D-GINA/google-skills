# Agent Execution Discipline Skill（Agent 執行紀律技能）

Status: `DRAFT`

## Purpose（目的）

檢查 Agent 是否真的依照任務目標執行，並區分合理偏離與執行崩潰。

白話：
不要只看 Agent 有沒有說「我理解了」，要看它實際做了什麼。

## When to Use（使用時機）

- 任務有明確計劃
- Agent 開始跳步
- Agent 做了計劃外操作
- Agent 過度服從壞計劃
- Agent 回報與實際結果不一致

## Plan Compliance Check（計劃遵循檢查）

每次交付都要回答：

```text
Original Plan（原計劃）:
Executed Steps（實際執行）:
Skipped Steps（跳過步驟）:
Added Steps（新增步驟）:
Deviation Reason（偏離原因）:
Validation After Deviation（偏離後驗證）:
```

## Smart Deviation Rule（智慧偏離規則）

允許偏離：

- 原計劃明顯不適用
- 原步驟會造成死循環
- 有更低風險方案可達成目標
- 環境條件不存在
- 可先回報再請 Zara Decision（Zara 裁決）

禁止偏離：

- 跳過 QA
- 跳過 Security Review（安全檢查）
- 跳過 APR
- 跳過來源標註
- 未說明原因直接改 production

## Bad Plan Risk（壞計劃風險）

壞計劃可能比沒有計劃更危險。

因此任務開始前要檢查：

- 計劃是否過度細碎？
- 是否把建議路徑寫成死命令？
- 是否有 Stop Rule（停止規則）？
- 是否有 Validation（驗證）？
- 是否允許合理偏離？
- 是否明確定義不可偏離紅線？

## Lessons Learned（實戰教訓）

亮亮在自由協作時表現聰明，但在過度受控的治理指令下可能變成不敢判斷、不敢重構、不敢停止。治理必須保留 Agent 的判斷力，而不是把 Agent 壓成機械執行器。
