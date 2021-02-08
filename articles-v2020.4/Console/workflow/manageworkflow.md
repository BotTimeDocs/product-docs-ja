# プロセス展開を管理
## プロセス展開を作成
プロセス展開ページで"新規作成"ボタンをクリックして新規作成を開始します。

手順1

1）プロセス展開基本情報を記入し、対応するプロセスパッケージとプロセスパッケージバージョン番号を選択します。

2）失敗した最大再試行回数を設定、プロセスの実行に失敗した後、その回数に応じて自動的に再試行します。

3）タスク優先度を設定（1−5000）：優先度が高いほど、先にタスクが実行されます。

![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/%E6%96%B0%E5%BB%BA%E6%B5%81%E7%A8%8B%E9%83%A8%E7%BD%B21.1.png)

4）プロセスパッケージの引数に値を代入：

手動で割り当て：代入する値を記入すればいいです。

資産をインポート："資産をインポート"をクリックして、資産管理ページにあらかじめ保存されている資産を選んで、割り当てを行うことができます。

![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/%E6%96%B0%E5%BB%BA%E6%B5%81%E7%A8%8B%E9%83%A8%E7%BD%B2%E7%AC%AC%E4%B8%80%E9%A1%B5%E8%A1%A5%E5%85%85.png
)

![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/%E6%96%B0%E5%BB%BA%E6%B5%81%E7%A8%8B%E9%83%A8%E7%BD%B2-%E5%AF%BC%E5%85%A5%E8%B5%84%E4%BA%A7.png)

手順2

"次へ"をクリックしてロボットの実行ターゲットを設定し、キューまたはロボットを選択して実行します。

1）キューで実行：リソースグループの下で作成されたキューから選択します。

![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow3.png)

2）ロボットを選択：リソースグループの下にあるすべてのロボットを示し、チェックを付けることで選択します。名前とラベルによって検索することができます。

![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow4.png)

保存をクリックすればプロセス展開の新規作成を完了できます。"保存してタスクプランを設定"をクリックすれば簡単にタスクプランを設定できます。（詳細は"タスクプラン管理"を参照してください。）


## プロセス展開の設定情報を表示

プロセス展開の"設定"ボタンをクリックすると、プロセス展開の設定情報が表示されます。

![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow5.png)

## 基本設定と引数の変更

プロセス展開の"設定"画面で"編集"ボタンをクリックすると、基本設定情報と引数情報を変更でき、修正が完了したら"保存"ボタンをクリックすればいいです。

![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow6.png)

## プロセス展開を削除

選択したプロセス展開の操作オプションの"削除"ボタンをクリックすれば、対応するプロセス展開を削除できます。

![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow7.png)
