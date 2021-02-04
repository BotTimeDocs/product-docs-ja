# Jave拡張
**Jave拡張**はJava 1.6および以上のアプリケーションの自動化に適用されます。

Java 9＋JREで開くアプリケーションについて：
Java 9の前に、JREはattachモジュールを含み、Javaプログラムの自動化を実行するためにJava拡張はこのモジュールに依存します。Java 9+については、attachモジュールはJDKにのみ含まれていますので、JRE 9+で開くプログラムに対しては、手動でJREディレクトリにこのモジュールを追加する必要があります。

## よくある問題
1. ヒント32ビット/64ビットのJava実行環境が見つかりませんでした。

    Encooは共通Java動作環境を見つかりません。Java拡張を初期化できません。ヒントに従って32ビットまたは64ビットのJREをインストールする必要があります。下記のアドレスに対応するバージョンのJavaをダウンロードできます。<https://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html>

    a）Accept License Argumentをクリック

    ![Accept License Argument](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/java-acceptLicenseArguments.png)

    b) Encooのヒントによって32ビットまたは64ビットJavaをダウンロード（x86は32ビット、x64は64ビット

   ![下载java](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/java-downloadJava.png)

 2. Java Appletのアプリケーションまたはatchができないアプリケーションは、Java拡張を手動でruntimeディレクトリにインストールする必要があります。

    a）StudioまたはRobotインストールディレクトリ下のJavaSupportフォルダを見つける

    ![查找JavaSupport文件夹](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/java-javaSupport.png)

    > **説明:**
    >
    > Robotは1.1.20101.17以降のバージョンはインストールディレクトリのExtensions\\Javaフォルダです。

    b）Java Supportフォルダ中accessibility.propertiesruntimeの\\libディレクトリにコピーします。

    JavaSupportフォルダの中にBotTimeJava Bridge.jarruntimeの\\lib\\extディレクトリにコピーします。

    そしてBotTimeJavaBridge-*dllとBotTimeJAWT Bridge-*dllはruntimeの\\bin\\カタログにコピーします。（runtimeが32または64ビットとして対応する接尾辞のdllを複製する）

     >**説明：**
     >
     > 1.1.2009.17とその後のバージョン:
     > フォルダの中accessibility.propertiesをruntimeの\lib下にコピーし、フォルダの中のBotTimeJavaBridge.jarをruntimeの\lib\extの下にコピーして、BotTimeJavaBridge-.dllとBotTimeJAWTBridge-.dllをruntimeの\bin\の下にコピー。

    |BotTime拡張ファイル|ターゲットパス|
    |---|---|
    |BotTimeJavaBridge-32/64.dll|%JAVAHOME%\bin|
    |BotTimeJAWTBridge-32/64.dll|%JAVAHOME%\bin|
    |accessibility.properties|%JAVAHOME%\lib|
    |BotTimeJavaBridge.jar|%JAVAHOME%\lib\ext|
    |jaccess.jar|%JAVAHOME%\lib\ext|
