# QA Validation Skill（驗收技能）

Status: `DRAFT`

## Purpose（目的）

讓 QA（驗收）不只檢查「功能有沒有動」，也檢查流程、證據、未知、Agent 偏離與使用者實際觀察。

## When to Use（使用時機）

- CC 回報已完成
- Lovable / 亮亮 / 其他 Agent 回報已修正
- 小程序準備進入 beta（測試）或 production（正式生產）
- 使用者回報與 Agent 回報不一致

## Inputs（輸入）

- Task brief（任務簡述）
- Expected behavior（預期行為）
- Actual behavior（實際行為）
- Test evidence（測試證據）
- Screenshots / logs（截圖 / 日誌，若有）

## Outputs（輸出）

```text
QA Status（驗收狀態）: PASS / FAIL / BLOCKED / PARTIAL
Verified Evidence（已驗證事實）:
Inference（模式推論）:
Hypothesis（假設性解讀）:
Unknown（未確認資訊）:
Required Fix（必要修正）:
Next Gate（下一閘門）:
```

## Validation Checklist（驗收清單）

- 主要使用者路徑可完成
- 錯誤狀態可辨識
- 沒有新增未授權功能
- 沒有跳過安全或 APR
- Agent 回報與實際測試一致
- Unknown（未確認資訊）已標示
- 若發現衝突資料，已列為 Conflict Detected（資料衝突）

## Stop Rule（停止規則）

若 QA 連續 2 輪發現同一類錯誤，必須停止繼續修正，改走 Zara Decision（Zara 裁決）。

## Lessons Learned（實戰教訓）

抽籤器事件顯示：QA 不能只驗 endpoint（端點）或頁面狀態，也要驗任務是否偏離、Agent 是否卡住、流程是否已經超出原始需求。
