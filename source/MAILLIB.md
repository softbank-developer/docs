## Members

<dl>
<dt><a href="#MAIL_FIELDS">MAIL_FIELDS</a> : <code>Object</code></dt>
<dd><p>メールデータフィールドインデックス</p>
</dd>
<dt><a href="#TRAIN_COLUMN">TRAIN_COLUMN</a> : <code>Object</code></dt>
<dd><p>学習対象選択オプション</p>
</dd>
<dt><a href="#MAX_THREADS">MAX_THREADS</a> : <code>Integer</code></dt>
<dd><p>GmailApp search 最大スレッド数</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#MAILUTIL_load_config">MAILUTIL_load_config(config_set)</a> ⇒ <code><a href="#Config">Config</a></code></dt>
<dd><p>設定情報の取得</p>
</dd>
<dt><a href="#MAILUTIL_get_newest">MAILUTIL_get_newest(mail_set)</a> ⇒ <code>Date</code></dt>
<dd><p>最新</p>
</dd>
<dt><a href="#MAILUTIL_get_messages">MAILUTIL_get_messages(mail_set)</a> ⇒ <code>MailData</code></dt>
<dd><p>メールを取得する</p>
</dd>
<dt><a href="#MAILUTIL_trim_exc">MAILUTIL_trim_exc(mail_set)</a> ⇒ <code><a href="#MailSet">MailSet</a></code></dt>
<dd><p>本文を正規表現で除外する</p>
</dd>
<dt><a href="#MAILUTIL_update_data">MAILUTIL_update_data(mail_set)</a></dt>
<dd><p>シートのメールデータを更新する</p>
</dd>
<dt><a href="#MAILUTIL_load_messages">MAILUTIL_load_messages()</a></dt>
<dd><p>取得メールをシートに配置する</p>
</dd>
<dt><a href="#MAILUTIL_train">MAILUTIL_train(train_set, creds_username, creds_password)</a> ⇒ <code>TrainResult</code></dt>
<dd><p>学習処理</p>
</dd>
<dt><a href="#MAILUTIL_train_set">MAILUTIL_train_set(clf_no)</a></dt>
<dd><p>対象分類器を学習する</p>
</dd>
<dt><a href="#MAILUTIL_train_all">MAILUTIL_train_all()</a></dt>
<dd><p>全分類器を学習</p>
</dd>
<dt><a href="#MAILUTIL_classify_all">MAILUTIL_classify_all()</a></dt>
<dd><p>全分類器で分類</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#ConfigMeta">ConfigMeta</a> : <code>Object</code></dt>
<dd><p>設定メタデータ</p>
</dd>
<dt><a href="#SheetConf">SheetConf</a> : <code>Object</code></dt>
<dd><p>データシート設定</p>
</dd>
<dt><a href="#NotifConf">NotifConf</a> : <code>Object</code></dt>
<dd><p>通知設定</p>
</dd>
<dt><a href="#ExcConf">ExcConf</a> : <code>Object</code></dt>
<dd><p>本文除外設定</p>
</dd>
<dt><a href="#Config">Config</a> : <code>Object</code></dt>
<dd><p>設定情報</p>
</dd>
<dt><a href="#MailSet">MailSet</a> : <code>Object</code></dt>
<dd></dd>
</dl>

<a name="MAIL_FIELDS"></a>

## MAIL_FIELDS : <code>Object</code>
メールデータフィールドインデックス

**Kind**: global variable  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| ID | <code>Integer</code> | メールID |
| DATE | <code>Integer</code> | 受信日時 |
| SUBJECT | <code>Integer</code> | 件名 |
| FROM | <code>Integer</code> | 送信元メールアドレス |
| TO | <code>Integer</code> | 送信先メールアドレス |
| CC | <code>Integer</code> | CCメールアドレス |
| BODY | <code>Integer</code> | 本文 |
| NORM_BODY | <code>Integer</code> | 本文(処理対象) |

<a name="TRAIN_COLUMN"></a>

## TRAIN_COLUMN : <code>Object</code>
学習対象選択オプション

**Kind**: global variable  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| SUBJECT | <code>String</code> | 件名のみ |
| BODY | <code>String</code> | 本文 |
| BOTH | <code>String</code> | 両方 |

<a name="MAX_THREADS"></a>

## MAX_THREADS : <code>Integer</code>
GmailApp search 最大スレッド数

**Kind**: global variable  
<a name="MAILUTIL_load_config"></a>

## MAILUTIL_load_config(config_set) ⇒ [<code>Config</code>](#Config)
設定情報の取得

**Kind**: global function  
**Returns**: [<code>Config</code>](#Config) - 設定情報  
**Throws**:

- <code>Error</code> 設定シートが不明です
- <code>Error</code> 設定シートに問題があります


| Param | Type | Description |
| --- | --- | --- |
| config_set | [<code>ConfigMeta</code>](#ConfigMeta) | メタデータ |

<a name="MAILUTIL_get_newest"></a>

## MAILUTIL_get_newest(mail_set) ⇒ <code>Date</code>
最新

**Kind**: global function  
**Returns**: <code>Date</code> - 最新日付  
**Throws**:

- <code>Error</code> データシートが不明です


| Param | Type | Description |
| --- | --- | --- |
| mail_set | [<code>MailSet</code>](#MailSet) | メール設定 |

<a name="MAILUTIL_get_messages"></a>

## MAILUTIL_get_messages(mail_set) ⇒ <code>MailData</code>
メールを取得する

**Kind**: global function  
**Returns**: <code>MailData</code> - メールデータ  

| Param | Type | Description |
| --- | --- | --- |
| mail_set | [<code>MailSet</code>](#MailSet) | 設定情報 |

<a name="MAILUTIL_trim_exc"></a>

## MAILUTIL_trim_exc(mail_set) ⇒ [<code>MailSet</code>](#MailSet)
本文を正規表現で除外する

**Kind**: global function  
**Returns**: [<code>MailSet</code>](#MailSet) - 編集結果  

| Param | Type | Description |
| --- | --- | --- |
| mail_set | [<code>MailSet</code>](#MailSet) | 設定情報 |

<a name="MAILUTIL_update_data"></a>

## MAILUTIL_update_data(mail_set)
シートのメールデータを更新する

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| mail_set | [<code>MailSet</code>](#MailSet) | メール情報 |

<a name="MAILUTIL_load_messages"></a>

## MAILUTIL_load_messages()
取得メールをシートに配置する

**Kind**: global function  
**Throws**:

- <code>Error</code> 過去分取得日数が不正です

<a name="MAILUTIL_train"></a>

## MAILUTIL_train(train_set, creds_username, creds_password) ⇒ <code>TrainResult</code>
学習処理

**Kind**: global function  
**Returns**: <code>TrainResult</code> - 学習結果  
**Throws**:

- <code>Error</code> データシートが不明です
- <code>Error</code> 学習・分類対象が不正です


| Param | Type | Description |
| --- | --- | --- |
| train_set | <code>TrainSet</code> | 学習情報 |
| creds_username | <code>String</code> | クレデンシャル |
| creds_password | <code>String</code> | クレデンシャル |

<a name="MAILUTIL_train_set"></a>

## MAILUTIL_train_set(clf_no)
対象分類器を学習する

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| clf_no | <code>Integer</code> | 分類器番号 |

<a name="MAILUTIL_train_all"></a>

## MAILUTIL_train_all()
全分類器を学習

**Kind**: global function  
<a name="MAILUTIL_classify_all"></a>

## MAILUTIL_classify_all()
全分類器で分類

**Kind**: global function  
**Throws**:

- <code>Error</code> 学習・分類対象が不正です
- <code>Error</code> データシートが不明です

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
| query | <code>String</code> | フィルタクエリ |
| search_limit | <code>Integer</code> | 最大取得スレッド数 |
| ago_days | <code>Integer</code> | 過去分取得日数 |

<a name="NotifConf"></a>

## NotifConf : <code>Object</code>
通知設定

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| notif_opt | <code>String</code> | 通知オプション{On,Off} |
| notif_ws | <code>String</code> | 設定シート名 |

<a name="ExcConf"></a>

## ExcConf : <code>Object</code>
本文除外設定

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| re_list | <code>Array.&lt;String&gt;</code> | 正規表現リスト |

<a name="Config"></a>

## Config : <code>Object</code>
設定情報

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| sheet_conf | [<code>SheetConf</code>](#SheetConf) | データシート設定 |
| notif_conf | [<code>NotifConf</code>](#NotifConf) | 通知設定 |
| exc_conf | [<code>ExcConf</code>](#ExcConf) | 本文除外設定 |

<a name="MailSet"></a>

## MailSet : <code>Object</code>
**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| ss_id | <code>String</code> | SS_ID |
| ws_name | <code>String</code> | シート名 |
| start_col | <code>String</code> | 開始列 |
| start_row | <code>String</code> | 開始行 |
| query | <code>String</code> | クエリ |
| search_limit | <code>String</code> | 最大スレッド数 |
| exc_res | <code>String</code> | 除外設定 |
| msgs | <code>String</code> | メッセージ |

