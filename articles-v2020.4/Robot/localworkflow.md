# プロセスライブラリ

ロボットは、デスクトップでクリックすることでプロセスを実行できます。コンソールを介してプロセスを一元管理して実行もできます。

コンソールの一元管理実行プロセスの詳細は次を参照してください。[プロセスを発行する方法](Console/../../Console/workflow/manageworkflow.md)

ローカルで実行されるプロセスは、次の2つのソースがあります。

1. ローカルプロセスファイル：エディターを介してエクスポートされたプロセスパッケージ（サフィックスが.dgsでのプロセス圧縮パッケージ）
2. コンソールプロセスライブラリ：ロボットが属するリソースグループから[プロセスパッケージ](..\Console\packages\aboutPackages.md)を取得

**コンソールプロセスライブラリ**はコンソールを介してアクティブ化されたロボットのみ使用できます。

同じロボットは同時に1つのプロセスしか実行できず、次のプロセスはプロセスが完了した後にのみ実行できます。


### ローカルプロセスを実行
1. ローカルプロセスライブラリを開く
2. プロセスをインポートをクリックして、エディターを介してエクスポートされたプロジェクトファイル（*.dgs）をローカルプロセスライブラリにインポート
3. 実行したいプロセスを選択します。プロセス名で検索できます。
4. "実行"をクリックすると、確認メッセージが表示されます。

    ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/flowofexecution20201201.png)
    
 - プロセス：実行するプロセスのプロセス名とバージョン番号を表示します。
 - 引数：プロセスが引数を入力する必要がある場合、実行をクリックすると、ポップアップウィンドウで引数の入力は求められます。
    > **説明：**
    >
    > 引数タイプが Encoo.DataType.FilePath、Encoo.DataType.FolderPath の場合、手動で入力する必要なく、引数タイプに応じてファイルまたはフォルダのパスを選択できます。
 - オプション：各オプション引数の説明は次の通りです。


    | オプション | 説明 |
    | :---- | :---- |
    | ビデオを録画 | プロセスの実行中に特定の実行状態のビデオを録画するか。 |
    | 実行中スクリーンショット | 実行の過程でスクリーンショットを取るか。 </br> <font color="grey" size="3" face="楷体"> **説明：** </br>   <ul><li>スクリーンショットは、現在のプロセスログディレクトリ下の Screenshots フォルダに保存されます。</li><li>画像名の形式：{プロセス名}-{スクリーンショット時間：年月日時分秒}.jpg、例：スクリーンショット-20201201164102599.jpg </li> </ul> </font>  |
    | 管理者権限で実行 | 管理者として実行するかどうか。チェックするとコンピュータ管理者として実行するとします。そうでない場合、通常のユーザーとして実行します。 |
    | タイムアウト | 実行時間が設定時間を超えると、処理は終了します。たとえば、"タイムアウト時間は1分"をチェックすると、実行が1分以内に完了する必要があることを意味します。そうしないと、プロセスを終了します。 |


5. OKをクリックすると、プロセスが自動的に実行されます。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/Robot-Process-0.png)


### コンソールプロセスを実行
1. プロセスライブラリを開く
2. コンソールプロセスライブラリをクリックして、プロセスライブラリ内のすべてのプロセスパッケージを取得できます。
3. プロセスパッケージ名を検索して、実行するプロセスパッケージを見つけることができます。
4. 実行するバージョンを選択し、実行をクリックします。
    ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/Robot-Process-Console-0.png)


### プロセスを終了

プロセスの実行中、ユーザーはいつでもプロセスを終了できます。

1. ローカル/コンソールのライブラリを開き、実行中のプロセスを見つける
2. 右側の**終了**ボタンをクリック
   >**説明:**
   >
   >ショートカットキーShift+F5を使用して、現在実行中のプロセスを終了できます。

3. **終了**を確認した後、ロボットはプロセスがどのステップまで行っても問わず強制的に実行中のプロセスを終了します。**終了**操作がキャンセル、削除できませんので、慎重に操作してください。

    ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/Robot-Process-Kill-0.png)


### ログの表示（録画したプロセスの実行ビデオを含む）

プロセスの実行が終了すると、ユーザはログを見ることができます。
1. ローカル/コンソールのプロセスライブラリを開いて、実行したプロセスを見つける
2. **ログ**をクリックして、このプロセスの実行記録を含むログフォルダーを開く、実行ビデオも含みます。
    ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/Robot-Process-Log-0.png)

### プロセスを削除
ユーザーがローカルライブラリのプロセスを削除することをサポートします。コンソールのプロセスライブラリ中のプロセスを削除する場合は、コンソールに行く必要があります。
1. ローカルライブラリを開いて、削除するプロセスとバージョン番号を選択。
2. **削除**をクリックして、現在のバージョンを削除するかどうか確認します。"OK"をクリックしてこのバージョンのプロセスを削除します。
    ![robot](https://docimages.blob.core.chinacloudapi.cn/images/Robot/robot-deleteflow-1.png)
