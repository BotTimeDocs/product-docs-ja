# パスワードを設定

敏感な情報に対して保護入力を行って、安全に保存と出力します。このアクティビティを使用する場合は、編集と実行は同じマシンで同じユーザ（ロボットを含む）である必要があります。プロセスファイルが異なるマシンやユーザの下で実行される場合は、アクティビティ"パスワードを設定"の入力を再編集する必要があります。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。


### 入力

- **パスワードを設定** ：敏感情報。文字列変数と文字列のみをサポートします。

### 出力

- **変数に代入** ：この変数に敏感な情報を格納します。文字列変数と文字列のみをサポートします。

## 操作サンプル
1. **パスワードを設定**アクティビティをデザインパネルにドラッグ:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setPassword-1.png)

2. ダブルクリックしてアクティビティの内に入り、プロパティの引数を設定。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setPassword-2.png)

3. **ログに書き込み**アクティビティをドラッグ、ユーザが設定したパスワードを出力する。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setPassword-3.png)

4. プロセスを実行、コンソールの出力を確認。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/setPassword-4.png)