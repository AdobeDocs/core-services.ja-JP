---
title: アカウントの環境設定と通知
description: Experience Cloudのユーザープロファイルとアカウントの環境設定について説明します。 製品通知を購読し、製品アラートを取得します。 ブラウザーと言語サポートについて説明します。
solution: Experience Cloud
feature: Account Preferences,Notifications,Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 1e34c6b2-a792-41c4-adb7-583de596237f
source-git-commit: 05ba40e4ef28c6d244446cc862a0320048f4b219
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 69%

---

# アカウントの環境設定と通知 {#preferences}

Experience Cloud の環境設定には、通知、購読、アラートが含まれます。アカウントの環境設定メニューで、次の操作を実行できます。

* ダークテーマを指定する（このテーマに対応していないアプリケーションもあります）
* [組織](../administration/organizations.md)を検索する
* ログアウト
* アカウントの環境設定、通知、サブスクリプションを設定する

環境設定を管理するには、アカウントメニュー ![環境設定](../assets/preferences-icon-sm.png) から「**[!UICONTROL 環境設定]**」を選択します。

![ユーザープロファイルとアカウントの環境設定](../assets/preferences-page.png)

[!UICONTROL Experience Cloud の環境設定]では、次の機能を設定できます。

| 機能 | 説明 |
|--- |--- |
| デフォルトの[組織](../administration/organizations.md) | Experience Cloud の起動時に表示する組織を選択します。 |
| [!UICONTROL 製品データ収集] | アドビ製品の使用方法に関するデータを収集するためにアドビが使用できるテクノロジーを選択します。 |
| [!UICONTROL パーソナライズされたラーニングのレコメンデーションとプロモーション] | Adobeの商品に関する [ パーソナライズされたヘルプ ](personalized-learning.md) を受け取る場所を選択します。 このヘルプは、メール、製品内およびExperience Leagueコミュニティから利用できます。 |
| [!UICONTROL サブスクリプション] | 購入する製品とカテゴリを選択します。[!UICONTROL  通知 ] ポップオーバーおよびメール内の通知。 |
| [!UICONTROL 優先度] | 優先度が高いと見なすカテゴリを選択します。これらのカテゴリには [!UICONTROL  高 ] タグが付き、アラートなどの配信用に設定できます。 |
| [!UICONTROL アラート] | ブラウザーにアラートを表示する通知を選択します。アラートは、ウィンドウの右上隅に数秒間表示されます。 |
| メール | 通知メールの受信頻度を指定します。（送信しない、即時、毎日または毎週） |

## [!UICONTROL  通知 ] 及び [!UICONTROL  お知らせ ] {#notifications}

「**[!UICONTROL 通知]**」を選択すると、製品リリース、メンテナンス通知、共有項目、承認リクエストなど、関連性の高い実用的な更新に関する警告が表示されます。

![通知とお知らせ](../assets/notifications-menu-small.png)

## [!DNL Slack] 通知

リリース：**2024 年 9 月 2 日**

アカウントの環境設定を行い、SlackにExperience Cloud通知を送信できます。

**前提条件**

* Experience Cloudアカウントが必要です
* [!DNL Slack] アカウントが必要です
* 少なくとも 1 つの [!DNL Slack] ワークスペースに属している必要があります

### Slack通知を設定するには

1. Experience Cloud にログインします。

1. アカウントアイコンをクリックしてから、**[!UICONTROL 環境設定]** をクリックします。

1. [!DNL Slack] の下の **[!UICONTROL Slackに追加]** をクリックします。

1. [!DNL Slack] が開いたら、「**[!UICONTROL 許可]**」をクリックします。

1. Experience Cloudの環境設定で、「**[!UICONTROL 通知]**」に移動します。

[Slackの通知](../assets/slack.png)

1. 目的 [!DNL Slack] 製品およびカテゴリの通知を有効にします。

## Experience Cloud でのブラウザーのサポート {#browser}

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

## Experience Cloud での言語サポート {#languages}

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