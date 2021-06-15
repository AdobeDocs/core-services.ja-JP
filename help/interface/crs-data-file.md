---
description: 顧客属性を Experience Cloud にアップロードするためのデータファイル要件および複数のデータソースについて説明します。
keywords: 顧客属性;コアサービス
solution: Experience Cloud
title: '顧客属性のデータファイルとデータソースについての説明 '
uuid: 9dd0e364-889b-45db-b190-85c0930a101e
feature: 顧客属性
topic: 管理
role: Administrator
level: Experienced
exl-id: e2dfe10d-7003-4afa-a5e6-57703d74efd4
source-git-commit: eef7326f9f04f68eefb60b5d9fd4cc91cbe52119
workflow-type: tm+mt
source-wordcount: '1198'
ht-degree: 70%

---

# 顧客属性のデータファイルおよびデータソースについて

顧客属性をデータにアップロードするためのデータファイル要件および複数のデータソースに関するExperience Cloud。

企業内のCRMデータや類似データにアクセスする必要があります。 Experience Cloud にアップロードするデータは `.csv` ファイルでなければなりません。FTP や sFTP を利用してアップロードする場合は、`.fin` ファイルもアップロードします。

顧客属性は、1 日に数ファイルを処理するように設計されています。小さなファイルが多数ある場合に処理を遅延させる問題を軽減するために、同じ組織から前のバッチから30分以内に送信されたファイルは、優先度の低いキューにルーティングされます。

## 許可されるファイルタイプと命名規則 {#section_6F64FA02ACCC4215B0862CB6A1821FBF}

<table id="table_C27955F6B52A45B28BEEAAF14FFC86D8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> ファイルタイプ </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .csv </span> </p> </td> 
   <td colname="col2"> <p>値をコンマで区切って入力したファイル（Excel で作成するファイルなど）。このファイルには、顧客属性データが含まれます。 </p> <p> <b>命名規則：</b>ファイル名拡張子に空白文字が含まれていないことを確認してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .fin </span> </p> </td> 
   <td colname="col2"> <p>（必須）<span class="filepath">.fin</span> ファイルは、データのアップロードの終了をシステムに知らせます。<span class="filepath">.fin</span> ファイルの名前は <span class="filepath">.csv</span> ファイルの名前と一致する必要があります。 </p> <p>アドビは、<span class="filepath">.fin</span> 拡張子を持つ空のテキストファイルを作成することを推奨します。空のファイルを使用して容量やアップロード時間を節約できます。 </p> <p> <p>注意：<span class="filepath">.fin</span> ファイルのアップロード後にファイル名を変更することはできません。<span class="filepath">.fin</span> ファイルは別個にアップロードする必要があり、既にアップロード済みのファイルの名前を変更しても、.fin ファイルとしては認識されません。 </p> </p> <p><span class="filepath">.fin</span> ファイルを顧客属性 FTP でアップロードすると、データはすばやく取得されます（1 分以内）。これは、あまり頻繁にデータを取得しない（1 時間に 1 回程度）他のアドビ FTP ベースのシステムとは異なる点です。 </p> <p>Web の UI でドラッグ＆ドロップしてアップロードする場合、<span class="filepath">.fin</span> ファイルは不要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .gz</span> または <span class="filepath">.zip </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath">.gz</span>（gzip）または <span class="filepath">.zip</span> - 圧縮ファイル用。<span class="filepath">.zip</span> ファイルは、アーカイブに複数のファイルを含めることはできません。 </p> <p> <b>命名規則：</b><span class="filepath">.zip</span> または <span class="filepath">.gz</span> の名前は <span class="filepath">.csv</span> の名前と一致する必要があります。例えば、<span class="filepath">.csv</span> ファイルが <span class="filepath">crm_small.csv</span> の場合、<span class="filepath">.zip</span> ファイルは <span class="filepath">crm_small.csv.zip</span> である必要があります。 </p> <p>.fin ファイルは .csv のファイル名と拡張子以外が一致する必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性データファイルの要件 {#section_169FBF5B7BBA47CE825B7A330CF3FE98}

**CSV の例**

CSV ファイルは次の形式に準拠する必要があります。

![](assets/cvs.png)

同じファイルをテキストエディターで表示した様子：

![](assets/csv_txt.png)

**ガイドライン**

<table id="table_A9849CC9AA784763921DE057F0F61515"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 項目 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ドラッグ＆ドロップ </p> </td> 
   <td colname="col2"> <p>ドラッグ&amp;ドロップの場合、ファイルのサイズは100 MB未満にする必要があります。 </p> <p>Web の UI でドラッグ＆ドロップしてアップロードする場合、<span class="filepath">.fin</span> ファイルは不要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>顧客 ID 列 </p> </td> 
   <td colname="col2"> <p> 1 列目は一意の顧客 ID でなければなりません。使用する ID は、Experience Cloud ID サービスに渡される ID に対応している必要があります。 </p> <p>Analytics の場合は、prop または eVar に格納されている ID です。 </p> <p>Target の場合は、setCustomerID 値です（<a href="core-services.md#section_AD473A6A21C1446498E700363F9A8437" format="dita" scope="local">Analytics と Adobe Target - 顧客 ID の同期</a>を参照してください）。 </p> <p> この顧客 ID は、データベース内の各ユーザーを表すために CRM で使用する一意の ID です。残りの列は CRM から取得される属性です。アップロードする属性の数を選択できます。 </p> <p>列の見出しには読みやすく、わかりやすい名前を使用することが推奨されますが、必須ではありません。アップロード後におこなうスキーマの検証の際に、アップロードされた行と列にわかりやすい名前をマッピングできます。 </p> <p> <b>顧客 ID について</b> </p> <p>通常、企業は、CRM システムからの顧客 ID を使用します。この ID は、ユーザーのログイン時に <span class="codeph">setCustomerIDs</span> 呼び出しを使用して設定されます。また、この ID は、Experience Cloud にアップロードされる CRM ファイルのキーとしても使用されます。<a href="t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8" format="dita" scope="local">エイリアス ID</a> は、エイリアスデータが格納される Audience Manager のデータストアの識別子です。システムは、エイリアスをこのデータストアに（setCustomerIDs を使用して）送信します。CRM ファイルは、このデータストアのデータに適用されます。 </p> <p><span class="codeph">setCustomerIDs</span> 情報については、<a href="https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=en" format="https" scope="external">顧客 ID と認証の状態</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 列目以降の見出しと列 </p> </td> 
   <td colname="col2"> <p>2 列目以降の見出しは、各属性の名前を表す必要があります。 </p> <p> これらの列は、CRM から取得される顧客属性を含んでいる必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>属性の制限 </p> </td> 
   <td colname="col2"> <p>数百の<span class="filepath"> .csv </span>列をExperience Cloudの顧客属性サービスにアップロードできます。 ただし、サブスクリプションを設定して属性を選択する場合、所有するソリューションに応じて、次の制限が適用されます。 </p> <p> 
     <ul id="ul_2BB85067918D4BB3B59394F3E3E37A6D"> 
      <li id="li_93703988B9934384B4B94A839D028380"> <b>Analytics Standard：</b>合計 3 件 </li> 
      <li id="li_D1E5E7BD24C54591B14D15DE97447835"> <b>Analytics Premium：</b>レポートスイートあたり 200 件 </li> 
      <li id="li_8C891FE3D1EF49FA9F81E2E32CD0B9CA"> <b>Adobe Target Standard：</b>5 件 </li> 
      <li id="li_2B66D43023F34EA685CE2C38A9250CEA"> <b>Adobe Target Premium：</b>200 件 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>行の制限 </p> </td> 
   <td colname="col2"> <p>行数に制限はありません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>列の制限 </p> </td> 
   <td colname="col2"> <p>実用上、列数は最大 200 個前後に制限されています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>文字制限 </p> </td> 
   <td colname="col2"> <p>Analytics サブスクリプションの作成時には、アップロードするファイルのフィールド長が 255 文字以下になるように切り詰められます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FTP に関するガイドラインとサイズ制限 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_E157EE6F98914EADA0C103D1D1E705D3"> 
      <li id="li_84FBD455DD164A28AC16F4A5AB19E4B3">FTP のファイルサイズの上限は、各アップロードで 4 GB です。 </li> 
      <li>ファイルサイズの下限は、各アップロードで 10 MB です。 </li>
      <li>30 分ごとに 1 つのファイルをアップロードできます。 </li>
      <li id="li_B69A20C51D824727AA99C1F6F78537A4"> <span class="filepath">.csv</span>（および <span class="filepath">.fin</span>）ファイルを FTP サイトのルートフォルダーにアップロードする必要があります。 </li> 
     </ul> </p> <p> <p>重要：FTP アカウントの合計許容量は 40 GB です。処理されたデータを削除するのは、ユーザーの責任です。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ファイル要件 </p> </td> 
   <td colname="col2"> <p> 各属性ソースには、コンマで区切った同数のフィールドが含まれる必要があります。 </p> <p> 改行、二重引用符またはコンマを含むフィールドは引用符で囲む必要があります。 </p> <p> フィールド内の二重引用符文字は、バックスラッシュ（\）を使用してエスケープする必要があります。 </p> <p> 空白の列は<span class="term">Null</span> として保存されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>複数のファイル </p> </td> 
   <td colname="col2"> <p>顧客属性データをアップロードする際に、複数のファイルを連続してすばやくアップロードする場合、特にファイルのサイズが大きい場合は、次のファイルをアップロードする前に、前のファイルが処理されていることを確認します。 これを監視するには、前のファイルが[!UICONTROL顧客属性] FTPアカウント内の処理済みフォルダーまたは失敗フォルダーに移動したタイミングを確認します。 </p> <p> サイズの大きいファイルを小さなファイルに分割し、それらを短時間で連続して送信すると、次のファイルを送信する前に各ファイルが確実に処理されない限り、実際に処理が遅くなる可能性があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>文字エンコーディング </p> </td> 
   <td colname="col2"> <p>日本では UTF-8 にする必要があります。 </p> </td> 
  </tr> 
   <tr> 
   <td colname="col1"> <p>履歴データ </p> </td> 
   <td colname="col2"> <p> 顧客属性は、基になる[!DNL Analytics]の訪問者プロファイルに結び付けられます。 そのため、[!UICONTROL顧客属性]は、[!DNL Analytics]でその訪問者プロファイルが有効である間ずっと、訪問者に関連付けられます。 このプロファイルには、顧客が初めてログインする前に発生した行動が含まれます。 </p> <p> Data Warehouseのバックフィル方法を使用している場合、データはAnalytics ID(AID)に基づくpost_visid_high/lowに結び付けられます。 Experience Cloud ID サービスを使用している場合、データは Experience Cloud ID（MID）に基づく post_visid_high/low に結び付けられます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>データフィード </p> </td> 
   <td colname="col2"> <p>顧客属性は、データフィードでは使用できません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 複数のデータソースの使用 {#section_76DEB6001C614F4DB8BCC3E5D05088CB}

顧客属性ソースを作成、変更または削除する場合、IDが新しいデータソースと同期され始めるまで、約1時間の遅延があります。

各顧客属性ソースのエイリアスIDは一意である必要があります。 同じIDを使用する複数のデータソースがある場合、次のように設定できます。

**VisitorAPI.js または Dynamic Tag Management の Experience Cloud ID ツール：**

適切なデータソースに対応する2つの顧客IDを設定します。

```
Visitor.setCustomerIDs({ 
     "ds_id1”:"123456", 
     "ds_id2":"123456" 
});
```

（詳しくは、[顧客 ID および認証の状態](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=en)を参照してください。）

**[!UICONTROL Experience Cloud]**／**[!UICONTROL People]**／**[!UICONTROL 顧客属性]**&#x200B;で：

上記の顧客 ID に対応する一意のエイリアス ID を使用して、2 つの顧客属性ソースを作成します。この方法を使用すると、同じ参照IDを複数の顧客属性ソースに送信できます。