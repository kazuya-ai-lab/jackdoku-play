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

- Source: `kazuya-ai-lab/jackdoku` `e962cf6dcd416decba18ebd15e3c6b6ea8858768`
- Source change: PR #29 `feat(levels): 2,000問Bankと犬SVG操作UIへ更新`
- Source workflow: Playtest Package Run #12
- Playable levels: 2,000
- Board progression: 5×5〜9×9
- Level 161〜2,000: 9×9
- Level Select: 50件Paging / 40 pages
- Mobile Dog input: Jack Russell Terrier inline SVG
- Hint: Player UIでは非提供
- Status: `Level / Dogs`のみ（TREATS / TIMEなし）
- Artifact size: 1,277,351 bytes
- Artifact SHA-256: `05cf2961c1acec681ee1cadeb2b0dde8f16648cb9897fb97d43a4e8bb5e7f778`
- Pages deployment: PR Merge後に`main`から自動再配信
