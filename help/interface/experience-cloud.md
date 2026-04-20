---
description: CX Enterprise（旧Experience Cloud）の中央インターフェイスコンポーネントについて説明します。 ユーザーと製品の管理に関するヘルプを取得し、共有インターフェイスサービスのアプリケーションを有効にします。 オーディエンスライブラリ、顧客属性、Assetsなどのヘルプを利用できます。
title: CX Enterprise インターフェイスおよび管理ガイド
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
TQID: https://experienceleague.adobe.com/7vFfu0DyoTnsrlrWVApm0LLW4jsC0LoXb55jJ3jdxeY
product_v2:
  - id: e1971122-7081-4556-9222-8a31bd71800c
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 553
ht-degree: 45%

---

# CX Enterpriseのインターフェイスと管理

[CX Enterprise](https://experience.adobe.com) （旧&#x200B;_Experience Cloud_）は、Adobeの統合デジタルマーケティングアプリケーション、製品、サービス群です。 直感的なインターフェイスから、クラウドアプリケーション、製品機能、サービスにすばやくアクセスできます。

<!-- ![CX Enterprise](assets/landing.png) -->

CX Enterpriseのヘッダーから、次の操作を実行できます。

* CX Enterpriseのあらゆるアプリケーションとサービスにアクセス
* ヘルプメニューから、製品ドキュメント、チュートリアル、コミュニティへの投稿を検索します。 Experience League で結果を表示します。
* 「検索」フィールドのグローバル検索を使用したビジネスオブジェクトの検索（Experience Platform ユーザーのみ）。
* アカウントの[環境設定](features/account-preferences.md)（アラート、通知、サブスクリプション）を管理します

## CX Enterpriseにログイン

ログインし、自分が適切な[組織](administration/organizations.md)に属していることを確認します。

1. [Adobe CX Enterprise](https://experience.adobe.com)に移動します。
1. Adobeの電子メールアドレスを入力し、**[!UICONTROL Continue]**&#x200B;をクリックします。
1. アカウントをクリックします。
1. パスワードを入力します。
1. 自分が適切な組織に属していることを確認します。

   ![自身が適切な組織に所属していることを確認](assets/organizations-menu.png)

   **組織の検証**

   [組織](administration/organizations.md)は、インターフェイスヘッダーに表示されます。

   組織でFederated IDを使用している場合は、CX Enterpriseを使用すると、メールアドレスとパスワードを入力しなくても、組織のシングルサインオンでログインできます。 CX Enterprise URL （`https://experience.adobe.com`）に`#/sso:@domain`を追加して、このタスクを実行します。

   例えば、Federated ID を持ち、ドメインが `example.com` の組織の場合、URL リンクを `https://experience.adobe.com/#/sso:@example.com` に設定します。 また、この URL にアプリケーションパスを付けてブックマークに追加することで、特定のアプリケーションに直接移動することもできます。 （例えば、Adobe Analytics の場合は `https://experience.adobe.com/#/sso:@example.com/analytics`。）

   **注：**&#x200B;お客様の組織の管理者は、IP アドレスによってAdobe製品へのアクセスを制限することができます。 その場合、CX Enterpriseにログインするか、これを有効にした組織に切り替えた後にエラーが発生する可能性があります。 詳細については、[IP アドレスによる製品アクセスの制限](https://helpx.adobe.com/enterprise/using/ip-based-access.html)を参照してください。


## CX Enterpriseアプリケーションへのアクセス

CX Enterpriseにログインすると、統合ヘッダーからすべてのアプリケーション、サービス、組織にすばやくアクセスできます。

組織内でプロビジョニングされたCX Enterprise アプリケーションとサービスにアクセスするには、アプリケーションセレクター![menu](assets/apps-icon.png)に移動します。

![CX Enterprise アプリケーションへのアクセス &#x200B;](assets/platform-core-services.png)

## お問い合わせとサポート

[Experience League](https://experienceleague.adobe.com/ja#home)に関するヘルプコンテンツ（ドキュメント、チュートリアル、コース）や個々のアプリケーションに関するその他のリソースなど、ヘッダーの&#x200B;**[!UICONTROL Help center]** （![asset](assets/help-icon.png)）を使用して、学習とヘルプにアクセスします。 自由形式のフィードバックを送信して、優先度の高いサポートチケットを作成することもできます。

![お問い合わせとサポート](assets/search-menu.png)

[!UICONTROL Help] メニューでは、次のアクセス権も使用できます。

* **[!UICONTROL Support]:** サポートチケットを作成するか、Twitterを使用して[!UICONTROL Support]にお問い合わせください。
* **[!UICONTROL Feedback]:** CX Enterprise エクスペリエンスに関するフィードバックを共有します。 フィードバックは、アドビの製品およびサービスを改善するために使用されます。
* **[!UICONTROL Status]:** `https://status.adobe.com/experience_cloud`に移動し、製品操作の状態と[!UICONTROL Manage Subscriptions]を確認します。
* **[!UICONTROL Developer Connection]:** `adobe.io`に移動して、開発者ドキュメントを見つけます。

## ユーザープロファイルの管理

[!UICONTROL Profile] メニューでは、次の操作を行うことができます。

* ダークテーマを指定する（このテーマに対応していないアプリケーションもあります）
* CX Enterprise [環境設定](features/account-preferences.md)の管理
* [組織](administration/organizations.md)を選択または検索する
* [!UICONTROL Legal Notices]を表示
* ログアウト
* アカウントの環境設定、通知、サブスクリプションを設定する

## 製品内通知とお知らせの表示

ベルアイコンをクリックすると、通知とお知らせが表示されます。 お知らせには、製品リリース、メンテナンス通知、共有項目、承認リクエストなど、関連性の高い実用的な更新が含まれる場合があります。

![通知とお知らせ](assets/notifications-menu-small.png)

通知とアラートを管理するには、[アカウントの環境設定と通知](features/account-preferences.md)を参照してください

