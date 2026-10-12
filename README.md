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

- Source: `kazuya-ai-lab/jackdoku` `b9ab6f9458ac11d2b613b84cf74de6efb1d559af`
- Source change: PR #37 `fix(ux): ライト外枠を細く戻しダーク盤面の黒枠と鮮明な配色を統一`
- Source workflow: Playtest Package Run #20
- Playable levels: 5,000
- Board progression: 5×5〜9×9
- Level 161〜5,000: 9×9
- Level Select: 50件Paging / 100 pages
- Single Tap / Click: ×（Double Tap判定待機 200ms）
- Double Tap / Double Click: Jack Russell Terrier
- Swipe / Drag: ×を一括入力
- 入力Mode切替Button: 非提供
- Right Click: Jack Russell Terrier（PC）
- Text selection: ゲームUIで抑止（Touch calloutも抑止）
- Theme: 端末設定に追従 / ライト / ダーク（設定をSave v2へ保存）
- Light board: 外枠は1px、領域区切り線は3px
- Dark board: くすみを抑えた明るく鮮やかな9色。外枠と領域区切り線を黒系（#18262f）で統一し、×にも同色を使用
- Compact layout: スマホ縦画面・低背PCでHeader / Level / Dogs / Board / Actions / Tutorial / Helpを残して画面高さに収める（極端に短い画面はスクロール許容）
- Scroll control: 1画面表示中は盤面外の縦スワイプによるページ移動・跳ね返りを抑制。Dialog内スクロールとピンチ拡大を維持
- Hint: Player UIでは非提供
- Status: `Level / Dogs`のみ（TREATS / TIMEなし）
- Artifact size: 3,103,370 bytes
- Artifact SHA-256: `0c1afa8f3ef7562c8470a659ef944d4648ad56d6a11950debe589a919f12a7c0`
- Pages deployment: PR Merge後に`main`から自動再配信
