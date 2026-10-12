# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `e4f95af7b346ae81a05d5a9e6075728935ca6dc0`
- Source change: `feat(game): レベルを4,000へ拡張しテキスト選択を抑止 (#33)`
- Playtest Package run: `#16`
- Playtest Package workflow run ID: `38186743107`
- Artifact ID: `11720116833`
- Artifact: `Jackdoku.html`
- Artifact size: `2486450 bytes`
- Artifact SHA-256: `6a90eb05f7ca918cd96401b703e7a60a8f22b8514c545a03f92bb66269650ba3`
- Artifact Git Blob SHA-1: `fe6f7819b614ff78077535e156718bf5be4470ee`
- Playable levels: `4000`
- Board progression: `5x5`〜`9x9`
- Level 161〜4000: `9x9`
- Level 1〜200 Published prefix SHA-256: `9fc0e8c60ca3695f667c08bd54b049d8cfcb2c302cb9b5cd7dab5e4dc6c0681b`
- Level 1〜3000 Compatibility prefix SHA-256: `056d61addba4de72c6ab415e418797894042b9a08527462b976661619c592cb4`
- Primary input: Single Tap / Click = ×, Double Tap / Double Click = Jack, Swipe / Drag = bulk ×
- Single Tap arbitration window: `200ms`
- Level Select: 50件Paging / 80 pages
- Text selection: ゲームUIで抑止（Touch calloutも抑止）
- Distribution target: `index.html`

## Promotion rule

1. Private開発リポジトリの`main`からPlaytest Packageを生成する。
2. Automated VerificationがGreenであることを確認する。
3. ArtifactのSHA-256を確認する。
4. Artifactを内容変更せず`index.html`としてこのPublic配布リポジトリへ昇格する。
5. Source commit / Artifact digestを本ファイルへ記録する。
6. Human Review後、Squash Mergeする。

Web配布用の都合でゲーム内容を直接編集しない。修正が必要な場合はPrivate開発リポジトリへ戻して検証し、新しいAccepted Buildを再昇格する。
