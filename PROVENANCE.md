# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `b9ab6f9458ac11d2b613b84cf74de6efb1d559af`
- Source change: `fix(ux): ライト外枠を細く戻しダーク盤面の黒枠と鮮明な配色を統一 (#37)`
- Playtest Package run: `#20`
- Playtest Package workflow run ID: `38219198481`
- Artifact ID: `11732824468`
- Artifact: `Jackdoku.html`
- Artifact size: `3103370 bytes`
- Artifact SHA-256: `0c1afa8f3ef7562c8470a659ef944d4648ad56d6a11950debe589a919f12a7c0`
- Artifact Git Blob SHA-1: `a233287fb01f8a75571a728fc10a4f1177d656f9`
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
- Light board: 外枠を1pxに細く戻す。Region境界は3pxのまま
- Dark board: くすみを抑えた明るく鮮やかな9色（L*約68〜85、C*約36〜61）。外枠・Region境界を3px・#18262fで統一し、×も同色。色差とContrastの回帰検査を通過
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
