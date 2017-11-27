# NLC 処理概要

## 学習処理

分類器を作成し、 シートの学習対象のテキストを学習させる

	※ UIが利用可能な場合は、確認ダイアログを表示する

### 1. 設定情報の取得 (NLCUTIL_load_config)

メタデータからユーザー設定情報を取得する

### 2. 分類器一覧の取得 ([NLCAPI_get_classifiers](../NLCLIB/#NLCAPI_get_classifiers))

APIを実行する

### 3. データシートの読み込み

データシートから学習の元データを取得する

1. データシートが取得できない場合は例外を発生する

1. 以下の条件のいずれかに該当する場合は学習データなしとして処理する

	!!! tip "条件"
	    - 最終行 < 開始行
	    - 最終列 < インテント列
	    - 最終列 < 学習テキスト列

### 4. 学習データの作成(CSV)

各行からCSV形式の学習データを作成する

1. 以下の条件のいずれかに該当する場合は学習データに含めない

	!!! tip "条件"
		- インテント名がブランクの場合
		- 学習テキストがブランクの場合

2. インテント名、学習テキストの編集

	!!! note "編集ルール"
		- 改行、タブは削除する
		- シングル・ダブルクォートは、ダブルクォートでエスケープする
		- 前後の空白はトリミングする
		- 長さが1024文字を超える場合は、先頭から1024文字以内に切りつめる

3. インテント名、学習テキストをカンマで結合し、学習データに改行(LF)を入れて追加する

### 5. 学習の実行

1. 分類器のバージョン一覧の取得 (NLCUTIL_clf_vers)

	分類器名を最新バージョン＋１に設定する

1. 分類器の作成 (NLCAPI_post_classifiers)

 	NLCのAPIを実行する

1. 旧バージョンの削除 (NLCAPI_delete_classifier)

 	APIの実行ステータスが200で、作成した分類器が３世代目になる場合は１世代目のバージョンを削除する

### 6. 分類器の状態チェック

1. 分類器状態更新処理 (NLCUTIL_exec_check_clfs)

	設定シートに表示されている分類器の状態を更新する

2. 状態更新処理をタイマーにセットする (NLCUTIL_set_trigger)

	分類器状態更新処理(NLCUTIL_exec_check_clfs)を指定間隔でタイマーにセットする

### 7. ログ出力 (NLCUTIL_log_train)

---

## モジュール構造図
```mermaid
graph TB
  subgraph NLCUTIL_classify_all
  A(NLCUTIL_load_config)-->B(NLCAPI_get_classifiers)
  B(NLCAPI_get_classifiers)-->C(NLCUTIL_clf_vers)
  C(NLCUTIL_clf_vers)-->D(NLCAPI_post_classifiers)
  D(NLCAPI_post_classifiers)-->E(NLCAPI_delete_classifier)
  E(NLCAPI_delete_classifier)-->F(NLCUTIL_exec_check_clfs)
  F(NLCUTIL_exec_check_clfs)-->G(NLCUTIL_set_trigger)
  G(NLCUTIL_set_trigger)-->H(NLCUTIL_log_classify)
  end
```
