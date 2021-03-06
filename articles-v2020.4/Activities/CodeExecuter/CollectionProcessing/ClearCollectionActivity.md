# コレクションをクリア

指定されたコレクションをクリアします。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

### 入力

- **コレクション** ：クリアしたいターゲットコレクションを指定します。

### 出力

- **コレクション** ：クリアされたコレクションを出力します。

## 操作サンプル
1. **コレクションを初期化**アクティビティをドラッグ、変数`コレクションList`を作成、変数の種類は`List<String>`で、以下の図のように：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/InitializeCollectionActivity1.png)
2. **コレクションに追加**アクティビティをドラッグ、**入力**を追加するオブジェクト`"A1"`に設定。**入力/出力**を`コレクションList`に設定。以下の図のように：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AddToCollectionActivity1.png)
3. **コレクションの長さを取得**アクティビティをドラッグ、変数`コレクションcount`を作成、**入力**を変数`コレクションList`に設定。**出力**を長さ変数`コレクションcount`に設定。
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfCollectionActivity1.png)
4. **ログに書き込み**アクティビティをドラッグ、`コレクションList`の長さをプリント。**ログの内容**を`コレクションcount.ToString()`に設定。プリント結果は`1`となります。以下の図のように：
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/GetLengthOfCollectionActivity2.png)
5. **コレクションをクリア**アクティビティをドラッグ、入力を`コレクションList`に設定。
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ClearCollectionActivity1.png)
6. コレクションをクリアしてからもう一度**コレクションの長さを取得**して、そして**ログに書き込み**。プリント結果は0で、下図のようになります。
   ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ClearCollectionActivity2.png)

