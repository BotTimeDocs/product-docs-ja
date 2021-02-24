# IBM DB2拡張

IBM DB2拡張をインストールしてIBM DB2データベースの自動化を行います。

> **説明:**
>
> IBM DB2拡張をインストールした後、"**データベースに接続**"アクティビティと合わせて利用します。

## インストール

1. エディタまたはロボットを管理者として実行する。エディターの"**スタート > ツール > 拡張**"またはロボットの"**設定 > 拡張機能**"で"**IBM DB2拡張**"があります。
2. **IBM DB2拡張**"アイコンをクリック。
3. ポップアップされた**IBM DB2拡張をインストール**"メッセージボックスで、"確定"ボタンをクリックしてインストールを開始。
   ![IBM DB2安装提示](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ibmdb220210105.png)
4. 正常にインストールされると、インストール成功というメッセージが表示される。
   ![安装成功 ](https://docimages.blob.core.chinacloudapi.cn/images/Activities/tips20210105.png)   
5. "確定"ボタンをクリックしてインストールを完了させる。

## アンインストール

1. エディタやロボットのインストール先を見つける。
    > **説明:**
    >
    > - エディタのデフォルトのインストールパスは`%UserProfile%\AppData\Local\Encoo Studio`です。
    > - ロボットのデフォルトのインストールパスは`%UserProfile%\AppData\Local\Encoo Studio`です。

2. このインストールパスでの`app-x.x.20xx.xx`のようなフォルダから次のフォルダとファイルを手動で削除する。
    ![卸载DB2](https://docimages.blob.core.chinacloudapi.cn/images/Robot/uninstallDB220210114.png)