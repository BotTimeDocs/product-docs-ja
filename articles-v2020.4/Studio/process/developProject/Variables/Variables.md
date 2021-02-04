# 変数
Encooエディタで、**変数**は自動化プロセス全体にわたって、複数のタイプのデータを格納するために使用されます。変数のもう一つの重要な点は、その値を変更することでループの実行回数を制御できます。

> 注意:
>
> 異なる作用スコープで使用しても、異なる名前で変数を作成する必要があります。

変数に格納されているデータは値と呼ばれ、さまざまな型があります。Encooエディタでは、テキスト、数字、時間、日付などの多くの型をサポートします。

## 変数を作成

![変数を作成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/variabletips.png)

> 注意:
>
> 編集エリアにアクティビティがないと変数は作成できません。

### ショートカットキーCtrl+Bで変数を作成

**アクティビティから** 

1. アクティビティパネルから編集エリアにアクティビティをドラッグして、アクティビティの入力ボックスに変数名を入力する
2. 名前を選択して右クリックし、コンテキストメニューから"変数を作成"を選択するか、ショートカットキー**Ctrl+B**を使用して変数を作成。変数の型とスコープは、変数リストで確認できます。

    ![変数を作成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/Activity-createVariable.png)

**プロパティパネルから**

1. いずれかのアクティビティのプロパティパネルで、あるプロパティを選択し、入力ボックスに変数名を入力する
2. 名前を選択して右クリックし、コンテキストメニューから"変数を作成"を選択するか、ショートカットキー**Ctrl+B**を使用して変数を作成。変数の型とスコープは、変数リストで確認できます。

    ![変数を作成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/Property-createVariable.png)

**式エディタから**

1. いずれかのアクティビティを選択して、アクティビティのあるプロパティの式エディターを開いて、表現式を入力する
2. 表現式の一部を選択して右クリックし、コンテキストメニューから"変数を作成"を選択するか、ショートカットキー**Ctrl+B**を使用して変数を作成。変数の型とスコープは、変数リストで確認できます。

    ![変数を作成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/Editor-createVariable.png)

> 注意:
>
> ショートカットキーで作成した変数は、選択したプロパティに応じて自動的に型を生成します。

### コンテキストメニューから変数を作成

1. 今のアクティビティを右クリックし、コンテキストメニューを呼び出し、"変数を作成"をクリック

    ![変数を作成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/menu-createVariable.png)

2. 名前を記入し、Enterキーを押す。変数リストでこの変数を見たり編集したりできます。このように作成された変数のスコープは、常にそれが属する最小のコンテナーに属します。

>  注意: 
>
> デフォルトでは、コンテキストメニューで作成される変数はすべてString型です。

### 変数リストから変数を作成

1. 編集エリアで"変数"をクリックすると、"変数"リストが表示される

    ![変数を作成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/variablePanel-createVariable.png)

2. "変数を作成"をクリックすると、デフォルトのフィールド値を持つ新しい変数が表示される

>  注意: 
>
> デフォルトでは、変数リストから変数を作成すると、すべての新しい変数がString型です。

## 変数を削除
1. 変数リストで変数を選択して右クリックし、コンテキストメニューで"削除"をクリック

    ![変数を削除](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/deleteVariable.png)

2. 変数リストで変数を選択し、 Delete キーを押す

> 注意:
>
> この操作をキャンセルする場合は、Ctrl+Zを押してください。

## .Netの変数の型を参照
"変数の型"のプルダウンボックスにデフォルトでは表示されていない変数の型を検索するには、以下の操作を行ってください。

1. 変数リストの"変数の型"プルダウンボックスから"型を参照"を選択する。".Netの型を参照と選択"画面が表示されます。

    ![型を参照](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/viewTypeOfVariable.png)

2. "型の名前"フィールドには、検索する変数の型のキーワードを入力する、例えば table

    ![変数の型を入力](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/inputTable.png)

3. table型を選択して"OK"をクリックする。この変数の型は、"変数の型"プルダウンボックスに表示されます。

    ![型を選択](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/confirmTable.png)

> 注意:
>
> ".Netの型を参照と選択"ウィンドウ中の変数の型を初めて使用する後、変数リストの"変数の型"プルダウンボックスに表示されます。
