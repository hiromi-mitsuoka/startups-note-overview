# 「 海外スタートアップ情報を共有するプラットフォーム「Startups Note」の開発 」

# デモ動画・AWS構成図・論文
- Google Drive: https://drive.google.com/drive/folders/1jbo3Fq7zX7K4ssPGFrWJLZLtnUvl1UyN?usp=sharing

# サービス概要
- 海外スタートアップに関するニュースを中心にキュレーションするサービス
- バッチ処理により、毎朝最新ニュースをお届け
- アカウントと紐付けてコメントすることで、世界の情報に関して、ユーザー間での意見の共有を可能にする

# 制作背景

## 国内でのスタートアップへの熱

```
- 2021年、国内スタートアップによる年間資金調達の合計額が8000億円を突破。
- 過去最高だった2019年と比較して約3000億円も増大。
- 政府は新たな成長につながる領域としてスタートアップ支援の強化を挙げ、経済産業省内に専門部署を新設すると明らかに。
- 3年度補正予算案では、創薬ベンチャー開発支援などに500億、研究開発型のスタートアップ支援事業に33億5千万円などを充てている。

（参考記事）
- https://signal.diamond.jp/articles/-/989
- https://www.sankei.com/article/20211130-AUJBKEWCSNPDXIWEGNPQTFB6EU/
```

## 世界との比較

```
- 企業評価額が10億ドル（約1000億円）以上、かつ設立10年以内の非上場ベンチャー企業を指す「ユニコーン」は世界で959社存在する中、日本は現在11社。

（参考記事）
- https://thebridge.jp/2022/01/cb-insights-venture-report-2021
```

## 制作経緯

```
- スタートアップに興味を持つ人を増やしたい。
- 海外のビジネス情報に触れる時間を作りたい。
- 海外の事例を知り、新しいアイデアの創出のきっかけに。
```


# 使用技術
- フロントエンド: Next.js
- バックエンド: Ruby on Rails
- インフラ・開発環境など: AWS（ECS, OpenSearch, RDS, ALB etc.）/ Firebase Authentication / Terraform / Docker / Elasticsearch

## リポジトリ
- バックエンド: https://github.com/hiromi-mitsuoka/startups-note-backend
- インフラ: https://github.com/hiromi-mitsuoka/startups-note-infra

# サービスに関する補足

## サービスの種類
- ユーザー側の画面: ダークモード画面
- 管理者側の画面: ダークモードでない画面

## 管理者側の画面で行うこと
- RSSで取得したニュースと、タグ検索で使用するニュースに紐づくタグの2つのユーザー画面での表示/非表示の切り替えを行う
  - 論理削除を使用し、DB・Elasticsearchへ反映する

## サービス運営に関して
- 現在、AWSのリソースを削除し、運営は停止しています。


