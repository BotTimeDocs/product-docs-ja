# 例外をスロー

プロセス実行時に自ら例外をスローすることをサポートします。

## プロパティ
### 基本
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。

### 入力
- **例外** ：スローしたい例外タイプと情報を設定します。

## 操作サンプル
1. **要素が表示されるまて待つ**アクティビティをドラッグ、要素を指定。エラー発生時に実行を継続を"はい"に設定。出力結果変数isTrueを追加する。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Throw-1.png)

2. **プロセス条件分岐**アクティビティをドラッグ、条件にisTrueを入力:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Throw-2.png)

3. **例外をスロー**アクティビティをドラッグ、異常情報`new Exception("要素が見つかりません")`を入力:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Throw-3.png)

4. プロセスを保存して実行をクリックし、実行結果を確認する。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/Throw-4.png)

