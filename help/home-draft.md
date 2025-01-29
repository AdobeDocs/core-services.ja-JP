---
description: Experience Cloud 用の中央インターフェイスコンポーネントについて説明します。Admin Console でユーザーと製品の管理に関するヘルプを取得し、Experience Cloud サービス用のアプリケーションを有効にします。オーディエンスライブラリ、顧客属性、Experience Cloud アセットなどに関するヘルプを取得します。
title: Experience Cloud インターフェイスのドキュメント
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: 163dc8ef83fb83a0e51879520bcb3ae697c95144
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 94%

---

# Experience Cloud 中央インターフェイスの概要

[Experience Cloud](https://experience.adobe.com) には、アドビが提供するデジタルマーケティングアプリケーション、製品およびサービスが統合されています。直感的なインターフェイスから、クラウドアプリケーション、製品機能、サービスにすばやくアクセスできます。

![Experience Cloud](assets/landing.png)

Experience Cloud のヘッダーから、次の操作を実行できます。

* すべての Experience Cloud アプリケーションとサービスにアクセスします
* ヘルプメニューから、製品ドキュメント、チュートリアル、コミュニティへの投稿を検索します。Experience League で結果を表示します。
* 「検索」フィールドのグローバル検索を使用したビジネスオブジェクトの検索（Experience Platform ユーザーのみ）。
* アカウントの[環境設定](features/account-preferences.md)（アラート、通知、サブスクリプション）を管理します

## Experience Cloud にサインインする {#signin}

ログインし、自分が適切な[組織](administration/organizations.md)に属していることを確認します。

1. [Adobe Experience Cloud](https://experience.adobe.com) に移動します。
1. Adobeのメールアドレスを入力し、「**[!UICONTROL 続行]**」をクリックします。
1. アカウントを選択します。
1. パスワードを入力します。
1. 自分が適切な組織に属していることを確認します。

   ![自身が適切な組織に所属していることを確認](assets/organizations-menu.png)

   **組織の検証**

   [組織](administration/organizations.md)は、インターフェイスヘッダーに表示されます。

   組織が Federated ID を使用している場合、Experience Cloud を使用すると、自身のメールアドレスとパスワードを入力しなくても、組織のシングルサインオンでログインできます。`#/sso:@domain` を Experience Cloud URL（`https://experience.adobe.com`）に追加して、このタスクを完成します。

   例えば、Federated ID を持ち、ドメインが `adobecustomer.com` の組織の場合、URL リンクを `https://experience.adobe.com/#/sso:@adobecustomer.com` に設定します。 また、この URL にアプリケーションパスを付けてブックマークに追加することで、特定のアプリケーションに直接移動することもできます。 （例えば、Adobe Analytics の場合は `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。）

## Experience Cloud アプリケーションへのアクセス {#navigation}

Experience Cloud にログインすると、統合ヘッダーからすべてのアプリケーション、サービスおよび組織にすばやくアクセスできます。

組織内でプロビジョニングされた Experience Cloud のアプリケーションおよびサービスにアクセスするには、アプリケーションセレクター ![メニュー](assets/menu-icon.png) に移動します。

![Experience Cloud アプリケーションへのアクセス](assets/platform-core-services.png)

## お問い合わせとサポート {#support}

[Experience League](https://experienceleague.adobe.com/?lang=ja#home) のヘルプコンテンツ（ドキュメント、チュートリアル、コース）および個々のアプリケーションの追加リソースなど、ヘッダーの&#x200B;**[!UICONTROL ヘルプセンター]**（![アセット](assets/help-icon.png)）を使用して、ラーニングとヘルプにアクセスします。自由形式のフィードバックを送信して、優先度の高いサポートチケットを作成することもできます。

![お問い合わせとサポート](assets/search-menu.png)

[!UICONTROL ヘルプ]メニューからも、次の項目にアクセスできます。

* **[!UICONTROL サポート]：** サポートチケットを作成するか、Twitter を使用して[!UICONTROL サポート]にお問い合わせください。
* **[!UICONTROL フィードバック]：** Experience Cloud のエクスペリエンスに関するフィードバックをお寄せください。フィードバックは、アドビの製品およびサービスを改善するために使用されます。
* **[!UICONTROL ステータス]：** に移動して、製品の `https://status.adobe.com/experience_cloud` 運用状況と[!UICONTROL サブスクリプションの管理]を確認します。
* **[!UICONTROL Developer Connection]：** `adobe.io` に移動して、開発者向けドキュメントを見つけます。

## ユーザープロファイルの管理

[!UICONTROL プロファイル]メニューで、次の操作を実行できます。

* ダークテーマを指定する（このテーマに対応していないアプリケーションもあります）
* Experience Cloud の[環境設定](features/account-preferences.md)を管理する
* [組織](administration/organizations.md)を選択または検索する
* [!UICONTROL 法律上の注意]を表示する
* ログアウト
* アカウントの環境設定、通知、サブスクリプションを設定する

## 製品内通知とお知らせの表示 {#notifications}

ベルアイコンをクリックすると、通知とお知らせが表示されます。お知らせには、製品リリース、メンテナンス通知、共有項目、承認リクエストなど、関連性の高い実用的な更新が含まれる場合があります。

![通知とお知らせ](assets/notifications-menu-small.png)

通知とアラートを管理するには、[アカウントの環境設定と通知](features/account-preferences.md)を参照してください


## 最新情報

Experience Cloud中央インターフェイスコンポーネントに対する最新の機能強化について説明します。

>[!BEGINTABS]

>[!TAB Experience CloudとのSlackの統合 ]

アカウントの環境設定を行い、[!DNL Slack] チャンネルにExperience Cloud通知を送信できます。

[!BADGE Beta]{type=Informative url="https://experienceleague.adobe.com/en/docs/core-services/interface/features/account-preferences#notifications" tooltip="Slackについて学ぶ"}


>[!TAB 新しい Campaign web ユーザーインターフェイス]

新しい Adobe Campaign ユーザーインターフェイスを体験しましょう。より現代的、直感的、動的です。

[![画像](assets/do-not-localize/learn-more-button.svg)](start/campaign-ui.md#ac-web-ui)


>[!TAB プッシュチャネルの今後の変更]

2024 年に Android Firebase Cloud Messaging（FCM）サービスに対するいくつかの重要な変更は、リリースする予定です。このリリースは、Adobe Campaign の実装に影響を与える場合があります。この変更をサポートするには、Android プッシュメッセージの購読サービス設定を更新する必要がある場合があります。今すぐ確認し、アクションを実行できます。

[![画像](assets/do-not-localize/learn-more-button.svg)](../technotes/upgrades/push-technote.md)



>[!ENDTABS]

## 基本について学ぶ

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
    <a href="start/whats-new.md"><img src="assets/do-not-localize/start-capabilities.png"></a>
    <div><strong>主な機能</strong><br/>：クロスチャネルキャンペーン管理のための Adobe Campaign v8 の主な機能について説明します。</div>
    </td>
    <td>
    <a href="start/connect.md"><img src="assets/do-not-localize/start-connect.jpeg"></a>
    <div><strong>Campaign v8 への接続</strong><br/>：Adobe Campaign v8 に接続し、クライアントコンソールをインストールおよび設定し、キャンペーン管理ジャーニーを開始する方法について説明します。</div><br/>
    </td>
    <td>
    <a href="start/create-message.md"><img src="assets/do-not-localize/start-send.jpeg"></a>
    <div><strong>メッセージの送信</strong><br/>：メール、SMS、プッシュ通知など、さまざまなチャネルでメッセージを送信する方法について説明します。
    </div></td>
    <td>
    <a href="audiences/create-profiles.md"><img src="assets/do-not-localize/start-profiles.png"></a>
    <div><strong>プロファイルのインポート</strong><br/>：Adobe Campaign v8 データベースでの簡単なプロファイル作成について説明します。手動またはインポートによるプロファイルの追加、顧客データの絞り込み、キャンペーンのカスタマイズを簡単に行うことができます。</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="start/whats-new.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="start/connect.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="start/create-message.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="audiences/create-profiles.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    </tr>
</table>

## ドキュメントの参照

<table style="table-layout:auto">
  <tr style="border: 0;">
    <td>
      <img src="assets/do-not-localize/icon-start.svg" width="35px">
    <br/>
      <strong>基本を学ぶ</strong><br/><a href="start/campaign-ui.md">ユーザーインターフェイス</a> - <a href="start/ac-components.md">コンポーネントとプロセス</a> - <a href="start/v7-to-v8.md">Classic v7 から v8 へ</a> - <a href="start/campaign-faq.md">FAQ</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-experience.svg" width="35px">
    <br/>
      <strong>顧客のエクスペリエンス</strong><br/><a href="../automation/workflow/about-workflows.md" target="_blank">ワークフローを使用した自動化</a> - <a href="../automation/campaigns/set-up-campaigns.md" target="_blank">キャンペーンオーケストレーション</a> - <a href="interaction/interaction.md">意思決定管理</a> - <a href="send/personalize.md">パーソナライゼーション</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-send.svg" width="35px">
    <br/>
      <strong>メッセージを送信</strong><br/><a href="start/create-message.md">基本を学ぶ</a> - <a href="send/preview-and-proof.md">プレビューと配達確認</a> - <a href="send/predictive.md">送信時間の最適化</a> - <a href="reporting/gs-reporting.md">レポーティングと分析</a>
    </td>
  </tr>
  <tr style="border: 0;">
    <td>
      <img src="assets/do-not-localize/icon_profile-audience.svg" width="35px">
    <br/>
      <strong>プロファイルとオーディエンス</strong><br/><a href="audiences/create-profiles.md">プロファイルを追加</a> - <a href="audiences/create-audiences.md">オーディエンスを作成</a> - <a href="start/subscriptions.md">購読の管理</a> - <a href="start/privacy.md">プライバシー</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-configure.svg" width="35px">
    <br/>
      <strong>アーキテクチャと設定</strong><br/><a href="architecture/architecture.md">アーキテクチャ</a> - <a href="start/implement.md">Campaign v8 の実装</a> - <a href="connect/integration.md">他のソリューションとの接続</a> - <a href="start/gs-permissions.md">ユーザーと権限</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-dev.svg" width="35px">
    <br/>
      <strong>開発者リソース</strong><br/><a href="dev/datamodel.md">Campaign v8 データモデル</a> - <a href="dev/schemas.md">スキーマ</a> - <a href="dev/api.md">API</a>
    </td>
  </tr>
</table>

## その他のリソース

[Adobe Campaign v8 の製品説明](https://helpx.adobe.com/jp/legal/product-descriptions/adobe-campaign-managed-cloud-services.html){target="_blank"} - [Adobe Campaign web ユーザーインターフェイスドキュメント](https://experienceleague.adobe.com/docs/campaign-web/v8/campaign-web-home.html?lang=ja){target="_blank"} - [チュートリアル](https://experienceleague.adobe.com/docs/campaign-learn/tutorials/overview.html?lang=ja){target="_blank"} - [[!DNL Adobe Campaign] 自動化ガイド](https://experienceleague.adobe.com/docs/campaign/automation/home.html?lang=ja){target="_blank"} - [Campaign v8 のコントロールパネル](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/key-features.html?lang=ja){target="_blank"}

