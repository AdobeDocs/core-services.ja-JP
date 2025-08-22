---
description: 顧客属性ソースを作成して、Adobe Experience Cloudにアップロードします。
solution: Experience Cloud
title: 顧客属性Sourceの作成とデータファイルのアップロード
uuid: 53dca789-9a91-4385-839d-c9d1aa36b9be
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 21ed7c35-aac9-46f1-a50c-84e7c075209c
source-git-commit: 3043cd913d5165c58fb84f3342b05a00a690d6a6
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 49%

---

# 顧客属性ソースの作成とデータファイルのアップロード

顧客属性ソース（`.csv` ファイルと `.fin` ファイル）を作成してデータをアップロードします。 準備できたら、データソースをアクティブ化できます。データソースがアクティブになったら、属性データを Analytics と Target で共有します。

## 顧客属性のワークフロー {#concept_BF0AF88E9EF841219ED4D10754CD7154}

![ 顧客属性のワークフロー ](assets/crs.png)

>[!IMPORTANT]
>
>この機能にアクセスするには、ユーザーを顧客属性製品プロファイル（顧客属性 – デフォルトアクセス）に割り当てる必要があります。 **[!UICONTROL Admin Console]** / **[!UICONTROL 製品]** に移動します。 *顧客属性* が [!UICONTROL &#x200B; 製品プロファイル &#x200B;] の 1 つとして表示されたら、開始する準備が整います。 顧客属性グループに追加されたユーザーには、Experience Cloud インターフェイスの左側に [!UICONTROL &#x200B; 顧客属性 &#x200B;] メニューが表示されます。
>
>また、顧客属性機能を使用するには、ユーザーがアプリケーションレベルのグループ（Adobe Analyticsまたは [!DNL Target]）に属している必要があります。

## データファイルの作成 {#create-data}

このデータは、CRM の企業顧客データです。データには、メンバー ID、権限付与されている製品、最も頻繁に起動する製品など、製品に関する購読者データが含まれます。

1. `.csv` ファイルを作成します。

   >[!NOTE]
   >
   >このプロセスの後半で、`.csv` ファイルをドラッグ&amp;ドロップしてファイルをアップロードします。 [FTP を使用してアップロード](t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)する場合は、`.csv` と同じ名前の `.fin` ファイルも必要です。

   企業顧客データファイルの例：

   ![企業顧客データファイルの例](assets/01_crs_usecase.png)

1. 続行する場合は、ファイルをアップロードする前に[データファイル要件](crs-data-file.md)の重要な情報を確認してください。
1. 以下に説明するように、[顧客属性ソースを作成してデータファイルをアップロードします](t-crs-usecase.md)。

## 属性ソースの作成とデータファイルのアップロード {#create-source}

Experience Cloudの新しい顧客属性ソースを作成ページでこれらの手順を実行します。

>[!IMPORTANT]
>
>顧客属性ソースを作成、変更または削除する場合、ID が新しいデータソースと同期され始めるまで、最大 1 時間の遅延があります。顧客属性ソースを作成または変更するには、Audience Manager の管理者権限が必要です。Audience Manager カスタマーケアまたはコンサルティングに問い合わせて、管理者権限を取得してください。

1. [!DNL Experience Cloud] で、メニュー ![ メニュー ](assets/menu-icon.png) アイコンを選択します。
1. **[!UICONTROL 顧客属性]** を選択します。

   [!UICONTROL &#x200B; 顧客属性 &#x200B;] ページでは、既存の属性データソースを管理および編集できます。

   ![ 顧客属性のメイン画面 ](assets/cust-attr.png)

1. 「**[!UICONTROL 新規]**」をクリックします。

   ![手順の結果](assets/04_crs_usecase.png)

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

## ファイルをアップロード {#upload}


1. ファイルをアップロードをクリックします。

2. `.csv`、`.zip` または `.gzip` のデータファイルをドラッグ&amp;ドロップウィンドウにドラッグ&amp;ドロップします。

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

1. [!UICONTROL &#x200B; 顧客属性Sourceを編集 &#x200B;] ページで、**[!UICONTROL Target]** または **[!UICONTROL Analytics]** サブスクリプション（「[!UICONTROL &#x200B; サブスクリプションの設定 &#x200B;]」の下）を削除します。
1. [更新されたフィールドを含む新しいデータファイルをアップロードします](t-crs-usecase.md)。

## 購読の設定と属性ソースの有効化 {#task_1ACA21198F0E46A897A320C244DFF6EA}

購読を設定すると、Experience Cloudとアプリケーション間のデータフローが設定されます。 属性ソースを有効化すると、購読しているアプリケーションでデータが利用できるようになります。アップロードした顧客レコードは、Web サイトまたはアプリケーションから入ってくる ID 信号と照合されます。

詳しくは、[サブスクリプションの設定](subscription.md)を参照してください。

**属性ソースを有効化するには**

[!UICONTROL &#x200B; 新規を作成または顧客属性Sourceを編集 &#x200B;] ページで、「[!UICONTROL &#x200B; アクティブ化 &#x200B;] 見出しを探し、「**[!UICONTROL アクティブ]**」をクリックします。

![手順の結果](assets/activate_attribute_source.png)

## Adobe Analyticsでの顧客属性の使用 {#task_7EB0680540CE4B65911B2C779210915D}

Adobe Analytics などのアプリケーションで利用できるデータを使用して、データをレポートおよび分析し、マーケティングキャンペーンで適切なアクションを起こすことができます。

以下の例は、アップロードした属性に基づいた [!DNL Analytics] セグメントを示しています。このセグメントは、最も頻繁に起動する製品が Photoshop である [!DNL Photoshop Lightroom] の購読者を示しています。

![アップロードされた属性に基づく Analytics セグメント](assets/08_crs_usecase.png)

セグメントをExperience Cloudに公開すると、Experience Cloud Audiences とAudience Managerで使用できるようになります。

## Adobe Targetでの顧客属性の使用 {#task_FC5F9D9059114027B62DB9B1C7D9E257}

[!DNL Target] では、オーディエンスの作成時に「[!UICONTROL 訪問者プロファイル]」セクションから顧客属性を選択できます。すべての顧客属性には、リストのプレフィックス `crs.` が付きます。 これらの属性を、必要に応じて他のデータ属性と組み合わせることで、オーディエンスを構築します。

![Adobe Target での顧客属性の使用](assets/crs-add-attribute-target.png)

[!DNL Target] ヘルプの[新しいオーディエンスの作成](https://experienceleague.adobe.com/docs/target/using/audiences/create-audiences/audiences.html)を参照してください。
