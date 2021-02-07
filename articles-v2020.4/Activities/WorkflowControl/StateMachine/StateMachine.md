# ステートマシン

ステートマシン関連のアクティビティを使って、ステートマシンベースのプロセスを実現できます。

Encooのアクティビテ体系において、ステートマシンアクティビテは*ステート*アクティビティと*最終状態*アクティビティとステートマシンのプロセスを作るために必要な他のアクティビティのコンテナです。これらのアクティビティを使ってプロセスを実現する時、アクティビティをステートマシンアクティビテに置く必要があります。

ステータスマシンはマイクロソフト.NETフレームワークの一種のプログラミングモデルであり、ステートの変化を通じてプログラムロジックの推進を実現します。ステートマシンの詳細については、[ステートマシンプロセス](https://docs.microsoft.com/zh-cn/dotnet/framework/windows-workflow-foundation/state-machine-workflows)を参照してください。

## プロパティ

### 基本

- **表示名** ：デフォルトはこのアクティビティの名前です。このアクティビティの表示名の変更、カスタマイズがサポートされています。

## 操作サンプル
DingDingにログインすることを例にします。
1. **ステートマシン**アクティビティをドラッグ、ダブルクリックして、ステートマシンを展開。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/stateMachine-1.png)

2. ダブルクリックしてデフォルト**ステータス**アクティビティを展開、**要素が表示されるまて待つ**アクティビティをEntry容器にドラッグ、DingDingにログインした後のいずれかの要素を指定し、出力結果変数を設定。エラー発生時に実行を継続を"はい"に設定。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/stateMachine-2.png)

3. **最終状態**アクティビティをドラッグ、判断条件を`isTrue == true`に設定、最終状態をダブルクリックして展開、Enterコンテナに**確認ボックス**をドラッグ、"DingDingにログイン成功"というヒントを追加する。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/stateMachine-3.png)

4. **ステータス**アクティビティをドラッグ、判断条件を`isTrue==false`に設定:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/stateMachine-5.png)

5. アクティビティをダブルクリックして展開、Enterコンテナに次のプロセスを作成：ユーザー名を入力、パスワードを入力、ログインをクリック、ログイン後の要素が表示されるまて待つ。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/stateMachine-6.png)

6. ステップ5の操作で要素を待つと、最終状態は登録済みとなり、プロセスは以下のように設定されます。
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/stateMachine-7.png)

[*Greess Number*](https://docimages.blob.core.chinacloudapi.cn/images/dgsSample/GuessNumber.dgs)プロセスを参照すると、ステートマシン関連アクティビティの他の使用法を理解できます。

