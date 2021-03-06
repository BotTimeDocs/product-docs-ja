# メールを取得（IMAP）

IMAPサービスを使用してメールを取得します。プロキシを使用することもできます。

## プロパティ

### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

### サーバー

- **サーバー** ：メールが取得されるターゲットメールボックスが属するサーバーのアドレス。文字列変数と文字列のみをサポートします。
- **ポート** ：メールが取得されるターゲットメールボックスのポート番号。整数変数と整数型のみをサポートします。
- **プロキシ** ：メールを取得する時にプロキシを使用したい場合、このプロパティを入力します。フォーマットは【サーバ：ポート】です。文字列変数と文字列のみをサポートします。

### メール

- **メールアドレス** ：このメールアドレスのメールを取得します。文字列変数と文字列のみをサポートします。
- **パスワード** ：メールが取得されるターゲットメールボックスのパスワード。文字列変数と文字列のみをサポートします。
- **メールフォルダ** ：メールを取得するフォルダを指定します。受信箱のメールを取得するには英語の"inbox"を記入する必要があります。inboxのサブフォルダのメールを取得するには、"/"で区切りする必要があります。例えば、"inbox/顧客メール"
- **取得するメールの数** ：取得するメールの数。デフォルトは1です。

### オプション

- **セキュア接続** ：暗号化を検出する方法を指定して、デフォルトは自動です。オプションは次があります：なし、自動、SSL、STARTTLS、STARTTLSが利用可能な場合は利用される。
- **未読メールだけを取得** ：デフォルトではすべての種類のメールを取得します。チェックしたら未読メールのみを取得します。

### 出力

- **メール** ：取得したメールをこの変数に格納します。

## 操作サンプル

1. **メールを取得（IMAP）**アクティビティをプロジェクトプロセスにドラッグ:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetMailIMAP20201223.png)

2. サーバー文字列とポート番号を入力。例:"×××.outlook.cn"と993。メールにList<MailMessage>型の変数を入力、例：mail。メールアドレス、メールフォルダとパスワードを入力、例：“××@encootech.com”、“受信箱”と“×××password”。下図のようになります。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetMailIMAP2020122302.png)

3. **ログに書き込み**アクティビティをドラッグ、**ログに書き込み**のログ内容を入力、取得した最初のメールの内容をプリント。例：mail[0].Body.ToString()、次の図のように：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetMailIMAP2020122303.png)

4. 実行をクリックして、実行結果を確認し、ログに書き込だメールの内容が正しいかどうかを確認します。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetMailIMAP2020122304.png)
