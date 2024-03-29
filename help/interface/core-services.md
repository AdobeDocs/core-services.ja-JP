---
description: クロスアプリケーションサービス用 Adobe Analytics および Adobe Target のアプリケーションを最新化します。Experience Cloud サービスの使用を開始する方法について説明します。
solution: Experience Cloud
title: クロスアプリケーションサービスに対してアプリケーションを有効化
index: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: 48e79e23-b339-4143-b3b1-969c370efeff
source-git-commit: 55b28d6a16f88955d7259a464bb690ee5985540e
workflow-type: tm+mt
source-wordcount: '2191'
ht-degree: 89%

---

# Experience Cloud サービスの実装を有効にする

Experience Platformタグを使用してExperience Cloudを最近実装した場合、顧客属性とExperience Cloudオーディエンスは既に設定されています。 また、Admin Console でユーザーや製品を管理することもできます。

既存のお客様は、アプリケーションの実装を最新化し、Experience Cloud を実装できます。これにより、Adobe Analytics、Audience Manager、Adobe Target をまたいで顧客属性とオーディエンス機能を使用できます。この実装を完了するために、以下をおこないます。

1. [Experience Cloud に加入して管理者になる](#section_2423F0BD3DF642658103310EE5EA6154)
1. [Experience Cloud ID サービス を実装します](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [レポートスイートを Experience Cloud 組織にマッピングする](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [Analytics の AppMeasurement コードを更新する](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [Adobe Target の実装を更新する](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [実装の検証](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [ユーザーと製品を管理する](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [属性とオーディエンスデータの共有を開始する](#section_960C06093623462E8EA247B3E97274A1)

## Experience Cloud に加入して管理者になる {#section_2423F0BD3DF642658103310EE5EA6154}

Experience Cloud に参加するために必要なことを次に示します。

1. 適切な Adobe Analytics または Adobe Target SKU を持っていることを確認する。

   * **Adobe Analytics：** Standard または Premium（レガシー [!DNL SiteCatalyst] SKU ではない）。
   * **Adobe Target：** Standard または Premium。

   >[!NOTE]
   >
   >[!DNL Target] の場合は、[!DNL mbox.js] から at.js に移行します。詳しくは、 [at.js 1. x から at.js 2.へのアップグレード x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/upgrading-from-atjs-1x-to-atjs-20.html?lang=ja).

1. 実装を最新化して管理者のプロビジョニングをおこなう。

   * 以下の手順（[ [!UICONTROL Experience Cloud ID Service]](core-services.md#section_3C9F6DF37C654D939625BB4D485E4354)の実装）に従います。
   * アカウントマネージャーに連絡し、Experience Cloud 用のプロビジョニングプロセスを開始します。

1.  [!UICONTROL Admin Console] でユーザーと製品を管理する。

### 管理者ログイン

管理者になると、[experience.adobe.com](https://experience.adobe.com) でログインできます。

**[!UICONTROL Admin Console]** リンクは、Experience Cloud メニューのナビゲーションで使用できます。

ヘルプについては、[Experience Cloud ユーザーおよび製品管理](admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)を参照してください。

### ユーザーログイン

Experience Cloud にログインするには、次のことが必要です。

* Adobe ID（または会社の Enterprise ID）を持っている。
* [experience.adobe.com](https://experience.adobe.com) でログインする。
* エンタープライズグループにマッピングされているアプリケーショングループに属します。
* 必要に応じて、アプリケーションアカウントを Adobe ID にリンクします（以下で説明）。

### オプション：既存のユーザーアカウントをリンクします。

ほとんどの場合は、既に Analytics グループなどのアプリケーショングループのメンバーになっているユーザーが存在するはずですが、このようなグループの管理はこれまで、[!UICONTROL Analytics]／[!UICONTROL 管理ツール]で行われていました。

これらのグループを Experience Cloud エンタープライズグループにマッピングする際、既にグループのメンバーになっているユーザーは、自分のアプリケーションアカウントの資格情報を自分の Adobe ID に手動でリンクする必要があります。

[Experience Cloud でのアカウントのリンク](organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)を参照してください。

>[!NOTE]
>
>エンタープライズグループとソリューショングループのマッピング後、新しいユーザーは自動的にリンクされます。（ソリューションの資格情報が自動的に作成されて Adobe ID にリンクされます）。

以下の節では、実装を最新化する方法を説明します。実装を最新化すると、Experience Cloud のコアサービスが有効になります。

## [!UICONTROL Experience Cloud ID サービス] を実装します {#section_3C9F6DF37C654D939625BB4D485E4354}

[!UICONTROL Experience Cloud ID サービス]は、アプリケーション間の統合に使用する共通の ID を提供します。クロスドメインの訪問者 ID と、[!UICONTROL 顧客属性]を介してアップロードされた CRM データに基づくクロスデバイス／ブラウザーのターゲティングおよびパーソナライズのためのパスを提供します。

Experience Cloud コアサービスを有効にする方法としては、 [!UICONTROL Experience Platform Launch] の [Experience Cloud ID サービス拡張機能](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html?lang=ja)を使用して、Analytics や Adobe Target に対してコアサービスを自動的にアクティブにするのが最も簡単です。

Experience Cloud ID サービス（以前の訪問者 ID）について詳しくは、[こちら](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=ja#intro)を参照してください。

**を使用していません [!UICONTROL Experience Platformタグ]?**

を使用しない場合、 [!UICONTROL Experience Platformタグ]を使用して、JavaScript デプロイメント (`VisitorAPI.js`) を次のように指定します。

| タスク | 説明 |
| -----------| ---------- |  
| [Experience Cloud ID サービスの Analytics への実装](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=ja) | また、追加の[顧客 ID](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=ja) を設定することを推奨します。これらの ID は各訪問者に関連付けられ、Experience Cloud の現在および将来の機能を有効にします。 |
| 既存の `s_code` をバージョン H.27.3 以降に更新、または既存の `AppMeasurement.js` をバージョン 1.4 以降に更新 | これらのファイルは、Analytics 管理ツールの[コードマネージャー](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/code-manager-admin.html?lang=ja)でダウンロードして入手できます（[!DNL AppMeasurement.js] について詳しくは、[JavaScript の実装](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=ja#js)を参照してください）。 |
| Analytics の顧客 ID の同期 | 以下の[Analytics - 顧客 ID の同期](core-services.md#section_AD473A6A21C1446498E700363F9A8437)を参照してください。 |

{style="table-layout:auto"}

### Analytics と Adobe Target - 顧客 ID の同期 {#section_AD473A6A21C1446498E700363F9A8437}

Analytics と [!DNL Target] については、Experience Cloud ID サービスを設定する際に[顧客 ID](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=ja) を Experience Cloud に同期させることを推奨します。

Adobe Target では、 `mbox3rdpartyid` は顧客 ID を取得して、それを [!DNL Target] に送信する必要があります。（[!DNL Target] のヘルプで[顧客属性の操作方法](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html?lang=ja)を参照してください）。

訪問者が web サイトで認証をおこなうとき、または別の方法で本人確認をおこなうとき、実装では、その人物の CRM 顧客 ID をページまたはアプリに公開する必要があります。その後、適切な機能呼び出しを使用して、顧客 ID と Experience Cloud を同期できます。この同期によって、訪問者の CRM 顧客 ID が Experience Cloud に格納され、その顧客属性が Experience Cloud で使用できるようになります。

例えば、Bob が CRM システムに顧客 ID `52mc210tr42` を持っているとします。Bob がサイトで認証をおこなうときは、その顧客 ID をページに公開し、その顧客 ID を使用して次のいずれかの方法で同期する必要があります。

* 訪問者 ID サービスを使用して `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` を呼び出します。または、
* prop または eVar に *`Customer ID (52mc210tr42)`* を設定します。

この顧客 ID を、顧客 ID が認識される個々の [!DNL Analytics] サーバー呼び出しに対して設定する必要があります。

#### Analytics：顧客 ID とData Warehouseのバックフィル方式の同期

Experience Cloud属性が初めて使用可能になったときに、顧客 ID サービスをまだ実装しておらず、顧客属性を簡単に利用できない場合がありました。 この問題を軽減するために、Adobeは、Adobe AnalyticsData Warehouseを使用して ID 同期のバックフィルをおこなう手段を作成しました。 この機能は、Data Warehouseバックフィルと呼ばれます。 Data Warehouseのバックフィルは、一般に必要なくなったので、2022 年 10 月以降は使用できなくなります。


### モバイル SDK

[Android™](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=ja) および [iOS](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=ja) モバイルアプリケーションで追加の顧客 ID を設定する方法の構文例については、*Experience Cloud ID サービス*&#x200B;の節を参照してください。

### 履歴データの属性の有効化

顧客属性データは、訪問者のログイン後に使用可能になります。まだ ID サービスを実装していない場合でも、顧客 ID を prop または eVar で履歴追跡していれば、Experience Cloud へのログイン履歴を送信するプロセスを要求できます。このプロセスを使用すると、顧客属性の使用をすぐに開始できます。

カスタマーケアに連絡して履歴データを有効にしてください。

## レポートスイートを Experience Cloud 組織にマッピングする {#section_7B08516B01BA421681DF03D0E86CE3BA}

>[!NOTE]
>
>レポートスイートのマッピング機能は、2020 年 11 月に廃止されます。ご質問があれば、カスタマーサポートにお問い合わせください。

Experience Cloud サービス（Experience Cloud ID サービスや [!UICONTROL People サービス]など）は、個々の Analytics レポートスイートではなく Experience Cloud 組織に関連付けられています。これらのサービスを正しく機能させるには、各 Analytics レポートスイートを Experience Cloud 組織にマッピングする必要があります。

## Analytics の AppMeasurement コードを更新する {#section_1798D9D0F05C47E29816AC4EEB9A0913}

Analytics を使用している場合は、地域データ収集（RDC）を使用していることを確認します。データ収集ドメインが `omtrdc.net` の場合、または CNAME が `omtrdc.net` にマッピングされている場合は、RDC を使用しています。詳しくは、[RDC への移行](https://experienceleague.adobe.com/docs/analytics/technotes/rdc/regional-data-collection.html?lang=ja)を参照してください。ファーストパーティ Cookie を使用している場合、データ収集 CNAME とクロスドメイン追跡については、[CNAME と Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/cname.html?lang=ja)を参照してください。

訪問者 API など JavaScript ライブラリを更新して Analytics の実装を最新化することが推奨されます。これをおこなう簡単な方法は、 [Adobe Analytics拡張機能](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=ja) (Experience Platformデータ収集 )。

## Adobe Target の実装を更新する {#section_C2F4493C7A36406DAE2266B429A4BD24}

* 次の項目を追加することをお勧めします。 [Adobe Target拡張機能](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target-v2/overview.html?lang=ja) in [!UICONTROL Experience Platform] タグを使用して、ライブラリの検索を自動的におこなうことができます。 また、 [Experience CloudID サービス拡張機能](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html?lang=ja) （およびを使用する他のアプリケーション用） [!UICONTROL Experience Platform] タグ。 The [!UICONTROL Experience CloudID サービス] 更新 **必須** Adobe Targetで People サービスを使用する場合。
* を使用しない場合、 [!UICONTROL Experience Platform] タグ、 [mbox ライブラリの更新](https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/implement-target-for-client-side-web.html?lang=ja) 手動で。
* [!DNL Adobe Target] のレポートソースとして Adobe Analytics を使用するためのアクセスをリクエストします。[!DNL Target] と [!DNL Analytics] のデータは、処理中に同じサーバー呼び出しで結合されるため、訪問者は 2 つのアプリケーション間で接続されます。[Analytics for Target の実装](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=ja)を参照してください。

  >[!IMPORTANT]
  >
  >すべての Analytics ユーザーは、顧客属性などコアサービスのために既にプロビジョニングされています。Analytics ユーザーになっていないユーザーがいる場合は、そのユーザーのプロビジョニングをカスタマーケアに依頼します。

## 実装の検証 {#section_E641782A0F4F44AF8C9C91216BE330D5}

Experience Cloud ID サービスがサイトに正しく実装されていることを確認するには、次の手順を実行します。

1. Experience Cloud ID サービスに対するリクエストを確認できるように、サイトの Cookie を消去します（リクエストは最初の訪問時におこなわれ、その後は訪問者ごとに 1 週間に 1 回おこなわれます）。
1. パケットアナライザーまたは Web ブラウザーデバッガーのネットワークパネルを使用して、[!DNL dpm.demdex.net] へのリクエストを検索します。
1. 応答に `d_mid` と値が含まれていることを確認します（例：`_setMarketingCloudFields({"d_mid":"4235...`）。
1. Analytics リクエストに `mid` パラメーター（Experience Cloud ID）が含まれていることを確認します。猶予期間中（有効になっている場合）には、`aid` パラメーター（Analytics 訪問者 ID）も表示されます。

Experience Cloud ID を含む期待される応答：

![Experience Cloud ID を含む期待される応答](assets/mac_id_response.png)

Experience Cloud ID（`mid` または&#x200B;_訪問者 ID_ とも呼ばれます）を含んだ Analytics の画像リクエスト：

![Experience Cloud ID を含む Analytics 画像リクエスト](assets/mid.png)

mbox リクエストの Experience Cloud ID：

![mbox リクエストの Experience Cloud ID](assets/mbox_request.png)

### 猶予期間とは

Experience Cloud ID サービスをデプロイすると、新しい訪問者はデータ収集サーバーから Analytics Experience Cloud ID を受け取らなくなります。サイトの一部で ID サービスの実装が終わっていない場合は、訪問者がこれらのセクションを訪問したときに、Experience Cloud ID が認識されず、訪問者には従来の Analytics 訪問者 ID が割り当てられてしまいます。その結果、訪問者数が重複してカウントされたり、誤った属性が割り当てられたりするなどの問題が生じる可能性があります。

例えば、サイトのサポートセクションを別の CMS で管理している場合は、そのセクション用に別の Analytics JavaScript ファイルを使用していることがあります。ID サービスをサポートサイトにデプロイする前に Experience Cloud ID をメインサイトにデプロイした場合、新しい訪問者がサポートセクションにアクセスすると、その訪問者は従来の Analytics ID を受け取ります。両方のサイトセクションにまたがる訪問は、異なる訪問としてレポートされます。

複数の JavaScript ファイルや他のテクノロジー（Flash など）を使用しているサイトに Experience Cloud ID サービスをデプロイすると、調整の問題が発生する可能性があります。これらの問題は、サイトのすべての部分で同時に Experience Cloud ID サービスを有効にする必要があるために発生します。猶予期間を設定すると、新しい訪問者は ID サービスから引き続き Analytics 訪問者 ID を受け取ります。訪問者 ID サービスを使用するようにアップグレードされていないサイトのセクションで、一貫して訪問者を識別できます。

## ユーザーと製品を管理する {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

起動して実行したら、[Admin Console](https://adminconsole.adobe.com/) に移動して、ユーザーと製品プロファイルを管理できます。

![Admin Console へのアクセス](assets/menu-administration-shell.png)

[Experience Cloud のユーザーおよび製品の管理](admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)を参照してください。

### 顧客属性

[!UICONTROL 顧客属性]グループに追加されたユーザーには、Experience Cloud の左側に「[!UICONTROL 顧客属性]」メニュー項目が表示されます。

## 属性とオーディエンスデータの共有を開始する {#section_960C06093623462E8EA247B3E97274A1}

次の機能を利用します。

### [!UICONTROL People]／[!UICONTROL 顧客属性]

エンタープライズ顧客データを顧客関係管理（CRM）データベースに取り込んでいる場合は、そのデータを Experience Cloud の顧客属性データソースにアップロードできます。アップロード後は、データを [!DNL Adobe Analytics] と [!DNL Adobe Target] で利用できます。

[顧客属性](attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)を参照してください。

### [!UICONTROL People]／[!UICONTROL オーディエンスライブラリ]

Experience Cloud [!UICONTROL オーディエンス]は、オーディエンスを作成したり、既存のオーディエンスを組み合わせて複合オーディエンスを作成したり、共有しているすべてのオーディエンスを表示したりできるインターフェイスです。

[Audiences](audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7) を参照してください。

## データストレージおよびプライバシー開示

Adobe [!DNL Experience Cloud] 内のリアルタイムのオーディエンスプロファイルおよびその他のコアサービスを利用する場合、これらのサービスの使用は、データが保管されるデータセンター（および国）の選択に影響を与えることがあります。特に、[!DNL Experience Cloud] は Audience Manager を使用するので、[!UICONTROL People] サービス内で使用されるデータは米国の Audience Manager サーバー内に存在する必要があります。

[!UICONTROL People] サービスを通じて使用可能なサービスを利用する場合、他のアドビ製品から Audience Management に送信されるデータのタイプは、次のようになります。

* [!DNL Analytics] キーと値のペア（prop、eVar、リスト変数、その他）。デフォルトでは、ログの行には、IP の最終オクテット（IP アドレスが Adobe [!DNL Analytics] の IP の不明化設定で変更されていないと仮定）を含む IP アドレスが含まれます。
* Audience Manager に設定されたルールに基づいて訪問者が資格を得る特性とセグメント。
* （オプション）お使いの ID のうちの 1 つまたは複数。ID サービスの導入に応じて、CRM ID またはハッシュの電子メールアドレスなど、お使いの ID のうち 1 つまたは複数が送信されることもあります。このデータが Adobe [!DNL Analytics] に送信されると、Adobe Audience Management に転送されます。個人データを Adobe [!DNL Analytics] に提供しないことを推奨します。代わりに、アドビに送付する前に、一方向のハッシュを使用してデータをマスクします。
* バックエンドのセグメント共有機能を使用して、[!DNL Analytics] から取得されるセグメント。
* サードパーティ Cookie がブロックされない場合、demdex.net Cookie が設定されます。`AMCV_###@AdobeOrg` ファーストパーティ Cookie は、常に Experience Cloud ID サービスを使用して設定されます。

これらすべてのデータ要素は、ログファイルの形式で Adobe Audience Manager に配信されます。Audience Manager は、このデータを米国内で処理および格納します。Audience Manager は、このデータを米国外に格納または処理するオプションは提供しません。

### Cookie とオプトアウト

リアルタイムのオーディエンスプロファイルの使用では、[!DNL Analytics] および [!DNL Target]に使用する Cookie に加えて、Audience Manager Cookie を使用します。

適切なオプトアウト機能を提供したい場合、サイトへの訪問者は、既存のオプトアウト処理に Audience Manager オプトアウトを追加する必要があります。

手順については、[Adobe Experience Cloud ヘルプのアドビオプトアウトの導入](https://experienceleague.adobe.com/docs/analytics/implementation/js/opt-out.html?lang=ja)を参照してください。

クロスドメイントラッキングの有効化については、[データ収集 CNAME およびクロスドメイントラッキング](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/cname.html?lang=ja)を参照してください。
