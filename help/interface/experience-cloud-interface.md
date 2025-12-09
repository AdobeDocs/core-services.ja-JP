---
description: ログイン方法と、Experience Cloud の中央インターフェイスコンポーネントについて説明します。グローバル検索、アカウント設定、インターフェイスの操作方法およびヘルプの入手方法について説明します。
solution: Experience Cloud
title: Experience Cloud Central の UI コンポーネント
feature: Central Interface Components
topic: Administration
role: Admin, User
level: Beginner, Intermediate, Experienced
source-git-commit: 63d5c080a7282c78eb7a66c5a54c69b5597545ab
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 78%

---

# Experience Cloud中央インターフェイスコンポーネント

Experience Cloud の中央インターフェイスコンポーネントには、次の機能が含まれます。

* ログインしてアプリケーションとサービスにアクセスする
* グローバル検索を使用して製品ヘルプとビジネスオブジェクトを検索する
* アカウント設定（アラート、通知、サブスクリプション）の管理

## Experience Cloud でのブラウザーのサポート

最高のパフォーマンスを実現するために、Experience Cloud は、一番人気のブラウザー（最新バージョンに加えて 2 つ前までのバージョンを含む）に合わせて最適化されています。

* Chrome
* Edge
* Firefox
* Opera
* Safari

ブラウザーがリストに表示されない場合でも、サポートされている可能性はありますが、リストに表示されたブラウザーの いずれかを使用することをお勧めします。

>[!NOTE]
>
>Experience Cloud ドメインで実行されているすべてのアプリケーションがすべてのブラウザーをサポートしているわけではありません。不明な場合は、特定のアプリケーションのドキュメントを確認してください。

## Experience Cloud での言語サポート

Experience Cloud は、アドビユーザーアカウントの環境設定で設定された各ユーザーの優先言語をサポートしています。現在サポートされている言語は次のとおりです。

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

すべてのアプリケーションチームはグローバルな言語サポートに取り組んでいますが、一部のアプリケーションは、上記のすべての言語では提供されていません。プライマリ言語が Experience Cloud アプリケーションでサポートされていない場合、利用可能であればセカンダリ言語をデフォルトに設定することもできます。 これは、[Experience Cloud のユーザーの環境設定](https://experience.adobe.com/preferences) で実行できます。

## Experience Cloud にサインインする

ログインし、自分が適切な組織に属していることを確認します。

1. [Adobe Experience Cloud](https://experience.adobe.com) に移動します。
1. 「**[!UICONTROL Sign in with an Adobe ID]**」をクリックします。
1. 自分が適切な組織に属していることを確認します。

   ![組織の検証](assets/organizations-menu.png)

   正しい組織にログインしていることを確認するには、「**[!UICONTROL Profile]**」をクリックして組織名を表示します。 複数の組織にアクセスできる場合は、**[!UICONTROL Organization]** セレクターを使用して別の組織を表示して切り替えることもできます。

   組織が Federated ID を使用している場合、Experience Cloud を使用すると、自身のメールアドレスとパスワードを入力しなくても、組織のシングルサインオンでログインできます。`#/sso:@domain` を Experience Cloud URL（`https://experience.adobe.com`）に追加して、このタスクを完成します。

   例えば、Federated ID を持ち、ドメインが `adobecustomer.com` の組織の場合、URL リンクを `https://experience.adobe.com/#/sso:@adobecustomer.com` に設定します。 また、この URL にアプリケーションパスを付けてブックマークに追加することで、特定のアプリケーションに直接移動することもできます。 （例えば、Adobe Analytics の場合は `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。）

## Experience Cloud アプリケーションへのアクセス

Experience Cloud にログインすると、統合ヘッダーからすべてのアプリケーション、サービスおよび組織にすばやくアクセスできます。

自身が所有しているExperience Cloud サービスにアクセスするには、アプリケーションセレクター ![&#x200B; メニュー &#x200B;](assets/menu-icon.png) をクリックします。

![Experience Cloud アプリケーションへのアクセス](assets/platform-core-services.png)

## Experience Cloud での検索とサポート

Experience Cloud の検索では、[Experience League](https://experienceleague.adobe.com/ja?lang=ja#home) 上のヘルプ（ドキュメント、チュートリアル、コース）を検索できます。

![Experience Cloud での検索とサポート](assets/search-menu.png)

[!UICONTROL Help] メニューからも、次の項目にアクセスできます。

* **[!UICONTROL Support]:** サポートチケットを作成するか、Twitter を使用して [!UICONTROL Support] に連絡します。
* **[!UICONTROL Feedback]:** フィードバックを使用してAdobeに連絡し、ご意見をお聞かせください。
* **[!UICONTROL Status]:** `https://status.adobe.com/experience_cloud` に移動して、製品の動作ステータスと [!UICONTROL Manage Subscriptions] を確認します。
* **[!UICONTROL Developer Connection]:** `adobe.io` に移動して、開発者向けドキュメントを見つけます。

## アカウント設定

アカウントの環境設定メニューで、次の操作を実行できます。

* ダークテーマを指定する（このテーマに対応していないアプリケーションもあります）
* 組織の検索
* ログアウト
* アカウントの[環境設定、通知、サブスクリプション](#preferences)を設定する

### Experience Cloud [!UICONTROL Preferences] の管理

Experience Cloud の環境設定には、通知、購読、アラートが含まれます。

* アカウントメニュー **[!UICONTROL Preferences]** 環境設定 ![&#x200B; から「](assets/preferences-icon-sm.png)」をクリックして、環境設定を管理します。

![Experience Cloud の管理](assets/preferences-page.png)

[!UICONTROL Experience Cloud preferences] では、次の機能を設定できます。

| 機能 | 説明 |
|--- |--- |
| デフォルトの組織 | Experience Cloud の起動時に表示する組織を選択します。 |
| [!UICONTROL Subscriptions] | 購入する製品とカテゴリを選択します。[!UICONTROL Notifications] ポップオーバーとメール内の通知。 |
| [!UICONTROL Priority] | 優先度が高いと見なすカテゴリを選択します。これらのカテゴリには「高」タグが付き、アラートんなどの配信用に設定できます。 |
| [!UICONTROL Alerts] | ブラウザーにアラートを表示する通知を選択します。アラートは、ウィンドウの右上隅に数秒間表示されます。 |
| メール | 通知メールの受信頻度を指定します。（送信しない、即時、毎日または毎週） |

{style="table-layout:auto"}

## 通知とお知らせ

「**[!UICONTROL Notifications]**」をクリックすると、重要な通知や、Adobeからのお知らせを表示できます。

![通知とお知らせ](assets/notifications-menu-small.png)

通知は、[Experience Cloud の環境設定](#preferences)で設定できます。
