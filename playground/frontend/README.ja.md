# Semantic Kernel Playground - Shadcn Frontend

このリポジトリは、Next.js と shadcn/ui コンポーネントを使用して構築された Semantic Kernel Playground のモダンなフロントエンドです。

## 機能

- shadcn/ui コンポーネントによるモダンでレスポンシブな UI
- 型安全性のための TypeScript
- カスタムコンポーネントによる使いやすさの向上
- ベクトル検索を利用した Semantic Memory デモ
- Functions & Plugins デモ (近日公開)
- Translation デモ (近日公開)
- Weather デモ (近日公開)
- Summarization デモ (近日公開)
- Filters & Security デモ (近日公開)
- Agent デモ (近日公開)
- Multi-agent デモ (近日公開)

## 開始方法

まずバックエンドサーバーが起動していることを確認し、開発サーバーを実行します。

```bash
npm install --legacy-peer-deps
npm run dev
```

ブラウザで [http://localhost:3000](http://localhost:3000) を開くと結果を確認できます。

## 使用技術

- [Next.js](https://nextjs.org/) - React フレームワーク
- [shadcn/ui](https://ui.shadcn.com/) - アクセシブルで美しいコンポーネントライブラリ
- [Tailwind CSS](https://tailwindcss.com/) - ユーティリティファーストな CSS フレームワーク
- [Axios](https://axios-http.com/) - Promise ベースの HTTP クライアント

このプロジェクトでは [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) を使用して、Vercel の新しいフォントファミリー [Geist](https://vercel.com/font) を自動的に最適化・読み込みます。

## さらに学ぶ

Next.js について詳しく知りたい場合は次の資料をご覧ください。

- [Next.js Documentation](https://nextjs.org/docs) - Next.js の機能や API
- [Learn Next.js](https://nextjs.org/learn) - インタラクティブなチュートリアル

[Next.js の GitHub リポジトリ](https://github.com/vercel/next.js) もぜひご覧ください。フィードバックや貢献をお待ちしています。

## Vercel でのデプロイ

Next.js アプリを最も簡単にデプロイする方法は、Next.js の開発元が提供する [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) を利用することです。

詳しくは [Next.js デプロイメントのドキュメント](https://nextjs.org/docs/app/building-your-application/deploying) を参照してください。
