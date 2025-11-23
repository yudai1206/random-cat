# random-cat

Next.js 14 の App Router で作った、The Cat API からランダムな猫画像を取得して表示するシンプルなサンプルです。ボタンで画像をリロードできます。

## セットアップ

```bash
npm install
```

開発サーバーを起動します。

```bash
npm run dev
```

ブラウザで http://localhost:3000 を開いて動作を確認してください。

## 環境変数

The Cat API の API キーを使う場合は、`.env.local` に下記を設定します（任意）。

```bash
CAT_API_KEY=あなたのAPIキー
```

## 仕組み

- `app/page.tsx` でサーバーコンポーネントから `fetchImage` を呼び、初回の猫画像を取得します。
- `app/cat-image.tsx` はクライアントコンポーネントで、ボタン押下時に再度 API を叩いて画像を更新します。
- 画像取得処理は `app/fetch-image.ts` に分離し、ログ出力で取得結果を確認できます。
- スタイルは `app/page.module.css` で定義しています。

## ライセンス

MIT
