# ディレイ

次のアクティビティが実行される前に待ち時間を追加します。指定時間が過ぎたら、このアクティビティ後のプロセスを実行開始します。

## プロパティ
### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

### 入力
- **待ち時間** ：待ち時間を設定、書式：時:分:秒

## 操作サンプル
1. **ブラウザを開く**アクティビティをドラッグ、URLを入力。"https://www.baidu.com":
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/delay-1.png)

2. **ディレイ**アクティビティをドラッグ、ディレイを設定。**テキストを入力**アクティビティをドラッグ、入力ボックス要素を指定し、入力テキストを設定。例えば、"Encoo技術"：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/delay-2.png)

3. プロセスを実行、ディレイ効果を確認。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/delay-3.png)