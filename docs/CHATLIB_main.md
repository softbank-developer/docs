## Members

<dl>
<dt><a href="#NB_CLFS">NB_CLFS</a> : <code>Integer</code></dt>
<dd><p>分類器数</p>
</dd>
<dt><a href="#CONF_INDEX">CONF_INDEX</a> : <code>Object</code></dt>
<dd><p>設定シートフィールドインデックス</p>
</dd>
<dt><a href="#SELF_SS">SELF_SS</a> : <code>Spreadsheet</code></dt>
<dd><p>バインドされているスプレッドシートオブジェクト</p>
</dd>
<dt><a href="#SS_ID">SS_ID</a> : <code>String</code></dt>
<dd><p>バインドされているスプレッドシートのID</p>
</dd>
<dt><a href="#CREDS">CREDS</a> : <code>Creds</code></dt>
<dd><p>クレデンシャル情報</p>
</dd>
<dt><a href="#CONFIG_SET">CONFIG_SET</a> : <code>ConfigSet</code></dt>
<dd><p>設定メタデータ</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#include">include(filename)</a> ⇒ <code>Object</code></dt>
<dd><p>インクルード
htmlコンテンツをインクルードする</p>
</dd>
<dt><a href="#doGet">doGet(e)</a> ⇒ <code>Object</code></dt>
<dd><p>HTMLサービス</p>
</dd>
<dt><a href="#doPost">doPost(e)</a> ⇒ <code>JSON</code></dt>
<dd><p>LINE応答処理</p>
</dd>
<dt><a href="#onOpen">onOpen()</a></dt>
<dd><p>オープン時処理</p>
</dd>
</dl>

<a name="NB_CLFS"></a>

## NB_CLFS : <code>Integer</code>
分類器数

**Kind**: global variable  
<a name="CONF_INDEX"></a>

## CONF_INDEX : <code>Object</code>
設定シートフィールドインデックス

**Kind**: global variable  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| ws_name | <code>Integer</code> | シート名 |
| start_col | <code>Integer</code> | 定義開始列 |
| start_row | <code>Integer</code> | 定義開始行 |
| text_col | <code>Integer</code> | 学習テキスト列 |
| intent1_col | <code>Integer</code> | インテント列1 |
| result1_col | <code>Integer</code> | 分類結果列1 |
| resconf1_col | <code>Integer</code> | 確信度列1 |
| restime1_col | <code>Integer</code> | 分類日時列1 |
| intent2_col | <code>Integer</code> | インテント列2 |
| result2_col | <code>Integer</code> | 分類結果列2 |
| resconf2_col | <code>Integer</code> | 確信度列2 |
| restime2_col | <code>Integer</code> | 分類日時列2 |
| intent3_col | <code>Integer</code> | インテント列3 |
| result3_col | <code>Integer</code> | 分類結果列3 |
| resconf3_col | <code>Integer</code> | 確信度列3 |
| restime3_col | <code>Integer</code> | 分類日時列3 |
| log_ws | <code>Integer</code> | ログシート名 |
| conv_ws | <code>Integer</code> | 応答設定シート名 |
| start_msg | <code>Integer</code> | 開始メッセージ |
| other_msg | <code>Integer</code> | 該当なしメッセージ |
| error_msg | <code>Integer</code> | 例外メッセージ |
| avatar_url | <code>Integer</code> | アバターアイコンURL |
| giveup_msg | <code>Integer</code> | テキスト以外のメッセージ |

<a name="SELF_SS"></a>

## SELF_SS : <code>Spreadsheet</code>
バインドされているスプレッドシートオブジェクト

**Kind**: global variable  
<a name="SS_ID"></a>

## SS_ID : <code>String</code>
バインドされているスプレッドシートのID

**Kind**: global variable  
<a name="CREDS"></a>

## CREDS : <code>Creds</code>
クレデンシャル情報

**Kind**: global variable  
<a name="CONFIG_SET"></a>

## CONFIG_SET : <code>ConfigSet</code>
設定メタデータ

**Kind**: global variable  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| ss_id | <code>String</code> | スプレッドシートID |
| ws_name | <code>String</code> | 設定シート名 |
| st_start_row | <code>Integer</code> | 設定シート定義開始行 |
| st_start_col | <code>Integer</code> | 設定シート定義開始列 |
| notif_start_row | <code>Integer</code> | 通知設定定義開始行 |
| notif_start_col | <code>Integer</code> | 通知設定定義開始列 |
| result_override | <code>Boolean</code> | 分類結果上書きオプション |
| clfs_start_col | <code>Integer</code> | 分類器表示開始列 |
| clfs_start_row | <code>Integer</code> | 分類器表示開始行 |
| log_start_col | <code>Integer</code> | ログ開始列 |
| log_start_row | <code>Integer</code> | ログ開始行 |

<a name="include"></a>

## include(filename) ⇒ <code>Object</code>
インクルード
htmlコンテンツをインクルードする

**Kind**: global function  
**Returns**: <code>Object</code> - HtmlService  

| Param | Type | Description |
| --- | --- | --- |
| filename | <code>String</code> | ファイル名 |

<a name="doGet"></a>

## doGet(e) ⇒ <code>Object</code>
HTMLサービス

**Kind**: global function  
**Returns**: <code>Object</code> - HTML  

| Param | Type | Description |
| --- | --- | --- |
| e | <code>Event</code> | イベントパラメータ |

<a name="doPost"></a>

## doPost(e) ⇒ <code>JSON</code>
LINE応答処理

**Kind**: global function  
**Returns**: <code>JSON</code> - 応答JSON  

| Param | Type | Description |
| --- | --- | --- |
| e | <code>Event</code> | イベントパラメータ |

<a name="onOpen"></a>

## onOpen()
オープン時処理

**Kind**: global function  
