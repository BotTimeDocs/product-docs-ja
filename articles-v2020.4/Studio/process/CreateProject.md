# プロセスプロジェクトを作成

## プロセスプロジェクト

**プロセスプロジェクト**は、単一の自動化タスクに関連するすべてのプロセスファイルを管理するためのセットです。例えば、お客様の注文を定時的に処理する自動化プロセスを作りたい場合は、プロセスプロジェクトを作ればいいです。このタスクに関するすべてのサブプロセスファイル、依存プロジェクトなどの情報がこのプロジェクトに現れます。プロセスプロジェクトは、開発、公開、およびロボットに配布して実行を行う基本単位です。通常、独立したジョブごとに新しいプロセスプロジェクトを作成する必要があります。

エディタを起動して新しいプロジェクトを作成した後、デフォルトでは、プロジェクトはパス-%USERPROFILE%\Documents\Encooに保存されます。

このプロジェクトには以下の二つの部分が含まれています。

- 自動作成されたMain.xamlプロセスファイル。このファイルはプロセス実行時のスタートファイルとして、エディタのメインプロセスが含まれています。
- その他の.xamlプロセスファイル。自動化プロセスを実行またはデバッグする場合は、Main.xamlファイルから開始するので、その他の.xamlプロセスファイルは[プロセスを呼び出し](../../Activities/WorkflowControl/InvokeWorkflow.md?_v=v2020.4)アクティビティを通じて、Main.xamlと連携する必要があります。

## プロセスを作成

この例では、基本的なプロセスプロジェクトを作成して実行する方法を説明します。 ブラウザを開き、天気予報を検索し、明日の天気情報を取得して、明日雨が降るかどうかを通知します。

1. Encooエディタを開く
2. 新規プロジェクトを作成し、プロジェクト名を入力する（MyFirstProject を例にして）</br>
   詳細設定にの**デスクトップ録画テクノロジー**の選択については、UEA3の使用を推奨します。

    UICA3とUEAの違いは、異なる技術に対するサポートの度合いが異なることである。</br>
      - WPFとWindows Store Appsに対して、UEA3のサポートがより良いです。
      - C#とWinFormsに対してUEAのサポートがもっといいです。

        > **注意：**
        >
        >UIA3とUIAを同じプロジェクトで同時に使用することはできません。

    ![创建项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/myfirstproject20201019.png)

3. アクティビティパネルから"ブラウザーを開く"アクティビティを検索し、編集エリアにドラッグしてスタートノードに接続する
4. このアクティビティのプロパティパネルに、以下の内容を入力する
    - ブラウザーの種類：IE
    - URL: "https://www.baidu.com"

    ![ブラウザーを開く](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/intoOpenBrowser.PNG)

5. "ブラウザーを開く"アクティビティをダブルクリックして、メニューバー-ツールの"スマートレコーダ"をクリックして、録画器を開く
6. IEブラウザの百度サイトのトップページを開けて、レコーダーの"スマート録画"をクリックして、ウェブサイトの操作の録画を行う

    ![録画](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/baidu.PNG)

7. Baiduのトップページの検索テキストボックスをクリックして、出現したボックスに検索するフレーズを入力する（天気を例にして）。

    ![テキストを入力](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/inputTianqi.PNG)

8. 検索ボタンをクリックして、またはEnterボタンを押す

    ![検索ボタン](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/clickBaidu.png)

9. レコーダーの画面を開き、"テキスト"->"テキストを取得"を選択し、黄色の長方形の枠が現れる時、明日の天気情報をクリックして天気テキストを取得する

    ![テキストを取得](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/getText.png)

10. キーボードの"Esc"ショートカットを押してウェブサイトの操作の録画を終了する
11. レコーダーの"保存と終了"をクリックして、録画された自動化プロセスをエディタに保存する

    ![プロセスを保存](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/saveExit.PNG)

12. 変数リストを開き、取得した天気テキストを格納するために文字列型（String）の変数-weatherを作成する

    ![変数を作成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/createVariable.PNG)

13. "テキストを取得"アクティビティを選択して、プロパティパネルに以下の内容を入力する
    - テキスト：weather

    ![変数を入力](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/inputWeather.PNG)

14. アクティビティパネルから"条件（If）"アクティビティをドラッグして"テキストを取得"アクティビティに接続する。このアクティビティのプロパティパネルには、以下の内容を入力する
    - 判断条件：weather.Contains(“雨”)

    ![条件アクティビティをドラッグ](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/intoIf.PNG)

15. 確認ボックスのアクティビティを条件のThen部分にドラッグし、このアクティビティのプロパティパネルに以下の内容を入力する：
    - タイトル："明日の天気のヒント"
    - 説明："明日は雨です。傘を持ってきてください。"

    ![確認ボックスをドラッグ](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/intoInput.PNG)

16. もう一つの確認ボックスを条件のElse部分にドラッグして、このアクティビティのプロパティパネルに以下の内容を入力する
    - タイトル："明日の天気のヒント"
    - 説明："明日は雨が降らないので、散歩に行きましょう。"

## プロセスを実行

1. "実行"をクリックして自動化プロセスを実行してみる

    ![プロセスを実行](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/runflow20201019.png)

2. 実行中、エディタは録画した過程を自動的に再生し、明日は雨が降るかどうかのヒントを与える

    <!-- ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/result.png) -->
