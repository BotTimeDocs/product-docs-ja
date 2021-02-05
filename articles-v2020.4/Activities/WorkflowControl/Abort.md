# プロセスを終了
このアクティビティを実行するとすぐに現在のプロセスを終了し、後のプロセスは実行しません。


## プロパティ
### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

## 操作サンプル
1. **繰り返し(Do While)**アクティビティをドラッグ、変数countを作成し、繰り返し条件count<=100を設定:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Abort-1.png)

2. 二つの変数を作成、それぞれはworkEndDT & workStartDT、変数タイプをTimeSpanに設定。デフォルト値はそれぞれ`DateTime.Parse("7:30").TimeOfDay` & `DateTime.Parse("20:30").TimeOfDay`である。**プロセス条件分岐**アクティビティをドラッグ、判定条件を設定：`DateTime.Now.TimeOfDay > workEndDT && DateTime.Now.TimeOfDay < workStartDT`:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Abort-2.png)

3. 条件がTrueであると判断すると、**プロセスを終了**アクティビティを使ってプロセスを終了します。もし条件がFalseであると判断すると、**代入**アクティビティを使って、変数をインクリメントし、ループは続ける。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Abort-3.png)

4. プロセス実行をクリックして、実行結果を確認。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Abort-4.png)