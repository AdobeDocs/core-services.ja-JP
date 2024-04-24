---
title: ユーザーと製品の管理
description: Admin Console にログインし、Experience Cloud のユーザー権限と製品（製品プロファイル）を管理します。Experience Cloud ユーザーへの管理権限の委任および Experience Cloud に対するブラウザーのサポートについて説明します。
solution: Admin
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: af9eda5b-d984-44b7-a7b3-52dfc4e03d8f
source-git-commit: f229ec33ff721527e6a4c920ea63eabb4102935a
workflow-type: ht
source-wordcount: '1582'
ht-degree: 100%

---

# [!DNL Experience Cloud] でのユーザーおよび製品の管理

Admin Console へのログイン、Experience Cloud ユーザーの権限および製品プロファイルの管理、ブラウザーのサポートについて説明します。

>[!IMPORTANT]
>
>次の情報は、Experience Cloud アプリケーションを対象としています。この情報は、すべての Adobe Cloud 製品を対象とする[エンタープライズ管理ユーザーガイド](https://helpx.adobe.com/jp/enterprise/admin-guide.html)の幅広い管理情報を補完するものです。

管理ツールでは、すべての Experience Cloud ユーザーとその詳細に関する、並べ替え可能でフィルタリング可能なリストを確認できます。詳しくは、[管理ツールでの Experience Cloud ユーザーの表示](admin-tool-experience-cloud.md)を参照してください。

## プロビジョニングの更新通知{#provisioning}

更新日：**2022 年 7 月 20 日（PT）**

>[!IMPORTANT]
>
>Experience Cloud のプロビジョニングに関する次の通知を確認してください。

Adobe は、一部の Experience Cloud 製品間の相互運用性を支援する基本的な機能に対するすべての Experience Cloud のお客様のアクセスを提供するために、プロビジョニングを更新しています。 ユーザーには、新しい使用権限として Experience Cloud 組織に Adobe Experience Platform が追加され、[!UICONTROL データ収集]のサービスが付属します。

Adobe Experience Platform の[!UICONTROL データ収集]には、汎用性のあるタグ管理を簡素化するための[タグ](https://experienceleague.adobe.com/ja/docs/tags)が含まれており、信頼性の高い、堅牢で完全なストリーミングデータインフラストラクチャを提供します。 タグを使用すると、顧客体験のデータ収集を簡略化し、エクスペリエンス配信を効率化できます。

**[!DNL Admin Console]** の変更点

管理者は、次のように、[!DNL Admin Console] の変更や追加を確認できます。

* Admin Console の Adobe Experience Platform 製品カードには、次が含まれます。

   * Places
   * Assurance
   * ID 名前空間
   * サンドボックス
   * エクスペリエンスデータモデル
   * スキーマ
   * データストリーム
   * 訪問者 ID

  現在 Experience Platform を使用していない組織の場合、上記の機能を含む _Adobe Experience Platform_ 製品が [!DNL Admin Console] に表示されます。

  現在 Experience Platform を使用している組織の場合、 _Places_ は Experience Platform カードに統合されます。

* Adobe Experience Platform のデータ収集（以前の Launch）およびプライバシーは、他の Experience Platform 機能とは別の製品カードとして引き続き表示されます。

新機能の詳細については、Experience League の各ページを参照してください。

* [データ収集](https://experienceleague.adobe.com/docs/discontinued/using/reports-and-analytics.html?lang=ja)
* [Places](https://experienceleague.adobe.com/ja/docs/places/using/home)
* [Assurance](https://experienceleague.adobe.com/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance.html?lang=ja)
* [ID 名前空間](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=ja)
* [サンドボックス](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=ja)
* [エクスペリエンスデータモデル](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ja)
* [スキーマ](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=ja)
* [データストリーム](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=ja)
* [訪問者 ID](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html?lang=ja#section_3C9F6DF37C654D939625BB4D485E4354)
* [プライバシー](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ja)

## Experience Cloud ユーザー認証（計画移行）{#migration}

2022年2月よりアドビは、組織が個々のプロファイルに対するビジネス権限をより適切に管理できるように、プロファイル管理システムを更新しています。 したがって、個々の Adobe ID（Type1） に対応する個人プロファイルを持つすべてのユーザーは、新しいビジネスプロファイルに移行されます。このプロファイルは _Business ID_（Type2e）に対応しています。

ID タイプについて詳しくは、[Adobe [!DNL Admin Console] の ID タイプ](https://helpx.adobe.com/jp/enterprise/using/identity.html)を参照してください。

### 移行プロセス

移行の時期が来たら、移行の 30 日前に組織の管理者に通知メールが届きます。

* 移行は午後 10 時から午前 6 時（組織の主要タイムゾーンまたは週末に基づく）の間に予定されています。
* 移行中、Experience Cloud アプリケーションは 15 分程度、[!DNL Admin Console] は最大 30 分間アクセスできなくなる可能性があります。そうでない場合、この移行はシームレスに行われます。

### 移行後の変更

[!DNL Admin Console]

* 複数のアカウントを持つ管理者が [!DNL Admin Console] にログインする際に、プロファイルセレクターが表示される場合があります。
* 個人の Adobe ID ユーザーは、Business ID に更新されます。
* Business ID ディレクトリは、**[!UICONTROL 設定]**／**[!UICONTROL ID]**／**[!UICONTROL ディレクトリ]**&#x200B;に追加されます。

  ![[!DNL Admin Console] ID - ビジネス ID](assets/identity-home.png)

### 移行後のログイン

この更新では、ログインのエクスペリエンスは変更されません。

1. 同じ資格情報を使用した `experience.adobe.com` へのログイン

1. Business ID に関連付けられた新しいプロファイルが作成されます。 「**[!UICONTROL 参加する]**」または「**[!UICONTROL スキップ]**」するよう求められます。

1. いずれかのオプションを選択すると、既存のランディングページのエクスペリエンスを使用することになります。

1. アドビプロファイルは各ビジネスプランに関連付けられ、追加のアドビのクラウドサービス（Creative Cloud と Document Cloud）から作成されたアセットを整理する機能を提供します。

詳しくは、[アドビプロファイルの概要](https://helpx.adobe.com/jp/enterprise/kb/introducing-adobe-profiles.html)を参照してください。

## 製品プロファイルとは {#section_AB50558124D541CF80A0D3D76D35A4BF}

_[!UICONTROL 製品プロファイル]_&#x200B;は、ユーザーに割り当てることができる製品とサービスのグループです。Experience Cloud では、権限はユーザーではなく、製品のプロファイルに基づきます。（ただし、管理権限は特定のユーザーに委任できます。）

例えば、Analytics では、Analysis Workspace や Report Builder などのレポートツールをレポートスイート、指標、ディメンションなどとともに 1 つのコレクションにまとめることができます。ユーザーをプロファイルに追加することにより、付与権限を割り当てることができます。

* 詳しくは、このページの「[製品プロファイルへの Analytics アクセス権限の割り当て](admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)」を参照してください。
* このページの[ユーザーへの管理者の役割の委任](#delegate-rights)を参照してください。

## Experience Cloud 製品プロファイルの管理 {#task_16335111C52D40E9BAC73D0699584DBF}

製品プロファイルを作成し、権限グループに割り当てます。

ユーザーを組織に招待する場合は、そのユーザーに製品および製品プロファイルへのアクセス権を付与することができます。ユーザーに制限付き管理権限を委任することもできます。同様に、ユーザーグループを作成し、そのグループを製品プロファイルに追加することによって、アクセス権を有効にすることもできます。

1. [[!DNL Admin Console] ](https://adminconsole.adobe.com/enterprise/)で、「**[!UICONTROL 製品]**」を選択します。
1. 組織名を選択します。
1. 「**[!UICONTROL 新規プロファイル]**」を選択します。
1. プロファイルの詳細を設定し、「**[!UICONTROL 保存]**」を選択します。

詳細（および Creative Cloud と Document Cloud 製品管理のヘルプ）については、『[管理ユーザーガイド](https://helpx.adobe.com/jp/enterprise/using/users.html)』の [ID](https://helpx.adobe.com/jp/enterprise/using/identity.html) を参照してください。

**関連するヘルプ**

* [!DNL Admin Console] での[ユーザーの管理](https://helpx.adobe.com/jp/enterprise/using/users.html)
* [!DNL Admin Console] で、[製品およびプロファイルを管理](https://helpx.adobe.com/jp/enterprise/using/manage-products.html)します。
* Adobe Target ヘルプの [Enterprise ユーザーの権限](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=ja)。
* ビデオ：[Adobe  [!DNL Admin Console] での Adobe Target Workspaces の設定方法](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-17521.html?lang=ja)

## ユーザーへの管理者の役割の委任 {#delegate-rights}

[!DNL Admin Console] では、組織内の他のユーザーに管理権限を制限付きで委任できます。委任された管理者の役割では、エンドユーザーに対するソフトウェアアクセスを管理したり、デプロイ機能へのアクセスを提供したりできます。また、サポート代行者としての役割を果たすこともできます。

例えば、次のことができます。

* クリエイティブディレクターが Creative Cloud へのアクセス権を付与できるようにする。
* マーケティングディレクターが Experience Cloud へのアクセス権を付与できるようにする。
* 管理者の役割と副管理者の役割を切り離して、お互いの役割を侵さないようにします。

副管理者の役割を使用すると、必要以上の機能を提供することなく、複数の人に同時に管理を委任できます。

1. [!DNL Admin Console] で「**[!UICONTROL ユーザー]**」を選択し、ユーザー名を選択します。

   ![[!DNL Admin Console]](assets/edit-admin-rights.png) での管理者権限

1. 「**[!UICONTROL 管理者権限を編集]**」を選択します。

   ![[!DNL Admin Console]](assets/edit-admin-rights-page.png) での管理者権限の編集

1. ユーザーの管理権限を指定します。
1. 「**[!UICONTROL 保存]**」を選択します。

## Analytics ユーザーと製品の管理 {#section_97DE101F92CD494AB073893680992F1A}

製品プロファイルに Analytics レポートのアクセス権限（レポートスイート、指標、ディメンションなど）を割り当てることができます。

例えば、複数の Analytics ツール（[!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics]、[!UICONTROL Report Builder]）を含む製品プロファイルを作成できます。これらのプロファイルには、特定の指標およびディメンション（eVar を含む）に対する権限と、セグメントや計算指標の作成などの機能が含まれます。

1. [[!DNL Admin Console]](https://adminconsole.adobe.com/enterprise) にログインし、「**[!UICONTROL 製品]**」を選択します。
1. [!UICONTROL 製品]ページで、製品を選択してから「**[!UICONTROL 権限]**」を選択します（管理者のみが使用できます）。
1. プロファイルの権限の設定：

| 要素 | 説明 |
|--- |--- |
| レポートスイート | 特定のレポートスイートに対する権限を有効にします。 |
| 指標 | トラフィック、コンバージョン、カスタムイベント、アプリケーションイベントおよびコンテンツ対応などに対する権限を有効にします。 |
| ディメンション | eVar、トラフィックレポート、アプリケーションレポートおよびパスレポートを含む、詳細なレベルでユーザーアクセスをカスタマイズします。 |
| レポートスイートツール | Web サービス、レポートスイートの管理、ツールとレポート、およびダッシュボードの項目に対するユーザー権限を有効にします。 |
| Analytics ツール | 一般的な項目（請求、ログなど）、会社の管理、ツール、web サービスへのアクセス、Report Builder および Data Connectors の統合に関するユーザー権限を有効にします。[!DNL Admin Console] のカスタマイズカテゴリの会社設定は、Analytics ツールに移動されました。 |

**ユーザーアカウントの移行**

Analytics 管理者がユーザーアカウントを Analytics User Management から [Adobe  [!DNL Admin Console]](https://adminconsole.adobe.com/enterprise/) へ移行する際に役立つ Analytics ユーザー ID 移行ツールを利用できます。

アカウントの移行は、顧客ごとに段階的に実施しています。既存のユーザーアカウントを&#x200B;**[!UICONTROL 管理ツール]**／**[!UICONTROL ユーザー管理]**&#x200B;から [!DNL Admin Console] へ移行する際には、アドビから通知が届き、サポートが提供されます。

移行後、ユーザーはそれぞれの Adobe ID（または Enterprise ID）を使用してログインし、Experience Cloud アプリケーションおよびサービスの認証を [experience.adobe.com](https://experience.adobe.com) で行います。従来のログイン（[!DNL my.omniture.com]、[!DNL sc.omniture.com] および [!DNL experiencecloud.adobe.com]）でログインしようとしたユーザーは、[!DNL experience.adobe.com] にリダイレクトされます。

**関連するヘルプ**

* [ [!DNL Admin Console] での Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=ja)
* [Analytics ユーザー ID の移行](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/user-product-management/migrate-users/c-migration-tool.html?lang=ja)

## Adobe Target の管理 - 製品プロファイルと Workspaces {#section_3860AF177C9E4C7E9C390D36A414F353}

Adobe Target では、Workspaces が製品プロファイルになります。組織でワークスペースを使用すると、特定のユーザーセットを特定のプロパティセットに割り当てることができます。多くの点で、Workspaces は Adobe Analytics のレポートスイートに似ています。

以下を参照してください。

* [Enterprise ユーザーの権限](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=ja)
* [製品およびプロファイルの管理](https://helpx.adobe.com/jp/enterprise/using/manage-products.html)
* ビデオ：[Adobe  [!DNL Admin Console] での Adobe Target ワークスペースの設定方法](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-17521.html?lang=ja)

## Campaign 製品プロファイル、テナント、セキュリティグループの管理 {#section_09CDF75366444CF5810CF321B7C712F3}

Campaign の&#x200B;*テナント*&#x200B;は、Admin Console の製品ページでは&#x200B;*製品*&#x200B;として表示されます。

*セキュリティグループ*&#x200B;は製品プロファイルとして表示されます。

セキュリティグループとセキュリティグループへのユーザーの割り当てについては、[グループとユーザーの管理](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/managing-groups-and-users.html?lang=ja)を参照してください。

## Experience Platform データ収集の管理 {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform [!UICONTROL データ収集]は、[!UICONTROL Admin Console] の[!UICONTROL 製品]ページに表示されます。データ収集製品プロファイルには、他のアプリケーションやサービスを含めることができます。

[!UICONTROL Platform データ収集]にユーザーを招待し、ユーザーの役割と権限を割り当てます。

[!DNL Admin Console] のユーザー権限とプロファイルへの権限の設定について詳しくは、[ユーザー権限](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html?lang=ja)を参照してください。

## Adobe Experience Manager as a Cloud Service

Adobe Enterprise の顧客は、Adobe [!DNL Admin Console] では組織として表されます。Experience Manager の顧客は、Adobe [!DNL Admin Console] を使用して、Experience Manager as a [!UICONTROL Cloud Service] に対する製品の使用権限や IMS 認証を管理できます。

[Adobe Experience Manager as a Cloud Service の IMS サポート](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/security/ims-support.html?lang=ja)を参照してください。

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Audience Manager ユーザーを作成し、グループに割り当てます。また、制限（特性、セグメント、宛先、[!DNL AlgoModel]）を表示することもできます。

Audience Manager ヘルプの[管理](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/administration/administration-overview.html?lang=ja)を参照してください。

## Experience Cloud でサポートされているブラウザー

* [!DNL Microsoft® Edge]（Microsoft® による Internet Explorer 8、9、10 の[サポートは既に終了しています](https://www.microsoft.com/ja-jp/WindowsForBusiness/End-of-IE-support)。そのため、今後アドビでは、Internet Explorer のこれらのバージョンに対して報告された問題は修正しません。）
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**メモ：** Experience Cloud インターフェイスはこれらのブラウザーをサポートしていますが、個々のアプリケーションがすべてのブラウザーに対応しているわけではありません（例えば、[Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/sys-reqs.html?lang=ja) は [!DNL Opera] をサポートしておらず、[!DNL Adobe Target] は [!DNL Safari] をサポートしていません）。

### 各ソリューションおよび製品の要件

* [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/sys-reqs.html?lang=ja)
* [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/report-builder-setup/system-requirements.html?lang=ja)
