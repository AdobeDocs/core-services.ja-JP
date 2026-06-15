---
description: CX Enterprise アセットフォルダーをCreative Cloud ユーザーと共有する方法について説明します。
solution: Experience Cloud
title: Experience Cloud アセットフォルダーの共有
uuid: 105cf627-0148-4bf8-ab6a-7afa612e198c
feature: Assets
topic: Administration
role: Admin
level: Experienced
exl-id: 32f4723e-0e66-46b6-b0c2-ae47b9a06a87
TQID: https://experienceleague.adobe.com/RC2C4CKPhWEO3O4k7baoAqknTj3qj-23Ic1bXtv2zP4
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
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 474
ht-degree: 37%

---

# CX Enterprise アセットフォルダーの共有

CX EnterpriseとCreative Cloud間でフォルダーとアセットを共有します。 Adobe Adobe Targetなどの顧客体験管理システム向けアプリケーションでは、共有アセットの共同作業、注釈付け、使用できます。 共有フォルダーはCX Enterpriseから作成する必要があります。

**共有の利点**

* クリエイティブ制作物の確認、承認および公開ワークフローを効率化できます。
* 複数の場所に分散された作業中ファイルやバージョンの管理にかかる時間を短縮できます。
* クリエイティブなアセットをより効果的に追跡および管理できます。
* 企業セキュリティを強化できます。
* クリエイティブとマーケターの間でファイルを共有、保存および送信できます。

Creative Cloud ユーザーがアセットにアクセスする前に、CX Enterpriseで許可リストに登録されている必要があります。 [Creative Cloud ユーザーの管理](manage-cc-users.md)を参照してください。

**CX Enterprise アセットフォルダーを共有するには**

1. アセットフォルダーで、**[!UICONTROL Creative Cloudに共有]**&#x200B;をクリックします。

   ![Creative Cloud で共有](../../assets/asset-share-cc.png)
1. 「Creative Cloudに共有」ページで、ユーザーを検索し、「**[!UICONTROL 追加]**」をクリックします。

   ![Creative Cloud ユーザーを追加](../../assets/asset-share-cc-page.png)

1. 「**[!UICONTROL 共有]**」をクリックします。
1. [!DNL Creative Cloud] デスクトップを起動し（またはブラウザーで[!UICONTROL Creative Cloud ファイル &#x200B;] ページに移動）、リクエスト通知を探します。

   ![リクエスト通知](../../assets/cc_share_request.png)
1. リクエストを開き、**[!UICONTROL 同意]**&#x200B;をクリックします。

   ![リクエストを承認](../../assets/cc_share_accept.png)
1. フォルダーの内容にアクセスするには、**[!UICONTROL フォルダーを開く]** （または&#x200B;**[!UICONTROL Web]**&#x200B;で表示）をクリックします。

   ![Web で表示](../../assets/creative_cloud_open_folder.png)
1. 共有アセットにコメントを追加して続行します。

   Creative Cloudで、画像を選択し、**[!UICONTROL アクティビティ]**&#x200B;をクリックして、画像にコメントを追加できます。 コメントは、[!DNL Creative Cloud] と [!DNL CX Enterprise] のアセットで同期されます。

   ![画像にコメントを追加](../../assets/asset_comment_cc.png)

   CX Enterpriseで、画像を選択してからタイムラインアイコンを選択し、画像にコメントを追加します。 コメントは、Creative CloudおよびCX Enterpriseのアセットで同期されます。

   ![画像にコメントを追加](../../assets/asset_comment_mac.png)

1. フォルダーの共有を解除するには、「**[!UICONTROL Share Using Creative Cloud]**」（[手順3](share.md)と同様）をクリックし、「X」を選択してユーザーを削除してから、「**[!UICONTROL Share]**」をクリックします。

   ![フォルダーの共有を解除する](../../assets/asset_remove_user.png)

   Creative Cloud ユーザーをすべて削除すると、そのフォルダーの共有が解除され、Creative Cloud ユーザーはそれらにアクセスできなくなります。

共有アセットを使用する他の方法には、アクティビティの画像に対して、Adobe Targetの[&#x200B; オファーライブラリ &#x200B;](https://experienceleague.adobe.com/docs/target/using/experiences/offers/manage-content.html?lang=ja)でアセットを読み込んだり入れ替えたりすることが含まれます。

Creative Cloud にフォルダーを共有すると、フォルダー上に Creative Cloud のロゴが表示されます。

![フォルダー上の Creative Cloud のロゴ](../../assets/asset-cc-logo.png)

関連するヘルプ：

* [Creative Cloud ヘルプ – ファイルの管理と同期](https://helpx.adobe.com/jp/creative-cloud/help/sync-creative-cloud-files.html)
* [Creative Cloud ヘルプ – 他のユーザーとの共同作業](https://helpx.adobe.com/jp/creative-cloud/help/collaboration.html)
* [Creative Cloud ヘルプ - Collaboration FAQ](https://helpx.adobe.com/jp/creative-cloud/help/collaboration-faq.html)

## Adobe Target とのアセットの共有について

[!DNL Adobe Target]でアクティビティを作成する場合、[!UICONTROL &#x200B; オファーライブラリ &#x200B;]で画像を入れ替える際に、共有の画像アセットを使用できます。

[!DNL Target] ヘルプの[オファーライブラリ](https://experienceleague.adobe.com/docs/target/using/experiences/offers/manage-content.html?lang=ja)を参照してください。

