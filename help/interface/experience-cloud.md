---
description: Experience Cloud 用の中央インターフェイスコンポーネントについて説明します。 このヘルプには、Admin Console でのユーザーと製品の管理、Experience Cloud サービスのアプリケーションの有効化、オーディエンスライブラリ、顧客属性、Experience Cloud アセットなどに関するヘルプが含まれます。
solution: Experience Cloud
title: Experience Cloud インターフェイスのヘルプとドキュメント
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: '"顧客属性"'
topic: 管理
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: 4534f764ea821576c3ac5cd1959d387a3689e837
workflow-type: tm+mt
source-wordcount: '1306'
ht-degree: 63%

---

# Experience Cloud の主要なインターフェイスコンポーネントガイド

[Experience Cloud](https://experience.adobe.com) には、アドビが提供するデジタルマーケティングアプリケーション、製品およびサービスが統合されています。直感的なインターフェイスから、クラウドアプリケーション、製品機能、サービスにすばやくアクセスできます。

![Experience Cloud](assets/landing.png)

Experience Cloud のヘッダーから、次の操作を実行できます。

* アプリケーションとサービスへのアクセス
* 製品ドキュメント、チュートリアル、コミュニティの投稿を検索する
* グローバル検索を使用したビジネスオブジェクトの検索（Experience Platform ユーザーのみ）
* アカウント設定（アラート、通知、サブスクリプション）の管理

## Experience Cloud にサインインする {#signin}

ログインし、自分が適切な[組織](organizations.md)に属していることを確認します。

1. [Adobe Experience Cloud](https://experience.adobe.com) に移動します。
1. 「**[!UICONTROL Adobe IDでログイン]**」を選択します。
1. 自分が適切な組織に属していることを確認します。

   ![](assets/organizations-menu.png)

   **組織の検証**

   自分が正しい[組織](organizations.md)にログインしたことを確認するには、自分のプロフィールのアバターをクリックして組織名を確認します。 複数の組織にアクセスできる場合は、ヘッダーバーで別の組織を表示して切り替えることもできます。

   組織がFederated IDを使用している場合、Experience Cloudを使用すると、電子メールアドレスとパスワードを入力しなくても、組織のシングルサインオンでサインインできます。 これをおこなうには、Experience CloudURL(`https://experience.adobe.com`)に`#/sso:@domain`を追加します。

   例えば、Federated IDとドメイン`adobecustomer.com`を持つ組織の場合、URLリンクを`https://experience.adobe.com/#/sso:@adobecustomer.com`に設定します。 また、このURLにアプリケーションパスを追加してブックマークを付けることで、特定のアプリに直接アクセスすることもできます。 (例：Adobe Analyticsの場合は`https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`)。

## Experience Cloud アプリケーションへのアクセス {#navigation}

Experience Cloud にログインすると、統合ヘッダーからすべてのアプリケーション、サービスおよび組織にすばやくアクセスできます。

組織内でプロビジョニングされたExperience Cloudアプリケーションおよびサービスにアクセスするには、アプリケーションセレクター![](assets/menu-icon.png)に移動します。

![](assets/platform-core-services.png)

## Experience Cloudでのブラウザーのサポート {#browser}

最高のパフォーマンスを得るために、Experience Cloudは、最新バージョンに加えて2つ前のバージョンを含む、最も一般的なブラウザーに最適化されています。

* Chrome
* Edge
* Firefox
* Opera
* Safari

ブラウザーが一覧に表示されない場合でも、サポートされている可能性がありますが、一覧に表示されたブラウザーの1つを使用することをお勧めします。

>[!NOTE]
>
>すべてのブラウザーがExperience Cloudドメインで実行されているアプリケーションでサポートされているわけではありません。 不明な場合は、特定のアプリケーションのドキュメントを確認してください。

## Experience Cloudでの言語サポート {#languages}

Experience Cloudは、ユーザーアカウントの環境設定で設定された、各Adobeの優先言語をサポートします。 現在サポートされている言語は次のとおりです。

* 中国語
* 英語
* フランス語
* ドイツ語
* イタリア語
* 日本語
* 韓国語
* ポルトガル語
* スペイン語
* 台湾語

すべてのアプリケーションチームはグローバル言語のサポートに取り組んでいますが、すべてのアプリケーションが上記のすべての言語で提供されるわけではありません。 プライマリ言語がExperience Cloudアプリケーションでサポートされていない場合は、セカンダリ言語をデフォルトに設定することもできます。 これは、[Experience Cloudのユーザー設定](https://experience.adobe.com/preferences)で実行できます。

## お問い合わせとサポート {#support}

[Experience League](https://experienceleague.adobe.com/?lang=ja#home)のヘルプコンテンツ（ドキュメント、チュートリアル、コース）や、個々のアプリケーションの追加リソースなど、ヘッダーのヘルプアイコン(![asset](assets/help-icon.png))を使用して、学習やヘルプにアクセスします。 また、オープンエンドのフィードバックを送信し、優先度の高いサポートチケットを作成することもできます。

![](assets/search-menu.png)

[!UICONTROL ヘルプ]メニューからも、次の項目にアクセスできます。

* **[!UICONTROL サポート]：** サポートチケットを作成するか、Twitter を使用して[!UICONTROL サポート]にお問い合わせください。
* **[!UICONTROL フィードバック]：** Experience Cloud のエクスペリエンスに関するフィードバックをお寄せください。フィードバックは、アドビの製品およびサービスを改善するために使用されます。
* **[!UICONTROL ステータス]：** に移動して、製品の `https://status.adobe.com/experience_cloud` 運用状況と[!UICONTROL サブスクリプションの管理]を確認します。
* **[!UICONTROL Developer Connection]：** `adobe.io` に移動して、開発者向けドキュメントを見つけます。

## オブジェクトとエンティティのグローバル検索 {#search}

グローバル検索を使用すると、シームレスで一貫性のあるワンクリックエクスペリエンスで、検索可能なビジネスオブジェクトやエンティティを検索できます。 この検索では、最近アクセスしたオブジェクトが表示されます。

![](assets/platform-search.png)

>[!NOTE]
>
>グローバル検索は、すべてのExperience Cloudアプリケーション内で使用できるわけではありませんが、インデックスが追加されると、関連するアプリケーションに追加されます。 2021年7月から利用可能：

* Experience Platform
* Journey Optimizer

## ユーザープロファイルとアカウントの環境設定 {#preferences}

Experience Cloud の環境設定には、通知、購読、アラートが含まれます。アカウントの環境設定メニューで、次の操作を実行できます。

* ダークテーマを指定する（このテーマに対応していないアプリケーションもあります）
* [組織](organizations.md)を検索する
* ログアウト
* アカウントの環境設定、通知、サブスクリプションを設定する

環境設定を管理するには、アカウントメニュー![](assets/preferences-icon-sm.png)から&#x200B;**[!UICONTROL 環境設定]**&#x200B;を選択します。

![](assets/preferences-page.png)

[!UICONTROL Experience Cloud の環境設定]では、次の機能を設定できます。

| 機能 | 説明 |
|--- |--- |
| デフォルトの[組織](organizations.md) | Experience Cloud の起動時に表示する組織を選択します。 |
| [!UICONTROL サブスクリプション] | 購入する製品とカテゴリを選択します。[!UICONTROL 通知]ポップオーバーとメール内の通知。 |
| [!UICONTROL 優先度] | 優先度が高いと見なすカテゴリを選択します。これらのカテゴリには「高」タグが付き、アラートんなどの配信用に設定できます。 |
| [!UICONTROL アラート] | ブラウザーにアラートを表示する通知を選択します。アラートは、ウィンドウの右上隅に数秒間表示されます。 |
| メール | 通知メールの受信頻度を指定します。（送信しない、即時、毎日または毎週） |

{style=&quot;table-layout:auto&quot;}

## 通知とお知らせ {#notifications}

**[!UICONTROL 通知]**&#x200B;を選択して、製品リリース、メンテナンス通知、共有項目、承認リクエストなど、関連性の高い実用的な更新に関する警告を表示します。

![](assets/notifications-menu-small.png)

## Experience Cloudドメイン {#domains}

Experience Cloudは、次のホストを使用してアプリケーションを配信し、パフォーマンスと製品のエクスペリエンスを向上します。 Adobeは、最適なエクスペリエンスを得るために、これらのドメインをファイアウォールの許可リストに追加することを推奨します。 Adobe Analyticsなどの特定のExperience Cloudアプリケーションで、追加のドメインが使用される場合もあります。 詳しくは、各アプリケーションのドキュメントを参照してください。

| 技術 | ドメイン |
|--- |--- |
| Adobe Experience Cloudドメイン | `adobe.com`、`adobe.net`、`adobe.io` |
| AdobeIdentity Managementサービス(IMS) | `adobelogin.com` |
| Experience Cloudフォント | `typekit.net` |
| Gainsight （製品ガイダンスおよびヘルプ用） | `esp.aptrinsic.com` |

## 管理およびクロスアプリケーションサービスに関するお問い合わせ

このガイドでは、Admin Console の Experience Cloud ユーザーと製品管理に関するヘルプにアクセスし、プラットフォームサービスのソリューションを有効にする方法について説明します。オーディエンスライブラリ、顧客属性、Experience Cloud アセットなどのヘルプにアクセスすることもできます。

* [[!UICONTROL オーディエンスライブラリ]](audience-library.md)
* [[!UICONTROL 顧客属性]](attributes.md)
* [[!UICONTROL Triggers]](triggers.md)
* [Experience Cloud [!UICONTROL Assets]](experience-cloud-assets.md)
* [Experience Cloud の cookie](cookies-privacy.md)
* [ユーザーおよび製品の管理](admin-getting-started.md)（Admin Console）
* [ソリューションのコアサービスへの対応](core-services.md)
* [よくある質問](admin-getting-started.md)
* [組織とアカウントのリンク](organizations.md)
* [統合](marketing-cloud-integrations.md)
* [Adobe Target と Experience Cloud の統合](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=ja)
* [Experience Cloud のプライバシーとセキュリティの概要](assets/Adobe-Marketing-Cloud-Privacy-and-Security-Overview.pdf)
* [DNS プリフェッチ](admin-getting-started.md#concept_6BC8C6856E3644F8956D7AD0A96383B7)

## ガイド

関連する Experience Cloud ガイドは次のとおりです。

* [Adobe Mobile](https://experienceleague.adobe.com/docs/mobile-services/using/home.html?lang=ja)
* [Experience Platform Co-op Graph](https://experienceleague.adobe.com/docs/device-co-op/using/home.html?lang=ja)
* [Exchange](https://exchange.adobe.com/experiencecloud)
* [Experience Cloud ID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)
* [Experience Platform データ収集／Launch](https://experienceleague.adobe.com/docs/launch.html?lang=ja)
* [Experience Cloud デバッガー](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=ja)
* [一般データ保護規則（GDPR）API](https://www.adobe.io/apis/experiencecloud/gdpr.html)
* [[!UICONTROL Dynamic Tag Management]](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=en)

## チュートリアル

セルフサービスのチュートリアルと、Experience League のクイックハウツーを活用：

* [Experience League のすべてのチュートリアル](https://experienceleague.adobe.com/?lang=ja#quick-how-tos)
* [Experience Platform チュートリアル](https://experienceleague.adobe.com/docs/launch-learn/tutorials/overview.html?lang=ja)
* [リアルタイム顧客データプラットフォーム](https://experienceleague.adobe.com/docs/platform-learn/tutorials/application-services/rtcdp/understanding-the-real-time-customer-data-platform.html?lang=ja)

## リリースノートおよび関連する Experience Cloud ヘルプ

* [すべての Experience Cloud ソリューションの製品ドキュメント](https://experienceleague.adobe.com/docs/home.html?lang=ja) - Experience Cloud のラーニングとサポートでヘルプを参照する
* [リリースノートと製品アップデート](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ja) - Experience Cloud の新機能を参照およびサブスクリプションでアップデートを入手する
* [コアサービスの実装に関するチュートリアル](https://experienceleague.adobe.com/docs/launch-learn/tutorials/overview.html?lang=en) - コアサービスに関するビデオやチュートリアルを参照する
* [Experience League で提供されるエキスパートヘルプ](https://experienceleague.adobe.com/?lang=ja) - 専門家やコミュニティからガイド付きの指導を受ける
* [教育とトレーニング](https://helpx.adobe.com/jp/learning.html?promoid=KAUDK) - アドビと連携してアドビ製品を最大限に活用する
* [エクスペリエンスブログ](https://blog.adobe.com/jp/topics/digital-transformation.html) - Experience Cloud のブログを読む
* [カスタマーケア](https://experienceleague.adobe.com/?support-solution=General&amp;lang=ja#support) - アドビカスタマーケアに問い合わせる
