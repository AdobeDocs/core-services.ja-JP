---
description: 顧客属性ソースを作成してデータをアップロードします。
keywords: 顧客属性;コアサービス
seo-description: 顧客属性ソースを作成してデータをアップロードします。
seo-title: 顧客属性ソースの作成とデータファイルのアップロード
solution: Experience Cloud
title: 顧客属性ソースの作成とデータファイルのアップロード
uuid: 53dam789-9a91-4385-839d- c9d1aa36b9be
translation-type: tm+mt
source-git-commit: b6058194725c3ad50d280a3daad737cd53416204

---


# 顧客属性ソースの作成とデータファイルのアップロード

顧客属性ソースを作成してデータをアップロードします。準備ができたら、データソースをアクティブにすることができます。データソースがアクティブになったら、属性データを Analytics と Target で共有します。

## 顧客属性のワークフロー {#concept_BF0AF88E9EF841219ED4D10754CD7154}

![](assets/crs.png)

1. [データファイルの作成](../attributes/t-crs-usecase.md#task_B5FB8C0649374C7A94C45DCF2878EA1A)
1. [属性ソースの作成とデータファイルのアップロード](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [スキーマの検証](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [購読の設定と属性ソースの有効化](../attributes/t-crs-usecase.md#task_1ACA21198F0E46A897A320C244DFF6EA)


データソースがアクティブになると、以下のことが可能になります。

* [Adobe Analytics での顧客属性の使用](../attributes/t-crs-usecase.md#task_7EB0680540CE4B65911B2C779210915D)
* [Adobe Target での顧客属性の使用](../attributes/t-crs-usecase.md#task_FC5F9D9059114027B62DB9B1C7D9E257)



>[!IMPORTANT]
>
>この機能にアクセスするには、ユーザー属性製品プロファイル（顧客属性-デフォルトアクセス）に割り当てる必要があります。（ **[!UICONTROL 管理]** / **[!UICONTROL 管理コンソール]** / **[!UICONTROL ユーザー]** /）。顧客属性グループに追加されたユーザーには、Experience Cloud インターフェイスの左側にある「[!UICONTROL Audiences]」に、[!UICONTROL 顧客属性]メニュー項目が表示されます。
>
>ソリューショングループのメンバーシップも必要です。

顧客属性機能を使用するためには、ユーザーがユーザー管理の Adobe 顧客属性グループとソリューションレベルのグループ（Analytics または Target）に属している必要があります。

[ユーザーとグループ](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)を参照してください。

## データファイルの作成 {#task_B5FB8C0649374C7A94C45DCF2878EA1A}

このデータは、CRM の企業顧客データです。データには、メンバー ID、権限付与されている製品、最も頻繁に起動する製品など、製品に関する購読者データが含まれます。


1. 指標をさらに制限する [!DNL .csv].


   >[!NOTE]
   >
   >このプロセスの後半で、ファイル [!DNL .csv] をドラッグ&amp;ドロップしてアップロードします。ただし、FTP経由 [でアップロード](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)する場合は、同じ名前の [!DNL .fin] ファイルも必要 [!DNL .csv]です。



   企業顧客データファイルの例：

   ![](assets/01_crs_usecase.png)

1. 続行する前に、ファイルをアップロードする前に [、データファイル要件](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)の重要な情報を確認してください。
1. [顧客属性ソースを作成し、以下に説明するデータ](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)をアップロードします。

## 属性ソースの作成とデータファイルのアップロード {#task_09DAC0F2B76141E491721C1E679AABC8}

Experience Cloud の新しい顧客属性ソースを作成ページでこれらの手順を実行します。


>[!IMPORTANT]
>
>顧客属性ソースを作成、変更または削除する場合、IDが新しいデータソースと同期され始めるまでに最大1時間かかります。顧客属性ソースを作成または変更するには、Audience Managerに管理者権限が必要です。Audience Managerカスタマーケアまたはコンサルティングに問い合わせて、管理者権限を取得してください。


1. で [!DNL Experience Cloud]、メニュー ![](assets/menu-icon.png) アイコンをクリックします。
1. Click **[!UICONTROL People]**, then click **[!UICONTROL Customer Attributes]**.

   [!UICONTROL 顧客属性]ページでは、既存の属性データソースを管理したり、編集したりできます。

   ![Step Result](assets/03_crs_usecase.png)
1. 「 **[!UICONTROL 新規]**」をクリックします。

   ![Step Result](assets/04_crs_usecase.png)
1. [!UICONTROL 顧客属性ソースを編集]ページで、以下のフィールドを設定します。


   * **[!UICONTROL 名前:]** データ属性ソースのわかりやすい名前。また [!DNL Adobe Target]、属性名にスペースを含めることはできません。スペースのある属性が渡された場合は、それを [!DNL Target] 無視します。サポートされていない他の文字は次のとおりです。 `< , >, ', "`を参照してください。

   * **[!UICONTROL 説明:]** （オプション）データ属性ソースの説明。

   * **[!UICONTROL エイリアスID:]** 特定のCRMシステムなど、顧客属性データのソースを表します。顧客属性ソースのコードで使用される一意の ID です。ID は一意で、スペースを含まないアルファベットおよびアンダースコアの組み合わせにしてください。Experience Cloud UI で顧客属性ソースのエイリアス ID フィールドに入力する値は、実装から（Dynamic Tag Management または Mobile SDK の JavaScript を使用して）渡されている値と一致させる必要があります。

      エイリアス ID は、追加の顧客 ID 値を設定する方法と一致させる必要があります。以下に例を示します。

      * **Dynamic tag management:** The Alias ID corresponds to the *Integration Code* value under [!UICONTROL Customer Settings], in the [Experience Cloud ID Service](https://marketing.adobe.com/resources/help/en_US/dtm/?f=macid) tool.

      * **訪問者 API：** エイリアス ID は、各訪問者と関連付けることができる追加の[顧客 ID](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_customer_ids) に対応しています。

         例えば、&quot;crm_ id *」* の場合、


         ```
         "crm_id":"67312378756723456"
         ```


      * **iOS:** エイリアスIDは、visitorSyncIdentifiers ** の [&quot;idType&quot;に対応しています。識別子](https://marketing.adobe.com/resources/help/en_US/mobile/ios/?f=methods)を使用します。

         以下に例を示します。

         `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`


      * **Android：** エイリアス ID は、*syncIdentifiers* の [&quot;idType&quot;](https://marketing.adobe.com/resources/help/en_US/mobile/android/?f=methods)。

         次に例を示します。

         `identifiers.put(`**`"idType"`**`, "idValue");`

         エイリアスIDフィールドと顧客IDに関するデータ処理について詳しくは、複数のデータソース [](../attributes/crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB) の活用を参照してください。
   * **[!UICONTROL ファイルのアップロード:]**[!DNL .csv] データファイルをドラッグ&amp;ドロップすることも、FTPを使用してデータをアップロードすることもできます。（FTPを使用するには [!DNL .fin] ファイルも必要です）。FTPを使用したデータ [のアップロードを参照](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)してください。


      >[!IMPORTANT]
      >
      >特定のデータファイル要件が存在します。詳しくは [、データファイルの要件](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) を参照してください。


      ファイルをアップロードすると、このページの「[!UICONTROL ファイルのアップロード]」見出しの下に、表データが表示されます。スキーマを検証したり、購読を設定したり、FTP を設定したりできます。



      **ファイルのアップロードのグラフィック**

      ![](assets/file_upload_attributes.png)

   * **[!UICONTROL ユニーク顧客ID:]** この属性ソースにアップロードした一意のID数を表示します。

   * **[!UICONTROL Experience Cloud訪問者IDにエイリアスされた顧客ID:]** Experience Cloud訪問者IDにエイリアスされたIDの数を表示します。

   * **[!UICONTROL エイリアス数の高い顧客ID:]** Experience Cloud訪問者IDが500以上エイリアスされた顧客IDの数を表示します。このような顧客提供 ID は、個人ではなくある種の共有ログインを表している可能性が最も高くなります。これらの ID に関連付けられた属性は、エイリアス数が 10,000 に達するまで、直近にエイリアスされた 500 個の Experience Cloud 訪問者 ID に振り分けられます。エイリアス数が 10,000 に達すると、顧客提供 ID は無効になり、関連付けられた属性の振り分けはおこなわれなくなります。










## スキーマの検証 {#task_404AAC411B0D4E129AB3AC8B7BE85859}

検証プロセスでは、アップロードした属性（文字列、整数、数値など）に表示名と説明を設定できます。また、スキーマを更新して属性を削除することもできます。

詳しくは、スキーマ [の検証を](../attributes/validate-schema.md#concept_B3A01A15D04E4F998118E09B3A9B5043)参照してください。

属性を削除するには、 [（オプション）スキーマを更新します（属性を削除する）](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C)。

## （オプション）スキーマの更新（属性の削除） {#task_6568898BB7C44A42ABFB86532B89063C}

スキーマの属性を削除したり属性を置換したりする方法。


1. 顧客属性ソース [!UICONTROL を編集] ページで、 **[!UICONTROL Targetまた]** は **[!UICONTROL Analytics]** のサブスクリプション（「購読 [!UICONTROL ]の設定」の下）を削除します。
1. [更新されたフィールドを含む新しいデータファイルをアップロード](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)します。

## 購読の設定と属性ソースの有効化 {#task_1ACA21198F0E46A897A320C244DFF6EA}

購読を設定すると、Experience Cloud とソリューション間のデータフローが設定されます。属性ソースを有効化すると、購読しているソリューションでデータが利用できるようになります。アップロードした顧客レコードは、Web サイトまたはアプリケーションから入ってくる ID 信号と照合されます。

詳しくは、購読 [の設定を](../attributes/subscription.md#concept_ECA3C44FA6D540C89CC04BA3C49E63BF)参照してください。

**属性ソースを有効化するには**

On the [!UICONTROL Create New [or Edit] Customer Attribute Source] page, locate the [!UICONTROL Activate] heading, then click **[!UICONTROL Active]**.

![Step Result](assets/activate_attribute_source.png)

## Adobe Analytics での顧客属性の使用 {#task_7EB0680540CE4B65911B2C779210915D}

現在、
<keyword>
Adobe Analytics
</keyword>を使用すると、データについてレポートし、分析し、マーケティングキャンペーンで適切なアクションを行うことができます。

以下の例は、アップロードした属性に基づいた [!DNL Analytics] セグメントを示しています。このセグメントは、最も頻繁に起動する製品が Photoshop である Photoshop Lightroom の購読者を示しています。

![](assets/08_crs_usecase.png)

セグメントをExperience Cloudに公開すると、Experience CloudオーディエンスおよびAudience Managerで使用できるようになります。

詳しくは、Analytics ヘルプの[顧客属性レポート](https://marketing.adobe.com/resources/help/en_US/reference/?f=reports_customer_attributes)を参照してください。

## Adobe Target での顧客属性の使用 {#task_FC5F9D9059114027B62DB9B1C7D9E257}

Target では、オーディエンスの作成時に「訪問者プロファイル」セクションから顧客属性を選択できます。すべての顧客属性には、リストにプレフィックス [!DNL crs.] が表示されます。これらの属性を、必要に応じて他のデータ属性と組み合わせることで、オーディエンスを構築します。

![](assets/crs-add-attribute-target.png)

Target ヘルプの[新しいオーディエンスの作成](https://marketing.adobe.com/resources/help/en_US/target/target/?f=t_creating_a_new_audience)を参照してください。
