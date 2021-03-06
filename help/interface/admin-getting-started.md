---
title: ユーザーと製品を管理する
description: Admin Console へのログイン方法と、Experience Cloud ユーザーの権限および製品プロファイルの管理方法をご覧ください。Experience Cloud ユーザーへの管理権限の委任、および Experience Cloud に対するブラウザーのサポートについて説明します。
solution: Admin
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: af9eda5b-d984-44b7-a7b3-52dfc4e03d8f
source-git-commit: 271d8496ee617f55741cb2e636eecc869e1ec284
workflow-type: tm+mt
source-wordcount: '1896'
ht-degree: 85%

---

# Experience Cloud ユーザーと製品の管理

Admin Console へのログイン、Experience Cloud ユーザー権限と製品プロファイルの管理、ブラウザーのサポートについて説明します。

>[!IMPORTANT]
>
>次の情報は、Experience Cloud アプリケーションを対象としています。この情報は、すべての Adobe Cloud 製品を対象とする[エンタープライズ管理ユーザーガイド](https://helpx.adobe.com/jp/enterprise/admin-guide.html)の幅広い管理情報を補完するものです。

管理ツールでは、すべての Experience Cloud ユーザーとその詳細に関する、並べ替え可能でフィルタリング可能なリストを確認できます。詳しくは、[管理ツールでの Experience Cloud ユーザーの表示](admin-tool-experience-cloud.md)を参照してください。

## プロビジョニングの更新通知{#provisioning}

更新： **2022 年 7 月 21 日**

>[!IMPORTANT]
>
>Experience Cloudのプロビジョニングに関する次の通知を確認してください。

Adobeは、一部のExperience Cloud製品間の相互運用性を支援する基本的な機能に対するすべてのExperience Cloudのお客様のアクセスを提供するために、プロビジョニングを更新しています。 ユーザーには、Adobe Experience PlatformをExperience Cloud組織に新しい権限として追加し、 [!UICONTROL データ収集] を付属のサービスとして使用します。

Adobe Experience Platform [!UICONTROL データ収集] 次を含む [タグ](https://experienceleague.adobe.com/docs/tags.html?lang=en) を使用すると、シンプルな universal tag management を実現し、信頼性の高い、堅牢で完全なストリーミングデータインフラストラクチャを提供します。 タグを使用すると、顧客体験のデータ収集を簡略化し、エクスペリエンス配信を効率化できます。

**Admin Consoleの変更**

管理者は、次のように、Admin Consoleの変更や追加を確認できます。

* Admin ConsoleのAdobe Experience Platform製品カードには、次が含まれます。

   * Places
   * アシュランス
   * ID 名前空間
   * サンドボックス
   * エクスペリエンスデータモデル
   * スキーマ
   * データストリーム
   * 訪問者 ID

   現在Experience Platformを使用していない組織の場合、 _Adobe Experience Platform_ 上記の機能を含む、Admin Console内の製品。

   現在Experience Platformを使用している組織の場合、 _場所_ は、Experience Platformカードに統合されます。

* Adobe Experience Platformのデータ収集（以前の Launch）およびプライバシーは、他のExperience Platform機能とは別の製品カードとして引き続き表示されます。

新機能の詳細については、各機能のExperience Leagueを参照してください。

* [データ収集](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/reporting-interface/overview-data-collection.html)
* [Places](https://experienceleague.adobe.com/docs/places/using/home.html?lang=ja)
* [アシュランス](https://experienceleague.adobe.com/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance.html%3Flang%3Dde)
* [ID 名前空間](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=ja)
* [サンドボックス](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=ja)
* [エクスペリエンスデータモデル](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ja)
* [スキーマ](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=ja)
* [データストリーム](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=en)
* [訪問者 ID](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html?lang=en#section_3C9F6DF37C654D939625BB4D485E4354)
* [プライバシー](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ja)

## Experience Cloud ユーザー認証（計画移行）{#migration}

2022年2月よりアドビは、組織が個々のプロファイルに対するビジネス権限をより適切に管理できるように、プロファイル管理システムを更新しています。 したがって、個々の Adobe ID（Type1） に対応する個人プロファイルを持つすべてのユーザーは、新しいビジネスプロファイルに移行されます。このプロファイルは _Business ID_（Type2e）に対応しています。

詳しくは、[Adobe Admin Consoleの ID タイプ](https://helpx.adobe.com/jp/enterprise/using/identity.html)を参照してください。

### 移行プロセス

移行の時期が来たら、移行の 30 日前に組織の管理者に通知メールが届きます。

* 移行は午後 10 時までに予定されています。 — 午前 6 時（組織の主要タイムゾーンまたは週末）。
* 移行中、Experience Cloud アプリケーションは 15 分程度、Admin Console は最大 30 分間アクセスできなくなる可能性があります。そうでない場合、この移行はシームレスに行われます。

### 移行後の変更

Admin Console

* 複数のアカウントを持つ管理者が [!UICONTROL Admin Console] にログインする際に、プロファイルセレクターが表示される場合があります。
* 個々の Adobe ID ユーザーは、Business ID に更新されます。
* Business ID ディレクトリは、**[!UICONTROL 設定]**／**[!UICONTROL ID]**／**[!UICONTROL ディレクトリ]**&#x200B;に追加されます。

   ![Admin Console ID — Business ID](assets/identity-home.png)

### 移行後のログイン

この更新では、ログインのエクスペリエンスは変更されません。

1. 同じ認証情報を使用した `experience.adobe.com` へのログイン

1. Business ID に関連付けられた新しいプロファイルが作成されます。 「**[!UICONTROL 参加する]**」または「**[!UICONTROL スキップ]**」するよう求められます。

1. いずれかのオプションを選択すると、既存のランディングページのエクスペリエンスを使用することになります。

1. アドビプロファイルは各ビジネスプランに関連付けられ、追加の Adobe Cloud サービス（Creative Cloud と Document Cloud）から作成されたアセットを整理する機能を提供します。

詳しくは、[アドビプロファイルの概要](https://helpx.adobe.com/jp/enterprise/kb/introducing-adobe-profiles.html)を参照してください。

## 製品プロファイルとは {#section_AB50558124D541CF80A0D3D76D35A4BF}

_[!UICONTROL 製品プロファイル]_&#x200B;は、ユーザーに割り当てることができる製品およびサービスのグループです。Experience Cloud では、権限はユーザーではなく、製品のプロファイルに基づきます。（ただし、管理権限は特定のユーザーに委任できます。）

例えば、Analytics では、Analysis Workspace や Report Builder などのレポートツールをレポートスイート、指標、ディメンションなどとともに 1 つのコレクションにまとめることができます。ユーザーをプロファイルに追加することにより、付与権限を製品プロファイルに割り当てることができます。

* 詳しくは、このページの[製品プロファイルへの Analytics アクセス権限の割り当て](admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)を参照してください。
* このページの[ユーザーへの管理者の役割の委任](#delegate-rights)を参照してください。

## Experience Cloud 製品プロファイルの管理 {#task_16335111C52D40E9BAC73D0699584DBF}

製品プロファイルを作成し、権限グループに割り当てます。

ユーザーを組織に招待する場合は、そのユーザーに製品および製品プロファイルへのアクセス権を付与することができます。ユーザーに制限付き管理権限を委任することもできます。同様に、ユーザーグループを作成し、そのグループを製品プロファイルに追加することによって、アクセス権を有効にすることもできます。

1. [Admin Console](https://adminconsole.adobe.com/enterprise/) で、「**[!UICONTROL 製品]**」を選択します。
1. 組織名を選択します。
1. 「**[!UICONTROL 新規プロファイル]**」を選択します。
1. プロファイルの詳細を設定し、「**[!UICONTROL 保存]**」を選択します。

詳細（および Creative Cloud と Document Cloud 製品管理のヘルプ）については、『[管理ユーザーガイド](https://helpx.adobe.com/jp/enterprise/admin-guide.html/jp/enterprise/using/users.ug.html)』の [ID](https://helpx.adobe.com/jp/enterprise/admin-guide.html/jp/enterprise/using/identity.ug.html) を参照してください。

**関連するヘルプ**

* 管理ユーザーガイドの[製品およびプロファイルの管理](https://helpx.adobe.com/jp/enterprise/admin-guide.html/jp/enterprise/using/manage-products.ug.html)。
* Adobe Target ヘルプの [Enterprise ユーザーの権限](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=ja)。
* ビデオ：[Adobe Admin Console で Adobe Target ワークスペースを設定する方法](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-17521.html?lang=ja)

## ユーザーへの管理者の役割の委任 {#delegate-rights}

Admin Console では、組織内の他のユーザーに管理権限を制限付きで委任できます。委任された管理者の役割では、エンドユーザーに対するソフトウェアアクセスを管理したり、デプロイ機能へのアクセスを提供したりできます。また、サポート代行者としての役割を果たすこともできます。

例えば、次のことができます。

* クリエイティブディレクターが Creative Cloud へのアクセス権を付与できるようにする。
* マーケティングディレクターが Experience Cloud へのアクセス権を付与できるようにする。
* 管理者の役割と副管理者の役割を切り離して、お互いの役割を侵さないようにします。

副管理者の役割を使用すると、必要以上の機能を提供することなく、複数の人に同時に管理を委任できます。

1. Admin Console で「**[!UICONTROL ユーザー]**」を選択してから、ユーザー名を選択します。

   ![Admin Console の管理者権限](assets/edit-admin-rights.png)

1. **[!UICONTROL 管理者権限を編集]**&#x200B;を選択します。

   ![Admin Console での管理者権限の編集](assets/edit-admin-rights-page.png)

1. ユーザーの管理権限を指定します。
1. 「**[!UICONTROL 保存]**」を選択します。

## Analytics ユーザーと製品の管理 {#section_97DE101F92CD494AB073893680992F1A}

製品プロファイルに Analytics レポートのアクセス権限（レポートスイート、指標、ディメンションなど）を割り当てることができます。

例えば、複数の Analytics ツール（[!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics]、[!UICONTROL Report Builder]）を含む製品プロファイルを作成できます。これらのプロファイルには、特定の指標およびディメンション（eVar を含む）に対する権限と、セグメントや計算指標の作成などの機能が含まれます。

1. [Admin Console](https://adminconsole.adobe.com/enterprise) にログインし、「**[!UICONTROL 製品]**」を選択します。
1. [!UICONTROL 製品]ページで、製品を選択してから「**[!UICONTROL 権限]**」を選択します（管理者のみが使用できます）。
1. プロファイルの権限の設定：

| 要素 | 説明 |
|--- |--- |
| レポートスイート | 特定のレポートスイートに対する権限を有効にします。 |
| 指標 | トラフィック、コンバージョン、カスタムイベント、アプリケーションイベントおよびコンテンツ対応などに対する権限を有効にします。 |
| ディメンション | eVar、トラフィックレポート、アプリケーションレポートおよびパスレポートを含む、詳細なレベルでユーザーアクセスをカスタマイズします。 |
| レポートスイートツール | Web サービス、レポートスイートの管理、ツールとレポート、およびダッシュボードの項目に対するユーザー権限を有効にします。 |
| Analytics ツール | 一般的な項目（請求、ログなど）、会社の管理、ツール、web サービスへのアクセス、Report Builder および Data Connectors の統合に関するユーザー権限を有効にします。Admin Console のカスタマイズカテゴリのカンパニー設定は、Analytics ツールに移動されました。 |

**ユーザーアカウントの移行**

Analytics 管理者がユーザーアカウントを Analytics User Management から [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/) / へ移行する際に役立つ Analytics ユーザー ID 移行ツールを入手できます。

アカウントの移行は、顧客ごとに段階的に実施しています。既存のユーザーアカウントを「**[!UICONTROL 管理ツール]**／**[!UICONTROL ユーザー管理]**」から Admin Console へ移行する順番が来た顧客には、アドビから通知し、サポートを提供します。

移行後、ユーザーはそれぞれの Adobe ID（または Enterprise ID）を使用してログインし、Experience Cloud アプリケーションおよびサービスの認証を [experience.adobe.com](https://experience.adobe.com) で行います。従来のログイン（[!DNL my.omniture.com]、[!DNL sc.omniture.com] および [!DNL experiencecloud.adobe.com]）でログインしようとしたユーザーは、[!DNL experience.adobe.com] にリダイレクトされます。

**関連するヘルプ**

* [Admin Console での Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=ja)
* [Analytics ユーザー ID の移行](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/migrate-users/c-migration-tool.html?lang=ja)

## Adobe Target の管理 - 製品プロファイルとワークスペース {#section_3860AF177C9E4C7E9C390D36A414F353}

Adobe Target では、ワークスペースが製品プロファイルになります。組織でワークスペースを使用すると、特定のユーザーセットを特定のプロパティセットに割り当てることができます。多くの点で、Workspaces は Adobe Analytics のレポートスイートに似ています。

以下を参照してください。

* [Enterprise ユーザーの権限](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=en)
* [製品およびプロファイルの管理](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html)
* ビデオ：[Adobe Admin Console で Adobe Target ワークスペースを設定する方法](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-17521.html?lang=en)

## Campaign 製品プロファイル、テナント、セキュリティグループの管理 {#section_09CDF75366444CF5810CF321B7C712F3}

Campaign の&#x200B;*テナント*&#x200B;は、Admin Console の製品ページで&#x200B;*製品*&#x200B;として表示されます。

*セキュリティグループ*&#x200B;は製品プロファイルとして表示されます。

セキュリティグループとセキュリティグループへのユーザーの割り当てについては、[グループとユーザーの管理](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/managing-groups-and-users.html?lang=ja)を参照してください。

## Experience Platform データ収集（Launch）の管理 {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform [!UICONTROL データ収集]（[!UICONTROL Launch]）は、[!UICONTROL Admin Console] の[!UICONTROL 製品]ページに表示されます。Launch 製品プロファイルには、他のアプリケーションやサービスを含めることができます。

[!UICONTROL Platform Launch] にユーザーを招待し、ユーザーの役割と権限を割り当てます。

Admin Console のユーザー権限と Launch 固有のオプションの形式について設定（プロファイルへの権限の割り当てなど）については、[ユーザー権限](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html?lang=ja)を参照してください。

## Adobe Experience Manager as a Cloud Service

Adobe Enterprise の顧客は、Adobe [!UICONTROL Admin Console] では組織として表されます。Adobe Experience Manager のお客様は、Adobe [!UICONTROL Admin Console] を使用して、Adobe Experience Manager as a [!UICONTROL Cloud Service] に対する製品の使用権限や IMS 認証を管理できます。

[Adobe Experience Manager as a Cloud Service の IMS サポート](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=ja)を参照してください。

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Audience Manager ユーザーを作成し、グループに割り当てます。また、制限（特性、セグメント、宛先、[!DNL AlgoModel]）を表示することもできます。

Audience Manager ヘルプの[管理](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/administration/administration-overview.html?lang=ja)を参照してください。

## Experience Cloud でサポートされているブラウザー

* [!DNL Microsoft® Edge]（Microsoft® による Internet Explorer 8、9、10 の[サポートは既に終了しています](https://www.microsoft.com/ja-jp/WindowsForBusiness/End-of-IE-support)。そのため、今後アドビでは、Internet Explorer のこれらのバージョンに対して報告された問題は修正しません。）
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**メモ：** Experience Cloud インターフェイスはこれらのブラウザーをサポートしていますが、個々のアプリケーションがすべてのブラウザーに対応しているわけではありません（例えば、[Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=ja) は [!DNL Opera] をサポートしておらず、[Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=ja) は [!DNL Safari] をサポートしていません）。

### 各ソリューションおよび製品の要件

* [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=en)
* [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/report-builder-setup/system-requirements.html?lang=ja)
* [Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=en)
