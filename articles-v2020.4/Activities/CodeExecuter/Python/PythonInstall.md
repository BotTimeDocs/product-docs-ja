# Pythonをインストール
ローカルにダウンロードしたPythonインストールファイルを選択して、指定されたディレクトリにインストールします。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。

### オプション

- **ディレクトリにインストール** ：Pythonのインストールディレクトリを入力して、変数を入力できます。

  > **説明:**
  >
  > 入力しない場合は、デフォルトのインストールパスを使用します。C:\Users\{user}\AppData\Local\Programs。


### 入力

- **インストールファイルパス** ：Pythonインストールパッケージがあるパス、変数を入力できます。

  > **説明:**
  >
  > ファイルタイプは".exe"と".msi"をサポートします。

## 操作サンプル
1. [Python公式サイト](https://www.python.org/downloads/)からpythonのインストールパッケージをダウンロードして、ローカルコンピュータに保存する
2. **Pythonをインストール**アクティビティをプロセスにドラッグ。
3. このアクティビティをダブルクリックして開き、ダウンロードしたPythonインストールパッケージを選択
4. インストールパスに対応するプロパティを設定

   ![配置安装路径](https://docimages.blob.core.chinacloudapi.cn/images/Activities/installpython20201216.png)

5. プロセスを保存して実行
6. コマンドラインに`python`を入力、バージョン番号情報が表示されたら、インストールに成功した
   ![验证Python是否安装成功](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pythonsucess20201216.png)