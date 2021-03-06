# セルをマージ

指定されたセル範囲をマージします。このアクティビティは"Excelを開く/新規作成"アクティビティ内だけで使用できます。デフォルトでは"Excelを開く/新規作成"アクティビティのブックを取りますので、再入力する必要はありません。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。


### 入力

- **シート名** ：マージ操作を実行したいセルが属するシートの名前を指定します。
- **範囲** ：マージ操作を実行したいセル範囲を指定します。

### 出力

- **マージ値** ：セルをマージした後セルの値。マージされるセルの範囲に値が一つしかない場合は、デフォルトでこの一意の値が出力されます。
マージされるセルの範囲に複数の値がある場合は、最初の非空のセルの値が出力されます。

## 操作サンプル

1. Excelファイルを新規作成。以下の通りです。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeCells1.png)

2. **Excelを開く/新規作成** アクティビティをプロジェクトプロセスにドラッグ:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. ダブルクリックして開き、 **...** をクリック。ローカルエクセルドキュメントを選択:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. **セルをマージ** と **ログに書き込み** アクティビティを **Excelを開く/新規作成** アクティビティにドラッグ、sheet名に "sheet2"を記入し、範囲に "A1: A3"を記入し、Stringタイプの変数mergeを新たに作成し、マージ値に設定する。マージ値の設定をログに書き込むの内容に設定。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeCells2.png)

5. 実行をクリックして、実行後にExcelを開いて、セルをマージの結果を確認する。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeCells3.png)

6. マージ後のタイトルがプリントされます。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergeCells4.png)