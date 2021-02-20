# FAQ

## インストールについて

1. **Q： インストール時にプログラムのクラッシュメッセージのポップアップが表示されます。以下の通り：**

    ![インストールクラッシュ](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/installCollapse.png)

    **A:** コントロールパネル->プログラム->プログラムをアンインストールを開き、アンインストールまたは変更プログラムリストで.Net Framework 4.6.1または以上のバージョンの.Net Frameworkの環境がインストールされているかを確認してください。インストールされていない場合は、まず.Net Framework 4.6.1をダウンロードしてインストールしてください。インストールが完了したら、コンピュータを再起動して、もう一回Encooエディタのインストールを行っていくだい。ダウンロード先:<https://www.microsoft.com/zh-CN/download/details.aspx?id=49982>

2. **Q: インストールをクリックしたらインストールに失敗しました**

    **A:** インストールディレクトリにおける現在のユーザの読み書き権限を確認し、もし現在のユーザがインストール先で読み書き権限がない場合は、管理者アカウントでログインして、インストールディレクトリで右ボタンをクリック、プロパティをクリック、セキュリティラベルをクリック、ターゲットアカウントを追加し、完全制御権限を追加し、最後に確定をクリックしてから管理者アカウントを終了し、ターゲットユーザでログインしてインストールします。

3. **Q: エディタのデフォルトのインストールディレクトリは何ですか？**

   **A：** `%UserProfile%\AppData\Local\Encoo Studio`

4. **Q: ロボットのデフォルトのインストールディレクトリは何ですか？**

   **A：** `%programfiles(x86)%\Encoo Robot`

## アンインストールについて

1. **Q: アンインストールに失敗しました**

    **A:** </br>
    (1) インストールディレクトリ(Program files x86)、25バージョン以降のインストールディレクトリは、ユーザーディレクトリのAppData\Local\にあり、下のencootechフォルダを削除</br>
    (2) C:\ProgramData\Package Cache\ でDigi4thを先頭としてのファイルを検索してすべてを削除</br>
    (3) windowsサービスDataBusServiceを削除（cmd コマンドラインは sc delete DataBusService）

## システムログについて

1. **Q: エディター・ロボットのシステムログのデフォルトパスは何ですか？**

   **A：** `%UserProfile%\AppData\Local\Encoo\Log`。

2. **Q: エディター・ロボットのインストールログのデフォルトパスは何ですか？**

   **A：** `%UserProfile%\AppData\Local\Encoo\Installation`。

## 市場について

1. **Q: 市場からダウンロードしたパッケージはローカルコンピュータのどのディレクトに保存されますか？**

   **A：** `%UserProfile%\.nuget\packages`

## 拡張について

1. **Q: Chromeの録画に失敗しました。自動化が失敗した理由は何ですか？**

    **A:** </br>
    (1) chromeブラウザの拡張機能を確認し、chromeプラグインをインストールして、図のように有効にしていますか？

    ![拡張を有効](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/chrome-usingExtension.png)</br>

    (2) chromeを開いたら、タスクマネージャに次のプロセスがあるかどうかを確認：EncooNativeMessageHost.exe このプロセスは、RPAとchromeブラウザの通信プロセスであり、存在しない場合は①を確認する。

    ![プロセスを確認](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/taskManager.png)</br>

1. **Q: どうやってchromeプラグインをインストールしますか？**

    **A:** エディタを開き、**スタート > ツール > 拡張**で、Chrome拡張機能をクリックして、指示に従って操作すればいいです。（インストール後、手動でブラウザを開き、拡張機能を有効にしてください：chrome://extensions/ で拡張機能を有効にします。)

    ![安装扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Market/extensioninpath20201019.png)
