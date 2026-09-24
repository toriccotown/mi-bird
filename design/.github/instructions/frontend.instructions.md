---
applyTo: "**/*.ts,**/*.tsx"
---

# フロントエンド開発ルール

# 言語

- TypeScript 5.7.2

# 技術スタック

使用ライブラリおよびバージョンは package.json を参照すること。

新規実装時は、既存依存ライブラリの利用を優先し、
同等機能を持つライブラリを重複導入しないこと。

## 基本方針

- TypeScript の厳密な型定義を行う
- 型安全性を最優先する
- 既存実装との整合性を重視する
- 重複コードを作らない
- 保守性を優先する

## コンポーネント設計

- 関数コンポーネントを使用する
- Named Export を使用する
- 1コンポーネント1責務を意識する
- 共通化可能なUIはコンポーネント化する

## State管理

- ローカル状態は useState を利用する
- 不要なStateは作成しない
- useMemo、useCallbackを必要に応じて利用する

## API呼び出し

- API通信は Service 層に実装する
- Component内に直接API処理を書かない
- fetch処理の共通化を行う

## ディレクトリ配置

- assets: 画像・フォントなどの静的リソース
- components: UIコンポーネント
- constants: 定数定義
- contexts: React Context
- pages: ページコンポーネント
- routes: ルーティング定義
- services: API通信処理
- themes: テーマ定義
- types: 型定義
- utils: ユーティリティ関数

## エラー処理

- 必ず例外処理を実装する
- ユーザー向けメッセージとログを分離する
- console.errorの多用を避ける

## 禁止事項

- any型の使用
- default export
- 複雑な業務ロジックをComponent内に実装すること
- DOM直接操作