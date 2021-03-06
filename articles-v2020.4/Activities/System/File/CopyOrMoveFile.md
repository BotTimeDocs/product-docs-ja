# ファイルをコピー/移動

ターゲットファイルをコピーまたは特定の場所に移動します。効果は、システムがファイルに対してのコピーと切り取り操作と同じで、ターゲットパスのファイル名の変更をサポートします。

## プロパティ

### 入力

- **ソースファイルパス** ：対象ファイルをコピーまたは移動します。相対パスと絶対パスをサポートします。アクティビティパネルでクリックしてポップアップダイアログを表示させ、ターゲットファイルを選択することができます。手動でパスを入力することもできます。パスが存在しない場合は、実行に失敗します。文字列変数と文字列のみをサポートします。
- **ターゲットパス** ：ターゲットファイルの配置先。2つの書き方をサポートします。ディレクトリだけを記入する、具体的なファイル名と拡張子を提供しません。この場合、目標位置はデフォルトでソースファイル名を使用します。詳細なファイル名と拡張子を記入する、目標位置は提供されたファイル名を使用します。文字列変数と文字列のみをサポートします。
- **コピー/移動** ：プルダウンボックスでファイルをコピーまたは移動を選択します。コピーを選択すると、ソースファイルのコピーをターゲットパスにコピーします。移動を選択すると、ソースファイルをソースの位置で削除し、移動してターゲットパスに配置します。この時、ファイルは一つしか存在しません。両者の違いはソースファイルのパスにソースファイルを保留するかどうかです。

### オプション

- **ファイルを上書き** ：同名のファイルがターゲットパスに含まれている場合のソリューションです。チェックを付けると、同名のファイルを削除し、コピー/移動するファイルを入れることができます。チェックしないと、同名のファイルがあると実行に失敗します。

## 操作サンプル
1. **ファイルをコピー/移動**アクティビティをドラッグ:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/moveFile-1.png)

2. ダブルクリックしてアクティビティの中に入る、ソースファイルパスは相対的と絶対的なパスをサポート。アクティビティパネルで"..."をクリックして、ポップアップダイアログでターゲットファイルを選択してもいいし、手動でパスを入力してもいいです。

3. "ターゲットパス"はターゲットファイルの配置先であり、手動でパスを入力する必要があります。

4. "コピー/移動"：コピーまたは移動が選択できます。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/moveFile-2.png)

5. プロセスを実行、**ファイルをコピー/移動**アクティビティが動作し始め、ユーザーの要求に応じて、EディスクのドキュメントをDディスクの"移動ファイル"のディレクトリの下にコピーしました。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/moveFile-3.png)

