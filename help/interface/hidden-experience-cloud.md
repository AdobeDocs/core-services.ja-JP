---
description: Experience Cloud 用の中央インターフェイスコンポーネントについて説明します。Admin Console でユーザーと製品の管理に関するヘルプを取得し、Experience Cloud サービス用のアプリケーションを有効にします。オーディエンスライブラリ、顧客属性、Experience Cloud Assets などに関するヘルプを取得します。
title: Experience Cloud インターフェイスおよび管理
hide: true
hidefromtoc: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
source-git-commit: 609eaf1819189cb4eac76b2b58703b246dfb843b
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 83%

---

# Experience Cloud インターフェイスおよび管理

[Experience Cloud](https://experience.adobe.com) には、アドビが提供するデジタルマーケティングアプリケーション、製品およびサービスが統合されています。直感的なインターフェイスから、クラウドアプリケーション、製品機能、サービスにすばやくアクセスできます。

10 月 30 日非表示

![Experience Cloud](assets/landing.png)

Experience Cloud のヘッダーから、次の操作を実行できます。

* すべての Experience Cloud アプリケーションとサービスにアクセスします
* ヘルプメニューから、製品ドキュメント、チュートリアル、コミュニティへの投稿を検索します。Experience League で結果を表示します。
* 「検索」フィールドのグローバル検索を使用したビジネスオブジェクトの検索（Experience Platform ユーザーのみ）。
* アカウントの[環境設定](features/account-preferences.md)（アラート、通知、サブスクリプション）を管理します

## Experience Cloud にサインインする {#signin}

ログインし、自分が適切な[組織](administration/organizations.md)に属していることを確認します。

1. [Adobe Experience Cloud](https://experience.adobe.com) に移動します。
1. Adobe メールアドレスを入力し、「**[!UICONTROL Continue]**」をクリックします。
1. アカウントをクリックします。
1. パスワードを入力します。
1. 自分が適切な組織に属していることを確認します。

   ![自身が適切な組織に所属していることを確認](assets/organizations-menu.png)

   **組織の検証**

   [組織](administration/organizations.md)は、インターフェイスヘッダーに表示されます。

   組織が Federated ID を使用している場合、Experience Cloud を使用すると、自身のメールアドレスとパスワードを入力しなくても、組織のシングルサインオンでログインできます。`#/sso:@domain` を Experience Cloud URL（`https://experience.adobe.com`）に追加して、このタスクを完成します。

   例えば、Federated ID を持ち、ドメインが `adobecustomer.com` の組織の場合、URL リンクを `https://experience.adobe.com/#/sso:@adobecustomer.com` に設定します。 また、この URL にアプリケーションパスを付けてブックマークに追加することで、特定のアプリケーションに直接移動することもできます。 （例えば、Adobe Analytics の場合は `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。）

## Experience Cloud アプリケーションへのアクセス {#navigation}

Experience Cloud にログインすると、統合ヘッダーからすべてのアプリケーション、サービスおよび組織にすばやくアクセスできます。

組織内でプロビジョニングされた Experience Cloud のアプリケーションおよびサービスにアクセスするには、アプリケーションセレクター ![メニュー](assets/apps-icon.png) に移動します。

![Experience Cloud アプリケーションへのアクセス](assets/platform-core-services.png)

## お問い合わせとサポート {#support}

**[!UICONTROL Help center]** Experience League![&#x200B; のヘルプコンテンツ（ドキュメント、チュートリアル、コース）および個々のアプリケーションの追加リソースなど、ヘッダーの &#x200B;](assets/help-icon.png) ール（[asset](https://experienceleague.adobe.com/?lang=ja#home)）を使用して、学習やヘルプにアクセスします。 自由形式のフィードバックを送信して、優先度の高いサポートチケットを作成することもできます。

![お問い合わせとサポート](assets/search-menu.png)

[!UICONTROL Help] メニューからも、次の項目にアクセスできます。

* **[!UICONTROL Support]:** サポートチケットを作成するか、Twitter を使用して [!UICONTROL Support] に連絡します。
* **[!UICONTROL Feedback]:** Experience Cloudのエクスペリエンスに関するフィードバックをお寄せください。 フィードバックは、アドビの製品およびサービスを改善するために使用されます。
* **[!UICONTROL Status]:** `https://status.adobe.com/experience_cloud` に移動して、製品の動作ステータスと [!UICONTROL Manage Subscriptions] を確認します。
* **[!UICONTROL Developer Connection]:** `adobe.io` に移動して、開発者向けドキュメントを見つけます。

## ユーザープロファイルの管理

[!UICONTROL Profile] メニューでは、次の操作を実行できます。

* ダークテーマを指定する（このテーマに対応していないアプリケーションもあります）
* Experience Cloud の[環境設定](features/account-preferences.md)を管理する
* [組織](administration/organizations.md)を選択または検索する
* [!UICONTROL Legal Notices] を表示
* ログアウト
* アカウントの環境設定、通知、サブスクリプションを設定する

## 製品内通知とお知らせの表示 {#notifications}

ベルアイコンをクリックすると、通知とお知らせが表示されます。お知らせには、製品リリース、メンテナンス通知、共有項目、承認リクエストなど、関連性の高い実用的な更新が含まれる場合があります。

![通知とお知らせ](assets/notifications-menu-small.png)

通知とアラートを管理するには、[アカウントの環境設定と通知](features/account-preferences.md)を参照してください
