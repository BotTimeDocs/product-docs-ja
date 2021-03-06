# 一致する画像を探す

指定された範囲で指定された画像を探して、該当する結果コレクションを返します。画像認識はサポートされていません。


## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。
- **タイムアウト(ミリ秒)** ：このアクティビティの実行時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。マッチングタイムアウト(ミリ秒)が含まれます。この時間を超えたら、アクティビティがまだ実行されていない場合、エラーがスローされます。


### 範囲
- **コントロール要素** ：変数を受信してターゲット要素とします。この項は**セレクタ**と二者択一で入力する必要があります。画像を検索する範囲を指定します。
- **[セレクタ](../Appendix/Selector.md)** ：取得したい特定のUI要素、画像を検索する範囲を示すために使用します。**要素を指定**をクリックすることで自動生成できます。文字列変数と文字列のみをサポートします。
- **検出タイムアウト（ミリ秒）** ：ターゲット要素を検索する時間を限定し、指定時間を超えたら待ちません。この時間を超えて指定された要素が検出されていない場合、エラーがスローされます。単位はミリ秒（ms）で、1000ms = 1sです。整数変数と整数型のみサポートされています。

### 画像
- **画像** ：プロパティ**画像**と**画像パス**両者は互いに排他的であり、かつ必ず1つを記入しなければなりません。この項目はマッチする画像を指します。Image型変数のみをサポートします。
- **画像パス** ：プロパティ**画像**と**画像パス**両者は互いに排他的であり、かつ必ず1つを記入しなければなりません。この項目はマッチする画像を指します。文字列変数と文字列のみをサポートします。
- **正確率** ：画像を探す時の精度

### 出力
- **結果コレクション** ：一致する画像の結果コレクションをこの変数に格納します。このサブコレクションは他のアクティビティのコントロール要素として入力できます。

### 注意点
- 範囲は静止ページに制限されています。スクロールバーがあるページはスクロールして検索しません。

## 操作サンプル
1. **スクリーンショット**アクティビティをドラッグ、出力変数をImageオブジェクト`imgEle`に設定:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/matchImage1.png)

2. **一致する画像を探す**アクティビティをドラッグ、前のステップで戻った画像オブジェクトimgEleを入力、出力に繰り返し可能な要素結果コレクション`images`を入力。
    ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/matchImage2.png)

3. **クリック**アクティビティをドラッグ、前のステップで戻った結果コレクションの最初の要素`images.ToList()[0]`を入力：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/matchImage3.png)

4. プロセスを実行、マッチされた最初の要素をクリックしました。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/matchImage4.png)