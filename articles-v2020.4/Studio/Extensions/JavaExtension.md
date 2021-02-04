# Jave拡張
Java 1.6および以上のアプリケーションの自動化に適用されます。

> Java 9＋JREで開くアプリケーションについて：Java 9の前に、JREはattachモジュールを含み、Javaプログラムの自動化を実行するためにJava拡張はこのモジュールに依存します。Java 9+については、attachモジュールはJDKにのみ含まれていますので、JRE 9+で開くプログラムに対しては、手動でJREディレクトリにこのモジュールを追加する必要があります。



## エディタからインストール
1. **すべてのJavaアプリケーションを閉じて**、エディタの左側のツールバーにある"ツール"アイコンをクリック
2. "拡張機能"> Java拡張機能 を選択すると、確認ウィンドウがポップアップされます。
3. "OK"をクリック後、管理者権限でJava拡張インストールプログラムを起動し、ユーザーアカウントコントロールウィンドウの"はい"をクリックしてインストールを開始します。
4. インストールが成功する後、Java拡張機能のインストール成功のメッセージが表示されます。

## コマンドラインでインストール
1. **すべてのJavaアプリケーションを閉じて**、Studioのインストールディレクトリの下にあるJavaSupportフォルダの下にある拡張機能インストールプログラムEncooJavaExtensionInstaller.exeを見つけ。

   > **説明：**
   >
   >異なるバージョンのインストールディレクトリについては、以下を参照してください。：
   > - 1.1.2009.X前のバージョンのインストールディレクトリ：“C:\Users\UserName\AppData\Local\Encoo\Encoo Studio\IDE\JavaSupport”、UserNameは実際のユーザー名です。
   >  - 1.1.2009.X後のバージョンのインストールディレクトリ：C:\Users\UserName\AppData\Local\Encoo Studio\app-x.x.xxxx.xx\Extensions\Java、UserNameは実際のユーザー名です。

2. 管理者権限でコマンドラインを開き、対応するバージョンのインストールディレクトリパスに切り替：
   ```cd C:\Users\UserName\AppData\Local\Encoo Studio\app-x.x.xxxx.xx\Extensions\Java```

3. コマンドを実行：
   ```EncooJavaExtensionInstaller.exe -install -a```

**注：Javaプラグインがインストールされておらず、自動的に挿入できないアプリケーションを録画しようとすると、エディターはJavaプラグインをインストールするようにガイドします。 現時点では、Javaプラグインは現在録画されているアプリケーションのJREにのみインストールされます。**


## 手動でインストール
自動インストールをサポートする以外に、自動インストールが機能しない状況に対処するために、手動インストールも引き続きサポートされています。

1. エディタやロボットのインストールディレクトリのJavaSupportフォルダを見つけ

![img](https://docimages.blob.core.chinacloudapi.cn/images/Amanda/Java/1.png)


   >**説明：**
   >
   > 1.1.2009.X後のバージョンはインストールディレクトリしたのExtensions\Javaフォルダー。


2. JavaSupportフォルダの中のaccessibility.propertiesをruntimeの\libの下にコピーして、JavaSupportフォルダの中のBotTimeJavaBridge.jarをruntime的\lib\extの下にコピーして、BotTimeJavaBridge-*.dllとBotTimeJAWTBridge-*.dllをruntime的\bin\の下にコピー。（runtimeが32ビットであるかまたは64ビットであるによって対応するdllをコピーします）

   >**説明：**
   >
   > 1.1.2009.Xとその後のバージョン:
   > フォルダの中accessibility.propertiesをruntimeの\lib下にコピーし、フォルダの中のBotTimeJavaBridge.jarをruntimeの\lib\extの下にコピーして、BotTimeJavaBridge-.dllとBotTimeJAWTBridge-.dllをruntimeの\bin\の下にコピー。


    |拡張ファイル|ターゲットパス|
    |---|---|
    |BotTimeJavaBridge-32/64.dll|%JAVAHOME%\bin|
    |BotTimeJAWTBridge-32/64.dll|%JAVAHOME%\bin|
    |accessibility.properties|%JAVAHOME%\lib|
    |BotTimeJavaBridge.jar|%JAVAHOME%\lib\ext|
    |jaccess.jar|%JAVAHOME%\lib\ext|

## EncooJavaExtensionInstallerツール

EncooJavaExtensionInstallerは、Java拡張機能をコンピューターに自動的にデプロイするために使用されるアプリケーションです。 フルスキャンまたは特定のディレクトリでJavaプラグインのインストール/アンインストールをサポートします。

**注：インストール中の権限の問題を回避するために、管理者権限で実行することをお勧めします。**

**ファイル占有の問題を回避するために、インストールまたはアンインストールの前にJavaアプリケーションを閉じることをお勧めします。**

### 利用方法：

1. インストール
    - EncooJavaExtensionInstaller.exe -install -a，ディスク全体をスキャンしてJREを検索し、Javaプラグインをインストール。この操作が遅い場合があります。
    - EncooJavaExtensionInstaller.exe -install -d，デフォルトパス(Program Files && Program Files (x86))をスキャンしてパブリックJREを検索し、Javaプラグインをインストールします。
    - EncooJavaExtensionInstaller.exe -install -p "specified path"，特定のパスにJavaプラグインをインストールします。パスは、java.exeまたはjavaw.exeのパスまたはディレクトリにすることができます。

2. アンインストール
    - EncooJavaExtensionInstaller.exe -uninstall -a，ディスク全体をスキャンしてJREを検索し、Javaプラグインをアンインストール。この操作には時間がかかります。
    - EncooJavaExtensionInstaller.exe -uninstall -d，デフォルトパス(Program Files && Program Files (x86))をスキャンしてパブリックJREを検索し、Javaプラグインをアンインストールします。
    - EncooJavaExtensionInstaller.exe -uninstall -p "specified path"，特定のパスのJavaプラグインをアンインストールします。パスは、java.exeまたはjavaw.exeのパスまたはディレクトリにすることができます。
