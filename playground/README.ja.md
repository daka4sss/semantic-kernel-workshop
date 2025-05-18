# Semantic Kernel Interactive Demo

このデモは、Semantic Kernel の機能を体験できるインタラクティブな Web アプリケーションです。セマンティック メモリ、AI 関数、翻訳、テキスト要約などを試すことができます。

## クイックスタート

1. Azure OpenAI の認証情報を記載した `.env` ファイルを作成します。
```
AZURE_OPENAI_DEPLOYMENT=your-deployment-name
AZURE_OPENAI_API_KEY=your-api-key
AZURE_OPENAI_ENDPOINT=your-endpoint
AZURE_OPENAI_EMBEDDING_DEPLOYMENT=your-embedding-deployment-name
```

2. 依存関係をインストールします。
```
cd frontend
npm install --legacy-peer-deps
```

3. アプリケーションを起動します。
```
./start.sh
```

スクリプトはバックエンド (http://localhost:8000) とフロントエンド (http://localhost:5173) の両方を起動します。停止するときは Ctrl+C を押してください。

## 機能

- **Semantic Memory**: セマンティック検索を用いた情報の保存と取得
- **AI Functions**: 自然言語で AI 関数を作成・利用
- **Translation**: 複数言語間の翻訳
- **Summarization**: 長文の要約生成
- **Weather Plugin**: ネイティブ プラグイン統合の例

## 必要条件

- Node.js (v14 以上)
- Python (v3.13 以上)
- Azure OpenAI API の認証情報

## プロジェクト構成

- `frontend/`: Material UI を使用した React アプリケーション
- `backend/`: Semantic Kernel を実装した FastAPI サーバー
- `start.sh`: 2 つのサービスを起動するためのスクリプト

詳細なドキュメントや例については [Semantic Kernel Documentation](https://learn.microsoft.com/en-us/semantic-kernel/overview/) を参照してください。
