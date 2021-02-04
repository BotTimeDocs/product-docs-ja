# ステップ3：自動化サービスを構成

## Android

### サービスに接続

1. ダウンロードしたモバイルサービスパッケージ **Enco.Android.Automationzip** を解凍する

> **説明:**
>
> 解凍パスに漢字が含まれていないことを確認する必要があります。

2. 解凍完了したフォルダで**Enco.Android.Automation.exe**をダブルクリック。

3. ポップアップされた**Encoo Androidサービスマネージャ**ウィンドウで**サービスに接続**をクリック

![Android连接服务](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Andriodconnect20201104.png)

4. サービスの接続が成功しました。下図のように。

![服务连接成功](https://docimages.blob.core.chinacloudapi.cn/images/Studio/serverconnectsucess20201104.png)

### アプリのインストール（初めて）

解凍されたフォルダの下の**apk**フォルダに、次の3つの携帯アプリのインストールパッケージがあります。必要に応じてインストールします。

![APP应用](https://docimages.blob.core.chinacloudapi.cn/images/Studio/app20201104.png)

| **番号** | **インストールパッケージ** | **説明** |
| -------- | ----------------- | ------------------------------------------------------ |
| 1        | pocorvice-debug | 携帯電話のページ要素コントロールの情報を表示します。 |
| 2        | SmsObserver | **SMS確認コードを取得**アクティビティと一緒に使用して、SMS確認コードを取得します。<br>**説明:**<br>-このアプリケーションは、Android 6.0および以上のバージョンをサポートします。<br>- "SMSの内容を読み込み"権限は"許可"に設定する必要があります。 |
| 3        | Yosemitee | テスト時にデフォルトで使用する入力法で、テスト後に手動で入力法を変更できます。 |

## IOS

### サービスに接続

**Macコンピュータ**で次のように操作します。

1. ダウンロードしたモバイルのサービスパッケージ **Enco.IOS.Automationzip** を解凍します。

> **説明:**
>
> 解凍パスに漢字が含まれていないことを確認する必要があります。

2. 解凍完了したフォルダで**EncooIOSAutomation**をダブルクリック。
> **説明:**
>- このアプリケーションを初めて実行する場合、Macの"設定 > 安全性とプライバシー"で"許可"スイッチを開く必要があります。
>- このアプリケーションをダブルクリックすると、"ファイルが壊れました"と表示される場合は、[解決策](https://www.macdo.cn/925.html)を参照できます。

3. ポップアップされた**Encoo iOSサービスマネージャ**ウィンドウ**サービスに接続**をクリック

![iOS连接服务](https://docimages.blob.core.chinacloudapi.cn/images/Studio/iosconnect20201104.png)

> **説明:**
>サービスを開始て携帯に接続すると、問題があるかもしれません。以下を参考にしてください。
>  - 問題1:xcode-select:error：tool‘instruuments’requires XcodeまたはIDEが接続中と表示する時に関連ログステータスが出力されます。
>  <br>解決の参考：
 >  <br> - Xcodeをインストールするパスを確認する（Xcodeを見つけて、直接に端末にドラッグしてパスを確認できます）
 >  <br> -  sudo xcode-select --switchを実行して、端末にXcodeのパス/Contents/Developer/が表示されます。
 > - 問題2：IDEは携帯に接続できません。
 > <br>解決の参考：/usr/binにpythonがインストールされているかどうかを確認する必要があります。もしあれば、元のpythonバージョンをアンインストールする必要があります。