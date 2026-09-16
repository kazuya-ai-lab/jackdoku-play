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

- Source: `kazuya-ai-lab/jackdoku` `fde1e03274631013e49238a1372328f4d6e0710b`
- Source change: PR #24 `feat(levels): Production Bankを1,000レベルへ拡張`
- Source workflow: Playtest Package Run #9
- Playable levels: 1,000
- Board progression: 5×5〜12×12
- Status: `Level / Dogs`のみ（TREATS / TIMEなし）
- Artifact size: 831,284 bytes
- Artifact SHA-256: `1fab0b5e9351302c0c689c01e98dcfc77d8eb7dabf935d69b5f2ca3d065c6545`
- Pages deployment: PR Merge後に`main`から自動再配信
