# メールトリガー（IMAP）

メールトリガー（IMAP）は、IMAPプロトコルをサポートするメールボックスが新しいメールを受信するイベント監視し、特定のトリガ条件を設定し、条件を満たすと自動的にプロセスを実行します。

## プロパティ

###　基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

###　サーバー

- **サーバー** ：監視されるサーバーのアドレスを入力します。文字列変数と文字列のみをサポートします。
- **ポート番号** ：監視されるポート番号を入力します。整数変数と文字列のみをサポートします。

###　メール

- **メールアドレス** ：監視されるメールアドレスを入力します。文字列変数と文字列のみをサポートします。
- **パスワード** ：監視されるメールに対応するパスワードを入力します。文字列変数と文字列のみをサポートします。

###　オプション

- **セキュア接続** ：検出する暗号化方法を指定します。デフォルトは自動です。オプションは次を含む、なし、自動、SSL、STARTTLS、STARTTLSが利用可能な場合は利用される
- **送信者** ：監視するメール中の送信者のメールアドレスを入力します。複数をサポートし、複数の場合はセミコロンで区切ります。新着メールの中に設定した送信者の一人が含まれている場合はトリガ条件を満たしていると見なします。変数をサポートします。
- **添付ファイル** ：添付ファイルがある新着メールを監視するかどうかを選択します。
- **フォルダ** ：監視されるメールフォルダを入力します。空の場合は受信箱全体を監視します。変数をサポートします。

  > **説明：**
  > 
  > 例：サブフォルダーを監視したい場合は、“受信箱\フォルダー名”を入力する必要があります。もし“受信箱”だけを入力すると、サブフォルダーのメールを監視できません。

- **件名キーワード** ：新着メールに含まれる件名キーワードを入力します。複数をサポートし、複数の場合はセミコロンで区切ります。新着メールの中に設定した件名キーワードの一つが含まれている場合はトリガ条件を満たしていると見なします。変数をサポートします。
- **タイムアウト** ：タイムアウト時間を入力します。フォーマット：時:分:秒
  
###　出力

- **新着メール** ：監視された新着メールを出力します。System.Net.Mail.MailMessage変数のみをサポートします。

## 操作サンプル
1. Outlookのメールボックスでを例にする。**メールトリガー（IMAP）**をドラッグ。変数`newmail`を作成、変数の種類を`MailMessage`に設定。サーバのアドレスに`"imap-mail.outlook.com"`**入力**、ポートを`993`に設定。メールアドレスとパスワードを**入力**、**出力**の新着メールを`newmail`に設定。
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/IMAPTrigger1.png)
2. **ログに書き込み**アクティビティをドラッグ、メールの内容をプリント。**ログの内容**に`newmail.Body`を入力、プログラムを実行し、実行中にこのメールボックスにメールを送信し、Outlookサーバがメールを受信した後、トリガー（IMAP）が新着メールを検出し、プリント結果を確認し、この新着メールの内容をプリントします。以下の図のように：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/IMAPTrigger2.png)
