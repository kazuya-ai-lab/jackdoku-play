# Jackdoku Play

Jackdokuのスマートフォン / Web配布用リポジトリです。

開発ソースはPrivateリポジトリで管理し、このPublicリポジトリにはHuman Reviewと自動検証を通過した生成済みゲームだけを配置します。

## Play

GitHub Pages有効化後、次のURLから遊べます。

`https://kazuya-ai-lab.github.io/jackdoku-play/`

スマートフォンではSafari / Chromeから開きます。iPhoneではSafariの共有メニューから「ホーム画面に追加」することで、Web Appのように起動できます。

## Distribution policy

- `index.html` はPrivate開発リポジトリのAccepted Buildから昇格する
- 開発ソースをこのリポジトリへ複製しない
- 配布時にSource commitとSHA-256を `PROVENANCE.md` に記録する
- 広告・Account・Analytics・外部Runtime APIを追加しない
- 更新はPull Request → Human Review → Squash Mergeを基本とする

## License

Apache License 2.0
