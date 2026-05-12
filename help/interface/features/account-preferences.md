---
title: アカウントの環境設定と通知
description: CX Enterpriseのユーザープロファイル、アカウント設定、製品使用データについて説明します。 メールおよび [!DNL Slack]の製品通知を購読し、製品アラートを設定します。
solution: Experience Cloud
feature: Account Preferences, Notifications, Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 1e34c6b2-a792-41c4-adb7-583de596237f
autotag-review: '2026-05-11T17:46:06.275Z'
TQID: 'https://experienceleague.adobe.com/wn3EBV0rf2PLh649pY8KqLjIHjvpGwpBkDxX4Ib03uw'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: e1eba07e-ab89-466f-9ab5-ceb891d7a67did: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id:id:id:id:id:id:
role_v2: id:
level_v2: id:
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f01d85af42b8f2c27dbada8f73546bc6fe4bf710
workflow-type: tm+mt
source-wordcount: 802
ht-degree: 5%

---

# アカウントの環境設定と通知

CX エンタープライズ環境設定を検索するには、ヘッダーの&#x200B;**[!UICONTROL Profile]** ![環境設定](../assets/preferences-icon-sm.png)をクリックし、**[!UICONTROL Preferences]**&#x200B;をクリックします。

![環境設定](../assets/preferences-navigation.png){width="100" zoomable="yes"}

[!UICONTROL CX Enterprise preferences] ページでは、次のアカウント機能を管理できます。

| 機能 | 説明 |
| --- | --- |
| [!UICONTROL Profile] | [Adobe アカウントプロファイル ](https://account.adobe.com/profile)を更新します。 <p>プロフィール写真と名前は、Adobe.com、Adobeの製品とサービス、および[!DNL Behance]などの公開サイトにログインすると表示されます。 |
| [!UICONTROL General] | [組織](../administration/organizations.md)を選択します。<p>この組織は、CX Enterpriseへのログイン時に使用されるデフォルトの組織です。 |
| [!UICONTROL Product usage data] | CX Enterprise アプリケーションを使用する際に、Adobeと共有される製品使用データを制御できます。 これは、組織のコンテンツやデータ自体ではなく、製品の利用方法に関するデータです。 Adobeでは、この情報を利用して、製品の改善、製品サポートの強化、お客様の体験とコミュニケーションのパーソナライズを図ります。 <p>詳しくは、[製品使用状況データ ](#product-usage-data) （このページ）を参照してください。 |
| [!UICONTROL Notifications] | 製品[通知](#subscribe-to-notifications-in-experience-cloud)とアラートを希望する方法とタイミングを設定します。 <ul><li>アラートを購読する製品を選択します</li><li>通知の種類（[!UICONTROL in-app]、[!UICONTROL email]または[Slack](#slack-notifications)）を設定します</li><li>通知メールの受信頻度を指定します。 （送信しない、即時、毎日または毎週）</li><li>アラートの優先順位の決定： アプリ内アラートは、ウィンドウの右上隅に数秒間表示されます。 または、アラートを閉じるまで表示するかどうかを指定できます。</li></ul> |

## [!UICONTROL Product usage data]

Adobeとの間で共有する製品使用状況データには、Adobe アプリケーションの使用と操作に関する次の種類の情報が含まれます。

* デバイスモデルとオペレーティングシステム、ソフトウェアとハードウェア情報、ブラウザーとデバイスの設定、一意の識別子（IP アドレス、Cookie ID、デバイス IDなど）、インストールされたメモリ量、言語設定、画面解像度などのブラウザーとデバイス情報。
* 使用する機能や選択したオプションなど、Adobe CX エンタープライズアプリの利用方法。
* Adobe製品情報（バージョン番号など）
* ページ数や一意のIDなど、コンテンツとドキュメントに関する情報。コンテンツ自体は含まれません。
* コンテンツへのアクセス回数や、アプリ内でのコンテンツの利用方法など、コンテンツの利用情報。
* クラッシュログとエラーログ。

Adobeでは、この情報を当社の製品向上に役立て、製品内およびカスタマーケアを通じてサポートを提供し、お客様の体験とコミュニケーションをパーソナライズするために使用します。 [ パーソナライズされたエクスペリエンス ](personalized-learning.md)の詳細をご覧ください。

## CX Enterpriseの通知の購読

購読したい商品やカテゴリーを選択できます。 通知は、[!UICONTROL Notifications] ポップオーバー（アプリ内）、メール、または[Slack](#slack-notifications)に表示されます（サブスクリプションによって異なります）。

メールおよびSlackの通知は、CX Enterpriseにログインしていない場合に役立ちます。

### アプリ内およびメール通知の購読

1. CX Enterprise [preferences](https://experience.adobe.com/preferences)に移動します。

1. **[!UICONTROL Notifications]**&#x200B;で、**[!UICONTROL In-app]**&#x200B;または&#x200B;**[!UICONTROL Email]**&#x200B;を有効にします。

   通知の変更は自動的に保存されます。

### [!DNL Slack]通知を購読

CX エンタープライズ通知を[!DNL Slack] チャネルに送信するように、アカウント設定を設定できます。

**前提条件**

* CX Enterprise アカウントが必要です。
* [!DNL Slack] アカウントが必要です。 [!DNL Slack]管理者は、[!DNL Slack]とのCX Enterprise統合を有効にします。
* 少なくとも1つの[!DNL Slack] ワークスペースに参加している必要があります。

**通知[!DNL Slack]を購読するには**

1. CX Enterprise [Preferences](https://experience.adobe.com/preferences)に移動します。

1. [!DNL Slack]を探し、**[!UICONTROL Add to Slack]**&#x200B;をクリックします。

   ![Slackに追加](../assets/add-to-slack.png)

   [!DNL Slack]がインストールされている場合、アプリケーションが開き、権限の要求メッセージが表示されます。 Slackがインストールされていない場合は、[権限をリクエスト ](#slack-troubleshoot)する必要があります。

1. 「**[!UICONTROL Allow]**」をクリックします。

1. **[!UICONTROL Notifications]**&#x200B;で、目的の製品とカテゴリに対して[!DNL Slack]通知を有効にします。

   ![Slack通知](../assets/slack.png)

   通知の更新は自動的に保存されます。

### [!DNL Slack]で権限を要求する（トラブルシューティング）

[!DNL Slack]がインストールされていない場合、**[!UICONTROL Add to Slack]**&#x200B;をクリックした後にSlackが開くと、_[!UICONTROL Request to install]_メッセージが表示されます。 例：

![Slack統合をリクエスト ](../assets/slack-workspace.png)

**Slackで権限をリクエストするには**

1. [!DNL Slack]で、**[!UICONTROL Workspace]** メニュー（右上隅）からワークスペースを選択します。

1. [!DNL Slack] ワークスペース マネージャーのアプリケーションの承認を要求するには、**[!UICONTROL Submit]**&#x200B;をクリックします。

1. 申請リクエストが承認されると、[!DNL Slack]に通知が届きます。

1. [!DNL Slack]の承認を受けた後、CX Enterprise **[!UICONTROL Notifications]**&#x200B;に戻り、手順に従って[Slack](#slack-notifications)を購入します（上記）。

### [!DNL Slack]に表示される内容

[!DNL Slack]を正常に統合すると、[!DNL Slack]通知に次の情報が表示されます。

* 個人用メッセージは、アプリケーション名&#x200B;_Adobe[!DNL CX Enterprise]_&#x200B;から受信されます。
* メッセージには、Adobe [!DNL Experience Platform]、Adobe [!DNL Experience Manager]など、特定のアプリケーションの製品ロゴが含まれています。
* CX Enterpriseのすべての通知を表示するリンク。
* CX Enterpriseの通知の環境設定を管理するためのリンク。

## CX Enterpriseでの[!UICONTROL notifications]と通知の表示

[!DNL CX Enterprise] ヘッダーでは、[購読](#notifications)の通知を表示したり、通知を表示したりできます。

1. ヘッダーのベルアイコンをクリックします。 ![通知とお知らせ](../assets/bell-icon.png)

1. 「**[!UICONTROL Notifications]**」または「**[!UICONTROL Announcements]**」をクリックします。

   この場所では、製品、同僚のユーザーとの共同作業、その他の関連する更新に関する重要な情報を受け取ることができます。 アップデートには、製品リリース、メンテナンス通知、共有アイテム、承認リクエストなどが含まれます。

