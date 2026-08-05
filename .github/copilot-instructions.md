# GitHub Copilot Instructions

Version: 2.0.1
Last Updated: 2026-08-05

目的

このファイルは GitHub Copilot に固有のルールおよびコード生成に関する指針を定義します。AI 共通ルール（レビュー手順、Unknown 管理、Evidence 必須、Definition of Done 等）は AGENTS.md に記載されているため、本ファイルでは Copilot 固有の運用に絞ります。

参照

- AI 共通ルール: AGENTS.md（必ず参照し遵守すること）
- 仕様書: MASTER_SPECIFICATION.md（Single Source of Truth）

主な責務（Copilot）

- 実装（Implementation）: コード、設定ファイル、CI 設定等の作成
- コード補完（Code Completion）: 既存コードの補完作業
- リファクタリング（Refactoring）: 可読性・保守性の向上
- ユニットテストの作成（Unit Tests）
- プルリクエストの作成（PR）と説明文の作成

禁止／制約（Copilot専用）

- MASTER_SPECIFICATION.md を直接編集しないこと
- 仕様が不明な場合に勝手に設計や数値を決めないこと（Unknown として報告する）
- 設計変更を伴う提案は PR で明確に "MAJOR" 分類として提出し、必ず Evidence を添付すること

コード生成ルール

- コメントスタイル
  - 日本語コメントは技術的な説明に限定し、英語コメントは外部公開用に整形する（両方併記可）
- Commit 単位
  - 1コミット = 1意図（例: バグ修正、機能追加、ドキュメント更新）
  - 小さすぎるコミットは避けるが、レビューが容易な粒度を保つこと
- PR 単位
  - 1 PR = 1機能または 1課題の完了
  - PR 本文に以下を含める: 目的、変更点、ビルド手順、テスト手順、Evidence
- ファイルヘッダ
  - 新規ファイルにはファイル目的とバージョンをヘッダに明記すること

C++ / Arduino コーディングスタイル（概要）

- 変数命名: lower_snake_case または lowerCamelCase（プロジェクト既存スタイルに合わせる）
- 定数: UPPER_SNAKE_CASE
- ヘッダファイル: include ガードまたは #pragma once を使用
- メモリ管理: 動的確保は最小限にし、スマートポインタ使用を検討
- Serial デバッグ: リリースでは適切に制御（ログレベル）する
- 配線周りのマクロや定義は MASTER_SPECIFICATION.md に合わせる

PR 作成時の必須項目（テンプレート）

- 対象 Issue 番号（ある場合）
- 変更の概要
- ビルド手順と確認ログ（ビルドチェックの結果）
- Evidence（根拠）
- レビュー完了条件（Definition of Done）への照合チェックリスト

Quality Gate（Copilot用）

- Copilot の作業は AGENTS.md の「Definition of Done」を満たすことが最終目標です。

最後に

不明点や矛盾があれば必ずユーザーへ確認を行い、勝手な推測や仕様変更は行わないでください。
