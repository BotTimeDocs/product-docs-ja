# キーと値のペアを追加

初期化されたディクショナリ変数にキーと値のペアを追加します。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

### 入出力

- **ディクショナリ**：変数パネルで定義されたディクショナリオブジェクト、変数のみ入力できます。
- **キー/値**：ディクショナリに追加するパラメーター key とパラメーター Value の値、変数を入力できます。

## 操作サンプル

1. 1つ**ディクショナリを初期化**アクティビティをプロセスにドラッグ。具体的なプロパティ構成は[ディクショナリを初期化](CodeExecuter/../InitializeDictionaryActivity.md)を参照してください。
2. 1つ**キーと値のペアを追加** アクティビティをプロセスにドラッグ
3. **キーと値のペアを追加** アクティビティのプロパティを設定

    - ディクショナリ：変数パネルで定義された辞書変数を入力します。例えば、`D`
    - キー/値：ディクショナリ変数に追加するキーと値のペアを入力します。例えば、`key3`、`value3`

4. **ログを書き込む**アクティビティを**キーと値のペアを追加**アクティビティの下にドラッグ、追加されたキーと値のペアを出力するために使用されます。
5. **ログを書き込む**アクティビティの属性を設定。

    - ログレベル：ログレベルを入力します。例えば、`Info`
    - ログの内容：ログの内容を入力します。`D["key3"]`、これは、key3キーに対応する値を出力することを意味します。

6. 最終的なプロセスは次の図に示します。

    ![流程图](https://docimages.blob.core.chinacloudapi.cn/images/Activities/addkeyvalue20210111.png)

7. プロセスを保存して実行する。
8. 実行結果が出力パネルに表示されます。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/addkeyvalueresult20210111.png)