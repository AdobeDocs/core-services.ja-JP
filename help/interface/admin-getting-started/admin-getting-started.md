---
description: Admin Console へのログインと Experience Cloud ユーザーの権限および製品プロファイルの管理について説明します。
keywords: コアサービス
seo-description: Admin Console へのログインと Experience Cloud ユーザーの権限および製品プロファイルの管理について説明します。
seo-title: Experience Cloud ユーザーと製品の管理
solution: Marketing Cloud
title: Experience Cloud ユーザーと製品の管理
uuid: aea4e4c3-f543-4e8d-b553-d838418477d6
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# Experience Cloud ユーザーと製品の管理 {#topic_3FCB4099640647E3B2411ADBFCE81909}

Admin Console へのログインと Experience Cloud ユーザーの権限および製品プロファイルの管理について説明します。


<!-- marketing-cloud-identity-management.xml -->

<!-- user_mgmt_admin.xml -->

<!-- domain change for 2018 
<ul id="ul_6654B3993EBE4DE0A3FBCFA5173A52D1"> 
 <li id="li_BE41EB31960B4C079E864FAA2E322BB4"> Private Beta - Support new domain alongside old domain for selected customers (June, 2018) </li> 
 <li id="li_0513CA457FAA4F37A9D5E514DEAF2067"> General Rollout - Serve both old and new domains seamlessly for all customers (Aug, 2018) </li> 
 <li id="li_AB89A6D00A274EB7863D0243757322DE"> Public Beta - Drive solution teams and customers to switch references from old domain to new domain (Aug - Oct, 2018) </li> 
 <li id="li_6FED48B1F361493082102E823EA335F4"> General Availability - Redirect all old domain requests to new domain (Oct, 2018) </li> 
</ul> -->

>[!IMPORTANT]
>
>Admin Console でのユーザー管理には、新しい用語、インターフェイスおよびナビゲーションが導入されています。ここでは、それらの変更について説明するとともに、追加のヘルプリソースへのリンクも示します。このヘルプは、すべての Adobe Cloud 製品を対象とする[管理ユーザーガイド](https://helpx.adobe.com/enterprise/managing/user-guide.html)を補足するものです。

## Experience Cloud ユーザー管理の新機能 {#concept_06A0A13362F644FB90F947238407637A}

Experience Cloud ユーザー管理の最新機能について説明します。


## Admin Console へのログイン {#section_705072FD4EBE4B70BC69EC81F2BB8669}

これまでソリューションでおこなっていた管理者によるユーザー管理の方法が変更されました。今後は、Experience Cloud のユーザーおよび製品を Admin Console で管理します。

**Admin Console にログインするには**

1. Navigate to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#).
1. [Adobe ID または Enterprise ID](https://helpx.adobe.com/enterprise/help/identity.html) とパスワードを入力します。


または、Experience Cloud メニュー（![](assets/menu-icon.png)）で&#x200B;**[!UICONTROL 管理]**／**[!UICONTROL Admin Console を起動]**&#x200B;をクリックします。

**関連するヘルプ**

Creative Cloud および Document Cloud の[管理ユーザーガイド](https://helpx.adobe.com/enterprise/using/users.html)。[ID タイプの管理](https://helpx.adobe.com/enterprise/help/identity.html)など、Experience Cloud のユーザー管理に関連する情報も含まれています。

[サインインとプロファイル設定の管理](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0) - パスワード、組織、および通知の管理について説明します。

## 製品プロファイルとグループ {#section_AB50558124D541CF80A0D3D76D35A4BF}

製品プロファイルの追加は、ソリューション製品およびサービスの従来の管理方法（グループを使用）が変更されたことを示しています。Admin Console では、権限はユーザーに割り当てることができる製品およびサービスのグループである製品プロファイルを基礎とします。

例えば、Analytics では、Analysis Workspace や Report Builder などのレポートツールをレポートスイート、指標、ディメンションなどとともに 1 つのコレクションにまとめることができます。ユーザーを製品プロファイルに追加することにより、ユーザーに権限を割り当てることができます。詳しくは、[製品プロファイルへの Analytics アクセス権限の割り当て](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)を参照してください。

**関連するヘルプ**

[制限付き管理権限の委任](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

Analytics のユーザー権限および製品権限は、Admin Console で管理します。

[製品プロファイルへの Analytics アクセス権限の割り当て](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)（このページ）

**ユーザーアカウントの移行**

Analytics 管理者がユーザーアカウントを Analytics User Management から [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/) / へ移行する際に役立つ Analytics ユーザー ID 移行ツールを入手できます。

アカウントの移行は、顧客ごとに段階的に実施しています。既存のユーザーアカウントを&#x200B;**[!UICONTROL 管理ツール]**／**[!UICONTROL ユーザー管理]**&#x200B;から Admin Console へ移行する順番が来た顧客には、アドビから通知し、サポートを提供します。

移行後、ユーザーはそれぞれの Adobe ID（または Enterprise ID）を使用してログインし、Experience Cloud ソリューションおよびサービスへ認証を [marketing.adobe.com](https://marketing.adobe.com) / でおこないます。従来のログイン（[!DNL my.omniture.com] および [!DNL sc.omniture.com]）でログインしようとしたユーザーは、[!DNL marketing.adobe.com] にリダイレクトされます。

**関連するヘルプ**

[Analytics ユーザー ID の移行](https://marketing.adobe.com/resources/help/en_US/experience-cloud/admin-console/analytics-migration/)

## Target - 製品プロファイルとワークスペース {#section_3860AF177C9E4C7E9C390D36A414F353}

Target では、ワークスペースが製品プロファイルになります。組織でワークスペースを使用すると、特定のユーザーセットを特定のプロパティセットに割り当てることができます。多くの点で、ワークスペースは Adobe Analytics のレポートスイートに似ています。

以下を参照してください。
* [Enterprise ユーザーの権限](https://marketing.adobe.com/resources/help/en_US/target/target/property_channel.html)
* [製品およびプロファイルの管理](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* ビデオ：[Adobe Admin Console で Target ワークスペースを設定する方法](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)




## Campaign - 製品プロファイル、テナント、セキュリティグループ {#section_09CDF75366444CF5810CF321B7C712F3}

Campaign の&#x200B;*テナント*&#x200B;は、Admin Console の製品ページでは&#x200B;*製品*&#x200B;として表示されます。

*セキュリティグループ*&#x200B;は製品プロファイルとして表示されます。

See Managing groups and users for information about security groups and assigning users to security groups.[](https://helpx.adobe.com/campaign/standard/administration/using/managing-groups-and-users.html)

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform Launch は、Admin Console の製品ページに表示されます。Launch 製品プロファイルには、他のソリューションやコアサービスを含めることができます。

See [User Management](https://marketing.adobe.com/resources/help/en_US/experience-cloud/launch/user-management.html) for information about user permissions in the Admin Console and set up Launch-specific options, including assigning rights to profiles.

## Dynamic Tag Manager {#section_3A41CF2BD5994B9891537D063571D4ED}

Dynamic Tag Management へのユーザー招待、ユーザーの役割の割り当て、グループへのユーザーの追加

See [Users and Permissions](https://marketing.adobe.com/resources/help/en_US/dtm/users.html) for information about how to invite users to Dynamic Tag Management and assign user roles and add users to groups.

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Audience Manager ユーザーを作成し、グループに割り当てます。制限（特性、セグメント、リンク先、AlgoModel）を表示することもできます。

See [Administration](https://marketing.adobe.com/resources/help/en_US/aam/c_administration.html) in Audience Manager help.

## Experience Cloud 製品の管理 {#task_16335111C52D40E9BAC73D0699584DBF}

製品プロファイルを作成し、権限グループに割り当てます。

ユーザーを組織に招待する場合は、そのユーザーに製品および製品プロファイルへのアクセス権を付与することができます。ユーザーに制限付き管理権限を委任することもできます。同様に、ユーザーグループを作成し、そのグループを製品プロファイルに追加することによって、アクセス権を有効にすることもできます。

1. In the [Admin Console](https://adminconsole.adobe.com/enterprise/), click **[!UICONTROL Products]**.
1. 「**[!UICONTROL 新しいプロファイル]**」をクリックします。
1. プロファイルの詳細を設定し、「**[!UICONTROL 次へ]**」をクリックします。
1. 「**[!UICONTROL 完了]**」をクリックします。

詳しくは、以下のヘルプ情報を参照してください。

* [製品およびプロファイルの管理](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* Target ヘルプの [Enterprise ユーザーの権限](https://marketing.adobe.com/resources/help/en_US/target/target/property_channel.html)
* ビデオ：[Adobe Admin Console で Target ワークスペースを設定する方法](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)


## 製品プロファイルへの Analytics アクセス権限の割り当て {#task_040673FE3E3E429B9531FBCB8B6A4391}

製品プロファイルに Analytics レポートアクセス権限（レポートスイート、指標、ディメンションなど）を割り当てます。

例えば、特定の指標やディメンション（eVar を含む）およびセグメントや計算指標の作成などの機能に対する権限を持つ、複数の Analytics ツール（[!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics]、および [!UICONTROL Report Builder]）が含まれる製品プロファイルを作成できます。

1. [Admin Console](https://adminconsole.adobe.com/enterprise) にログインしてから、「**[!UICONTROL 製品]**」（または製品名）をクリックします。
1. 製品プロファイルで、「**[!UICONTROL 権限]**」をクリックします（管理者のみクリックできます）。
1. プロファイルの権限の設定：


| 要素 | 説明 |
|--- |--- |
| レポートスイート | 特定のレポートスイートに対する権限を有効にします。 |
| 指標 | トラフィック、コンバージョン、カスタムイベント、ソリューションイベントおよびコンテンツ対応などに対する権限を有効にします。 |
| ディメンション | eVar、トラフィックレポート、ソリューションレポートおよびパスレポートを含む、詳細なレベルでユーザーアクセスをカスタマイズします。 |
| レポートスイートツール | Web サービス、レポートスイートの管理、ツールとレポート、およびダッシュボードの項目に対するユーザー権限を有効にします。 |
| Analytics ツール | 一般的な項目（課金、ログなど）、会社の管理、ツール、Web サービスへのアクセス、Report Builder および Data Connectors の統合に関するユーザー権限を有効にします。Admin Console のカスタマイズカテゴリのカンパニー設定は、Analytics ツールに移動されました。 |



## ユーザーへの管理者ロールの委任 {#task_3A072C4AA9734BC59FFA7E015271BC7E}


<!-- t_admin-roles.xml -->
Admin Console では、組織内の他のユーザーに管理権限を制限付きで委任できます。委任された管理者ロールでは、エンドユーザーに対するソフトウェアアクセスを管理したり、デプロイ機能へのアクセスを提供したりできます。また、サポート代行者としての役割を果たすこともできます。

例えば、次のことができます。

* クリエイティブディレクターが Creative Cloud へのアクセス権を付与できるようにする。
* マーケティングディレクターが Experience Cloud へのアクセス権を付与できるようにする。
* 管理者ロールと副管理者ロールを切り離して、お互いのロールを侵さないようにします。


副管理者ロールを使用すると、必要以上の機能を提供することなく、複数の人に同時に管理を委任できます。

1. Admin Console で「**[!UICONTROL ユーザー]**」をクリックしてから、ユーザー名をクリックします。
1. 「**[!UICONTROL 管理権限を編集]**」をクリックします。
1. ユーザーの管理権限を設定します。
1. 「**[!UICONTROL 次へ]**」をクリックして設定を確認し、「**[!UICONTROL 保存]**」をクリックします。

## サポートされているブラウザーと必要システム構成 {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Experience Cloud でサポートされているブラウザーは次のとおりです。


<!-- browsers.xml -->
**Experience Cloud コアサービス**

* Microsoft の最新の Internet Explorer（Microsoft による Internet Explorer 8、9、10 の[サポートは既に終了しています](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support)。そのため、今後アドビでは、Internet Explorer のこれらのバージョンに対して報告された問題は修正しません）。
* Google Chrome
* Mozilla Firefox
* Apple Safari


**ソリューションと製品の要件**

* [Analysis Workspace および Reports &amp; Analytics](https://marketing.adobe.com/resources/help/en_US/sc/user/?f=requirements)（Adobe Social を含む）
* [Report Builder](https://marketing.adobe.com/resources/help/en_US/arb/?f=system_requirements)
* [Ad Hoc Analysis](https://marketing.adobe.com/resources/help/en_US/dsc/index.html?f=c_sys_reqs)
* [Data Workbench](https://marketing.adobe.com/resources/help/en_US/insight/install/?f=c_Data_Workbench_Client_install)
* [Adobe Target](https://marketing.adobe.com/resources/help/en_US/target/ov/?f=r_supported_browsers)
* [Adobe Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/?f=c_supported_browsers)
* [Adobe Campaign Standard](https://helpx.adobe.com/campaign/standard/start/using/compatible-browsers.html)
* [Adobe Campaign Classic](https://helpx.adobe.com/campaign/kb/compatibility-matrix.html)
