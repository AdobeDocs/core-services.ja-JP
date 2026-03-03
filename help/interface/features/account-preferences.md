---
title: アカウントの環境設定と通知
description: Experience Cloud のユーザープロファイル、アカウントの環境設定、製品使用状況データについて説明します。メールおよび  [!DNL Slack] の製品通知を購読し、製品アラートを設定します。
solution: Experience Cloud
feature: Account Preferences, Notifications, Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 1e34c6b2-a792-41c4-adb7-583de596237f
TQID: https://experienceleague.adobe.com/2IL6hUlA1oNxJIFMwbVQUbxEGkJoghVUTyMi5wSRBsE
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: e1eba07e-ab89-466f-9ab5-ceb891d7a67did: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: bdea9bc8-5600-45db-b85e-d74bb59dfcffid: dc42f745-24d2-44a4-99c3-dece518fa4bcid: eaef3029-0844-43fe-9e1c-7666a24f4d03id: eb1ae5c4-ef16-4998-851c-73cc9f0b7f06id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ce4fa63a4babc195f89c595009adcf19f34cdd9
workflow-type: tm+mt
source-wordcount: 788
ht-degree: 6%

---

# アカウントの環境設定と通知

Experience Cloudの環境設定を見つけるには、ヘッダーの **[!UICONTROL Profile]**![ 環境設定 ](../assets/preferences-icon-sm.png)」をクリックし、「**[!UICONTROL Preferences]**」をクリックします。

![ 環境設定 ](../assets/preferences-navigation.png){width="100" zoomable="yes"}

[!UICONTROL Experience Cloud preferences] ページでは、次のアカウント機能を管理できます。

| 機能 | 説明 |
| --- | --- |
| [!UICONTROL Profile] | [Adobe アカウントプロファイル ](https://account.adobe.com/profile) を更新します。 <p>プロファイルの写真と名前は、Adobe.comやAdobeの製品とサービスにログインしたときに表示されます。また、[!DNL Behance] のような公開サイトにも表示されます。 |
| [!UICONTROL General] | [ 組織 ](../administration/organizations.md) を選択します。<p>この組織は、Experience Cloudにログインする際に使用されるデフォルトの組織です。 |
| [!UICONTROL Product usage data] | Experience Cloud アプリケーションを使用するときに、Adobeで共有される製品の使用状況データを制御できます。 これは、お客様の組織のコンテンツやデータそのものではなく、お客様の製品の使用方法に関するデータです。 Adobeでは、この情報を使用して、商品の品質向上、強化された製品内サポートの提供、お客様のアドビからのエクスペリエンスやお知らせのパーソナライズを行います。 <p>詳しくは、[ 製品の使用状況データ ](#product-usage-data) （このページ）を参照してください。 |
| [!UICONTROL Notifications] | 製品 [ 通知 ](#subscribe-to-notifications-in-experience-cloud) およびアラートを希望する方法とタイミングを設定します。 <ul><li>アラートを登録する製品を選択します</li><li>通知のタイプ （[!UICONTROL in-app]、[!UICONTROL email] または [Slack](#slack-notifications)）を設定</li><li>通知メールの受信頻度を指定します。（送信しない、即時、毎日または毎週）</li><li>アラートの優先度を決定します。 アプリ内アラートは、ウィンドウの右上隅に数秒間表示されます。 または、解除するまでアラートを表示するかどうかを指定できます。</li></ul> |

## [!UICONTROL Product usage data]

Adobeと共有する製品の使用状況データには、Adobe アプリケーションの使用方法と操作方法に関する次の種類の情報が含まれます。

* ブラウザーおよびデバイス情報（デバイスモデルおよびオペレーティングシステム、ソフトウェアおよびハードウェア情報、ブラウザーおよびデバイスの設定、一意の識別子（IP アドレス、cookie ID、デバイス ID など）、インストールされたメモリの量、言語設定、画面の解像度など）
* 使用する機能や選択するオプションなど、Adobe Experience Cloud アプリとのやり取り。
* Adobe商品情報（バージョン番号など）
* ページ数と一意の ID など、コンテンツとドキュメントに関する情報（コンテンツ自体に関する情報ではありません）。
* コンテンツの使用状況情報（コンテンツへのアクセス回数、アプリ内のコンテンツの操作方法など）。
* クラッシュ ログとエラーログ。

Adobeは、この情報を商品の品質向上、製品内およびカスタマーケア経由の両方でのサポートの提供、お客様の体験やお客様からのお知らせのパーソナライズに活用します。 詳しくは、[ パーソナライズされたエクスペリエンス ](personalized-learning.md) を参照してください。

## Experience Cloudの通知の購読

購読する製品とカテゴリを選択できます。 通知は、[!UICONTROL Notifications] ポップオーバー（アプリ内）、メールまたは [Slack](#slack-notifications) （購読に応じて）に表示されます。

メール通知とSlack通知は、Experience Cloudにログインしていない場合に役立ちます。

### アプリ内通知およびメール通知のサブスクライブ

1. Experience Cloud[ 環境設定 ](https://experience.adobe.com/preferences) に移動します。

1. 「**[!UICONTROL Notifications]**」で、「**[!UICONTROL In-app]**」または「**[!UICONTROL Email]**」を有効にします。

   通知に対する変更は自動的に保存されます。

### [!DNL Slack] 通知のサブスクライブ

アカウントの環境設定を行い、Experience Cloud通知を [!DNL Slack] チャンネルに送信できます。

**前提条件**

* Experience Cloud アカウントが必要です。
* [!DNL Slack] アカウントが必要です。 [!DNL Slack] 管理者は、Experience Cloudと [!DNL Slack] の統合を有効にします。
* 少なくとも 1 つの [!DNL Slack] ワークスペースに属している必要があります。

**[!DNL Slack] 通知の配信登録**

1. Experience Cloud[ 環境設定 ](https://experience.adobe.com/preferences) に移動します。

1. [!DNL Slack] を見つけ、「**[!UICONTROL Add to Slack]**」をクリックします。

   ![Slackに追加 ](../assets/add-to-slack.png)

   [!DNL Slack] がインストールされている場合は、アプリケーションが開き、権限要求メッセージが表示されます。 Slackがインストールされていない場合は、[ 権限をリクエスト ](#slack-troubleshoot) する必要があります。

1. 「**[!UICONTROL Allow]**」をクリックします。

1. **[!UICONTROL Notifications]** の下で、目的の製品およびカテゴリの [!DNL Slack] 通知を有効にします。

   ![Slackの通知 ](../assets/slack.png)

   通知に対する更新は自動的に保存されます。

### [!DNL Slack] でのリクエスト権限（トラブルシューティング）

[!DNL Slack] がインストールされていない場合、「_[!UICONTROL Request to install]_」をクリックした後にSlackを開くと、**[!UICONTROL Add to Slack]**のメッセージが表示されます。 例：

![Slack統合のリクエスト ](../assets/slack-workspace.png)

**Slackで権限をリクエストするには**

1. [!DNL Slack] の場合、ワークス **[!UICONTROL Workspace]** ーメニュー（右上隅）からワークスペースを選択します。

1. [!DNL Slack] Workspace Manager のアプリケーションの承認をリクエストするには、「**[!UICONTROL Submit]**」をクリックします。

1. 申請リクエストが承認されると、[!DNL Slack] に通知が届きます。

1. 承認 [!DNL Slack] 受け取ったら、Experience Cloud **[!UICONTROL Notifications]** に戻り、手順に従って [Slackに登録 ](#slack-notifications) します（上記）。

### [!DNL Slack] に表示される内容

[!DNL Slack] の統合が成功すると、[!DNL Slack] の通知に次の情報が表示されます。

* 個人用メッセージはアプリケーション名 _Adobe[!DNL Experience Cloud]_ から受信されます。
* メッセージには、Adobe [!DNL Experience Platform]、Adobe [!DNL Experience Manager] など、特定のアプリケーションの製品ロゴが含まれます。
* Experience Cloudのすべての通知を表示するためのリンクです。
* Experience Cloudの通知環境設定を管理するためのリンクです。

## Experience Cloudで [!UICONTROL notifications] ファーとお知らせを表示する

[!DNL Experience Cloud] ヘッダーでは、自分が [ 購読 ](#notifications) している通知を表示したり、お知らせを表示したりできます。

1. ヘッダーのベルアイコンをクリックします。 ![通知とお知らせ](../assets/bell-icon.png)

1. 「**[!UICONTROL Notifications]**」または「**[!UICONTROL Announcements]**」をクリックします。

   この場所では、製品、他のユーザーとの共同作業、その他の関連する更新に関する重要な情報を受け取ることができます。 アップデートには、製品リリース、メンテナンス通知、共有項目、承認リクエストが含まれます。

