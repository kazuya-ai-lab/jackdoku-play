# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `e962cf6dcd416decba18ebd15e3c6b6ea8858768`
- Source change: `feat(levels): 2,000問Bankと犬SVG操作UIへ更新 (#29)`
- Playtest Package run: `#12`
- Artifact: `Jackdoku.html`
- Artifact size: `1277351 bytes`
- Artifact SHA-256: `05cf2961c1acec681ee1cadeb2b0dde8f16648cb9897fb97d43a4e8bb5e7f778`
- Artifact Git Blob SHA-1: `f41d9198ff74eab20346eeb6bdbe320033dfae06`
- Playable levels: `2000`
- Board progression: `5x5`〜`9x9`
- Level 1〜200 Published prefix SHA-256: `9fc0e8c60ca3695f667c08bd54b049d8cfcb2c302cb9b5cd7dab5e4dc6c0681b`
- Level 1〜1000 Compatibility prefix SHA-256: `915a4e9fda2ef489fc7e73df188bc8db1b31a2fec3f633a97cf4ef68e170c95a`
- Distribution target: `index.html`

## Promotion rule

1. Private開発リポジトリの`main`からPlaytest Packageを生成する。
2. Automated VerificationがGreenであることを確認する。
3. ArtifactのSHA-256を確認する。
4. Artifactを内容変更せず`index.html`としてこのPublic配布リポジトリへ昇格する。
5. Source commit / Artifact digestを本ファイルへ記録する。
6. Human Review後、Squash Mergeする。

Web配布用の都合でゲーム内容を直接編集しない。修正が必要な場合はPrivate開発リポジトリへ戻して検証し、新しいAccepted Buildを再昇格する。
