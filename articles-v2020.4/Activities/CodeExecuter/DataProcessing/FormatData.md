# データを書式化

DateTime、Intなどのタイプのデータの入力をサポートし、実際のビジネスの必要に相応しいデータフォーマット（数値、パーセンテージ、通貨、日付時間）に変換します。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。
- **タイムアウト(ミリ秒)** ：このアクティビティの実行時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。マッチングタイムアウト(ミリ秒)が含まれます。この時間を超えたら、アクティビティがまだ実行されていない場合、エラーがスローされます。


### 入力

- **データ** ：書式化される元データ。Int、Int32、Int64、Float、Double、DateTimeなどのデータタイプをサポートします。

### 出力

- **書式化されたデータ** ：書式化した後に戻った値をこの変数に格納します。Stringデータタイプをサポートします。

## 操作サンプル

1. **データを書式化**アクティビティをドラッグ、**String**型の変数を作成、**入力**に小数点を含む複数の位数の数を入力。
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FormatData1.png)

2. **データを書式化**アクティビティをダブルクリックして開く、**データ形式を設定**をクリック、形式の種類を**数値**に設定。小数点以下は何桁残すを記入。**サウザンドスプリット**は非必要である。
	![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FormatData2.png)

3. **ログに書き込み**アクティビティをドラッグ、**データを書式化**後の変数をプリントして確認:
	![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FormatData3.png)

4. 実行をクリックすると、**データを書式化**処理後の変数の結果が表示される。ステップ2で設定した2桁の小数しか保持していません。
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FormatData4.png)

5. 他のフォーマットのタイプを選択して、もう一度プロセスを**実行**、出力結果は対応するフォーマットになります。
	![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FormatData5.png)
	![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/FormatData6.png)