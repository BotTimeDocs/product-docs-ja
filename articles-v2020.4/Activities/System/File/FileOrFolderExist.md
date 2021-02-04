# パスの存在を確認

指定されたファイルやフォルダが存在するかどうかを判断し、結果を返します。

## プロパティ

### 入力

- **タイプ** ：プルダウンボックスからファイルまたはフォルダを選択し判断する種類とします。
- **パス** ：判断を実行するファイルまたはフォルダのパス。相対および絶対パスをサポートします。文字列変数と文字列のみをサポートします。

### 出力

- **存在の有無** ：判定結果をこの変数に格納します。

## 操作サンプル
1. **パスの存在を確認**アクティビティをドラッグ:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-1.png)

2. ダブルクリックしてアクティビティの内に入る。パスは手動で入力し、相対と絶対パスをサポートします。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-2.png)

3. パスが存在するかどうかを判断するために変数"exists"を作成。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-3.png)

4. **ログに書き込み**アクティビティ検索してドラッグ：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-4.png)

5. プロセスを実行、"E:\shirley\hello.txt"が存在と判断し、"True"を出力：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-5.png)