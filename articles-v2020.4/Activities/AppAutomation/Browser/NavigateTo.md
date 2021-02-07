# ナビゲート

このアクティビティを使用して、現在のブラウザオブジェクトの範囲内の現在のタブページからジャンプします。ジャンプ後、ブラウザをバインドし直しなくても、新しいページ内の要素を正常に操作できます。クリックなどは新しいページで有効です。

このアクティビティは必ず*ブラウザをバインド*または*ブラウザを開く*アクティビティで使用します。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **実行前の待機時間(ミリ秒)** ：このアクティビティの実行前の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、前のアクティビティの実行が完了したら、一秒後にこのアクティビティを実行するという意味です。
- **実行後の待機時間(ミリ秒)** ：このアクティビティの実行後の待ち時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。ここに1000を記入すると、このアクティビティの実行が完了したら、一秒後に次のアクティビティを実行するという意味です。
- **タイムアウト(ミリ秒)** ：このアクティビティの実行時間を指定します。単位はミリ秒（ms）で、1000ms = 1sです。マッチングタイムアウト(ミリ秒)が含まれます。この時間を超えたら、アクティビティがまだ実行されていない場合、エラーがスローされます。

### オプション

- **ロードが完了するまで待つ** ：チェックすると、操作を実行する前に、ターゲットユーザーインターフェイスの要素のロードが完了するまで待ってから、次のアクティビティ操作を実行します。

### 入力

- **URL** ：このURLを開きます。文字列変数と文字列のみをサポートします。

## 操作サンプル

1. **ブラウザをバインド**アクティビティをプロジェクトプロセスにドラッグ:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/AttacBrowser20201221.png)

2. ダブルクリックして開いて、ブラウザを指定。例：Encoo公式サイト、**ナビゲート**アクティビティをドラッグ、Encoo学院のURLを入力して、下図のようになります。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/NavigateTo20201221.png)

3. 実行をクリックして、実行結果を確認する。Encoo学院のホームページに移動しました。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/NavigateTo2020122102.png)