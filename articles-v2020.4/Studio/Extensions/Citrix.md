# Citrix 拡張（エンタープライズ版）

## Citrix TechnologyAutomationについて

Citrixは、CitrixDesktopとCitrixAppの2つの仮想リソース配信方法を指します。

Encoo RPAは、自動化機能を改善するためにCitrixをサポートしています。ローカルクライアントで Encoo Citrix 拡張をインストール、リモートサーバー（Citrix Desktop またはCitrix Apps）で Encoo Remote Runtime をインストールすれば、ユーザーがローカルクライアントを使用するようにCitrixリモートサーバーのインターフェイス要素（"クリック"、"テキストを入力"、"テキストを取得"などインストール自動化操作）を操作できます。これにより、画像認識などの自動化テクノロジを使用せずに、 Citrix Desktop または Citrix Appでネイティブ自動化と同じエクスペリエンスを得ることができます。

**サポートされている機能**は次のようになります。
Encoo Citrix 拡張機能と Encoo Remote Runtime をインストールした後、次の操作を実行できます。

- CitrixAppsとDesktop中のユーザーインターフェイス要素にセレクターを生成します。
- UiAutomationアクティビティを使用できます。
- CitrixAppsで開いたブラウザーにたいして自動化を実行します。

## インストールと構成の手順

### 前提条件

Citrixクライアントをローカルコンピューターにインストールします（つまり、[Citrix Receiver](https://www.citrix.com/downloads/citrix-receiver/) または [Citrix Workspace](https://www.citrix.com/downloads/workspace-app/)）。

### ローカルクライアントを構成する

Encoo Studio / RobotがCitrix関連のアプリケーションをネイティブに自動化できるように、Citrix拡張機能をローカルコンピューターにインストールします。

1. エディターで "**スタート>ツール**ページで、ローカル Encoo Citrix 拡張を入手する。
2. **Citrix 拡張**をクリック、インストールウィザードに従ってインストール。
![安装 Citrix 扩展](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/citrixpath20210107.png)

### リモートサーバーを構成する

Encoo Remote Runtimeは、Citrixサーバー上で実行されるアクティビティであり、CitrixリモートデスクトップまたはリモートアプリケーションがCitrixローカル拡張機能と通信できるようにして、セレクターをローカルで生成し、自動操作を実行できます。

1. コンソールでの "**ホーム > インストールパッケージのダウンロード**"でリモートサーバーの Encoo Remote Runtime インストールパッケージを入手する。
2. 自動化するCitrixアプリケーションサーバーにEncoo Remote Runtimeインストールパッケージをインストール
3. (オプション)リモートマシンでブラウザやJavaアプリケーションを自動化する必要がある場合は、より良い自動化サポートを得るためにサーバに対応する拡張機能をインストールする必要があります。

    - **Web拡張インストール**

      a.Remote Runtimeインストールディレクトリ下のWeb拡張インストールプログラムを見つける(Encoo.Web.ExtensionInstall.exe)、パスは"C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Web\Encoo.Web.ExtensionInstall.exe"
      b.コマンドラインを開いて、次のコマンドを実行：` cd C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Web\`　インストールプログラムがあるディレクトリに切り替える。
      c.必要に応じてブラウザ拡張機能をインストール、以下のコマンドでインストールを実行します。
       - Chromeブラウザ
           `Encoo.Web.ExtensionInstall.exe -install -t Chrome -l zh-CN`
       - FireFoxブラウザ
            `Encoo.Web.ExtensionInstall.exe -install -t FireFox -l zh-CN`
       - Web 360ブラウザ
            `Encoo.Web.ExtensionInstall.exe -install -t Web360 -l zh-CN`

       - Microsoft Edgeブラウザ
            `Encoo.Web.ExtensionInstall.exe -install -t Edge -l zh-CN`

    - **Java拡張インストール**
    a.RemoteRuntimeインストールディレクトリのJava拡張インストールプログラム(EncooJavaExtensionInstaller.exe)を見つけ。パスは"C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Java\EncooJavaExtensionInstaller.exe"
    b. **管理者権限**でコマンドラインを開き、次のコマンドを実行：`cd C:\Program Files (x86)\EncooRemoteRuntime\app-XXXXXX\packages\XXXXXX\Extensions\Java\`、インストールプログラムがあるディレクトリに切り替える。
    c. 以下のコマンドを実行してインストールを実行する。
        `EncooJavaExtensionInstaller.exe -install -a`

### アクティビティのCitrixセッションを再起動

Encoo Remote RuntimeとEnco Citrix拡張プログラムをインストールした後に、Citrixアクティビティセッションを再起動する必要があります。そうすと変更は有効になります。

1.  Citrix Receiver トレイアイコンを右クリックし、「接続センター」をクリック。

    ![重启生效](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/citrixreceiver20210107.png)

2. ポップアップされた「Citrix接続センター」画面で、アクティビティセッションを選択し、「ログアウト」ボタンをクリック。

    > **説明:**
    >
    > この動作はすべてのアクティビティセッションのために実行する必要があります。

3. 「閉じる」ボタンをクリックして、すべての変更を確認し、ウィンドウを閉じる。

## Citrixをアンインストール

- ローカルクライアントEnco Citrix 拡張をアンインストール
  ローカルコンピュータ上の`C:\Program Files (x86)\Citrix\ICA Client\`下の`EncooRemotePluginCitrix.dll`ファイルを手動で削除すればいいです。

- リモートサービス端末の Encoo Remote Runtime プログラムをアンインストール
  コントロールパネルの中で正常にプログラムをアンインストールするのと同じに、`Encoo Remote Runtime 程序`をアンインストールすればいいです。

## Citrix動作例

Citrix技術自動化の働きを示すために、簡単な自動化プロセスを作成します。このプロセスは、ブラウザからウェブページのデータをキャプチャしてメモ帳に保存し、フォントを修正します。

1. ローカルクライアントのエディタで、リモートサービスのウェブページのデータをキャプチャしてメモ帳に保存してフォントを修正するプロセスを作成。
![Citrix Demo](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/citrixdemo20210108.png)

2. プロセスを保存して実行し、実行結果を確認します。
![Citrix 演示结果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/citrixdemoresult20210108.png)

## よくある問題

1. **Q：Encoo Remote Runtime プログラムをインストールした後、なぜCitrix自動化操作ができないですか？**
    **A:**
    - Encoo Remote Runtime プログラムは、ローカルクライアントが使用する自動化アクティビティのバージョンに対応していなければ、正常に動作しません。
     >**説明:**
     >
     >- ローカルクライアントが使用する**自動化アクティビティバージョン**はプロジェクトパネルの依存項で確認できます。
     >- リモートサービスが使用する **Encoo Remote Runtime プログラムバージョン**はインストールパッケージをダウンロードする時に確認できます。

    - エディタやロボットがアップグレードしたら、Encoo Remote Runtime プログラムも対応するバージョンにアップグレードしなければなりません。そうでないと正常に動作しません。

2. **Q：なぜCitrixの"最初のオプション > 表示"を設定したら、Web要素を指定する時に位置ずれが発生、デスクトップ要素はウィンドウをスクロールしても、検証は元の位置にハイライトされますか？**
   **A：** 現在のEncoo Remote Runtimeは、「最適解像度」だけで動作します。この現象が発生した場合、Citrixの"最初のオプション > 表示"に「最適解像度」を設定する必要があります。
   ![最佳分辨率](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/citrixproblem20210108.png)
