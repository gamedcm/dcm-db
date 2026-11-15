# dcm-db (GGENDB)

SDガンダム ジージェネレーション エターナルのHARDステージ攻略データベース（非公式ファンサイト）。
公開先: https://gamedcm.github.io/dcm-db/

## 機能

- ステージ一覧（ドロップ / 捕獲 / キャラクターリクエスト）
- 作品（シリーズ）別フィルタ、ヒストリー除外トグル
- 武装強化パーツ別クイックフィルタ（★付き捕獲フィルタ含む）
- キーワード検索（ユニット名・ステージ名の逆引き。ドロップ・捕獲・リクエスト横断）
- 並び順の正順/逆順切り替え
- ガチャシミュレーター（タイトルロゴをタップ）

## データの持ち方

- `data.json` … ステージ情報の本体（id / series / name / drops / captures / charaRequest）
- `index.html` … 本体（CSS/JSインライン）。次回マスターリーグ情報はJS内の `NEXT_LEAGUE` 定数で管理
- フッターの「データ最終更新」は data.json の Last-Modified から自動表示

## 更新手順

1. ステージ追加・修正は `data.json` を編集（idは連番、重複なし）
2. マスターリーグのシーズンが切り替わったら `index.html` の `NEXT_LEAGUE` を書き換える
3. push すると GitHub Pages に自動で反映される
