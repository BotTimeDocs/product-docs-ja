# クリップボードからテキストを取得

クリップボードのテキストの内容を取得し、Stringタイプで出力します。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。


### 出力

- **出力** ：Stringタイプのクリップボードのテキストの内容を出力します。

## 操作サンプル
1. **クリップボードからテキストを取得**アクティビティをデザインパネルにドラッグ:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-1.png)

2. ダブルクリックしてアクティビティ内に入り、出力テキストボックスに変数"copy_text"を記入。テキストボックスがStringタイプのクリップボードのテキストの内容を出力。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-2.png)

3. **ログに書き込み**アクティビティをデザインパネルにドラッグ:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-3.png)

4. ウェブページを開いて、ある内容をクリップボードにコピー。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-4.png)

5. プロセスを実行、コンソールに取得したクリップボードのテキスト内容が出力される。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getClipboard-5.png)
