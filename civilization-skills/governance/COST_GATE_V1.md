# COST_GATE_V1（成本閘門）

Status: `DRAFT`

## Purpose（目的）

讓 Agent 在時間、token、外部服務費用、人工注意力開始失控前主動停止或升級裁決。

## Cost Types（成本類型）

- Token Cost（Token 成本）
- Human Attention Cost（人工注意力成本）
- Tool Usage Cost（工具使用成本）
- Deployment Risk Cost（部署風險成本）
- Opportunity Cost（機會成本）

## Gate Levels（閘門分級）

### Green（綠燈）

條件：

- 小修正
- 可回滾
- 不寫 production（正式生產）
- 低風險

處置：Agent 可繼續。

### Yellow（黃燈）

條件：

- 已進入第 2 輪修正
- 需求開始變形
- 驗收結果不穩定
- 需要跨 Agent 協調

處置：需要 Zara Review（Zara 審閱）。

### Red（紅燈）

條件：

- 連續 3 輪未通過驗收
- 需要 production write（正式生產寫入）
- 涉及外部公開使用者
- 涉及金流、個資、正式抽籤、正式公告

處置：停止，等待 Gina APR（Gina 核定）。

## Required Cost Report（成本回報格式）

```text
Estimated Cost（預估成本）:
Spent Cost（已消耗成本）:
Remaining Risk（剩餘風險）:
Gate Level（目前閘門）:
Recommendation（建議）:
```

## Lesson Learned（實戰教訓）

小程序也可能因為多 Agent 反覆修正而產生高成本。成本不是只看金錢，也要看 Gina 的注意力與治理判斷消耗。
