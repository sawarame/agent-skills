---
name: commit-message-generator
description: ステージされた変更からConventional Commitsに沿った日本語のコミットメッセージを生成するスキルです。
---

# コミットメッセージ生成スキル

このスキルは、ステージされた変更（`git add` されたファイルの差分）を解析し、Conventional Commitsのフォーマットに従った日本語のコミットメッセージを自動生成するためのものです。エージェントは以下の手順で動作します。

## 手順
  1. `git diff --staged` を実行して差分を読み取ってください。
  2. 差分がない場合は「Stagedされた変更がありません」と伝えて終了してください。
  3. 差分から、Conventional Commitsに沿った日本語のコミットメッセージを生成してください。
  4. Conventional Commits のフォーマットに従って簡潔なコミットメッセージを作成してください。
  5. 最後に `git commit -m "生成したメッセージ"` を実行するかどうか、私に(y/n)で確認してください。
