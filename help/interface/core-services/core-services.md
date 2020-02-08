---
description: Experience Cloud を実装して管理者になります。このプロセスでは、顧客属性やオーディエンスなどのコアサービス機能向けにソリューションを最新化します。
keywords: core services;customer attributes
seo-description: Experience Cloud を実装して管理者になります。このプロセスでは、顧客属性やオーディエンスなどのコアサービス機能向けにソリューションを最新化します。
seo-title: コアサービス向けに Experience Cloud ソリューションを有効化
solution: Experience Cloud
title: コアサービス向けにソリューションを有効化
uuid: 5820060f-9b18-4339-81e0-401d964f7a03
translation-type: tm+mt
source-git-commit: 02b0163b95c24eb58bf2379c3e0d9f5f31c40925

---


# コアサービス向けにソリューションを有効化

既存のお客様に対して、ソリューションの実装を最新化し、顧客属性やオーディエンスなどの機能を使用できるようにExperience cloudを実装する方法を説明します。 これを達成するには、次の操作を行います。

1. [Experience Cloud に加入して管理者になる](#section_2423F0BD3DF642658103310EE5EA6154)
1. [Experience Cloud IDサービスの実装](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [レポートスイートのExperience cloud組織へのマッピング](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [Analytics appMeasurementコードの更新](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [Adobe target実装の更新](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [コアサービスの実装を確認する](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [ユーザーと製品を管理する](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [コアサービスの使用を開始する](#section_960C06093623462E8EA247B3E97274A1)

<!-- <p>https://marketing-beta.adobe.com/resources/help/core/core-services.html </p> 
<p>https://adobe.sharepoint.com/sites/AGSConsulting/CoreServices/PA/_layouts/15/start.aspx#/ </p> -->

<!-- Core services architecture and data flow wiki: https://wiki.corp.adobe.com/pages/viewpage.action?pageId=1004285689 -->

## 手順 1.Experience Cloud に加入して管理者になる {#section_2423F0BD3DF642658103310EE5EA6154}

Experience Cloud に加入するために必要なことを次に示します。

![](assets/step1_icon.png)適切な Adobe Analytics または Adobe Target SKU を持っていることを確認する。

* **Adobe Analytics：** Standard または Premium（レガシー SiteCatalyst SKU ではない）。
* **Adobe Target：** Standard または Premium。

>[!NOTE]
>
>Targetの場合は、mbox.jsからat.jsに移行します。 at.js 1 [からのアップグレードを参照してください。 xをat.js 2に置き換えます。 x](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/upgrading-from-atjs-1x-to-atjs-20.html).

![](assets/step2_icon.png)実装を最新化して管理者のプロビジョニングをおこなう。

1. 後述する手順に従って [Experience Cloud ID サービスをデプロイ](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354)します。
1. アカウントマネージャーに連絡し、Experience Cloud 用のプロビジョニングプロセスを開始します。

![](assets/step3_icon.png)[!UICONTROL  Admin Console でのユーザーと製品の管理].

**管理者アクセス**

After you are an administrator, you can log in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).

Experience Cloud メニューナビゲーションに「**[!UICONTROL 管理]**」リンクが表示されます。

ヘルプについては、[Experience Cloud ユーザーおよび製品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)を参照してください。

**ユーザーアクセス**

Experience Cloud にログインするには、次のことが必要です。

1. Adobe ID を持っている。
1. Sign in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. エンタープライズグループにマッピングされているソリューショングループに属する。
1. 必要に応じて、ソリューションアカウントを Adobe ID にリンクする（以下で説明）。

![](assets/step4_icon.png)オプション：既存のユーザーアカウントのリンク

Most likely, you have users who are already members of solution groups, such an Analytics group that you previously managed in [!UICONTROL Analytics] > [!UICONTROL Admin Tools].

これらのグループを Experience Cloud エンタープライズグループにマッピングする際、既にグループのメンバーになっているユーザーは、自分のソリューションアカウントの資格情報を自分の Adobe ID に手動でリンクする必要があります。

[Experience Cloud でのアカウントのリンク](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)を参照してください。

> [!NOTE]
> 
> エンタープライズグループとソリューショングループのマッピング後、新しいユーザーは自動的にリンクされます（ソリューションの資格情報が自動的に作成されて Adobe ID にリンクされます）。

以下のセクションでは、実装を最新化する方法を説明します。実装を最新化すると、Experience Cloud のコアサービスが有効になります。

## 手順 2：Experience Platform Launch( [!UICONTROL Dynamic Tag Management] )を使用し [!UICONTROL たExperience Cloud IDサービス]の実装 {#section_3C9F6DF37C654D939625BB4D485E4354}

Experience Cloud IDサー [!UICONTROL ビスは] 、クロスソリューション統合の共通IDを提供します。 顧客属性を介してアップロードされたCRMデータに基づいて、クロスドメインの訪問者の識別と、デバイス/ブラウザー間のターゲット設定およびパーソナライゼーションのためのパ [!UICONTROL スを提供しま]す。

Experience cloudコアサービスを有効にする最も簡単な方法は、 [Experience Platform Launchの](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html) Experience Cloud IDサービス拡張を使用するか [!UICONTROL 、]Dynamic Tag ManagementのECIDツールを使用して、AnalyticsおよびTarget用にコアサービスを自動的にアクティブ化する方法です 。 （エクスペリエンスプラットフォームの起動を強くお勧めします）。

![](assets/menu-activation-shell.png)

For complete Experience Cloud ID Service help (formerly, visitor ID), go [here](https://docs.adobe.com/content/help/en/id-service/using/home.html).

**エクスペリエン[!UICONTROL スプラットフォームの起動]、[!UICONTROL Dynamic Tag Managementを使用しない]。**

If you are not using [!UICONTROL Experience Platform Launch] or [!UICONTROL Dynamic Tag Management], manually implement the ID service via the JavaScript Deployment ([!DNL VisitorAPI.js]), as follows:

| タスク | 説明 |
| -----------| ---------- |  
| [Experience Cloud ID サービスの Analytics への実装](https://docs.adobe.com/content/help/en/id-service/using/implementation/setup-analytics.html) | また、追加の[顧客 ID](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) を設定することを推奨します。これらのIDは各訪問者に関連付けられ、Experience cloudの現在および将来の機能を有効にします。 |
| 既存の [!DNL s_code] をバージョン H.27.3 以降に更新するか、既存の [!DNL AppMeasurement.js] をバージョン 1.4 以降に更新します。 | これらのファイルは、Analytics 管理ツールの[コードマネージャー](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/code-manager-admin.html)でダウンロードして入手できます（[ について詳しくは、](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html)JavaScript の実装[!DNL AppMeasurement.js]を参照してください）。 |
| Analyticsの顧客IDの同期 | 以下の[Analytics - 顧客 ID の同期](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437)を参照してください。 |

## Analytics と Target - 顧客 ID の同期 {#section_AD473A6A21C1446498E700363F9A8437}

As a part of setting up the Experience Cloud ID Service, Adobe recommends for Analytics and [!DNL Target] that you synchronize your [customer IDs](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) with the Experience Cloud.

In Adobe Target, the `mbox3rdpartyid` needs to get the customer ID and send it to [!DNL Target]. (See [Working with Customer Attributes](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) in [!DNL Target].)

訪問者が Web サイトで認証をおこなうとき、または別の方法で本人確認をおこなうときは、その人物の CRM 顧客 ID をページまたはアプリに公開する必要があります。その後、適切な機能呼び出しを使用して、顧客 ID と Experience Cloud を同期できます。この同期によって、訪問者の CRM 顧客 ID が Experience Cloud に格納され、その顧客属性が Experience Cloud で使用できるようになります。

例えば、Bob が CRM システムに顧客 ID `52mc210tr42` を持っているとします。Bob がサイトで認証をおこなうときは、その顧客 ID をページに公開し、その顧客 ID を使用して次のいずれかの方法で同期する必要があります。

* 訪問者 ID サービスを使用して `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` を呼び出します。または
* prop または eVar に&#x200B;*`Customer ID (52mc210tr42)`*&#x200B;を設定します。

この顧客 ID を、顧客 ID が認識される個々の [!DNL Analytics] サーバー呼び出しに対して設定する必要があります。

### モバイル SDK

*Android* / [iOS](https://docs.adobe.com/content/help/en/mobile-services/android/overview.html)[](https://docs.adobe.com/content/help/en/mobile-services/ios/overview.html) mobileアプリケーションで追加の顧客IDを設定する方法の構文例については、「Experience Cloud IDサービス」の節を参照してください。

### 履歴データの属性の有効化

顧客属性データは、訪問者のログイン後に使用可能になります。まだ最新のExperience Cloud IDサービスを実装していない場合や、顧客IDをpropまたはeVarで過去に追跡している場合は、Experience cloudへのログイン履歴を送信するプロセスをリクエストできます。 このプロセスを使用すると、顧客属性の使用をすぐに開始できます。

カスタマーケアに連絡して履歴データを有効にしてください。

## 手順 3.Map report suites to an Experience Cloud Organization {#section_7B08516B01BA421681DF03D0E86CE3BA}

Experience Cloud services (such as Experience Cloud ID Service and the [!UICONTROL People service]) are associated with an Experience Cloud organization instead of an individual Analytics report suite. これらのサービスを正しく機能させるには、各 Analytics レポートスイートを Experience Cloud 組織にマッピングする必要があります。

[組織へのレポートスイートのマッピング](report-suite-mapping.md)を参照してください。

## 手順 4.(Adobe Analytics) Update your Analytics AppMeasurement code {#section_1798D9D0F05C47E29816AC4EEB9A0913}

地域データ収集サーバー（RDC）を使用していることを確認します。データ収集ドメインが [!DNL omtrdc.net] の場合、または CNAME が [!DNL omtrdc.net] にマッピングされている場合は、RDC を使用しています。詳しくは、[RDC への移行](https://docs.adobe.com/content/help/en/analytics/technotes/rdc/regional-data-collection.html)を参照してください。If you are using first-party cookies, refer to [CNAME and the Experience Cloud ID Service](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html) for information about data collection CNAMEs and cross-domain tracking.

訪問者 API など JavaScript ライブラリを更新して Analytics の実装を最新化することが推奨されます。これをおこなう最も簡単な方法は、Dynamic Tag Management で [!DNL Adobe Analytics] ツールを追加し、設定方法に *`Automatic`* を指定することです。

In [!UICONTROL Dynamic Tag Management], click **[!UICONTROL <Web Property Name>]**／**[!UICONTROL &#x200B;概要&#x200B;]**／**[!UICONTROL &#x200B;ツールを追加&#x200B;]**／**[!UICONTROL  Adobe Analytics ]**をクリックします。導入情報については、Dynamic Tag Management の[Adobe Analytics の設定](https://docs.adobe.com/content/help/en/dtm/using/tools/analytics-dtm.html)を参照してください。

## 手順 5.(Adobe Target) Update your Adobe Target implementation {#section_C2F4493C7A36406DAE2266B429A4BD24}

* It is recommended that you add an [Adobe Target extension](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/targetv2-extension/adobe-target-extension-v2.html) in [!UICONTROL Experience Platform Launch], so that your library retrieval is automatic. また、 [Experience Platform Launchを使用して](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html) 、Target用の [!UICONTROL Experience Cloud IDサービス拡張機能（およびその他のソリューション）を設定するこ]ともできます。 [!UICONTROL Targetがコアサービス] を使用するには **、** Experience Cloud IDサービスの更新が必要です。 ( [!UICONTROL Dynamic Tag Managementを使用する場合]、 [Adobe targetツールを追加します](https://docs.adobe.com/content/help/en/dtm/using/tools/target.html)。 You can also use [!UICONTROL Dynamic Tag Management] to deploy the Experience Cloud ID Service for Target.)
* エクスペリエンスプラットフォームの起動 [!UICONTROL (Experience Platform Launch] )または [!UICONTROL Dynamic Tag Management(]Dynamic Tag Management)を使用しない場合は、手動でmboxラ [イブラリを更新します](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/target-download-config-mbox.html) 。
* Request access to use Adobe Analytics as the reporting source for [!DNL Adobe Target]. [!DNL Target]処理中に同じサーバーコールで と のデータが結合され、これら 2 つのソリューション間で訪問者が接続されます。[!DNL Analytics][Target のための Analytics の実装に関する説明](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t.html)を参照してください。

   >[!IMPORTANT]
   >
   >Analyticsのすべてのお客様は、顧客属性などのコアサービス用に既にプロビジョニングされています。 Analytics ユーザーになっていないユーザーがいる場合は、そのユーザーのプロビジョニングをカスタマーケアに依頼します。

## 手順 6.コアサービスの実装を確認する {#section_E641782A0F4F44AF8C9C91216BE330D5}

Experience Cloud IDサービスがサイトに正しく実装されていることを確認するには、次のプロセスを使用します。

1. Experience Cloud IDサービスへのリクエストを確認できるように、サイトのcookieを消去します（リクエストは最初の訪問時に行われ、その後は訪問者あたり約1週間に1回行われます）。
1. パケットアナライザーまたは Web ブラウザーデバッガーのネットワークパネルを使用して、[!DNL dpm.demdex.net] へのリクエストを検索します。
1. 応答に `d_mid` と値が含まれていることを確認します（例：`_setMarketingCloudFields({"d_mid":"4235...`）。
1. Verify that the Analytics request contains the `mid` parameter (the Experience Cloud ID). During the grace period (if it is enabled), you should also see an `aid` parameter (the Analytics visitor ID).

Experience Cloud ID を含む期待される応答：

![](assets/mac_id_response.png)

Experience Cloud ID(別名または訪問者ID `mid` )を含む解析イメージリクエ _スト_:

![](assets/mid.png)

mbox リクエストの Experience Cloud ID：

![](assets/mbox_request.png)

**猶予期間とは**

Experience Cloud IDサービスを導入した後、新しい訪問者は、データ収集サーバーからAnalytics Experience Cloud IDを受け取らなくなります。 サイトの一部でExperience Cloud IDサービスを実装していない場合、訪問者がこれらのセクションを閲覧すると、Experience Cloud IDが認識されず、訪問者には従来のAnalytics訪問者IDが割り当てられます。 その結果、訪問者数が重複してカウントされたり、誤った属性が割り当てられたりするなどの問題が生じる可能性があります。

例えば、サイトのサポートセクションを別の CMS で管理している場合は、そのセクション用に別の Analytics JavaScript ファイルを使用していることがあります。IDサービスをサポートサイトに導入する前にExperience Cloud IDをメインサイトに導入した場合、新しい訪問者がサポートセクションを訪問する際に従来のAnalytics IDを受け取り、両方のサイトセクションにまたがる訪問は異なる訪問としてレポートされます。

複数のJavaScriptファイルや他のテクノロジー（Flashなど）を使用するサイトにExperience Cloud IDサービスをデプロイすると、サイトのすべての部分でExperience Cloud IDサービスを同時に有効にする必要があるので、調整の問題が発生する可能性があります。 猶予期間を設定すると、新しい訪問者は引き続きIDサービスからAnalytics訪問者IDを受け取るので、訪問者IDサービスを使用するようにアップグレードされていないサイトのセクションで、訪問者を一貫して識別できます。

## 手順 7.ユーザーと製品を管理する {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Once you are up and running, navigate to the [Admin Console](https://adminconsole.adobe.com/), where you can manage users and product profiles.

![](assets/menu-administration-shell.png)

[Experience Cloud のユーザーおよび製品の管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)を参照してください。

**顧客属性**

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Target). 
 </note> </p> 
 -->

Users that are added to the [!UICONTROL Customer Attributes] group will see the [!UICONTROL Customer Attributes] menu item on the left side of the Experience Cloud interface

## 手順 8.Begin using core services {#section_960C06093623462E8EA247B3E97274A1}

次のコアサービス機能を利用します。

![](assets/menu-audiences-shell.png)

**[!UICONTROL 人]/顧[!UICONTRO客属性]**

エンタープライズ顧客データを顧客関係管理（CRM）データベースに取り込んでいる場合は、そのデータを Experience Cloud の顧客属性データソースにアップロードできます。アップロード後は、データを [!DNL Adobe Analytics] と [!DNL Adobe Target] で利用できます。

[顧客属性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)を参照してください。

**[!UICONTROL ユーザー]/オーディエ[!UICONTROL ンスライブラリ]**

Experience Cloud [!UICONTROL Audiences] is the interface that lets you create audiences, combine existing audiences to create composite audiences, and view all shared audiences.

[オーディエンス](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)を参照してください。

<!-- aam_mc.xml -->

## データストレージとプライバシー開示

Adobe [!DNL Experience Cloud] 内のリアルタイムのオーディエンスプロファイルおよびその他のコアサービスを利用する場合、これらのサービスの使用は、データが保管されるデータセンター（および国）の選択に影響を与えることがあります。Specifically, because the core services of the Adobe [!DNL Experience Cloud] leverage Adobe Audience Manager, data used within the [!UICONTROL People] service must reside within Audience Manager servers in the United States.

When leveraging core services made available via the [!UICONTROL People] service, the types of data sent from other Adobe products to audience management are:

* [!DNL Analytics] キーと値のペア（prop、eVar、リスト変数、その他）。デフォルトでは、ログの行には、IP の最終オクテット（IP アドレスが Adobe [!DNL Analytics] の IP の不明化設定で変更されていないと仮定）を含む IP アドレスが含まれます。
* Audience Manager に設定されたルールに基づいて訪問者が資格を得る特徴とセグメント。
* （オプション）お使いの ID のうちの 1 つまたは複数。ID サービスの導入に応じて、CRM ID またはハッシュの電子メールアドレスなど、お使いの ID のうち 1 つまたは複数が送信されることもあります。このデータが Adobe [!DNL Analytics] に送信されると、Adobe Audience Management に転送されます。個人データを Adobe [!DNL Analytics] に提供しないことを推奨します。代わりに、アドビに送付する前に、一方向のハッシュを使用してデータを偽名化します。
* バックエンドのセグメント共有機能を使用した、[!DNL Analytics] から取得されるセグメント。
* サードパーティ Cookie がブロックされない場合、demdex.net Cookie が設定されます。The `AMCV_###@AdobeOrg` first-party cookie is always set with the Experience Cloud ID Service.

これらすべてのデータ要素は、ログファイルの形式で Adobe Audience Manager に配信されます。Audience Manager は、このデータを米国内で処理および格納します。Audience Manager は、このデータを米国外に格納または処理するオプションは提供しません。

**Cookie およびオプトアウト**

リアルタイムのオーディエンスプロファイルの使用では、[!DNL Analytics] および [!DNL Target] に使用する Cookie に加えて、Audience Manager Cookie を利用します。

適切なオプトアウト機能を提供したい場合、サイトへの訪問者は、既存のオプトアウト処理に Audience Manager オプトアウトを追加する必要があります。

手順については、Adobe Experience Cloud ヘルプの[アドビオプトアウトの導入](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/data-collection/opt-out.html)を参照してください。

クロスドメイントラッキングの有効化については、[データ収集 CNAME およびクロスドメイントラッキング](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html)を参照してください。
