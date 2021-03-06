# 証明書を識別
デフォルトでは現在のユーザのログイン権限を使用し、証明書の情報を識別します。

> **説明:**
>
> ユーザーが該当サービスアカウントを設定していない場合、ユーザは当日無料サービス回数のみ利用できます。このサービスを引き続き利用するにはEncoo[AI HUB](https://aihub.encoo.com/serviceAccount) に行って、使用クォータを設定する必要があります。


## プロパティ
### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。
### 入力
- **引数** ：アクティビティの【引数設定】ボタンをクリックして、下記の引数を設定できます。
  - サービス：識別できるの証明書の種類。今は身分証明書、実行証、営業許可証、銀行カード、車のナンバーをサポートしています。
  - プラットフォーム：サードパーティAIプラットフォーム。今alibabacloud、Tencent AI、Baidu AI、訊飛AI、huawei cloudをサポートしています。
  - 画像ファイル：識別したい画像のパスを指定し、変数をサポートします。一般的なjpg、jpeg、pngピクチャフォーマットを使用することを推奨します。
### 出力
- **識別結果** ：識別後のオリジンデータ（JSON）を出力し、変数のみをサポートします。

## 操作サンプル

1. **証明書を識別**アクティビティをプロジェクトプロセスにドラッグし、変数result（String）を設定する。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/IdentificationOfCredentials_1.png)

2. ダブルクリックして証明書を識別を開き、画像を選択する。例:"D:\\テスト画像.jpg"のように画像パスを入力し、必要なタイプと対応するプラットフォームを選択し、出力に変数resultを追加。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/IdentificationOfCredentials_2.png)

3. 実行をクリックして、実行結果を確認する。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/IdentificationOfCredentials_3.png)


   > **説明:**
   >
   > コンソールアカウントを使ってエディタにログインする必要があります。（プライベートエンタープライズ版はまだサポートしていません。）試用回数を超えたら、Encoo[AI HUB](https://aihub.encoo.com/serviceAccount)に行って設定してください。下図のように。

   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/IdentificationOfCredentials_4.png)

