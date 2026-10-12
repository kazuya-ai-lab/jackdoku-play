# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `64382f36c10d7565de0dae6c98e058701b6dcfee`
- Source change: `fix(ux): ライト境界を3pxに揃えダーク枠線を青みグレーへ改善 (#39)`
- Playtest Package run: `#22`
- Playtest Package workflow run ID: `38240831528`
- Artifact ID: `11743073430`
- Artifact: `Jackdoku.html`
- Artifact size: `3103792 bytes`
- Artifact SHA-256: `021de174ef99a1abe78509258dd63753ca236802b52323b585b8dceb38548930`
- Artifact Git Blob SHA-1: `4abd9ade0dfb7eb8698ee28c20e0a77662c99df9`
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
- Light board: 外枠とRegion境界4方向を各辺CSS 3pxに統一。Region境界は隣接セルが両側へ描画。通常Cell gridは1pxを維持
- Dark board: 明るく鮮やかな9色（L*約68〜85、C*約36〜61）を維持。外枠とRegion境界は3px・#5b6975で統一し、ページに約3.1:1、Regionに最小約2.3:1のコントラスト。×は#18262fのままでRegionとの3:1以上を維持
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
