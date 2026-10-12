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

- Source: `kazuya-ai-lab/jackdoku` `d04ec030d9f56a1142d6e1f99d725d344d31fa9d`
- Source change: PR #40 `fix(ux): ダーク盤面を落ち着いた低輝度の9色に調整`
- Source workflow: Playtest Package Run #23
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
- Light board: 外枠・Region境界をともに各辺CSS 3pxに統一。通常のCell gridは1pxを維持
- Dark board: 眩しさを抑えた低輝度・色相の異なる9色へ変更。外枠とRegion境界は柔らかいスレートグレー #98a6b0、×はオフホワイト #e4e8e8。境界線の幅3pxを維持
- Compact layout: スマホ縦画面・低背PCでHeader / Level / Dogs / Board / Actions / Tutorial / Helpを残して画面高さに収める（極端に短い画面はスクロール許容）
- Scroll control: 1画面表示中は盤面外の縦スワイプによるページ移動・跳ね返りを抑制。Dialog内スクロールとピンチ拡大を維持
- Hint: Player UIでは非提供
- Status: `Level / Dogs`のみ（TREATS / TIMEなし）
- Artifact size: 3,103,783 bytes
- Artifact SHA-256: `fb61b96f4632dedb94844733d0405aa0bfe99f93a7601aad5c931ea64d740225`
- Pages deployment: PR Merge後に`main`から自動再配信
