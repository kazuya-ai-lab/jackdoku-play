# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `8c4c263ecc26005387af2db9993875edae4f0fb2`
- Source change: `feat(game): TREATSとTIMEを削除 (#22)`
- Playtest Package run: `#8`
- Artifact: `Jackdoku.html`
- Artifact size: `206060 bytes`
- Artifact SHA-256: `9478c61df88044d58dfe97ed351bf1223fcfe9329f05875f4554ee79886c2d10`
- Artifact Git Blob SHA-1: `93d93ec6aae7f2f4784e4ca1305f368714cc6cea`
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
