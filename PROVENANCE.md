# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `2e7a7d205d6fc10db9b01f84784443f0c4a87611`
- Source change: `feat(levels): 200レベルBankと10,000対応基盤を追加 (#21)`
- Playtest Package run: `#7`
- Artifact: `Jackdoku.html`
- Artifact size: `210992 bytes`
- Artifact SHA-256: `83c79ae666aff350c127f5d4a8fdde8c371db88eea761bd0e93017b371dbc6eb`
- Artifact Git Blob SHA-1: `9280f02f7fc52c817d0baff3ecdb0bfad0965c64`
- Playable levels: `200`
- Distribution target: `index.html`

## Promotion rule

1. Private開発リポジトリの`main`からPlaytest Packageを生成する。
2. Automated VerificationがGreenであることを確認する。
3. ArtifactのSHA-256を確認する。
4. Artifactを内容変更せず`index.html`としてこのPublic配布リポジトリへ昇格する。
5. Source commit / Artifact digestを本ファイルへ記録する。
6. Human Review後、Squash Mergeする。

Web配布用の都合でゲーム内容を直接編集しない。修正が必要な場合はPrivate開発リポジトリへ戻して検証し、新しいAccepted Buildを再昇格する。
