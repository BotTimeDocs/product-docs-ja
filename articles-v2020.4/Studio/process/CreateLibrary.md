# アクティビティライブラリを作成

## アクティビティライブラリ

**アクティビティライブラリ**は、一つまたは1つ以上の重複使用可能なアクティビティを含むライブラリです。このプロジェクトをアクティビティ市場にリリースすることで、他のプロジェクトにパッケージとしてインストールして、依存項として使用されることができます。

アクティビティライブラリの作成は、[プロセスプロジェクトを作成](./CreateProject.md)に似ています。アクティビティライブラリは他のプロジェクトで参照できることは主な違いです。

エディタを起動し、アクティビティライブラリを作成した後、デフォルトでは、プロジェクトはパス-%USERPROFILE%\Documents\Encooに保存されます。

## プロセスを作成

この例では、どのようにアクティビティライブラリを作成するか、または他のプロジェクトで使用するために、アクティビティ市場に公開することを教えます。具体的は"Excelファイルから一部のデータを取得し、他のExcelファイルに追加"を実行します。

1. Encooエディタを開く

2. スタートページでは、アクティビティライブラリを新規作成し、ライブラリ名を入力する（Excelデータの移行を例にして）。パスを選択してタイプを設定し、詳細設定については[プロセスプロジェクトを作成](./CreateProject.md)を参照できます。ここではデフォルト値を使います。
![创建组件项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/newlibrary20201112.png)

3. 引数リストを開き、公開後のアクティビティの入力プロパティとして、2つの文字列型（String）の入力変数を作成する
    - 読み込みのパス --データを読み込むExcelファイルのパス
    - 書き込みのパス --データを書き込むExcelファイルのパス
![打开参数列表](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/createref20201112.png)
4. アクティビティパネルから"Excelを開く/新規作成"アクティビティを検索し、編集エリアにドラッグして開始ノードに接続する
![打开新建组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/opencreate20201112.png)

5. このアクティビティのプロパティパネルには、以下の内容を### 入力
    - ファイルパス: 読み込みのパス
![读取路径](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/readpath20201112.png)
6. アクティビティパネルから"範囲を読み込み"アクティビティを検索し、"Excelを開く/新規作成"アクティビティの内部にドラッグ
![读取区域组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/readarea20201112.png)
7. このアクティビティのプロパティパネルには、以下の内容を### 入力
    - シート名："Sheet1"  --データを読み込むシート名（デフォルト名Sheet1を例にして）
    - 範囲："A1:B6"  --読み込みのエリア
    - データ：Data  --このフィールドの入力ボックスをクリックし、Dataを変数名として入力し、すべてDataを選択し、ショートカットキーCtrl+Bを使って変数を作成します。
![读取区域プロパティ](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/setactivities20201112.png)
8. 再びアクティビティパネルから"Excelを開く/新規作成"アクティビティをドラッグして、前の"Excelを開く/新規作成"アクティビティに接続する
![第二个打开新建组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/opencreatetwo20201112.png)

9. このアクティビティのプロパティパネルには、以下の内容を入力：
    - ファイルパス:書き込みのパス
![写入路径](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/writepath20201112.png)
10. アクティビティパネルから"範囲に書き込み"アクティビティを検索し、第二の"Excelを開く/新規作成"アクティビティの内部にドラッグ
![写入区域](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/writearea20201112.png)
11. このアクティビティのプロパティパネルには、以下の内容を### 入力
    - シート名："Sheet1"  --データを書き込むシート名（デフォルト名Sheet 1を例にして）
    - 開始セル："A1"
    - データテーブル：Data
![写入区域プロパティ](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/setwritearea20201112.png)

## プロセスを実行

1. "実行"をクリックするか、ショートカットキーCtrl+F6を使って、プロセスを実行させる

2. 引数のデフォルト値を設定し、第一ののExcelファイルから一部のデータを読み出して第二のExcelファイルに記入することを確認する
![设置流程参数](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/setflowref20201112.png)

## アクティビティライブラリを公開

このプロジェクトを再利用可能なアクティビティとして、他の自動化プロジェクトに追加するには、パッケージ化して、アクティビティ市場に公開する必要があります。

1. 作成したアクティビティライブラリを開く

2. メニューバーで"アクティビティ市場に公開"をクリックして、公開ウィンドウを開く
   ![发布到组件市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/publishactivities20201112.png)
    - ターゲット市場を選択して、市場がなければ、"市場を管理する"をクリックして作成します。どのように市場を作成しますか？[市場を管理する](../market/Market.md)を参照してください。
    - **最新バージョン**フィールドでは、現在公開するバージョンを設定できます。
    - **説明**フィールドでは、このアクティビティライブラリに関する詳細情報を追加できます。

## アクティビティライブラリをエクスポート

他のプロジェクトで参照できるようにアクティビティライブラリをエクスポートする必要がある場合は、プロジェクトを選択して右クリックし、"プロジェクトをエクスポート"を選択します。ポップアップの"プロジェクトをエクスポート"ダイアログボックスで、必要に応じて関連する構成を選択します。

![导出项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Debugging/exportproject20201214.png)

> **説明：**
> エクスポートされたアクティビティライブラリは“.egs”を拡張しとします。これは拡張子が".dgs"であるプロセスプロジェクトとは異なります。

## アクティビティをインストールして利用する

他の自動化プロジェクトでこのパッケージを使うなら、先にインストールして、自動化プロジェクトの依存ライブラリとして追加してください。

1. プロセスプロジェクトを作成。[プロセスプロジェクトを作成](./CreateProject.md)を参照してください。

2. アクティビティパネルで、"アクティビティ市場"をクリックして、アクティビティ市場のウィンドウを開く

3. ウィンドウの左側に前に作成された市場を選択して、公開されたパッケージを検索して選択する。この例では、このパッケージ名はExcelデータ移行です。

4. ［インストール］をクリックして、インストールが完了したらウィンドウを閉じる。このとき、このパッケージは今のプロセスプロジェクトに追加された。アクティビティパネルに表示される。
![组件安装](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/useactivitiesmarket20201112.png)

5. アクティビティパネルから、"Excelデータ移行"アクティビティを編集エリアにドラッグしてスタートノードに接続する

6. このアクティビティのプロパティパネルには、以下の内容を入力する
    - 読み込みのパス："C:\Users\ユーザー名\Documents\Encoo\アクティビティライブラリを使用して編集したアクティビティ\start.xlsx"　--データを読み込むExcelファイルの全パス
    - 書き込みのパス："C:\Users\ユーザー名\Documents\Encoo\アクティビティライブラリを使用して編集したアクティビティ\final.xlsx" --データを書き込むExcelファイルの全パス

    > **注意：**
    >
    > アクティビティにパスのプロパティが含まれている場合、相対パスは使用できません。全パスを使用しなければなりません。

7. "実行"をクリックして、start.xlsxの一部のデータをfinal.xlsxに移行することができる。
![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/runresult20201112.png)
