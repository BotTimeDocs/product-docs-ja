# ファイルをマージ

複数のPDFファイルを一つのPDFファイルにマージすることができます。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。


### 入力

- **元のPDFファイルのパス** ：マージしたいファイルパスのリストを入力します。"..."をクリックして、ファイルを選択してから自動的にファイルリストの配列を作成できます。IEnumerableタイプの変数およびオブジェクトを入力できます。例えば、配列またはセット。
- **新しいPDFファイルパス** ：この列をソートします。列のインデックス（例：1，つまり第一列をソート）を入力します。文字列変数と文字列のみをサポートします。

### オプション

- **ファイルを上書き** ：新しいファイルがあるディレクトリ下の同名ファイルを置換するかどうかを指定します。

## 操作サンプル

1. **ファイルをマージ**アクティビティをプロジェクトプロセスにドラッグ:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergePDF_1.png)

2. ダブルクリックして"ファイルをマージ"を開き、pdfを選択。例えば、"D:\\didi領収書 (1).pdf"、"D:\\didi領収書.pdf"。以下の図のように：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergePDF_2.png)

3. 新しいファイル""D:\\didi領収書 (2).pdf"が作成される。実行をクリックして、実行結果を表示します。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/MergePDF_3.png)