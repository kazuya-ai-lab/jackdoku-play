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

- Source: `kazuya-ai-lab/jackdoku` `80337653392657346009cdfaa6712f773e71799f`
- Source change: PR #30 `feat(game): タップ入力刷新とProduction Bank 3,000問化`
- Source workflow: Playtest Package Run #13
- Playable levels: 3,000
- Board progression: 5×5〜9×9
- Level 161〜3,000: 9×9
- Level Select: 50件Paging / 60 pages
- Single Tap / Click: ×
- Double Tap / Double Click: Jack Russell Terrier
- Swipe / Drag: ×を一括入力
- 入力Mode切替Button: 非提供
- Right Click: Jack Russell Terrier（PC）
- Hint: Player UIでは非提供
- Status: `Level / Dogs`のみ（TREATS / TIMEなし）
- Artifact size: 1,879,841 bytes
- Artifact SHA-256: `758f43db33705f604181fb6a2979b349570a70d560088459f71f7e7d532d9c86`
- Pages deployment: PR Merge後に`main`から自動再配信
