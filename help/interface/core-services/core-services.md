---
description: Experience Cloudを実装し、管理者になります。 このプロセスは、顧客属性やオーディエンスなどのコアサービス機能のソリューションを最新化します。
keywords: core services;customer attributes
seo-description: Experience Cloudを実装し、管理者になります。 このプロセスは、顧客属性やオーディエンスなどのコアサービス機能のソリューションを最新化します。
seo-title: コアサービス向けに Experience Cloud ソリューションを有効化
solution: Experience Cloud
title: コアサービス向けにソリューションを有効化
uuid: 5820060f-9b18-4339-81e0-401d964f7a03
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# コアサービス向けにソリューションを有効化

既存のお客様の場合、ソリューションの実装を最新化し、顧客属性やオーディエンスなどの機能を使用できるようにExperience Cloudを実装する方法を説明します。 これを達成するには、次の操作を行います。

1. [Experience Cloud に加入して管理者になる](#section_2423F0BD3DF642658103310EE5EA6154)
1. [Experience Cloud IDサービスの実装](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [レポートスイートのExperience Cloud組織へのマッピング](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [Analytics AppMeasurementコードの更新](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [Adobe Target実装の更新](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [コアサービスの実装を確認する](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [ユーザーと製品を管理する](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [コアサービスの使用を開始する](#section_960C06093623462E8EA247B3E97274A1)

## 手順 1.Experience Cloud に加入して管理者になる {#section_2423F0BD3DF642658103310EE5EA6154}

Experience Cloud に加入するために必要なことを次に示します。

![](assets/step1_icon.png)適切な Adobe Analytics または Adobe Target SKU を持っていることを確認する。

* **Adobe Analytics:** StandardまたはPremium(従来の [!DNL SiteCatalyst] SKUではない)。
* **Adobe Target:** StandardまたはPremium。

>[!NOTE]
>
>の場 [!DNL Target]合は、からat.jsに移行しま [!DNL mbox.js]す。 See [Upgrading from at.js 1. x to at.js 2. x](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/upgrading-from-atjs-1x-to-atjs-20.html).

![](assets/step2_icon.png)実装を最新化して管理者のプロビジョニングをおこなう。

1. 「 [Experience Cloud IDサービスのデプロイ」の [!UICONTROL 手順]](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354)に従います。
1. アカウントマネージャーに問い合わせて、Experience Cloudのプロビジョニングプロセスを開始します。

![](assets/step3_icon.png) 管理コンソールでユーザーと製品 [!UICONTROL を管理します]。

### 管理者ログイン

After you are an administrator, you can log in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).

Experience Cloud メニューナビゲーションに「**[!UICONTROL 管理]**」リンクが表示されます。

ヘルプについては、[Experience Cloud ユーザーおよび製品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)を参照してください。

### ユーザーログイン

Experience Cloudにログインするには、次の操作を行う必要があります。

1. Adobe ID（または会社のEnterprise ID）を持っている。
1. Sign in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. エンタープライズグループにマップされているソリューショングループに属します。
1. 必要に応じて、ソリューションアカウントをAdobe IDにリンクします（以下を参照）。

![](assets/step4_icon.png)オプション：既存のユーザーアカウントのリンク

おそらく、以前に [!UICONTROL Analytics] /管理ツールで管理したAnalyticsグループなど、既にソリューショングループのメンバーであるユーザ [!UICONTROL ーがいます]。

これらのグループをExperience Cloudエンタープライズグループにマップする場合、それらのユーザーは、ソリューションアカウントの資格情報をAdobe IDに手動でリンクする必要があります。

Experience Cloudでの [アカウントのリンクを参照してください。](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

>[!NOTE]
>
>エンタープライズグループとソリューショングループのマッピング後、新しいユーザーは自動的にリンクされます（ソリューションの資格情報が自動的に作成され、Adobe IDにリンクされます）。

次の節では、実装を最新化する方法について説明します。 実装を最新化すると、Experience Cloudのコアサービスが有効になります。

## 手順 2：Experience Platform Launch [!UICONTROL (] Dynamic Tag Management [!UICONTROL )を使用したExperience Cloud IDサービス]の実装 {#section_3C9F6DF37C654D939625BB4D485E4354}

Experience Cloud IDサー [!UICONTROL ビスは] 、ソリューション間の統合のための共通IDを提供します。 顧客属性を介してアップロードされたCRMデータに基づいて、クロスドメインの訪問者の識別と、デバイス/ブラウザー間のターゲット設定およびパーソナライゼーションのパスを [!UICONTROL 提供します]。

Experience Cloudコアサービスを有効にする最も簡単な方法は、 [Experience Cloud Launchの](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html) Experience Cloud ID Service Extension [!UICONTROL 、または]Dynamic Tag ManagementのECIDツールを使用して、AnalyticsとAdobe Targetのコアサービスを自動的にアクティブ化する方法です 。 （エクスペリエンスプラットフォームの起動を強くお勧めします）。

![](assets/menu-activation-shell.png)

Experience Cloud IDサービスの完全なヘルプ（以前の訪問者ID）については、こちらを参照してく [ださい](https://docs.adobe.com/content/help/en/id-service/using/home.html)。

**エクスペリエンスプ[!UICONTROL ラットフォームの起動]、または[!UICONTROL Dynamic Tag Managementを使用しない]か。**

If you are not using [!UICONTROL Experience Platform Launch] or [!UICONTROL Dynamic Tag Management], manually implement the ID service via the JavaScript Deployment ([!DNL VisitorAPI.js]), as follows:

| タスク | 説明 |
| -----------| ---------- |  
| [Experience Cloud ID サービスの Analytics への実装](https://docs.adobe.com/content/help/en/id-service/using/implementation/setup-analytics.html) | また、追加の顧客IDを設定するこ [とをお勧めします](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html)。 これらのIDは各訪問者に関連付けられ、Experience Cloudの現在および将来の機能を有効にします。 |
| 既存の [!DNL s_code] をバージョン H.27.3 以降に更新するか、既存の [!DNL AppMeasurement.js] をバージョン 1.4 以降に更新します。 | これらのファイルは、Analytics管理ツールのコードマネー [ジャー](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/code-manager-admin.html) (Code Manager)からダウンロードできます。  (詳しくは、 [『](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) JavaScript導入ガイド [!DNL AppMeasurement.js]』を参照してください。) |
| Analyticsの顧客IDの同期 | 以下の[Analytics - 顧客 ID の同期](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437)を参照してください。 |

## Analytics &amp; Adobe Target - synching the customer ID {#section_AD473A6A21C1446498E700363F9A8437}

As a part of setting up the Experience Cloud ID Service, Adobe recommends for Analytics and [!DNL Target] that you synchronize your [customer IDs](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) with the Experience Cloud.

In Adobe Target, the `mbox3rdpartyid` needs to get the customer ID and send it to [!DNL Target]. (の「顧 [客属性の操作](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) 」を参 [!DNL Target]照)。

訪問者がWebサイトで認証を行う場合、または別の方法で本人確認を行う場合は、その人物のCRM顧客IDをページまたはアプリに公開する必要があります。 その後、適切な関数呼び出しを使用して、顧客IDをExperience Cloudと同期できます。 この同期により、訪問者のCRM顧客IDがExperience Cloudに保存され、その顧客属性がExperience Cloudで使用できるようになります。

例えば、Bob が CRM システムに顧客 ID `52mc210tr42` を持っているとします。Bob がサイトで認証をおこなうときは、その顧客 ID をページに公開し、その顧客 ID を使用して次のいずれかの方法で同期する必要があります。

* 訪問者 ID サービスを使用して `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` を呼び出します。または,
* propまたはeVar *`Customer ID (52mc210tr42)`* にを入力します。

この顧客 ID を、顧客 ID が認識される個々の [!DNL Analytics] サーバー呼び出しに対して設定する必要があります。

### モバイル SDK

*Androidおよび* iOS [](https://docs.adobe.com/content/help/en/mobile-services/android/overview.html)[](https://docs.adobe.com/content/help/en/mobile-services/ios/overview.html) Mobileアプリケーションで追加の顧客IDを設定する方法の構文例については、「Experience Cloud IDサービス」の節を参照してください。

### 履歴データの属性の有効化

顧客属性データは、訪問者のログイン後に使用可能になります。 最新のExperience Cloud IDサービスをまだ実装していない場合や、顧客IDをpropまたはeVarで過去に追跡している場合は、Experience Cloudへのログイン履歴を送信するプロセスをリクエストできます。 このプロセスにより、顧客属性の使用をすぐに開始できます。

履歴データを有効にするには、カスタマーケアにお問い合わせください。

## 手順 3.Map report suites to an Experience Cloud Organization {#section_7B08516B01BA421681DF03D0E86CE3BA}

Experience Cloudサービス(Experience Cloud IDサービスや [!UICONTROL Peopleサービス])は、個々のAnalyticsレポートスイートではなく、Experience Cloud組織に関連付けられます。 これらのサービスが正しく動作するように、各AnalyticsレポートスイートをExperience Cloud組織にマッピングする必要があります。

[組織へのレポートスイートのマッピング](report-suite-mapping.md)を参照してください。

## 手順 4.(Adobe Analytics) Update your Analytics AppMeasurement code {#section_1798D9D0F05C47E29816AC4EEB9A0913}

地域データ収集サーバー（RDC）を使用していることを確認します。データ収集ドメインが [!DNL omtrdc.net] の場合、または CNAME が [!DNL omtrdc.net] にマッピングされている場合は、RDC を使用しています。詳しくは [、「RDCへの移行](https://docs.adobe.com/content/help/en/analytics/technotes/rdc/regional-data-collection.html) 」を参照してください。 ファーストパーティcookieを使用している場合は、データ収集CNAMEとクロスドメイントラッキングについて [、「](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html) CNAMEとExperience Cloud IDサービス」を参照してください。

訪問者 API など JavaScript ライブラリを更新して Analytics の実装を最新化することが推奨されます。これをおこなう最も簡単な方法は、Dynamic Tag Management で [!DNL Adobe Analytics] ツールを追加し、設定方法に *`Automatic`* を指定することです。

In [!UICONTROL Dynamic Tag Management], click **[!UICONTROL <Web Property Name>]**/概**[!UICONTROL &#x200B;要&#x200B;]**/ツ**[!UICONTROL &#x200B;ールを追加&#x200B;]**/**[!UICONTROL  Adobe Analytics ]**。 導入情[報については](https://docs.adobe.com/content/help/en/dtm/using/tools/analytics-dtm.html)、Dynamic Tag ManagementのAdobe Analyticsの設定を参照してください。

## 手順 5.(Adobe Target) Update your Adobe Target implementation {#section_C2F4493C7A36406DAE2266B429A4BD24}

* ライブラリの取得が自動的に行われるように、 [Experience Platform](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/targetv2-extension/adobe-target-extension-v2.html) Launch [!UICONTROL でAdobe Target拡張機能を追加することをお勧めします]。 また、 [Experience Platform Launchを使用して](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html) 、Adobe Target（および他のソリューション）用の [!UICONTROL Experience Cloud IDサービス拡張を設定するこ]ともできます。 Adobe Targetがコ [!UICONTROL アサービスを使用す] るには **** 、Experience Cloud IDサービスの更新が必要です。 ( [!UICONTROL Dynamic Tag Managementを使用する場合]、 [Adobe Targetツールを追加します](https://docs.adobe.com/content/help/en/dtm/using/tools/target.html)。 また、 [!UICONTROL Dynamic Tag Managementを使用して] 、Adobe Target用のExperience Cloud IDサービスをデプロイすることもできます)。
* エクスペリエンスプラットフォームの起動 [!UICONTROL または] Dynamic Tag Managementを使用しない場合は [!UICONTROL 、手動]でmboxライブラリを更新します [](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/target-download-config-mbox.html) 。
* Request access to use Adobe Analytics as the reporting source for [!DNL Adobe Target]. [!DNL Target]処理中に同じサーバーコールで と のデータが結合され、これら 2 つのソリューション間で訪問者が接続されます。[!DNL Analytics]See [Analytics for Target Implementation](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t.html).

   >[!IMPORTANT]
   >
   >Analyticsのすべてのお客様は、顧客属性などのコアサービス用に既にプロビジョニングされています。 Analytics ユーザーになっていないユーザーがいる場合は、そのユーザーのプロビジョニングをカスタマーケアに依頼します。

## 手順 6.コアサービスの実装を確認する {#section_E641782A0F4F44AF8C9C91216BE330D5}

Experience Cloud IDサービスがサイトに正しく実装されていることを確認するには、次のプロセスを使用します。

1. Experience Cloud IDサービスへのリクエストを確認できるように、サイトのcookieを消去します（リクエストは最初の訪問時に行われ、その後は訪問者あたり約1週間に1回行われます）。
1. Using a packet analyzer or the network panel in a web browser debugger, look for a request going to [!DNL dpm.demdex.net].
1. 応答に `d_mid` と値が含まれていることを確認します（例：`_setMarketingCloudFields({"d_mid":"4235...`）。
1. Analyticsリクエストにパラメーター(Experience Cloud ID) `mid` が含まれていることを確認します。 猶予期間中（有効な場合）には、パラメーター（Analytics訪問者ID） `aid` も表示される必要があります。

次のExperience Cloud IDを含む期待される応答：

![](assets/mac_id_response.png)

Experience Cloud ID(別名または訪問者ID `mid` )を含むAnalyticsイメージリクエ _スト_:

![](assets/mid.png)

mboxリクエストのExperience Cloud ID:

![](assets/mbox_request.png)

### 猶予期間とは

Experience Cloud IDサービスを導入すると、新しい訪問者は、データ収集サーバーからAnalytics Experience Cloud IDを受け取らなくなります。 サイトのセクションにExperience Cloud IDサービスが実装されていない場合、訪問者がこれらのセクションを閲覧すると、Experience Cloud IDは認識されず、訪問者には従来のAnalytics訪問者IDが割り当てられます。 これにより、訪問回数の重複や誤ったアトリビューションなど、潜在的な問題が発生する可能性があります。

例えば、サイトのサポートセクションが別のCMSで管理されている場合、このセクション用に別のAnalytics JavaScriptファイルが存在する可能性があります。 IDサービスをサポートサイトに導入する前にExperience Cloud IDをメインサイトに導入した場合、新しい訪問者がサポートセクションを訪問すると、従来のAnalytics IDが新しい訪問者に提供され、両方のサイトセクションにまたがる訪問は異なる訪問としてレポートされます。

複数のJavaScriptファイルや他のテクノロジー（Flashなど）を使用するサイトにExperience Cloud IDサービスをデプロイすると、調整の問題が発生する可能性があります。これは、サイトのすべての部分でExperience Cloud IDサービスを同時に有効にする必要があるためです。 猶予期間を設定すると、新しい訪問者は引き続きIDサービスからAnalytics訪問者IDを受け取るので、訪問者IDサービスを使用するようにアップグレードされていないサイトのセクションで、訪問者を一貫して識別できます。

## 手順 7.ユーザーと製品を管理する {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Once you are up and running, navigate to the [Admin Console](https://adminconsole.adobe.com/), where you can manage users and product profiles.

![](assets/menu-administration-shell.png)

[Experience Cloud のユーザーおよび製品の管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)を参照してください。

### 顧客属性

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Adobe Target). 
 </note> </p> 
 -->

Users that are added to the [!UICONTROL Customer Attributes] group will see the [!UICONTROL Customer Attributes] menu item on the left side of the Experience Cloud interface.

## 手順 8.Begin using core services {#section_960C06093623462E8EA247B3E97274A1}

次のコアサービス機能を利用します。

![](assets/menu-audiences-shell.png)

### [!UICONTROL 人] / [!UICONTROl顧客属性]

エンタープライズ顧客データを顧客関係管理（CRM）データベースに取り込んでいる場合は、そのデータを Experience Cloud の顧客属性データソースにアップロードできます。アップロード後は、データを [!DNL Adobe Analytics] と [!DNL Adobe Target] で利用できます。

[顧客属性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)を参照してください。

### [!UICONTROL 人物] /オーディエ [!UICONTROL ンスライブラリ]

Experience Cloud [!UICONTROL Audiences] is the interface that lets you create audiences, combine existing audiences to create composite audiences, and view all shared audiences.

[オーディエンス](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)を参照してください。

## データストレージとプライバシー開示

Adobe [!DNL Experience Cloud] 内のリアルタイムのオーディエンスプロファイルおよびその他のコアサービスを利用する場合、これらのサービスの使用は、データが保管されるデータセンター（および国）の選択に影響を与えることがあります。Specifically, because the core services of the Adobe [!DNL Experience Cloud] leverage Adobe Audience Manager, data used within the [!UICONTROL People] service must reside within Audience Manager servers in the United States.

When leveraging core services made available via the [!UICONTROL People] service, the types of data sent from other Adobe products to audience management are:

* [!DNL Analytics] キーと値のペア（prop、eVar、リスト変数、その他）。デフォルトでは、ログの行には、IP の最終オクテット（IP アドレスが Adobe [!DNL Analytics] の IP の不明化設定で変更されていないと仮定）を含む IP アドレスが含まれます。
* Audience Managerで設定されたルールに基づいて訪問者が資格を得る特性とセグメント。
* （オプション）1つ以上のID。 IDサービスの実装によっては、CRM IDやハッシュ化された電子メールアドレスなど、1つ以上のIDを送信する場合もあります。 このデータが Adobe [!DNL Analytics] に送信されると、Adobe Audience Management に転送されます。個人データを Adobe [!DNL Analytics] に提供しないことを推奨します。アドビに送信する前に、一方向のハッシュを使用してデータをマスクします。
* バックエンドのセグメント共有機能を使用した、[!DNL Analytics] から取得されるセグメント。
* サードパーティ Cookie がブロックされない場合、demdex.net Cookie が設定されます。The `AMCV_###@AdobeOrg` first-party cookie is always set with the Experience Cloud ID Service.

これらすべてのデータ要素は、ログファイルの形式でAdobe Audience Managerに配信されます。 Audience Managerは、このデータを米国内で処理および保存します。 Audience Managerには、このデータを米国外に保存または処理するオプションはありません。

### cookieとオプトアウト

リアルタイムのオーディエンスプロファイルの使用では、[!DNL Analytics] および [!DNL Target] に使用する Cookie に加えて、Audience Manager Cookie を利用します。

適切なオプトアウト機能を提供したい場合、サイトへの訪問者は、既存のオプトアウト処理に Audience Manager オプトアウトを追加する必要があります。

手順につ [いては、「Adobe Experience Cloud — アドビのオプトアウトの実装](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/data-collection/opt-out.html) 」を参照してください。

クロスド [メイントラッキングを有効にする方法については、「データ収集CNAMEとクロスドメイントラッキング](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html) 」を参照してください。
