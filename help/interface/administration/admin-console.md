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
source-git-commit: 77841faeb5b005e4913408edb3e9cfbbdfc8961d
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 5%

---

# ユーザー管理および製品ライセンス

このページでは、一般的なユーザーおよび製品管理ドキュメントへのリンクを含め、Experience Cloud管理者向けの情報を提供します。

すべてのAdobe アプリケーションに適用される一般的な ID 管理ヘルプについては、『 [ エンタープライズおよびチーム管理者ガイド ](https://helpx.adobe.com/jp/enterprise/admin-guide.html) 』を参照してください。

## Admin Consoleの管理者の役割

Admin Consoleには、3 つの主要な管理者の役割が用意されており、それぞれに固有のアクセスレベルと責務レベルがあります。

| 役割 | 説明 |
| ------- | ------- |
| システム管理者 | フルアクセス – コンソールのすべての側面を管理します。 <br> 主な責務：<br><ul><li>ユーザーを追加、削除、管理します。</li><li>製品ライセンスの割り当てと失効。</li><li>ID および認証設定の指定</li><li>請求情報を表示および管理します。</li><li>追加の管理者とデリゲート役割を設定します。</li></ul> **最適：** IT 管理者またはチームリードが、組織のAdobe環境全体を監視します。 |
| 製品管理者 | 製品固有の管理 – 特定のAdobe製品のアクセスと権限を制御します。<br> 主な責任：<ul><li>特定の製品のライセンスを割り当てて管理します。</li><li>製品プロファイルを作成および管理します。</li><li>割り当てられた製品内のユーザーを追加または削除します。</li></ul>   **最適：** Marketo EngageやAdobe Creative Cloudなど、特定のソフトウェアを管理するチームまたはユーザー。 |
| 製品プロファイル管理者 | 詳細な役割管理 – 製品内のユーザーグループと権限の管理に重点を置いています。<br> 主な責務：<ul><li>製品プロファイルを作成および管理します。</li><li>プロファイル内に権限と機能アクセス権を割り当てます。</li><li>プロファイル内のユーザーの追加または削除。</li></ul> **最適な対象：** 部門のリーダーやチームマネージャーが、特殊なニーズを持つ小規模なグループを監督します。 <br> 管理者は、組織の要件に応じて、役割を組み合わせて柔軟性を高めることができます。 |

## Experience CloudのAdmin Console

Experience Cloud アプリケーションの ID および製品ライセンスを管理するには、[Admin Console](https://adminconsole.adobe.com/enterprise/) に移動します。

Admin Consoleの管理者として作業を開始する際に必要になる可能性のあるリソースを次に示します。

### リソースの設定

| ヘルプリンク | 説明 |
| ------- | ------ |
| [ID とシングルサインオンの設定 ](https://helpx.adobe.com/jp/enterprise/using/set-up-identity.html) | Admin Console ]**/**[!UICONTROL  設定 ]**<br> を**[!UICONTROL  リックして、シングルサインオン（SSO）の有無にかかわらず、様々な ID タイプのユーザーのアカウントを設定する方法を説明します。 Adobe ソフトウェア用に SSO を設定し、SAML を設定して、最も一般的な質問とエラーを調べます。 |
| [ ディレクトリ信頼を使用した組織の設定 ](https://helpx.adobe.com/enterprise/using/directory-trust.html) | 別の組織が既に要求しているドメインに対してユーザーを認証します。 組織の検索と切り替えについて詳しくは、[Experience Cloudの組織 ](organizations.md) を参照してください。 |
| [ 認証設定（エンタープライズ） ](https://helpx.adobe.com/enterprise/using/authentication-settings.html) | Admin Consoleでは、安全性とセキュリティを確保するために、複数のパスワード保護レベルおよびポリシーをサポートしています。 パスワード保護レベルを使用して、組織全体のすべてのユーザーに適用するように指定できます。 |
| [ プライバシーおよびセキュリティに関する連絡先 ](https://helpx.adobe.com/enterprise/using/security-contacts.html) | 組織およびユーザーのデータを保護します。 当社のソフトウェアソリューションに関するセキュリティインシデントが発生した場合、適切なコンプライアンス担当者に通知が送信されます。 企業には、データ保護、整合性、その他のコンプライアンスに関する事項に固有の役割を持つスタッフがいます。 したがって、セキュリティインシデントが発生した場合に迅速に通知を受けられるようにするために、これらの担当者の連絡先情報が重要になります。 |

### ユーザー管理

| ヘルプリンク | 説明 |
| ------- | ------- |
| [ 複数ユーザーの管理 ](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) | **[!UICONTROL Admin Console]** > **[!UICONTROL ユーザー]** <br>Admin Consoleへの CSV 一括アップロードを使用して複数のユーザーを管理する方法を説明します。 |
| [ID タイプ ](https://helpx.adobe.com/jp/enterprise/using/identity.html) | ID タイプを使用すると、組織は、ユーザーのアカウントとデータを様々なレベルで制御できます。 ID モデルの選択は、組織のアセットの保存および共有方法に影響します。 Federated ID モデルとEnterprise ID モデルは組織で作成および管理されますが、Adobe ID は個人で作成および管理されます。 |
| [ ユーザー同期ツール ](https://helpx.adobe.com/enterprise/using/user-sync.html) （UST） | Adobe ユーザー同期ツールは、組織の ID 管理システム（Active Directory など）とAdobe Admin Consoleの間でユーザーデータを自動的に同期するために使用されるデスクトップアプリケーションです。 このツールを使用すると、管理者は、Adobe製品全体でユーザーのプロビジョニング、更新、アクティベート解除を合理化できます。 |
| [ ユーザーの詳細の表示（管理ツール） ](admin-tool-experience-cloud.md) | [!UICONTROL  管理ツール ] に、すべてのExperience Cloud ユーザーとポリシーの並べ替え可能でフィルタリング可能なリストと詳細が表示されます。 |

### レポートとログ

| ヘルプリンク | 説明 |
| ------- |------- |
| [ 監査ログ ](https://helpx.adobe.com/enterprise/using/audit-logs.html) | **[!UICONTROL インサイト]**/**[!UICONTROL ログ]**/**[!UICONTROL 監査ログ]** <br> Admin Consoleで行われたすべての変更を追跡します。 |


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

すべてのAdobe アプリケーションに関する Admin Console ヘルプの大部分は、[ エンタープライズおよびチーム管理ガイド ](https://helpx.adobe.com/jp/enterprise/admin-guide.html) に記載されています。
