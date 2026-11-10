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

- Source: `kazuya-ai-lab/jackdoku` `70261865ff90e18d9446f0a9d8d2c744d71f6891`
- Source change: PR #41 `fix(ui): ライトモードの盤面線を半分の太さに調整` ＋ PR #42 `test(ui): ライトモード線幅テストの検証を修正`
- Source workflow: Playtest Package Run #25（検証成功）
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
- Light board: 外枠・Region境界をCSS 3px→1.5px、通常Cell gridを1px→0.5pxに調整（ダークモードは従来どおり）
- Dark board: 眩しさを抑えた低輝度・色相の異なる9色へ変更。外枠とRegion境界は柔らかいスレートグレー #98a6b0、×はオフホワイト #e4e8e8。境界線の幅3pxを維持
- Compact layout: スマホ縦画面・低背PCでHeader / Level / Dogs / Board / Actions / Tutorial / Helpを残して画面高さに収める（極端に短い画面はスクロール許容）
- Scroll control: 1画面表示中は盤面外の縦スワイプによるページ移動・跳ね返りを抑制。Dialog内スクロールとピンチ拡大を維持
- Hint: Player UIでは非提供
- Status: `Level / Dogs`のみ（TREATS / TIMEなし）
- Artifact size: 3,103,816 bytes
- Artifact SHA-256: `519c17df8a61977197bd02c056586cbd3c9d770628d9477bab0dd87ac24d8595`
- Pages deployment: PR Merge後に`main`から自動再配信
