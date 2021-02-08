# データシート編集モード
データシート編集モードページは、データシート内のデータに対して並べ替え、フィルタ、フォーマット設定などの操作を提供し、Excelを操作するようにミニプログラムのデータシートを操作します。

![数据表详情](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/tabledetail20201207.png)
 </br> 

## データシートの操作

- **シート名を変更** ：データシート名を右クリックし、ポップアップメニューから"名前を変更"を選択すると、シート名を変更できます。
![重命名表名](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/rename20201207.png)
 </br> 

- **シートを削除** ：データシート名を右クリックし、ポップアップメニューから"削除"を選択すると、シートを削除できます。
![删除表名](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/deletetablename20201207.png)
 </br> 
- **編集モードを終了** ：データシート名の上にある"編集を終了"リンクをクリックすると、編集モードを終了し、データシート管理リストページに戻ります。
![退出编辑模式](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/exitedit20201207.png)
 </br> 

## データシートの内容の操作
- **行/列を挿入**
  - 方式一：シート行/列の最後の![新增行/列](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/addcolum20201207.png)アイコンをクリックします。
  - 方式二：あるシート/列/全シートを選択し、右クリックメニューから**行/列を挿入**メニューを選択して、行/列を挿入する位置を選択します。

  ![插入行/列](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/addline20201207.png)
   </br> 

- **シートデータを変更**
変更するシートのセルにカーソルを合わせて、データを入力します。
 </br> 

- **セルをコピー/貼り付け**
シートの一部のデータを選択して、右クリックして"コピー"を選択し、貼り付ける場所にカーソルを合わせて、右クリックして"貼り付け"を選択。
  >**说明：**
  >Shiftキーを押しながらカーソルで選択します。複数のセルを削除またはコピーできます。

  ![复制/粘贴单元格](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/copycaste20201207.png)
 </br> 

- **エリアにデータを拡張**
単一のセルのデータを選択して、セルの右下隅のカーソルをドラッグすると、横向きまたは縦向きのセルのデータが現在選択されている単一のセルのデータに上書きされます。
![扩展数据至范围](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/extend20201207.png)
 </br> 

- **シートデータをフィルタ**
  - シートのヘッダフィールドの右側の逆三角形アイコンをクリックして、値や条件に応じてデータをフィルタすることができます。
  ![筛选列数据](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/filterdata20201207.png)
   </br> 

  - セル内で配列形式のデータを参照すると、フィルタされたデータをプレビューできます。
  ![筛选单元格数据](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/filtercell20201207.png)
   </br> 


- **シートデータをソート**
  - **列をソート** ：シートのヘッダフィールドの右側の逆三角形アイコンをクリックして、昇順、降順、またはソートしないでデータを並べ替えできます。
 
    ![排序表数据](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/sort20201207.png)
 </br> 

  - **ドラッグ＆ドロップでソート** ：移動する行/列のいずれかを選択し、ターゲット所にドラッグします。

    ![表头字段排序](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/movesort20201208.png)
 </br> 


- **列の書式を設定**
  - 方式1：列全体または単一のセルを選択し、右クリックして**列の書式を設定**を選択。ポップアップされたダイアログで必要に応じて設定します。
  - 方式2：列全体または単一のセルを選択し、上の**列の書式を設定**ボタンをクリックします。ポップアップされたダイアログで必要に応じて設定します。
  >**説明:**
  >
  > 列の書式設定のみがサポートされており、単一のセルの書式設定はサポートされていません。

  ![设置列格式](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/setcoulm20201207.png)

 </br> 

- **数式をセルに適用する**
単一のシート/列/全シートを選択して、現在選択されている項目の値/数式を表示します。セルでサポートされている数式は、[数式リスト](https://formulajs.info/functions/)を参照してください。
![应用公式到单元格](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/folum20201207.png)
 </br> 

- **シートをエクスポート**
上の"エクスポート"ボタンをクリックして、現在のシートをxlsxまたはcsv形式にエクスポートし、自動的にローカルコンピュータにダウンロードします。
![导出表格](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/exportexcel20201207.png)