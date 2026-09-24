---
applyTo: "**/*.sql"
---

# SQL開発ルール

## データ***

- MySQL 8.x

## SQL***ール

- SQLキーワードは大文字
- イン***を統一する
- 可*****先する
- SELECT***を使用しない

例

SELECT
    user******   user_name
FROM
*** users
WHERE***  delete***ag = 0;

## JOINルール

- 暗黙JOINは禁止***明示的JOINを利用する

***
INNER***IN
LEFT JOIN

##***ォーマンス

- インデックス***意識する
-******早い段階で実施する
******RDER BYを避ける
- 不***ISTINCTを***

## 集計

- GROUP***の整合性を確認する
- COUNT***を**に利用する

## UPDATE**必ずWHERE句を指定する

禁止***UPDATE users
SET status** 'ACTIVE';

## DELETE

必ずWHERE句を指**る

禁止例

DELETE FROM users;

## セ**リティ

- SQL**njectionを防止する
- ユ**ー入力を直接**しない
- プレ**ホルダを利用する

##****ー観点

SQL作**に確認すること

- イン**クス**用されるか
- SELECT** を使用していないか
- JOIN****
- 不**サブクエリはないか
- 実**数は適切か**