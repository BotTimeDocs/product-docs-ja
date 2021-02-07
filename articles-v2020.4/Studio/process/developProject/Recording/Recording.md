# スマート録画

**スマート録画**はEncooエディタの重要な部分です。ビジネスプロセスを自動化するときに多くの時間を節約するのに役立ちます。この機能を使用すると、画面上のユーザーアクションを簡単にキャプチャして、シーケンスに変換できます。

録画機能を使って、自動化プロセスプロジェクトを録画した後、これらのプロジェクトを修正して、対応する引数を調整して、他のプロセスで簡単に呼び出しできます。

## 録画の説明

画面に黄色の矩形の枠が現れたら、録画が開始されたことを表します。この時点で、ターゲット要素をクリックすることができます。矩形は識別された要素を表しています。データを取得するためにクリックしたり、また他の方法でインタラクティブできます。下図のように、正しいボタン、テキスト、メニューが選択されていることを確保できます。

![録画中](https://docimages.blob.core.chinacloudapi.cn/images/Studio/recording/recording.png)

録画中、UI要素とのインタラクションは、情報性のスクリーンショットを生成します。選択された録画の種類にかかわらず、記録可能な操作があり、記録できないものもあります。

**録画可能な操作** 

* ボタンをマウスで左クリック、選択ボックス、プルダウンリスト、その他のグラフィックユーザーインターフェース要素
* 入力中のテキスト

**録画できない操作** 

* キーボードショートカットキー

> 注意:
>
> 表示設定を変更した場合、コンピュータを再起動しないと、要素を正しく認識できない場合があります。

## レコーダー

Encooエディタは主に2種類の録画タイプがあります。それぞれはウェブサイトの録画、デスクトップの録画です。

すべての録画タイプは同じレコーダーを使っています。レコーダーはWebアプリケーションとデスクトップアプリケーションでの録画操作のために設計されています。いろいろな操作環境での動作を録画できます。

レコーダーを使って以下のことができます：

* 画面上で実行される複数のアクションを自動的に記録します

* 手動で単一の操作を記録します。例えば、

  * 画面要素をクリックまたはダブルクリック
  * テキストボックスにテキストを入力する
  * 要素の検索または要素が消えるまで待つ

録画時に使用できるキーボードショートカット：
* F2 –5秒遅れて録画します。
* Esc –録画を終了します。
* Ctrl+マウスで枠をドラッグ–画像認識。

### レコーダーの画面操作
**レコーダー画面**

![レコーダー](https://docimages.blob.core.chinacloudapi.cn/images/Studio/recording/recorder.PNG)

| オプション | 説明 |
|-----|-----|
| スマート録画 | クリックしてウェブサイトやデスクトップアプリケーションの録画を開始します。 |
| 保存と終了 | 録画した自動化プロセスをEncooエディタに保存し、レコーダーを終了します。 |
| クリア | レコーダーに録画された自動化のプロセスを削除します。 |
| クリック | クリック、ダブルクリック、選択に分けます。<br>クリック/ダブルクリック: 画面要素を手動でクリック/ダブルクリックします。<br>選択: 界面要素を選択します。 |
| テキスト | テキストを取得、テキストを入力に分けます。<br>テキストを取得: テキストの内容を取得します。<br>テキストを入力: テキストボックスに内容がない場合は、テキストボックスにテキストを直接入力することができます。 |
| イベント | 要素が表示されるまで待つ、要素が消えるまで待つ。主に判断に用いられます。<br>要素が表示されるまで待つ：界面元素の出現を待ちます。<br>要素が消えるまで待つ：界面元素の消失を待ちます。 |

**レコーダーのプレビュー画面**

レコーダーがいくつかの自動化の操作を録画した後、プレビュー画面が生成されます。この画面では、録画された操作を変更・削除でき、自動化のプロセスを改善することができます。

![プレビュー画面](https://docimages.blob.core.chinacloudapi.cn/images/Studio/recording/preview.PNG)