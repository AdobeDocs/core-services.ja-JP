---
description: 管理コンソールへのサインイン、Experience Cloudユーザー権限と製品プロファイルの管理、およびブラウザーサポートについて説明します。
keywords: core services
seo-description: 管理コンソールへのサインイン、Experience Cloudユーザー権限と製品プロファイルの管理、およびブラウザーサポートについて説明します。
seo-title: Experience Cloud ユーザーと製品の管理
solution: Experience Cloud
title: Experience Cloud ユーザーと製品の管理
uuid: aea4e4c3-f543-4e8d-b553-d838418477d6
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Experience Cloud ユーザーと製品の管理 {#topic_3FCB4099640647E3B2411ADBFCE81909}

管理コンソールへのサインイン、Experience Cloudユーザー権限と製品プロファイルの管理、およびブラウザーサポートについて説明します。

>[!IMPORTANT]
>
>Admin Console でのユーザー管理には、新しい用語、インターフェイスおよびナビゲーションが導入されています。ここでは、それらの変更について説明するとともに、追加のヘルプリソースへのリンクも示します。This help supplements the information in the [Enterprise Administration User Guide](https://helpx.adobe.com/enterprise/managing/user-guide.html) for all Adobe cloud products.

## Experience Cloud ユーザー管理の新機能 {#concept_06A0A13362F644FB90F947238407637A}

Experience Cloud ユーザー管理の最新機能について説明します。

<!-- ### Business ID type

Adobe is now introducing a new identity type: **Business ID**. This identity type, improves the control of user and product management, and content, while increasing the flexibility of Experience Cloud and Creative Cloud storage usage among your team. With the introduction of this new identity type, Adobe is migrating all Adobe IDs (owned by the individual) used for business to the new Business IDs (owned by the organization).

If you're an existing Creative Cloud for enterprise or teams customer, Adobe will migrate all your users on the Admin Console with Adobe IDs to Business IDs. If you're a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID. 

Beginning May 89, 2020, enterprise admins cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a users was a member of multiple organizations before the migration.) -->

### 管理ツール

管理者は、すべてのExperience Cloudユーザーとその詳細の並べ替え可能なフィルター可能なリストを管理ツールで表示できます。 管理ツ [ールのExperience Cloudユーザーの表示を参照してください](admin-tool-experience-cloud.md)。

## Admin Console へのログイン {#section_705072FD4EBE4B70BC69EC81F2BB8669}

管理者は、ソリューションでユーザーを管理しなくなりました。 Experience Cloudのユーザーと製品の管理が、管理コンソールで行われるようになりました。

**Admin Console にログインするには**

1. Navigate to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#).
1. Adobe IDまたは [Enterprise IDとパスワードを入力します](https://helpx.adobe.com/enterprise/help/identity.html) 。

Alternatively, from the Experience Cloud menu ( ![](assets/menu-icon.png)), click **[!UICONTROL Administration]** > **[!UICONTROL Launch Admin Console]**.

**関連するヘルプ**

[Creative CloudおよびDocument Cloudの管理](https://helpx.adobe.com/enterprise/using/users.html) ユーザーガイドを参照してください。 IDタイプの管理など、Experience Cloudのユーザー管理に関連する情 [報があります](https://helpx.adobe.com/enterprise/help/identity.html)。

[ログインとプロファイル設定の管理](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0) - パスワード、組織、および通知の管理について説明します。

## 製品のプロファイルとグループ {#section_AB50558124D541CF80A0D3D76D35A4BF}

製品プロファイルの追加は、ソリューション製品やサービスの以前の管理方法（グループを使用）からの移行を示します。 管理コンソールでは、権限は製品プロファイルに基づいて決まります。製品プロファイルは、ユーザーに割り当て可能な製品とサービスのグループです。

例えば、Analyticsでは、Analysis WorkspaceやReport Builderなどのレポートツールのコレクションと、レポートスイート、指標、ディメンションなどを設定できます。 ユーザーを製品プロファイルに追加することで、ユーザーに権限を付与できます。 See [Assign Analytics access permissions to a product profile](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391).

**関連するヘルプ**

[制限付き管理権限の委任](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

Analytics のユーザー権限および製品権限は、Admin Console で管理します。

[製品プロファイルへの Analytics アクセス権限の割り当て](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)（このページ）

**ユーザーアカウントの移行**

Analytics 管理者がユーザーアカウントを Analytics User Management から [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/) / へ移行する際に役立つ Analytics ユーザー ID 移行ツールを入手できます。

アカウントの移行は、顧客ごとに段階的に実施しています。Adobe will notify and assist you when it is your time to migrate existing user accounts from **[!UICONTROL Admin Tools]** > **[!UICONTROL User Management]** to the Admin Console.

After the migration, users sign in using their Adobe ID (or Enterprise ID) and authenticate to their Experience Cloud solutions and services at [experiencecloud.adobe.com](https://experiencecloud.adobe.com). 従来のログイン（[!DNL my.omniture.com] および [!DNL sc.omniture.com]）でログインしようとしたユーザーは、[!DNL experiencecloud.adobe.com] にリダイレクトされます。

**関連するヘルプ**

[AnalyticsユーザーIDの移行](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Adobe Target - product profiles vs workspaces {#section_3860AF177C9E4C7E9C390D36A414F353}

Adobe Targetでは、ワークスペースは製品プロファイルです。 組織は、特定のユーザーのセットを特定のプロパティのセットに割り当てることができます。 多くの点で、ワークスペースは Adobe Analytics のレポートスイートに似ています。

以下を参照してください。
* [Enterprise User Permissions](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html)
* [製品とプロファイルの管理](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* ビデオ：Adobe管 [理コンソールでのAdobe Targetワークスペースの設定方法](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Campaign - 製品プロファイル、テナント、セキュリティグループ {#section_09CDF75366444CF5810CF321B7C712F3}

Campaign の&#x200B;*テナント*&#x200B;は、Admin Console の製品ページでは&#x200B;*製品*&#x200B;として表示されます。

*セキュリティグループは* 、製品プロファイルとして表示されます。

セキュリテ [ィグループとセキュリティグループへの](https://helpx.adobe.com/campaign/standard/administration/using/managing-groups-and-users.html) 「ユーザーの割り当て」の詳細は、「グループとユーザーの管理」を参照してください。

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

エクスペリエンスプラットフォームの起動は、管理コンソールの製品ページに表示されます。 起動製品プロファイルに他のソリューションやサービスを含めることができます。

管理コン [ソールでのユーザー権限、およびプロファイルへの権限の割り当てを含む起動固有のオプションの設定については、「ユーザー管理](https://docs.adobelaunch.com/launch-reference/administration/user-permissions) 」を参照してください。

## Dynamic Tag Manager {#section_3A41CF2BD5994B9891537D063571D4ED}

Dynamic Tag Management へのユーザー招待、ユーザーの役割の割り当て、グループへのユーザーの追加

See [Users and Permissions](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) for information about how to invite users to Dynamic Tag Management and assign user roles and add users to groups.

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Audience Managerユーザーを作成し、グループに割り当てます。 制限（特性、セグメント、宛先およびAlgoModel）を表示することもできます。

Audience Managerヘル [プの](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) 「管理」を参照してください。

## Experience Cloud 製品の管理 {#task_16335111C52D40E9BAC73D0699584DBF}

製品プロファイルを作成し、権限グループに割り当てます。

ユーザーを組織に招待する場合、製品と製品プロファイルへのアクセスをユーザーに付与できます。 また、制限付き管理権限をユーザーに委任することもできます。 同様に、ユーザーグループを作成し、そのグループを製品プロファイルに追加してアクセスを有効にすることもできます。

1. In the [Admin Console](https://adminconsole.adobe.com/enterprise/), click **[!UICONTROL Products]**.
1. 「**[!UICONTROL 新しいプロファイル]**」をクリックします。
1. プロファイルの詳細を設定し、「**[!UICONTROL 次へ]**」をクリックします。
1. **[!UICONTROL 完了]** をクリックします。

その他のヘルプは、次のURLを参照してください。

* [製品とプロファイルの管理](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* [Adobe Targetヘルプの](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html) 「エンタープライズユーザー権限」を参照してください。
* ビデオ：Adobe管 [理コンソールでのAdobe Targetワークスペースの設定方法](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 製品プロファイルへの Analytics アクセス権限の割り当て {#task_040673FE3E3E429B9531FBCB8B6A4391}

製品プロファイルに Analytics レポートアクセス権限（レポートスイート、指標、ディメンションなど）を割り当てます。

例えば、特定の指標やディメンション（eVar を含む）およびセグメントや計算指標の作成などの機能に対する権限を持つ、複数の Analytics ツール（[!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics]、および [!UICONTROL Report Builder]）が含まれる製品プロファイルを作成できます。

1. Sign in to the [Admin Console](https://adminconsole.adobe.com/enterprise), then click **[!UICONTROL Products]** (or click your product name).
1. 製品プロファイルで、「**[!UICONTROL 権限]**」をクリックします（管理者のみクリックできます）。
1. プロファイルの権限の設定：

| 要素 | 説明 |
|--- |--- |
| レポートスイート | 特定のレポートスイートに対する権限の有効化 |
| 指標 | トラフィック、コンバージョン、カスタムイベント、ソリューションイベント、コンテンツ対応などの権限を有効にします。 |
| ディメンション | eVar、トラフィックレポート、ソリューションレポート、パスレポートなど、詳細なレベルでユーザーアクセスをカスタマイズします。 |
| レポートスイートツール | Webサービス、レポートスイートの管理、ツールとレポート、およびダッシュボードの項目に関するユーザー権限を有効にします。 |
| Analytics ツール | 一般的な項目（課金、ログなど）、会社の管理、ツール、Web サービスへのアクセス、Report Builder および Data Connectors の統合に関するユーザー権限を有効にします。Admin Console のカスタマイズカテゴリのカンパニー設定は、Analytics ツールに移動されました。 |

## ユーザーへの管理者ロールの委任 {#task_3A072C4AA9734BC59FFA7E015271BC7E}

管理コンソールでは、制限付き管理権限を組織内の他のユーザーに委任できます。 委任された役割を使用すると、エンドユーザーに対するソフトウェアアクセスの管理、アクセス展開機能の提供、およびサポート委任としての機能をユーザーに提供できます。

例えば、次の操作が可能です。

* クリエイティブディレクターがCreative Cloudへのアクセスを許可する。
* マーケティングディレクターがExperience Cloudへのアクセスを許可します。
* この2つの役割を別々にして、お互いの役割を超えないようにします。

これらの役割を使用すると、必要以上の機能を提供することなく、同時に他のユーザーに管理を委任できます。

1. Admin Console で「**[!UICONTROL ユーザー]**」をクリックしてから、ユーザー名をクリックします。
1. 「**[!UICONTROL 管理権限を編集]**」をクリックします。
1. ユーザーの管理権限を設定します。
1. 「**[!UICONTROL 次へ]**」をクリックして設定を確認し、「**[!UICONTROL 保存]**」をクリックします。

## サポートされているブラウザーと必要システム構成 {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Experience Cloudでサポートされるブラウザー。

Experience Cloudでサポートされるブラウザーは次のとおりです。

* [!DNL Microsoft Edge] (Microsoftは、 [Internet Explorer](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) 8、9、10のサポートを終了しました。 したがって、アドビでは、これらの特定のバージョンのInternet Explorerに関して報告された問題を修正しません)。
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**メモ：** Experience Cloud インターフェイスはこれらのブラウザーをサポートしていますが、個々のソリューションがすべてのブラウザーに対応しているわけではありません(For example, [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html) does not support [!DNL Opera], and [Adobe Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html) does not support [!DNL Safari].)

**ソリューションと製品の要件**

* [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html)
* [Report Builder](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html)
