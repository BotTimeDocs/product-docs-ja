# テキストを数値に変換

テキストから数値への変換を実現します。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

### 入力

- **テキスト** ：数値に変換するテクスト、変数のみ入力できます。

### 出力

- **数値** ：変換された数値変数、変数のみ入力できます。

    > **説明：**
    >
    > このプロパティ変数の引数ータイプは、Int、Double、Float、Decimalのみをサポートします。

## 操作サンプル

1. **テキストを数値に変換**アクティビティをプロセスにドラッグ。
2. **テキストを数値に変換**アクティビティのプロパティを設定。

    ![配置プロパティ](https://docimages.blob.core.chinacloudapi.cn/images/Activities/texttonum20210104.png)

    - テキスト：数値に変換する文字列を入力します。`"123.56"`
    - 数値：数値に変換された変数を入力します。`S`

3. **テキストを数値に変換**アクティビティの下で、**ログに書き込み**アクティビティをドラッグ、数値に変換されたテキストの値を出力する。
4. ダブルクリック**ログに書き込み**アクティビティの空白部分で、プロパティを構成します。

    - ログレベル：ドロップダウンしてログレベルを選択。たとえば、`Info`
    - ログ内容：出力するログ内容を入力します。`"テキストから変換された数値は："+S`

5. プロセスを保存して実行します。
6. エディターの出力パネルで実行結果を表示します。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/texttonumresult20210104.png)