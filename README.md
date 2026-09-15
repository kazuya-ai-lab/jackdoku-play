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

- Source: `kazuya-ai-lab/jackdoku` `d12277802ee3dbc6ab85c9600c1a36f1c569f385`
- Source workflow: Playtest Package Run #4
- Public main: `073fb2f9903c0632c123a474e814b1dcce268783`
- Artifact SHA-256: `5ebcd9b118a3fbe70a65115c03f056cc4e7dded31beb799f24ae61477ef06d3a`
- Pages deployment: SUCCESS
