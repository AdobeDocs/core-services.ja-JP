---
description: 組織の概要と、ソリューションアカウントの Experience Cloud へのリンクについて説明します。
keywords: Adobe Experience Cloud サービス
solution: Experience Cloud
title: '組織とアカウントのリンク '
uuid: ae47ad18-ac33-4efa-8b68-2bfaf77397aa
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 6eb58530-2a7a-48c7-9a5b-48a6e980a034
source-git-commit: ec724555c3799eeca350592498267d0b71b4ff04
workflow-type: ht
source-wordcount: '506'
ht-degree: 100%

---

# Experience Cloud の組織

Experience Cloud での組織の管理と切り替えについて説明します。

## 組織を特定する {#concept_384D169B0B724B799D573B8ECB5C39BF}

*組織は*、管理者がグループおよびユーザーの設定や、Experience Cloud でのシングルサインオンの制御をおこなえるエンティティです。組織は、すべての Experience Cloud 製品およびソリューションをまたいだログイン会社のように機能します。ほとんどの場合、組織は勤務先の会社名です。ただし、1 つの会社が多くの組織を持つことができます。

正しい組織にログインしたことを確認するには、プロファイルのアバターをクリックして組織名を表示します。複数の組織にアクセスできる場合は、ヘッダーバーで別の組織を表示して切り替えることもできます。

組織が Federated ID を使用している場合、Experience Cloud を使用すると、メールアドレスとパスワードを入力しなくても、組織のシングルサインオンでログインできます。 これをおこなうには、Experience Cloud の URL（`https://experience.adobe.com`）に `#/sso:@domain` を追加します。

例えば、Federated ID を持ち、ドメインが `adobecustomer.com` の組織の場合、URL リンクを `https://experience.adobe.com/#/sso:@adobecustomer.com` に設定します。また、この URL にアプリケーションパスを付けてブックマークに追加することで、特定のアプリケーションに直接移動することもできます。 （例えば、Adobe Analytics の場合は `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。）

![手順の結果](assets/organization-switch.png)

## 組織 ID を見つける {#concept_EA8AEE5B02CF46ACBDAD6A8508646255}

サポートを受けるために組織 ID が必要になる場合があります。**[!UICONTROL 組織]** メニューを使用して、自分が正しい組織に属していることを確認したり、組織を切り替えたりできます。

**組織 ID：**&#x200B;プロビジョニングされた Experience Cloud の会社に関連付けられた ID。この ID は 24 文字の英数字から成る文字列で、その後に @AdobeOrg（必須）が続きます。

組織 ID を表示するには、Experience Cloud ランディングページに移動するか、（![](assets/menu-icon.png)）を選択してから、「**[!UICONTROL 管理]**」を選択します。組織 ID は、[!UICONTROL Experience Cloud 使用の手引き]ページまたは[!UICONTROL 管理]ページの下部にあります。

![](assets/administration-page.png)

## ソリューションアカウントを Adobe ID にリンクする {#task_FD389E78640848919E247AC5E95B8369}

通常は、Experience Cloud 管理者がソリューションやサービスへのアクセス権を付与します。まれに、ソリューションの資格情報を Adobe ID にリンクすることが必要になる場合があります。

1. Experience Cloud への招待メールに記載されている手順に従います。
1. Adobe ID または Enterprise ID を使用してログインします。
1. ソリューションセレクター（![](assets/menu-icon.png)）を選択します。

   ![](assets/solutions-active.png)

   アクセスできるソリューションはカラー表示されます。
1. 目的のソリューションを選択します。

   ![](assets/analytics-link-accounts.png)

   このタイプのメッセージは、ユーザーが適切なグループに属している（かつソリューションに対する権限を持っている）ものの、そのアカウントの資格情報をまだ Adobe ID にリンクしていない場合に表示されます。
1. 「**[!UICONTROL アカウントにリンク]**」を選択し、認証情報を設定します。

## デフォルトの組織とランディングページを指定する {#concept_6A191B42A9874A9780882903BA18F071}

ログイン時に使用するデフォルトの組織およびランディングページを指定できます。

自分のプロファイルで、「**[!UICONTROL プロファイルを編集]**」を選択します。

![](assets/edit-profile.png)

デフォルトの組織およびランディングページでは、ログインエクスペリエンスをカスタマイズできます。

![](assets/default-organization.png)

## アカウントのリンクに関する問題のトラブルシューティング {#concept_DFCB29A3B4834FC59AA29E0BBA301584}

アカウントのリンクに起因する問題に関するヘルプです。

一般的に、アカウントのリンクは、Adobe ID が以前のユーザーにリンクされていることが原因で失敗します。アカウントのリンクに失敗した場合は、

* [アドビサポートにお問い合わせ](https://experienceleague.adobe.com/?support-solution=General&amp;lang=ja#support)ください。
* 問題の解決前でも、標準ログインを使用してソリューションにアクセスできます。
