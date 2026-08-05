# GitHub AI ワークフロー（docs/github_ai_workflow.md）

このドキュメントは、AI が関与する開発フローの補助資料です。主な目的は AGENTS.md と .github/copilot-instructions.md に記載した運用ルールを視覚的・手順的にまとめ、他の AI や人間が理解しやすくすることです。

概要フロー

1. 要求受領
   - ユーザーまたは Issue によりタスクが発生
2. 事前確認
   - MASTER_SPECIFICATION.md → CHANGELOG.md → AGENTS.md → .github/copilot-instructions.md の順に確認
3. 仕様の不明点確認
   - 不明点は Unknown として MASTER_SPECIFICATION.md に記載し、Issue を作成
4. 実装・作業
   - Copilot: 実装・テスト・PR作成
   - ChatGPT/Gemini: 設計レビュー、アルゴリズム検証、数値検証
5. ビルド・検証
   - Arduino コンパイル、OpenSCAD レンダリング、KiCad ERC/DRC 等を実施
6. Evidence 収集
   - メーカー資料、データシート、実測データ、CI ログ等を添付
7. レビュー
   - AGENTS.md のレビュー手順に従いレビューを実施（PASS/MINOR/MAJOR/BLOCKER）
8. 承認と更新
   - 承認された変更は MASTER_SPECIFICATION.md（必要時）、CHANGELOG.md へ反映
9. リリース準備
   - バージョン更新、BOM 更新、ドキュメント更新

Unknown 発生時の例

- Unknown が検出されたら即座に: MASTER_SPECIFICATION.md に Unknown を追加 → Issue 作成 → assignee を決定
- その後、測定やメーカー問い合わせなどで証拠を収集し、Evidence を添えてレビュー→承認→仕様反映→Issue Close

ビルドチェックの標準手順（簡易）

- Arduino
  - ローカルまたは CI でビルドを実行し、成功ログを添付
  - 依存ライブラリは library.json や platformio.ini、README にバージョンを明記
- OpenSCAD
  - scad を Render (F6) してエラーがないことを確認
  - export で STL を生成できることを確認
- KiCad
  - ERC と DRC を実行し、問題がないことを確認
  - フットプリントとライブラリ参照を確認

証拠（Evidence）例

- メーカー公式ドキュメント PDF
- センサーデータシートの該当ページ引用
- 実測値の CSV と測定条件メモ
- CI のビルドログのスクリーンショット／テキスト

注記

- 本ドキュメントは補助資料です。プロジェクトの公式ルールは AGENTS.md と .github/copilot-instructions.md を優先してください。
