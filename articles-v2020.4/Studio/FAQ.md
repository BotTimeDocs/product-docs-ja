1. **Q：** インストール時にプログラムのクラッシュメッセージのポップアップが表示されます。以下の通り：

    ![インストールクラッシュ](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/installCollapse.png)

    **A:** コントロールパネル->プログラム->プログラムをアンインストールを開き、アンインストールまたは変更プログラムリストで.Net Framework 4.6.1または以上のバージョンの.Net Frameworkの環境がインストールされているかを確認してください。インストールされていない場合は、まず.Net Framework 4.6.1をダウンロードしてインストールしてください。インストールが完了したら、コンピュータを再起動して、もう一回Encooエディタのインストールを行っていくだい。ダウンロード先:<https://www.microsoft.com/zh-CN/download/details.aspx?id=49982>

2. **Q:** インストールをクリックしたらインストールに失敗しました。

    **A:** インストールディレクトリにおける現在のユーザの読み書き権限を確認し、もし現在のユーザがインストール先で読み書き権限がない場合は、管理者アカウントでログインして、インストールディレクトリで右ボタンをクリック、プロパティをクリック、セキュリティラベルをクリック、ターゲットアカウントを追加し、完全制御権限を追加し、最後に確定をクリックしてから管理者アカウントを終了し、ターゲットユーザでログインしてインストールします。

3. **Q:** アンインストールに失敗しました。

    **A:** ① インストールディレクトリ(Program files x86)、25バージョン以降のインストールディレクトリは、ユーザーディレクトリのAppData\Local\にあり、下のencootechフォルダを削除</br>
    ② C:\ProgramData\Package Cache\ でDigi4thを先頭としてのファイルを検索してすべてを削除</br>
    ③ windowsサービスDataBusServiceを削除（cmd コマンドラインは sc delete DataBusService）

4. **Q:** エディタのデフォルトのインストールディレクトリは何ですか？

   **A：** %USERNAME%\AppData\Local\Encootech\Encoo Studio

5. **Q:** ロボットのデフォルトのインストールディレクトリは何ですか？

   **A：** %programfiles(x86)%\Encootech\Encoo Robot

6. **Q:** デフォルトのログパスは何ですか？

   **A：** %username%\AppData\Local\Encoo\Log（Installationはインストールログ）

7. **Q:** 市場からダウンロードしたパッケージはローカルコンピュータのどのディレクトに保存されますか？

   **A：** %username%\\.botTimeRPA\packages\Activity

8. **Q:** どうすれば外部ネットワークがアクセスできないコンピュータでアクティビティ市場のアクティビティを使用できますか？

    **A:** ダウンロードされたローカルパッケージのパスを開きます。C:\Users\\%USERNAME%\\.botTimeRPA\packages\Activity

    ![ローカルダウンロードパッケージパス](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/localActivitiesPosition.png)

    ① 必要なパッケージフォルダをコピー</br>
    ② コピーしたフォルダをターゲットコンピュータの同じパスに置く、パスがない場合は手動で作成できます。</br>
    ③ NotePad++または他のテキストエディタでターゲットプロジェクトフォルダの下のbotTimeRPA.jsonファイルを開く</br>
    ④ botTimeRPA.jsonファイル内でDependenciesプロパティを修正して依存を追加し、DataTableToolsツールパッケージを例にして：(ローカルプロジェクトのこのプロパティをターゲットプロジェクトファイルに直接コピーできます。)

    ![依存を追加](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/addDependence.png)

    ⑤ 最終的にエディタを再起動または開くと、プロジェクトを開くと自動的に市場パッケージを参照することができます。

9. **Q:** Chromeの録画に失敗しました。自動化が失敗した理由は何ですか？

    **A:** ① chromeブラウザの拡張機能を確認し、chromeプラグインをインストールして、図のように有効にしていますか？

    ![拡張を有効](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/chrome-usingExtension.png)

    ② chromeを開いたら、タスクマネージャに次のプロセスがあるかどうかを確認：EncooNativeMessageHost.exe このプロセスは、RPAとchromeブラウザの通信プロセスであり、存在しない場合は①を確認する。

    ![プロセスを確認](https://docimages.blob.core.chinacloudapi.cn/images/Studio/FAQ/taskManager.png)


10. **Q:** どうやってchromeプラグインをインストールしますか？

    **A:** エディタを開き、ウィンドウのツールバーで"拡張"をクリックし、Chrome拡張機能をクリックして、指示に従って操作すればいいです。（インストール後、手動でブラウザを開き、拡張機能を有効にしてください。：chrome://extensions/ で拡張機能を有効にします。

    ![拡張をインストール](https://docimages.blob.core.chinacloudapi.cn/images/Studio/userInterface/toolbar-extension.PNG)
