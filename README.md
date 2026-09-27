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

- Source: `kazuya-ai-lab/jackdoku` `08cce5db8f15d7b8510202280704056de52db769`
- Source change: PR #32 `fix(input): シングルタップ待機を200msへ短縮`
- Source workflow: Playtest Package Run #15
- Playable levels: 3,000
- Board progression: 5×5〜9×9
- Level 161〜3,000: 9×9
- Level Select: 50件Paging / 60 pages
- Single Tap / Click: ×（Double Tap判定待機 200ms）
- Double Tap / Double Click: Jack Russell Terrier
- Swipe / Drag: ×を一括入力
- 入力Mode切替Button: 非提供
- Right Click: Jack Russell Terrier（PC）
- Hint: Player UIでは非提供
- Status: `Level / Dogs`のみ（TREATS / TIMEなし）
- Artifact size: 1,879,841 bytes
- Artifact SHA-256: `9dc69c4e8d605ffd49f688cd01a24cf8bd70fd4f66665a849c6a23bcea024cce`
- Pages deployment: PR Merge後に`main`から自動再配信
