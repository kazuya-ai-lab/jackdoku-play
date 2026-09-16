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

- Source: `kazuya-ai-lab/jackdoku` `2e7a7d205d6fc10db9b01f84784443f0c4a87611`
- Source change: PR #21 `feat(levels): 200レベルBankと10,000対応基盤を追加`
- Source workflow: Playtest Package Run #7
- Playable levels: 200
- Artifact size: 210,992 bytes
- Artifact SHA-256: `83c79ae666aff350c127f5d4a8fdde8c371db88eea761bd0e93017b371dbc6eb`
- Pages deployment: PR Merge後に`main`から自動再配信
