# 自動化プロジェクトを公開

**自動化プロジェクトを公開**とは編集された自動化プロジェクトを公開および保存して、後続のロボットの実行または共有プロセスに使用できます。

自動化プロジェクトをコンソールに公開すると、指定されたロボットに割り当てて実行するために、プロセスパッケージ管理ページに格納されます。プロセス市場に公開すると、共有を実現するために指定されたプロセス市場に格納されます。

自動化プロジェクトを直接ロボットに渡して実行したいなら、ロボットに公開することで、自動化プロジェクトを対応ロボットに送ることができます。

プロセスの公開を実行するには、ツールバー→公開で、公開したい場所を選択してクリックします。

![プロジェクトを公開](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/publishProject/publishinpath20201019.png)

## プロセスを公開

1. 自動化プロジェクトを作成。詳細設定については[プロセスプロジェクトを作成](./CreateProject.md)を参照できます。
2. ツールバー->公開、公開の場所を選択：
    - コンソールに公開

        ![コンソールに公開](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/publishProject/publishToConsole.PNG)

        a. **リソースグループ**は、プロジェクトを公開するリソースグループを選択できます。

        b. **プロセスパッケージ名**はデフォルトでプロジェクト名であり、変更できます。

        c. **バージョン**は、プロジェクトの**現在のバージョン**を表示し、必要に応じて**最新のバージョン**を追加できます。 バージョン情報を変更する場合は、最新のバージョンが現在のバージョンより大きいする必要があることに注意してください。

        d. (オプション)**備考**は今の自動化プロジェクトに関するバージョンとその他の情報を入力します。備考の内容は220文字を超えてはいけません。

        f. “**依頼関係を含む**”をチェックにすると、プロジェクトを公開する時にプロジェクトの依存関係がプロセスパッケージに含まれます。チェックしない場合は、依存関係がプロセスパッケージに含まれていないことを意味します。

    - ロボットに公開

        ![ロボットに公開](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/publishProject/publishToRobot.png)

        a. **ロボット**は、現在のシステムでアクティブになっているロボットの名前が表示されます。

        b. **プロセスパッケージ名**はデフォルトではプロジェクト名で、変更できます。

        c. **バージョン**はプロジェクトの**現在のバージョン**を選択し、必要に応じて追加します。**最新バージョン**。バージョン番号情報を変更する場合、最新のバージョン番号は現在のバージョン番号より大きくなります。

        d. (オプション)**備考**は今の自動化プロジェクトに関するバージョンとその他の情報を入力します。備考の内容は200文字を超えてはいけません。

        f. “**依頼関係を含む**”をチェックにすると、プロジェクトを公開する時にプロジェクトの依存関係がプロセスパッケージに含まれます。チェックしない場合は、依存関係がプロセスパッケージに含まれていないことを意味します。

    - プロセス市場に公開

        ![プロセス市場に公開](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/publishProject/publishToFlowmarket.PNG)

        a. **プロセス市場**は、プロジェクトをどのプロセス市場に公開するかを選択することができます。初めての公開の前に、**市場を管理する**で市場を設定する必要があります。具体的な手順は[市場を管理する](../market/Market.md?_v=v2020.4)を参考してください。

        b. **プロセスパック名**デフォルトではプロジェクト名ですので、変更できます。

        c. **バージョン**はプロジェクトの**現在のバージョン**を選択し、必要に応じて追加します。**最新バージョン**。バージョン情報を変更する場合、最新のバージョンは現在のバージョンより大きくなります。

        d. (オプション)**アイコン**は現在公開されているプロセスを識別するために使用されます。

        e. **説明**は今の自動化プロジェクトの機能などに関する紹介を入力します。説明の内容は200文字を超えてはいけません。

        f. (オプション)**ラベル**は現在のプロセスを定義します。

        g. “**依頼関係を含む**”をチェックにすると、プロジェクトを公開する時にプロジェクトの依存関係がプロセスパッケージに含まれます。チェックしない場合は、依存関係がプロセスパッケージに含まれていないことを意味します。

3. "公開"をクリックして、指定の場所に公開
4. 公開に成功すると、メッセージボックスが表示されます。以下が内容です。
    - 公開成功のプロジェクト名
    - プロジェクトのバージョン

        ![公開に成功](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/publishProject/publishSuccess.PNG)
