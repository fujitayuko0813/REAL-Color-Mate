# CHANGELOG

All notable changes for REAL Color Mate Version 2.0.

---

## [2.0] - 2026-08-04

### Documentation Refactoring (No Specification Changes)

#### Changed

- **AGENTS.md**: Refactored to remove duplicated technical specifications
  - Replaced technical specifications with references to MASTER_SPECIFICATION.md
  - Reorganized file structure for clarity
  - Kept only operational guidance and AI collaboration rules
  - Status: Specifications preserved, operational guidance clarified

- **.github/copilot-instructions.md**: Updated reading order and references
  - Changed reading order to: MASTER_SPECIFICATION.md → CHANGELOG.md → AGENTS.md
  - Added "Single Source of Truth" emphasis for MASTER_SPECIFICATION.md
  - Updated all specification references to point to MASTER_SPECIFICATION.md
  - Version bumped to 2.0
  - Status: Reading order clarified, references verified

#### Verified

- ✅ MASTER_SPECIFICATION.md remains unchanged (Single Source of Truth)
- ✅ All project specifications preserved
- ✅ No hardware specifications modified
- ✅ No software specifications modified
- ✅ No optical specifications modified
- ✅ No calibration specifications modified
- ✅ Documentation is internally consistent
- ✅ No broken internal links
- ✅ Repository structure unchanged

### Rationale

This refactoring improves separation of responsibilities:
- MASTER_SPECIFICATION.md: Official specifications (authority)
- AGENTS.md: Operational guidance and AI collaboration rules
- .github/copilot-instructions.md: Copilot-specific workflow instructions

The refactoring maintains all project decisions while clarifying documentation structure.

---

## [2.0.1] - 2026-08-05

### AI Collaboration Rules (Non-functional changes)

#### Added

- **AGENTS.md**: Added AI 共通ルールの改善
  - ビルド・コンパイル整合性チェックをレビュー項目に追加（Arduino / OpenSCAD / KiCad / ドキュメント）
  - Unknown 管理ルールを明確化（MASTER_SPECIFICATION への記載、Issue 連携、担当決定～承認～仕様更新～CHANGELOG 反映までのフロー）
  - Evidence（根拠）を必須化（許容される根拠の例を列挙）
  - レビュー結果の分類を追加（PASS / MINOR / MAJOR / BLOCKER）
  - Definition of Done（レビュー完了条件）を追加

- **.github/copilot-instructions.md**: 役割分離を明確化（Copilot 専用ルールのみを記載）

- **docs/github_ai_workflow.md**: AI 共同開発のワークフロー補助資料を追加

#### Rationale

- 既存仕様には変更を加えず、AI 関係ドキュメントの運用・レビュー手順の改善を行いました。

---
