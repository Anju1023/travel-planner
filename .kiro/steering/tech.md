# 技術スタック

## フレームワーク & ランタイム

- **Next.js 15.5.4** - App Router を使用する React フレームワーク
- **React 19.1.0** - 最新機能を搭載した UI ライブラリ
- **TypeScript 5** - 型安全な JavaScript 開発
- **Node.js** - ランタイム環境

## スタイリング & UI

- **Tailwind CSS 3.4.17** - ユーティリティファーストの CSS フレームワーク
- **CSS Modules** - コンポーネントスコープのスタイリング（page.module.css パターン）
- **PostCSS** - CSS 処理とオートプレフィックス
- **Geist フォント** - Vercel 製のモダンフォントファミリー

## 開発ツール

- **ESLint 9** - Next.js 設定でのコードリンティング
- **Turbopack** - 開発とビルド用の高速バンドラー
- **TypeScript strict mode** - 強化された型チェック

## ビルドシステム

- **Turbopack** - 開発とビルドの両方で使用
- **Next.js コンパイラー** - 内蔵の最適化とバンドリング

## よく使うコマンド

### 開発

```bash
npm run dev          # Turbopackで開発サーバー起動
```

### 本番

```bash
npm run build        # Turbopackで本番ビルド
npm run start        # 本番サーバー起動
```

### コード品質

```bash
npm run lint         # ESLintチェック実行
```

## 設定のポイント

- App Router 使用（Pages Router ではない）
- TypeScript パスマッピングで`@/*`エイリアス設定済み
- 厳密な TypeScript 設定が有効
- 幅広いブラウザ対応のため ES2017 ターゲット
