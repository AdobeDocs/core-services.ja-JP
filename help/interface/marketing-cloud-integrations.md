---
description: Adobe Experience Cloud で利用可能なソリューション統合について説明します。
keywords: 統合
solution: Experience Cloud
title: 'Experience Cloud の統合 '
uuid: a9893c6b-bccc-4fb5-b724-724644c7def5
feature: Admin Console
topic: 管理
role: Administrator
level: Experienced
exl-id: 7f8fa610-32f0-4b18-8054-3ba05436a10e
source-git-commit: 6b6dd0fd0ac51d485877e20bd94322415e80e65e
workflow-type: tm+mt
source-wordcount: '1528'
ht-degree: 55%

---

# Experience Cloud統合の概要

Adobe Experience Cloudは、共通の強力な機能セットを持つ共通のデータプラットフォーム上に構築された、クラス最高の統合アプリケーションとサービスの包括的なセットです。

## Experience Cloud アプリケーションの Platform サービスへの対応 {#section_A3D024994DA3492F8435CFCC4EF035C2}

ヘルプ：[Platform サービスへのアプリケーションの対応](core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)

次の方法について説明しています。

* Experience Cloud で会社をプロビジョニングする。
* 管理者になれるようにする。
* [Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en)を実装する。
* Platformデータ収集を使用して、[!DNL Analytics]および[!DNL Target]実装を最新化する。
* コアサービスの使用を開始する。

ソリューションまたはサービス：

* Activation -Experience Platformデータ収集（以前のLaunch）
* Analytics
* Target 
* [Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en)

## Experience Cloud ID サービス {#section_6ECCCFA2D84D4D4F88C879C799CA9D78}

ID サービスは、Experience Cloud のすべてのソリューションで訪問者を識別する永続的な汎用 ID を提供します。このサービスを、Analytics、Audience Manager、Adobe Target、ビデオハートビートなどのサービスや、その他のExperience Cloudアプリケーションおよび製品のID生成コードの代わりに使用できます。

[Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en)を参照してください。

**適用可能なソリューションまたはサービス**

* [Adobe Analytics](https://experienceleague.adobe.com/docs/id-service/using/home.htmlmcvid-setup-analytics.html?lang=en)
* [Adobe Target](https://experienceleague.adobe.com/docs/id-service/using/home.htmlmcvid-setup-target.html?lang=en)
* [[!UICONTROL Data Workbench]](https://experienceleague.adobe.com/docs/id-service/using/home.htmlmcvid-dwb.html?lang=en)

## オーディエンス {#section_5F60D7B0833348B9A1D74663AADCB42C}

ヘルプ：[Audiences](audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

Experience Cloud オーディエンスライブラリでオーディエンスを作成および管理します。オーディエンスは、次のような各種ソースから作成または取得できます。

* [!DNL Experience Cloud] で作成される新しいソース。
* [!DNL Analytics] に公開された [!DNL Experience Cloud] セグメントから。
* [!DNL Audience Manager] から。

**適用可能なソリューションまたはサービス**

* [Adobe Target のアクティビティ](https://experienceleague.adobe.com/docs/target/using/activities/activities.html?lang=en)
* Audience Manager の[セグメント化](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/audience-analytics-workflow/aam-analytics-segments.html?lang=en)
* [Media Manager](https://enterprise.efrontier.com/CMDashboard?ticket=JrciD7q2bF1y2mDWFHmEyibmxtHqnZFSOMml-n993zOBc-ovZGNZkX5vgePWqKNMoMmPSqf9PkzFeYF4UN6GqSXDVNDvwgnvv9KT8PvVxk8%3D)（ログインが必要）

## 顧客属性 {#section_6A9EA6847F654F129381869E5016626C}

ヘルプ：[顧客属性](attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

>[!NOTE]
>
>顧客属性は、現在は維持中の従来のサービスです。

エンタープライズ顧客データを顧客関係管理（CRM）データベースに取り込んでいる場合は、そのデータを Experience Cloud の顧客属性データソースにアップロードできます。アップロード後は、データを [!DNL Adobe Analytics] と [!DNL Adobe Target] で利用できます。

**適用可能なソリューションまたはサービス**

* Adobe Analytics：[顧客属性レポート](https://experienceleague.adobe.com/docs/analytics/components/variables/dimensions-reports/reports-customer-attributes.html?lang=en)
* Adobe Target：顧客属性に対する Adobe Target の[サブスクリプション](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html?lang=en)の設定

## Experience Cloud Assets {#section_92BC5DFDB0E0499CB0DD34B85E06F79A}

ヘルプ：[Creative Cloud との Experience Cloud フォルダーの共有](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html?lang=en)

>[!NOTE]
>
>アセットは従来のコアサービスで、現在はメンテナンス中です。

Experience Cloud と Creative Cloud の間でフォルダーやアセットを共有します。共有アセットで共同作業をしたり、注釈を付けたり、それらを [!DNL Social] や [!DNL Target] などの Experience Cloud ソリューションで使用したりできます。

**適用可能なソリューションまたはサービス**

* [!DNL Experience Cloud]
* [!DNL Creative Cloud]
* [!DNL Target]
* [!DNL Social]

## Analytics - Analytics での AEM Assets レポート {#section_0A16AE14F128470AA02EFC6457BDCE75}

ヘルプ：[Analytics での AEM Assets レポート](https://experienceleague.adobe.com/docs/analytics/integration/aem-assets-reporting.html?lang=en)

AEM Assets インサイトから提供されるアセットのインプレッション数とクリック数の情報を収集できます。

**適用可能なソリューションまたはサービス**

* [!DNL Analytics]
* [!DNL Experience Manager]

## Audience Manager 統合 {#section_8FEFE1746E26416EB7E73095BBAD5345}

[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/implementation-and-integration.html?lang=en)

Experience Cloud ソリューションや他の外部システムのデータを Audience Manager で操作します。

**適用可能なソリューションまたはサービス**

* [Analytics のサーバー側転送](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=en)
* [Analytics への Audience Manager セグメントの送信](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/experience-cloud-destinations/create-analytics-destination.html?lang=en)
* [Adobe Targetデータ統合](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/aam-target-integration.html?lang=en)

## Activation {#section_A23510A2D57842F6BAD043650C06DE42}

ヘルプ：[はじめに](https://experienceleague.adobe.com/docs/launch/using/get-started/quick-start.html?lang=en#get-started)

Experience Cloud Activation ソリューションを使用して、Experience Cloud ソリューションの設定とデバッグをおこないます。

1. [Experience Platform Launch](https://experienceleague.adobe.com/docs/launch/using/overview.html?lang=en) または [Dynamic Tag Management](https://experienceleague.adobe.com/docs/dtm/using/dtm-home.html?lang=en) を使用して、ページ上で [Adobe Experience Cloud ソリューション](solutions-core-services.md#topic_BD726D3A649E4FC49063029E86B70C62)をアクティベートするコードを挿入します。
1. [Adobe Cloud Platform Auditor](https://experienceleague.adobe.com/docs/auditor/using/overview.html?lang=en) を使用して実装をテストします。

Adobe Experience Cloud Debugger 拡張機能を使用して、Auditor によって検出された問題をデバッグしたり、実装に関する他の情報を調べたりします。

**適用可能なソリューションまたはサービス**

* [Analytics](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=en)
* [Audience Manager](https://experienceleague.adobe.com/docs/dtm/using/tools/audiencemgmt.html?lang=en)
* [Media Manager](https://experienceleague.adobe.com/docs/dtm/using/tools/media-optimizer.html?lang=en)
* [Adobe Target](https://experienceleague.adobe.com/docs/dtm/using/tools/target.html?lang=en)
* [MAC ID サービス](https://experienceleague.adobe.com/docs/dtm/using/tools/macid.html?lang=en)
* [Nielsen トラッキング](https://experienceleague.adobe.com/docs/dtm/using/tools/nielsen.html?lang=en)

## Adobe Target {#section_739716AB6022424CBC38724CDED10701}

ヘルプ：[Adobe Target と Experience Cloud の統合](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=en)

Adobe Target と Adobe Analytics およびその他の Experience Cloud ソリューションを統合して、同じデータ、Audiences、属性および指標を両方のソリューションで使用できるようにします。

**適用可能なソリューションまたはサービス**

* 顧客属性：顧客属性に対する Adobe Target の[サブスクリプション](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html?lang=en)の設定
* Experience Cloud Audiences：[Experience Cloud Audience ライブラリ](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=en)
* Analytics：[Adobe Target のレポートソースとしての Adobe Analytics](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=en)
* Dynamic Tag Management：[DTM を使用した Adobe Target の実装のベストプラクティス](https://experienceleague.adobe.com/docs/dtm/implementing/overview.html?lang=en)
* Audience Manager：[Adobe Audience Manager との Adobe Target データの統合](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/aam-target-integration.html?lang=en)
* Campaign：[Adobe Target と Campaign の統合](https://experienceleague.adobe.com/docs/target/using/integrate/campaign-and-target.html?lang=en)

## Adobe Experience Manager の統合 {#section_32FB010EF8B4429FBC63C8DC2A9BE98F}

ヘルプ：[Experience Managerドキュメント](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=en)

AEM と他のソリューションおよびサードパーティのサービスと統合します。

**適用可能なソリューションまたはサービス**

* [Analytics](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/sitecatalyst.html)
* [Analytics と外部プロバイダー](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/external-providers.html)
* [Experience Cloud](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud.html)
* [Creative Cloud](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/creative-cloud.html)
* [Audience Manager](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/audiencemanager.html)
* [Campaign](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/campaign.html)
* [Scene7](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/scene7.html)
* [Adobe Target](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/target/target-configuring.html)
* [サードパーティのサービス](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/third-party-services.html)（Data Connectors）
* [拡張機能](https://docs.adobe.com/content/docs/en/aem/6-2/develop/extending.html)

## Adobe Experience Manager - Assets {#section_CB865F8EFE4C4147BF8E2E4B66B5A318}

ヘルプ：[Experience Cloud および Creative Cloud との AEM Assets 統合の設定](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/configure-assets-cc-integration.html)

Adobe Experience Manager（AEM）Assets 内のアセットを Adobe Creative Cloud に（またはその逆に）同期します。また、アセットを Experience Cloud に（またはその逆に）同期することもできます。この同期は Experience Cloud を使用してセットアップできます。

**適用可能なソリューションまたはサービス**

* AEM
* Creative Cloud
* [Experience Cloud](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud.html)

## [!DNL Adobe Advertising] {#section_9B1935F8BBC147C89C6DB68A35CB1BAB}

ヘルプ（ログインが必要）：[Adobe Experience Cloud ソリューションおよびサービスとの統合](https://enterprise.efrontier.com/CMDashboard/help/internal/concepts_and_features/media_optimizer_integration_with_adobe_marketing_cloud.htm)

**適用可能なソリューションまたはサービス**

**Analytics:** は、サイトエンゲージメントおよびコンバージョンデータを毎日 [!DNL Adobe Advertising]に送信できます（このデータを広告の最適化とレポート作成に使用します）。また、[!DNL Advertising]は、検索エンジンおよびソーシャルネットワークのトラフィックデータを毎日Analyticsに送信できます。Analyticsでは、Reports &amp; Analytics、Report BuilderおよびAd Hoc Analysisの各機能でデータを利用できます。

**Dynamic Tag Manager:** Dynamic Tag Managerを使用して、検索、ソーシャル、ディスプレイ広告のランディングページに対して、広告のピクセルベースのコンバージョントラッキングタグ [](https://docs.adobe.com/content/help/ja-JP/dtm/using/tools/media-optimizer.html)に加えて、サードパーティのトラッキングタグを作成できます。（[!DNL Advertising]タグを[!DNL Advertising]内に直接作成することもできます）。

**Experience Cloud Audiences：**（表示を管理する広告主）任意の [Adobe Experience Cloud Audiences](https://docs.adobe.com/content/help/ja-JP/core-services/interface/audiences/audience-library.html) を、ディスプレイ広告のターゲットとして使用できます。Adobe Experience Cloudで作成したオーディエンスとAdobe Experience Cloudに公開したAnalyticsのオーディエンスを自動的に使用できます。また、[!DNL Adobe Advertising]アカウントで許可されている場合は、Audience Managerのオーディエンスを使用できます。 Adobe Experience CloudとProfiles &amp; Audiencesへのアクセスおよび[!DNL Adobe Advertising]とAdobe Experience Cloud Audiencesの初期設定について詳しくは、担当のアカウントマネージャーにお問い合わせください。 **注意：** Adobe Target も使用する場合、Adobe Experience Cloud に公開した任意の Audiences も Adobe Target でのアクティビティに使用できます。

**Experience Cloud Assets：**（表示を管理する広告主）任意の Adobe Experience Cloud アセットを、新しいディスプレイベータ表示を使用したディスプレイ広告のクリエイティブとして使用できます。Adobe Experience Cloudアセットにアクセスするには、Adobe Experience Cloud](https://enterprise-test.efrontier.com/CMDashboard/help/internal/getting_started/t_log_in_from_adobe_marketing_cloud.htm)を通じてAdobe広告に[ログインしている必要があります。 Adobe Experience Cloud へのアクセスについて詳しくは、アカウントマネージャーにお問い合わせください。

**Experience Cloud 通知：**&#x200B;各ページの上部にある通知リンクから、検索ベータアラートテンプレートに加えて、Adobe Experience Cloud システムアップデート、投稿、メンションおよびアセット共有から生成されたすべてのアラートを表示できます。通知にアクセスするには、Adobe Experience Cloud](https://enterprise-test.efrontier.com/CMDashboard/help/internal/getting_started/t_log_in_from_adobe_marketing_cloud.htm)を通じてAdobe広告に[ログインしている必要があります。 Adobe Experience Cloud へのアクセスについて詳しくは、アカウントマネージャーにお問い合わせください。
