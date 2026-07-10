---
title: ユーザーおよび製品ライセンス管理
description: Admin Console for CX Enterprise アプリケーションのユーザーと製品ライセンスを管理します。
application: Experience Cloud
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: c82821c4-aa5d-48ae-8bef-5937fede8db2
autotag-review: '2026-05-12T21:16:07.250Z'
TQID: 'https://experienceleague.adobe.com/tONTr5mo5qLUxNS-q-uHGMCc5jKkURApIR-2RW0aV3w'
product_v2:
  - id: e1971122-7081-4556-9222-8a31bd71800c
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: eb7e29b9-c5e9-4ed0-8e4b-6465dabb3cb1
  - id: f1299f18-ec4b-4531-b2a2-df3b94ff9a68
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 25446910430bf15dcfa0fc70e25e0681f9faeb95
workflow-type: tm+mt
source-wordcount: 1073
ht-degree: 8%

---

# ユーザーおよび製品の管理

Adobe [Admin Console](https://adminconsole.adobe.com/enterprise/)では、ユーザーと製品ライセンスを管理できます。 すべてのAdobe アプリケーションに適用される一般的なID管理に関するヘルプについては、[&#x200B; エンタープライズ版およびグループ版の管理者ガイド &#x200B;](https://helpx.adobe.com/jp/enterprise/admin-guide.html)を参照してください。

このページでは、CX Enterprise管理者に特に役立つ情報を提供し、役割を定義し、エンタープライズガイドの一般的なユーザーおよび製品管理のトピックへのリンクを提供します。

## Admin Consoleの管理者

Admin Consoleには3つの主要な管理ロールがあり、それぞれ特定のレベルのアクセスと責任を持ちます。

| 役割 | 説明 |
| ------- | ------- |
| システム管理者 | フルアクセス – コンソールのすべての側面を管理します。 <br>主な責任：<br><ul><li>ユーザーの追加、削除、管理。</li><li>製品ライセンスの割り当てと取り消し。</li><li>IDと認証の設定</li><li>請求情報の表示と管理。</li><li>追加の管理者とデリゲートの役割を設定します。</li></ul> **組織全体のAdobe環境を管理する**&#x200B;人のIT管理者またはチームリーダーに最適です。 |
| 製品管理者 | 製品固有の管理 – 特定のAdobe製品へのアクセスと権限を制御します。<br>主な責任：<ul><li>特定の製品のライセンスを割り当てて管理します。</li><li>商品プロファイルの作成と管理。</li><li>割り当てられた製品内のユーザーを追加または削除します。</li></ul>   **Marketo EngageやAdobe Creative Cloudなどの特定のソフトウェアを管理する** チーム/ユーザーに最適です。 |
| 製品プロファイル管理者 | 詳細なロール管理：製品内でのユーザーグループと権限の管理に焦点を当てます。<br>主な責任：<ul><li>商品プロファイルの作成と管理。</li><li>プロファイル内で権限と機能アクセスを割り当てます。</li><li>プロファイル内のユーザーを追加または削除します。</li></ul> **特殊なニーズを持つ小規模なグループを管理する**&#x200B;部門のリードまたはチームマネージャーに最適です。<br> 管理者は、組織の要件に応じて、より柔軟に役割を組み合わせることができます。 |

## Admin Console for CX Enterprise

CX Enterprise アプリケーションのIDと製品ライセンスを管理するには、[Admin Console](https://adminconsole.adobe.com/enterprise/)に移動します。

Admin Consoleで管理者として作業を開始する際に必要になる可能性のあるリソースを以下に示します。

### リソースの設定

| ヘルプリンク | 説明 |
| ------- | ------ |
| [IDとシングルサインオンを設定](https://helpx.adobe.com/jp/enterprise/using/set-up-identity.html) | **[!UICONTROL Admin Console]** > **[!UICONTROL Settings]** <br> シングルサインオン（SSO）の有無にかかわらず、異なるID タイプを持つユーザーアカウントを設定する方法について説明します。 Adobe ソフトウェアのSSOを設定し、SAML設定を行い、最も一般的な質問とエラーを確認します。 |
| [&#x200B; ディレクトリ信頼経由で組織を設定](https://helpx.adobe.com/jp/enterprise/using/directory-trust.html) | 別の組織が既に要求しているドメインに対して、ユーザーを認証します。 組織の検索と切り替えについて詳しくは、[CX Enterpriseの組織](organizations.md)を参照してください。 |
| [認証設定（エンタープライズ） &#x200B;](https://helpx.adobe.com/jp/enterprise/using/authentication-settings.html) | Admin Consoleでは、安全性とセキュリティを確保するために、いくつかのパスワード保護レベルとポリシーをサポートしています。 パスワード保護レベルを使用して、組織のすべてのユーザーに適用するように指定できます。 |
| [&#x200B; プライバシーとセキュリティの連絡先](https://helpx.adobe.com/jp/enterprise/using/security-contacts.html) | 組織とユーザーのデータを保護。 当社のソフトウェアソリューションに関するセキュリティインシデントが発生した場合、適切なコンプライアンス担当者に通知が送信されます。 企業には、データ保護、完全性、その他のコンプライアンス事項に特化した役割を持つ人材が揃っています。 したがって、セキュリティ上の問題が発生した場合に迅速に通知を行うために、このような担当者の連絡先情報が重要です。 |

### ユーザー管理

| ヘルプリンク | 説明 |
| ------- | ------- |
| [Adobe IDをリセット &#x200B;](https://helpx.adobe.com/jp/account/individual/sign-in-and-security/security-and-recovery/cant-sign-in-to-adobe-account.html) | ログアウトし、**[!UICONTROL ヘルプのログインを取得]**/**[!UICONTROL パスワードをリセット]**&#x200B;をクリックします。 |
| [複数のユーザーを管理](https://helpx.adobe.com/jp/enterprise/using/bulk-upload-users.html) | **[!UICONTROL Admin Console]** > **[!UICONTROL ユーザー]** <br>CSVの一括アップロードを使用して複数のユーザーをAdmin Consoleに管理する方法について説明します。 |
| [ID タイプ &#x200B;](https://helpx.adobe.com/jp/enterprise/using/identity.html) | ID タイプにより、組織はユーザーのアカウントとデータをさまざまなレベルで制御できます。 ID モデルの選択は、組織がアセットを保存および共有する方法に影響します。 Federated IDとEnterprise ID モデルは組織で作成および管理されますが、Adobe IDは個人で作成および管理されます。 |
| [&#x200B; ユーザー同期ツール &#x200B;](https://helpx.adobe.com/jp/enterprise/using/user-sync.html) （UST） | Adobe User Sync Toolは、組織のID管理システム（Active Directoryなど）とAdobe Admin Console間でユーザーデータを自動的に同期するために使用されるデスクトップアプリケーションです。 管理者は、このツールを使用することで、Adobe製品全体でユーザーのプロビジョニング、更新、非アクティブ化を合理化できます。 |
| [&#x200B; ユーザーの詳細を表示（管理ツール） &#x200B;](admin-tool-experience-cloud.md) | [!UICONTROL 管理ツール &#x200B;]の詳細を含む、すべてのCX Enterprise ユーザーとポリシーの並べ替え可能でフィルター可能なリストを表示します。 |

### レポートとログ

| ヘルプリンク | 説明 |
| ------- | ------- |
| [監査ログ &#x200B;](https://helpx.adobe.com/jp/enterprise/using/audit-logs.html) | **[!UICONTROL インサイト]** > **[!UICONTROL ログ]** > **[!UICONTROL 監査ログ]** <br> Admin Consoleで行われたすべての変更を追跡します。 |


## アプリケーションに特化したリソース

これらのリンクは、特定のCX Enterprise アプリケーションの管理情報を見つけるのに役立ちます。

<!--
| Application | Link to resource|
| ------- | ------- |
|  [!DNL Analytics] <p>Customer Journey Analytics| [Analytics in the Adobe Admin Console overview](https://experienceleague.adobe.com/ja/docs/analytics/admin/admin-console/home) <p>[Administration requirements](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace) |
| [!DNL Audience Manager] | [Audience Manager user migration to Admin Console](https://experienceleague.adobe.com/ja/docs/audience-manager/user-guide/features/administration/admin-console-migration) |
| [!DNL Campaign] v8 |  [Get started with permissions](https://experienceleague.adobe.com/ja/docs/campaign/campaign-v8/admin/permissions/gs-permissions) |
| [!DNL Campaign Standard] to [!DNL Campaign v8] | [User access management from Campaign Standard to Campaign V8](https://experienceleague.adobe.com/ja/docs/campaign-web/acs-to-ac/user-management-acs) |
| [!DNL Commerce] | [Configure the Commerce Admin Integration with Adobe ID](https://experienceleague.adobe.com/ja/docs/commerce-admin/start/admin/ims/adobe-ims-config) |
| [!DNL Dynamic Media Classic] | [Administration setup](https://experienceleague.adobe.com/ja/docs/dynamic-media-classic/using/setup/administration-setup#user_administration) |
| [!DNL Experience Manager as a Cloud Service] |  [Accessing the Admin Console](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console) |
| [!DNL Experience Platform] <p>[!DNL Data Collection] | [Access control UI overview](https://experienceleague.adobe.com/ja/docs/experience-platform/access-control/ui/overview) <p>[Permission management for data collection in Experience Platform](https://experienceleague.adobe.com/ja/docs/experience-platform/collection/permissions)|
| [!DNL GenStudio for Performance Marketing] | [Provision Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/ja/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning) |
| [!DNL Journey Optimizer] | [Manage users and roles](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/access-control/permissions) |
| [!DNL Journey Optimizer B2B Edition] | [User management](https://experienceleague.adobe.com/ja/docs/journey-optimizer-b2b/user/admin/user-management) |
|[!DNL  Journey Orchestration] | [Access management](https://experienceleague.adobe.com/ja/docs/journeys/using/starting-with-journeys/access-management) |
| [!DNL Marketo Engage] | [Understanding Marketo Subscription and User Migration to the Adobe Admin Console](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console) |
| [!DNL Marketo Measure] | [Adobe Admin Console Setup](https://experienceleague.adobe.com/ja/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup) |
| [!DNL Mix Modeler] | [Access controls](https://experienceleague.adobe.com/ja/docs/mix-modeler/using/data-governance/access-controls) |
| [!DNL Pass] | [Get started with Account IQ](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started) |
| [!DNL Target] | [Administrator first steps](https://experienceleague.adobe.com/ja/docs/target/using/administer/start-target) <p> [User management](https://experienceleague.adobe.com/ja/docs/target/using/administer/manage-users/user-management) |
| [!DNL Workfront] | [Manage users in the Adobe Admin Console](https://experienceleague.adobe.com/ja/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console) |

-->

* [Advertising Search, Social, &amp; Commerce](https://experienceleague.adobe.com/en/docs/advertising/search-social-commerce/target/user-administration)
* [Analytics](https://experienceleague.adobe.com/ja/docs/analytics/admin/admin-console/home)
* [Customer Journey Analytics](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace)
* [Audience Manager](https://experienceleague.adobe.com/ja/docs/audience-manager/user-guide/features/administration/admin-console-migration)
* [Campaign v8](https://experienceleague.adobe.com/ja/docs/campaign/campaign-v8/permissions/gs-permissions)
* [Campaign Standard](https://experienceleague.adobe.com/ja/docs/campaign-web/acs-to-ac/user-management-acs)
* [Commerce](https://experienceleague.adobe.com/ja/docs/commerce-admin/start/admin/ims/adobe-ims-config)
* [Dynamic Media Classic](https://experienceleague.adobe.com/ja/docs/dynamic-media-classic/using/setup/administration-setup#user_administration)
* [Experience Manager as a Cloud Service](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console)
* [Experience Platform](https://experienceleague.adobe.com/ja/docs/experience-platform/access-control/ui/overview)および[Data Collection](https://experienceleague.adobe.com/ja/docs/experience-platform/collection/permissions)
* [GenStudio for Performance Marketing](https://experienceleague.adobe.com/ja/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning)
* [Journey Optimizer](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/access-control/permissions)
* [Journey Optimizer B2B edition](https://experienceleague.adobe.com/ja/docs/journey-optimizer-b2b/user/admin/user-management)
* [Journey Orchestration](https://experienceleague.adobe.com/ja/docs/journeys/using/starting-with-journeys/access-management)
* [Marketo Engage](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console)
* [Marketo Measure](https://experienceleague.adobe.com/ja/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup)
* [Mix Modeler](https://experienceleague.adobe.com/ja/docs/mix-modeler/using/data-governance/access-controls)
* [ターゲット](https://experienceleague.adobe.com/ja/docs/target/using/administer/start-target)
* [Workfront](https://experienceleague.adobe.com/ja/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console)

すべてのAdobe アプリケーションのAdmin Console ヘルプの大部分は、[&#x200B; エンタープライズ版およびグループ版の管理ガイド &#x200B;](https://helpx.adobe.com/jp/enterprise/admin-guide.html)に記載されています。

