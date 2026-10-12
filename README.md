# jackdoku-play

Jackdokuのスマートフォン・Web配布用リポジトリです。

開発ソースはPrivateリポジトリ`kazuya-ai-lab/jackdoku`で管理し、このPublicリポジトリには検証済みの生成物と配布メタデータのみを配置します。

## Play

https://kazuya-ai-lab.github.io/jackdoku-play/

## Distribution policy

- ゲーム実装はこのPublicリポジトリで直接修正しません。
- Private側でBuild / Test / Distribution Checkを完了したArtifactだけを昇格します。
- `PROVENANCE.md`にSource commit、Workflow Run、Artifact digestを記録します。
- `Verify Distribution` Workflowで`PROVENANCE.md`のSHA-256と`index.html`実体を照合します。
- GitHub Pagesは`main` / `/(root)`から配信します。

## Current distribution

- Source: `kazuya-ai-lab/jackdoku` `e4f95af7b346ae81a05d5a9e6075728935ca6dc0`
- Source change: PR #33 `feat(game): レベルを4,000へ拡張しテキスト選択を抑止`
- Source workflow: Playtest Package Run #16
- Playable levels: 4,000
- Board progression: 5×5〜9×9
- Level 161〜4,000: 9×9
- Level Select: 50件Paging / 80 pages
- Single Tap / Click: ×（Double Tap判定待機 200ms）
- Double Tap / Double Click: Jack Russell Terrier
- Swipe / Drag: ×を一括入力
- 入力Mode切替Button: 非提供
- Right Click: Jack Russell Terrier（PC）
- Text selection: ゲームUIで抑止（Touch calloutも抑止）
- Hint: Player UIでは非提供
- Status: `Level / Dogs`のみ（TREATS / TIMEなし）
- Artifact size: 2,486,450 bytes
- Artifact SHA-256: `6a90eb05f7ca918cd96401b703e7a60a8f22b8514c545a03f92bb66269650ba3`
- Pages deployment: PR Merge後に`main`から自動再配信
