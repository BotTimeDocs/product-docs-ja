# HTTPリクエスト

このアクティビティは、HTTリクエストを送信し、応答されたデータを返します。構成したHTTPリクエストが利用可能かどうかのテストをサポートします。

## プロパティ

### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。
- **タイムアウト(ミリ秒)** ：このアクティビティの実行時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。マッチングタイムアウト(ミリ秒)が含まれます。この時間を超えたら、アクティビティがまだ実行されていない場合、エラーがスローされます。

### 入力

- **URL** ：リクエストのURLを入力します。文字列変数と文字列のみをサポートします。
- **リクエストメソッド** ：リクエストのメソッドを選択します。GET、POST、HEAD、PUT、DELETE、OPTIONS、PATCHをサポートします。
- **内容の種類** ：リクエストの内容の種類を選択します。例えば、application/json
- **リクエストヘッダー** ：リクエストのヘッダを入力します。Dictionary変数のみをサポートします。"リクエストモードを設定"のポップアップ画面にリクエストヘッダー情報を入力することができます。同時にこのプロパティボックスとポップアップウィンドウにリクエストヘッダーを指定する場合、ポップアップウィンドウに設定された変数を使用します。
- **リクエストボディ** ：リクエストボディを入力します。文字列変数と文字列のみをサポートします。
- **タイムアウト(s)** ：リクエストタイムアウトの秒数を入力します。整形変数と整形値のみをサポートします。

### 出力

- **レスポンスボディ** ：このHTTPリクエストの戻りデータを出力します。変数のみをサポートします。

## 操作サンプル
1. 例ではaliyunの**為替レート**インターフェースを使用、インターフェースの説明：[aliyunの為替レート](https://market.aliyun.com/products/57000002/cmapi011221.html?spm=5176.12901015.0.i12901015.17e2525cz4KoQ4&innerSource=search_%E6%B1%87%E7%8E%87%E6%9F%A5%E8%AF%A2%E8%BD%AC%E6%8D%A2#sku=yuncode522100006)
2. インターフェースドキュメントは、下図のようになります。
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPRequest1.png)
3. **HTTPリクエスト**アクティビティをドラッグ、下図のように設定。
- `リクエストメソッド`：GET
- `URL`:
`https://jisuhurilv.market.alicloudia.com/exchange/convert？amount=10&from=CNY&to=USD`
- `内容の種類`:`none`
- `リクエストヘッダー`:`Authorization(key)`,`APPCODE APPcode値(value)`：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPRequest2.png)

4. `テスト`をクリック、テスト結果を確認、下図のように。
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/HTTPRequest3.png)