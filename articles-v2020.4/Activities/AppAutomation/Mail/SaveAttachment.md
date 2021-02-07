# 添付ファイルを保存

メールの添付ファイルを指定の場所に保存します。

## プロパティ

### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

### 入力

- **メール** ：このメール変数の添付ファイルを取って、保存操作を行います。
- **フォルダーパス** ：添付ファイルの保存先。同じ名前のファイルがあるとエラーが発生します。相対パスと絶対パスをサポートします。パスが存在しないと自動的に新規作成します。文字列変数と文字列のみをサポートします。

## 操作サンプル

1. **メールを取得(Outlook)**アクティビティをプロジェクトプロセスにドラッグ:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail20201222.png)

2. メールにList<MailMessage>型の変数を入力、例：mail。メールフォルダを入力、例：“××@encootech.com”。下図のようになります。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail2020122202.png)

3. **添付ファイルを保存**と**ログに書き込み**アクティビティをドラッグイン、**添付ファイルを保存**のメールを入力、**メールを取得（Outlook）**の出力メールは Listであるので、ここに入力する変数のタイプはMailMessageである。 maillist 的の最初の要素を取得できます。例えば、mail [0]。フォルダパスを入力、例： "C：\\Encoo Technology"、**ログに書き込み**の内容を入力、最初に取得したメールの内容をプリント。例：mail [0].Body.ToString()。次の図のように：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail2020122203.png)

4. 実行をクリックして実行の結果を確認。取得した添付ファイルとログに書き込んだメールの内容が正しいかどうかを確認します。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetOutlookMail2020122204.png)