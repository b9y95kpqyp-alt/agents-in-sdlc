---
slug: ja-jp/real-world-development/cli
title: "GitHub Copilot CLI"
description: "Copilot CLI のモード、カスタマイズ、MCP ツール、プル リクエストの自動化を学びながら、Tailspin Toys に 2 つの変更を加え、検証して提供します。"
authors:
  - geektrainer
lastUpdated: 2026-09-18
---

**[GitHub Copilot CLI][about-copilot-cli]** は、ターミナルで GitHub Copilot をエージェント型のコーディング アシスタントとして利用できるようにします。コードベースを探索し、コードを生成し、コマンドを実行し、外部ツールに接続できます。すべてコマンド ラインから行えるため、グラフィカル エディターに切り替えずに作業の流れを保てます。

このワークショップでは、Tailspin Toys で一連の作業を行います。

1. GitHub Codespaces でプロジェクトを準備し、Copilot CLI をインストールして、基本を確認します。
2. 小さな星評価の変更を加え、ブラウザーでレビューして、最初のプル リクエスト (PR) を手動でマージします。
3. フィルタリングの issue から始め、Plan モードで方針を決め、Autopilot モードで実装し、Interactive モードでレビューします。
4. リポジトリの指示を更新し、フィルタリング作業に適用します。
5. 既存の `quality-checks` スキルをカスタマイズして、プロジェクトのチェックを実行します。
6. Playwright Model Context Protocol (MCP) サーバーを追加し、ブラウザーでフィルタリングを確認します。
7. QA (品質保証) カスタム エージェントを作成して使用し、要件、テスト範囲、検証の証拠を確認します。
8. フィルタリングの変更全体をレビューし、Agent Merge を使って PR をマージします。
9. コンテキスト、モデル、共有、任意のクラウド委任に役立つ slash command を確認します。

ワークショップに集中できるよう、PR は 2 つ作成します。1 つ目は星評価、2 つ目は指示の更新、スキルの更新、QA プロファイル、テストを含むフィルタリングです。フィルタリングと品質確認の作業では、会話とブランチを共有するため、各ツールを試しながら作業を積み重ねられます。

## レッスン

| レッスン | トピック | 説明 |
| ------ | ----- | ----------- |
| [0. 前提条件][ex0] | セットアップ | リポジトリと codespace を作成する |
| [1. Copilot CLI のインストール][ex1] | インストール | Copilot CLI をインストールして認証し、基本を確認する |
| [2. 星評価を追加する][ex2] | 最初の変更 | 既存の評価と未評価時の表示を追加し、最初の PR をマージする |
| [3. エージェント モード: Plan と Autopilot][ex3] | エージェント モード | issue から機能を計画し、Autopilot で構築して Interactive でレビューする |
| [4. カスタム指示で Copilot を導く][ex4] | コンテキスト | 指示を確認・更新し、フィルタリングに適用する |
| [5. quality-checks スキルをカスタマイズして使う][ex5] | 繰り返し可能なチェック | 既存のスキルを確認し、レポート形式を変更して実行する |
| [6. Playwright MCP で機能を検証する][ex6] | ブラウザーでの確認 | CLI で MCP を構成し、フィルタリングの動作を確認する |
| [7. QA エージェントを作成して使う][ex7] | 要件とテスト範囲 | 専門プロファイルを作成して選択し、最終的な検証の証拠を集める |
| [8. 機能の PR を作成してマージする][ex8] | レビューとマージ | 変更全体をレビューし、PR を作成して Agent Merge を使う |
| [9. GitHub Copilot CLI の便利な機能][ex9] | CLI 機能 | コンテキスト、モデル、共有、任意のクラウド エージェントへの委任を確認する |
| [10. 振り返りと次のステップ][ex10] | まとめ | ワークフロー、再利用可能なカスタマイズ、その他のリソースを確認する |
| [オプション: Foundry を組み込む][foundry] | ホスト型エージェント | モデルを準備し、カタログに基づいたエージェントをデプロイしてサイトに接続する |

## 前提条件

このワークショップに参加する前に、次を準備してください。

- [ ] **Copilot Student、Pro、Pro+、Business、Enterprise** のいずれかの有効なプランがある GitHub アカウント
- [ ] リポジトリと codespace を作成する権限
- [ ] ターミナルまたはコマンド ライン操作の基本的な知識

> [!TIP]
> 有料プランがありませんか。認証済みの学生は [GitHub Education][student-plan] を通じて GitHub Copilot を無料で利用できます。**Copilot Student** プランには、このワークショップで使用する agent、MCP、code review、Copilot CLI の機能が含まれています。

> [!NOTE]
> Copilot Business または Copilot Enterprise を使用している場合は、管理者が Copilot CLI を有効にしていることを確認してください。

## はじめる

**[前提条件から始める →][ex0]**

[about-copilot-cli]: https://docs.github.com/copilot/concepts/agents/about-copilot-cli
[student-plan]: https://github.com/education/students
[ex0]: 0-prerequisites/
[ex1]: 1-install-copilot-cli/
[ex2]: 2-add-star-rating/
[ex3]: 3-agent-modes/
[ex4]: 4-custom-instructions/
[ex5]: 5-agent-skills/
[ex6]: 6-mcp-playwright/
[ex7]: 7-qa-agent/
[ex8]: 8-create-pull-request/
[ex9]: 9-cli-power-tools/
[ex10]: 10-review/
[foundry]: 8-foundry-agent/
