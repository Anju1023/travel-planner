# プロジェクト構造

## ルートディレクトリ構成

```
travel-planner/
├── app/                    # Next.js App Routerディレクトリ
├── public/                 # 静的アセット
├── .kiro/                  # Kiro設定とsteering
├── node_modules/           # 依存関係
└── [設定ファイル群]          # 各種設定ファイル
```

## App ディレクトリ (`/app`)

Next.js 15 App Router 規約を使用：

- `layout.tsx` - グローバルスタイルとフォントを含むルートレイアウトコンポーネント
- `page.tsx` - ホームページコンポーネント
- `globals.css` - グローバル CSS スタイル
- `page.module.css` - ページ固有の CSS モジュール
- `favicon.ico` - サイトファビコン

## 公開アセット (`/public`)

ルートから配信される静的ファイル：

- `*.svg` - アイコンアセット（next.svg、vercel.svg など）
- `/ファイル名.拡張子` の URL でアクセス可能

## 設定ファイル

- `package.json` - 依存関係とスクリプト
- `next.config.ts` - Next.js 設定
- `tsconfig.json` - TypeScript コンパイラオプション
- `tailwind.config.js` - Tailwind CSS 設定
- `postcss.config.js` - PostCSS 設定
- `eslint.config.mjs` - ESLint 設定

## 命名規則

- **コンポーネント**: PascalCase（例：`RootLayout`、`Home`）
- **ファイル**: ページは kebab-case、コンポーネントは camelCase
- **CSS モジュール**: `[名前].module.css` パターン
- **型定義**: TypeScript の interface と type を使用

## インポートパターン

- 内部インポートには`@/*`パスエイリアスを使用
- Next.js コンポーネントは`next/*`からインポート
- React 型は`type`キーワードでインポート
- ページコンポーネントはデフォルトエクスポートを使用

## アセット整理

- 静的アセットは`/public`ディレクトリ
- コンポーネント固有のスタイルは CSS モジュール
- グローバルスタイルは`app/globals.css`
- フォント読み込みは`next/font/google`経由
