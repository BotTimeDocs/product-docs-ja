# テキストを追加

指定したテキストを元のテキストの最後に追加します。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

### オプション

- **改行追加** ：改行が必要かどうか。チェック後、元のテキストが改行後に新しいテキストを追加します。それ以外の場合は改行なしで追加します。

### 出力

- **結果を追加** ：追加の結果、変数のみ入力できます。

### 入る

- **ソーステキスト** ：元のテキストコンテンツを入力、変数のみ入力できます。
- **テキストを追加** ：追加したいテキスト内容を入力、変数のみ入力できます。

## 操作サンプル

1. **テキストを追加**アクティビティをプロセスにドラッグ。
2. **テキストを追加**アクティビティの空白部分でダブルクリック、そのプロパティを設定。

    ![追加文本](https://docimages.blob.core.chinacloudapi.cn/images/Activities/appendtext20210111.jpg)

    - ソーステキスト：元のテキストコンテンツを入力します。`"Hello"`
    - テキストの追加：追加するテキストコンテンツを入力します。たとえば、`" World!"`
    - 追加結果： String タイプの変数を定義して、追加結果を格納します。例えば、S

3. **テキストを追加**アクティビティの下に、**ログに書き込み**アクティビティをドラッグ。
4. **ログに書き込み**アクティビティをダブルクリック、そのプロパティを構成。

    - ログレベル：ドロップダウンしてログレベルを選択します。例えば、`Info`。
    - ログの内容：ログを入力します。たとえば、`"追加した结果:"+S`。

5. プロセスを保存して実行する
6. 実行結果が出力パネルに表示されます。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/appendtextresult20210111.png)