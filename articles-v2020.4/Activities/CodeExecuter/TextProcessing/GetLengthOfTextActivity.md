# テキストの長さを取得

テキストの長さを取得します。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。


### 入力

- **テキスト** ：テキストデータを入力します。文字列変数と文字列のみをサポートします。

### 出力
- **長さ** ：現在のテキストの長さを出力します。Int変数のみをサポートします。

## 操作サンプル

1. **テキストの長さを取得**アクティビティをドラッグ、対応する変数を作成して記入する。

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfTextActivity2021010501.png)

2. 他のアクティビティにドラッグ。例：**ログに書き込み**アクティビティをドラッグ、取得したテキストの長さをテキスト形式でログに出力する。

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfTextActivity2021010502.png)

3. 実行をクリックして、プロセスの実行に成功し、テキストの長さを取得しました。

![Image text](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfTextActivity2021010503.png)