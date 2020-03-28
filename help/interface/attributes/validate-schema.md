---
description: 検証プロセスでは、アップロードした属性（文字列、整数、数値など）に表示名と説明をマッピングできます。これらの設定に基づいてスキーマが作成されます。 このスキーマは、このデータソースにアップロードされる将来のすべてのデータを検証するために使用されます。 このマッピング処理では、元のデータは変更されません。
keywords: customer attributes;core services
seo-description: 検証プロセスでは、アップロードした属性（文字列、整数、数値など）に表示名と説明をマッピングできます。これらの設定に基づいてスキーマが作成されます。 このスキーマは、このデータソースにアップロードされる将来のすべてのデータを検証するために使用されます。 このマッピング処理では、元のデータは変更されません。
seo-title: スキーマの検証
solution: Experience Cloud
title: スキーマの検証
uuid: 163a4dbe-d60b-4089-8ff8-65f7461fbdf7
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# スキーマの検証

検証プロセスでは、アップロードした属性（文字列、整数、数値など）に表示名と説明をマッピングできます。これらの設定に基づいてスキーマが作成されます。 このスキーマは、このデータソースにアップロードされる将来のすべてのデータを検証するために使用されます。 このマッピング処理では、元のデータは変更されません。

>[!NOTE]
>
>検証後にスキーマを更新すると、顧客属性が削除されます。[スキーマの更新（属性の削除）](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C)を参照してください。

**[!UICONTROL 顧客属性ソース]** /新 **[!UICONTROL 規顧客属性ソースを作成]** / **[!UICONTROL 表示/編集スキーマ]**

![](assets/view_edit_schema.png)

[!UICONTROL スキーマの検証]ページでは、スキーマの各行は、アップロードされた CSV ファイルの列を表しています。

![](assets/06_crs_usecase.png)

* **[!UICONTROL データの追加：]**&#x200B;新しい属性データをこのデータソースにアップロードできます。

* **[!UICONTROL スキーマを表示 / 編集：]**&#x200B;次の手順で説明するように、表示名を属性データにマッピングします。

* **[!UICONTROL FTP のセットアップ：]**[ FTP を使用してデータをアップロードします](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)。

* **[!UICONTROL ID 検索：]**`.csv` から顧客 ID（CID）を入力して、その ID の Experience Cloud 情報を検索します。この機能は、訪問者に対して属性データが表示されない理由をトラブルシューティングするのに役立ちます。

   * **[!UICONTROL ECID(Experience Cloud ID):]** 最新のExperience Cloud IDサービスを使用している場合に表示されます。 MCIDサービスを使用しているが、ここにIDが表示されていない場合、Experience CloudはそのCIDのエイリアスを受け取っていません。 つまり、その訪問者がログインしていないか、実装がその ID を渡していません。

   * **[!UICONTROL CID（顧客 ID）：]**&#x200B;この CID と関連付けられている属性。prop または eVar を使用して CID（AVID）をアップロードし、属性は表示されるが AVID は表示されない場合は、訪問者がサイトにログインしていないことを意味します。

   * **[!UICONTROL AVID（Analytics 訪問者 ID）：]** prop または eVar を使用して CID をアップロードする場合に表示されます。これらのIDがExperience Cloudに渡される場合、入力したCIDに関連付けられている訪問者IDがここに表示されます。

また、Experience Cloudで顧客属性ソースとFTPアカウントを作成した後に、FTP経由でデータをアップロードすることもできます。 属性ソースごとに1つのFTPアカウントを作成します。 アップロードされたファイルは、そのアカウントのルートフォルダに保存されます。 データは.csv形式で、アップロードが完了したことを示す2つ目の.finファイルが含まれている必要があります

文字列、整数および数値に適用する名前は、[!DNL Analytics] 指標の作成に使用されます。詳しくは [、ヘルプの「顧客属性レポ](https://docs.adobe.com/help/en/analytics/components/variables/dimensions-reports/reports-customer-attributes.html)[!DNL Analytics] ート」を参照してください。

* **[!UICONTROL 属性：]**&#x200B;アップロードされた `.csv` ファイルから読み出された属性データ。

* **[!UICONTROL タイプ：]**&#x200B;データタイプ。次のようなものがあります。

   * **文字列：** 一連の文字。

   * **整数：** 整数。

   * **数字：** 小数点以下2桁まで設定できます。

* **[!UICONTROL 表示名：]**&#x200B;属性のわかりやすい名前。例えば、*顧客の年齢*&#x200B;を、*顧客となった年数*&#x200B;に変更できます。

* **[!UICONTROL 説明：]**&#x200B;属性のわかりやすい説明。
