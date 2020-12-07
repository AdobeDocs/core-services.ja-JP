---
description: Adobe Experience Cloud で利用可能なソリューション統合について説明します。
keywords: integrations
solution: Experience Cloud
title: Experience Cloudの統合 |Adobe Experience Cloud
uuid: a9893c6b-bccc-4fb5-b724-724644c7def5
translation-type: tm+mt
source-git-commit: 4bea0c29afa580dc63b21535ce5c275cd649c9a5
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 99%

---


# Experience Cloud の統合

Adobe Experience Cloud は、共通の強力な機能セットを持つ共通のデータプラットフォーム上に構築された、クラス最高の統合ソリューションの包括的なセットです。

## Experience Cloud アプリケーションの Platform サービスへの対応 {#section_A3D024994DA3492F8435CFCC4EF035C2}

ヘルプ：[Platform サービスへのアプリケーションの対応](core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)

次の方法について説明しています。

* Experience Cloud で会社をプロビジョニングする。
* 管理者になれるようにする。
* [Experience Cloud ID サービス](https://docs.adobe.com/content/help/ja-JP/id-service/using/home.html)を実装する。
* DTM を使用して [!DNL Analytics] および [!DNL Target] 実装を最新化する。
* コアサービスの使用を開始する。

ソリューションまたはサービス：

* Activation - Experience Platform Launch（推奨）または Dynamic Tag Management
* Analytics
* Target 
* [Experience Cloud ID サービス](https://docs.adobe.com/content/help/ja-JP/id-service/using/home.html)

## Experience Cloud ID サービス {#section_6ECCCFA2D84D4D4F88C879C799CA9D78}

ID サービスは、Experience Cloud のすべてのソリューションで訪問者を識別する永続的な汎用 ID を提供します。このサービスを、Analytics、Audience Manager、Adobe Target、ビデオハートビートなどのサービスや、その他の Experience Cloud のソリューションまたは機能の ID 生成コードの代わりに使用できます。

[Experience Cloud ID サービス](https://docs.adobe.com/content/help/ja-JP/id-service/using/home.html)を参照してください。

**適用可能なソリューションまたはサービス**

* [Adobe Analytics](https://docs.adobe.com/content/help/ja-JP/id-service/using/home.htmlmcvid-setup-analytics.html)
* [Adobe Target](https://docs.adobe.com/content/help/ja-JP/id-service/using/home.htmlmcvid-setup-target.html)
* [[!UICONTROL Data Workbench]](https://docs.adobe.com/content/help/ja-JP/id-service/using/home.htmlmcvid-dwb.html)

## オーディエンス {#section_5F60D7B0833348B9A1D74663AADCB42C}

ヘルプ：[Audiences](audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

Experience Cloud オーディエンスライブラリでオーディエンスを作成および管理します。オーディエンスは、次のような各種ソースから作成または取得できます。

* [!DNL Experience Cloud] で作成される新しいソース。
* [!DNL Analytics] に公開された [!DNL Experience Cloud] セグメントから。
* [!DNL Audience Manager] から。

**適用可能なソリューションまたはサービス**

* [Adobe Target のアクティビティ](https://docs.adobe.com/content/help/ja-JP/target/using/activities/activities.html)
* Audience Manager の[セグメント化](https://docs.adobe.com/content/help/ja-JP/analytics/integration/audience-analytics/audience-analytics-workflow/aam-analytics-segments.html)
* [Media Manager](https://enterprise.efrontier.com/CMDashboard/help/internal/concepts_and_features/media_optimizer_integration_with_adobe_marketing_cloud.htm)（ログインが必要）

## 顧客属性 {#section_6A9EA6847F654F129381869E5016626C}

ヘルプ：[顧客属性](attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

エンタープライズ顧客データを顧客関係管理（CRM）データベースに取り込んでいる場合は、そのデータを Experience Cloud の顧客属性データソースにアップロードできます。アップロード後は、データを [!DNL Adobe Analytics] と [!DNL Adobe Target] で利用できます。

**適用可能なソリューションまたはサービス**

* Adobe Analytics：[顧客属性レポート](https://docs.adobe.com/content/help/ja-JP/core-services/interface/customer-attributes/attributes.html)
* Adobe Target：顧客属性に対する Adobe Target の[サブスクリプション](https://docs.adobe.com/content/help/ja-JP/core-services/interface/customer-attributes/subscription.html)の設定

## Experience Cloud Assets {#section_92BC5DFDB0E0499CB0DD34B85E06F79A}

ヘルプ：[Creative Cloud との Experience Cloud フォルダーの共有](https://docs.adobe.com/content/help/ja-JP/core-services/interface/assets/creative-cloud.html)

Experience Cloud と Creative Cloud の間でフォルダーやアセットを共有します。共有アセットで共同作業をしたり、注釈を付けたり、それらを [!DNL Social] や [!DNL Target] などの Experience Cloud ソリューションで使用したりできます。

**適用可能なソリューションまたはサービス**

* [!DNL Experience Cloud]
* [!DNL Creative Cloud]
* [!DNL Target]
* [!DNL Social]

## Analytics - Analytics での AEM Assets レポート {#section_0A16AE14F128470AA02EFC6457BDCE75}

ヘルプ：[Analytics での AEM Assets レポート](https://docs.adobe.com/content/help/ja-JP/analytics/integration/aem-assets-reporting.html)

AEM Assets インサイトから提供されるアセットのインプレッション数とクリック数の情報を収集できます。

**適用可能なソリューションまたはサービス**

* [!DNL Analytics]
* [!DNL Experience Manager]

## Audience Manager 統合 {#section_8FEFE1746E26416EB7E73095BBAD5345}

[Audience Manager](https://docs.adobe.com/content/help/ja-JP/audience-manager/user-guide/implementation-integration-guides/implementation-and-integration.html)

Experience Cloud ソリューションや他の外部システムのデータを Audience Manager で操作します。

**適用可能なソリューションまたはサービス**

* [Analytics のサーバー側転送](https://docs.adobe.com/content/help/ja-JP/analytics/admin/admin-tools/server-side-forwarding/ssf.html)
* [Analytics への Audience Manager セグメントの送信](https://docs.adobe.com/content/help/ja-JP/audience-manager/user-guide/features/destinations/experience-cloud-destinations/create-analytics-destination.html)
* [Adobe Target のデータ統合](https://docs.adobe.com/content/help/ja-JP/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/aam-target-integration.html)

## Activation {#section_A23510A2D57842F6BAD043650C06DE42}

ヘルプ：[はじめに](https://docs.adobelaunch.com/getting-started)

Experience Cloud Activation ソリューションを使用して、Experience Cloud ソリューションの設定とデバッグをおこないます。

1. [Experience Platform Launch](https://docs.adobe.com/content/help/ja-JP/launch/using/overview.html) または [Dynamic Tag Management](https://docs.adobe.com/content/help/ja-JP/dtm/using/dtm-home.html) を使用して、ページ上で [Adobe Experience Cloud ソリューション](solutions-core-services.md#topic_BD726D3A649E4FC49063029E86B70C62)をアクティベートするコードを挿入します。
1. [Adobe Cloud Platform Auditor](https://docs.adobe.com/content/help/ja-JP/auditor/using/overview.html) を使用して実装をテストします。

Adobe Experience Cloud Debugger 拡張機能を使用して、Auditor によって検出された問題をデバッグしたり、実装に関する他の情報を調べたりします。

**適用可能なソリューションまたはサービス**

* [Analytics](https://docs.adobe.com/content/help/ja-JP/analytics/analyze/analysis-workspace/home.html)
* [Audience Manager](https://docs.adobe.com/content/help/ja-JP/dtm/using/tools/audiencemgmt.html)
* [Media Manager](https://docs.adobe.com/content/help/ja-JP/dtm/using/tools/media-optimizer.html)
* [Adobe Target](https://docs.adobe.com/content/help/ja-JP/dtm/using/tools/target.html)
* [MAC ID サービス](https://docs.adobe.com/content/help/ja-JP/dtm/using/tools/macid.html)
* [Nielsen トラッキング](https://docs.adobe.com/content/help/ja-JP/dtm/using/tools/nielsen.html)

## Adobe Target {#section_739716AB6022424CBC38724CDED10701}

ヘルプ：[Adobe Target と Experience Cloud の統合](https://docs.adobe.com/content/help/ja-JP/core-services/interface/audiences/audience-library.html)

Adobe Target と Adobe Analytics およびその他の Experience Cloud ソリューションを統合して、同じデータ、Audiences、属性および指標を両方のソリューションで使用できるようにします。

**適用可能なソリューションまたはサービス**

* 顧客属性：顧客属性に対する Adobe Target の[サブスクリプション](https://docs.adobe.com/content/help/ja-JP/core-services/interface/customer-attributes/subscription.html)の設定
* Experience Cloud Audiences：[Experience Cloud Audience ライブラリ](https://docs.adobe.com/content/help/ja-JP/core-services/interface/audiences/audience-library.html)
* Analytics：[Adobe Target のレポートソースとしての Adobe Analytics](https://docs.adobe.com/content/help/ja-JP/target/using/integrate/a4t/a4t.html)
* Dynamic Tag Management：[DTM を使用した Adobe Target の実装のベストプラクティス](https://docs.adobe.com/content/help/ja-JP/dtm/implementing/overview.html)
* Audience Manager：[Adobe Audience Manager との Adobe Target データの統合](https://docs.adobe.com/content/help/ja-JP/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/aam-target-integration.html)
* Campaign：[Adobe Target と Campaign の統合](https://docs.adobe.com/content/help/ja-JP/target/using/integrate/campaign-and-target.html)

## Adobe Experience Manager の統合 {#section_32FB010EF8B4429FBC63C8DC2A9BE98F}

ヘルプ：[ソリューション統合](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/user-guide.html?topic=/experience-manager/6-2/sites/administering/morehelp/integration.ug.js)

AEM と他のソリューションおよびサードパーティのサービスと統合します。

**適用可能なソリューションまたはサービス**

* [Analytics](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/adobeanalytics.html)
* [Analytics と外部プロバイダー](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/external-providers.html)
* [Experience Cloud](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/marketing-cloud.html)
* [Creative Cloud](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/creative-cloud.html)
* [Audience Manager](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/audiencemanager.html)
* [Campaign](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/campaign.html)
* [Dynamic Tag Management](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/dtm.html)
* [Scene7](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/scene7.html)
* [Adobe Target](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/target-configuring.html)
* [サードパーティのサービス](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/third-party-services.html)（Data Connectors）
* [拡張機能](https://helpx.adobe.com/jp/experience-manager/6-2/sites/developing/user-guide.html)

## Adobe Experience Manager - Assets {#section_CB865F8EFE4C4147BF8E2E4B66B5A318}

ヘルプ：[Experience Cloud および Creative Cloud との AEM Assets 統合の設定](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/configure-assets-cc-integration.html)

Adobe Experience Manager（AEM）Assets 内のアセットを Adobe Creative Cloud に（またはその逆に）同期します。また、アセットを Experience Cloud に（またはその逆に）同期することもできます。この同期は Experience Cloud を使用してセットアップできます。

**適用可能なソリューションまたはサービス**

* AEM
* Creative Cloud
* [Experience Cloud](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/marketing-cloud.html)

## Advertising Cloud {#section_9B1935F8BBC147C89C6DB68A35CB1BAB}

ヘルプ（ログインが必要）：[Adobe Experience Cloud ソリューションおよびサービスとの統合](https://enterprise.efrontier.com/CMDashboard/help/internal/concepts_and_features/media_optimizer_integration_with_adobe_marketing_cloud.htm)

**適用可能なソリューションまたはサービス**

**Analytics：** は、サイトエンゲージメントおよびコンバージョンデータを毎日 Media Manager に送信できます（Media Manager では、データを広告の最適化とレポート作成に使用します）。また、Media Manager は、検索エンジンおよびソーシャルネットワークのトラフィックデータを毎日 Analytics に送信できます（Analytics では、Reports &amp; Analytics、Report Builder および Ad Hoc Analysis の各機能でデータを利用できます）。

**Dynamic Tag Manager：**&#x200B;検索、ソーシャル、ディスプレイ広告ランディングページ用に、サードパーティのトラッキングタグに加えて、[Dynamic Tag Manager を使用して、Media Manager のピクセルベースのコンバージョントラッキングタグを作成](https://docs.adobe.com/content/help/ja-JP/dtm/using/tools/media-optimizer.html)できます（また、Media Manager タグを Media Manager 内に直接作成できます）。

**Experience Cloud Audiences：**（表示を管理する広告主）任意の [Adobe Experience Cloud Audiences](https://docs.adobe.com/content/help/ja-JP/core-services/interface/audiences/audience-library.html) を、ディスプレイ広告のターゲットとして使用できます。Adobe Experience Cloud で作成した Audiences および Adobe Experience Cloud に公開した Analytics からの Audiences を自動的に使用できます。また、Media Manager アカウントで許可されている場合は、Audience Manager からの Audiences を使用できます。Adobe Experience Cloud と Profiles および Audiences へのアクセスおよび Media Manager と Adobe Experience Cloud Audiences の初期設定について詳しくは、担当のアカウントマネージャーにお問い合わせください。**注意：** Adobe Target も使用する場合、Adobe Experience Cloud に公開した任意の Audiences も Adobe Target でのアクティビティに使用できます。

**Experience Cloud Assets：**（表示を管理する広告主）任意の Adobe Experience Cloud アセットを、新しいディスプレイベータ表示を使用したディスプレイ広告のクリエイティブとして使用できます。Adobe Experience Cloud にアクセスするには、[Adobe Experience Cloud を通じて Media Manager にログイン](https://enterprise-test.efrontier.com/CMDashboard/help/internal/getting_started/t_log_in_from_adobe_marketing_cloud.htm)しておく必要があります。Adobe Experience Cloud へのアクセスについて詳しくは、アカウントマネージャーにお問い合わせください。

**Experience Cloud 通知：**&#x200B;各ページの上部にある通知リンクから、検索ベータアラートテンプレートに加えて、Adobe Experience Cloud システムアップデート、投稿、メンションおよびアセット共有から生成されたすべてのアラートを表示できます。通知にアクセスするには、[Adobe Experience Cloud を通じて Media Manager にログイン](https://enterprise-test.efrontier.com/CMDashboard/help/internal/getting_started/t_log_in_from_adobe_marketing_cloud.htm)しておく必要があります。Adobe Experience Cloud へのアクセスについて詳しくは、アカウントマネージャーにお問い合わせください。
