## Members

<dl>
<dt><a href="#NLCAPI_CLF_STATUS">NLCAPI_CLF_STATUS</a> : <code>Object</code></dt>
<dd><p>分類器のステータス</p>
</dd>
<dt><a href="#CLFNAME_PREFIX">CLFNAME_PREFIX</a> : <code>String</code></dt>
<dd><p>分類器名のプリフィクス</p>
</dd>
<dt><a href="#CLF_SEP">CLF_SEP</a> : <code>String</code></dt>
<dd><p>分類器名のセパレータ</p>
</dd>
<dt><a href="#NOTIF_OPT">NOTIF_OPT</a> : <code>Object</code></dt>
<dd><p>通知オプション</p>
</dd>
<dt><a href="#NOTIF_INDEX">NOTIF_INDEX</a> : <code>Object</code></dt>
<dd><p>通知ルールレコードのフィールドインデックス</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#NLCUTIL_load_creds">NLCUTIL_load_creds()</a> ⇒ <code><a href="#Creds">Creds</a></code></dt>
<dd><p>クレデンシャル情報の取得</p>
<p>利用するNLCインスタンスのクレデンシャル情報をスクリプトプロパティから取得する</p></dd>
<dt><a href="#NLCUTIL_load_config">NLCUTIL_load_config(config_set)</a> ⇒ <code><a href="#Config">Config</a></code></dt>
<dd><p>設定情報の取得</p>
<p>メタデータを元にユーザーの設定情報を取得する</p></dd>
<dt><a href="#NLCUTIL_expand_tags">NLCUTIL_expand_tags(target, fields)</a> ⇒ <code><a href="#ExpandResult">ExpandResult</a></code></dt>
<dd><p>通知ルール用の埋め込みタグを展開する</p>
<p>対象テキスト中に埋め込まれたタグをインデックスに該当する対象フィールドに置換する</p>
<p>埋め込みタグの形式 [[#インデックス]] ※インデックスは1以上の列として有効な整数</p></dd>
<dt><a href="#NLCUTIL_load_notif_rules">NLCUTIL_load_notif_rules(config_set)</a> ⇒ <code><a href="#Rules">Array.&lt;Rules&gt;</a></code></dt>
<dd><p>通知条件の取得</p>
<p>
</p></dd>
<dt><a href="#NLCUTIL_escape_formula">NLCUTIL_escape_formula(text)</a> ⇒ <code>String</code></dt>
<dd><p>数式評価文字抑止</p>
<p><p>セルの数式として評価される特殊文字をシングルクォートでエスケープする</p>
</dd>
<dt><a href="#NLCUTIL_norm_text">NLCUTIL_norm_text(target)</a> ⇒ <code>String</code></dt>
<dd><p>NLC学習用にテキストをノーマライズする</p>
<ul>
<li>シングルとダブルのクォートはダブルクォートでエスケープ</li>
<li>タブ、改行は削除</li>
<li>前後の空白をトリミング</li>
</ul></dd>
<dt><a href="#NLCUTIL_clf_vers">NLCUTIL_clf_vers(clf_list, target_name)</a> ⇒ <code><a href="#ClfVers">ClfVers</a></code></dt>
<dd><p>分類器のバージョン一覧を取得</p>
<p>分類器一覧から分類器名(ex. CLF1)に該当するバージョン一覧を生成する</p></dd>
<dt><a href="#NLCUTIL_select_clf">NLCUTIL_select_clf(clf_name, creds_username, creds_password)</a> ⇒ <code><a href="#ClfInfo">ClfInfo</a></code></dt>
<dd><p>利用可能な分類器の最新バージョンを取得する</p>
<p>ステータスコードが200以外の場合、IDに空白、ステータスにNLCの実行ステータスをセットする</p>
<p>バージョン件数が０件の場合、IDに空白、ステータスに&#39;Nothing&#39;をセットする</p>
<p>各バージョンの状態を取得する</p>
<p>状態が&#39;Available&#39;でバージョンが最新の分類器情報を返す</p></dd>
<dt><a href="#NLCUTIL_send_mail">NLCUTIL_send_mail(mail_set)</a></dt>
<dd><p>メールの送信</p>
<p>GmailAppのsendEmailを実行する</p></dd>
<dt><a href="#NLCUTIL_check_notify">NLCUTIL_check_notify(notif_set, record, upd_flg)</a></dt>
<dd><p>メール通知条件チェック</p>
<p>通知条件にマッチした場合はメールを送信する</p>
<p>件名と本文の埋め込みタグを展開する</p>
<p>インテントがブランクの場合はワイルドカード扱いする</p></dd>
<dt><a href="#NLCUTIL_log_classify">NLCUTIL_log_classify(log_set, test_set, test_result)</a></dt>
<dd><p>分類結果ログ出力</p>
</dd>
<dt><a href="#NLCUTIL_log_delete">NLCUTIL_log_delete(log_set, del_set, del_result)</a></dt>
<dd><p>分類器削除ログ出力</p>
</dd>
<dt><a href="#NLCUTIL_open_dialog">NLCUTIL_open_dialog(title, msg, buttons)</a> ⇒ <code>Object</code></dt>
<dd><p>ダイアログオープン</p>
</dd>
<dt><a href="#NLCUTIL_classify_all">NLCUTIL_classify_all()</a></dt>
<dd><p>イベント実行用分類処理</p>
</dd>
<dt><a href="#NLCUTIL_exec_check_clfs">NLCUTIL_exec_check_clfs()</a></dt>
<dd><p>タイマー起動用分類器状態チェック</p>
</dd>
<dt><a href="#NLCUTIL_set_trigger">NLCUTIL_set_trigger(func_name, int_min)</a></dt>
<dd><p>タイマーをセットする</p>
</dd>
<dt><a href="#NLCUTIL_del_trigger">NLCUTIL_del_trigger(func_name)</a></dt>
<dd><p>タイマーを解除する</p>
</dd>
<dt><a href="#NLCUTIL_train">NLCUTIL_train(train_set, creds_username, creds_password)</a> ⇒ <code>Object</code></dt>
<dd><p>学習処理</p>
</dd>
<dt><a href="#NLCUTIL_train_set">NLCUTIL_train_set(clf_no)</a></dt>
<dd><p>特定分類器で学習して結果をログに出力する</p>
</dd>
<dt><a href="#NLCUTIL_train_all">NLCUTIL_train_all()</a></dt>
<dd><p>イベント実行用学習処理</p>
</dd>
<dt><a href="#NLCUTIL_delete_classifier">NLCUTIL_delete_classifier(clf_no)</a></dt>
<dd><p>分類器削除</p>
</dd>
<dt><a href="#NLCUTIL_del_clf1">NLCUTIL_del_clf1()</a></dt>
<dd><p>分類器1削除</p>
</dd>
<dt><a href="#NLCUTIL_del_clf2">NLCUTIL_del_clf2()</a></dt>
<dd><p>分類器2削除</p>
</dd>
<dt><a href="#NLCUTIL_del_clf3">NLCUTIL_del_clf3()</a></dt>
<dd><p>分類器3削除</p>
</dd>
<dt><a href="#NLCUTIL_log_train">NLCUTIL_log_train(log_set, train_set, res)</a></dt>
<dd><p>学習結果ログ出力</p>
</dd>
<dt><a href="#NLCUTIL_check_classifiers">NLCUTIL_check_classifiers(clf_set, creds)</a></dt>
<dd><p>分類器の状態確認</p>
</dd>
<dt><a href="#NLCAPI_get_classifiers">NLCAPI_get_classifiers(p_username, p_password)</a> ⇒ <code><a href="#APIResult">APIResult</a></code></dt>
<dd><p>Classifier一覧取得</p>
<p>GET /v1/classifiers</p>
<p>概要: NLCサービスのClassifier一覧を取得する</p></dd>
<dt><a href="#NLCAPI_post_classifiers">NLCAPI_post_classifiers(p_username, p_password, p_training_data, p_classname, p_langcode)</a> ⇒ <code><a href="#APIResult">APIResult</a></code></dt>
<dd><p>Classifier生成</p>
<p>POST /v1/classifiers</p>
<p>概要: 資格情報に該当するNLCサービスにClassifierを新規作成する</p></dd>
<dt><a href="#NLCAPI_post_classify">NLCAPI_post_classify(p_username, p_password, p_classid, p_phrase)</a> ⇒ <code><a href="#APIResult">APIResult</a></code></dt>
<dd><p>クラス分類</p>
<p>POST /v1/classifiers/{classifier_id}/classify</p>
<p>概要: 文章を対象の分類器で分類する</p></dd>
<dt><a href="#NLCAPI_get_classify">NLCAPI_get_classify(p_username, p_password, p_classid, p_phrase)</a> ⇒ <code><a href="#APIResult">APIResult</a></code></dt>
<dd><p>クラス分類</p>
<p>GET /v1/classifiers/{classifier_id}/classify</p>
<p>概要: 文章を対象のClassifierで分類する</p></dd>
<dt><a href="#NLCAPI_delete_classifier">NLCAPI_delete_classifier(p_username, p_password, p_classid)</a> ⇒ <code><a href="#APIResult">APIResult</a></code></dt>
<dd><p>Classifier削除</p>
<p>DELETE /v1/classifiers/{classifier_id}</p>
<p>概要: 対象のClassifierを削除する</p></dd>
<dt><a href="#NLCAPI_get_classifier">NLCAPI_get_classifier(p_username, p_password, p_classid)</a> ⇒ <code><a href="#APIResult">APIResult</a></code></dt>
<dd><p>Classifier情報取得</p>
<p>GET /v1/classifiers/{classifier_id}</p>
<p>概要: 対象のClassifierについてステータスなどの情報を取得する</p></dd>
<dt><a href="#NLCAPI_createBoundary">NLCAPI_createBoundary()</a> ⇒ <code>String</code></dt>
<dd><p>multipartデータ送信のバウンダリ生成</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#SheetSet">SheetSet</a> : <code>Object</code></dt>
<dd><p>シート基本情報</p>
</dd>
<dt><a href="#Creds">Creds</a> : <code>Object</code></dt>
<dd><p>クレデンシャル情報</p>
</dd>
<dt><a href="#ConfigMeta">ConfigMeta</a> : <code>Object</code></dt>
<dd><p>設定メタデータ</p>
</dd>
<dt><a href="#SheetConf">SheetConf</a> : <code>Object</code></dt>
<dd><p>データシート設定</p>
</dd>
<dt><a href="#NotifConf">NotifConf</a> : <code>Object</code></dt>
<dd><p>通知設定</p>
</dd>
<dt><a href="#Config">Config</a> : <code>Object</code></dt>
<dd><p>設定情報</p>
</dd>
<dt><a href="#ExpandResult">ExpandResult</a> : <code>Object</code></dt>
<dd><p>展開結果</p>
</dd>
<dt><a href="#Mail">Mail</a> : <code>Object</code></dt>
<dd><p>メール設定</p>
</dd>
<dt><a href="#Rules">Rules</a> : <code>Object</code></dt>
<dd><p>通知条件</p>
</dd>
<dt><a href="#ClassifierInfoPayload">ClassifierInfoPayload</a> : <code>Object</code></dt>
<dd><p>分類器情報</p>
</dd>
<dt><a href="#ClfVers">ClfVers</a> : <code>Object</code></dt>
<dd><p>分類器バージョン一覧</p>
</dd>
<dt><a href="#ClfInfo">ClfInfo</a> : <code>Object</code></dt>
<dd><p>分類器情報</p>
</dd>
<dt><a href="#SheetSet">SheetSet</a> : <code>Object</code></dt>
<dd><p>クレデンシャル情報</p>
</dd>
<dt><a href="#APIResult">APIResult</a> : <code>Object</code></dt>
<dd><p>分類器情報</p>
</dd>
</dl>

<a name="NLCAPI_CLF_STATUS"></a>

## NLCAPI_CLF_STATUS : <code>Object</code>
分類器のステータス

**Kind**: global variable  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| AVAILABLE | <code>String</code> | 利用可能 |
| TRAINING | <code>String</code> | トレーニング中 |
| NOTHING | <code>String</code> | 利用不可 |

<a name="CLFNAME_PREFIX"></a>

## CLFNAME_PREFIX : <code>String</code>
分類器名のプリフィクス

**Kind**: global variable  
<a name="CLF_SEP"></a>

## CLF_SEP : <code>String</code>
分類器名のセパレータ

**Kind**: global variable  
<a name="NOTIF_OPT"></a>

## NOTIF_OPT : <code>Object</code>
通知オプション

**Kind**: global variable  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| ON | <code>String</code> | オン |
| OFF | <code>String</code> | オフ |

<a name="NOTIF_INDEX"></a>

## NOTIF_INDEX : <code>Object</code>
通知ルールレコードのフィールドインデックス

**Kind**: global variable  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| result1 | <code>Integer</code> | 分類結果1 |
| result2 | <code>Integer</code> | 分類結果2 |
| result3 | <code>Integer</code> | 分類結果3 |
| from | <code>Integer</code> | 送信元メールアドレス |
| to | <code>Integer</code> | 送信先メールアドレス |
| cc | <code>Integer</code> | CCメールアドレス |
| bcc | <code>Integer</code> | BCCメールアドレス |
| subject | <code>Integer</code> | 件名 |
| body | <code>Integer</code> | 本文 |

<a name="NLCUTIL_load_creds"></a>

## NLCUTIL_load_creds() ⇒ [<code>Creds</code>](#Creds)
クレデンシャル情報の取得
<p>利用するNLCインスタンスのクレデンシャル情報をスクリプトプロパティから取得する</p>

**Kind**: global function  
**Returns**: [<code>Creds</code>](#Creds) - クレデンシャル情報  
**Throws**:

- <code>Error</code> クレデンシャルが不明です

<a name="NLCUTIL_load_config"></a>

## NLCUTIL_load_config(config_set) ⇒ [<code>Config</code>](#Config)
設定情報の取得
<p>メタデータを元にユーザーの設定情報を取得する</p>

**Kind**: global function  
**Returns**: [<code>Config</code>](#Config) - コンフィグ  
**Throws**:

- <code>Error</code> 設定シートが不明です
- <code>Error</code> 設定シートに問題があります
- <code>Error</code> 学習・分類対象列が不正です'


| Param | Type | Description |
| --- | --- | --- |
| config_set | [<code>ConfigMeta</code>](#ConfigMeta) | コンフィグメタデータ |

<a name="NLCUTIL_expand_tags"></a>

## NLCUTIL_expand_tags(target, fields) ⇒ [<code>ExpandResult</code>](#ExpandResult)
通知ルール用の埋め込みタグを展開する
<p>対象テキスト中に埋め込まれたタグをインデックスに該当する対象フィールドに置換する</p>
<p>埋め込みタグの形式 [[#インデックス]] ※インデックスは1以上の列として有効な整数</p>

**Kind**: global function  
**Returns**: [<code>ExpandResult</code>](#ExpandResult) - 展開結果  

| Param | Type | Description |
| --- | --- | --- |
| target | <code>String</code> | 変換対象テキスト |
| fields | <code>Array.&lt;String&gt;</code> | 展開対象フィールド |

<a name="NLCUTIL_load_notif_rules"></a>

## NLCUTIL_load_notif_rules(config_set) ⇒ [<code>Array.&lt;Rules&gt;</code>](#Rules)
通知条件の取得
<p>
</p>

**Kind**: global function  
**Returns**: [<code>Array.&lt;Rules&gt;</code>](#Rules) - 通知条件  
**Throws**:

- <code>Error</code> 通知設定シートに問題があります


| Param | Type | Description |
| --- | --- | --- |
| config_set | [<code>SheetSet</code>](#SheetSet) | 設定情報 |

<a name="NLCUTIL_escape_formula"></a>

## NLCUTIL_escape_formula(text) ⇒ <code>String</code>
数式評価文字抑止
<p>セルの数式として評価される特殊文字をシングルクォートでエスケープする

**Kind**: global function  
**Returns**: <code>String</code> - 編集結果  

| Param | Type | Description |
| --- | --- | --- |
| text | <code>String</code> | 対象テキスト |

<a name="NLCUTIL_norm_text"></a>

## NLCUTIL_norm_text(target) ⇒ <code>String</code>
NLC学習用にテキストをノーマライズする
<ul>
<li>シングルとダブルのクォートはダブルクォートでエスケープ</li>
<li>タブ、改行は削除</li>
<li>前後の空白をトリミング</li>
</ul>

**Kind**: global function  
**Returns**: <code>String</code> - 変換結果  

| Param | Type | Description |
| --- | --- | --- |
| target | <code>String</code> | 変換対象テキスト |

<a name="NLCUTIL_clf_vers"></a>

## NLCUTIL_clf_vers(clf_list, target_name) ⇒ [<code>ClfVers</code>](#ClfVers)
分類器のバージョン一覧を取得
<p>分類器一覧から分類器名(ex. CLF1)に該当するバージョン一覧を生成する</p>

**Kind**: global function  
**Returns**: [<code>ClfVers</code>](#ClfVers) - バージョン一覧  

| Param | Type | Description |
| --- | --- | --- |
| clf_list | [<code>Array.&lt;ClassifierInfoPayload&gt;</code>](#ClassifierInfoPayload) | 分類器一覧 |
| target_name | <code>String</code> | 分類器名 |

<a name="NLCUTIL_select_clf"></a>

## NLCUTIL_select_clf(clf_name, creds_username, creds_password) ⇒ [<code>ClfInfo</code>](#ClfInfo)
利用可能な分類器の最新バージョンを取得する
<p>ステータスコードが200以外の場合、IDに空白、ステータスにNLCの実行ステータスをセットする</p>
<p>バージョン件数が０件の場合、IDに空白、ステータスに'Nothing'をセットする</p>
<p>各バージョンの状態を取得する</p>
<p>状態が'Available'でバージョンが最新の分類器情報を返す</p>

**Kind**: global function  
**Returns**: [<code>ClfInfo</code>](#ClfInfo) - 分類器情報  

| Param | Type | Description |
| --- | --- | --- |
| clf_name | <code>String</code> | 分類器名 ex.CLF1 |
| creds_username | <code>String</code> | ユーザー名(クレデンシャル) |
| creds_password | <code>String</code> | パスワード(クレデンシャル) |

<a name="NLCUTIL_send_mail"></a>

## NLCUTIL_send_mail(mail_set)
メールの送信
<p>GmailAppのsendEmailを実行する</p>

**Kind**: global function  
**Throws**:

- <code>Error</code> メールの送信に失敗しました


| Param | Type | Description |
| --- | --- | --- |
| mail_set | [<code>Mail</code>](#Mail) | メール通知設定 |

<a name="NLCUTIL_check_notify"></a>

## NLCUTIL_check_notify(notif_set, record, upd_flg)
メール通知条件チェック
<p>通知条件にマッチした場合はメールを送信する</p>
<p>件名と本文の埋め込みタグを展開する</p>
<p>インテントがブランクの場合はワイルドカード扱いする</p>

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| notif_set | <code>NotifSet</code> | 通知設定 |
| record | <code>Array.&lt;String&gt;</code> | 通知対象データ |
| upd_flg | <code>Array.&lt;Integer&gt;</code> | 更新フラグ |

<a name="NLCUTIL_log_classify"></a>

## NLCUTIL_log_classify(log_set, test_set, test_result)
分類結果ログ出力

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| log_set | <code>Object</code> | ログ出力設定 |
| test_set | <code>Object</code> | テスト設定 |
| test_result | <code>Object</code> | テスト結果 |

<a name="NLCUTIL_log_delete"></a>

## NLCUTIL_log_delete(log_set, del_set, del_result)
分類器削除ログ出力

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| log_set | <code>Object</code> | ログ設定 |
| del_set | <code>Object</code> | 削除設定 |
| del_result | <code>Object</code> | 削除結果 |

<a name="NLCUTIL_open_dialog"></a>

## NLCUTIL_open_dialog(title, msg, buttons) ⇒ <code>Object</code>
ダイアログオープン

**Kind**: global function  
**Returns**: <code>Object</code> - 選択したボタン  
**Throws**:

- <code>Error</code> データシートが不明です


| Param | Type | Description |
| --- | --- | --- |
| title | <code>String</code> | タイトル |
| msg | <code>String</code> | メッセージ |
| buttons | <code>Object</code> | 配置ボタン |

<a name="NLCUTIL_classify_all"></a>

## NLCUTIL_classify_all()
イベント実行用分類処理

**Kind**: global function  
**Throws**:

- <code>Error</code> データシートが不明

<a name="NLCUTIL_exec_check_clfs"></a>

## NLCUTIL_exec_check_clfs()
タイマー起動用分類器状態チェック

**Kind**: global function  
<a name="NLCUTIL_set_trigger"></a>

## NLCUTIL_set_trigger(func_name, int_min)
タイマーをセットする

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| func_name | <code>String</code> | セットする関数名 |
| int_min | <code>Integer</code> | 実行間隔(分) |

<a name="NLCUTIL_del_trigger"></a>

## NLCUTIL_del_trigger(func_name)
タイマーを解除する

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| func_name | <code>String</code> | 解除する関数名 |

<a name="NLCUTIL_train"></a>

## NLCUTIL_train(train_set, creds_username, creds_password) ⇒ <code>Object</code>
学習処理

**Kind**: global function  
**Returns**: <code>Object</code> - 学習結果  
**Throws**:

- <code>Error</code> データシートが不明です


| Param | Type | Description |
| --- | --- | --- |
| train_set | <code>Object</code> | 学習設定 |
| creds_username | <code>String</code> | クレデンシャル |
| creds_password | <code>String</code> | クレデンシャル |

<a name="NLCUTIL_train_set"></a>

## NLCUTIL_train_set(clf_no)
特定分類器で学習して結果をログに出力する

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| clf_no | <code>Integer</code> | 分類器番号 |

<a name="NLCUTIL_train_all"></a>

## NLCUTIL_train_all()
イベント実行用学習処理

**Kind**: global function  
<a name="NLCUTIL_delete_classifier"></a>

## NLCUTIL_delete_classifier(clf_no)
分類器削除

**Kind**: global function  
**Throws**:

- <code>Error</code> サーバーエラーが発生しました


| Param | Type | Description |
| --- | --- | --- |
| clf_no | <code>Integer</code> | 分類器番号 |

<a name="NLCUTIL_del_clf1"></a>

## NLCUTIL_del_clf1()
分類器1削除

**Kind**: global function  
<a name="NLCUTIL_del_clf2"></a>

## NLCUTIL_del_clf2()
分類器2削除

**Kind**: global function  
<a name="NLCUTIL_del_clf3"></a>

## NLCUTIL_del_clf3()
分類器3削除

**Kind**: global function  
<a name="NLCUTIL_log_train"></a>

## NLCUTIL_log_train(log_set, train_set, res)
学習結果ログ出力

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| log_set | <code>Object</code> | ログ出力設定 |
| train_set | <code>Object</code> | 学習設定 |
| res | <code>Object</code> | 学習結果 |

<a name="NLCUTIL_check_classifiers"></a>

## NLCUTIL_check_classifiers(clf_set, creds)
分類器の状態確認

**Kind**: global function  
**Throws**:

- <code>Error</code> 設定シートが不明です


| Param | Type | Description |
| --- | --- | --- |
| clf_set | <code>Object</code> | メタデータ |
| creds | [<code>Creds</code>](#Creds) | クレデンシャル |

<a name="NLCAPI_get_classifiers"></a>

## NLCAPI_get_classifiers(p_username, p_password) ⇒ [<code>APIResult</code>](#APIResult)
Classifier一覧取得
<p>GET /v1/classifiers</p>
<p>概要: NLCサービスのClassifier一覧を取得する</p>

**Kind**: global function  
**Returns**: [<code>APIResult</code>](#APIResult) - APIの実行結果  

| Param | Type | Description |
| --- | --- | --- |
| p_username | <code>String</code> | NLCサービス資格情報のusername |
| p_password | <code>String</code> | NLCサービス資格情報のpassword |

<a name="NLCAPI_post_classifiers"></a>

## NLCAPI_post_classifiers(p_username, p_password, p_training_data, p_classname, p_langcode) ⇒ [<code>APIResult</code>](#APIResult)
Classifier生成
<p>POST /v1/classifiers</p>
<p>概要: 資格情報に該当するNLCサービスにClassifierを新規作成する</p>

**Kind**: global function  
**Returns**: [<code>APIResult</code>](#APIResult) - APIの実行結果  

| Param | Type | Description |
| --- | --- | --- |
| p_username | <code>String</code> | NLCサービス資格情報のusername |
| p_password | <code>String</code> | NLCサービス資格情報のpassword |
| p_training_data | <code>String</code> | トレーニングデータ(CSV) |
| p_classname | <code>String</code> | クラス名(training_metadata) |
| p_langcode | <code>String</code> | 言語コード(オプション) |

<a name="NLCAPI_post_classify"></a>

## NLCAPI_post_classify(p_username, p_password, p_classid, p_phrase) ⇒ [<code>APIResult</code>](#APIResult)
クラス分類
<p>POST /v1/classifiers/{classifier_id}/classify</p>
<p>概要: 文章を対象の分類器で分類する</p>

**Kind**: global function  
**Returns**: [<code>APIResult</code>](#APIResult) - APIの実行結果  

| Param | Type | Description |
| --- | --- | --- |
| p_username | <code>String</code> | NLCサービス資格情報のusername |
| p_password | <code>String</code> | NLCサービス資格情報のpassword |
| p_classid | <code>String</code> | 分類器のクラスID |
| p_phrase | <code>String</code> | 分類する文章 |

<a name="NLCAPI_get_classify"></a>

## NLCAPI_get_classify(p_username, p_password, p_classid, p_phrase) ⇒ [<code>APIResult</code>](#APIResult)
クラス分類
<p>GET /v1/classifiers/{classifier_id}/classify</p>
<p>概要: 文章を対象のClassifierで分類する</p>

**Kind**: global function  
**Returns**: [<code>APIResult</code>](#APIResult) - APIの実行結果  

| Param | Type | Description |
| --- | --- | --- |
| p_username | <code>String</code> | NLCサービス資格情報のusername |
| p_password | <code>String</code> | NLCサービス資格情報のpassword |
| p_classid | <code>String</code> | Classifier_id |
| p_phrase | <code>String</code> | 分類する文章 |

<a name="NLCAPI_delete_classifier"></a>

## NLCAPI_delete_classifier(p_username, p_password, p_classid) ⇒ [<code>APIResult</code>](#APIResult)
Classifier削除
<p>DELETE /v1/classifiers/{classifier_id}</p>
<p>概要: 対象のClassifierを削除する</p>

**Kind**: global function  
**Returns**: [<code>APIResult</code>](#APIResult) - APIの実行結果  

| Param | Type | Description |
| --- | --- | --- |
| p_username | <code>String</code> | NLCサービス資格情報のusername |
| p_password | <code>String</code> | NLCサービス資格情報のpassword |
| p_classid | <code>String</code> | 削除対象のClassifier_id |

<a name="NLCAPI_get_classifier"></a>

## NLCAPI_get_classifier(p_username, p_password, p_classid) ⇒ [<code>APIResult</code>](#APIResult)
Classifier情報取得
<p>GET /v1/classifiers/{classifier_id}</p>
<p>概要: 対象のClassifierについてステータスなどの情報を取得する</p>

**Kind**: global function  
**Returns**: [<code>APIResult</code>](#APIResult) - APIの実行結果  

| Param | Type | Description |
| --- | --- | --- |
| p_username | <code>String</code> | NLCサービス資格情報のusername |
| p_password | <code>String</code> | NLCサービス資格情報のpassword |
| p_classid | <code>String</code> | 取得対象のClassifier_id |

<a name="NLCAPI_createBoundary"></a>

## NLCAPI_createBoundary() ⇒ <code>String</code>
multipartデータ送信のバウンダリ生成

**Kind**: global function  
**Returns**: <code>String</code> - バウンダリ  
<a name="SheetSet"></a>

## SheetSet : <code>Object</code>
シート基本情報

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| ss_id | <code>String</code> | スプレッドシートID |
| ws_name | <code>String</code> | シート名 |
| start_col | <code>Integer</code> | 開始列 |
| start_row | <code>Integer</code> | 開始行 |

<a name="Creds"></a>

## Creds : <code>Object</code>
クレデンシャル情報

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| username | <code>String</code> | ユーザー名 |
| password | <code>String</code> | パスワード |
| url | <code>String</code> | エンドポイント |

<a name="ConfigMeta"></a>

## ConfigMeta : <code>Object</code>
設定メタデータ

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| ss_id | <code>String</code> | スプレッドシートID |
| ws_name | <code>String</code> | 設定シート名 |
| st_start_row | <code>Integer</code> | 定義開始行 |
| st_start_col | <code>Integer</code> | 定義開始列 |

<a name="SheetConf"></a>

## SheetConf : <code>Object</code>
データシート設定

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| ws_name | <code>String</code> | データシート名 |
| start_row | <code>Integer</code> | 定義開始行 |
| start_col | <code>Integer</code> | 定義開始列 |
| intent_col | <code>Array.&lt;Integer&gt;</code> | インテント列1to3 |
| result_col | <code>Array.&lt;Integer&gt;</code> | 分類結果列1to3 |
| resconf_col | <code>Array.&lt;Integer&gt;</code> | 確信度列1to3 |
| restime_col | <code>Array.&lt;Integer&gt;</code> | 分類日時列1to3 |
| log_ws | <code>String</code> | ログシート名 |

<a name="NotifConf"></a>

## NotifConf : <code>Object</code>
通知設定

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| notif_opt | <code>String</code> | 通知オプション{On,Off} |
| notif_ws | <code>String</code> | 設定シート名 |

<a name="Config"></a>

## Config : <code>Object</code>
設定情報

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| sheet_conf | [<code>SheetConf</code>](#SheetConf) | データシート設定 |
| notif_conf | [<code>NotifConf</code>](#NotifConf) | 通知設定 |

<a name="ExpandResult"></a>

## ExpandResult : <code>Object</code>
展開結果

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| code | <code>String</code> | 結果コード |
| text | <code>String</code> | 結果テキスト |

<a name="Mail"></a>

## Mail : <code>Object</code>
メール設定

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| from | <code>String</code> | 送信元メールアドレス |
| to | <code>String</code> | 送信先メールアドレス |
| cc | <code>String</code> | ccメールアドレス |
| bcc | <code>String</code> | bccメールアドレス |
| subject | <code>String</code> | 件名 |
| body | <code>String</code> | 本文 |

<a name="Rules"></a>

## Rules : <code>Object</code>
通知条件

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| res_int | <code>Array.&lt;String&gt;</code> | 分類結果1to3 |
| mail | [<code>Mail</code>](#Mail) | メール設定 |

<a name="ClassifierInfoPayload"></a>

## ClassifierInfoPayload : <code>Object</code>
分類器情報

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| classifier_id | <code>String</code> | ID |
| name | <code>String</code> | 名称 |
| created | <code>String</code> | 作成日 |

<a name="ClfVers"></a>

## ClfVers : <code>Object</code>
分類器バージョン一覧

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| count | <code>Integer</code> | 件数 |
| min_ver | <code>Integer</code> | 最小バージョン |
| max_ver | <code>Integer</code> | 最大バージョン |
| clfs | [<code>Array.&lt;ClassifierInfoPayload&gt;</code>](#ClassifierInfoPayload) | 分類器情報 |

<a name="ClfInfo"></a>

## ClfInfo : <code>Object</code>
分類器情報

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| clf_id | <code>String</code> | ID |
| status | <code>String</code> | ステータス |

<a name="SheetSet"></a>

## SheetSet : <code>Object</code>
クレデンシャル情報

**Kind**: global typedef  
**Properties**

| Name | Type |
| --- | --- |
| ユーザー名 | <code>String</code> | 

<a name="APIResult"></a>

## APIResult : <code>Object</code>
分類器情報

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| status | <code>Integer</code> | レスポンスコード |
| body | <code>Object</code> | レスポンスボディ |
| from | <code>Long</code> | 開始時刻 |
| to | <code>Long</code> | 終了時刻 |
| delta | <code>Long</code> | 応答時間 |

