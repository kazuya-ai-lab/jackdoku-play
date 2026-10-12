# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `b3cb39c5d9ec7070a187c0a40e52c8b3c4902bf7`
- Source change: `fix(ux): ライト盤面の外枠と色境界を2pxへ統一 (#38)`
- Playtest Package run: `#21`
- Playtest Package workflow run ID: `38230592353`
- Artifact ID: `11738018928`
- Artifact: `Jackdoku.html`
- Artifact size: `3103771 bytes`
- Artifact SHA-256: `a73a661ee0ea72b463ef98a492a2d65707c4c1fdd38e98bc177316330db5a9e9`
- Artifact Git Blob SHA-1: `22a8e903ea15bb838321b79d6d14316af93ee0d4`
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
- Light board: 外枠2px、Regionの可視境界は隣接セルの1px＋1pxで合計2pxに統一（通常Cell gridは1px）。ダーク側の外枠・Region境界3pxは維持
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
