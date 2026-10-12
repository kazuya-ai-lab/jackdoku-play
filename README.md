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

- Source: `kazuya-ai-lab/jackdoku` `b0be5e8632aa350b323ef933508739b60566709b`
- Source change: PR #36 `fix(ux): 盤面外のスクロール抑止とダーク配色の微調整`
- Source workflow: Playtest Package Run #19
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
- Dark board: 彩度を少し高めた9色、ページ背景から見分けやすいグレーの外枠、青墨色の内側境界と×
- Compact layout: スマホ縦画面・低背PCでHeader / Level / Dogs / Board / Actions / Tutorial / Helpを残して画面高さに収める（極端に短い画面はスクロール許容）
- Scroll control: 1画面表示中は盤面外の縦スワイプによるページ移動・跳ね返りを抑制。Dialog内スクロールとピンチ拡大を維持
- Hint: Player UIでは非提供
- Status: `Level / Dogs`のみ（TREATS / TIMEなし）
- Artifact size: 3,103,172 bytes
- Artifact SHA-256: `556a5166675091ef9ac2f41a427e6fdb253c68eb6a5b3519de220c692617720b`
- Pages deployment: PR Merge後に`main`から自動再配信
