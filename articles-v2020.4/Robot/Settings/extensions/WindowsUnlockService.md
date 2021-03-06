# Windows画面ロック解除サービス

## ケース紹介

いくつかのロボットのプロセスをトリガするにはcronジョブを設定する必要があります。毎日同じ時間で、異なる頻度でプロセスを実行します。ロボットが起動している時に、コンピュータがロックされている状態であれば、プロセスの実行にエラーが発生します。

このような場合に対して、RPAロボットのロック防止機能を提供します。

## ケース実現

ロボットまたはエディタが[スクリーンをロック](System/Screen/WindowsLockActivity.md)または[ロックを解除](System/Screen/WindowsUnlockActivity.md)を実行する前、Windowsのソフトウェアインターフェイスの操作を自動化するには、**管理者**として**Windows画面ロック解除サービス**をインストールする必要があります。

1. **Windows画面ロック解除サービスをインストール**</br>

   a. 管理者として**エディタ**または**ロボット**を実行</br>
   b. Windows画面ロック解除サービスをクリックしてインストールします。</br>

   >**説明:**
   >
   >- エディタでWindows画面ロック解除サービスの入り口：ホームページ > ツール
   >- ロボットでWindows画面ロック解除サービスの入り口：設定 > 拡張。

2. **スクリーンをロック**</br>

    プロセス中スクリーンロックを実行する必要があるところに、スクリーンをロックアクティビティをドラッグし、そのプロパティを設定して、手動で"Win＋L"キーを押すのを代わります。プロセスはまだスクリーンロック状態で実行されます。

3. **ロックを解除**</br>

プロセス中ロック解除を行う必要があるところに、ロック解除アクティビティをドラッグしプロパティを設定し、手動でユーザ名とパスワードを入力するのを代わります。コンピュータの画面を自動的にロック解除することができます。

## よくある問題

1. **Windows画面ロック解除サービスはどのOSをサポートしますか？**</br>
   現在サポートされているOSは、Windows 7、Windows 10、Windows Server 2008、Windows Server 2016、Windows Server 2019があります。

2. **Windows画面ロック解除はどうやってアンインストールしますか？**</br>
    手順1：アンインストールプログラムの入り口：[アンインストールプログラム](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/EncooCredentialProviderUnInstall.bat)</br>
    手順2：右クリックして管理者として実行させ、アンインストール成功は下図のようになります。</br>
    ![Windows 屏幕解锁服务卸载完成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/uninstall20201202.png)</br>

3. **Windows 10システムでメールオンラインアカウントでログインする場合、ロック解除アクティビティに記入されたユーザ名プロパティは無効**</br>
   ロック解除アクティビティの"ユーザ名"プロパティに、C:\Users"ディレクトリの下で作成されたメールオンラインアカウント名のフォルダ名を記入します。

4. **ドメインユーザでログインする時、ロック解除アクティビティに記入されたユーザ名プロパティは無効**</br>
   ドメインユーザでログインする場合は、ロック解除アクティビティのユーザー名プロパティに"{ドメイン\ユーザー名}"を記入する必要があります。例えば：EncooFrank\Administrator

5. **エンタープライズ版やServer版のオペレーティングシステムがスクリーンをロックした後、画面に"Ctrl+Alt+Deleteでロック解除"という文字がありますが、自動ロック解除はサポートされていませんか？**</br>
    自動ロック解除をサポートしますが、次の前提条件があります。"コントロールパネル > システムとセキュリティ > 管理ツール > ローカルポリシー"の下の"インタラクティブログイン：Ctrl+Alt+Delを押す必要がない"の"有効"をチェックしてください。
