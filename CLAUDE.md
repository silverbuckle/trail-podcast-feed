# Trail Podcast Feed - GitHub Pages 配信リポジトリ

## 概要
`trail-podcast` のパイプラインが生成した MP3 と RSS フィードを GitHub Pages で配信するリポジトリ。

## 構成
```
docs/
├── feed.xml          # RSS フィード（Podcast アプリが参照）
├── cover_new.jpg     # カバー画像
└── episodes/         # MP3 ファイル
```

## フィード URL
`https://silverbuckle.github.io/trail-podcast-feed/feed.xml`

## 運用
- `trail-podcast/src/upload.py` が MP3 コピー・feed.xml 生成・git push を自動実行
- 手動でファイル名変更する場合は feed.xml の `<enclosure url>` と `<guid>` も更新すること
- Spotify のキャッシュバストには MP3 ファイル名の変更が必要（URL が変わらないと古い音声を返す）

## 関連リポジトリ
- `trail-podcast/` — パイプライン本体（収集・台本・TTS・アップロード）
