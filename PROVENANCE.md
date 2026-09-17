# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `1a4f4e9f18cd6a20294fd4abac8d87b63a9e7af0`
- Source change: `feat(ux): Human Playtestを反映して9×9上限と盤面視認性を改善 (#27)`
- Playtest Package run: `#11`
- Artifact: `Jackdoku.html`
- Artifact size: `691798 bytes`
- Artifact SHA-256: `2bbd171c63c217034c515afb801054af1563d83d4ffe11a44a99a05ec2f987ac`
- Artifact Git Blob SHA-1: `b3d6b29765ef01f922f727b6f046d2c8d98db0c1`
- Playable levels: `1000`
- Board progression: `5x5`〜`9x9`
- Published Level 1〜200 SHA-256: `9fc0e8c60ca3695f667c08bd54b049d8cfcb2c302cb9b5cd7dab5e4dc6c0681b`
- Distribution target: `index.html`

## Promotion rule

1. Private開発リポジトリの`main`からPlaytest Packageを生成する。
2. Automated VerificationがGreenであることを確認する。
3. ArtifactのSHA-256を確認する。
4. Artifactを内容変更せず`index.html`としてこのPublic配布リポジトリへ昇格する。
5. Source commit / Artifact digestを本ファイルへ記録する。
6. Human Review後、Squash Mergeする。

Web配布用の都合でゲーム内容を直接編集しない。修正が必要な場合はPrivate開発リポジトリへ戻して検証し、新しいAccepted Buildを再昇格する。
