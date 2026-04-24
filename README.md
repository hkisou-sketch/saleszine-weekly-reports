# saleszine-weekly-reports

[Saleszine](https://saleszine.jp/) の記事を毎週月曜9時（JST）にスキャンし、キーワード傾向を自動レポートするリポジトリです。パブリシティ戦略（調査レポートのピッチング先テーマ選定）に活用します。

## 仕組み

- Claude Code の定期エージェント（remote routine）が毎週月曜 00:00 UTC（= 月曜 9:00 JST）に起動
- Saleszine の新着記事一覧を取得し、タイトル・カテゴリ・タグを抽出
- 先週分との比較でキーワード頻度・伸びているテーマ・新規登場テーマを分析
- `reports/YYYY-MM-DD.md` として commit & push

## ディレクトリ

- `reports/` — 週次レポート（ファイル名は実行日のUTC日付）
- `data/` — 生データ（記事一覧のJSONなど、任意）

## ローカルでの使い方

```bash
git pull
open reports/
```

最新のmdを開いて、提案すべきテーマを検討する。
