---
description: Experience Cloud を実装して管理者になります。このプロセスでは、顧客属性やオーディエンスなどのコアサービス機能向けにソリューションを最新化します。
keywords: コアサービス;顧客属性
seo-description: Experience Cloud を実装して管理者になります。このプロセスでは、顧客属性やオーディエンスなどのコアサービス機能向けにソリューションを最新化します。
seo-title: コアサービス向けに Experience Cloud ソリューションを有効化
solution: Experience Cloud
title: コアサービス向けにソリューションを有効化
uuid: 5820060f-9b18-4339-81e0-401d964f7a03
translation-type: tm+mt
source-git-commit: b4809ff0b4546f105ac6270eca1bfce2b6467876

---


# コアサービス向けにソリューションを有効化

Experience Cloud を実装して管理者になります。このプロセスでは、顧客属性やオーディエンスなどのコアサービス機能向けにソリューションを最新化します。

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
>For Target, [migrate to at.js from mbox.js](https://marketing.adobe.com/resources/help/en_US/target/ov2/t_target-migrate-atjs.html).


![](assets/step2_icon.png)実装を最新化して管理者のプロビジョニングをおこなう。


1. 後述する手順に従って [Experience Cloud ID サービスをデプロイ](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354)します。
1. アカウントマネージャーに連絡し、Experience Cloud 用のプロビジョニングプロセスを開始します。

![](assets/step3_icon.png)Admin Console でユーザーと製品を管理する。

**管理者アクセス**

管理者になると、[marketing.adobe.com](https://marketing.adobe.com) / でログインできます。

Experience Cloud メニューナビゲーションに「**[!UICONTROL 管理]**」リンクが表示されます。

ヘルプについては、[Experience Cloud ユーザーおよび製品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)を参照してください。

**ユーザーアクセス**

Experience Cloud にログインするには、次のことが必要です。


1. Adobe ID を持っている。
1. [!DNL marketing.adobe.com] にログインする。
1. エンタープライズグループにマッピングされているソリューショングループに属する。
1. 必要に応じて、ソリューションアカウントを Adobe ID にリンクする（以下で説明）。

![](assets/step4_icon.png)オプション：既存のユーザーアカウントのリンク

ほとんどの場合は、既に Analytics グループなどのソリューショングループのメンバーになっているユーザーが存在するはずですが、このようなグループの管理は従来、Analytics／管理ツールでおこなわれていました。

これらのグループを Experience Cloud エンタープライズグループにマッピングする際、既にグループのメンバーになっているユーザーは、自分のソリューションアカウントの資格情報を自分の Adobe ID に手動でリンクする必要があります。

[Experience Cloud でのアカウントのリンク](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)を参照してください。

> [!NOTE]
> 
> エンタープライズグループとソリューショングループのマッピング後、新しいユーザーは自動的にリンクされます（ソリューションの資格情報が自動的に作成されて Adobe ID にリンクされます）。

以下のセクションでは、実装を最新化する方法を説明します。実装を最新化すると、Experience Cloud のコアサービスが有効になります。

## 手順 2：Dynamic Tag Manager または Experience Platform Launch を利用して Experience Cloud ID サービスを実装する {#section_3C9F6DF37C654D939625BB4D485E4354}

Experience Cloud コアサービスを有効にする最も簡単な方法は、Dynamic Tag Manager の [Experience Cloud ID サービスツール](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-dtm-implement.html)を使用して、Analytics および Target 用にコアサービスを自動的にアクティブにすることです（または Experience Platform Launch を使用できます）。

![](assets/menu-activation-shell.png)

Experience Cloud ID サービス（以前の訪問者 ID）について詳しくは、[こちら](https://marketing.adobe.com/resources/help/en_US/mcvid/)を参照してください。

[Launch, by Adobe](https://marketing.adobe.com/resources/help/en_US/experience-cloud/launch/) は次世代のタグ管理ソリューションです。

**Dynamic Tag Management も Launch も使用していない場合**

Dynamic Tag Management を使用していない場合は、次に示すように、JavaScript 導入ファイル（[!DNL VisitorAPI.js]）を利用して ID サービスを手動で実装します。

1. [Experience Cloud ID サービスの Analytics への実装](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-analytics.html)で説明している手順を実行します。

   また、追加の[顧客 ID](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-authenticated-state.html) を設定することを推奨します。これらの ID は各訪問者に関連付けられ、Experience Cloud コアサービスの現在および将来の機能を有効にします。

1. 既存の [!DNL s_code] をバージョン H.27.3 以降に更新するか、既存の [!DNL AppMeasurement.js] をバージョン 1.4 以降に更新します。

   これらのファイルは、Analytics 管理ツールの[コードマネージャー](https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=code_manager_admin)でダウンロードして入手できます

   （[ について詳しくは、](https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html)JavaScript の実装[!DNL AppMeasurement.js]を参照してください）。

1. Analytics の顧客 ID を同期します。以下の[Analytics - 顧客 ID の同期](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437)を参照してください。

## Analytics と Target - 顧客 ID の同期 {#section_AD473A6A21C1446498E700363F9A8437}

Analytics と Target については、Experience Cloud ID サービスを設定する際に[顧客 ID](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-authenticated-state.html) を Experience Cloud に同期させることを推奨します。

Target では、[!DNL mbox3rdpartyid] として顧客 ID を取得し、それを Target に送信する必要があります（Target ヘルプで[顧客属性の操作方法](https://marketing.adobe.com/resources/help/en_US/target/target/c_working-with-customer-attributes.html)を参照してください）。

訪問者が Web サイトで認証をおこなうとき、または別の方法で本人確認をおこなうときは、その人物の CRM 顧客 ID をページまたはアプリに公開する必要があります。その後、適切な機能呼び出しを使用して、顧客 ID と Experience Cloud を同期できます。この同期によって、訪問者の CRM 顧客 ID が Experience Cloud に格納され、その顧客属性が Experience Cloud で使用できるようになります。

例えば、Bob が CRM システムに顧客 ID `52mc210tr42` を持っているとします。Bob がサイトで認証をおこなうときは、その顧客 ID をページに公開し、その顧客 ID を使用して次のいずれかの方法で同期する必要があります。

* 訪問者 ID サービスを使用して `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` を呼び出します。または
* prop または eVar に&#x200B;*`Customer ID (52mc210tr42)`*&#x200B;を設定します。


この顧客 ID を、顧客 ID が認識される個々の [!DNL Analytics] サーバー呼び出しに対して設定する必要があります。

**モバイル SDK**

*Android* / [iOS](https://marketing.adobe.com/resources/help/en_US/mobile/android/?f=methods)[](https://marketing.adobe.com/resources/help/en_US/mobile/ios/?f=methods) mobileアプリケーションで追加の顧客IDを設定する方法の構文例については、「Experience Cloud IDサービス」の節を参照してください。

**履歴データの属性の有効化**

顧客属性データは、訪問者のログイン後に使用可能になります。まだ最新の Experience Cloud ID サービスを実装していない場合でも、顧客 ID を prop または eVar で履歴追跡していれば、Experience Cloud へのログイン履歴を送信するプロセスを要求できます。このプロセスを使用すると、顧客属性の使用をすぐに開始できます。

カスタマーケアに連絡して履歴データを有効にしてください。

## 手順 3.レポートスイートを Experience Cloud 組織にマッピングする {#section_7B08516B01BA421681DF03D0E86CE3BA}

Experience Cloud サービス（Experience Cloud ID サービスや People など）は、個々のレポートスイートではなく Experience Cloud 組織に関連付けられています。これらのサービスを正しく機能させるには、各 Analytics レポートスイートを Experience Cloud 組織にマッピングする必要があります。

[組織へのレポートスイートのマッピング](report-suite-mapping.md)を参照してください。

## 手順 4.（Analytics のみ）Adobe Analytics AppMeasurement コードを最新化する{#section_1798D9D0F05C47E29816AC4EEB9A0913}

地域データ収集サーバー（RDC）を使用していることを確認します。データ収集ドメインが [!DNL omtrdc.net] の場合、または CNAME が [!DNL omtrdc.net] にマッピングされている場合は、RDC を使用しています。詳しくは、[RDC への移行](https://marketing.adobe.com/resources/help/en_US/whitepapers/rdc/?f=rdc_transition)を参照してください。ファーストパーティ Cookie を使用している場合、データ収集 CNAME とクロスドメイン追跡については、[CNAME と訪問者 ID サービス](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_cname)を参照してください。

訪問者 API など JavaScript ライブラリを更新して Analytics の実装を最新化することが推奨されます。これをおこなう最も簡単な方法は、Dynamic Tag Management で [!DNL Adobe Analytics] ツールを追加し、設定方法に *`Automatic`* を指定することです。

Dynamic Tag Management で、**[!UICONTROL <Web Property Name>]**／**[!UICONTROL 概要]**／**[!UICONTROL ツールの追加]**／**[!UICONTROL Adobe Analytics]**をクリックします。導入情報については、Dynamic Tag Management の[Adobe Analytics の設定](https://marketing.adobe.com/resources/help/en_US/dtm/?f=analytics_dtm)を参照してください。

## 手順 5.（Adobe Target）Adobe Target の実装を最新化する{#section_C2F4493C7A36406DAE2266B429A4BD24}

* Dynamic Tag Management で [Adobe Target ツール](https://marketing.adobe.com/resources/help/en_US/dtm/target.html)を追加してライブラリの検索を自動化することが推奨されます。Dynamic Tag Management で、**[!UICONTROL <Web Property Name>]**／**[!UICONTROL 概要]**／**[!UICONTROL ツールの追加]**／**[!UICONTROL Adobe Target]**をクリックします。**&#x200B;注意：**Dynamic Tag Management を使用して、Target（およびその他のソリューション）用に Experience Cloud ID サービスをデプロイすることもできます。Target でコアサービスを使用するには、Experience Cloud ID サービスのアップデートが**&#x200B;必要&#x200B;**です。
* Dynamic Tag Management を使用していない場合は、手動で [mbox ライブラリを更新](https://marketing.adobe.com/resources/help/en_US/target/ov/?f=t_mbox_download)します。
* Adobe Analytics を Adobe Target のレポートソースとして使用するためのアクセスを要求します。処理中に同じサーバーコールで Target と Analytics のデータが結合され、これら 2 つのソリューション間で訪問者が接続されます。[Target のための Analytics の実装に関する説明](https://marketing.adobe.com/resources/help/en_US/target/a4t/?f=a4t)を参照してください。
* 
   >[!IMPORTANT]
   >
   >すべての Analytics ユーザーは、顧客属性などコアサービスのために既にプロビジョニングされています。Analytics ユーザーになっていないユーザーがいる場合は、そのユーザーのプロビジョニングをカスタマーケアに依頼します。

## 手順 6.コアサービスの実装を確認する {#section_E641782A0F4F44AF8C9C91216BE330D5}

Experience Cloud ID サービスがサイトに正しく実装されていることを確認するには、次の手順を実行します。

1. Experience Cloud ID サービスに対するリクエストを確認できるように、サイトの Cookie を消去します（リクエストは最初の訪問時におこなわれ、その後は訪問者あたり約 1 週間に 1 回おこなわれます）。1. パケットアナライザーまたは Web ブラウザーデバッガーのネットワークパネルを使用して、[!DNL dpm.demdex.net] へのリクエストを検索します。
1. 応答に `d_mid` と値が含まれていることを確認します（例：`_setMarketingCloudFields({"d_mid":"4235...`）。
1. Analytics リクエストに mid パラメーター（Experience Cloud ID）が含まれていることを確認します。猶予期間中（有効になっている場合）には、aid パラメーター（Analytics 訪問者 ID）も表示されます。

Experience Cloud ID を含む期待される応答：

![](assets/mac_id_response.png)

Experience Cloud ID（mid）を含む Analytics イメージリクエスト：

![](assets/mid.png)

mbox リクエストの Experience Cloud ID：

![](assets/mbox_request.png)

**猶予期間とは**

訪問者 ID サービスをデプロイすると、新しい訪問者はデータ収集サーバーから Analytics 訪問者 ID を受け取らなくなります。サイトの一部で訪問者 ID サービスの導入が終わっていない場合は、訪問者がこれらのセクションを訪問したときに、Experience Cloud ID が認識されず、訪問者には従来の Analytics 訪問者 ID が割り当てられてしまいます。その結果、訪問者数が重複してカウントされたり、誤った属性が割り当てられたりするなどの問題が生じる可能性があります。

例えば、サイトのサポートセクションを別の CMS で管理している場合は、そのセクション用に別の Analytics JavaScript ファイルを使用していることがあります。このサポートサイトに訪問者 ID サービスをデプロイする前にメインサイトで訪問者 ID をデプロイした場合は、新しい訪問者はサポートセクションの訪問時に従来の Analytics ID を受け取り、両方のサイトセクションへの訪問がそれぞれ異なる訪問としてレポートされます。

複数の JavaScript ファイルまたは他のテクノロジー（Flash など）を使用しているサイトに訪問者 ID サービスを導入すると、サイトのすべての部分で同時に訪問者 ID サービスを有効にする必要があるので、調整の問題が発生する可能性があります。猶予期間を設定することにより、新しい訪問者は訪問者 ID サービスから引き続き Analytics 訪問者 ID を受け取るので、アップグレードされておらずまだ訪問者 ID サービスを使用していないサイトのセクションでも、訪問者を一貫性のある形で識別できます。

## 手順 7.ユーザーと製品を管理する {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

準備が整ったら、**[!UICONTROL 管理]**／**[!UICONTROL Admin Console を起動]**&#x200B;をクリックし、ユーザーおよび製品プロファイルを管理できます。

![](assets/menu-administration-shell.png)

[Experience Cloud のユーザーおよび製品の管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)を参照してください。

**顧客属性**

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Target). 
 </note> </p> 
 -->

顧客属性グループに追加されたユーザーには、Experience Cloud インターフェイスの左側に[!UICONTROL 顧客属性]メニュー項目が表示されます。

## 手順 8.コアサービスの使用を開始する {#section_960C06093623462E8EA247B3E97274A1}

次のコアサービス機能を利用します。

![](assets/menu-audiences-shell.png)

**People／顧客属性**

エンタープライズ顧客データを顧客関係管理（CRM）データベースに取り込んでいる場合は、そのデータを Experience Cloud の顧客属性データソースにアップロードできます。アップロード後は、データを [!DNL Adobe Analytics] と [!DNL Adobe Target] で利用できます。

[顧客属性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)を参照してください。

**People／オーディエンスライブラリ**

Experience Cloud オーディエンスは、オーディエンスを作成したり、既存のオーディエンスを組み合わせて複合オーディエンスを作成したり、共有しているすべてのオーディエンスを表示したりできるインターフェイスです。

[オーディエンス](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)を参照してください。

<!-- aam_mc.xml -->

## データストレージおよびプライバシー開示情報

Adobe [!DNL Experience Cloud] 内のリアルタイムのオーディエンスプロファイルおよびその他のコアサービスを利用する場合、これらのサービスの使用は、データが保管されるデータセンター（および国）の選択に影響を与えることがあります。特に、Adobe [!DNL Experience Cloud] のコアサービスは Adobe Audience Manager を利用するので、People コアサービス内で使用されるデータは米国の Audience Manager サーバー内に存在する必要があります。

コアサービスの利用を People コアサービス経由で有効にした場合、他のアドビ製品から Audience Management に送信されるデータのタイプは、次のようになります。

* [!DNL Analytics] キーと値のペア（prop、eVar、リスト変数、その他）。デフォルトでは、ログの行には、IP の最終オクテット（IP アドレスが Adobe [!DNL Analytics] の IP の不明化設定で変更されていないと仮定）を含む IP アドレスが含まれます。
* Audience Manager に設定されたルールに基づいて訪問者が資格を得る特徴とセグメント。
* （オプション）お使いの ID のうちの 1 つまたは複数。ID サービスの導入に応じて、CRM ID またはハッシュの電子メールアドレスなど、お使いの ID のうち 1 つまたは複数が送信されることもあります。このデータが Adobe [!DNL Analytics] に送信されると、Adobe Audience Management に転送されます。個人データを Adobe [!DNL Analytics] に提供しないことを推奨します。代わりに、アドビに送付する前に、一方向のハッシュを使用してデータを偽名化します。
* バックエンドのセグメント共有機能を使用した、[!DNL Analytics] から取得されるセグメント。
* サードパーティ Cookie がブロックされない場合、demdex.net Cookie が設定されます。`AMCV_###@AdobeOrg` ファーストパーティ Cookie は、常に Experience Cloud ID（以前の訪問者 ID サービス）を使用して設定されます。


これらすべてのデータ要素は、ログファイルの形式で Adobe Audience Manager に配信されます。Audience Manager は、このデータを米国内で処理および格納します。Audience Manager は、このデータを米国外に格納または処理するオプションは提供しません。

**Cookie およびオプトアウト**

リアルタイムのオーディエンスプロファイルの使用では、[!DNL Analytics] および [!DNL Target] に使用する Cookie に加えて、Audience Manager Cookie を利用します。

適切なオプトアウト機能を提供したい場合、サイトへの訪問者は、既存のオプトアウト処理に Audience Manager オプトアウトを追加する必要があります。

手順については、Adobe Experience Cloud ヘルプの[アドビオプトアウトの導入](https://marketing.adobe.com/resources/help/en_US/sc/implement/opt_out.html)を参照してください。

クロスドメイントラッキングの有効化については、[データ収集 CNAME およびクロスドメイントラッキング](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_cname)を参照してください。
