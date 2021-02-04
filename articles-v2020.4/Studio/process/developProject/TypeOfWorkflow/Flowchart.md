# プロセスチャート
**プロセスチャート**はさまざまな状況に利用できます。大型プロジェクトから小型プロジェクトまで、それらプロジェクトでプロセスチャートを繰り返し利用できます。

シーケンスとは異なり、プロセスチャートはより複雑なビジネスロジックに適用できます。 複数の異なる論理演算子を使用して、自動化プロジェクトをより多様な方法で簡単かつ迅速に統合できます。

## プロセスチャートの例
プロセスチャートについては、"ユーザーログインが成功するかを判断する"を例にして説明します。具体的な操作は以下の通りです。

1. 空白のプロセスプロジェクトを作成する。"スタートページ"で"新規プロジェクト"をクリックして新規プロジェクトを作成して、プロジェクト名を入力する、例えば"flowTest"

    ![プロジェクトを作成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/createiteminflow20201019.png)

2. 編集エリアで"変数"をクリックし、変数リストを呼び出し、"変数を作成"をクリックして、2つ文字列型（String）変数（name、password）を作成する

    ![変数を作成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-createVariables.png)

3. "プロセスチャート"を編集エリアに追加し、"開始"ノードに接続する。このアクティビティのプロパティパネルには、以下の内容を入力する
     * 表示名："ユーザーログイン"

    ![プロセスチャート](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flowchartinitem20201019.png)

4. ダブルクリックしてプロセスチャートを開き、"入力ボックス"をプロセスチャートに追加し、"開始"ノードに接続する

    ![入力ボックス](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/inputboxinflowchart20201019.png)

5. "入力ボックス"のプロパティパネルには、以下の内容を入力する
    * 入力コンテンツ：name
    * タイトル："ユーザー名"
    * 説明："ユーザー名を入力してください"
    * 表示名：ユーザー名を入力してください

    ![入力ボックスのプロパティ](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-input1Properties.png)

6. "プロセス条件分岐"を編集エリアに追加し、"入力ボックス"に接続する。このアクティビティはユーザがユーザ名を正しく入力しているかどうかを判断できます。

    ![プロセス条件分岐](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flowdecisioninflow20201019.png)

7. "プロセス条件分岐"のプロパティパネルには、以下の内容を入力する
    * 判断条件：name==""。このフィールドはユーザー名が空であるかどうかを判断するために使用されます。
    * 表示名：ユーザー名が空であるかどうかを判断。このフィールドは自分の内容に変更できます。

    ![プロセス条件分岐のプロパティ](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-decision1Properties.png)

8. "入力ボックス"を追加して、プロセス条件分岐のFalse分岐に接続する。プロセス条件分岐のTrue分岐を前の"入力ボックス"に接続し、ユーザー名を再入力するために使用されます。

    ![入力ボックス](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/inputbox2inflow20201019.png)

9. "入力ボックス"のプロパティパネルには、以下の内容を入力する
    * 入力コンテンツ：password
    * タイトル："パスワード"
    * 説明："パスワードを入力してください。"
    * 表示名：パスワードを入力してください。

    ![入力ボックスのプロパティ](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-input2Properties.png)

10. "プロセス条件分岐"を追加して"入力ボックス"に接続する。このアクティビティは、ユーザーがパスワードを正しく入力しているかどうかを判断することができます。

    ![プロセス条件分岐](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/decision2inflow20201019.png)

11. "プロセス条件分岐"のプロパティパネルには、以下の内容を入力する
    * 判断条件：password==""。このフィールドはパスワードが空であるかどうかを判断するために使用されます。
    * 表示名：パスワードが空かどうかを判断します。このフィールドは自分の内容に変更できます。

    ![プロセス条件分岐プロパティ](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-decision2Properties.png)

12. "確認メッセージボックス"を追加して、プロセス条件分岐のFalse分岐に接続する。プロセス条件分岐のTrue分岐を前の"入力ボックス"に接続し、パスワードを再入力するために使用されます。

    ![確認メッセージボックス](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/comfirmbox2inflow20201019.png)

13. "確認メッセージボックス"のプロパティパネルには、以下の内容を入力する
    * タイトル："ユーザーログイン"
    * 説明：name+"ログイン成功" 

14. 最終的に、プロセスチャートは以下の通りです。

    ![例](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-example.PNG)

実行パネルで"実行"をクリックして、ユーザー名とパスワードを入力して、最終的にTewinログインが成功したと表示されます。

 ![結果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/loginsucess20201019.png)

