# デバイスに接続
指定の携帯電話を接続して、携帯電話の自動化を実現します。
## プロパティ
### アンドロイド
 - **シリアル番号** ：接続されるAndroidモバイルデバイスのシリアル番号。**プラットフォーム種類**は**アンドリオッド**を選択する時にこのプロパティが表示されます。

### iOS
- **UUID** ：接続されるiOSモバイルデバイスのUUID。ワンタッチでのフィルをサポートします。
- **バージョン号** ：接続されるiOSモバイルデバイスのバージョン号。ワンタッチでのフィルをサポートします。
- **デバイス名** ：接続されるiOSモバイルデバイスのデバイス名。ワンタッチでのフィルをサポートします。

### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）です。

### 接続の設定

- **プラットフォームの種類** ：接続されるデバイスの種類は、AndriodとiOSに分けられます。
- **ターミナルアドレス** ：サービスのアドレス、例えば："sh.encootech.com:28888"

## 操作サンプル

1. 携帯とパソコンはもう接続済み。[モバイルデバイスマネージャ](/articles-v2020.4/Studio/process/developProject/MobileDevicesManage/Download.md)を参照してください。

2. **デバイスに接続**アクティビティをプロセス中にドラッグ。
3. **モバイルデバイスマネージャ**ウィンドウで追加したデバイス情報をコピー。
   ![复制设备信息](https://docimages.blob.core.chinacloudapi.cn/images/Activities/copydeviceinformation20201222.png)

4. ダブルクリック**接続デバイス**アクティビティの空白のところから、構成画面に入ります。
5. 選択**プラットフォームの種類**をクリックします**ワンタッチ充填**"ボタンを押します**接続デバイス**アクティビティの構成。\
    ![配置连接设备](https://docimages.blob.core.chinacloudapi.cn/images/Activities/settingconnectservice20201222.png)

6. プロセスを保存して実行する