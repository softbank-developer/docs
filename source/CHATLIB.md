## Members

<dl>
<dt><a href="#CONV_INDEX">CONV_INDEX</a> : <code>Object</code></dt>
<dd><p>応答設定フィールドインデックス</p>
</dd>
<dt><a href="#LINE_REPLY_URL">LINE_REPLY_URL</a> : <code>String</code></dt>
<dd><p>LINE応答メッセージ用URL</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#CHATUTIL_load_creds">CHATUTIL_load_creds()</a> ⇒ <code><a href="#ChatCreds">ChatCreds</a></code></dt>
<dd><p>クレデンシャル情報の取得</p>
<p>利用するNLCインスタンスのクレデンシャル情報をスクリプトプロパティから取得する</p>
<p>利用するLINEアカウントのアクセストークンをスクリプトプロパティから取得する</p></dd>
<dt><a href="#CHATUTIL_load_config">CHATUTIL_load_config(config_set)</a> ⇒ <code><a href="#ChatConfig">ChatConfig</a></code></dt>
<dd><p>設定情報の取得</p>
</dd>
<dt><a href="#CHATUTIL_load_conv_rules">CHATUTIL_load_conv_rules(config_set)</a> ⇒ <code>Config</code></dt>
<dd><p>応答設定の取得</p>
</dd>
<dt><a href="#CHATUTIL_expand_tags">CHATUTIL_expand_tags(p_temp, p_dict)</a> ⇒ <code>Object</code></dt>
<dd><p>埋め込みタグ展開</p>
</dd>
<dt><a href="#CHATUTIL_select_message">CHATUTIL_select_message(conv_set, res_classes)</a> ⇒ <code>Array.&lt;String&gt;</code></dt>
<dd><p>メッセージ選択</p>
</dd>
<dt><a href="#CHATUTIL_store_dialog">CHATUTIL_store_dialog(conv_set, res_classes)</a></dt>
<dd><p>会話記録</p>
</dd>
<dt><a href="#CHATUTIL_store_reply">CHATUTIL_store_reply(input, res_msg)</a></dt>
<dd><p>応答記録</p>
</dd>
<dt><a href="#CHATUTIL_send_message">CHATUTIL_send_message(input_text)</a> ⇒ <code>Object</code></dt>
<dd><p>メッセージ送信</p>
</dd>
<dt><a href="#CHATUTIL_train">CHATUTIL_train(train_set, log_set)</a></dt>
<dd><p>分類器の学習</p>
</dd>
<dt><a href="#CHATUTIL_train_set">CHATUTIL_train_set(clf_no)</a></dt>
<dd><p>[CHATUTIL_train_set description]</p>
</dd>
<dt><a href="#CHATUTIL_train_all">CHATUTIL_train_all()</a></dt>
<dd><p>全分類器を学習</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#ChatCreds">ChatCreds</a> : <code>Object</code></dt>
<dd><p>クレデンシャル情報</p>
</dd>
<dt><a href="#ChatConfig">ChatConfig</a> : <code>Object</code></dt>
<dd><p>設定情報</p>
</dd>
</dl>

<a name="CONV_INDEX"></a>

## CONV_INDEX : <code>Object</code>
応答設定フィールドインデックス

**Kind**: global variable  
<a name="LINE_REPLY_URL"></a>

## LINE_REPLY_URL : <code>String</code>
LINE応答メッセージ用URL

**Kind**: global variable  
<a name="CHATUTIL_load_creds"></a>

## CHATUTIL_load_creds() ⇒ [<code>ChatCreds</code>](#ChatCreds)
クレデンシャル情報の取得
<p>利用するNLCインスタンスのクレデンシャル情報をスクリプトプロパティから取得する</p>
<p>利用するLINEアカウントのアクセストークンをスクリプトプロパティから取得する</p>

**Kind**: global function  
**Returns**: [<code>ChatCreds</code>](#ChatCreds) - クレデンシャル情報  
**Throws**:

- <code>Error</code> NLCクレデンシャルが不明です
- <code>Error</code> LINEクレデンシャルが不明です

<a name="CHATUTIL_load_config"></a>

## CHATUTIL_load_config(config_set) ⇒ [<code>ChatConfig</code>](#ChatConfig)
設定情報の取得

**Kind**: global function  
**Returns**: [<code>ChatConfig</code>](#ChatConfig) - 設定情報  
**Throws**:

- <code>Error</code> 設定シートが不明です
- <code>Error</code> 設定シートに問題があります


| Param | Type | Description |
| --- | --- | --- |
| config_set | <code>ConfigMeta</code> | メタデータ |

<a name="CHATUTIL_load_conv_rules"></a>

## CHATUTIL_load_conv_rules(config_set) ⇒ <code>Config</code>
応答設定の取得

**Kind**: global function  
**Returns**: <code>Config</code> - 応答設定  
**Throws**:

- <code>Error</code> 応答設定シートに問題があります


| Param | Type | Description |
| --- | --- | --- |
| config_set | <code>ConfigMeta</code> | メタデータ |

<a name="CHATUTIL_expand_tags"></a>

## CHATUTIL_expand_tags(p_temp, p_dict) ⇒ <code>Object</code>
埋め込みタグ展開

**Kind**: global function  
**Returns**: <code>Object</code> - 展開結果  

| Param | Type | Description |
| --- | --- | --- |
| p_temp | <code>String</code> | 対象文字列 |
| p_dict | <code>EnvVars</code> | 辞書 |

<a name="CHATUTIL_select_message"></a>

## CHATUTIL_select_message(conv_set, res_classes) ⇒ <code>Array.&lt;String&gt;</code>
メッセージ選択

**Kind**: global function  
**Returns**: <code>Array.&lt;String&gt;</code> - 応答メッセージ  

| Param | Type | Description |
| --- | --- | --- |
| conv_set | <code>ConvSet</code> | 応答設定 |
| res_classes | <code>Object</code> | 分類結果 |

<a name="CHATUTIL_store_dialog"></a>

## CHATUTIL_store_dialog(conv_set, res_classes)
会話記録

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| conv_set | <code>ConvSet</code> | 応答設定 |
| res_classes | <code>Object</code> | 分類結果 |

<a name="CHATUTIL_store_reply"></a>

## CHATUTIL_store_reply(input, res_msg)
応答記録

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| input | <code>String</code> | 入力情報 |
| res_msg | <code>String</code> | 応答メッセージ |

<a name="CHATUTIL_send_message"></a>

## CHATUTIL_send_message(input_text) ⇒ <code>Object</code>
メッセージ送信

**Kind**: global function  
**Returns**: <code>Object</code> - 応答メッセージ  

| Param | Type | Description |
| --- | --- | --- |
| input_text | <code>String</code> | ユーザー入力 |

<a name="CHATUTIL_train"></a>

## CHATUTIL_train(train_set, log_set)
分類器の学習

**Kind**: global function  
**Throws**:

- <code>Error</code> データシートが不明です


| Param | Type | Description |
| --- | --- | --- |
| train_set | <code>TrainSet</code> | 学習設定 |
| log_set | <code>LogSet</code> | ログ設定 |

<a name="CHATUTIL_train_set"></a>

## CHATUTIL_train_set(clf_no)
[CHATUTIL_train_set description]

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| clf_no | <code>Integer</code> | 分類器番号 |

<a name="CHATUTIL_train_all"></a>

## CHATUTIL_train_all()
全分類器を学習

**Kind**: global function  
<a name="ChatCreds"></a>

## ChatCreds : <code>Object</code>
クレデンシャル情報

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| username | <code>String</code> | NLCのユーザー名 |
| password | <code>String</code> | NLCのパスワード |
| url | <code>String</code> | NLCのエンドポイント |
| channel_access_token | <code>String</code> | LINEチャネルアクセストークン |

<a name="ChatConfig"></a>

## ChatConfig : <code>Object</code>
設定情報

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| sheet_conf | <code>SheetConf</code> | データシート設定 |
| conv_conf | <code>ConvConf</code> | 応答設定 |

