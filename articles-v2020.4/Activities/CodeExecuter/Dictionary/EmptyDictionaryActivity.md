# ディクショナリをクリア

変数パネルで作成されたディクショナリ（Dictionary <TKey,TValue>）の内容をクリアします。つまり、すべてのキーと値を削除します。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

### 入出力

- **ディクショナリ** ：変数パネルで定義されたディクショナリオブジェクト、変数のみ入力できます。

## 操作サンプル

1. 1つ**ディクショナリを初期化**アクティビティをプロセスにドラッグ。具体的なプロパティ構成は[ディクショナリを初期化](CodeExecuter/../InitializeDictionaryActivity.md)を参照してください。
2. 1つ**キーと値のペアを追加** アクティビティをプロセスにドラッグ
3. **キーと値のペアを追加** アクティビティのプロパティを設定

    - ディクショナリ：変数パネルで定義された辞書変数を入力します。例えば、`D`
    - キー/値：ディクショナリ変数に追加するキーと値のペアを入力します。例えば、`key3`、`value3`

4. **キーと値のペアを追加**アクティビティの下に、**ディクショナリをクリア**アクティビティをドラッグ。
5. **ディクショナリをクリア**アクティビティのプロパティを設定。

    - ディクショナリ：クリアするディクショナリ変数を入力します。たとえば、`D`

6. 完全なプロセスチャートは次のとおりです。

    ![完整流程](https://docimages.blob.core.chinacloudapi.cn/images/Activities/emptydictionary20210112.png)

7. プロセスを保存して実行します。