---
description: CX Enterpriseの一元的なインターフェイスコンポーネントにログインする方法と概要について説明します。 グローバル検索、アカウント設定、インターフェイスの操作方法およびヘルプの入手方法について説明します。
solution: Experience Cloud
title: Experience Cloud Central の UI コンポーネント
feature: Central Interface Components
topic: Administration
role: Admin, User
level: Beginner, Intermediate, Experienced
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 42%

---

# CX Enterpriseの中央インターフェイスのコンポーネント

CX Enterpriseの中央インターフェイスコンポーネントには、次の機能が含まれています。

* ログインしてアプリケーションとサービスにアクセスする
* グローバル検索を使用して製品ヘルプとビジネスオブジェクトを検索する
* アカウント設定（アラート、通知、サブスクリプション）の管理

## CX Enterpriseでのブラウザーのサポート

最高のパフォーマンスを実現するために、CX Enterpriseは、最新バージョンと以前の2つのバージョンを含む、最も人気のあるブラウザーに最適化されています。

* Chrome
* Edge
* Firefox
* Opera
* Safari

ブラウザーがリストに表示されない場合でも、サポートされている可能性はありますが、リストに表示されたブラウザーの いずれかを使用することをお勧めします。

>[!NOTE]
>
>CX Enterprise ドメインで実行されているすべてのアプリケーションが、すべてのブラウザーをサポートしているわけではありません。 不明な場合は、特定のアプリケーションのドキュメントを確認してください。

## CX Enterpriseの言語サポート

CX Enterpriseでは、Adobe ユーザーアカウントの環境設定で設定されている、各ユーザーの優先言語をサポートしています。 現在サポートされている言語は次のとおりです。

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

すべてのアプリケーションチームはグローバルな言語サポートに取り組んでいますが、一部のアプリケーションは、上記のすべての言語では提供されていません。 CX Enterprise アプリケーションで主要言語がサポートされていない場合は、セカンダリ言語をデフォルトの言語に設定することもできます。 これは、[CX Enterpriseのユーザー設定](https://experience.adobe.com/preferences)で実行できます。

## CX Enterpriseにログイン

ログインして、正しい組織に属していることを確認します。

1. [Adobe CX Enterprise](https://experience.adobe.com)に移動します。
1. 「**[!UICONTROL Sign in with an Adobe ID]**」をクリックします。
1. 自分が適切な組織に属していることを確認します。

   ![組織の検証](assets/organizations-menu.png)

   正しい組織にログインしていることを確認するには、**[!UICONTROL Profile]**&#x200B;をクリックして組織名を表示します。 複数の組織にアクセスできる場合は、**[!UICONTROL Organization]** セレクターを使用して別の組織を表示して切り替えることもできます。

   組織でFederated IDを使用している場合は、CX Enterpriseを使用すると、メールアドレスとパスワードを入力しなくても、組織のシングルサインオンでログインできます。 CX Enterprise URL （`https://experience.adobe.com`）に`#/sso:@domain`を追加して、このタスクを実行します。

   例えば、Federated ID を持ち、ドメインが `example.com` の組織の場合、URL リンクを `https://experience.adobe.com/#/sso:@example.com` に設定します。 また、この URL にアプリケーションパスを付けてブックマークに追加することで、特定のアプリケーションに直接移動することもできます。 （例えば、Adobe Analytics の場合は `https://experience.adobe.com/#/sso:@example.com/analytics`。）

## CX Enterpriseアプリケーションへのアクセス

CX Enterpriseにログインすると、統合ヘッダーからすべてのアプリケーション、サービス、組織にすばやくアクセスできます。

アプリケーションセレクター![menu](assets/menu-icon.png)をクリックして、所有しているCX Enterprise サービスにアクセスします。

![CX Enterprise アプリケーションへのアクセス ](assets/platform-core-services.png)

## CX Enterpriseでの検索とサポート

CX Enterprise検索を使用すると、[Experience League](https://experienceleague.adobe.com/ja#home)でヘルプ（ドキュメント、チュートリアル、コース）を検索できます。

![CX Enterpriseでの検索とサポート ](assets/search-menu.png)

[!UICONTROL Help] メニューでは、次のアクセス権も使用できます。

* **[!UICONTROL Support]:** サポートチケットを作成するか、Twitterを使用して[!UICONTROL Support]にお問い合わせください。
* **[!UICONTROL Feedback]:** フィードバックを使用してAdobeにお問い合わせください。ご意見をお聞かせください。
* **[!UICONTROL Status]:** `https://status.adobe.com/experience_cloud`に移動し、製品操作の状態と[!UICONTROL Manage Subscriptions]を確認します。
* **[!UICONTROL Developer Connection]:** `adobe.io`に移動して、開発者ドキュメントを見つけます。

## アカウント設定

アカウントの環境設定メニューで、次の操作を実行できます。

* ダークテーマを指定する（このテーマに対応していないアプリケーションもあります）
* 組織の検索
* ログアウト
* アカウントの[環境設定、通知、サブスクリプション](#preferences)を設定する

### CX Enterprise [!UICONTROL Preferences]を管理

CX Enterpriseの環境設定には、通知、サブスクリプション、アラートが含まれます。

* アカウントメニュー![環境設定](assets/preferences-icon-sm.png)の&#x200B;**[!UICONTROL Preferences]**&#x200B;をクリックして、環境設定を管理します。

![CX Enterpriseの管理](assets/preferences-page.png)

[!UICONTROL CX Enterprise preferences]では、次の機能を設定できます。

| 機能 | 説明 |
| --- | --- |
| 既定の組織 | CX Enterpriseの起動時に表示する組織を選択します。 |
| [!UICONTROL Subscriptions] | 購入する製品とカテゴリを選択します。 [!UICONTROL Notifications] ポップオーバーとメール内の通知。 |
| [!UICONTROL Priority] | 優先度が高いと見なすカテゴリを選択します。 これらのカテゴリには「高」タグが付き、アラートんなどの配信用に設定できます。 |
| [!UICONTROL Alerts] | ブラウザーにアラートを表示する通知を選択します。 アラートは、ウィンドウの右上隅に数秒間表示されます。 |
| メール | 通知メールの受信頻度を指定します。 （送信しない、即時、毎日または毎週） |

{style="table-layout:auto"}

## 通知とお知らせ

**[!UICONTROL Notifications]**&#x200B;をクリックすると、重要なお知らせ、およびAdobeからのお知らせが表示されます。

![通知とお知らせ](assets/notifications-menu-small.png)

[CX Enterpriseの環境設定](#preferences)で通知を設定できます。
