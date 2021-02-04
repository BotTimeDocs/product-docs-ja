
# ステップ2：携帯電話に接続
携帯電話のクライアントソフトを開発する時は、シミュレータと実機の二つの方法を使ってAPPのデバッグを行います。ここでは二つの方法両方とも紹介しますが、実際の操作過程では、自分のニーズに合わせて選択できます。

## Android

#### 方式一：Androidシミュレータ

**Androidシミュレータ**は、パーソナルコンピュータで実行できるAndroid携帯電話システムをシミュレートするシミュレータです。Androidアプリケーションをインストール、使用、アンインストールできます。Androidシミュレータを利用すれば、ユーザーは携帯電話のハードウェア設備がなくても、シミュレータでモバイルアプリケーションを使用できます。

1. 今利用できるシミュレータの種類はたくさんあります。例えば、MuMu、逍遥、夜神シミュレータなど、自分のニーズに応じてPC端末でAndroidシミュレータをダウンロードしてインストールします。

![安卓模拟器](https://docimages.blob.core.chinacloudapi.cn/images/Studio/androidmonitor20201104.png)

2. 携帯と似ています。シミュレータの**開発者オプション-USBデバッグを許可する** 開く必要があります。

![开发者选项](https://docimages.blob.core.chinacloudapi.cn/images/Studio/developeroption20201104.png)

> **説明:**
>
> 主流なシミュレータは、下表を参照してください。

| **番号** | **シミュレータ名** | **ADB接続コード**             |
| -------- | -------------- | --------------------------- |
| 1        | 网易mumu       | adb connect 127.0.0.1:7555  |
| 2        | 夜神           | adb connect 127.0.0.1:62001 |
| 3        | 逍遥           | adb connect 127.0.0.1:21503 |
| 4        | iTools         | adb connect 127.0.0.1:54001 |
| 5        | 天天           | adb connect 127.0.0.1:6555  |
| 6        | 海马玩         | adb connect 127.0.0.1:26744 |
| 7        | BlueStacks     | adb connect 127.0.0.1:5555  |

3. ADB を環境変数に追加します。

4. PC端の**コマンドライン**インタフェースで、シミュレータに対応するADB接続コードを介してAndroid端末デバイスとPC端末を接続します。

![命令行提示符](https://docimages.blob.core.chinacloudapi.cn/images/Studio/cmd20201104.png)

#### 方式二：Android実機をUSBで接続
今サポートされている携帯電話システムのバージョンはAndroid 4.4からAndroid 10までです。その中のAndroid 9とAndroid 10に基づくのMIUI 11とMIUI 12は除外されます。


1. Androidの実機をUSBケーブルでPCと接続します。
2. 開発者モードを有効にする

各携帯電話の開発者モードを開く方法には違いがあるかもしれませんが、自分の携帯電話の開発者モードをどうやって有効にするかが分からない場合は、グーグルで"xxx型携帯はどうやって開発者モードを有効にしますか？"を検索してください。

   > **説明:**
   >
   > - 開発者モードを有効にした後、**開発者オプション**の**USBデバッグ**にチェックを入れる。
   > - 一部の携帯は"**シミュレーション位置を許可する**"、"**USBでアプリケーションをインストールするを許可**"有効にしなければなりません。

3. コンピュータに接続

コンピュータに接続する時は、携帯電話のドライバをインストールする必要があります。ドライバをインストールしたこそコンピュータが携帯を認識できます。
   > **説明:**
   >一般的にはコンピュータのUSBポートにケーブルを接続すると、自動的に携帯電話のドライバがインストールされます。パソコンで"ドライバのインストールに失敗しました"などのメッセージが出る場合にしか手動でインストールする必要があります。

4. 接続テスト

a. ADBを環境変数に追加する

   > **説明:**
    > ADBはGoogle公式が提供するAndroidデバッグツールです。

​	 <br>環境変数を作成して、Pathに追加します。例えば、"D:\workspace\Encoo\Encoo.Android.Automation\airtest\core\android\static\adb\windows"。自分の実際の状況によって置き換えられます。

   ![环境变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/environment20201104.png)

   > **説明:**
   > - システム環境変数に他のADB環境変数の構成が既に存在する場合（例えば、シミュレータ）は、ADB環境変数に対応する構成を削除する必要があります。
   > - Androidサービスパッケージを更新するたびに、サービスパスが変更される場合は、ADB環境変数を再構成する必要があります。

   b. 設備の接続を確認

PCの**コマンドライン**インターフェースで、adbコマンドを入力し、接続成功例は以下の通りです。

   ```shell
      >adb.exe

      devicesList of devices attached

      0ddc4c2d(実行のデバイス番号、もしあるの場合) device

      127.0.0.1:7555（シミュレータのデバイス番号、もしあるの場合）device
   ```

   > **説明:**
   >
   > 接続に失敗した場合は、以下の点を参照してください。
   >
   > - **adbは内部または外部コマンドではありません。** のヒントが表示された場合は、adbのシステム環境変数が設定されているかどうかを確認してください。
   > - **デバイス番号 device**この行が見えない場合は、この携帯電話の対応する公式ドライバソフトがコンピュータにインストールされているかどうかを確認する必要があります。ドライバがインストールされていない場合は、携帯電話が認識されません。自分で携帯電話ブランドの公式サイトを検索し、公式ドライバーをダウンロードしてインストールしてください。
   > - できるだけコンピュータ背中のUSBポートを使うのはお勧めです。本体正面のUSBポートは安定性が悪いかもしれません。
   > - 携帯電話では開発者オプションとUSBデバッグオプションをオンにする必要があります。パソコンに接続する時に、このPCがデバイスのデバッグを許可するように選択します。そうでないと、携帯のステータスは**unauthorized**で接続できません。
   > - コンピュータ上のすべての携帯電話のアシスタントタイプのソフトウェアはすでにシャットダウンされており、adbプロセスは完全に終了していることを確認する必要があります（ほとんどの携帯電話のアシスタントは手動でタスクマネージャでプロセスを終了する必要があります）。

## IOS

Xcodeは、システムMac OS X上で動作する統合開発ツール（IDE）であり、それぞれの機種のiphone/ipad/iwatch itvのシミュレータを持っています。このシミュレータはデバッグ用であり、App Store上のAppをインストールすることはできません。

**Macコンピュータ**上で次のように操作します。
> **説明:**
>
>Macパソコンと携帯電話を接続する時：携帯電話の**スクリーンをロック**（携帯電話の設定→表示と明るさ→オートロック）を**永遠にロックしない**に設定するのはお勧めです。録画や再生中の携帯画面ロックによる操作失敗を防ぎます。



1. 開発デバッグツールxcode 11.1バージョンをダウンロードします。

    ダウンロードリンク:<https://developer.apple.com/download/more>

![安装Xcode](https://docimages.blob.core.chinacloudapi.cn/images/Studio/installxcode20201104.png)

> **説明:**
>
> - 携帯電話のシステムバージョンがiOS 13.0以上（iOS 14.0および以上のシステムはしばらく対応していません）の場合、携帯電話の対応バージョンのデバッグパッケージを解凍した後のファイルを次のパスに入れる必要があります。/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/DeviceSupport その後にXcodeを再起動します。
> - 各バージョンのデバッグパッケージのダウンロードリンク：https://pan.baidu.com/s/1O9x8-wE0UIsA7GLWdLrMkw  パスワード:refx

2. 依存をインストール

Mac PC端末で下記のようなインストール操作を行います。

a. **brewをインストール**

brewはMacOS上のパッケージ管理ツールであり、macOSとLinuxオペレーティングシステム上のソフトウェアのインストールを簡単にすることができます。

Step 1：インストールコマンドを入力:

```
 /usr/bin/ruby -e "$(curl -fsSL https://hellogithub.cn-bj.ufileos.com/file/brew_install.sh)"
```

あるいは

```
/usr/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)" 
```

Step 2：インストールが成功したかを確認します。

```
brew --version
```
>説明:
>
> 操作中、下記の問題が発生する可能性があります。参考にしてください。
> - 問題1：Homebrewインストールエラーカーラー： (7) Failed to connect to raw.githubusercontent.com port 443: Operation
> 参考：https://www.jianshu.com/p/dea776e7effb または  https://blog.csdn.net/heroacool/article/details/102844367
> - 問題2:/usr/bin/zsh：No such file or directory
> 参考： brew install zsh
>     https://www.cnblogs.com/mafeng/p/10569559.html
> - 問題3：brewのインストールがタイムアウトしました。スピードが遅い。
>  参考：https://www.jianshu.com/p/6b486e12454f

b. **brew install usbmuxd**
> **説明:**
>
> 操作中、下記の問題が発生する可能性があります。参考してください。
> - 問題1：local権限問題
> 参考：https://www.cnblogs.com/tinys-top/p/12299663.html

c. **brew install libimobiledevice**

d. **brew install idviceinstaller** 

3. 実機のUDIDを取得

UDID（Unique Device Identifeier）は、アルファベットと数字からなる40文字列の番号で、iPhone、iPad、iPod touchesを含むユニークなiOSデバイスを区別するために使用されます。

Xcodeツールで、**Window-Devices**で設備のidentifeierを見て、コピーして貼り付けして、開発者（Encooの開発者）に連絡して、デバッグできる証明書を配置します。

![获取真机UDID](https://docimages.blob.core.chinacloudapi.cn/images/Studio/getudid20201104.png)

> **説明:**
>
> Xcodeのシミュレータ画面は下図のように。

![iOS模拟器](https://docimages.blob.core.chinacloudapi.cn/images/Studio/iosmonitor20201104.png)

4. 設定済みの証明書をXcodeツールにダウンロードします。

​      a. Xcodeツールを開く

![xcode图标](https://docimages.blob.core.chinacloudapi.cn/images/Studio/xcodeicon20201104.png)

​      b. **Xcode最初のオプション > Acceounts**をクリックし、画面左下の"+"をクリックして、Apple IDのアカウント（開発者）とパスワードを入力して保存します。

![Xcode账号配置](https://docimages.blob.core.chinacloudapi.cn/images/Studio/xcodeaccount20201104.png)

c.設定済みの証明書を選択し、**Download Manual Profiles**をクリックしてダウンロードします。

![下载证书](https://docimages.blob.core.chinacloudapi.cn/images/Studio/downloadprofiles20201104.png)
