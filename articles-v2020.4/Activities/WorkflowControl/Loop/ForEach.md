# 繰り返し(For Each)

ユーザーがあるオブジェクト内のデータを1つずつアクセスして処理することをサポートします。

## プロパティ
### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

### 入力
-  **本体** ：繰り返しを実行されるオブジェクトセット

### 出力
-  **現在のインデックス** ：今回の繰り返しのオブジェクトインデックス


## 操作サンプル
1. 変数listを設定。変数の種類は`List<String>`に設定。デフォルト値 `new List<String>{"a","b","c"}`を追加。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/forEach-1.png)

2. **繰り返し（For Each）**アクティビティをドラッグ、本体を変数リストに設定。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/forEach-2.png)

3. ダブルクリックしてアクティビティを展開。**ログに書き込み**アクティビティを繰り返し（For Each）アクティビティコンテナにドラッグ、ログテキストを設定：“今の値は： ” + item、プロセス実行をクリック、出力されたログを確認。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/forEach-3.png)

