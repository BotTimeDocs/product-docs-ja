# SAP自動化設定の手順

この機能はEncooエンタープライズ版エディタでのみサポートされます。

## SAP WinGUIスクリプトを有効にする
`SAP WinGUIスクリプトを有効にすることは、安全上の問題はありません。`
### トランザクションを実行し、引数を変更
1. SAPを開いて、ログインする
2. トランザクションコード**RZ11**を実行
3. 引数名 **sapgui/user_scripting**を入力して、Enterキーを押す
4. **引数ファイルの引数を編集**ウィンドウに引数名に**sapgui/user_scripting**を入力、**表示**をクリック
5. **値を変更**をクリックし、**新しい値**を**TRUE**に設定して、**変更を保存**
5. ステップ4を繰り返し、それぞれ下記の引数の値を**FALSE**に変更
    - sapgui/user\_scripting\_disable\_recording
    - sapgui/user\_scripting\_force\_notification
    - sapgui/user\_scripting\_per\_user
    - sapgui/user\_scripting\_set\_readonly

    >**説明：**
    >
    >トランザクションRZ11における引数のすべての変更は即時に有効となり、システムの再起動時に失われます。変更を永久に有効にするには、SAPシステム管理者に連絡してください。

6. ログアウトして再ログインします。

### スクリプトを有効にするをチェック
1. クリックして**オプション**メニューを開く
2. **補助機能とスクリプト**に移動し、**スクリプト**をクリック
3. **スクリプトを有効にする**をチェック
4. 下記のオプションをチェックしない:
    - スクリプトがSAP GUIに付加されるときに通知します。
    - スクリプトが接続を開くときに通知します。

     >**説明：**
    >
    >スクリプトを有効にするの手順が実行されていない場合、プロセスの実行中に次の図が表示されます。スクリプトを有効にするをチェックの手順に従って設定してください。
    
    ![注意](https://docimages.blob.core.chinacloudapi.cn/images/Amanda/SAPWarning.png)