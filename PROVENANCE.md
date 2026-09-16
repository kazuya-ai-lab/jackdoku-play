# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `fde1e03274631013e49238a1372328f4d6e0710b`
- Source change: `feat(levels): Production Bankを1,000レベルへ拡張 (#24)`
- Playtest Package run: `#9`
- Artifact: `Jackdoku.html`
- Artifact size: `831284 bytes`
- Artifact SHA-256: `1fab0b5e9351302c0c689c01e98dcfc77d8eb7dabf935d69b5f2ca3d065c6545`
- Artifact Git Blob SHA-1: `7b0dd71b342d79f36eb2c6a6c89caa9acda7d2dc`
- Playable levels: `1000`
- Board progression: `5x5`〜`12x12`
- Distribution target: `index.html`

## Promotion rule

1. Private開発リポジトリの`main`からPlaytest Packageを生成する。
2. Automated VerificationがGreenであることを確認する。
3. ArtifactのSHA-256を確認する。
4. Artifactを内容変更せず`index.html`としてこのPublic配布リポジトリへ昇格する。
5. Source commit / Artifact digestを本ファイルへ記録する。
6. Human Review後、Squash Mergeする。

Web配布用の都合でゲーム内容を直接編集しない。修正が必要な場合はPrivate開発リポジトリへ戻して検証し、新しいAccepted Buildを再昇格する。
