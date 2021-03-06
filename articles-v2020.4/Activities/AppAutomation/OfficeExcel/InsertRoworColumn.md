# 行/列を挿入

指定されたシートに任意の行または列を挿入します。このアクティビティは"Excelを開く/新規作成"アクティビティ内だけで使用できます。デフォルトでは"Excelを開く/新規作成"アクティビティのブックを取りますので、再入力する必要はありません。

## プロパティ

### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。


### 入力

- **シート名** ：行または列を挿入するシートの名前を指定します。
- **挿入モード** ：挿入行/列を選択します。
- **挿入行/列の数** ：行/列を挿入したい数。値は整数です。
- **開始位置** ：行/列を挿入したいの開始位置。

## 操作サンプル
1. Excelファイルを新規作成。以下の通りです。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InsertRowOrColumn1.png)

2. **Excelを開く/新規作成**アクティビティをプロジェクトプロセスにドラッグ:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel1.png)

3. ダブルクリックして開き、 **...** をクリック。ローカルエクセルドキュメントを選択:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)

4. **行/列を挿入**アクティビティを**Excelを開く/新規作成**アクティビティにドラッグ、挿入行/列数を入力し、挿入モードで"挿入行"を選択し、シート名と開始位置を記入する。列を挿入する操作は、挿入行と同じです。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InsertRowOrColumn2.png)

5. 実行が成功したら、エクセルを開いて、sheet1の3行目に空白行2行が挿入されました。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InsertRowOrColumn3.png)
