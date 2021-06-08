---
title: ユーザーと製品を管理する
description: Admin Consoleにログインし、ユーザーの権限と製品プロファイルをExperience Cloudする方法を説明します。 管理者権限をExperience Cloudユーザーに委任する方法と、ブラウザーでのExperience Cloudのサポートについて説明します。
solution: Admin
index: true
feature: Admin Console
topic: 管理
role: Administrator
level: Experienced
exl-id: af9eda5b-d984-44b7-a7b3-52dfc4e03d8f
source-git-commit: ebefd433e96da422674e7ee71c8988d4011fed11
workflow-type: tm+mt
source-wordcount: '1276'
ht-degree: 48%

---

# Experience Cloud ユーザーと製品の管理

Admin Console へのログイン、Experience Cloud ユーザーの権限および製品プロファイルの管理、ブラウザーのサポートについて説明します。

>[!IMPORTANT]
>
>次の情報は、特にExperience Cloud・アプリケーション向け。 この情報は、すべてのAdobeクラウド製品を対象とする『[エンタープライズ管理ユーザーガイド](https://helpx.adobe.com/jp/enterprise/admin-guide.html)』に記載されている、より広範な管理情報を補足するものです。

管理ツールでは、すべてのExperience Cloudユーザーとその詳細に関する、並べ替え可能でフィルタリング可能なリストを表示できます。 詳しくは、[管理ツールでの Experience Cloud ユーザーの表示](admin-tool-experience-cloud.md)を参照してください。

## 製品プロファイルとは {#section_AB50558124D541CF80A0D3D76D35A4BF}

[!UICONTROL 製品プ] ロファイルは、ユーザーに割り当てることができる製品およびサービスのグループです。Experience Cloudでは、権限はユーザーではなく、製品のプロファイルに基づきます。 （ただし、管理権限は特定のユーザーに委任できます）。

例えば、Analyticsでは、Analysis WorkspaceやReport Builderなどのレポートツールのコレクションと、レポートスイート、指標、ディメンションを設定できます。 ユーザーをプロファイルに追加することで、製品プロファイルに権限を付与できます。

* 詳しくは、このページの「[製品プロファイルへの Analytics アクセス権限の割り当て](admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)」を参照してください。
* このページの[ユーザーへの管理者ロールの委任](#delegate-rights)を参照してください。

## Experience Cloud製品プロファイルの管理 {#task_16335111C52D40E9BAC73D0699584DBF}

製品プロファイルを作成し、権限グループに割り当てることができます。

ユーザーを組織に招待する場合は、そのユーザーに製品および製品プロファイルへのアクセス権を付与することができます。ユーザーに制限付き管理権限を委任することもできます。同様に、ユーザーグループを作成し、そのグループを製品プロファイルに追加することによって、アクセス権を有効にすることもできます。

1. [Admin Console](https://adminconsole.adobe.com/enterprise/) で、「**[!UICONTROL 製品]**」をクリックします。
1. 組織名をクリックします。
1. 「**[!UICONTROL 新しいプロファイル]**」をクリックします。
1. プロファイルの詳細を設定し、「**[!UICONTROL 保存]**」をクリックします。

詳細については、『管理Creative Cloudガイド』の[ID](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/identity.ug.html)を参照してください。[](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/users.ug.html)

**関連するヘルプ**

* [製品およびプロファ](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html) イルの管理は、管理ユーザーガイドで行います。
* Adobe Target ヘルプの [Enterprise ユーザーの権限](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=en)
* ビデオ：[Adobe Admin Console で Adobe Target ワークスペースを設定する方法](https://helpx.adobe.com/jp/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

<!-- ## What's new in Experience Cloud user management {#concept_06A0A13362F644FB90F947238407637A}

Learn about the latest features in Experience Cloud user and product management.

### Business ID type

Adobe is introducing an identity type called Business ID. This identity type improves the control of user and product management. Adobe is migrating all Adobe IDs (owned by individuals) that are used for business to the new enterprise Business IDs owned by your organization.

If you are an existing Experience Cloud customer, Adobe will migrate all your users with Adobe IDs in the Admin Console to Business IDs. If you are a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID.

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a user was a member of multiple organizations before the migration.)

Beginning May 2020, enterprise administrators cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM-->

## ユーザーへの管理者ロールの委任 {#delegate-rights}

Admin Console では、組織内の他のユーザーに管理権限を制限付きで委任できます。委任された管理者ロールでは、エンドユーザーに対するソフトウェアアクセスを管理したり、デプロイ機能へのアクセスを提供したりできます。また、サポート代行者としての役割を果たすこともできます。

例えば、次のことができます。

* クリエイティブディレクターが Creative Cloud へのアクセス権を付与できるようにする。
* マーケティングディレクターが Experience Cloud へのアクセス権を付与できるようにする。
* 管理者ロールと副管理者ロールを切り離して、お互いのロールを侵さないようにします。

副管理者ロールを使用すると、必要以上の機能を提供することなく、複数の人に同時に管理を委任できます。

1. Admin Console で「**[!UICONTROL ユーザー]**」をクリックしてから、ユーザー名をクリックします。

   ![](assets/edit-admin-rights.png)

1. 「**[!UICONTROL 管理権限を編集]**」をクリックします。

   ![](assets/edit-admin-rights-page.png)

1. ユーザーの管理者権限を指定します。
1. 「**[!UICONTROL 保存]**」をクリックします。

## Analyticsユーザーと製品の管理 {#section_97DE101F92CD494AB073893680992F1A}

製品プロファイルにAnalyticsレポートアクセス権限（レポートスイート、指標、ディメンションなど）を割り当てることができます。

例えば、複数のAnalyticsツール([!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics]、[!UICONTROL Report Builder])を含む製品プロファイルを作成できます。 これらのプロファイルには、特定の指標およびディメンション（eVarを含む）に対する権限と、セグメントや計算指標の作成などの機能が含まれます。

1. [Admin Console](https://adminconsole.adobe.com/enterprise)にログインし、「**[!UICONTROL 製品]**」をクリックします。
1. [!UICONTROL Products]ページで、製品をクリックしてから「 」をクリックし、「 **[!UICONTROL 権限]** 」をクリックします（管理者のみが使用できます）。
1. プロファイルの権限の設定：

| 要素 | 説明 |
|--- |--- |
| レポートスイート | 特定のレポートスイートに対する権限を有効にします。 |
| 指標 | トラフィック、コンバージョン、カスタムイベント、ソリューションイベントおよびコンテンツ対応などに対する権限を有効にします。 |
| ディメンション | eVar、トラフィックレポート、ソリューションレポートおよびパスレポートを含む、詳細なレベルでユーザーアクセスをカスタマイズします。 |
| レポートスイートツール | Web サービス、レポートスイートの管理、ツールとレポート、およびダッシュボードの項目に対するユーザー権限を有効にします。 |
| Analytics ツール | 一般的な項目（課金、ログなど）、会社の管理、ツール、Webサービスへのアクセス、Report BuilderおよびData Connectorsの統合に関するユーザー権限を有効にします。 Admin Console のカスタマイズカテゴリのカンパニー設定は、Analytics ツールに移動されました。 |

**ユーザーアカウントの移行**

Analytics 管理者がユーザーアカウントを Analytics User Management から [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/) / へ移行する際に役立つ Analytics ユーザー ID 移行ツールを入手できます。

アカウントの移行は、顧客ごとに段階的に実施しています。既存のユーザーアカウントを「**[!UICONTROL 管理ツール]**／**[!UICONTROL ユーザー管理]**」から Admin Console へ移行する順番が来た顧客には、アドビから通知し、サポートを提供します。

移行後、ユーザーはAdobe ID(またはEnterprise ID)を使用してログインし、Experience Cloudソリューションおよびサービスへの認証を[experience.adobe.com](https://experience.adobe.com)でおこないます。 従来のログイン（[!DNL my.omniture.com]、[!DNL sc.omniture.com]および[!DNL experiencecloud.adobe.com]）でログインしようとすると、ユーザーは[!DNL experience.adobe.com]にリダイレクトされます。

**関連するヘルプ**

詳しくは、[AnalyticsのユーザーIDの移行](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=en)を参照してください。

## Adobe Targetの管理 — 製品プロファイルとワークスペース {#section_3860AF177C9E4C7E9C390D36A414F353}

Adobe Target では、ワークスペースが製品プロファイルになります。組織でワークスペースを使用すると、特定のユーザーセットを特定のプロパティセットに割り当てることができます。多くの点で、ワークスペースは Adobe Analytics のレポートスイートに似ています。

以下を参照してください。

* [Enterprise ユーザーの権限](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=en)
* [製品およびプロファイルの管理](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html)
* ビデオ：[Adobe Admin Console で Adobe Target ワークスペースを設定する方法](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Campaign製品プロファイル、テナント、セキュリティグループの管理 {#section_09CDF75366444CF5810CF321B7C712F3}

Campaign の&#x200B;*テナント*&#x200B;は、Admin Console の製品ページでは&#x200B;*製品*&#x200B;として表示されます。

*セキュリティグループ*&#x200B;は製品プロファイルとして表示されます。

セキュリティグループとセキュリティグループへのユーザーの割り当てについては、[グループとユーザーの管理](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/managing-groups-and-users.html?lang=en)を参照してください。

## Experience Platformデータ収集の管理(Launch) {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform[!UICONTROL データ収集]([!UICONTROL Launch])は、[!UICONTROL Admin Console]の[!UICONTROL Products]ページに表示されます。 Launch 製品プロファイルには、他のソリューションやサービスを含めることができます。

[!UICONTROL Platform Launch] にユーザーを招待し、ユーザーの役割と権限を割り当てます。

Admin Consoleでのユーザー権限と、Launch固有のオプションの設定（プロファイルへの権限の割り当てを含む）については、[ユーザー権限](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html?lang=ja#admin)を参照してください。

## Experience Manager as a Cloud Service

Adobeのエンタープライズのお客様は、Adobe[!UICONTROL Admin Console]では組織として表されます。 Experience Managerのお客様は、Adobe[!UICONTROL Admin Console]を使用して、Experience Managerに対する製品の使用権限や、[!UICONTROL Cloud Service]としてのIMS認証を管理できます。

[Cloud ServiceとしてのExperience ManagerのIMSサポート](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=ja)を参照してください。

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Audience Manager ユーザーを作成し、グループに割り当てます。また、制限（特性、セグメント、宛先、[!DNL AlgoModel]）を表示することもできます。

Audience Manager ヘルプの[管理](https://experienceleague.adobe.com/docs/dtm/using/admin/users.html?lang=en)を参照してください。

## Experience Cloudでサポートされているブラウザー

* [!DNL Microsoft® Edge] (Microsoft®は、 [Internet ](https://www.microsoft.com/ja-jp/WindowsForBusiness/End-of-IE-support) Explorer 8、9および10のサポートを終了しました。そのため、Adobeでは、Internet Explorerのこれらのバージョンに対して報告された問題は修正されません)。
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**注意：** Experience Cloudインターフェイスはこれらのブラウザーをサポートしていますが、個々のアプリケーションがすべてのブラウザーに対応しているわけではありません。（例えば、[Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=en) は [!DNL Opera] をサポートしておらず、[Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=en) は [!DNL Safari] をサポートしていません）。

### 各ソリューションおよび製品の要件

* [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=en)
* [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/report-builder-setup/system-requirements.html?lang=en)
* [Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=en)
