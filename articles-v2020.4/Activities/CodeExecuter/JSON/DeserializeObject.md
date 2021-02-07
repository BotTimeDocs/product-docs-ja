

# オブジェクトを逆シリアル化

このアクティビティはJSON文字列を.NETオブジェクトに逆シリアル化することができます。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。
- **タイムアウト(ミリ秒)** ：このアクティビティの実行時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。マッチングタイムアウト(ミリ秒)が含まれます。この時間を超えたら、アクティビティがまだ実行されていない場合、エラーがスローされます。

### 入力

- **JSON文字列** ：逆シリアル化されるJSONデータを入力します。文字列変数と文字列のみをサポートします。

### 出力

- **結果** ：逆シリアル化されたオブジェクトを入力します。変数のみをサポートします。

## 操作サンプル

1. **アクティビティ**エリアから**オブジェクトを逆シリアル化**と**ログに書き込み**を**編集エリア**にドラッグ。図の順序で接続し、名前空間**Newtonsoft.Json.Linq**をインポート:![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DeserializeObject1.png)

2. 2つの変数を作成。1つの変数タイプは**String**に設定。変数の値を*jsonタイプの文字列*に設定。例えば、**`"{'名前':'RPA','バージョン':1.0}"`** または **`"{""名前"":""RPA"",""バージョン"":1.0}"`** (全部英語の引用符です。単双引用符と引用符の数に注意してください。）他の変数のタイプは**JObject**に設定。もし変数タイプリストがない場合、**タイプをブラウザ**をクリック、ポップアップウィンドウで**JObject**を検索、選択してOKをクリック。![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DeserializeObject2.png)

3. アクティビティ**オブジェクトを逆シリアル化**右のプロパティの設定で、先ほど作成した2つの変数を入力。![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DeserializeObject3.png)

4. 一番目のログに書き込みのログの内容に変数**json文字列**を入力。2番目のログに書き込みのログの内容に**jsonオブジェクト.ToString()**を入力、**実行**プロセスをクリック、逆シリアル化されたものを見ることができます：![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/DeserializeObject4.png)

> **json**の内容もっと知りたい場合は、ネットワーク上の**[jsonチュートリアル](https://www.runoob.com/json/json-tutorial.html)**を参照してください。