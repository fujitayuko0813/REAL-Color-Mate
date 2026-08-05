# REAL Color Mate - AI 開発ガイド (AGENTS.md)

バージョン: 2.0.1
最終更新: 2026-08-05

目的

この文書は REAL Color Mate プロジェクトにおけるAI共通ルール（すべてのAIエージェントに適用）を定義します。Copilot固有のルールは含まず、.github/copilot-instructions.md を参照してください。

基本方針

- MASTER_SPECIFICATION.md が唯一の仕様書（Single Source of Truth）です。仕様の変更は明示的な承認を受けた場合のみ許可されます。
- 既存の設計・仕様を勝手に変更してはなりません。
- Unknown（仕様未確定事項）は推測して埋めないでください。Unknown は必ず追跡・解決します（Unknown 管理ルール参照）。
- 提案やレビューは常に Evidence（根拠）を付けてください（Evidenceの例は下記）。
- 変更履歴は CHANGELOG.md に追記してください。

適用範囲

- 本書は ChatGPT、Gemini、Copilot 等、プロジェクト内で利用されるすべてのAIに適用されます。
- Copilot専用のコード生成方針やコメントスタイル等は .github/copilot-instructions.md に記載し、本書では参照のみとします。

レビュー手順（共通）

以下の観点に基づいてレビューを実施します。ビルド・コンパイル整合性チェックを必須レビュー項目として追加しています。

1. 仕様整合
   - MASTER_SPECIFICATION.md に照合し、差分や矛盾がないことを確認します。
2. Unknown の有無
   - 未解決の Unknown がある場合は Issue 作成済みであることを確認し、Issue 番号を MASTER_SPECIFICATION.md に併記します。
3. Evidence の提示
   - 提案・修正には必ず Evidence（根拠）を添付します。
4. ビルド・コンパイル整合性チェック（成果物ごと）
5. ドキュメント整合（リンク切れ、Markdown 構文）
6. BOM・回路・図面等の整合

ビルド・コンパイル整合性チェック（必須レビュー項目）

成果物ごとに以下を確認し、検証ログや出力をレビューに添付してください。

- Arduino (ESP32/Arduinoフレームワーク)
  - コンパイル成功（IDE/CIビルドログを添付）
  - include 漏れなし
  - 依存ライブラリ確認（ライブラリ名とバージョンを明記）

- OpenSCAD
  - Render (F6) が成功すること
  - STL エクスポートが可能であること（エクスポートログを添付）
  - include/use の漏れなし

- KiCad
  - ERC（Electrical Rules Check）実行・確認結果を添付
  - DRC（Design Rules Check）実行・確認結果を添付
  - フットプリント欠落なし（ライブラリ参照の整合を確認）

- ドキュメント
  - Markdown 構文エラーなし（Markdown lint の結果を添付）
  - リンク切れなし（相対・絶対リンク両方の確認結果を添付）

Unknown 管理ルール（必須）

Unknown は放置せず、以下のフローで管理します。Unknown は必ず GitHub Issue と紐付けます。

運用フロー

1. Unknown 発生（作業中に仕様未確定点を検出）
2. MASTER_SPECIFICATION.md に Unknown を明記（該当セクションに追記し、"Unknown" タグと Issue 番号を併記）
3. GitHub Issue を作成（タイトルに "Unknown:" を含める）
4. 担当決定（Issue に assignee を設定）
5. 調査を実施
6. データ取得（実測、メーカー資料、データシート等）
7. レビュー（Evidence を添付）
8. 承認（責任者・担当者による承認）
9. MASTER_SPECIFICATION.md を更新（変更履歴を残す）
10. CHANGELOG.md を更新（バージョン番号付与）
11. Issue をクローズ

- 進捗や結果は Issue スレッドに記録します。
- Unknown のステータスは常に最新に保ってください（例：Issue にラベル: unknown を付与）。

Evidence（根拠）の要件

- 提案や修正には必ず Evidence を添付することを必須とします。
- 許容される Evidence の例:
  - メーカー公式資料
  - データシート
  - 実測値（測定手法と条件を明記）
  - 公式ドキュメント
  - ユーザー測定結果（方法と生データ）
- 推測や未確認の仮定は Evidence として扱いません。仮説は明示的に"仮説"としてタグ付けし、必ず追加の調査/測定で裏付けてください。

レビュー結果の分類

- PASS: 修正不要
- MINOR: 軽微修正（仕様変更を伴わない）
- MAJOR: 設計変更が必要（MASTER_SPECIFICATION への修正案を作成）
- BLOCKER: 重大問題（リリース/次工程を停止するレベル）

Definition of Done（レビュー完了条件）

レビューは以下の項目すべてを満たしたときに完了とします。

- [ ] MASTER_SPECIFICATION 整合
- [ ] CHANGELOG 更新（該当する場合）
- [ ] Unknown なし（残る場合は Issue 作成済み）
- [ ] ビルド成功（該当成果物）
- [ ] ドキュメント更新（該当する場合）
- [ ] BOM 整合
- [ ] 回路整合
- [ ] OpenSCAD 整合（該当する場合）
- [ ] KiCad 整合（該当する場合）
- [ ] バージョン更新（該当する場合）

作業前チェックリスト

- MASTER_SPECIFICATION.md を熟読
- CHANGELOG.md を確認
- AGENTS.md を確認（本ファイル）
- .github/copilot-instructions.md（Copilot用ルール）を確認
- 関連ドキュメント（docs/）を確認

記録と追跡

- すべての決定、Evidence、レビューコメントは Issue または PR に記録します。
- MASTER_SPECIFICATION.md へ仕様追記を行った場合、必ず Issue 番号を記載してください。

注記

- Copilot専用ルール（コード生成指針等）は .github/copilot-instructions.md に限定して記載してください。本書はAI共通ルールおよびレビュー／品質管理に集中します。
