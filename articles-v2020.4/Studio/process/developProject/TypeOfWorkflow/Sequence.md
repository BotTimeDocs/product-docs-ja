# シーケンス
**シーケンス**は、最小のプロジェクトタイプです。線形過程に適用されます。一つのアクティビティから他のアクティビティにシームレスに移行することができ、単一のアクティビティブロックとして機能することができます。

シーケンスの重要な特徴の一つは、独立した自動化プロジェクトまたはプロセスチャートの一部として繰り返し再利用できることです。

Windows Workflow Foundationの制限のため、多くのアクティビティを一つのシーケンスから他のシーケンスにコピーしたい場合は、事前に下にスクロールすることを推奨します。

> 注意：
> シーケンスは接続線を使用しません。

## シーケンスの例
"ユーザーに名前と年齢を聞いて、その答えを表示"の例を作成することでシーケンスを説明します。具体的な操作は以下の通りです。

1. 空白のプロセスプロジェクトを作成する。"スタートページ"で"新規プロジェクト"をクリックして新規プロジェクトを作成して、プロジェクト名を入力する、例えば"sequenceTest"

    ![プロジェクトを作成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/sequencetestitem20201019.png)

2. アクティビティパネルから"シーケンス"アクティビティを編集エリアにドラッグする

    ![シーケンス](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/sequenceactivity20201019.png)

3. ユーザーからのデータを保存するため、2つの文字列型（String）変数を作成する。例えばNameやAge。デフォルトのフィールドを空にして、デフォルトの値がないことを表します。

    ![変数を作成](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/seq-createVariables.png)

4. 二つの"入力ボックス"アクティビティを編集エリアにドラッグして、一つをもう一つの下に置く

    ![入力ボックス](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/inputboxinsequence20201019.png)

5. 第一の"入力ボックス"を選択して、ユーザー名を入力することを要求する説明とカスタムタイトルをプロパティパネルに追加する

6. 入力のコンテンツフィールドにName変数を追加する。これは、この変数がユーザによって追加された値に更新されることを示しています。

    ![入力ボックスのプロパティ](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/seq-input1Properties.png)

7. 第二の"入力ボックス"アクティビティに対して、ステップ5−6を繰り返し、ユーザの年齢を尋ねて、Age変数に格納する

    ![入力ボックスのプロパティ](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/seq-input2Properties.png)

8. 第二の"入力ボックス"の下に"確認メッセージボックス"アクティビティを追加する

    ![確認メッセージボックス](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/comfirminsequence20201019.png)

9. "確認メッセージボックス"を選択して、プロパティパネルの"説明"フィールドに変数と文字列を追加して、ユーザーから収集されたすべての情報を表示することができる。例えば、Name+"の年齢は"＋Age＋"歳です。""</br>（オプション）"タイトル"フィールドに、"ユーザ情報"を記入することができる

    ![確認メッセージボックスのプロパティ](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/seq-confirmProperties.png)

10. 最終的に、シーケンスは以下の通りです。

    ![例](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/seq-example.PNG)

実行パネルで"実行"をクリックして、Tewin、24を入力し、"Tewinの年齢は24歳です"が表示されます。

![結果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/sequenceresult20201019.png)

