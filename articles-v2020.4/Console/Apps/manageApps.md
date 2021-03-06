## ミニプログラム管理
**プログラム管理**画面に入って、現在のリソースグループの下にあるすべての公開されたミニプログラムを見ることができます。**リソースグループ**を切り替えすることで違うリソースグループ下のミニプログラムを表示できます。

## ミニプログラムを表示

ミニプログラムリストは、公開されたすべてのミニプログラムおよびミニプログラムの現在のステータスを表示します。
**有効にする** ：現在のミニプログラムが公開されたことを指します。リソースグループの下のユーザーがミニプログラムサイトの**私のミニプログラム**アクセスすることでこのミニプログラムを表示して実行できます。
**無効にする** ：現在のミニプログラムが公開されない状態で、ユーザーが見えないことを指します。

有効されたミニプログラムは現在有効されたバージョン番号をマークします。
ミニプログラムの名前をクリックしてミニプログラムの詳細を見ることができます。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/manageapps.png)

## ミニプログラムの詳細を表示
ミニプログラムの名前をクリックして、ミニプログラムの詳細を開きます。
ミニプログラムの詳細画面で、ミニプログラムの現在のバージョンと履歴バージョンを確認できます。現在有効にされたバージョンはバージョンの所に**現在**のマークが表示されます。
詳細ページでミニプログラムの現在バージョンを試してもできます。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/appsdetail.png)

**他のバージョンを見る**をクリックして、ミニプログラムの他のバージョンを表示できます。
矢印がマークしたのは現在のプレビューバージョンで、バージョンをクリックすることでプレビューバージョンを切り替えることができます。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/appsdetail2.png)

現在のミニプログラムの有効にされたバージョンを切り替えたい場合は、**他のバージョンを見る**で有効にしたいバージョンの詳細に切り替えて、詳細画面で**現在のバージョンに切り替え**をクリックすると、現在選択されているバージョンに切り替えられます。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/appsdetail3.png)

注意：無効にされたミニプログラムは公開されていないので、現在の有効にされバージョンはありません。

## ミニプログラムを有効にする
**無効**ステータスのミニプログラムに対しては、リストまたは詳細の有効ボタンでミニプログラムを有効にすることができます。
リストでミニプログラムを有効にすると、デフォルトではミニプログラムの最新バージョンが有効になります。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/activeapps1.png)
詳細画面でミニプログラムを有効にすると、デフォルトでは詳細画面で選択された最新バージョンが有効になります。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/activeapps2.png)

## ミニプログラムを無効にする
**有効**のミニプログラムに対しては、リストまたは詳細の無効ボタンでミニプログラムを無効にすることができます。
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/inactiveapps1.png)
![robot](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/inactiveapps2.png)

## ミニプログラムを削除
単一のバージョンまたはすべてのミニプログラムを削除することができます。

ミニプログラム全体を削除すると、ミニプログラムのすべてのバージョンが削除されます。ミニプログラムサイトのオリジナルの開発パッケージも削除されます。

### ミニプログラムを削除
ミニプログラム管理ページに入り、削除するミニプログラムを見つけ、削除をクリックし、二回確認したら削除します。
![package](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/deleteApps.png)



### ミニプログラムのバージョンを削除
ミニプログラム管理ページに入り、削除するバージョンのミニプログラムを見つけます。
ミニプログラムの詳細画面でバージョンを表示をクリックします。
削除するバージョンを見つけ、削除をクリックすれば削除できます。
![package](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/deleteApps1.png)
バージョンを削除するには以下の条件を満たす必要があります。
 - バージョンが"現在"の状態ではありません。