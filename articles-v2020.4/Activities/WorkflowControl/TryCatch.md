# 例外処理(TryCatch)

例外処理については、プロセスチャートまたはアクティビティ中の指定した例外タイプをキャッチし、エラー通知を表示するか実行を継続することができます。例外処理は三つの部分で構成されています。

- **Try** ：アクティビティが実行中にスロー可能の例外
- **Catches** ：例外がスローされる時のソリューション
    - **Exception** ：キャッチの例外のタイプ、複数追加可能
- **Finally** ：アクティビティ終了時に実行

## プロパティ
### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

## 操作サンプル

  1. **ブラウザを開く** アクティビティをドラッグ、次のURLを入力：https://www.aliyun.com"

  2. 変数listを設定。変数の種類を`List<String>`に設定、デフォルト値を`new List<String>{"最新の活動","製品","ソリューション"}`に設定。

    ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/tryCatch-1.png)

3. **繰り返し（For Each）** アクティビティを設定し、循環体を変数listに設定。 **例外処理(TryCatch)** アクティビティをドラッグ:

    ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/tryCatch-2.png)  

4. ダブルクリックして例外処理アクティビティを展開し、 **クリック**アクティビティをtryCatchコンテナにドラッグ、指定されたウェブページの一番上の"最新の活動"要素をクリックし、セレクタを開いてSinfo値の"最新の活動"を変数"{item}"に置き換える。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/tryCatch-3.png)

5. "新しいキャッチを追加"をクリックしてSystem.Exceptionオプションを選択、 **ログに書き込み** アクティビティをドラッグ、出力に`exception.Message+"最初のページに切り替え"`を入力; **ナビゲート** アクティビティをドラッグして次のURLを入力：https://www.aliyun.com"

    >**说明：**
    >
    >try容器でlistの最初の要素をクリックした後、現在のページは他のページに遷移し、そうすると、listの他の要素を循環的にクリックする時に失敗する。そのため、catchで初最初のページに切り替えを設定して、ページを初期化して、listの他の要素を正常にクリックすることができます。

    ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/tryCatch-4.png)

6. プロセスを実行して、結果を確認する。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/tryCatch-5.png)