---
title: アカウントの環境設定と通知
description: Experience Cloud のユーザープロファイル、アカウントの環境設定、製品使用状況データについて説明します。メールおよび  [!DNL Slack] の製品通知を購読し、製品アラートを設定します。
solution: Experience Cloud
feature: Account Preferences, Notifications, Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 1e34c6b2-a792-41c4-adb7-583de596237f
source-git-commit: eddbda54bc3f1cbbc98d7a993d0b477e05c5b01c
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 5%

---

# アカウントの環境設定と通知 {#preferences}

Experience Cloudの環境設定を見つけるには、ヘッダーの **[!UICONTROL プロファイル]** ![ 環境設定 ](../assets/preferences-icon-sm.png) をクリックし、**[!UICONTROL 環境設定]** をクリックします。

![ 環境設定 ](../assets/preferences-navigation.png){width="100" zoomable="yes"}

[!UICONTROL Experience Cloud環境設定 &#x200B;] ページでは、次のアカウント機能を管理できます。

| 機能 | 説明 |
|--- |--- |
| [!UICONTROL プロファイル] | [Adobeアカウントプロファイル ](https://account.adobe.com/profile) を更新します。 <p>プロファイルの写真と名前は、Adobe.comやAdobeの製品およびサービスにログインしたときに表示されます。また、[!DNL Behance] のような公開サイトにも表示されます。 |
| [!UICONTROL &#x200B; 一般 &#x200B;] | [ 組織 ](../administration/organizations.md) を選択します。<p>Experience Cloudにログインした際に使用されるデフォルトの組織です。 |
| [!UICONTROL &#x200B; 製品の使用状況データ &#x200B;] | Experience Cloudアプリケーションを使用する際に、Adobeと共有する製品使用状況データを制御できます。 これは、お客様の組織のコンテンツやデータそのものではなく、お客様の製品の使用方法に関するデータです。 Adobeでは、この情報を使用して、商品の品質向上、強化された製品内サポートの提供、お客様のエクスペリエンスとアドビからのお知らせのパーソナライズを行います。 <p>詳しくは、[ 製品の使用状況データ ](#product-usage-data) （このページ）を参照してください。 |
| [!UICONTROL &#x200B; 通知 &#x200B;] | 製品 [ 通知 ](#subscribe-to-notifications-in-experience-cloud) およびアラートを希望する方法とタイミングを設定します。 <ul><li>アラートを登録する製品を選択します</li><li>通知のタイプ （[!UICONTROL &#x200B; アプリ内 &#x200B;]、[!UICONTROL &#x200B; メール &#x200B;] または [Slack](#slack-notifications)）を設定</li><li>通知メールの受信頻度を指定します。（送信しない、即時、毎日または毎週）</li><li>アラートの優先度を決定します。 アプリ内アラートは、ウィンドウの右上隅に数秒間表示されます。 または、解除するまでアラートを表示するかどうかを指定できます。</li></ul> |

## [!UICONTROL &#x200B; 製品の使用状況データ &#x200B;] {#product-usage-data}

Adobeと共有する製品の使用状況データには、Adobeアプリケーションの使用方法と操作方法に関する次の種類の情報が含まれます。

* ブラウザーおよびデバイス情報（デバイスモデルおよびオペレーティングシステム、ソフトウェアおよびハードウェア情報、ブラウザーおよびデバイスの設定、一意の識別子（IP アドレス、cookie ID、デバイス ID など）、インストールされたメモリの量、言語設定、画面の解像度など）
* 使用する機能や選択するオプションなど、Adobe Experience Cloud アプリとのやり取り。
* Adobe商品情報（バージョン番号など）
* ページ数と一意の ID など、コンテンツとドキュメントに関する情報（コンテンツ自体に関する情報ではありません）。
* コンテンツの使用状況情報（コンテンツへのアクセス回数、アプリ内のコンテンツの操作方法など）。
* クラッシュ ログとエラーログ。

Adobeは、この情報を使用して、商品の改善、製品内およびカスタマーケアによるサポートの提供、お客様のエクスペリエンスとアドビからのお知らせのパーソナライズを行います。 詳しくは、[ パーソナライズされたエクスペリエンス ](personalized-learning.md) を参照してください。

## Experience Cloudでの通知のサブスクライブ {#notifications}

購読する製品とカテゴリを選択できます。 通知は、（購読に応じて） [!UICONTROL &#x200B; 通知 &#x200B;] ポップオーバー（アプリ内）、メールまたは [Slack](#slack-notifications) に表示されます。

メール通知とSlack通知は、Experience Cloudにログインしていない場合に役立ちます。

### アプリ内通知およびメール通知のサブスクライブ

1. Experience Cloud[ 環境設定 ](https://experience.adobe.com/preferences) に移動します。

1. 「**[!UICONTROL 通知]**」で、「**[!UICONTROL アプリ内]**」または「**[!UICONTROL メール]**」を有効にします。

   通知に対する変更は自動的に保存されます。

### [!DNL Slack] 通知のサブスクライブ {#slack}

アカウントの環境設定を行い、[!DNL Slack] チャンネルにExperience Cloud通知を送信できます。

**前提条件**

* Experience Cloudアカウントが必要です。
* [!DNL Slack] アカウントが必要です。 [!DNL Slack] 管理者は、[!DNL Slack] とのExperience Cloud統合を有効にします。
* 少なくとも 1 つの [!DNL Slack] ワークスペースに属している必要があります。

**[!DNL Slack] 通知の配信登録**

1. Experience Cloud[ 環境設定 ](https://experience.adobe.com/preferences) に移動します。

1. [!DNL Slack] を見つけ、「**[!UICONTROL Slackに追加]**」をクリックします。

   ![Slackに追加 ](../assets/add-to-slack.png)

   [!DNL Slack] がインストールされている場合は、アプリケーションが開き、権限要求メッセージが表示されます。 Slackがインストールされていない場合は、[ 権限をリクエスト ](#slack-troubleshoot) する必要があります。

1. **[!UICONTROL 許可]** をクリックします。

1. **[!UICONTROL 通知]** で、目的の製品 [!DNL Slack] カテゴリの通知を有効にします。

   ![Slackの通知 ](../assets/slack.png)

   通知に対する更新は自動的に保存されます。

### [!DNL Slack] でのリクエスト権限（トラブルシューティング） {#slack-troubleshoot}

[!DNL Slack] がインストールされていない場合、「_[!UICONTROL Slackに追加&#x200B;]&#x200B;**」をクリックした後にSlackが開くと、**&#x200B;[!UICONTROL インストールをリクエスト]_ メッセージが表示されます。 例：

![ リクエストSlackの統合 ](../assets/slack-workspace.png)

**Slackで権限をリクエストするには**

1. [!DNL Slack] で、**[!UICONTROL Workspace]** メニュー（右上隅）からワークスペースを選択します。

1. [!DNL Slack] Workspace Manager のアプリケーションの承認をリクエストするには、「**[!UICONTROL 送信]**」をクリックします。

1. 申請リクエストが承認されると、[!DNL Slack] に通知が届きます。

1. 承認 [!DNL Slack] 受け取ったら、Experience Cloud **[!UICONTROL 通知]** に戻り、手順に従って [Slackを購読 ](#slack-notifications) します（上記）。

### [!DNL Slack] に表示される内容

[!DNL Slack] の統合が成功すると、[!DNL Slack] の通知に次の情報が表示されます。

* 個人用メッセージはアプリケーション名 _のAdobe[!DNL Experience Cloud]_ から受信されます。
* メッセージには、Adobe[!DNL Experience Platform]、Adobe[!DNL Experience Manager] など、特定のアプリケーションの製品ロゴが含まれます。
* Experience Cloud時のすべての通知を表示するためのリンク。
* Experience Cloudの通知設定を管理するためのリンクです。

## Experience Cloudで [!UICONTROL &#x200B; 通知 &#x200B;] とお知らせを表示する {#view-notifications}

[!DNL Experience Cloud] ヘッダーでは、自分が [ 購読 ](#notifications) している通知を表示したり、お知らせを表示したりできます。

1. ヘッダーのベルアイコンをクリックします。 ![通知とお知らせ](../assets/bell-icon.png)

1. **[!UICONTROL 通知]** または **[!UICONTROL お知らせ]** をクリックします。

   この場所では、製品、他のユーザーとの共同作業、その他の関連する更新に関する重要な情報を受け取ることができます。 アップデートには、製品リリース、メンテナンス通知、共有項目、承認リクエストが含まれます。
