---
description: Adobe CX Enterpriseで利用可能なアプリケーション統合を見つける。
solution: Experience Cloud
title: Experience Cloud の統合
uuid: a9893c6b-bccc-4fb5-b724-724644c7def5
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 7f8fa610-32f0-4b18-8054-3ba05436a10e
TQID: https://experienceleague.adobe.com/6Sh6sOZ--ct2sz5sMR-qRwZmvoC51zQkV9LqVRXmi-o
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: dab36b01-8bfa-48f3-8392-626455a058e6id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4bid: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: d27b1945-f442-4607-91bd-537a0b16e687id: ecb4a972-6786-444c-a014-abc528b9407aid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66id: df401a2a-327d-468c-a5e4-b7b7ccd071a0id: e1e0219c-f879-479f-8427-888ed2a6e9c2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 1116
ht-degree: 31%

---

# CX エンタープライズ統合

このページでは、CX Enterprise アプリケーションの統合を開始するための複数の方法について説明します。 詳しくは、Experience Leagueの[統合ビデオチュートリアル ](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ja)のライブラリを参照してください。

## プラットフォームサービス向けのCX エンタープライズアプリケーションの有効化

次の方法について説明しています。

* CX Enterpriseで自社をプロビジョニングする。
* 管理者になれるようにする。
* [CX Enterprise ID サービスを実装](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)。
* [!UICONTROL Platform データ収集]を使用して、[!DNL Analytics]および[!DNL Target]の実装を最新化します。
* [顧客属性](../services/customer-attributes/attributes.md)や[ オーディエンスライブラリ ](../services/audiences/overview.md)などのCX エンタープライズサービスの使用を開始します。

ソリューションまたはサービス：

* [[!DNL Experience Platform Data Collection]](https://experienceleague.adobe.com/docs/experience-platform.html?lang=ja)
* [[!DNL Analytics]](https://experienceleague.adobe.com/docs/analytics.html?lang=ja)
* [[!DNL Target]](https://experienceleague.adobe.com/docs/target.html)
* [CX Enterprise ID Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)

## CX Enterprise ID Service

ID サービスは、CX Enterpriseのすべてのアプリケーションをまたいで訪問者を識別する、ユニバーサルで永続的なIDを提供します。 Adobe Analytics、Audience Manager、Adobe Target、動画ハートビート、CX Enterprise アプリケーションなどのサービスや製品のID生成コードを置き換えることができます。

[CX Enterprise ID サービス ](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)を参照してください

**適用可能なアプリケーションまたはサービス**

* [Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/overview)
* [Adobe Target](https://experienceleague.adobe.com/en/docs/id-service/using/implementation/setup-target)

## オーディエンス

ヘルプ：[オーディエンス](/help/interface/services/audiences/overview.md)

CX Enterprise [!UICONTROL  オーディエンスライブラリ ]でオーディエンスを作成および管理します。 オーディエンスは、次のような各種ソースから作成または取得できます。

* [!DNL CX Enterprise]に新しいオブジェクトが作成されました。
* [!DNL Analytics] セグメントが[!DNL CX Enterprise]に公開されました。
* [!DNL Audience Manager] から。

**適用可能なソリューションまたはサービス**

* [Adobe Target のアクティビティ](https://experienceleague.adobe.com/docs/target/using/activities/activities.html)
* Audience Manager の[セグメント化](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/audience-analytics-workflow/aam-analytics-segments.html)
* [Advertising Cloud](https://enterprise.efrontier.com/CMDashboard/?ticket=JrciD7q2bF1y2mDWFHmEyibbOnNwb2JBRF7z6tKAOIWkBimlPxCUaZyJnPLqsfdqsf3fpxWoxGasvatKA8S6-h4tlDvxQcm8Gc10dSF9q_E%3D&ticket=JrciD7q2bF1y2mDWFHmEyibmxtHqnZFSOMml-n993zOBc-ovZGNZkX5vgePWqKNMoMmPSqf9PkzFeYF4UN6GqSXDVNDvwgnvv9KT8PvVxk8%3D) （ログインが必要）

## 顧客属性

ヘルプ：[顧客属性](/help/interface/services/customer-attributes/attributes.md)

顧客関係管理（CRM）データベースで企業顧客データを取得する場合は、CX Enterpriseの顧客属性データソースにデータをアップロードできます。 アップロード後は、データを [!DNL Adobe Analytics] と [!DNL Adobe Target] で利用できます。

**適用可能なソリューションまたはサービス**

* Adobe Analytics：顧客属性レポート
* Adobe Target：顧客属性を使用するようにAdobe Targetの[ サブスクリプション ](/help/interface/services/customer-attributes/subscription.md)を設定します

## CX Enterprise Assets

ヘルプ：[Creative CloudとCX Enterprise Foldersを共有](/help/interface/services/assets/share.md)

CX EnterpriseとCreative Cloud間でフォルダーとアセットを共有します。 Adobe Adobe Targetなどの顧客体験管理システム向けアプリケーションでは、共有アセットの共同作業、注釈付け、使用できます。

**適用可能なアプリケーションまたはサービス**

* Adobe CX Enterprise
* Adobe Creative Cloud
* Adobe Target

## Analytics - Analytics での AEM Assets レポート

ヘルプ：[Analytics での AEM Assets レポート](https://experienceleague.adobe.com/docs/analytics/integration/aem-assets-reporting.html)

Analytics が、AEM Assets Insights から提供されるアセットのインプレッション数とクリック数を収集できるようになります。

**適用可能なアプリケーションまたはサービス**

* [!DNL Analytics]
* [!DNL Experience Manager]

## Audience Manager 統合

[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/implementation-and-integration.html)

CX Enterprise アプリケーションやAudience Manager内の他の外部システムからのデータを扱えます。

**適用可能なアプリケーションまたはサービス**

* [Analytics サーバーサイド転送](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=ja)
* [AnalyticsへのAudience Manager セグメントの送信](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/experience-cloud-destinations/create-analytics-destination.html)
* [Adobe Targetとの連携](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-applications/aam-target-integration.html)

## Adobe Target

ヘルプ：[Adobe TargetとCX Enterpriseの統合](/help/interface/services/audiences/overview.md)

Adobe TargetをAdobe Analyticsやその他のCX Enterprise アプリケーションと統合することで、両方のアプリケーションで同じデータ、オーディエンス、属性、指標を使用できるようになります。

**適用可能なソリューションまたはサービス**

* 顧客属性：顧客属性に対する Adobe Target の[サブスクリプション](/help/interface/services/customer-attributes/subscription.md)の設定
* CX エンタープライズオーディエンス：[CX エンタープライズオーディエンスライブラリ ](/help/interface/services/audiences/overview.md)
* Analytics：[Adobe Target のレポートソースとしての Adobe Analytics](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)
* Audience Manager：[Adobe Audience Manager との Adobe Target データの統合](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/aam-target-integration.html)
* Campaign：[Adobe Target と Campaign の統合](https://experienceleague.adobe.com/docs/target/using/integrate/campaign-and-target.html?lang=ja)

## Adobe Experience Manager の統合

* ビデオチュートリアル：[Experience Managerとの統合](https://experienceleague.adobe.com/docs/integrations-learn/experience-cloud/integrations-between-applications/overview.html)

* 製品ドキュメント：[Experience Manager ドキュメント ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=ja)

## Adobe Experience Manager - Assets

ヘルプ：[CX EnterpriseおよびCreative CloudとのAEM Assets統合の設定](https://experienceleague.adobe.com/docs/?lang=ja)

Adobe Experience Manager（AEM）Assets 内のアセットを Adobe Creative Cloud に（またはその逆に）同期します。 また、アセットをCX EnterpriseやCX Enterpriseと同期することもできます。 この同期は、CX Enterpriseで設定できます。

**適用可能なアプリケーションまたはサービス**

* AEM
* Creative Cloud
* [CX Enterprise](https://experienceleague.adobe.com/docs/?lang=ja)

## [!DNL Adobe Advertising]

* ヘルプ（ログインが必要）: [Adobe CX Enterprise Solutions and Servicesとの統合](https://enterprise.efrontier.com/CMDashboard?ticket=JrciD7q2bF1y2mDWFHmEyhyMKZp71ZLeaANvF-RcNMF7oNuZNABh76cKJLNlJJeJ1hQ5vAW1AO1t1DW8tZWM3lYZ8TSh96YAQISUdtHCCgA%3D&ticket=JrciD7q2bF1y2mDWFHmEyibbOnNwb2JBRF7z6tKAOIWkBimlPxCUaZyJnPLqsfdqsf3fpxWoxGasvatKA8S6-h4tlDvxQcm8Gc10dSF9q_E%3D)

* Experience Leagueの[Adobe Advertising ドキュメント ](https://experienceleague.adobe.com/docs/advertising.html)

**適用可能なアプリケーションまたはサービス**

**Analytics：**&#x200B;サイトエンゲージメントおよびコンバージョンデータを毎日 [!DNL Adobe Advertising] に送信できます（データは広告の最適化とレポート作成に使用されます）。 また、[!DNL Advertising] は、検索エンジンおよびソーシャルネットワークのトラフィックデータを毎日 Analytics に送信できます（Analytics では、Reports &amp; Analytics、Report Builder および Ad Hoc Analysis の各機能でデータを利用できます）。

**タグ：** [Experience Platform タグを使用して、検索、ソーシャル、ディスプレイ広告のランディングページ用に、Advertising ピクセルベースのコンバージョントラッキングタグ ](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ja)およびサードパーティのトラッキングタグを作成できます。 （[!DNL Advertising] タグを [!DNL Advertising] 内に直接作成することもできます。）

**CX Enterprise Audiences:** （ディスプレイ管理機能を持つ広告主）ディスプレイ広告のターゲットとして[Adobe CX Enterprise Audiences](../services/audiences/overview.md)のいずれかを使用できます。 CX Enterpriseで作成したオーディエンスと、CX Enterpriseに公開したAnalyticsのオーディエンスを自動的に使用できます。 [!DNL Adobe Advertising] アカウントが許可するように設定されている場合は、Audience Managerのオーディエンスを使用することもできます。

Adobe CX Enterpriseおよびプロファイルとオーディエンスへのアクセスについて、および[!DNL Adobe Advertising]とAdobe CX Enterprise Audiencesの間の初期設定について詳しくは、アカウントマネージャーにお問い合わせください。 **メモ：** Adobe Targetも使用している場合、Adobe CX Enterpriseに公開したオーディエンスは、Adobe Targetのアクティビティでも利用できます。

**CX Enterprise Assets:** （ディスプレイ管理付き広告主）新しいディスプレイBeta ビューを使用すると、Adobe CX Enterprise アセットのいずれかをディスプレイ広告のクリエイターとして使用できます。 Adobe CX Enterprise アセットにアクセスするには、[Adobe CX Enterprise](https://enterprise.efrontier.com/CMDashboard)を介してAdobe Advertisingにログインしている必要があります。 Adobe CX Enterpriseへのアクセスについて詳しくは、アカウントマネージャーにお問い合わせください。

**CX エンタープライズ通知：**&#x200B;各ページの上部にある通知リンクから、検索ベータ通知テンプレートから生成されたすべてのアラートを表示できます。 システムのアップデート、投稿、メンション、アセットを共有することも可能です。 通知にアクセスするには、[Adobe CX Enterprise](https://enterprise.efrontier.com/CMDashboard)を通じてAdobe Advertisingにログインする必要があります。 Adobe CX Enterpriseへのアクセスについて詳しくは、アカウントマネージャーにお問い合わせください。

