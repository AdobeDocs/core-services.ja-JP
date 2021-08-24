---
description: 'ログイン方法と、Experience Cloudの中央のインターフェイスコンポーネントについて説明します。 グローバル検索、アカウント設定、インターフェイスの操作方法、ヘルプの参照方法について説明します。 '
solution: Experience Cloud
title: 'Experience Cloud 中央の UI コンポーネント '
feature: 「中央インターフェイスコンポーネント」
topic: 管理
role: Admin, User
level: Beginner, Intermediate, Experienced
source-git-commit: c9a6059b0af9c6229fd72580f997c1c6f2dfbbe4
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 50%

---

# Experience Cloud インターフェイスヘルプ

Experience Cloud の中央インターフェイスコンポーネントには、次の機能が含まれます。

* ログインしてアプリケーションとサービスにアクセスする
* グローバル検索を使用して製品ヘルプとビジネスオブジェクトを検索する
* アカウント設定（アラート、通知、サブスクリプション）の管理

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

## Experience Cloud にサインインする {#signin}

ログインし、自分が適切な[組織](organizations.md)に属していることを確認します。

1. [Adobe Experience Cloud](https://experience.adobe.com) に移動します。
1. 「**[!UICONTROL Adobe IDでログイン]**」を選択します。
1. 自分が適切な組織に属していることを確認します。

   ![](assets/organizations-menu.png)

   自分が正しい[組織](organizations.md)にログインしたことを確認するには、自分のプロフィールのアバターをクリックして組織名を確認します。 複数の組織にアクセスできる場合は、ヘッダーバーで別の組織を表示して切り替えることもできます。

   組織がFederated IDを使用している場合、Experience Cloudを使用すると、電子メールアドレスとパスワードを入力しなくても、組織のシングルサインオンでサインインできます。 これをおこなうには、Experience CloudURL(`https://experience.adobe.com`)に`#/sso:@domain`を追加します。

   例えば、Federated IDとドメイン`adobecustomer.com`を持つ組織の場合、URLリンクを`https://experience.adobe.com/#/sso:@adobecustomer.com`に設定します。 また、このURLにアプリケーションパスを追加してブックマークを付けることで、特定のアプリに直接アクセスすることもできます。 (例：Adobe Analyticsの場合は`https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`)。

## Experience Cloud アプリケーションへのアクセス {#navigation}

Experience Cloud にログインすると、統合ヘッダーからすべてのアプリケーション、サービスおよび組織にすばやくアクセスできます。

所有するアプリケーションサービスにアクセスするには、Experience Cloudセレクター![](assets/menu-icon.png)を選択します。

![](assets/platform-core-services.png)

## Experience Cloud での検索とサポート {#search}

Experience Cloud の検索では、[Experience League](https://experienceleague.adobe.com/?lang=ja#home) 上のヘルプ（ドキュメント、チュートリアル、コース）を検索できます。

![](assets/search-menu.png)

[!UICONTROL ヘルプ]メニューからも、次の項目にアクセスできます。

* **[!UICONTROL サポート]：** サポートチケットを作成するか、Twitter を使用して[!UICONTROL サポート]にお問い合わせください。
* **[!UICONTROL フィードバック]：**&#x200B;フィードバックを使用してアドビに連絡し、ご意見をお聞かせください。
* **[!UICONTROL ステータス]：** に移動して、製品の `https://status.adobe.com/experience_cloud` 運用状況と[!UICONTROL サブスクリプションの管理]を確認します。
* **[!UICONTROL Developer Connection]：** `adobe.io` に移動して、開発者向けドキュメントを見つけます。

## アカウント設定 {#account-menu}

アカウントの環境設定メニューで、次の操作を実行できます。

* ダークテーマを指定する（このテーマに対応していないアプリケーションもあります）
* [組織](organizations.md)を検索する
* ログアウト
* アカウントの[環境設定、通知、サブスクリプション](#preferences)を設定する

### Experience Cloud の[!UICONTROL 環境設定]を管理する {#preferences}

Experience Cloud の環境設定には、通知、購読、アラートが含まれます。

アカウントメニュー![](assets/preferences-icon-sm.png)から「**[!UICONTROL 環境設定]**」を選択して、環境設定を管理します。

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

「**[!UICONTROL 通知]**」を選択すると、重要な通知や、Adobeからのお知らせを表示できます。

![](assets/notifications-menu-small.png)

通知は、[Experience Cloud の環境設定](#preferences)で設定できます。
