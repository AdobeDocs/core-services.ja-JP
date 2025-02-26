---
title: ユーザーと製品のライセンス管理
description: Experience Cloud アプリケーション用のAdmin Consoleでユーザーおよび製品ライセンスを管理します。
application: Experience Cloud
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: c82821c4-aa5d-48ae-8bef-5937fede8db2
source-git-commit: e2e6c0daf8f765fe76f9c7bd44042d91dce142f2
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 5%

---

# ユーザー管理および製品ライセンス

このページでは、一般的なユーザーおよび製品管理ドキュメントへのリンクを含め、Experience Cloud管理者向けの情報を提供します。

すべてのAdobe アプリケーションに適用される一般的な ID 管理ヘルプについては、『 [ エンタープライズおよびチーム管理者ガイド ](https://helpx.adobe.com/jp/enterprise/admin-guide.html) 』を参照してください。

次の節では、Admin Console ヘルプ内のリソースへのリンクを示します。

## Admin Consoleの設定

Experience Cloud アプリケーションの ID および製品ライセンスを管理するには、[Admin Console](https://adminconsole.adobe.com/enterprise/) に移動します。

* [ID とシングルサインオンの設定 ](https://helpx.adobe.com/jp/enterprise/using/set-up-identity.html) - シングルサインオン（SSO）の有無にかかわらず、様々な ID タイプのユーザーのアカウントを設定する方法を説明します。 Adobe ソフトウェア用に SSO を設定し、SAML を設定して、最も一般的な質問とエラーを調べます。

* [ ディレクトリの信頼を使用した組織の設定 ](https://helpx.adobe.com/enterprise/using/directory-trust.html) - ディレクトリの信頼を使用して、別の組織が既に要求しているドメインに対してユーザーを認証します。

  組織について詳しくは、[Experience Cloudの組織 ](organizations.md) を参照してください。

* [Authentication settings （enterprise） ](https://helpx.adobe.com/enterprise/using/authentication-settings.html) - Admin Consoleでは、安全性とセキュリティを確保するために、複数のパスワード保護レベルおよびポリシーをサポートしています。 パスワード保護レベルを使用して、組織全体のすべてのユーザーに適用するように指定できます。 Adobe カスタマーケアには 3 つのレベルのセキュリティがあります。

* [ プライバシーとセキュリティの連絡先 ](https://helpx.adobe.com/enterprise/using/security-contacts.html) - Adobeでは、組織およびユーザーのデータの保護に重点を置いています。 当社のソフトウェアソリューションに関するセキュリティインシデントが発生した場合、適切なコンプライアンス担当者に通知が送信されます。

  企業には、データ保護、整合性、その他のコンプライアンスに関する事項に固有の役割を持つスタッフがいます。 したがって、セキュリティインシデントが発生した場合に迅速に通知を受けられるようにするために、これらの担当者の連絡先情報が重要になります。

## ユーザー管理

* [ 複数のユーザーの管理 ](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html)CSV の一括アップロード - Adobe Admin Consoleで CSV の一括アップロードを使用して複数のユーザーを管理する方法について説明します。

* [ID タイプ ](https://helpx.adobe.com/jp/enterprise/using/identity.html) - ID タイプを使用すると、組織は、ユーザーのアカウントとデータを様々なレベルで制御できます。 ID モデルの選択は、組織のアセットの保存および共有方法に影響します。 Federated ID モデルとEnterprise ID モデルは組織で作成および管理されますが、Adobe ID は個人で作成および管理されます。

* [User Sync Tool](https://helpx.adobe.com/enterprise/using/user-sync.html) （UST） – Adobe User Sync Tool は、組織の ID 管理システム（Active Directory など）とAdobe Adobe Admin Consoleの間でユーザーデータを同期するプロセスを自動化するデスクトップアプリケーションです。 このツールを使用すると、管理者は、Adobe製品全体でユーザーのプロビジョニング、更新、アクティベート解除を合理化できます。

  ユーザー同期ツールを使用すると、ディレクトリサービスとAdobe システムの間でユーザーデータ（ロール、グループ、アクセス権限など）を自動的に同期することで、ユーザーアカウントとライセンスの管理を簡略化できます。 このツールは、特に大規模なチームを持つ企業で役立ちます。 これにより、一貫性とセキュリティを維持しながら、ユーザーが権利を持つ製品やサービスにのみアクセスできるようにします。

* [ ユーザーの詳細の表示（管理ツール） ](admin-tool-experience-cloud.md) – 管理者は、[!UICONTROL  管理ツール ] で、詳細を含むすべてのExperience Cloud ユーザーとポリシーの並べ替え可能でフィルタリング可能なリストを表示できます。

## レポートとログ

* [ 監査ログ ](https://helpx.adobe.com/enterprise/using/audit-logs.html) Admin Consoleで行われたすべての変更を追跡します。

上記の場所に記載されていないヘルプについては、[ エンタープライズおよびチーム管理者ガイド ](https://helpx.adobe.com/jp/enterprise/admin-guide.html) を参照してください。

## アプリケーション固有のリソース

これらのリンクは、特定のExperience Cloud アプリケーションの管理情報を検索する場合に役立ちます。

<!-- | Application | Link to resource|
| ------- | ------- |
|  [!DNL Analytics] <p>Customer Journey Analytics| [Analytics in the Adobe Admin Console overview](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home) <p>[Administration requirements](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace) |
| [!DNL Audience Manager] | [Audience Manager user migration to Admin Console](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/administration/admin-console-migration) |
| [!DNL Campaign] v8 |  [Get started with permissions](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/admin/permissions/gs-permissions) |
| [!DNL Campaign Standard] to [!DNL Campaign v8] | [User access management from Campaign Standard to Campaign V8](https://experienceleague.adobe.com/en/docs/campaign-web/acs-to-ac/user-management-acs) |
| [!DNL Commerce] | [Configure the Commerce Admin Integration with Adobe ID](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-config) |
| [!DNL Dynamic Media Classic] | [Administration setup](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/setup/administration-setup#user_administration) |
| [!DNL Experience Manager as a Cloud Service] |  [Accessing the Admin Console](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console) |
| [!DNL Experience Platform] <p>[!DNL Data Collection] | [Access control UI overview](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/overview) <p>[Permission management for data collection in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/collection/permissions)|
| [!DNL GenStudio for Performance Marketing] | [Provision Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning) |
| [!DNL Journey Optimizer] | [Manage users and roles](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/permissions) |
| [!DNL Journey Optimizer B2B Edition] | [User management](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management) |
|[!DNL  Journey Orchestration] | [Access management](https://experienceleague.adobe.com/en/docs/journeys/using/starting-with-journeys/access-management) |
| [!DNL Marketo Engage] | [Understanding Marketo Subscription and User Migration to the Adobe Admin Console](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console) |
| [!DNL Marketo Measure] | [Adobe Admin Console Setup](https://experienceleague.adobe.com/en/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup) |
| [!DNL Mix Modeler] | [Access controls](https://experienceleague.adobe.com/en/docs/mix-modeler/using/data-governance/access-controls) |
| [!DNL Pass] | [Get started with Account IQ](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started) |
| [!DNL Target] | [Administrator first steps](https://experienceleague.adobe.com/en/docs/target/using/administer/start-target) <p> [User management](https://experienceleague.adobe.com/en/docs/target/using/administer/manage-users/user-management) |
| [!DNL Workfront] | [Manage users in the Adobe Admin Console](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console) |

 -->

* [Analytics](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home)
* [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace)
* [Audience Manager](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/administration/admin-console-migration)
* [Campaign v8](https://experienceleague.adobe.com/ja/docs/campaign/campaign-v8/admin/permissions/gs-permissions)
* [Campaign Standard](https://experienceleague.adobe.com/en/docs/campaign-web/acs-to-ac/user-management-acs)
* [Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-config)
* [Dynamic Media Classic](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/setup/administration-setup#user_administration)
* [Experience Manager as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console)
* [Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/overview) および [ データ収集 ](https://experienceleague.adobe.com/en/docs/experience-platform/collection/permissions)
* [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning)
* [Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/permissions)
* [Journey OptimizerB2B edition](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management)
* [Journey Orchestration](https://experienceleague.adobe.com/en/docs/journeys/using/starting-with-journeys/access-management)
* [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console)
* [Marketo Measure](https://experienceleague.adobe.com/en/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup)
* [Mix Modeler](https://experienceleague.adobe.com/en/docs/mix-modeler/using/data-governance/access-controls)
* [Adobe Pass](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started)
* [Target](https://experienceleague.adobe.com/en/docs/target/using/administer/start-target)
* [Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console)