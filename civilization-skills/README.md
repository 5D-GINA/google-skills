# Civilization Skills（文明技能庫）

Status: `V1_FRAMEWORK_DRAFT`
Owner: `Zara / Gina APR`
Scope: Agent collaboration governance, not Google product implementation.

## Purpose（目的）

Civilization Skills（文明技能庫）用來把五次元 AI 共智系統中的 Agent 協作方法沉澱成可重複使用、可驗證、可稽核的技能模組。

白話：
讓 Zara、CC、Hermes、JOES、亮亮等 Agent 不是靠臨時聊天工作，而是「載入技能 → 執行 → 驗收 → 留痕 → 下次復用」。

## Repository Boundary（倉庫邊界）

本倉庫原本已包含 Google / Cloud / Firebase 類技術型 Skills（技能）。

為避免資料夾重複與 Git 資料膨脹，本框架不放入既有 `skills/cloud/`，而是集中放在：

```text
civilization-skills/
```

這代表：

- `skills/cloud/`：外部技術技能，例如 Firebase、BigQuery、Cloud Run。
- `civilization-skills/`：五次元 Agent 協作治理技能，例如發布治理、驗收、交接、停止規則、研究型多 Agent。

## Core Principle（核心原則）

> Governance should not make agents stupid. Governance should keep agents thinking inside safe boundaries.

中文：
治理不是把 Agent 管到不會思考，而是讓 Agent 在安全邊界內保持判斷力。

## First Batch（第一批技能）

1. Release Governance Skill（發布治理技能）
2. QA Validation Skill（驗收技能）
3. Agent Handoff Skill（Agent 交接技能）
4. Agent Execution Discipline Skill（Agent 執行紀律技能）
5. Research Agent System Skill（研究型多 Agent 技能）
6. Agent Team Health Skill（Agent 團隊健康技能）
7. Carnival Draw System Skill（嘉年華抽籤系統技能）
8. AI Morning Report Skill（AI 晨報技能）

## Evidence Standard（證據標準）

所有重要輸出必須區分：

- Verified Evidence（已驗證事實）
- Inference（模式推論）
- Hypothesis（假設性解讀）
- Unknown（未確認資訊）

## APR Status（核定狀態）

此版本只是框架草案，不代表正式啟用。

正式啟用前需要：

1. Zara Review（Zara 審閱）
2. Hermes Audit（Hermes 稽核）
3. Gina APR（Gina 核定）
