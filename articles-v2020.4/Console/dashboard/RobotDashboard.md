# ロボットモニタ
**本機能はエンタープライズ版のみで見られます。**

ロボットモニタページは、今日、最近7日間、最近30日間またはカスタム時間でロボットの運行状況を確認できます。具体的には下図のようになります。

![机器人监控](https://docimages.blob.core.chinacloudapi.cn/images/Console/Dashboard/robotdashboard20201203.png)

| 番号 | 引数 | 説明                                                                        |
| ---- | ------------------------- | ------------------------------------------------------------ |
| 1    | 利用可能なロボットの実行タスクの総数 | 現在のリソースグループ下のすべてのロボットが選択した時間範囲内での実行プロセス数を統計します。 |
| 2    | 利用可能なロボットの忙しい総時間 | 現在のリソースグループ下のすべてのロボットが選択した時間範囲内のビジー合計時間を統計します。（すべてのロボットがビジーであるの累積時間） |
| 3    | 利用可能なロボットの平均ビジー率 | 現在のリソースグループ下のすべてのロボットが選択した時間範囲内の平均ビジー率を統計します。（すべてのロボットの忙しい総時間 / 選択した時間範囲内のすべてのロボットの存在時間）。 |
| 4    | 利用可能なロボットの故障率TOP 10| すべてのプロセスに発生した障害（つまり、失敗）の分布を統計します。 </br> 各ロボットの故障率=現在のロボットが失敗したプロセス数 / この期間に失敗した総プロセス数。例えば、1000個のruninstanceは、その中の100個はAロボットに失敗した場合、10%と計算されます。 |
| 5    | 利用可能なロボットの状態分布 | 現在のリソースグループ下のすべてのロボットが選択した時間範囲内にの状態分布を統計します。ロボットの状態はライセンスされた、ライセンスされていない、切断、ビジー、暇などに分けられます。 |
| 6    | 利用可能なロボットのビジー総時間トップ10 | 現在のリソースグループ下のすべてのロボットの忙しさ（実行プロセス数）と具体的なプロセスパッケージの状況を示します。 |

