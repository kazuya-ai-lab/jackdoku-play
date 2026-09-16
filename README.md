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

- Source: `kazuya-ai-lab/jackdoku` `8c4c263ecc26005387af2db9993875edae4f0fb2`
- Source change: PR #22 `feat(game): TREATSとTIMEを削除`
- Source workflow: Playtest Package Run #8
- Playable levels: 200
- Status: `Level / Dogs`のみ（TREATS / TIMEなし）
- Artifact size: 206,060 bytes
- Artifact SHA-256: `9478c61df88044d58dfe97ed351bf1223fcfe9329f05875f4554ee79886c2d10`
- Pages deployment: PR Merge後に`main`から自動再配信
