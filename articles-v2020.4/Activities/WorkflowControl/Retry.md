# リトライ

実行するプロセスが条件に適合し、それにエラーが発生した場合は再度実行を試します。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

### オプション

- **リトライカウント** ：リトライの回数を設定します。変数を入力できます。
- **リトライ時間間隔** ：リトライの間隔を設定します。デフォルトは分秒のフォーマットです：00:00:00。

## 操作サンプル

1. **リトライ**アクティビティをドラッグ、必要に応じてリトライ回数（3）とリトライ時間間隔（00:00:05）を設定します。ダブルクリックして展開し、**要素が表示されるまて待つ**アクティビティをドラッグ、操作する要素を指定し、結果変数を出力。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Retry-1.png)

2. リトライ条件を設定、`isTrue==false`、保存して実行プロセスをクリック、実行結果を確認。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Retry-2.png)

    - **条件** ：再実行の条件を設定します。条件表現式またはTrueなどのブール変数を接続できます。
