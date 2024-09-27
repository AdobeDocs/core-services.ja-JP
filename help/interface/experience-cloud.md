---
description: Experience Cloud 用の中央インターフェイスコンポーネントについて説明します。Admin Console でユーザーと製品の管理に関するヘルプを取得し、Experience Cloud サービス用のアプリケーションを有効にします。オーディエンスライブラリ、顧客属性、Experience Cloud アセットなどに関するヘルプを取得します。
title: Experience Cloud インターフェイスのドキュメント
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: cd5d4978f2dcaf79030022cbc0fe67c4c8099775
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 85%

---

# Experience Cloud 中央インターフェイスの概要

[Experience Cloud](https://experience.adobe.com) には、アドビが提供するデジタルマーケティングアプリケーション、製品およびサービスが統合されています。直感的なインターフェイスから、クラウドアプリケーション、製品機能、サービスにすばやくアクセスできます。

![Experience Cloud](assets/landing.png)

Experience Cloud のヘッダーから、次の操作を実行できます。

* すべてのExperience Cloudアプリケーションおよびサービスへのアクセス
* ヘルプメニューから、製品ドキュメント、チュートリアル、コミュニティへの投稿を検索します。Experience League で結果を表示します。
* 「検索」フィールドのグローバル検索を使用したビジネスオブジェクトの検索（Experience Platform ユーザーのみ）。
* アカウントの管理 [ 環境設定 ](features/account-preferences.md) （アラート、通知、購読）

## Experience Cloud にサインインする {#signin}

ログインし、自分が適切な[組織](administration/organizations.md)に属していることを確認します。

1. [Adobe Experience Cloud](https://experience.adobe.com) に移動します。
1. アドビのメールアドレスを入力し、「**[!UICONTROL 続行]**」を選択します。
1. アカウントを選択します。
1. パスワードを入力します。
1. 自分が適切な組織に属していることを確認します。

   ![自身が適切な組織に所属していることを確認](assets/organizations-menu.png)

   **組織の検証**

   正しい [組織](administration/organizations.md) にログインしていることを確認するには、プロファイルのアバターをクリックして組織名を表示します。複数の組織にアクセスできる場合は、ヘッダーバーで別の組織を表示して切り替えることもできます。

   組織が Federated ID を使用している場合、Experience Cloud を使用すると、自身のメールアドレスとパスワードを入力しなくても、組織のシングルサインオンでログインできます。`#/sso:@domain` を Experience Cloud URL（`https://experience.adobe.com`）に追加して、このタスクを完成します。

   例えば、Federated ID を持ち、ドメインが `adobecustomer.com` の組織の場合、URL リンクを `https://experience.adobe.com/#/sso:@adobecustomer.com` に設定します。 また、この URL にアプリケーションパスを付けてブックマークに追加することで、特定のアプリケーションに直接移動することもできます。 （例えば、Adobe Analytics の場合は `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。）

## Experience Cloud アプリケーションへのアクセス {#navigation}

Experience Cloud にログインすると、統合ヘッダーからすべてのアプリケーション、サービスおよび組織にすばやくアクセスできます。

組織内でプロビジョニングされた Experience Cloud のアプリケーションおよびサービスにアクセスするには、アプリケーションセレクター ![メニュー](assets/menu-icon.png) に移動します。

![Experience Cloud アプリケーションへのアクセス](assets/platform-core-services.png)

## お問い合わせとサポート {#support}

[Experience League](https://experienceleague.adobe.com/?lang=ja#home) のヘルプコンテンツ（ドキュメント、チュートリアル、コース）および個々のアプリケーションの追加リソースなど、ヘッダーのヘルプアイコン（![アセット](assets/help-icon.png)）を使用して、学習やヘルプにアクセスします。自由形式のフィードバックを送信して、優先度の高いサポートチケットを作成することもできます。

![お問い合わせとサポート](assets/search-menu.png)

[!UICONTROL ヘルプ]メニューからも、次の項目にアクセスできます。

* **[!UICONTROL サポート]：** サポートチケットを作成するか、Twitter を使用して[!UICONTROL サポート]にお問い合わせください。
* **[!UICONTROL フィードバック]：** Experience Cloud のエクスペリエンスに関するフィードバックをお寄せください。フィードバックは、アドビの製品およびサービスを改善するために使用されます。
* **[!UICONTROL ステータス]：** に移動して、製品の `https://status.adobe.com/experience_cloud` 運用状況と[!UICONTROL サブスクリプションの管理]を確認します。
* **[!UICONTROL Developer Connection]：** `adobe.io` に移動して、開発者向けドキュメントを見つけます。

## ユーザープロファイルの管理

ユーザープロファイル メニューでは、次の操作を実行できます。

* ダークテーマを指定する（このテーマに対応していないアプリケーションもあります）
* Experience Cloud の[環境設定](features/account-preferences.md)を管理する
* [ 組織 ](administration/organizations.md) を選択または検索
* 表示 [!UICONTROL  法律上の注意 ]
* ログアウト
* アカウントの環境設定、通知、サブスクリプションを設定する

## 製品内通知とお知らせの表示 {#notifications}

ベルアイコンをクリックして、通知とお知らせを表示します。 お知らせは、製品リリース、メンテナンス通知、共有項目、承認リクエストなど、関連性の高い実用的な更新にすることができます。

![通知とお知らせ](assets/notifications-menu-small.png)

通知とアラートを管理するには、[ アカウント設定と通知 ](features/account-preferences.md) を参照してください。
