# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `b0be5e8632aa350b323ef933508739b60566709b`
- Source change: `fix(ux): 盤面外のスクロール抑止とダーク配色の微調整 (#36)`
- Playtest Package run: `#19`
- Playtest Package workflow run ID: `38207243085`
- Artifact ID: `11727718039`
- Artifact: `Jackdoku.html`
- Artifact size: `3103172 bytes`
- Artifact SHA-256: `556a5166675091ef9ac2f41a427e6fdb253c68eb6a5b3519de220c692617720b`
- Artifact Git Blob SHA-1: `2fe899f3303d1e484b7c7c344085589a24f753a9`
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
- Dark board: 彩度を適度に高めた9色と、背景から判別しやすいグレー系外枠。青墨色のRegion境界 / Cell grid / ×は維持。色差とContrast検査を通過
- Responsive gameplay: Smartphone portrait / 低背DesktopでLevel、Dogs、Controls、Tutorial、Helpを省略せずViewport高さへ収める
- Scroll behavior: コンパクトスマホ画面のページスクロール / Bounceを抑止。Dialog内スクロール、ピンチ拡大、低背画面Fallbackを維持
- Distribution target: `index.html`

## Promotion rule

1. Private開発リポジトリの`main`からPlaytest Packageを生成する。
2. Automated VerificationがGreenであることを確認する。
3. ArtifactのSHA-256を確認する。
4. Artifactを内容変更せず`index.html`としてこのPublic配布リポジトリへ昇格する。
5. Source commit / Artifact digestを本ファイルへ記録する。
6. Human Review後、Squash Mergeする。

Web配布用の都合でゲーム内容を直接編集しない。修正が必要な場合はPrivate開発リポジトリへ戻して検証し、新しいAccepted Buildを再昇格する。
