# Semantic Kernel Workshop

このワークショップは、Microsoft の Semantic Kernel フレームワークを利用してインテリジェントな AI アプリケーションを構築するためのハンズオン形式の教材です。Python と Azure OpenAI を使った実践的な例を通じて、現実的な AI アプリケーション パターンを体験できます。

## ワークショップ概要

本ワークショップでは、基礎から応用までを一連の Jupyter Notebook と実践例を通して学びます。以下の内容を習得します:

- Microsoft の Semantic Kernel フレームワークを用いた AI アプリケーション開発
- さまざまな能力と役割を持つ AI エージェントの作成とオーケストレーション
- Process Framework を活用した構造化された AI ワークフローの構築
- セキュリティとスケーラビリティを考慮したエンタープライズ向け機能の実装

## インタラクティブ プレイグラウンド デモ

プレイグラウンドを通じて Semantic Kernel を体験できます。視覚的なデモにより、ワークショップで扱う主要な概念を直接試すことができます。

![Semantic Kernel Playground Demo](playground/assets/sk-playground.gif)

プレイグラウンドでは次のような操作が可能です:

- セマンティック関数をリアルタイムでテスト
- エージェントの機能や相互作用を確認
- メモリや埋め込みを試す
- ネイティブ プラグイン統合の確認
- Process Framework の動作を見る

ワークショップの最後まで待つ必要はありません。学習を進めながら、いつでもプレイグラウンドを試して概念を強化しましょう。

セットアップ方法や実行手順については [Playground README](playground/README.md) を参照してください。

## 前提条件

- Python 3.10 以上
- Azure OpenAI API の利用権限 (API キー、エンドポイント、デプロイ名)
- Python の基本的な知識
- プロンプト エンジニアリングの概念 (必須ではありませんが理解しておくと役立ちます)
- [UV パッケージマネージャー](https://docs.astral.sh/uv/getting-started/installation/)

### ローカル依存関係のセットアップ

このプロジェクトは `pyproject.toml` と [UV パッケージマネージャー](https://docs.astral.sh/uv/getting-started/installation/) で管理されています。

ローカルで実行する場合は、次のコマンドで `.venv` 環境を初期化します。

```shell
uv sync --prerelease=allow
. ./.venv/bin/activate
```

> 現在、本ワークショップはプレリリース版ライブラリに依存しています。

## ワークショップ モジュール

### 01. Introduction to Semantic Kernel

Semantic Kernel の基礎を学びます。

- コアとなるアーキテクチャ コンポーネント (Kernel、AI Services、Plugins)
- プロンプトを用いたセマンティック関数の作成
- Python コードによるネイティブ関数の実装
- 持続的なコンテキストのためのメモリ実装
- AI エージェントの自動関数呼び出しを有効化

**主な Notebook:**

- `01-intro.ipynb`: コア概念、サービス、関数作成
- `02-memory.ipynb`: 埋め込みを用いたセマンティック メモリ実装

### 02. Semantic Kernel Agents

AI エージェントの作成とオーケストレーションを学びます。

- 異なるペルソナを持つ専用エージェントの作成
- マルチエージェント通信パターンの実装
- エージェント選択戦略とオーケストレーション
- 複雑なシナリオに対応したエージェント トポロジの構築
- プラグインを組み合わせた機能拡張

**主な Notebook:**

- `02.1-agents.ipynb`: エージェントの作成と設定
- `02.2-agents-chats.ipynb`: エージェント間の通信と複雑なパターン

### 03. Process Framework

構造化されたイベント駆動型 AI ワークフローの構築方法を学びます。

- Process Framework のアーキテクチャ理解
- イベント、ステップ、状態管理の定義
- Process を利用した会話型 AI システムの構築
- AI 機能を組み込んだ複雑なビジネス ロジックの実装
- 保守性とテスト性に優れた AI ワークフローの作成

**主な Notebook:**

- `03.1-intro-to-processes.ipynb`: 状態を持つイベント駆動型プロセスの構築

## プロジェクト構成

```
semantic-kernel-workshop/
├── 01-intro-to-semantic-kernel/    # コア概念の紹介
│   ├── 01-intro.ipynb              # 基本概念と関数
│   └── 02-memory.ipynb             # メモリ実装
├── 02-semantic-kernel-agents/      # エージェントの作成とオーケストレーション
│   ├── 02.1-agents.ipynb           # エージェントの基礎
│   ├── 02.2-agents-chats.ipynb     # マルチエージェント通信
│   └── .env.sample                 # 環境変数テンプレート
├── 03-process-framework/           # 構造化 AI ワークフロー
│   └── 03.1-intro-to-processes.ipynb  # Process の基礎
└── playground/                     # インタラクティブアプリケーション
    ├── backend/                    # FastAPI サーバー
    ├── frontend/                   # React アプリケーション
    ├── start.sh                    # 起動スクリプト
    └── README.md                   # Playground のドキュメント
```

## はじめに

1. このリポジトリをクローンします。

2. 仮想環境を作成します。

   **Linux/macOS:**
   ```bash
   # 仮想環境を作成
   python -m venv venv

   # 仮想環境を有効化
   source venv/bin/activate
   ```

   **Windows:**
   ```cmd
   # 仮想環境を作成
   python -m venv venv

   # 仮想環境を有効化
   venv\Scripts\activate
   ```

3. 環境変数テンプレートをコピーします。
   ```bash
   cp .env.example .env
   ```

4. `.env` ファイルに Azure OpenAI の認証情報を追加します。
   ```
   AZURE_OPENAI_DEPLOYMENT=your-deployment-name
   AZURE_OPENAI_API_KEY=your-api-key
   AZURE_OPENAI_ENDPOINT=your-azure-endpoint
   AZURE_OPENAI_API_VERSION=2024-02-15-preview
   AZURE_OPENAI_EMBEDDING_DEPLOYMENT=your-embedding-deployment
   ```

5. 最初の Notebook から始めてください。
   - `01-intro-to-semantic-kernel/01-intro.ipynb` には Semantic Kernel のインストール方法などが記載されています。

## 学習の流れ

効率よく学ぶために、以下の順序で進めることを推奨します。

1. **基礎概念**: `01-intro.ipynb` でコア コンポーネントを理解
2. **メモリ実装**: `02-memory.ipynb` でセマンティック メモリの仕組みを学習
3. **基本的なエージェント**: `02.1-agents.ipynb` で最初のエージェントを作成
4. **高度なエージェント パターン**: `02.2-agents-chats.ipynb` で複雑なエージェントのやり取りを学習
5. **Process Framework**: `03.1-intro-to-processes.ipynb` で構造化ワークフローを学習
6. **実践**: インタラクティブ プレイグラウンドで総合的に試す

## さらに深く学ぶためのリソース

より高度なパターンやエンタープライズ向けデプロイ シナリオについては、[Semantic Kernel Advanced Usage](https://github.com/Azure-Samples/semantic-kernel-advanced-usage) リポジトリを参照してください。以下の内容が含まれています。

- スケーラブルな分散システムのための Dapr 統合
- 認証とセキュリティ パターン
- 自然言語から SQL への変換
- Copilot Studio との連携
- Microsoft Graph API 連携
- 本番環境へのデプロイ アーキテクチャ

## 追加リソース

- [Semantic Kernel Documentation](https://learn.microsoft.com/en-us/semantic-kernel/overview/)
- [Azure OpenAI Service](https://azure.microsoft.com/en-us/products/ai-services/openai-service/)
- [Microsoft Copilot Studio](https://www.microsoft.com/en-us/microsoft-copilot/microsoft-copilot-studio)

## ライセンス

このプロジェクトは MIT ライセンスの下で提供されています。詳細は LICENSE ファイルを参照してください。
