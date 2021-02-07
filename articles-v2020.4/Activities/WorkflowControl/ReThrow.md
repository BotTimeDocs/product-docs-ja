# 例外を再スロー

プロセス実行時に例外のオリジン情報を再度スローすることをサポートします。

## プロパティ
### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。。

## 操作サンプル
1. **繰り返し(While)**アクティビティをドラッグ、変数を設定、繰り返し条件を入力し、**例外処理(TryCatch)**をコンテナにドラッグ、下図のようにします。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Rethrow-1.png)

2. ダブルクリックしてエラーキャプチャ(Try Catch)アクティビティを展開し、それぞれ**クリック**と**代入**アクティビティをドラッグ、対応する要素を指定して、変数の増加を設定。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Rethrow-2.png)

3. **例外を再スロー**アクティビティをCatchコンテナにドラッグ、保存して実行プロセスをクリックして実行結果を確認。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Rethrow-3.png)
