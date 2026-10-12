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

- Source: `kazuya-ai-lab/jackdoku` `48677bf8e0e47716aafa3cde7854bb2aec0b68a2`
- Source change: PR #35 `fix(ux): ダーク盤面の配色と1画面に収まるプレイUIを改善`
- Source workflow: Playtest Package Run #18
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
- Dark board: 低彩度・識別しやすい9色、白を避けた青墨色の境界と×
- Compact layout: スマホ縦画面・低背PCでHeader / Level / Dogs / Board / Actions / Tutorial / Helpを残して画面高さに収める（極端に短い画面はスクロール許容）
- Hint: Player UIでは非提供
- Status: `Level / Dogs`のみ（TREATS / TIMEなし）
- Artifact size: 3,102,684 bytes
- Artifact SHA-256: `3c8948d31b2716e583c840b8c3f393a996059f09255695ebb9300e0507e0a206`
- Pages deployment: PR Merge後に`main`から自動再配信
