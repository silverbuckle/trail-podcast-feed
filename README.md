# trail-podcast-feed

トレイルランニング・デイリー のポッドキャストフィード配信リポジトリ。

## 配信先

- **RSS フィード**: https://silverbuckle.github.io/trail-podcast-feed/feed.xml
- **Spotify**: RSS フィード URL を Spotify for Podcasters に登録済み

## 構成

```
docs/
├── feed.xml       ← RSS フィード（upload.py が自動更新）
├── cover.jpg      ← カバーアート（手動追加）
├── episodes/      ← MP3 ファイル
└── .nojekyll      ← GitHub Pages ビルド高速化
```

## 更新方法

`trail-podcast` リポジトリの `upload.py` が自動的に：
1. 新エピソードの MP3 を `docs/episodes/` にコピー
2. `docs/feed.xml` を更新
3. `git push` してデプロイ
