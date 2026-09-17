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

- Source: `kazuya-ai-lab/jackdoku` `1a4f4e9f18cd6a20294fd4abac8d87b63a9e7af0`
- Source change: PR #27 `feat(ux): Human Playtestを反映して9×9上限と盤面視認性を改善`
- Source workflow: Playtest Package Run #11
- Playable levels: 1,000
- Board progression: 5×5〜9×9
- Level 161〜1,000: 9×9
- Status: `Level / Dogs`のみ（TREATS / TIMEなし）
- Artifact size: 691,798 bytes
- Artifact SHA-256: `2bbd171c63c217034c515afb801054af1563d83d4ffe11a44a99a05ec2f987ac`
- Pages deployment: PR Merge後に`main`から自動再配信
