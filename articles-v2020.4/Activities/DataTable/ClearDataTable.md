# データテーブルをクリア

データテーブルを空にします。既存のスキーマは保存されます。データだけをクリアします。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。


### 入力

- **データテーブル** ：クリア操作が行われるデータテーブル

## 操作サンプル

1. **データテーブルを構築** アクティビティをプロジェクトプロセスにドラッグ:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. ダブルクリックしてデータテーブルビルダーを開け、列情報と行値を編集し、データテーブルを格納するためのDataTableタイプの変数を作成。例：table、下の図のように。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable2020122402.png)

3. **データテーブルをクリア** アクティビティと **データテーブルをプレビュー** アクティビティをドラッグに、構築されたデータテーブル変数tableを記入。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/EmptyDataTable20201225.png)

4. 実行をクリックして、実行結果を確認し、プレビューのデータテーブルがクリアされたかどうかを確認。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/EmptyDataTable2020122502.png)

