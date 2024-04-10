---
description: Adobe Experience Cloud で利用可能なアプリケーション統合について説明します。
solution: Experience Cloud
title: Experience Cloud の統合
uuid: a9893c6b-bccc-4fb5-b724-724644c7def5
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 7f8fa610-32f0-4b18-8054-3ba05436a10e
source-git-commit: 56936fd32f7208fb2a0c4a2abc67d48f30dd788c
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 78%

---

# Experience Cloud の統合の概要

ここでは、Experience Cloudアプリケーションの統合を開始する方法をいくつか説明します。 詳しくは、次のライブラリを参照してください [統合ビデオチュートリアル](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ja) Experience League上。

## Experience Cloud アプリケーションの Platform サービスへの対応 {#section_A3D024994DA3492F8435CFCC4EF035C2}

ヘルプ：[Platform サービスへのアプリケーションの対応](core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)

次の方法について説明しています。

* Experience Cloudで会社をプロビジョニングします。
* 管理者になれるようにする。
* [Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)を実装する。
* の最新化 [!DNL Analytics] および [!DNL Target] を介した実装 [!UICONTROL Platform データ収集].
* などのExperience Cloudサービスの使用を開始する [[!DNL Customer Attributes]](attributes.md) および [[!DNL Audience Library]](audience-library.md).

ソリューションまたはサービス：

* [[!DNL Experience Platform Data Collection]](https://experienceleague.adobe.com/docs/experience-platform.html?lang=ja)
* [[!DNL Analytics]](https://experienceleague.adobe.com/docs/analytics.html?lang=ja)
* [[!DNL Target]](https://experienceleague.adobe.com/docs/target.html?lang=en)
* [Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)

## Experience Cloud ID サービス {#section_6ECCCFA2D84D4D4F88C879C799CA9D78}

ID サービスは、Experience Cloud内のすべてのアプリケーションで訪問者を識別する永続的な汎用 ID を提供します。 Analytics、Audience Manager、Adobe Target、ビデオハートビートなどのサービスや、その他の Experience Cloud のアプリケーションや製品で、ID 生成コードの代わりに使用できます。

[Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)を参照してください。

**適用可能なアプリケーションまたはサービス**

* [Adobe Analytics](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=ja)
* [Adobe Target](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html?lang=ja)

## オーディエンス {#section_5F60D7B0833348B9A1D74663AADCB42C}

ヘルプ：[Audiences](audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

Experience Cloudでのオーディエンスの作成と管理 [!UICONTROL オーディエンスライブラリ]. オーディエンスは、次のような各種ソースから作成または取得できます。

* [!DNL Experience Cloud] で作成される新しいソース。
* [!DNL Analytics] に公開された [!DNL Experience Cloud] セグメントから。
* [!DNL Audience Manager] から。

**適用可能なソリューションまたはサービス**

* [Adobe Target のアクティビティ](https://experienceleague.adobe.com/docs/target/using/activities/activities.html?lang=ja)
* Audience Manager の[セグメント化](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/audience-analytics-workflow/aam-analytics-segments.html?lang=ja)
* [Advertising Cloud](https://enterprise.efrontier.com/CMDashboard/?ticket=JrciD7q2bF1y2mDWFHmEyibbOnNwb2JBRF7z6tKAOIWkBimlPxCUaZyJnPLqsfdqsf3fpxWoxGasvatKA8S6-h4tlDvxQcm8Gc10dSF9q_E%3D&amp;ticket=JrciD7q2bF1y2mDWFHmEyibmxtHqnZFSOMml-n993zOBc-ovZGNZkX5vgePWqKNMoMmPSqf9PkzFeYF4UN6GqSXDVNDvwgnvv9KT8PvVxk8%3D) （ログインが必要）

## 顧客属性 {#section_6A9EA6847F654F129381869E5016626C}

ヘルプ：[顧客属性](attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

大規模法人の顧客データを顧客関係管理（CRM）データベースに取り込んでいる場合は、そのデータをExperience Cloudの顧客属性データソースにアップロードできます。 アップロード後は、データを [!DNL Adobe Analytics] と [!DNL Adobe Target] で利用できます。

**適用可能なソリューションまたはサービス**

* Adobe Analytics：顧客属性レポート
* Adobe Target：顧客属性に対する Adobe Target の[サブスクリプション](subscription.md)の設定

## Experience Cloud Assets {#section_92BC5DFDB0E0499CB0DD34B85E06F79A}

ヘルプ：[Creative Cloud との Experience Cloud フォルダーの共有](creative-cloud.md)

Experience Cloud と Creative Cloud の間でフォルダーとアセットを共有します。共有アセットで共同作業をしたり、注釈を付けたり、それらを [!DNL Social] や [!DNL Target] などの Experience Cloud アプリケーションで使用したりできます。

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

## Adobe Target {#section_739716AB6022424CBC38724CDED10701}

ヘルプ： [Adobe TargetとExperience Cloudの統合](audience-library.md)

Adobe Target と Adobe Analytics およびその他の Experience Cloud アプリケーションを統合して、同じデータ、オーディエンス、属性および指標を両方のソリューションで使用できるようにします。

**適用可能なソリューションまたはサービス**

* 顧客属性：顧客属性に対する Adobe Target の[サブスクリプション](subscription.md)の設定
* Experience Cloud Audiences：[Experience Cloud Audience ライブラリ](audience-library.md)
* Analytics：[Adobe Target のレポートソースとしての Adobe Analytics](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=ja)
* Dynamic Tag Management：[DTM を使用した Adobe Target の実装のベストプラクティス](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ja)
* Audience Manager：[Adobe Audience Manager との Adobe Target データの統合](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/aam-target-integration.html?lang=ja)
* Campaign：[Adobe Target と Campaign の統合](https://experienceleague.adobe.com/docs/target/using/integrate/campaign-and-target.html?lang=ja)

## Adobe Experience Manager の統合 {#section_32FB010EF8B4429FBC63C8DC2A9BE98F}

* ビデオチュートリアル： [Experience Manager統合](https://experienceleague.adobe.com/docs/integrations-learn/experience-cloud/integrations-between-applications/overview.html)

* 製品ドキュメント： [Experience Managerドキュメント](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=ja)

## Adobe Experience Manager - Assets {#section_CB865F8EFE4C4147BF8E2E4B66B5A318}

ヘルプ：[Experience Cloud および Creative Cloud との AEM Assets 統合の設定](https://experienceleague.adobe.com/docs/?lang=ja)

Adobe Experience Manager（AEM）Assets 内のアセットを Adobe Creative Cloud に（またはその逆に）同期します。また、アセットを Experience Cloud に（またはその逆に）同期することもできます。この同期は Experience Cloud を使用してセットアップできます。

**適用可能なアプリケーションまたはサービス**

* AEM
* Creative Cloud
* [Experience Cloud](https://experienceleague.adobe.com/docs/?lang=ja)

## [!DNL Adobe Advertising] {#section_9B1935F8BBC147C89C6DB68A35CB1BAB}

* ヘルプ（ログインが必要）：[Adobe Experience Cloud ソリューションおよびサービスとの統合](https://enterprise.efrontier.com/CMDashboard?ticket=JrciD7q2bF1y2mDWFHmEyhyMKZp71ZLeaANvF-RcNMF7oNuZNABh76cKJLNlJJeJ1hQ5vAW1AO1t1DW8tZWM3lYZ8TSh96YAQISUdtHCCgA%3D&amp;ticket=JrciD7q2bF1y2mDWFHmEyibbOnNwb2JBRF7z6tKAOIWkBimlPxCUaZyJnPLqsfdqsf3fpxWoxGasvatKA8S6-h4tlDvxQcm8Gc10dSF9q_E%3D)

* [Adobe Advertisingドキュメント](https://experienceleague.adobe.com/docs/advertising.html?lang=en) Experience League時

**適用可能なアプリケーションまたはサービス**

**Analytics：**&#x200B;サイトエンゲージメントおよびコンバージョンデータを毎日 [!DNL Adobe Advertising] に送信できます（データは広告の最適化とレポート作成に使用されます）。また、[!DNL Advertising] は、検索エンジンおよびソーシャルネットワークのトラフィックデータを毎日 Analytics に送信できます（Analytics では、Reports &amp; Analytics、Report Builder および Ad Hoc Analysis の各機能でデータを利用できます）。

**タグ :** 次を使用できます [Advertising のピクセルベースのコンバージョントラッキングタグを作成するためのExperience Platformタグ](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ja)検索、ソーシャル、ディスプレイ広告ランディングページ用の、サードパーティトラッキングタグ （[!DNL Advertising] タグを [!DNL Advertising] 内に直接作成することもできます。）

**Experience Cloud Audiences：**（表示を管理する広告主）任意の [Adobe Experience Cloud Audiences](audience-library.md) を、ディスプレイ広告のターゲットとして使用できます。Experience Cloudで作成したオーディエンスおよびExperience Cloudに公開した Analytics のオーディエンスを自動的に使用できます。 次の場合に、Audience Managerのオーディエンスを使用することもできます [!DNL Adobe Advertising] 許可するようにアカウントが設定されています。

Adobe Experience Cloud とプロファイルおよび Audiences へのアクセスおよび [!DNL Adobe Advertising] と Adobe Experience Cloud Audiences の間の初期設定について詳しくは、担当のアカウントマネージャーにお問い合わせください。**注意：** Adobe Target も使用する場合、Adobe Experience Cloud に公開した任意のオーディエンスも Adobe Target でのアクティビティに使用できます。

**Experience Cloud Assets：**（表示を管理する広告主）任意の Adobe Experience Cloud アセットを、新しいディスプレイベータ表示を使用したディスプレイ広告のクリエイティブとして使用できます。Adobe Experience Cloud にアクセスするには、[Adobe Experience Cloud を通じて Adobe Advertising にログイン](https://enterprise-test.efrontier.com/CMDashboard?ticket=JrciD7q2bF1y2mDWFHmEyoBomG0VowpcEgK5zzKFq3mDArroL6xIS3XkmJFZMeeXlj0uIZz-IEcOn3nVHmy9bwdSxEcDv6FMvTkjwz5rpIs%3D&amp;ticket=JrciD7q2bF1y2mDWFHmEykzc2nFNvATOY54xOo03rW0GSLGdEpu5MvttCo6msEyImNVq7_lmlTup-LwCdnPIHA7mJrhugFMnbqTmSB-dfmw%3D)しておく必要があります。Adobe Experience Cloud へのアクセスについて詳しくは、アカウントマネージャーにお問い合わせください。

**Experience Cloud 通知：**&#x200B;各ページの上部にある通知リンクから、検索ベータアラートテンプレートから生成されたすべてのアラートを表示できます。また、Experience Cloud システムの更新、投稿、メンションおよびアセットの共有を取得できます。通知にアクセスするには、[Adobe Experience Cloud を通じて Adobe Advertising にログイン](https://enterprise-test.efrontier.com/CMDashboard?ticket=JrciD7q2bF1y2mDWFHmEyoBomG0VowpcEgK5zzKFq3mDArroL6xIS3XkmJFZMeeXlj0uIZz-IEcOn3nVHmy9bwdSxEcDv6FMvTkjwz5rpIs%3D&amp;ticket=JrciD7q2bF1y2mDWFHmEykzc2nFNvATOY54xOo03rW0GSLGdEpu5MvttCo6msEyImNVq7_lmlTup-LwCdnPIHA7mJrhugFMnbqTmSB-dfmw%3D)しておく必要があります。Adobe Experience Cloud へのアクセスについて詳しくは、アカウントマネージャーにお問い合わせください。
