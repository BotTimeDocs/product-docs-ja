# ファイルサービスを管理

## フォルダ管理

フォルダ管理は、各フォルダ、サブフォルダを新規作成や削除などの操作をできます。ファイルサービスのファイルは、あるフォルダ/サブフォルダに保存しなければなりません。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileervice1.png)

### 新規フォルダ
左側のリストの"新規作成"ボタンをクリックするとフォルダを新規作成でき、作成されたフォルダの"名前付き枠"は自動的に編集可能な状態になり、名前を入力してエンターキーを押せば保存できます。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileservice2.png)

### 新規サブフォルダ
あるフォルダを選択し、対応する"新規サブフォルダー"ボタンをクリックしてサブフォルダを追加できます。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileservice3.png)


### フォルダ&サブフォルダの削除
あるフォルダを選択し、対応する"削除"ボタンをクリックすると、このフォルダを削除できます。


## ファイル管理

### ファイルをアップロード
あるフォルダを選択して、対応する"アップロード"ボタンをクリックして、ポップアップ画面でアップロードするファイルを選択すればフォルダにファイルをアップロードできます。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/uploadfile.png)


### ファイルアップロードプロセス管理
すべてのファイルのアップロードプロセスを展示します。主に全部アップロード成功、一部アップロード成功、全部アップロード失敗の三つの状態が含まれます。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/uploadstatus.png)

### ファイルをダウンロード
あるファイルを選択して、対応する"ダウンロード"ボタンをクリックし、二回確認してから、このフォルダをダウンロードできます。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/downloadfile.png)

### ファイルを削除
あるファイルを選択して、対応する"削除"ボタンをクリックし、二回確認してから、このフォルダを削除できます。
![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/deletefile.png)


## ファイルサービス権限を管理

ファイルサービスの権限は一級フォルダによって設定されていますが、ユーザーがある一級フォルダに対して何らかの権限を持つと、その一級フォルダの下のすべてのフォルダまたはファイルに対して同じ権限を持っています。

### 権限編集ページを開く

一級フォルダの操作オプションの"権限を管理"ボタンをクリックして権限編集ページに遷移し、編集が完了したら"保存"ボタンをクリックすれば保存できます。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileauthority1.png)


### 作成者権限
作成者はフォルダの作成者であり、デフォルトで管理権限が割り当てられています。

### ユーザー権限を指定

ユーザー権限を指定は、異なるユーザーに異なるユーザー権限を与えることができます。

1）"追加"ボタンをクリックすると、現在のテナントの下にすべての追加可能なユーザーリストが表示されます。

2）追加するユーザーをチェックし、"確定"ボタンをクリック

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileauthority2.png)

3）追加された後にデフォルトで読み取り可能な権限を持ち、プルダウンから選択することで特定のユーザーの権限を変更することができます。

![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileauthority3.png)

4）ユーザー名の前にある"削除"ボタンをクリックすると、対応するユーザーを指定されたユーザーリストから削除することができます。


### 他のユーザーの権限

その他のユーザーは、現在のテナントの下に作成者、指定したユーザーリスト以外のすべてのユーザーを指します。デフォルトでは権限がありません。プルダウンから選択することで権限を変更できます。
![fileservice](https://docimages.blob.core.chinacloudapi.cn/images/Console/Datacentor/fileauthority5.png)
