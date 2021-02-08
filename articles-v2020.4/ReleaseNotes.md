# Encoo製品リリースの説明

> **ヒント：**
>
> コミュニティ版とエンタープライズ版の違いについての説明とオフラインドキュメントのダウンロードについては、[Q&Aページ](QA.md)を参照してください。

## 2021.01.07リリースの説明

2021.01.07 にEncoo RPA がリリースされました。今回リリースされた製品とバージョンは以下となります：
|         | バージョン      |
| -----:  | -----:     |
| コンソール  | 3.0.34008 |

[*Encoo コンソール*](https://console.encoo.com/)で関連製品をダウンロードして体験することができます。

### 機能を追加

#### 【コンソール】

1. コンソールのホームページに携帯自動化（IOSとAndroid）のインストールパッケージを追加しました。
2. ロボット管理ページに、ホスト状態が追加され、ホストされていないロボットは、コンソールのタスクによってスケジュールされません。
3. コンソールのフロントエンドにタイムアウトしたら自動的にシステムからログアウトというシステムメカニズムが追加されました。システムの安全性を向上させます。
4. キューの詳細にタスクリストを追加しました。キュータスクを素早く管理できます。

### 改善と強化

#### 【コンソール】

1. コンソール全体のインターフェーススタイルをアップグレードし、ユーザー体験と視覚効果を高めます。
    - タブを切り替えのスタイルを最適化
    - ポップアップを最適化
    - 二級詳細ページの左リストを最適化
    - 二級詳細ページの全体レイアウトとスタイルを最適化
    - 一部のリストの選択された状態のスタイルがを最適化

2. 英語環境下のシステムのインターフェーススタイルを最適化しました。
3. ダッシュボードのデータ保持方式を最適化しました。
4. ゲートウェイの呼び出しロジックを最適化し、同時性能を向上させました。
5. システムアラームメッセージを最適化しました。
6. システムメール送信テンプレートを最適化しました。

## 2020.12.28 リリース説明

2021.01.07 にEncoo RPA がリリースされました。今回リリースされた製品とバージョンは以下となります：
|         | バージョン      |
| -----:  | -----:     |
| ミニプログラム   | 1.1.1125 |

[*Encoo コンソール*](https://console.encoo.com/)で関連製品をダウンロードして体験することができます。

### 機能を追加

#### 【アプレット】

1. 新たに新しい[データテーブル管理](Apps/devApps/appsedit/TableManagement/TableManage.md)機能を追加:
    - ユーザーがインポートまたは新規作成することにより、ミニプログラムにデータシートを作成することをサポートします。
    - シルキーで使いやすいデータ処理：即時変更の応答、エリアのコピーと貼り付け、ドラッグ&ドロップで上書き、などの方法をサポートして、ユーザーがデータをすばやく変更できるようにします。
    - 強力な数式システム：セルの数式計算とデータ参照をサポートし、シートデータの多様性を作成します。
    - データ可視化操作を構築：複数の列フォーマットをサポート、ユーザーに適した編集形式を定義します。
    - クイック検索：多様なフィルタソート機能を提供し、迅速にデータを整理と分析します。
    - 強力な連携機能：複数のユーザーが同時にシートに対しての修正をサポートし、データの正確な応答とローディングを保証します。
2. より強力なインタラクティブインターフェースを構築します。
    - モジュールアクティビティを追加:[シート](Apps/devApps/appsedit/component/ModuleComponents/Table.md)、[フォーム](Apps/devApps/appsedit/component/ModuleComponents/Form.md)、[説明リスト](Apps/devApps/appsedit/component/ModuleComponents/DescriptionList.md)、[OCR結果の比較](Apps/devApps/appsedit/component/ModuleComponents/CompareOCRResult.md)。
    - アクティビティカスタムページとデータシートのインタラクティブを介して、エンドユーザーが簡単にインタフェースを通じてデータシートを操作することができるようにします。
3. **About Us** ページでミニプログラムシステムのバージョンが表示され、システムバージョンの管理に便利です。
4. EncooフォーラムとEncooアカデミーへのクイックアクセスを追加しました。

### 改善と強化

#### 【アプレット】

1. 全面的にミニプログラムのエディタのインタラクティブのスタイルを最適化して、インタフェースを更にさわやかにして、インタラクションを更に簡潔にします。
2. プログラムインターフェースのエラーメッセージの内容を最適化し、ユーザーがより明確にします。

## 2020.12.24 リリース説明

2020.12.24 にEncoo RPA がリリースされました。今回リリースされた製品とバージョンは以下となります：
|         | バージョン      |
| -----:  | -----:     |
| コンソール   | 3.0.33343 |

[*Encoo コンソール*](https://console.encoo.com/)で関連製品をダウンロードして体験することができます。

### 機能を追加

#### 【コンソール】

1. [キューモニタ](Console/dashboard/QueueDashboard.md)機能を追加、マルチ次元でキュー内のロボット、プロセスタスクの実行スケジュール状況を統計と監視します。
    - キューの数、キュータスク実行の時間、プロセス展開数、ロボットの数、ロボットのビジープロポーションを統計します。
    - キューの成功率TOP 10、キューの故障率TOP 10を統計します。
    - キューのタスク状態分布を統計します。
    - キューの忙しい状況とプロセス実行の状況を示します。
    - キュータスクの平均待ち時間TOP 10を統計します。
2. ユーザーがプロセスタスクをトリガする時に指定されたロボットを修正することをサポートします。ユーザーが実行先をリアルタイムで変更することができます。
3. コンソールのすべてのモジュールに上部エリアと機能ヒントを追加し、ユーザーに機能を理解させながら、システムのスタイルを美化しました。
4. プロセス展開、キューおよびタスクレコードでは、タスク優先度の調整がサポートされており、タスクの実行順序の調整が容易である。
5. プロセス展開する時に、資産管理で定義されたアカウント、パスワード、証明書と引数を使って代入、プロセスを実行することができます。
6. 資産を暗号化APIを新規追加し、アクティビティ側に公開し、呼び出しできます。

### 改善と強化

#### 【コンソール】

1. システム内のユーザー名、個人の名前を統一し、一部の姓名データの同期メカニズムを最適化しました。
2. コンソールメニューバーの全体的なインタラクション、スタイル、アイコンを最適化し、視覚効果を向上させました。
3. コンソールのグローバルリストのスタイル、引き出しの浮き窓のスタイルを最適化し、ユーザーの体験を向上させました。
4. ダッシュボードのデータ統計方式を最適化し、システム性能を向上させました。
5. 英語環境下の画面のスタイルを統一しました。
6. フロントエンドインターフェースが IE 11へのサポート及び適応効果を改善し、ユーザー体験を向上させました。
7. 監査ログ、ダッシュボードの時間照会問題を最適化しました。

## 2020.12.21リリース説明

2020.12.21 にEncoo RPA がリリースされました。今回リリースされた製品とバージョンは以下となります：
|         | バージョン  |
| -----:  | -----:     |
| エディタ   | 1.1.2012.10 |
|ロボット |1.1.2012.10|

[*Encoo コンソール*](https://console.encoo.com/)で関連製品をダウンロードして体験することができます。

### 新規機能

#### 【エディタ】

1. エンタープライズ版は[携帯の自動化](Studio/process/developProject/MobileDevicesManage/Download.md)操作をサポートし、PC端末で携帯電話の各要素を操作できるようにします。
2. [外部プロジェクトを参照](Studio/process/ReferenceProject.md)をサポートします。依存項として、現在のプロセスに使用されます。
3. [バージョンコントロール（プレビュー）](Studio/VersionControl.md)機能の有効化をサポート：ローカルプロジェクトのファイル内容の変更を記録して、指定されたバージョンの修正状況を後で確認できます。
4. インポートファイルをサポートします。他のファイルを現在選択されているフォルダにインポートします。
5. 例外処理に単一のアクティビティを含むことをサポートします。選択された単一のアクティビティを例外処理を使ってTryモジュールに含んで、デバッグを容易にします。
6. [アクティベーション](Studio/quickStart/Activation.md)方式の切り替えをサポート：About usページでコミュニティ版/エンタープライズ版エディタのアクティブ化方式の切り替えをできます。

#### 【アクティビティライブラリ】

1. コードツール > タイプ変換:[テキストを日付と時刻に変換](Activities/CodeExecuter/TypeConversion/TextToDateActivity.md)、[配列をコレクションに変換](Activities/CodeExecuter/TypeConversion/ArrayToCollectionActivity.md)、[コレクションを配列に変換](Activities/CodeExecuter/TypeConversion/CollectionToArrayActivity.md)。
2. システム > スクリーン:[スクリーンをロック](Activities/System/Screen/WindowsLockActivity.md)、[ロックを解除](Activities/System/Screen/WindowsUnlockActivity.md)。パソコンがロックされてもwebの自動化操作や自動ロックを解除をサポートします。
3. コンソール > [ファイルをダウンロード](Activities/Console/FileDownloadActivity.md)：EncooRPAコンソール"データセンター> ファイルサービス"でアップロードされたファイルをダウンロードします。
4. UiAutomation > [マウスをドラッグ](Activities/UIAutomation/DragDrop.md)：マウスを押してドラッグする操作をシミュレートします。例えば、マウスの左ボタンを押してファイルを別のフォルダにドラッグします。
5. アプリケーション自動化 > Office Excel：[列を分ける](Activities/AppAutomation/OfficeExcel/OfficeExcelTextToColumns.md)、[エリアをコピー](Activities/AppAutomation/OfficeExcel/OfficeExcelCopyAndPasteArea.md)。
6. プロセスコントロール > [プロセスを呼び出し（プロジェクトを参照）](Activities/WorkflowControl/InvokeReferencedWorkflow.md)：参照されたプロジェクトプロセスファイルを現在のプロジェクトプロセスに使用されるために、参照されたプロジェクトプロセスファイルの呼び出しを実現します。
7. コードツール > Python:[Pythonをインストール](Activities/CodeExecuter/Python/PythonInstall.md)、[Python環境](Activities/CodeExecuter/Python/PythonScope.md)、[Pythonコードを実行](Activities/CodeExecuter/Python/PythonExcuteFile.md)。

#### 【ロボット】

1. プロセスの[実行中スクリーンショット](Robot/localworkflow.md)をサポートします。運用および保守担当者が異常のトラブルシューティングと追跡を行うと便利です。
2. プロセス実行の[タイムアウト](Robot/localworkflow.md)の防止をサポートします：実行時間が設定された時間を超えた場合はプロセスを終了します。たとえば、"タイムアウト時間は1分"をチェックすると、実行が1分以内に完了する必要があることを意味します。そうしないと、プロセスを終了します。 |

### 改善と強化

#### 【エディタ】

1. **ファイルを開く**、**ディレクトリを開く**、**日付**などの引数タイプが追加されます。プロセスを実行する時、手動入力の代わりに手動で選択し、ユーザー体験を向上させます。
2. **プロジェクトをエクスポート**機能を最適化しました。エクスポートされたアクティビティライブラリは“.egs”を拡張しとします。これは拡張子が".dgs"であるプロセスプロジェクトとは異なります。
3. [市場を管理](Studio/market/Market.md)、[コード市場](Studio/market/NuGetMarket.md)、[アクティビティ市場](Studio/market/activityMarket.md)のインタフェースのスタイルを最適化しました：元のポップアップ形式からラベルのページ形式に最適化しました。
4. プロジェクトをエクスポートと[プロジェクトを公開](Studio/process/PublishProject.md)を最適化しました：依頼関係をプロセスパッケージにエクスポートできます。
5. アクティビティコメントの最適化：アクティビティコメントショートカット**Shift+F2**をサポートします。
6. すべてのファイルを表示することをサポートします。プロジェクトを公開する時にファイルまはフォルダーをプロジェクトから除外できます。

#### 【アクティビティライブラリ】

1. リトライアクティビティを最適化：このアクティビティの**リトライ時間間隔**プロパティのデフォルト値は時間書式（00:00:00）です。ユーザーの入力ミスを避け、ユーザー入力体験を向上させます。
2. [要素のプロパティ値を取得](Activities/UIAutomation/GetElementAttributeValue.md)、[要素のプロパティ値を待つ](Activities/UIAutomation/WaitElementAttributeValue.md)、[プロパティをチェック](Activities/Check/AttributeCheck.md)これらのアクティビティに対しては、カスタムプロパティの取得をサポートします。
3. [セレクタエディタ](Activities/Appendix/Selector.md)はプロパティ値が変数（変数はデフォルト値が必要）である場合、複数の同じ要素の検証をサポートし、ユーザー体験を向上させます。
4. [セレクタエディタ](Activities/Appendix/Selector.md)、[要素検出器](Activities/Appendix/UiDetector.md)のプロパティ値は、定数変数混合入力をサポートし、ユーザーインターフェース要素を識別するために必要なすべての要素をサポートし、適用済みと未適用の状態で分類して展示し、ユーザー体験を向上させます。
5. コードツール> > C# > [C#コードを呼び出し](Activities/codeexcuter/../CodeExecuter/CSharp/ExecuteCSharp.md)：クラス、関数の作成をサポートし、アクティビティの機能を強化します。
6. データベース系列のアクティビティ([SQLを実行](Activities/Database/ExecuteNonQuery.md)、[クエリ](Activities/Database/Select.md)）：実際の状況に応じてタイムアウトを設定でき、異なるアプリケーションシーンを適用することができます。
7. アプリケーション自動化 > Office Excel > [検索](Activities/appautomation/officeexcel/Search.md)：あいまい検索と精確な検索をサポートし、ユーザーにより柔軟で便利な操作体験をもたらします。

#### 【ロボット】

1. プロセスを実行する時の[引数の設定方式](Robot/localworkflow.md)を最適化:**ファイルを開く**、**ディレクトリを開く**、**日付**などの引数タイプが追加されます。プロセスを実行する時、手動入力の代わりに手動で選択し、ユーザー体験を向上させます。
2. 最適化[プロセス市場インターフェース](Robot/ProcessMarket.md)マウスを任意のプロセスにホバーさせると、"実行"ボタンが表示され、ユーザー体験を向上させます。
3. [概要画面](Robot/Overview.md)を最適化：cronジョブと最近の実行プロセスがない場合は、対応ページの関連をサポートし、ユーザーを導き、操作体験を向上させます。

## 2020.12.10リリース説明

2020.12.10 にEncoo RPA がリリースされました。今回リリースされた製品とバージョンは以下となります：
|         | バージョン      |
| -----:  | -----:     |
| コンソール（エンタープライズ版） | 3.0.31848 |

[*Encoo コンソール*](https://console.encoo.com/)で関連製品をダウンロードして体験することができます。

### 新規機能

#### 【コンソール】

1. [ロボットモニタパネル](Console/dashboard/RobotDashboard.md)を追加しました。時間帯をカスタマイズして、対応するロボットの実行状況をクエリすることができます。例えば、ロボットが実行タスクの総数/忙しい総時間/平均ビジー率/故障率TOP 10/状態分布/ビジーTOPなど。
2. [ロボット実行統計表](Console/dashboard/dashboard2.md)を追加しました。時間帯をカスタマイズして、ロボットの実行タスク数、実行成功数、忙しい総時間、多忙時間の長さ、平均ビジー率、平均成功率などの詳細と変化の動きのクエリをサポートします。
3. [ユーザープロセス統計表](Console/dashboard/dashboard3.md)を追加しました。時間帯をカスタマイズして、ユーザーが作成したプロセス展開数、作成したタスクプラン数、対応するタスクの実行状態などの詳細と動向のクエリをサポートします。
4. 共有ロボットを追加しました。各リソースグループのキューとプロセス展開のタスクに対して、共有ロボットを使ってタスクを実行できます。ロボットの利用率を増加します。
5. プロセス展開は、コマンドを配布してロボットの録画を制御することをサポートします。ログの詳細ページはビデオの再生をサポートします。
6. コンソールに埋設ポイントスイッチを追加しました。ユーザーが便利に自由にシステム行動を監視するかどうかを選択できます。
7. 新しい携帯検証API、ユーザーリストAPIをリリースしました。Encooシステム間のデータの流すのに便利です。

### 改善と強化

#### 【コンソール】

1. 登録とログインページのスタイルをアップグレードし、ユーザーのログインと登録体験をアップグレードしました。
2. システムのサービスエンドのエラー処理とフロントエンドのユーザーのヒントを最適化しました。
3. システム部分のページの空きデータまたはアクセス権限のないの表示方式を最適化しました。
4. セキュリティ問題を修復し、システムの安全性を向上させます。例えば、アカウントのパスワードチェック規則の制限、失敗のロックなど。
5. 英語版のシステムの部分的のスタイルと文言を最適化しました。

## 2020.11.26リリース説明

2020.11.26 にEncoo RPA がリリースされました。今回リリースされた製品とバージョンは以下となります：
|         | バージョン  |
| -----:  | -----:     |
| エディタ   　　| 1.1.2011.12 |
| ロボット   　　| 1.1.2011.12 |
| コンソール   　| 3.0.30440 |
| ミニプログラム | V1.0.1|

[*Encoo コンソール*](https://console.encoo.com/)で関連製品をダウンロードして体験することができます。

### 新規機能

#### 【エディタ】

1. プロセスを[EXCELにエクスポート](Studio/Introduction/TheUserInterface.md)する機能をサポートします：プロセス編集エリアにあるコンテナ内のアクティビティ（プロセスチャート/シーケンス/ステータスマシン）の空白を右クリックし、ポップアップされたコンテキストメニューから"EXCELにエクスポート"を選択し、XAMLファイルの内容をExcelにエクスポートすることができます。業務員がプロセス構造を手軽に確認できます。
2. "開始 > 開く > ローカルプロジェクト"のリストの上に、"更新"ボタンを追加しました。手動でローカルプロジェクトリストを更新でき、現在のパスの下のプロジェクトフォルダをリロードすることを実現します。
3. "開始 > ヘルプ"ページでは、AI HUB実用リンクを追加しました。ユーザーがAI HUB製品をよりよく理解することに役に立ちます。
4. "新規 > テンプレートから作成"リストに、モジュール化された"[エンタープライズプロセステンプレート](Studio/process/ProjectTemplates.md)"を追加しました。より多くのテンプレートの表示をサポートします。
5. 界面自動化アーキテクチャを調整し、安定性を増強しました。

#### 【アクティビティライブラリ】

1. システム > [日付と時間の選択ボックス](Activities/System/TimePickerDialogActivity.md)アクティビティ：プロセスの実行中、ポップアップウィンドウでが表示され、ユーザーが日付と時刻を選択して出力することができます。
2. AI Hubシリーズアクティビティ：[証明書の識別](Activities/AIHub/IdentificationOfCredentials.md)、[ビル識別](Activities/AIHub/BillIdentification.md)、[共通文字認識](Activities/AIHub/GeneralCharacterRecognition.md)。
3. コードツール > テキスト処理 > [GUIDを生成](Activities/CodeExecuter/TextProcessing/GenerateGUIDActivity.md)アクティビティは、新しいGUIDを生成します。
4. ワークプロセス > [プロセスを終了](Activities/WorkflowControl/Abort.md)アクティビティは、このアクティビティを実行するとすぐに現在のプロセスを終了し、後続のプロセスを実行しないことを実現します。
5. UiAutomation > [座標によるクリック](Activities/UIAutomation/Coordinate.md)アクティビティ：絶対座標に従って、指定されたユーザーインターフェイス要素をクリックします。
6. UiAutomation > [マウスを移動](Activities/UIAutomation/MoveMouse.md)アクティビティ：マウスカーソルの位置を移動します。
7. UiAutomation > [マウスの位置を取得](Activities/UIAutomation/GetMousePosition.md)アクティビティト：マウスの最終カーソル位置を取得します。
8. UiAutomation > 画面テキスト化シリーズアクティビティ（エンタープライズ版）：[画面上のテキストを取得](Activities/UIAutomation/ScreenText/GetScreenText.md)、[画面上にテキストを含む要素を取得](Activities/UIAutomation/ScreenText/GetTextElement.md)、[テキストが画面に存在するかを判断](Activities/UIAutomation/ScreenText/IdentifyScreenTextExist.md)、[画面上のテキストをクリック](Activities/UIAutomation/ScreenText/ClickScreenText.md)。

#### 【ロボット】

1. 新規スケジューラーでを作成する時、[Cron式で](Robot/CronJob.md)スケジューラーを設定することをサポートし、ユーザーがスケジューラーをカスタマイズするシーンを満たします。


#### 【コンソール】

1. データセンターに[ファイルサービス](Console/datacentor/fileservice/Aboutfileservice.md)機能を追加しました。フォルダの追加・削除・編集、ファイルのアップロード、ダウンロードなどの操作をサポートします。同時にRPAプロセスに各種のファイルサービスを提供します。
2. [文書理解](Console/docreader/aboutDocreader.md)サービスでは、OCR抽出モデルを追加し、アクティビティを通じて現在のテンプレートサービスを呼び出すことで、RPAプロセスが非構造テキスト情報を大量に抽出することができます。
3. [ライセンス](Console/management/license/aboutLicense.md)ページで文書理解の回数を追加しました。文書理解のテンプレートの呼び出し回数を制御します。

#### 【ミニプログラム】

1. [タスクレコード](Apps/devApps/appsedit/component/workflowlog.md)アクティビティは、タスクレコードリストを介してタスク情報、現在のステータス、ログなどの情報を確認することができます。

### 改善と強化

#### 【エディタ】

1. 検索アクティビティの機能を最適化しました。アクティビティパネルでは、アクティビティ名のピンインの頭文字でアクティビティ名をぼかして検索することができます。ユーザーエクスペリエンスを向上させます。
2. 公開ウィンドウを最適化しました。公開ウィンドウにプロジェクトのプロパティ情報を追加しました。例えば、プロジェクト名、最新バージョンなど、ユーザーがプロセスを発表する時にもっと明確にこのプロジェクトの基本情報を確認できます。
3. 式エディタの入力体験を最適化しました。アクティビティプロパティボックスにコードを書くと、自動的に後の括弧を補完します。例えば、xx.ToString—>xx.ToString()。
4. セレクタエディタを最適化しました。セレクタエディタのノードプロパティリストにURLプロパティが追加されました。ページTitleが設定されていない場合は、URLを使ってページを特定します。
5. セレクタエディタを最適化しました。セレクタエディタノードプロパティリストでは、AutomationId/ClassName/Nameの値はワイルドカードをサポートします。

#### 【アクティビティライブラリ】

1. 検証 > [値をチェック](Activities/Check/ValueCheck.md)アクティビティを最適化しました。"開始/終了"のチェック条件を追加し、文字列が指定された文字列の文字で開始および終了するかどうかを確認します。。
2. システム > ファイル > [ファイル/フォルダを作成](Activities/System/File/NewFileOrFolder.md)アクティビティを最適化しました。"ファイルを上書き"オプションプロパティを追加し、新規ファイル/フォルダを作成する時、同名の場合は上書き置換します。
3. 検証 > [プロパティをチェック](Activities/Check/AttributeCheck.md)アクティビティを最適化しました。プロパティをチェックアクティビティのプロパティ名プルダウンボックスには、現在の要素がサポートされているプロパティのみが表示されます。
4. アプリケーション自動化 > ブラウザシリーズのアクティビティ： [ブラウザを開く](Activities/AppAutomation/Browser/OpenBrowser.md)、[ナビゲート](Activities/AppAutomation/Browser/NavigateTo.md)、[ブラウザーをリフレッシュ](Activities/AppAutomation/Browser/RefreshBrowser.md)に"ロードが完了するまで待つ"というオプションプロパティが追加されています。ページ全体のロードが完了したこそアクティビティの実行が成功とします。
5. UiAutomation > [アイテムを選択](Activities/UIAutomation/SelectItem.md)アクティビティを最適化しました。プロジェクトテキスト入力ボックスはプルダウンフレームに最適化され、他の同じシリーズのアクティビティと一致します。
6. 要素のプロパティ値を取得、要素のプロパティ値を待つ、プロパティをチェックアクティビティを最適化し、識別能力を向上させます。

#### 【ロボット】

1. 実行中のプロセスを停止する操作を最適化しました。ホットキーのShift+F5を押して、現在実行中のプロセスを終了することをサポートします。便利ですばやいです。
2. インストール後の体験を最適化しました。アクティブにしないでプロセス市場などの機能を利用できます。
3. ロボットのAboutページを最適化しました。エンタープライズ版のユーザーがローカルアクティブにした後、このページでライセンスの有効期限を確認できます。

#### 【ミニプログラム】

1. ロゴを最適化し、製品名を変更しました。元のワークベンチ/アプリケーションは、ミニプログラムに変更されました。

### 修復した問題

#### 【アクティビティライブラリ】

1. クリックアクティビティを修復しました。元素を指定する時、F2を押して操作を遅延すると、再度指定要素をクリックすることができません。異常が発生しないようにします。

## 2020.10.19 リリースの説明

2020.10.19にEncooエディタがリリースされました。今回リリースされた製品のバージョンは以下となります：
|         | バージョン      |
| -----:  | -----:     |
| エディタ | 1.1.2010.17 |
| ロボット | 1.1.2010.17 |

[*Encoo コンソール*](https://console.encoo.com/)で関連製品をダウンロードして体験することができます。

### 新規機能

#### 【エディタ】

1. [アクティビティライブラリを作成](./Studio/process/CreateLibrary.md)が追加されました。複数の繰り返し使用可能なプロセスをパッケージ化します。
2. テンプレートから自動化プロジェクトの新規作成をサポートします。
3. コンソールのプロセスの表示と編集をサポートします。
4. プロジェクト編集操作を追加しました。(フォルダ作成/プロジェクトプロパティ設定/ステータスマシンファイルを追加)
5. デバッグ状態では無視、再試行、再起動をサポートします。
6. ショートカットキー Ctrl + E がサポートされ、式エディターをすばやく開くことができます。
7. Homepageビューを追加しました。

### 【アクティビティ】

1. **アプリケーション自動化 > PDF** ：[PDFファイルをマージ](Activities/AppAutomation/PDF/MergePDF.md)、[PDFを新規ファイルに抽出](Activities/AppAutomation/PDF/ExtractToNewFile.md)、[PDFのページ数を取得](Activities/AppAutomation/PDF/GetPageNumbers.md)、[PDF中の画像を取得](Activities/AppAutomation/PDF/ExtractImages.md)、[PDFのテキストを取得](Activities/AppAutomation/PDF/ExtractText.md)
2. **システム > ファイル > [ファイル/フォルダの名前を変更](Activities/System/File/RenameFileOrFolder.md)**
3. **システム > [パスワードを入力](Activities/System/InputPasswordDialogActivity.md)**
4. **コンソール > [文書理解](Activities/Console/DocReader.md)** ：組み込みの文書理解アクティビティは、文書理解サービスがコンソールにデプロイされている限り、文書理解機能を使用できます。
5. **コンソール > [資産を取得](Activities/Console/GetAssets.md)** ：プロセスで資産を取得アクティビティを直接使用して、コンソールに保存されているデータアセットを取得できます。
6. **コードツール > 配列処理** ：[配列を初期化](Activities/CodeExecuter/数组处理/InitializeArrayActivity.md)、[要素存在の有無](Activities/CodeExecuter/数组处理/ExistsInArrayActivity.md)、[配列の長さを取得](Activities/CodeExecuter/数组处理/GetLengthOfArrayActivity.md)
7. **コードツール > HTTP > [ファイルをダウンロード](Activities/CodeExecuter/HTTP/HTTPDownload.md)**

### 【ロボット】

1. [タスクスケジューラ](Robot/CronJob.md)を追加しました。もともとコンソールで購入する必要があった機能は、ロボットで実行できます。
2. [Encooプロセス市場](Robot/ProcessMarket.md)におけるプロセスの取得と実行をサポートします。

### 改善と強化

#### 【エディタ】

1. **スタートメニューページ**の**プロセス市場**、**アクティビティ市場**などのアプリケーションの入り口の位置を最適化しました。

#### 【アクティビティ】

1. **トリガー > [ファイルトリガー](Activities/Triggers/FileTrigger.md)** ：モニタを出力するファイルのパスを追加しました。
2. **トリガー > メールトリガー（IMAP）** ：[メールトリガー（IMAP）](Activities/Triggers/IMAPTrigger.md)、[邮件触发器(Outlook)](Activities/Triggers/OutlookTrigger.md)和[メールトリガー（Exchange）](Activities/Triggers/ExchangeTrigger.md) モニタを新しいメールに出力を追加しました。
3. **アプリケーション自動化 > Office Excel > [最後列の番号を取得](Activities/AppAutomation/OfficeExcel/GetLastColumn.md)** ：アルファベットと数字列番号の出力を追加しました。

## 2020.09.27リリースの説明

2020.09.27にEncooエディタ、ロボット、ワークベンチがリリースされました。今回リリースされた製品のバージョンは以下となります：

|               | バージョン      |
| -----:        | -----:     |
| エディタ  　　 | 1.1.2009.11 |
| ロボット   　　| 1.1.2009.11 |
| ワークベンチ   | V1.0.0 |

[*Encoo コンソール*](https://console.encoo.com/)でエディタとロボットをダウンロードして体験することができます。ワークベンチ製品の試用も申し込みできます。

### 新規機能

#### 【エディタ】

1. Microsoft Edgeをサポートします。Edgeの操作を自動化する前に、[Microsoft Edge拡張機能](Studio\Extensions\EdgeExtension.md)をインストールしてください。
2. **セレクタエディタ**は XPath 機能を追加しました。要素はXPathの形式で表示できます。[セレクター](Activities\Appendix\Selector.md)をご参照ください。
3. **IEフロントエンドログコレクタプログラム**を追加しました。このアプリケーションを使用して、IEで完成したRPAプロセスをデバッグし、デバッグログを取得します。[IEフロントエンドログを収集するツール](Activities\Appendix\IELog.md)をご参照ください。

#### 【アクティビティ】

1. **トリガー > [ファイルトリガー](Activities/Triggers/FileTrigger.md)** ：指定されたフォルダー内のファイルの変更を監視し、特定のトリガー条件を設定し、プロセスを自動的に実行するために使用されます。
1. **トリガー > [メールトリガー(Outlook)](Activities/Triggers/OutlookTrigger.md)** ：Outlookメールボックスが新しいメールを受信するイベントを監視し、特定のトリガー条件を設定し、条件が満たされたときにプロセスを自動的に実行するために使用されます。
1. **トリガー > [メールトリガー（Exchange）](Activities/Triggers/ExchangeTrigger.md)** ：Exchangeメールボックスが新しいメールを受信するイベントを監視し、特定のトリガー条件を設定し、条件が満たされたときにプロセスを自動的に実行するために使用されます。
1. **トリガー > [メールトリガー（IMAP）](Activities/Triggers/IMAPTrigger.md)** ： IMAP プロトコルをサポートするメールボックスが新しいメールを受信するイベントを監視し、特定のトリガー条件を設定し、条件が満たされたときにプロセスを自動的に実行するために使用されます。
2. **コードツール  > JSON > [JSON - オブジェクトのシリアル化](Activities/CodeExecuter/JSON/SerializeObject.md)** ：.NETオブジェクトをJSON文字列にシリアル化できます。
3. **コードツール  > JSON > [JSON - オブジェクトの逆シリアル化](Activities/CodeExecuter/JSON/DeserializeObject.md)** ：JSON文字列を.NETオブジェクトに逆シリアル化できます。
4. **アプリケーション自動化 > [Excel - ピボットテーブルを更新](Activities/AppAutomation/OfficeExcel/RefreshPivotTable.md)** ：指定したピボットテーブルのデータを更新します。
5. **アプリケーション自動化 > [Excel - ピボットテーブルを作成](Activities/AppAutomation/OfficeExcel/CreatePivotTable.md)** ：Excelでピボットテーブルを作成します。
6. **コードツール  > HTTP > [HTTP - HTTP要求](Activities/CodeExecuter/HTTP/HTTPRequest.md)** ：HTTP要求を送信して応答データを返すことを実現し、構成されたHTTP要求が使用可能かどうかのテストもサポートします。

#### 【ミニプログラム】

Appsの詳細については、[Encooワークベンチについて](Apps/aboutApps.md)をご参照ください。

1. アプリ内で複数のページジャンプをサポートするために、上部ナビゲーションと左側のナビゲーションアクティビティを追加しました。
2. プロセスアクティビティを追加し、ワンクリックでコンソールのプロセスの実行をサポートします。
3. アプリケーションのバージョン管理をサポートし、コンソールはアプリケーションのオンラインとオフラインとバージョン管理を統一に行います。
4. **自分のアプリケーション**を検索して実行することをサポートします。

#### 【コンソール】

1. コンソールの全体的な構造をアップグレードし、RPAスケジューリング機能を強化しました。オンラインクラウド版と私有化版がリリースされました。サポート機能は次を含みます。[キュー](Console/queue/aboutqueue.md)、[タスクレコード](Console/job/aboutJob.md)、 [文書理解](Console/docreader/aboutDocreader.md)、[資産管理](Console/asset/AboutAsset.md)。

### 改善と強化

#### 【エディタ】

1. インストール/アップグレード体験を最適化し、インストールフレームを変更しました。アンチウイルスソフトウェアによって引き起こされるインストール失敗の問題を解決しました。
2. 管理者以外の権限でエディターを実行するときは、要素認識時に外層ウィンドウをハイライトし、クリック時にヒントを与えます。
3. セレクタエディタについては、JavaアプリケーションのNameプロパティのすべての階層はワイルドカードをサポートします。
4. セレクタエディタの画面を最適化しました。
5. UiAutomationアクティビティはすぐプロセスを終了することをサポートします。

#### 【アクティビティ】

1. UiAutomationの下のすべてのアクティビティにタイムアウトのプロパティを追加しました。
2. **OCRテキストを含む要素を取得**、**OCRテキストが存在するかを判断**アクティビティのテキストプロパティは正規表現をサポートします。
3. DingDingプログラム内の要素の識別を最適化しました。録画技術UIAはほとんどの要素を識別できます。

#### 【ロボット】

1. インストール・アップグレードの体験を最適化しました。

## 2020.08.31リリースの説明

2020.08.31にEncooエディタ、ロボットがリリースされました。今回リリースされた製品のバージョンは以下となります：

|         | バージョン      |
| -----:  | -----:     |
| エディタ | 1.1.2008.12 |
| ロボット | 1.1.2008.12 |

[*Encoo コンソール*](https://console.encoo.com/)で関連製品をダウンロードして体験することができます。

### 新規機能

#### 【エディタ】

1. **アウトライン**をサポートして、現在のプロセスの構造を表示し、アクティビティをすばやく見つけることができます。
2. カーソルをプロパティ入力ボックスに置くと、マウスの右クリックで**式エディター**メニューをすばやく開くでき、変数、引数ー、または式を操作できます。
3. グローバルショートカット**Ctrl+Alt+F5**を追加しました。エディタを最小化してバックグラウンドで動作させた場合、プロセスの実行を停止することもできます。
4. デバッグの一時停止は、いつでもデバッグプロセスをすばやく一時停止できます。 一時停止すると、デバッグ中のアクティビティがハイライトで表示されます。

#### 【アクティビティ】

1. **システム > [プロンプトボックス](Activities/System/PromptBox.md)** ：Windowsデスクトップの右下隅にプロセスで必要なプロンプト情報を表示するために使用されます。
2. **アプリケーション自動化 > Office Excel > [パスワードをリセット](Activities/AppAutomation/OfficeExcel/OfficeExcelResetPassword.md)** ：**Excelを開く/新規作成**アクティビティで使用して、Excelファイルにパスワードを追加、更新、またはクリアします。

#### 【ロボット】

1. **設定**ページで[Aboutページ](Robot/Settings/About.md)を追加しました。ソフトウェアのバージョン、ライセンスの有効期間を表示し、アクティベーション方法を変更できます。
2. [実行中](Robot/RunningProcess.md)ページが追加されました。実行中のプロセスに関する情報が表示されます。
3. プロセス実行時には、権限設定をサポートします。具体的な機能は[プロセスライブラリ](Robot/localworkflow.md)を参照してください。

### 改善と強化

#### 【エディタ】

1. プロジェクト開くのスピードを以前よりも速く最適化し、ユーザーエクスペリエンスを向上させます。
2. アクティビティをコピーして貼り付けのスピードを前よりも速く最適化し、ユーザーエクスペリエンスを向上させます。
3. プロジェクトの操作中またはデバッグ中に、出力パネルは現在のプロセスを提示し、ユーザーに現在実行プロセスについてより明確にします。

## 2020.08.13リリースの説明

2020.08.13にEncooエディタ、ロボットがリリースされました。今回リリースされた製品のバージョンは以下となります：

|         | バージョン      |
| -----:  | -----:     |
| エディタ | 1.1.2008.5 |
| ロボット | 1.1.2008.5 |

[*Encoo コンソール*](https://console.encoo.com/)で関連製品をダウンロードして体験することができます。

### 新規機能

#### 【エディタ】

1. プロセスの編集中に、アクティビティを右クリックして、アクティビティを無効にするか有効にするかを選択できます。 実行中またはデバッグ時に、無効にされたアクティビティは無視されて実行されます。
2. **意見フィードバック**ボタンが追加され、迅速に助けを求めることができます。
3. 出力パネルには出力情報を分類でフィルターできます。**エラー**、**情報**、**デバッグ**の三つの種類を含みます。カテゴリ別にログ情報を表示するために使用されます。

#### 【アクティビティ】

1. **UiAutomation > [一致する画像を探す](Activities/UIAutomation/MatchImage.md)** ：指定された範囲で指定された画像を見つけて、一致する結果セットを返します。
2. **UiAutomation > [フォーカスを設定](Activities/UIAutomation/SetFocus.md)** ：指定された要素のフォーカスを設定します。デスクトップとブラウザをサポートします。
3. **UiAutomation > [複数のアイテムを選択](Activities/UIAutomation/SelectMultipleItems.md)** ：複数のアイテムを同時に選択できます。このアクティビティは、元のページが複数の選択をサポートしている場合にのみ有効になります。
4. **UiAutomation > [ハイライト](Activities/UIAutomation/Highlight.md)** ：指定された要素をハイライトで表示します。色と時間を選択できます。
5. **UiAutomation > [要素のプロパティ値を待つ](Activities/UIAutomation/WaitElementAttributeValue.md)** ：指定された要素のプロパティ値が指定された値になるまで待ってから次のアクティビティを実行します。そうでない場合は、タイムアウト範囲中にずっと待機します。
6. **UiAutomation > [要素のプロパティ値を取得](Activities/UIAutomation/GetElementAttributeValue.md)** ：指定された要素のプロパティ値を取得し、それを出力変数のプロパティ値に格納します。
7. **UiAutomation > OCR > [OCRテキストを取得](Activities/UIAutomation/OCR/GetOCRText.md)（企エンタープライズ版）** ：指定された要素または画像に対してOCRを実行し、結果を返します。
8. **UiAutomation > OCR > [OCRテキストを含む要素を取得](Activities/UIAutomation/OCR/GetSpecificTextOCRElement.md)（企エンタープライズ版）** ：指定された要素または画像に対してOCRを実行し、指定されたテキストを含む要素を見つけて、出力プロパティOCR要素に格納します。
9. **UiAutomation > OCR > [OCRテキストが存在するかを判断](Activities/UIAutomation/OCR/IdentifyOCRTextExist.md)（企エンタープライズ版）** ：指定された要素または画像に対してOCRを実行し、指定されたテキストが存在するかどうかを判別して、結果を出力プロパティOCR要素に格納します。
10. **アプリケーション自動化 > 邮件** ：[メールを取得（Exchange）](Activities/AppAutomation/Mail/GetExchangeMail.md)、[メールを送信（Exchange）](Activities/AppAutomation/Mail/SendExchangeMail.md)
11. **コードツール > テキスト処理** ： [テキストを確認](Activities/CodeExecuter/TextProcessing/VerifyTextActivity.md)、[テキストを抽出](Activities/CodeExecuter/TextProcessing/ExtractTextActivity.md)、[テキストを置き換え](Activities/CodeExecuter/TextProcessing/ReplaceTextActivity.md)、[文字列を切り出し](Activities/CodeExecuter/TextProcessing/GetSubstringActivity.md)、[テキストの長さを取得](Activities/CodeExecuter/TextProcessing/GetLengthOfTextActivity.md)、[テキストのインデックスを取得](Activities/CodeExecuter/TextProcessing/GetIndexOfTextActivity.md)
12. **ワークプロセス > [複数代入](Activities/WorkflowControl/MultipleAssign.md)**
13. **アプリケーション自動化 > Office Excel > [Office Excel->画像を挿入](Activities/AppAutomation/OfficeExcel/InsertPicture.md)** ：指定したセルに画像を挿入します。
14. **ワークプロセス > 判断 > [条件（Switch）](Activities/WorkflowControl/Determine/Switch.md)** ：C＃式を指定し、各ケースに応じて判断して、条件に会うプロセスを実行します。
15. **システム > ファイル > [繰り返し(各ファイル)](Activities/System/File/ForeachFolder.md)**
16. **コードツール > コレクション処理** ：[コレクションに存在の有無](Activities/CodeExecuter/CollectionProcessing/ExistsInCollectionActivity.md)、[コレクションに追加](Activities/CodeExecuter/CollectionProcessing/AddToCollectionActivity.md)、[コレクションをクリア](Activities/CodeExecuter/CollectionProcessing/ClearCollectionActivity.md)、[コレクションから削除](Activities/CodeExecuter/CollectionProcessing/RemoveFromCollectionActivity.md)、[コレクションの長さを取得](Activities/CodeExecuter/CollectionProcessing/GetLengthOfCollectionActivity.md)、[コレクションを初期化](Activities/CodeExecuter/CollectionProcessing/InitializeCollectionActivity.md)

#### 【ロボット】

1. ロボット[概要ページ](Robot/Overview.md)を追加しました。現在のロボットのグローバルデータを表示できます。
1. [プロセス実行履歴ページ](Robot/ProcessHistory.md)を追加しました。プロセス実行の履歴を表示できます。
1. **設定 > 基本**ページを追加しました。[ログとビデオファイルの保留時間を設定](Robot/Settings/Basic.md)できます。

### 改善と強化

#### 【エディタ】

1. プロジェクトを公開する前に、プロジェクトの正確性をチェックします。
2. 一部のポップアップウィンドウをプロセスティングウィンドウに変更しました。ユーザー体験を向上させます。

#### 【アクティビティ】

[プロセスを呼び出し](Activities/WorkflowControl/InvokeWorkflow.md)アクティビティの体験を向上させ、**引数をインポート**をクリックすると直接サブプロセスの引数を導入することができます。

#### 【自動化ドライバ】

1. NCへのサポートを強化しました。
2. EAS中、レポートタイプ画面で**構造化データを取得**を使ってレポートデータを取得できます。
3. 画像認識モードで、**要素が表示されるまて待つ**アクティビティが返したコントロール要素はアンカーではなく、画像です。
4. IEブラウザにインサートされた要素の識別をサポートします。
5. 360のセキュリティブラウザ互換モードにおける要素の識別をサポートします。
6. ブラウザ側は**画像認識**機能をサポートします。
7. デスクトップアプリケーションに対して、**テキストを入力する**アクティビティは**テキストをクリア**操作をサポートします。
8. **範囲テキストを取得**アクティビティ名は**JSON構造を取得**に変更されました。（エンタープライズ版）
9. **ホバー**アクティビティテは画像認識をサポートします。

## 2020.07.17リリースの説明

2020.07.17にEncooエディタ、ロボットのコミュニティ版がリリースされました。今回リリースされた製品のバージョンは以下となります：

|         | バージョン      |
| -----:  | -----:     |
| エディタ   | 1.1.2007.29 |
| ロボット   | 1.1.2007.29 |

Encoo コンソール -> [*インストールパッケージをダウンロード*](https://console.encoo.com/#/download)で関連製品をダウンロードして体験することができます。

### 新規機能

#### 【エディタ】

1. 式エディターで変数名を選択し、**Ctrl+B**ショートカットを使用して変数をすばやく作成することをサポートします。
2. 複数のxamlファイルを含む複雑なプロセスの場合、[ファイルをデバッグ・実行](Studio\process\Debugging\partialDebug.mdを介して単独なデバッグをサポートします。
3. エディタを使って直接自動化プロジェクトをローカルロボットに公開することができます。
4. エディタの右下にプロセスティングウィンドウ通知をサポートします。エディタの更新と一部のプロジェクト操作のフィードバックに対して提示し、ポップアップ通知によって引き起こされる干渉率を減らし、ユーザーエクスペリエンスを向上させます。
5. NuGetを統合し、NuGetアプリケーションを簡単に参照することができます。
6. UIDetectorを使って要素を選択することをサポートします。これまでのセレクターエディタより機能が強いです。この機能はエンタープライズ版のみでサポートされています。[UIDetector](Activities/Appendix/UiDetector.md)を参照してください。
7. プロジェクト設定では、アクティビティの遅延とタイムアウトのプロパティの設定をサポートし、デフォルトのブラウザプロパティの設定をサポートします。[プロジェクト設定](Studio/process/ProjectSettings.md)を参照してください。

#### 【アクティビティ】

1. **ワークプロセス >  [ステートマシン](Activities/WorkflowControl/StateMachine/StateMachine.md)** ：ステートマシンパラダイムに基づくプロセス
2. **コードツール > データ処理 > [データを書式化](Activities/CodeExecuter/DataProcessing/FormatData.md)** ：数値、日時、通貨、パーセンテージに従って入力データをフォーマットします。
3. **ワークプロセス** ：[リトライ](Activities/WorkflowControl/Retry.md)、[例外をスロー](Activities/WorkflowControl/Throw.md)、[例外を再スロー](Activities/WorkflowControl/ReThrow.md)
4. **システム > [プルダウンリストボックス](Activities/System/DropdownListDialog.md)** ：プルダウン選択ボックス形式のユーザーインタラクションインターフェイスは、プロセス中に簡単にポップアップできます。
5. **データテーブル > [CSVファイルに追加](Activities/DataTable/AppendToCSV.md)** ：データテーブルを既存のCSVファイルに追加します。
6. **アプリケーション自動化 > メール**[メールを取得（Outlook）](Activities/AppAutomation/Mail/GetOutlookMail.md)、[メールを送信（Outlook）](Activities/AppAutomation/Mail/SendOutlookMail.md)
7. **UiAutomation > デスクトップコントロールエ専用** ：[フォーカスコントロールを取得](Activities/UIAutomation/DesktopOnly/GetFocus.md)、[コントロールをスイッチ](Activities/UIAutomation/DesktopOnly/SwitchControl.md)この二つのアクティビティはエンタープライズ版のみでサポートされます。

### 改善と強化

#### 【エディタ】

1. シーケンスかローチャートをサブプロセスとして追加することをサポートします。
2. プロジェクトをエクスポートするとき、エクスポート後所在のフォルダを開くかを選択できます。
3. プロジェクトをエクスポートするとき、エクスポート後すぐこのプロジェクトを開くかを選択できます。
4. プロジェクト名とプロセスパッケージ名の命名ルールが統一され、プロセスの公開時に名前の検証が失敗するのを防ぎます。
5. Java拡張機能をサポートします。Java拡張機能を使って、本来は認識できないデスクトップJavaアプリケーションの要素を識別することができます

#### 【アクティビティ】

1. [メールを送信（SMTP）](Activities/AppAutomation/Mail/SendMailSMTP.md)、[メールを取得（IMAP）](Activities/AppAutomation/Mail/GetMailIMAP.md)、[メールを取得（POP3）](Activities/AppAutomation/Mail/GetMailPOP3.md)アクティビティは手動で安全方法を選択することができます。
2. [メールを取得（IMAP）](Activities/AppAutomation/Mail/GetMailIMAP.md)アクティビティは未読メールだけを取得をサポートします。

## 2020.06.16リリースの説明

2020.06.16にEncooエディタ、ロボットのコミュニティ版がリリースされました。今回リリースされた製品のバージョンは以下となります：

|         | バージョン      |
| -----:  | -----:     |
| エディタ | 1.1.2006.16 |
| ロボット | 1.1.2006.16 |

Encoo コンソール -> [*インストールパッケージをダウンロード*](https://console.encoo.com/#/download)で関連製品をダウンロードして体験することができます。

### 新規機能

### 【エディタ】

1. デバッグプロセス中に、[変数パネル](Studio\process\Debugging\ValuePanel.md)で現在のアクティビティの各変数のタイプと値を表示できます。これでプロセスが正しく実行されているかどうかを判断でき、プロセスエラーを見つけるのに役立ちます。 プロセスエラーの位置を特定するのにも役立ちます。
2. 新規プロジェクトを作成する場合は、デスクトップ録画技術 UIA/UIA3の選択をサポートします。
3. インポートリストで、使用されないまたはエラーの[名前空間](Studio\process\developProject\ImportNamespaces.md)の削除をサポートします。
4. 実行時にエディタのメイン画面を最小にするかの設定をサポートします。インターフェイス自動化プロジェクトの実行への干渉率を減らします。
5. より多くのショートカットキーをサポートします。詳細は[キーボードショートカットキー](Studio/quickStart/KeyboardShortcuts.md)を参照してください。
6. UiAutomation > 360セキュリティブラウザをサポートします。

### 【アクティビティ】

1. **UiAutomation > SAP** ：[SAPにログイン](Activities/UIAutomation/SAP/SAP_Login.md)、[ステータスバーを読み取り](Activities/UIAutomation/SAP/SAP_GetStatus.md)、[日付を選択](Activities/UIAutomation/SAP/SAP_SelectCalendar.md)、[SAP項目を選択](Activities/UIAutomation/SAP/SAP_Select.md)、[トランザクションを呼び出し](Activities/UIAutomation/SAP/SAP_Transaction.md)、エンタープライズ版エディタにSAP関連のアクティビティが含まれています。
2. **UiAutomation > [スクリーンショット](Activities/UIAutomation/Screenshot.md)**
3. **システム > [日付と時刻を設定](Activities/System/SetDateTime.md)** ：日付と時刻を指定し、DateTimeタイプの結果を出力します。
4. **システム** ：[ファイルを選択](Activities/System/File/SelectFile.md)、[フォルダーを選択](Activities/System/File/SelectFolder.md)
5. **アプリケーション自動化 > Office Excel > [セルのフォントの色を設定](Activities/AppAutomation/OfficeExcel/SetTextColor.md)** ：カラー設定エクスペリエンスを向上させます。

#### 【ロボット】

ローカルプロセスを実行する時、プロセス引数の記入をサポートします。[ローカルプロセスを実行](Robot/localworkflow.md)を参照してください。

### 改善と強化

#### 【エディタ】

1. 出力パネルの改造などの画面最適化をしました。
2. より詳細な項目のオープンとコンパイルエラーの説明を提供します。エラーの位置をより容易に位置づけられます。

#### 【アクティビティ】

1. **アプリケーション自動化 > Office Excel > [ソート](Activities/AppAutomation/OfficeExcel/Sort.md)**アクティビティを最適化しました。開始行番号の指定をサポートします。
1. **アプリケーション自動化 > Office Excel > [セルの背景色を設定](Activities/AppAutomation/OfficeExcel/SetCellBackcolor.md)**アクティビティを最適化しました。カラーピッカーをサポートし、カラー設定エクスペリエンスを向上させます。

#### 【自動化シーン】

1. 用友 NC と金蝶EASへのサポートを強化しました。
2. UIA3 がWeChatに対すの識別を強化しました。テキストを取得してまたはアイテムを選択するときに、連絡先リストを自動的にスクロールできます。
3. JAVAアプリが異なるDPIでの識別再生を強化しました。
4. **クリックア**クティビティは補助キーのプロパティを追加しました。例えば、クリックしながら**Ctrl**キーを押すことができます。

## 2020.05.21リリースの説明

2020.05.21にEncooエディタ、ロボットのコミュニティ版がリリースされました。今回リリースされた製品のバージョンは以下となります：

|         | バージョン      |
| -----:  | -----:     |
| エディタ | 1.1.2005.3 |
| ロボット | 1.1.2005.3 |

Encoo コンソール -> [*インストールパッケージをダウンロード*](https://console.encoo.com/#/download)で関連製品をダウンロードして体験することができます。

### 新規機能

#### 【アクティビティ】

1. **アプリケーション自動化 > メール > [メールを取得（IMAP）](Activities/AppAutomation/Mail/GetMailIMAP.md?_v=v2020.4)**。
1. **アプリケーション自動化 > Office Excel > [範囲をオートフィル](Activities/AppAutomation/OfficeExcel/AutoFillRange.md?_v=v2020.4)**。
2. **系统 > [テキストをクリップボードに設定](Activities/System/SetContentsToClipboard.md?_v=v2020.4)** ：テキストコンテンツをクリップボードに設定

#### 【アクティビティ市場】

1. **アクティビティ市場**に[OfficePPTパッケージ](https://marketplace.encoo.com/#/activity/detail?packageId=Encootech.OfficePPT)を追加しました。PPTの一般的な機能のサポートを実現します。
2. **アクティビティ市場**に[竹間智能音声認識](https://marketplace.encoo.com/#/activity/detail?packageId=Emotibot)を追加しました。音声からテキストへの機能を実現します。

#### 【エディタ】

プロセス中のアクティビティをサブプロセスファイルとして保存することをサポートします。この機能を使って複雑なプロセスをいくつかの簡単なプロセスに分解することができます。

### 改善と強化

#### 【アクティビティ】

 **アプリケーション自動化 > Office Excel**アクティビティの実行性能を向上させました。

#### 【エディタ】

1. **式エディタ**の**インテリジェントな知覚機能**を強化し、変数/引数/メソッド名の連想をサポートします。
2. コミュニティ版のライセンスがクォータを超えた場合、解決方法のヒントを追加しました。
3. 変数/引数を作成する際に、DataTable/IUiObjectタイプの変数/引数を素早く作成することをサポートします。
4. アクティビティの右クリックメニューを介してアクティビティのヘルプドキュメントにアクセスすることをサポートします。

### 修復した問題

#### 【エディタ】

1. 式を編集する時、自動的に補足された変数名が不備である問題を修正しました。
2. デバッグ時に容器類のアクティビティ中の最後のアクティビティのプロパティを確認できない問題を修正しました。
3. アクティビティを検索するときに検索結果が不完全に表示される問題を修正しました。
4. 変数値を変更した後、プロジェクトをデバッグするときに変更が有効にならない問題を修正しました。
5. エディターインターフェイスがときどきクリックされない問題を修正しました。
