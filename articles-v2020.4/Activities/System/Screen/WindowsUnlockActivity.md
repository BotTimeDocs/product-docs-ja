# ロックを解除
システムのスクリーンのロックを解除して、システムのデスクトップに入ります。
> **説明:**
>
> このアクティビティを実行する前に、。[Windows画面ロック解除サービス](Studio/../../../../Studio/Extensions/WindowsUnlockService.md)拡張をインストールすることが必要です。

## プロパティ

### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。


### 入力
- **ユーザー名** ：システムにログインするのユーザー名またはマイクロソフトアカウント、変数を入力できます。
- **パスワード** ：システムにログインするパスワード（マイクロソフトアカウントはマイクロソフトアカウントのパスワードを入力する必要があります）、変数を入力できます。

## 操作サンプル
1. 一つ**ロックを解除**アクティビティをプロセス（**スクリーンをロック**アクティビティがあるプロセス）にドラッグ
2. **ロックを解除**アクティビティ引数を設定、下図のようになります。

    ![解锁组件示例](https://docimages.blob.core.chinacloudapi.cn/images/Activities/unlock20201216.png)

    - ユーザー名：ローカルコンピュータのアカウント名を入力します。
    - パスワード：ローカルコンピュータのパスワードを入力します。

3. プロセスを保存してエディタを終了
4. エディタを管理者として実行

    ![管理员运行编辑器](https://docimages.blob.core.chinacloudapi.cn/images/Activities/adminrun20201216.png)

5. エディタで"ツール > Windows画面ロック解除サービス"をクリックして、Windows画面ロック解除サービスをインストール

    ![Windows解锁服务](https://docimages.blob.core.chinacloudapi.cn/images/Activities/windowsunlockservice20201216.png)

6. 作成したプロジェクトのプロセスを開けて実行します。自動的にロックされたスクリーンを解除することが実現できます。画面が下図のようになります。

    ![运行效果](https://docimages.blob.core.chinacloudapi.cn/images/Activities/unlockresult20201216.gif)  