# Distribution Provenance

このリポジトリの`index.html`は、Private開発リポジトリで検証済みとなったPlaytest Package ArtifactをそのままWeb配布へ昇格したものです。

## Current distribution

- Source repository: `kazuya-ai-lab/jackdoku` (Private)
- Source `main` commit: `d04ec030d9f56a1142d6e1f99d725d344d31fa9d`
- Source change: `fix(ux): ダーク盤面を落ち着いた低輝度の9色に調整 (#40)`
- Playtest Package run: `#23`
- Playtest Package workflow run ID: `38315918640`
- Artifact ID: `11777011335`
- Artifact: `Jackdoku.html`
- Artifact size: `3103783 bytes`
- Artifact SHA-256: `fb61b96f4632dedb94844733d0405aa0bfe99f93a7601aad5c931ea64d740225`
- Artifact Git Blob SHA-1: `b821e9ec02cba0f7dbc90a46203d9808eac0f1f4`
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
- Dark board: 9色を眩しさを抑えた中間暗色（L*約43〜45、平均相対輝度は前版比で約72%減）に変更。Regionの色相差・×とのコントラストを確保。外枠とRegion境界は3px・#98a6b0、×は#e4e8e8。眼精疲労軽減の実感は実機で評価する
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
