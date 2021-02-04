# データベースに接続

指定されたデータベースに接続します。*構成ウィザード*をクリックすれば接続テストができます。アクティビティの実行が完了したら、自動的に接続が切断されます。すべてのデータベース関連の操作がこのアクティビティに配置される必要があり、接続の再構成は不要です。

> DB2データベースに接続する必要があれば、 *Microsoft Visual C++ 2005 RunTime Pack* がインストールされていることを確認してください。インストールされていない場合、 [RunTimePack.zip](https://docimages.blob.core.chinacloudapi.cn/images/Studio/DataBase/RuntimePack.zip)でダウンロードしてインストールできます。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。


### 入力

- **ConctionString** ：データベースとの接続を確立するために使用します。文字列変数と文字列のみをサポートします。例えば、MySQLの接続文字列は"Server=サーバアドレス;Database=DB名;Port=ポート番号;Uid=uid;Pwd=password"
- **ProviderName** ：接続するデータベースの種類。現在は5種類をサポートします。SQL Server, MySql, Oracle, DB2, Teradata


## 操作サンプル
1. **データベースに接続**アクティビティをドラッグ、アクセスするデータベースの種類を選択して、データベース接続文字列を構成する。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db1.png)

2. **データベースに接続**アクティビティダブルクリック、"構成ウィザード"ボタンをクリックして、データベース文字列情報が設定済み、ターゲットデータベースの種類も選択済みの場合は、"接続をテスト"ボタンをクリックして、テスト成功の場合は緑色のチェックが表示され、逆に失敗。失敗の場合は、データベース接続文字列の内容を更新して、接続を再テストする。"確認"をクリックして設定画面を終了します。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db2.png)

3. **クエリ**アクティビティをドラッグ、sqlクエリ文を設定し、変数に出力。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db3.png)
4. **データテーブルをプレビュー**アクティビティをドラッグ、入力変数にクエリアクティビティで定義された出力変数を記入。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db4.png)
5. プロセス実行をクリック、結果を確認。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db5.png)
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db6.png)
