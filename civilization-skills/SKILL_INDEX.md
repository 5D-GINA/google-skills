# Skill Index（技能索引）

Status: `V1_FRAMEWORK_DRAFT`

## Governance Documents（治理文件）

| File | Purpose |
|---|---|
| `governance/SKILL_STANDARD_V1.md` | 所有 Civilization Skills（文明技能）的母標準 |
| `governance/AGENT_STOP_RULE_V1.md` | 防止 Agent 無限修正、無限消耗 |
| `governance/COST_GATE_V1.md` | 成本與時間失控前的停止閘門 |
| `governance/EVIDENCE_REQUIREMENT_V1.md` | 事實、推論、假設、未知的標示規則 |
| `governance/REPOSITORY_HYGIENE_V1.md` | 避免 Skill 資料夾重複與 Git 倉庫膨脹 |
| `governance/AGENT_TRIGGER_HYGIENE_V1.md` | 避免 Agent 名稱錯置、Issue 錯位造成觸發誤判 |

## Skills（技能）

| Skill | Path | Use Case |
|---|---|---|
| Release Governance Skill（發布治理技能） | `skills/release-governance/SKILL.md` | App / 頁面 / Agent / workflow 上線前 |
| QA Validation Skill（驗收技能） | `skills/qa-validation/SKILL.md` | 驗證功能、流程、證據、未知 |
| Agent Handoff Skill（Agent 交接技能） | `skills/agent-handoff/SKILL.md` | 換視窗、換 Agent、跨階段交接 |
| Agent Execution Discipline Skill（Agent 執行紀律技能） | `skills/agent-execution-discipline/SKILL.md` | 檢查計劃遵循、偏離、停止條件 |
| Research Agent System Skill（研究型多 Agent 技能） | `skills/research-agent-system/SKILL.md` | 論文、TED、深度研究、課程素材 |
| Agent Team Health Skill（Agent 團隊健康技能） | `skills/agent-team-health/SKILL.md` | 檢查 Agent 是否過度受控、卡死或失去判斷力 |
| Carnival Draw System Skill（嘉年華抽籤系統技能） | `skills/carnival-draw-system/SKILL.md` | 把抽籤器教訓沉澱成可復用技能 |
| AI Morning Report Skill（AI 晨報技能） | `skills/ai-morning-report/SKILL.md` | 每日 AI 新聞、安全、TED/論文、AI 英文 |

## Do Not Duplicate（避免重複）

不要再新增平行目錄：

```text
agent-skills/
five-d-skills/
skill-library/
civilization-skill-library/
```

統一使用：

```text
civilization-skills/
```
