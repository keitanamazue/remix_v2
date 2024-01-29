# おくりびと相続

## Requirements

- Node.jsのversionを20.11.0にする

```bash
nvm install 20.11.0
```

- yarnのversionを4.0.2にする

```bash
yarn set version stable
```

## Setup

```bash
yarn
```

## Develop

First, run the development server:

```bash
yarn dev

open http://localhost:3000
```

## Git

### Commit Message Prefix

| Prefix   | 説明                 |
| -------- | -------------------- |
| feat     | 機能追加             |
| refactor | リファクタリング     |
| fix      | バグ修正             |
| chore    | ライブラリ追加等     |
| docs     | ドキュメントのみ変更 |
| style    | スタイルのみ変更     |
| test     | テストの追加         |

### Branch Model

以下を参考にブランチを切ってください。

| ブランチ名 | 説明                                               |
| ---------- | -------------------------------------------------- |
| main       | 起点となるブランチ。マージしたら本番環境へ反映する |
| staging    | マージしたら本番環境へ反映する                     |
| feat/XXX   | 機能開発用ブランチ                                 |
| ref/XXX    | リファクタリング用ブランチ                         |
| fix/XXX    | バグ修正用ブランチ                                 |
| hotfix/XXX | 本番環境で発生している緊急バグ修正用ブランチ       |

## Directory

コンポーネントの分割粒度は Atomic Design に倣う

```
├── public ...静的ファイル群
└── app
    ├── _components ...共通コンポーネント
    ├── routes ...ルーティングに関する設定ファイルやディレクトリ
    └── utils ...共通項目
```
