---
description: Adobe Experience Cloud で利用可能なアプリケーション統合について説明します。
keywords: 統合
solution: Experience Cloud
title: 'Experience Cloud の統合 '
uuid: a9893c6b-bccc-4fb5-b724-724644c7def5
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 7f8fa610-32f0-4b18-8054-3ba05436a10e
source-git-commit: 542d3b9a246ca9616a853f4b6711efea290398d7
workflow-type: tm+mt
source-wordcount: '1422'
ht-degree: 99%

---

# Experience Cloud の統合の概要

Adobe Experience Cloud は、共通の強力な機能セットを備え、共通のデータプラットフォーム上に構築された、アプリケーションとサービスを統合したクラス最高の包括的なセットです。

## Experience Cloud アプリケーションの Platform サービスへの対応 {#section_A3D024994DA3492F8435CFCC4EF035C2}

ヘルプ：[Platform サービスへのアプリケーションの対応](core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)

次の方法について説明しています。

* Experience Cloud で会社をプロビジョニングする。
* 管理者になれるようにする。
* [Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)を実装する。
* Platform データ収集を使用して、[!DNL Analytics] および [!DNL Target] の実装を最新化する。
* コアサービスの使用を開始する。

ソリューションまたはサービス：

* Activation - Experience Platform データ収集（旧称 Launch）
* Analytics
* Target 
* [Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en)

## Experience Cloud ID サービス {#section_6ECCCFA2D84D4D4F88C879C799CA9D78}

ID サービスは、Experience Cloud のすべてのアプリケーションで訪問者を識別する永続的な汎用 ID を提供します。Analytics、Audience Manager、Adobe Target、ビデオハートビートなどのサービスや、その他の Experience Cloud のアプリケーションや製品で、ID 生成コードの代わりに使用できます。

[Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en)を参照してください。

**適用可能なアプリケーションまたはサービス**

* [Adobe Analytics](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=ja)
* [Adobe Target](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html?lang=ja)

## オーディエンス {#section_5F60D7B0833348B9A1D74663AADCB42C}

ヘルプ：[Audiences](audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

Experience Cloud オーディエンスライブラリでオーディエンスを作成および管理します。オーディエンスは、次のような各種ソースから作成または取得できます。

* [!DNL Experience Cloud] で作成される新しいソース。
* [!DNL Analytics] に公開された [!DNL Experience Cloud] セグメントから。
* [!DNL Audience Manager] から。

**適用可能なソリューションまたはサービス**

* [Adobe Target のアクティビティ](https://experienceleague.adobe.com/docs/target/using/activities/activities.html?lang=ja)
* Audience Manager の[セグメント化](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/audience-analytics-workflow/aam-analytics-segments.html?lang=ja)
* [Advertising Cloud](https://enterprise.efrontier.com/CMDashboard/?ticket=JrciD7q2bF1y2mDWFHmEyibbOnNwb2JBRF7z6tKAOIWkBimlPxCUaZyJnPLqsfdqsf3fpxWoxGasvatKA8S6-h4tlDvxQcm8Gc10dSF9q_E%3D&amp;ticket=JrciD7q2bF1y2mDWFHmEyibmxtHqnZFSOMml-n993zOBc-ovZGNZkX5vgePWqKNMoMmPSqf9PkzFeYF4UN6GqSXDVNDvwgnvv9KT8PvVxk8%3D) （ログインが必要）

## 顧客属性 {#section_6A9EA6847F654F129381869E5016626C}

ヘルプ：[顧客属性](attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

エンタープライズ顧客データを顧客関係管理（CRM）データベースに取り込んでいる場合は、そのデータを Experience Cloud の顧客属性データソースにアップロードできます。アップロード後は、データを [!DNL Adobe Analytics] と [!DNL Adobe Target] で利用できます。

**適用可能なソリューションまたはサービス**

* Adobe Analytics：顧客属性レポート
* Adobe Target：顧客属性に対する Adobe Target の[サブスクリプション](subscription.md)の設定

## Experience Cloud Assets {#section_92BC5DFDB0E0499CB0DD34B85E06F79A}

ヘルプ：[Creative Cloud との Experience Cloud フォルダーの共有](creative-cloud.md)

Experience Cloud と Creative Cloud の間でフォルダーやアセットを共有します。共有アセットで共同作業をしたり、注釈を付けたり、それらを [!DNL Social] や [!DNL Target] などの Experience Cloud アプリケーションで使用したりできます。

**適用可能なソリューションまたはサービス**

* [!DNL Experience Cloud]
* [!DNL Creative Cloud]
* [!DNL Target]
* [!DNL Social]

## Analytics - Analytics での AEM Assets レポート {#section_0A16AE14F128470AA02EFC6457BDCE75}

ヘルプ：[Analytics での AEM Assets レポート](https://experienceleague.adobe.com/docs/analytics/integration/aem-assets-reporting.html?lang=ja)

Analytics が、AEM Assets Insights から提供されるアセットのインプレッション数とクリック数を収集できるようになります。

**適用可能なアプリケーションまたはサービス**

* [!DNL Analytics]
* [!DNL Experience Manager]

## Audience Manager 統合 {#section_8FEFE1746E26416EB7E73095BBAD5345}

[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/implementation-and-integration.html?lang=ja)

Experience Cloud アプリケーションや他の外部システムのデータを Audience Manager で操作します。

**適用可能なアプリケーションまたはサービス**

* [Analytics のサーバー側転送](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=ja)
* [Analytics への Audience Manager セグメントの送信](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/experience-cloud-destinations/create-analytics-destination.html?lang=ja)
* [Adobe Target データ統合](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-applications/aam-target-integration.html?lang=ja)

## Activation {#section_A23510A2D57842F6BAD043650C06DE42}

ヘルプ：[はじめに](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html?lang=ja)

Experience Cloud Activation アプリケーションを使用して、Experience Cloud アプリケーションの設定とデバッグを行います。

1. [Experience Platform Launch](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ja) を使用して、ページ上で Experience Cloud アプリケーションをアクティベートするコードを挿入します。
1. [Adobe Cloud Platform Auditor](https://experienceleague.adobe.com/docs/auditor/using/overview.html?lang=ja) を使用して実装をテストします。

Adobe Experience Cloud Debugger 拡張機能を使用して、Auditor によって検出された問題をデバッグしたり、実装に関する他の情報を調べたりします。

**適用可能なアプリケーションまたはサービス**

* [Analytics](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=ja)
* [Audience Manager](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/audience-manager/overview.html?lang=ja)
* [Advertising Cloud](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=en)
* [Adobe Target](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=en)
* [MAC ID サービス](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=en)
* [Nielsen トラッキング](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=en)

## Adobe Target {#section_739716AB6022424CBC38724CDED10701}

ヘルプ：[Adobe Target と Experience Cloud の統合](audience-library.md)

Adobe Target と Adobe Analytics およびその他の Experience Cloud アプリケーションを統合して、同じデータ、オーディエンス、属性および指標を両方のソリューションで使用できるようにします。

**適用可能なソリューションまたはサービス**

* 顧客属性：顧客属性に対する Adobe Target の[サブスクリプション](subscription.md)の設定
* Experience Cloud Audiences：[Experience Cloud Audience ライブラリ](audience-library.md)
* Analytics：[Adobe Target のレポートソースとしての Adobe Analytics](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=ja)
* Dynamic Tag Management：[DTM を使用した Adobe Target の実装のベストプラクティス](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=en)
* Audience Manager：[Adobe Audience Manager との Adobe Target データの統合](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/aam-target-integration.html?lang=ja)
* Campaign：[Adobe Target と Campaign の統合](https://experienceleague.adobe.com/docs/target/using/integrate/campaign-and-target.html?lang=ja)

## Adobe Experience Manager の統合 {#section_32FB010EF8B4429FBC63C8DC2A9BE98F}

ヘルプ：[Experience Manager ドキュメント](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=ja)

AEM と他のアプリケーションおよびサードパーティのサービスと統合します。

**適用可能なアプリケーションまたはサービス**

* [Analytics](https://experienceleague.adobe.com/docs/?lang=ja)
* [Analytics と外部プロバイダー](https://experienceleague.adobe.com/docs/)
* [Experience Cloud](https://experienceleague.adobe.com/docs/)
* [Creative Cloud](https://experienceleague.adobe.com/docs/)
* [Audience Manager](https://experienceleague.adobe.com/docs/)
* [Campaign](https://experienceleague.adobe.com/docs/)
* [Scene7](https://experienceleague.adobe.com/docs/)
* [Adobe Target](https://experienceleague.adobe.com/docs/)
* [サードパーティのサービス](https://experienceleague.adobe.com/docs/)（Data Connectors）
* [拡張機能](https://experienceleague.adobe.com/docs/)

## Adobe Experience Manager - Assets {#section_CB865F8EFE4C4147BF8E2E4B66B5A318}

ヘルプ：[Experience Cloud および Creative Cloud との AEM Assets 統合の設定](https://experienceleague.adobe.com/docs/)

Adobe Experience Manager（AEM）Assets 内のアセットを Adobe Creative Cloud に（またはその逆に）同期します。また、アセットを Experience Cloud に（またはその逆に）同期することもできます。この同期は Experience Cloud を使用してセットアップできます。

**適用可能なアプリケーションまたはサービス**

* AEM
* Creative Cloud
* [Experience Cloud](https://experienceleague.adobe.com/docs/)

## [!DNL Adobe Advertising] {#section_9B1935F8BBC147C89C6DB68A35CB1BAB}

ヘルプ（ログインが必要）：[Adobe Experience Cloud ソリューションおよびサービスとの統合](https://enterprise.efrontier.com/CMDashboard?ticket=JrciD7q2bF1y2mDWFHmEyhyMKZp71ZLeaANvF-RcNMF7oNuZNABh76cKJLNlJJeJ1hQ5vAW1AO1t1DW8tZWM3lYZ8TSh96YAQISUdtHCCgA%3D&amp;ticket=JrciD7q2bF1y2mDWFHmEyibbOnNwb2JBRF7z6tKAOIWkBimlPxCUaZyJnPLqsfdqsf3fpxWoxGasvatKA8S6-h4tlDvxQcm8Gc10dSF9q_E%3D)

**適用可能なアプリケーションまたはサービス**

**Analytics：**&#x200B;サイトエンゲージメントおよびコンバージョンデータを毎日 [!DNL Adobe Advertising] に送信できます（データは広告の最適化とレポート作成に使用されます）。また、[!DNL Advertising] は、検索エンジンおよびソーシャルネットワークのトラフィックデータを毎日 Analytics に送信できます（Analytics では、Reports &amp; Analytics、Report Builder および Ad Hoc Analysis の各機能でデータを利用できます）。

**Dynamic Tag Manager：**[Dynamic Tag Manager を使用して、Advertising のピクセルベースのコンバージョントラッキングタグ](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=en)および検索、ソーシャル、ディスプレイ広告ランディングページ用にサードパーティのトラッキングタグを作成できます。（[!DNL Advertising] タグを [!DNL Advertising] 内に直接作成することもできます。）

**Experience Cloud Audiences：**（表示を管理する広告主）任意の [Adobe Experience Cloud Audiences](audience-library.md) を、ディスプレイ広告のターゲットとして使用できます。Experience Cloud で作成したAudiences と、Adobe Experience Cloud に公開した Analytics の Audiences を自動的に使用できます。[!DNL Adobe Advertising]アカウントで許可するよう設定されている場合は、Audience Manager の Audiences を使用することもできます。Adobe Experience Cloud とプロファイルおよび Audiences へのアクセスおよび [!DNL Adobe Advertising] と Adobe Experience Cloud Audiences の間の初期設定について詳しくは、担当のアカウントマネージャーにお問い合わせください。**注意：** Adobe Target も使用する場合、Adobe Experience Cloud に公開した任意の Audiences も Adobe Target でのアクティビティに使用できます。

**Experience Cloud Assets：**（表示を管理する広告主）任意の Adobe Experience Cloud アセットを、新しいディスプレイベータ表示を使用したディスプレイ広告のクリエイティブとして使用できます。Adobe Experience Cloud にアクセスするには、[Adobe Experience Cloud を通じて Adobe Advertising にログイン](https://enterprise-test.efrontier.com/CMDashboard?ticket=JrciD7q2bF1y2mDWFHmEyoBomG0VowpcEgK5zzKFq3mDArroL6xIS3XkmJFZMeeXlj0uIZz-IEcOn3nVHmy9bwdSxEcDv6FMvTkjwz5rpIs%3D&amp;ticket=JrciD7q2bF1y2mDWFHmEykzc2nFNvATOY54xOo03rW0GSLGdEpu5MvttCo6msEyImNVq7_lmlTup-LwCdnPIHA7mJrhugFMnbqTmSB-dfmw%3D)しておく必要があります。Adobe Experience Cloud へのアクセスについて詳しくは、アカウントマネージャーにお問い合わせください。

**Experience Cloud 通知：**&#x200B;各ページの上部にある通知リンクから、検索ベータアラートテンプレートから生成されたすべてのアラートを表示できます。また、Experience Cloud システムの更新、投稿、メンションおよびアセットの共有を取得できます。通知にアクセスするには、[Adobe Experience Cloud を通じて Adobe Advertising にログイン](https://enterprise-test.efrontier.com/CMDashboard?ticket=JrciD7q2bF1y2mDWFHmEyoBomG0VowpcEgK5zzKFq3mDArroL6xIS3XkmJFZMeeXlj0uIZz-IEcOn3nVHmy9bwdSxEcDv6FMvTkjwz5rpIs%3D&amp;ticket=JrciD7q2bF1y2mDWFHmEykzc2nFNvATOY54xOo03rW0GSLGdEpu5MvttCo6msEyImNVq7_lmlTup-LwCdnPIHA7mJrhugFMnbqTmSB-dfmw%3D)しておく必要があります。Adobe Experience Cloud へのアクセスについて詳しくは、アカウントマネージャーにお問い合わせください。
