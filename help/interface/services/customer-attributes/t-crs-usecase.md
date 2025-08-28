---
description: 顧客属性ソースの作成方法と、Adobe Experience Cloudへのアップロード方法を説明します。
solution: Experience Cloud
title: 顧客属性データのSource ファイルの作成とアップロード
uuid: 53dca789-9a91-4385-839d-c9d1aa36b9be
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 21ed7c35-aac9-46f1-a50c-84e7c075209c
source-git-commit: 32f3bd4eb6229a910366f274f9adfbc609440764
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 49%

---

# 顧客属性ソースの作成とデータファイルのアップロード

顧客属性ソース（`.csv` ファイルと `.fin` ファイル）を作成してデータをアップロードします。 準備できたら、データソースをアクティブ化できます。データ ソースがアクティブになったら、属性データを [!DNL Analytics] と [!DNL Target] に共有します。

**顧客属性のワークフロー**

![ 顧客属性のワークフロー ](assets/crs.png)

## 前提条件

**製品へのアクセス：**&#x200B;[!DNL Customer Attributes] 製品にアクセスするには、ユーザーをAdmin Console（**[!UICONTROL ）の「顧客属性」製品プロファイル（]** 顧客属性 – デフォルトアクセス `adminconsole.adobe.com`）に割り当てる必要があります。

**[!UICONTROL Admin Console]** / **[!UICONTROL 製品]** に移動します。 *顧客属性* が製品の 1 つ（[!UICONTROL &#x200B; 製品プロファイル &#x200B;]）として表示されたら、開始する準備が整います。 顧客属性製品プロファイルに追加されたユーザーには、「アプリ **[!DNL Customer Attributes]** セレクターに **[!UICONTROL が表示さ]** ます。 （![ 顧客属性のワークフロー ](assets/menu-icon.png)）

**アプリケーショングループ：** **[!DNL Customer Attributes]** 機能を使用するには、ユーザーがアプリケーションレベルのグループ（Adobe [!DNL Analytics] または [!DNL Adobe Target]）にも属している必要があります。

## データファイルの作成 {#create-data}

このデータは、CRM の企業顧客データです。データには、メンバー ID、権限付与されている製品、最も頻繁に起動する製品など、製品に関する購読者データが含まれます。

1. `.csv` ファイルを作成します。

   >[!NOTE]
   >
   >このプロセスの後半で、`.csv` ファイルをドラッグ&amp;ドロップしてファイルをアップロードします。 [FTP を使用してアップロード](t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)する場合は、`.csv` と同じ名前の `.fin` ファイルも必要です。

   企業顧客データファイルの例：

   ![企業顧客データファイルの例](assets/01_crs_usecase.png)

1. 続行する場合は、ファイルをアップロードする前に[データファイル要件](crs-data-file.md)の重要な情報を確認してください。
1. 以下に説明するように、[顧客属性ソースを作成してデータファイルをアップロードします](t-crs-usecase.md#create-source)。

## 属性ソースの作成とデータファイルのアップロード {#create-source}

Experience Cloudの新しい顧客属性ソースを作成ページでこれらの手順を実行します。

>[!IMPORTANT]
>
>顧客属性ソースを作成、変更または削除する場合、ID が新しいデータソースと同期され始めるまで、最大 1 時間の遅延があります。顧客属性ソースを作成または変更するには、Audience Manager の管理者権限が必要です。Audience Manager カスタマーケアまたはコンサルティングに問い合わせて、管理者権限を取得してください。

1. [!DNL Experience Cloud] で、**[!UICONTROL アプリ]**![ メニュー ](assets/menu-icon.png)/**[!DNL Customer Attributes]** をクリックします。

   ![ 顧客属性ページ ](assets/cust-attr.png)

1. 「**[!UICONTROL 新規]**」をクリックします。

   ![手順の結果](assets/new-customer-attribute-source.png)

1. [!UICONTROL &#x200B; 顧客属性Sourceを作成 &#x200B;] ページで、次のフィールドを設定します。

   * **[!UICONTROL 名前：]**&#x200B;データ属性ソースのわかりやすい名前。[!DNL Adobe Target] の場合、属性名にスペースを含めることはできません。スペースを含む属性が渡された場合、[!DNL Target] はその属性を無視します。次の文字もサポートされていません。`< , >, ', "`

   * **[!UICONTROL 説明：]**（オプション）データ属性ソースの説明。

   * **[!UICONTROL エイリアス ID：]**&#x200B;特定の CRM システムなど、顧客属性データのソースを表します。[!UICONTROL &#x200B; エイリアス ID] は、[!UICONTROL &#x200B; 顧客属性Source] コードで使用される一意の ID です。 ID は一意で、スペースを含まないアルファベットおよびアンダースコアの組み合わせにしてください。Experience Cloudで顧客属性ソースの [!UICONTROL &#x200B; エイリアス ID] フィールドに入力する値は、実装から（Platform データ収集または Mobile SDKのJavaScriptを使用して）渡されている値と一致させる必要があります。

     >[!IMPORTANT]
     >
     >エイリアス ID は複数のサービスに保存され、サービス間でプロファイルをマッピングするために使用されるので、エイリアス ID に関連付けられたデータソースを削除しても、エイリアス ID は使用できません。

     エイリアス ID は、追加の顧客 ID 値を設定する特定の領域に対応します。 例：

      * **タグ：** エイリアス ID は、*Experience Cloud ID サービス* ツールの [!UICONTROL &#x200B; 顧客設定 &#x200B;] の下にある [Integration Code](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ja) 値に対応しています。

      * **訪問者 API:** エイリアス ID は、各訪問者に関連付けることができる追加の [ 顧客 ID](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) に対応します。

        例：*crm_id* の場合：

        ```
        "crm_id":"67312378756723456"
        ```

      * **iOS:** エイリアス ID は *visitorSyncIdentifiers*[ の :identifiers&quot;idType&quot;](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=ja) に対応しています。

        例：

        `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`

      * **Android™：**&#x200B;エイリアス ID は [syncIdentifiers](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=ja) の *&quot;idType&quot;*&#x200B;に対応しています。

        例：

        `identifiers.put(`**`"idType"`**`, "idValue");`

        エイリアス ID フィールドと顧客 ID に関するデータ処理について詳しくは、[ 複数のデータソースの活用 ](crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB) を参照してください。

   * **[!UICONTROL 名前空間コード：]** この値を使用して、AEP WebSDK 実装の一環として [IdentityMap](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/identity/overview) を使用する際に顧客属性ソースを識別します。

1. 「**[!UICONTROL 保存]**」をクリックします。

## ファイルをアップロード {#upload}

顧客属性レコードが作成され、顧客属性を編集してファイルをアップロードできます。

1. [!DNL Customer Attributes] ページで、属性ソースをクリックします。

1. [!UICONTROL &#x200B; 顧客データのSourceを編集 &#x200B;] ページで、「**[!UICONTROL ファイルのアップロード]**」をクリックします。

   ![ ファイルのアップロードとスキーマの検証 ](assets/file-upload-schema-validation.png)

1. `.csv`、`.zip` または `.gzip` のデータファイルをドラッグ&amp;ドロップウィンドウにドラッグ&amp;ドロップします。

>[!IMPORTANT]
>
>特定のデータファイル要件が存在します。詳しくは、[データファイル要件](crs-data-file.md)を参照してください。

ファイルをアップロードすると、このページの「[!UICONTROL ファイルのアップロード]」見出しの下に、表データが表示されます。スキーマを検証したり、購読を設定したり、FTP を設定したりできます。

![ 属性 ](assets/file_upload_attributes.png)

* **[!UICONTROL 一意の顧客 ID:]** この属性ソースにアップロードした一意の顧客 ID の数を表示します。

* **[!UICONTROL Experience Cloud訪問者 ID にエイリアスされた顧客提供の ID:]** Experience Cloud訪問者 ID にエイリアスされた ID の数を表示します。

* **[!UICONTROL エイリアス数の多い顧客提供 ID:]** エイリアスが 500 以上あるExperience Cloud訪問者 ID を持つ顧客提供 ID の数を表示します。 このような顧客提供 ID は、個人ではなくある種の共有ログインを表している可能性が最も高くなります。これらの ID に関連付けられた属性は、エイリアス数が 10,000 に達するまで、直近にエイリアスされた 500 個の Experience Cloud 訪問者 ID に振り分けられます。次に、システムは顧客から提供された ID を無効にし、関連付けられた属性を配布しなくなります。—>

## スキーマの検証 {#validate-schema}

検証プロセスでは、アップロードした属性（文字列、整数、数値など）に表示名と説明をマッピングできます。また、スキーマを更新して属性を削除することもできます。

[スキーマの検証](validate-schema.md)を参照してください。

属性を削除するには、[（オプション）スキーマの更新（属性の削除）](t-crs-usecase.md)を参照してください。

## （オプション）スキーマの更新（属性の削除）  {#task_6568898BB7C44A42ABFB86532B89063C}

スキーマの属性を削除したり属性を置換したりする方法。

1. [!UICONTROL 顧客属性ソースを編集]ページで、**[!UICONTROL Target]** または **[!UICONTROL Analytics]** サブスクリプション（「**[!UICONTROL サブスクリプションの設定]**」の下）を削除します。

1. [更新されたフィールドを含む新しいデータファイルをアップロードします](t-crs-usecase.md)。

## 購読の設定と属性ソースの有効化 {#task_1ACA21198F0E46A897A320C244DFF6EA}

購読を設定すると、Experience Cloudとアプリケーション間のデータフローが設定されます。 属性ソースを有効化すると、購読しているアプリケーションでデータが利用できるようになります。アップロードした顧客レコードは、Web サイトまたはアプリケーションから入ってくる ID 信号と照合されます。

[ 購読の設定とデータソースのアクティベート ](subscription.md) を参照してください。

## Adobe Analyticsでの顧客属性の使用 {#task_7EB0680540CE4B65911B2C779210915D}

Adobe Analytics などのアプリケーションで利用できるデータを使用して、データをレポートおよび分析し、マーケティングキャンペーンで適切なアクションを起こすことができます。

以下の例は、アップロードした属性に基づいた [!DNL Analytics] セグメントを示しています。このセグメントは、最も頻繁に起動する製品が Photoshop である [!DNL Photoshop Lightroom] の購読者を示しています。

![アップロードされた属性に基づく Analytics セグメント](assets/08_crs_usecase.png)

セグメントをExperience Cloudに公開すると、Experience Cloud Audiences とAudience Managerで使用できるようになります。

## Adobe Targetでの顧客属性の使用 {#task_FC5F9D9059114027B62DB9B1C7D9E257}

[!DNL Target] では、オーディエンスの作成時に「[!UICONTROL 訪問者プロファイル]」セクションから顧客属性を選択できます。すべての顧客属性には、リストのプレフィックス `crs.` が付きます。 これらの属性を、必要に応じて他のデータ属性と組み合わせることで、オーディエンスを構築します。

![Adobe Target での顧客属性の使用](assets/crs-add-attribute-target.png)

[!DNL Target] ヘルプの[新しいオーディエンスの作成](https://experienceleague.adobe.com/docs/target/using/audiences/create-audiences/audiences.html)を参照してください。
