# マウスの位置を取得
マウスの最終カーソルの位置を取得します。

## プロパティ
### 基本
- **タイムアウト（ミリ秒）** ：最大待機時間を指定します（ミリ秒を単位に）。この時間以降にアクティビティが実行されない場合、システムはエラーをスローします。
- **実行前の待機時間(ミリ秒)** ：アクティビティ操作を実行した後の待ち時間（ミリ秒を単位に）。
- **実行後の待機時間(ミリ秒)** ：アクティビティ操作を実行する前の待ち時間（ミリ秒を単位に）。
- **エラー発生時に実行を継続** ：このアクティビティが実行失敗した場合、エラーを無視して次のアクティビティを実行するかどうかを設定します。プルダウンフレーム選択に"はい"を選択すると、このアクティビティが実行中にエラーが発生した場合、プロセスは次のアクティビティを実行し続け、停止しません。"いいえ"を選択した場合、このアクティビティが実行中にエラーが発生した場合、プロセスは実行を停止し、エラーをスローします。
- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。
### 出力
- **X/Y座標** ：Windowsオペレーティングシステムでは、画面上のすべてのポイントに一意の座標があり、座標は2つの整数で構成されます。1つはx（つまり、横座標）と呼ばれ、もう1つはy（つまり、縦座標）と呼ばれます。

## 操作サンプル
普通は**座標によるクリック**アクティビティと組み合わせして使用する。操作サンプルは[座標クリック](activity/../Coordinate.md)を参照してください。