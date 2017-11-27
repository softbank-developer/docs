## Members

<dl>
<dt><a href="#RSS_FIELDS">RSS_FIELDS</a> : <code>Object</code></dt>
<dd><p>RSSデータフィールドインデックス</p>
</dd>
<dt><a href="#FEED_FIELDS">FEED_FIELDS</a> : <code>Object</code></dt>
<dd><p>取得フィードフィールドインデックス</p>
</dd>
<dt><a href="#FEED_WS_NAME">FEED_WS_NAME</a> : <code>String</code></dt>
<dd><p>フィード取得用シート名</p>
</dd>
<dt><a href="#RSS_NAMES">RSS_NAMES</a> : <code>Array.&lt;String&gt;</code></dt>
<dd><p>取得フィード項目名</p>
</dd>
<dt><a href="#TRAIN_COLUMN">TRAIN_COLUMN</a> : <code>Object</code></dt>
<dd><p>学習対象選択オプション</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#RSSUTIL_load_config">RSSUTIL_load_config(config_set)</a> ⇒ <code>Object</code></dt>
<dd><p>設定情報を取得する</p>
</dd>
<dt><a href="#RSSUTIL_get_feeds">RSSUTIL_get_feeds(feed_set)</a> ⇒ <code>Object</code></dt>
<dd><p>RSSフィードを取得する</p>
</dd>
<dt><a href="#RSSUTIL_clear_work">RSSUTIL_clear_work(feed_set)</a></dt>
<dd><p>ワークエリアを消去する</p>
</dd>
<dt><a href="#RSSUTIL_update_data">RSSUTIL_update_data(data_set)</a></dt>
<dd><p>RSSフィードを追記する</p>
</dd>
<dt><a href="#RSSUTIL_load_rss">RSSUTIL_load_rss(feed_set, rss_set)</a></dt>
<dd><p>RSSフォードを取得してシートに追記する</p>
</dd>
<dt><a href="#RSSUTIL_crawl">RSSUTIL_crawl()</a></dt>
<dd><p>全てのRSSフィードを取得してシートに追記する</p>
</dd>
<dt><a href="#RSSUTIL_train">RSSUTIL_train(train_set, creds_username, creds_password)</a> ⇒ <code>Object</code></dt>
<dd><p>RSSフィードのテキストを学習する</p>
</dd>
<dt><a href="#RSSUTIL_train_set">RSSUTIL_train_set(clf_no)</a></dt>
<dd><p>特定分類器で学習して結果をログに出力する</p>
</dd>
<dt><a href="#RSSUTIL_train_all">RSSUTIL_train_all()</a></dt>
<dd><p>イベント実行用学習処理</p>
</dd>
<dt><a href="#RSSUTIL_classify">RSSUTIL_classify(test_set, creds_username, creds_password, override)</a> ⇒ <code>Object</code></dt>
<dd><p>RSSフィードのテキストを分類する</p>
</dd>
<dt><a href="#RSSUTIL_classify_set">RSSUTIL_classify_set(clf_no)</a></dt>
<dd><p>特定分類器で分類して結果をログに出力する</p>
</dd>
<dt><a href="#RSSUTIL_classify_all">RSSUTIL_classify_all()</a></dt>
<dd><p>イベント実行用分類処理</p>
</dd>
<dt><a href="#RSSUTIL_train_no1">RSSUTIL_train_no1()</a></dt>
<dd><p>分類器1の学習</p>
</dd>
<dt><a href="#RSSUTIL_train_no2">RSSUTIL_train_no2()</a></dt>
<dd><p>分類器2の学習</p>
</dd>
<dt><a href="#RSSUTIL_train_no3">RSSUTIL_train_no3()</a></dt>
<dd><p>分類器3の学習</p>
</dd>
<dt><a href="#RSSUTIL_classify_no1">RSSUTIL_classify_no1()</a></dt>
<dd><p>分類器1の分類</p>
</dd>
<dt><a href="#RSSUTIL_classify_no2">RSSUTIL_classify_no2()</a></dt>
<dd><p>分類器2の分類</p>
</dd>
<dt><a href="#RSSUTIL_classify_no3">RSSUTIL_classify_no3()</a></dt>
<dd><p>分類器3の分類</p>
</dd>
</dl>

<a name="RSS_FIELDS"></a>

## RSS_FIELDS : <code>Object</code>
RSSデータフィールドインデックス

**Kind**: global variable  
<a name="FEED_FIELDS"></a>

## FEED_FIELDS : <code>Object</code>
取得フィードフィールドインデックス

**Kind**: global variable  
<a name="FEED_WS_NAME"></a>

## FEED_WS_NAME : <code>String</code>
フィード取得用シート名

**Kind**: global variable  
<a name="RSS_NAMES"></a>

## RSS_NAMES : <code>Array.&lt;String&gt;</code>
取得フィード項目名

**Kind**: global variable  
<a name="TRAIN_COLUMN"></a>

## TRAIN_COLUMN : <code>Object</code>
学習対象選択オプション

**Kind**: global variable  
<a name="RSSUTIL_load_config"></a>

## RSSUTIL_load_config(config_set) ⇒ <code>Object</code>
設定情報を取得する

**Kind**: global function  
**Returns**: <code>Object</code> - 設定情報  
**Throws**:

- <code>Error</code> 設定シートが不明です
- <code>Error</code> 設定シートに問題があります


| Param | Type | Description |
| --- | --- | --- |
| config_set | <code>Object</code> | メタデータ |

<a name="RSSUTIL_get_feeds"></a>

## RSSUTIL_get_feeds(feed_set) ⇒ <code>Object</code>
RSSフィードを取得する

**Kind**: global function  
**Returns**: <code>Object</code> - フィード  

| Param | Type | Description |
| --- | --- | --- |
| feed_set | <code>Object</code> | 設定情報 |

<a name="RSSUTIL_clear_work"></a>

## RSSUTIL_clear_work(feed_set)
ワークエリアを消去する

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| feed_set | <code>Object</code> | 取得設定 |

<a name="RSSUTIL_update_data"></a>

## RSSUTIL_update_data(data_set)
RSSフィードを追記する

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| data_set | <code>Object</code> | 配置情報 |

<a name="RSSUTIL_load_rss"></a>

## RSSUTIL_load_rss(feed_set, rss_set)
RSSフォードを取得してシートに追記する

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| feed_set | <code>Object</code> | 取得設定 |
| rss_set | <code>Object</code> | 配置設定 |

<a name="RSSUTIL_crawl"></a>

## RSSUTIL_crawl()
全てのRSSフィードを取得してシートに追記する

**Kind**: global function  
<a name="RSSUTIL_train"></a>

## RSSUTIL_train(train_set, creds_username, creds_password) ⇒ <code>Object</code>
RSSフィードのテキストを学習する

**Kind**: global function  
**Returns**: <code>Object</code> - 学習結果  
**Throws**:

- <code>Error</code> データシートが不明です
- <code>Error</code> 学習・分類対象が不正です


| Param | Type | Description |
| --- | --- | --- |
| train_set | <code>Object</code> | 学習設定 |
| creds_username | <code>String</code> | クレデンシャル |
| creds_password | <code>String</code> | クレデンシャル |

<a name="RSSUTIL_train_set"></a>

## RSSUTIL_train_set(clf_no)
特定分類器で学習して結果をログに出力する

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| clf_no | <code>Integer</code> | 分類器番号 |

<a name="RSSUTIL_train_all"></a>

## RSSUTIL_train_all()
イベント実行用学習処理

**Kind**: global function  
<a name="RSSUTIL_classify"></a>

## RSSUTIL_classify(test_set, creds_username, creds_password, override) ⇒ <code>Object</code>
RSSフィードのテキストを分類する

**Kind**: global function  
**Returns**: <code>Object</code> - 分類結果  
**Throws**:

- <code>Error</code> データシートが不明です
- <code>Error</code> 学習・分類対象が不正です


| Param | Type | Description |
| --- | --- | --- |
| test_set | <code>Object</code> | 分類設定 |
| creds_username | <code>String</code> | クレデンシャル |
| creds_password | <code>String</code> | クレデンシャル |
| override | <code>Boolean</code> | 上書きオプション |

<a name="RSSUTIL_classify_set"></a>

## RSSUTIL_classify_set(clf_no)
特定分類器で分類して結果をログに出力する

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| clf_no | <code>Integer</code> | 分類器番号 |

<a name="RSSUTIL_classify_all"></a>

## RSSUTIL_classify_all()
イベント実行用分類処理

**Kind**: global function  
**Throws**:

- <code>Error</code> データシートが不明です
- <code>Error</code> 学習・分類対象が不正です

<a name="RSSUTIL_train_no1"></a>

## RSSUTIL_train_no1()
分類器1の学習

**Kind**: global function  
<a name="RSSUTIL_train_no2"></a>

## RSSUTIL_train_no2()
分類器2の学習

**Kind**: global function  
<a name="RSSUTIL_train_no3"></a>

## RSSUTIL_train_no3()
分類器3の学習

**Kind**: global function  
<a name="RSSUTIL_classify_no1"></a>

## RSSUTIL_classify_no1()
分類器1の分類

**Kind**: global function  
<a name="RSSUTIL_classify_no2"></a>

## RSSUTIL_classify_no2()
分類器2の分類

**Kind**: global function  
<a name="RSSUTIL_classify_no3"></a>

## RSSUTIL_classify_no3()
分類器3の分類

**Kind**: global function  
