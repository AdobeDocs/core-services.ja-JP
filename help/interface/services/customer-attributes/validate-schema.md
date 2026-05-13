---
description: Adobe CX Enterpriseで [!DNL Customer Attributes]  スキーマを検証する方法について説明します。
solution: Experience Cloud
title: ' [!DNL Customer Attributes]  スキーマの検証方法'
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 776d1fd3-c733-4970-a76b-4c3c0119ee77
TQID: https://experienceleague.adobe.com/J-AaDn4HtD1bS-VCPn2XiPLVBbTnYyl5o1NpJ9HFj1g
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 308
ht-degree: 43%

---

# スキーマの検証

検証プロセスでは、アップロードした属性（文字列、整数、数値など）に表示名と説明をマッピングできます。

これらの設定に基づいてスキーマが作成されます。 このスキーマは、このデータソースに今後アップロードされるすべてのデータの検証に使用されます。 マッピングプロセスによって元のデータが変更されることはありません。

>[!NOTE]
>
>検証後にスキーマを更新すると、顧客属性が削除されます。 [スキーマの更新（属性の削除）](t-crs-usecase.md)を参照してください。

**スキーマを検証するには**

1. [!DNL Customer Attributes]で、編集する属性ソースをクリックします。

1. **[!UICONTROL Edit Customer Attribute Source]**&#x200B;で、**[!UICONTROL File Upload]**&#x200B;をクリックします。

1. [!UICONTROL File Upload and Schema Validation] ページで、**[!UICONTROL Actions]** > **[!UICONTROL View/Edit Schema]**&#x200B;をクリックします

   ![スキーマの編集](assets/actions.png)

   [!UICONTROL Edit Schema] ページでは、スキーマの各行が、アップロードされたCSV ファイルの列を表します。

   ![CX Enterpriseのスキーマページを編集](assets/schema-edit.png)

**アクション**

* **[!UICONTROL Add Data:]**&#x200B;このデータソースに新しい属性データをアップロードします。

* **[!UICONTROL View/Edit Schema:]**&#x200B;次の手順で説明するように、表示名を属性データにマッピングします。

* **[!UICONTROL FTP Setup:]** FTP アカウントを作成して[FTP](t-upload-attributes-ftp.md)経由でデータをアップロードします（オプション）。

* **[!UICONTROL ID Lookup:]** `.csv`から顧客ID （CID）を入力して、そのIDのCX Enterprise情報を検索します。 この機能は、訪問者に対して属性データが表示されない理由をトラブルシューティングするのに役立ちます。

   * **[!UICONTROL ECID (CX Enterprise ID):]**&#x200B;最新のCX Enterprise ID サービスを使用している場合に表示されます。 MCID サービスを利用していても、ここにリストされているIDがない場合、CX EnterpriseはそのCIDのエイリアスを受信していません。 つまり、その訪問者がログインしていないか、実装がその ID を渡していません。

   * **[!UICONTROL CID (customer ID):]**&#x200B;このCIDに関連付けられている属性。 prop または eVar を使用して CID（AVID）をアップロードし、属性は表示されるが AVID は表示されない場合は、訪問者がサイトにログインしていないことを意味します。

   * **[!UICONTROL AVID (Analytics visitor ID):]** PropまたはeVarを使用してCIDをアップロードする場合に表示されます。 これらのIDがCX Enterpriseに渡されている場合、入力したCIDに関連付けられている訪問者IDがここに表示されます。
