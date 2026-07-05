# REPOSITORY_HYGIENE_V1（倉庫整潔規則）

Status: `DRAFT`

## Purpose（目的）

避免 Git 倉庫因重複資料夾、平行技能庫、未整理研究材料、產物檔案與大型附件而膨脹。

## Current Scan（目前掃描）

已確認：

- Repository（倉庫）: `5D-GINA/google-skills`
- Default branch（預設分支）: `main`
- Repo size（倉庫大小）: 約 `486 KB`
- Existing scope（既有範圍）: Google Agent Skills（Google 技術技能）
- Existing skill root（既有技能根目錄）: `skills/cloud/`

## Boundary Decision（邊界裁定）

Civilization Skills（文明技能）不放入 `skills/cloud/`，避免與 Google 技術技能混雜。

統一新增於：

```text
civilization-skills/
```

## Do Not Add（禁止新增）

不要新增下列平行資料夾：

```text
agent-skills/
five-d-skills/
skill-library/
civilization-skill-library/
research-skills/
workflow-skills/
```

若需要新增內容，先放入：

```text
civilization-skills/inbox/
```

等 Zara Review（Zara 審閱）後再移入正式 skills。

## File Size Rule（檔案大小規則）

不得直接提交：

- 影片
- 音檔
- 大型 PDF
- 大型圖片
- 匯出 zip
- build output（建置產物）
- node_modules
- raw transcript（未蒸餾逐字稿）

上述資料應放外部儲存或 Obsidian raw vault，再以摘要、引用與連結進入 Git。

## Skill File Rule（技能檔案規則）

每個 Skill 以 Markdown 小檔為主：

```text
SKILL.md
checklist.md
lessons-learned.md
```

避免把完整文章、長逐字稿或未蒸餾材料直接塞進 Git。

## Review Trigger（審閱觸發）

若新增超過 10 個檔案、單次變更超過 500 行、或出現大型附件，必須觸發 Repository Hygiene Review（倉庫整潔審閱）。
