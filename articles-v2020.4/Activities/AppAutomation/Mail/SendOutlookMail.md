# メールを送信（Outlook）

ローカルのOutlookで設定されているメールアカウントを使用してメールを送信します。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。


### 送信者

- **共有メールアドレス** ：Outlookの共有メールアドレスを送信者としてメールを送信します。文字列変数と文字列のみをサポートします。
- **メールアドレス** ：送信者のメールアドレス。文字列変数と文字列のみがサポートされています。注意："共有メールアドレス"が有効で、現在のプロパティに入力されているメールアドレスが"共有メールアドレス"の権限がある場合、送信メールの"送信者情報"に共有メールの情報が表示されます。

### 受信者

- **受信者** ：メール受信者のメールアドレス。複数の受信者を入力でき、"; "で区切りすればいいです。例えば【[user1@encootech.com; user2@encootech.com](mailto:user1@encootech.com;%20user2@encootech.com)】。文字列変数と文字列のみをサポートします。
- **Cc** ：メール送信時のCcのメールアドレス。複数の受信者を入力でき、"; "で区切りすればいいです。例えば【[user1@encootech.com; user2@encootech.com](mailto:user1@encootech.com;%20user2@encootech.com)】。文字列変数と文字列のみをサポートします。
- **Bcc** ：メール送信時のBccのメールアドレス。複数の受信者を入力でき、"; "で区切りすればいいです。例えば【[user1@encootech.com; user2@encootech.com](mailto:user1@encootech.com;%20user2@encootech.com)】。文字列変数と文字列のみをサポートします。

### メール

- **メールの件名** ：送信するメールの件名。文字列変数と文字列のみをサポートします。
- **メール本文** ：送信するメールの本文。文字列変数と文字列のみをサポートします。
- **添付ファイル** ：送信するメールの添付ファイル。相対パスと絶対パスをサポートします。複数の添付ファイルを入力できます。具体的な書き方は次を参照できます：new List<string>(){"ファイル1のパス","ファイル2のパス"}、"..."をクリックして、ファイルを選択して自動作成することもできます。
- **下書きとして保存** ：編集したメールを送信者の下書きボックスに保存し、送信操作を実行しません。
- **HTML形式** ：メール内容がHTML形式であるかどうかを示します。チェックしたらHTML形式でメール内容を処理します。

### メール### 転送

- **メール** ：転送するメールを入力します。outlookで選択したメールに対して"転送"をクリックと同じ効果です。System.Net.Mail.MailMessageタイプのみがサポートされています。

## よくある質問

1. "あるプログラムがOutlookでユーザーに代わってメールを送信しようとしています"の警告が表示されます。<br>
   ![发送邮件outlook](https://docimages.blob.core.chinacloudapi.cn/images/Activities/sendoutlookmail20201204.png)<br>
   ソリューション：[公式回答](https://docs.microsoft.com/zh-cn/outlook/troubleshoot/security/a-program-is-trying-to-send-an-email-message-on-your-behalf)を参照してください。

## 操作サンプル

1. **メールを送信（Outlook）**アクティビティをプロジェクトプロセスにドラッグ:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SendOutlookMail2020122201.png)

2. 送信者メールアドレス文字列を入力、例：“××@encootech.com”。受信者の文字列を入力、例：“×× 2@encootech.com”、添付ファイルを選択ボタンをクリック、添付するファイルを選択、例：new List <string>{"C:\\Desktop\\領収書.png"}。メールの内容文字列を入力、例：“Encoo：メールを送信（Outlook）”。メールの件名文字列を入力、例：“メールを送信（Outlook）”。下図のようになります。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SendOutlookMail2020122202.png)

3. 実行をクリックして、実行結果を確認して、メールの送信が成功したかどうかを確認します。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/SendOutlookMail2020122203.png)