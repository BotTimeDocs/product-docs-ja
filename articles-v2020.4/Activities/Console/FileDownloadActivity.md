# ファイルをダウンロード

EncooRPAコンソール"データセンター > ファイルサービス"でアップロードされたファイルをダウンロードします。
> **説明:**
> - このアクティビティは**エンタープライズ版**のみが利用可能です。
> - 現在は単一ファイルのダウンロードのみに対応しています。

## プロパティ
### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

### オプション
- **ディレクトリに保存** ：ダウンロードされたファイルはディレクトリパスに保存され、変数を入力できます。

  >**説明:**
  >- 指定されたディレクトリが存在しない場合は、指定されたディレクトリで新規作成します。
  >- この項目を入力しないと、デフォルトはwindowsのダウンロードディレクトリです。

- **タイムアウト** ：タイムアウト時間（時分秒）。デフォルトではタイムアウト時間を制限しません：00:00:00。変数を入力できます。

- **ファイルを上書き** ：ダウンロードされたファイルがフォルダに保存される場合、同名のファイルがある場合は、既存のファイルを上書きしますか。チェックすると、上書きします。そうでないと、上書きしません。上書きしない時は、元のファイル名に現在のタイムスタンプを追加します。例えば、元のファイル名-YYYYMMDDhhmmss。

### 入力

- **ファイルパス** ：コンソールファイルサービスにおけるファイルパスを入力または選択し、変数を入力できます。

### 出力

- **ローカルファイルパス** ：ローカルにダウンロードした後の絶対パスを出力します。


## 操作サンプル

1. **ファイルをダウンロード**アクティビティをプロセスにドラッグ。
2. アクティビティをダブルクリックして開き、ダウンロードするファイルを選択

    ![选择控制台文件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/downloadfile20201216.png)

3. プロパティの引数を設定

    ![保存至目录](https://docimages.blob.core.chinacloudapi.cn/images/Activities/savepath20201216.png)   

4. プロセスを保存して実行
5. リソースマネージャで設定されたダウンロードパスに従って、ダウンロードされたファイルを確認

   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/readfile20201216.png)