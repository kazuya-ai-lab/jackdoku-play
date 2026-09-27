# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `08cce5db8f15d7b8510202280704056de52db769`
- Source change: `fix(input): シングルタップ待機を200msへ短縮 (#32)`
- Playtest Package run: `#15`
- Artifact: `Jackdoku.html`
- Artifact size: `1879841 bytes`
- Artifact SHA-256: `9dc69c4e8d605ffd49f688cd01a24cf8bd70fd4f66665a849c6a23bcea024cce`
- Artifact Git Blob SHA-1: `99f8611e3c7159fb32a58a358ff0518f15f598ba`
- Playable levels: `3000`
- Board progression: `5x5`〜`9x9`
- Level 161〜3000: `9x9`
- Level 1〜200 Published prefix SHA-256: `9fc0e8c60ca3695f667c08bd54b049d8cfcb2c302cb9b5cd7dab5e4dc6c0681b`
- Level 1〜2000 Compatibility prefix SHA-256: `aea24b369f78070051921728f4a82c3af8f918b5f6fdd2ef46e87011e80db1ab`
- Primary input: Single Tap / Click = ×, Double Tap / Double Click = Jack, Swipe / Drag = bulk ×
- Single Tap arbitration window: `200ms`
- Distribution target: `index.html`

## Promotion rule

1. Private開発リポジトリの`main`からPlaytest Packageを生成する。
2. Automated VerificationがGreenであることを確認する。
3. ArtifactのSHA-256を確認する。
4. Artifactを内容変更せず`index.html`としてこのPublic配布リポジトリへ昇格する。
5. Source commit / Artifact digestを本ファイルへ記録する。
6. Human Review後、Squash Mergeする。

Web配布用の都合でゲーム内容を直接編集しない。修正が必要な場合はPrivate開発リポジトリへ戻して検証し、新しいAccepted Buildを再昇格する。
