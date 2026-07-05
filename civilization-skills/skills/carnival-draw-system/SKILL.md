# Carnival Draw System Skill（嘉年華抽籤系統技能）

Status: `DRAFT`

## Purpose（目的）

把嘉年華展位抽籤器事件沉澱成可復用技能，未來任何抽籤、分配、排序、現場流程小工具都可先載入本技能，避免再次失控。

## Scope（範圍）

此技能適用於：

- 展位位置抽籤
- 志工分組
- 體驗路線分派
- 小規模公平分配工具

## Minimal User-Facing Rule（前台最小呈現規則）

抽籤頁只呈現必要資訊：

```text
展位名稱
展位號碼
限定 3 日內完成
```

不放不必要的隱私、權利、複雜治理說明。

## Governance Requirements（治理要求）

- Production Draw（正式抽籤）預設 frozen（凍結）
- Test Draw（測試抽籤）必須與正式資料分離
- Formal Release（正式放行）需 Gina APR
- Deadline（期限）必須明確
- Admin Proxy（管理員代抽）需記錄理由與操作者
- Audit Log（稽核紀錄）必須可查

## QA Checklist（驗收清單）

- 測試抽籤不污染正式資料
- 正式抽籤未核定前不可寫入
- deadline 過後一般使用者不可抽籤
- admin proxy 可追溯
- 使用者頁面簡潔
- 統計資料可查
- legacy data（既有資料）未被覆蓋

## Stop Rule（停止規則）

若出現以下任一情況，立即停止：

- 正式資料被測試污染
- Agent 無法確認 freeze 狀態
- QA 與實際頁面不一致
- 抽籤結果不可追溯
- 需求開始擴張超過抽籤本身

## Lessons Learned（實戰教訓）

抽籤只是確認展位位置，不應過度設計成高隱私、高權利風險流程。治理要抓住真實風險，不要讓過度治理壓垮小工具。
