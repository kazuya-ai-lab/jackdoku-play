# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `48677bf8e0e47716aafa3cde7854bb2aec0b68a2`
- Source change: `fix(ux): ダーク盤面の配色と1画面に収まるプレイUIを改善 (#35)`
- Playtest Package run: `#18`
- Playtest Package workflow run ID: `38203071188`
- Artifact ID: `11726695197`
- Artifact: `Jackdoku.html`
- Artifact size: `3102684 bytes`
- Artifact SHA-256: `3c8948d31b2716e583c840b8c3f393a996059f09255695ebb9300e0507e0a206`
- Artifact Git Blob SHA-1: `70264b0543ad5aae5c22b4aaa6312aa4028b1829`
- Playable levels: `5000`
- Board progression: `5x5`〜`9x9`
- Level 161〜5000: `9x9`
- Level 1〜200 Published prefix SHA-256: `9fc0e8c60ca3695f667c08bd54b049d8cfcb2c302cb9b5cd7dab5e4dc6c0681b`
- Level 1〜3000 Compatibility prefix SHA-256: `056d61addba4de72c6ab415e418797894042b9a08527462b976661619c592cb4`
- Primary input: Single Tap / Click = ×, Double Tap / Double Click = Jack, Swipe / Drag = bulk ×
- Single Tap arbitration window: `200ms`
- Level Select: 50件Paging / 100 pages
- Text selection: ゲームUIで抑止（Touch calloutも抑止）
- Display theme: system / light / dark、設定値をSave v2に互換保存
- Dark board: 低彩度の9色、青墨色のRegion境界 / Cell grid / ×に変更。色差とContrastの回帰テストを通過
- Responsive gameplay: Smartphone portrait / 低背DesktopでLevel、Dogs、Controls、Tutorial、Helpを省略せずViewport高さへ収める
- Distribution target: `index.html`

## Promotion rule

1. Private開発リポジトリの`main`からPlaytest Packageを生成する。
2. Automated VerificationがGreenであることを確認する。
3. ArtifactのSHA-256を確認する。
4. Artifactを内容変更せず`index.html`としてこのPublic配布リポジトリへ昇格する。
5. Source commit / Artifact digestを本ファイルへ記録する。
6. Human Review後、Squash Mergeする。

Web配布用の都合でゲーム内容を直接編集しない。修正が必要な場合はPrivate開発リポジトリへ戻して検証し、新しいAccepted Buildを再昇格する。
