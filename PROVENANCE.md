# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `80337653392657346009cdfaa6712f773e71799f`
- Source change: `feat(game): タップ入力刷新とProduction Bank 3,000問化 (#30)`
- Playtest Package run: `#13`
- Artifact: `Jackdoku.html`
- Artifact size: `1879841 bytes`
- Artifact SHA-256: `758f43db33705f604181fb6a2979b349570a70d560088459f71f7e7d532d9c86`
- Artifact Git Blob SHA-1: `201b6b648dc6e104ec9524e8dcb6c49609f73924`
- Playable levels: `3000`
- Board progression: `5x5`〜`9x9`
- Level 161〜3000: `9x9`
- Level 1〜200 Published prefix SHA-256: `9fc0e8c60ca3695f667c08bd54b049d8cfcb2c302cb9b5cd7dab5e4dc6c0681b`
- Level 1〜2000 Compatibility prefix SHA-256: `aea24b369f78070051921728f4a82c3af8f918b5f6fdd2ef46e87011e80db1ab`
- Primary input: Single Tap / Click = ×, Double Tap / Double Click = Jack, Swipe / Drag = bulk ×
- Distribution target: `index.html`

## Promotion rule

1. Private開発リポジトリの`main`からPlaytest Packageを生成する。
2. Automated VerificationがGreenであることを確認する。
3. ArtifactのSHA-256を確認する。
4. Artifactを内容変更せず`index.html`としてこのPublic配布リポジトリへ昇格する。
5. Source commit / Artifact digestを本ファイルへ記録する。
6. Human Review後、Squash Mergeする。

Web配布用の都合でゲーム内容を直接編集しない。修正が必要な場合はPrivate開発リポジトリへ戻して検証し、新しいAccepted Buildを再昇格する。
