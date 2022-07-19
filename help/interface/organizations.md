---
description: 組織（IMS 組織 ID）の概要と、ソリューションアカウントの Experience Cloud へのリンクについて説明します。
keywords: Adobe Experience Cloud サービス
solution: Experience Cloud
title: '組織とアカウントのリンク '
uuid: ae47ad18-ac33-4efa-8b68-2bfaf77397aa
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 6eb58530-2a7a-48c7-9a5b-48a6e980a034
source-git-commit: 00a6aa791dd08c2907cd09c17b7e2a1e62b060c1
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 72%

---

# Experience Cloud の組織

Experience Cloud での組織の管理と切り替えについて説明します。

## 組織を特定する {#concept_384D169B0B724B799D573B8ECB5C39BF}

An *組織* (Org ID) は、管理者がグループおよびユーザーの設定や、Experience Cloudでのシングルサインオンの制御をおこなえるエンティティです。 この組織は、Experience Cloud のすべての製品とアプリケーションにまたがるログイン会社のように機能します。ほとんどの場合、組織は勤務先の会社名です。ただし、1 つの会社が多くの組織を持つことができます。

正しい組織にログインしたことを確認するには、プロファイルのアバターをクリックして組織名を表示します。複数の組織にアクセスできる場合は、ヘッダーバーで別の組織を表示して切り替えることもできます。

組織が Federated ID を使用している場合、Federated ID を使用すると、電子メールアドレスやパスワードを入力する必要なく、組織のシングルサインオンでExperience Cloudすることができます。 追加 `#/sso:@domain` をExperience CloudURL (`https://experience.adobe.com`) をクリックして、このタスクを実行します。

例えば、Federated ID を持ち、ドメインが `adobecustomer.com` の組織の場合、URL リンクを `https://experience.adobe.com/#/sso:@adobecustomer.com` に設定します。 また、この URL にアプリケーションパスを付けてブックマークに追加することで、特定のアプリケーションに直接移動することもできます。 （例えば、Adobe Analytics の場合は `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。）

![手順の結果](assets/organization-switch.png)

## 組織 ID を表示する {#concept_EA8AEE5B02CF46ACBDAD6A8508646255}

割り当てられた組織 ID は、サポートのために見つけることができます。 **[!UICONTROL 組織]** メニューを使用して、自分が正しい組織に属していることを確認したり、組織を切り替えたりできます。

組織 ID は、プロビジョニングされている Experience Cloud の会社に関連付けられた ID です。この ID は 24 文字の英数字から成る文字列の後に `@AdobeOrg`（必須）を付けたものです。

キーボードショートカットを使用して、組織 ID を他のアカウント情報と共に表示できます **Ctrl + i** 任意のページから `https://experience.adobe.com`.

**組織 ID を表示するには、以下を実行します。**

1. In [Experience Cloud](https://experience.adobe.com)を押します。 **Ctrl + i** キーボードで

   ![割り当てられた組織 ID](assets/assigned-organization.png)

1. の下 **[!UICONTROL ユーザー情報]**&#x200B;を探します。 **[!UICONTROL 現在の組織 ID]**&#x200B;組織 ID が表示されます。

   または、管理者がAdmin Console( [https://adminconsole.adobe.com](https://adminconsole.adobe.com)) をクリックし、URL に組織 ID を表示します。

   例として、次の URL を見てみましょう。

   `https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

   ID は次のとおりです。

   `C538193582390300A495CC9@AdobeOrg`

## アプリケーションアカウントを Adobe ID にリンクする {#task_FD389E78640848919E247AC5E95B8369}

通常は、Experience Cloud 管理者がアプリケーションやサービスへのアクセス権を付与します。まれに、アプリケーションの資格情報をAdobe IDにリンクすることがあります。

1. Experience Cloud への招待メールに記載されている手順に従います。
1. Adobe ID または Enterprise ID を使用してログインします。
1. アプリケーションセレクター（![](assets/menu-icon.png)）を選択します。

   ![アプリケーションアカウントを Adobe ID にリンクする](assets/solutions-active.png)

   アクセスできるアプリケーションはカラー表示されます。
1. 目的のアプリケーションを選択します。

   ![目的のアプリケーションを選択](assets/analytics-link-accounts.png)

   このタイプのメッセージは、ユーザーが適切なグループに属している（かつアプリケーションに対する権限を持っている）が、そのアカウントの資格情報をまだ Adobe ID にリンクしていない場合に表示されます。
1. 「**[!UICONTROL アカウントにリンク]**」を選択し、認証情報を設定します。

## デフォルトの組織とランディングページを指定する {#concept_6A191B42A9874A9780882903BA18F071}

ログイン時に使用するデフォルトの組織およびランディングページを指定できます。

自分のプロファイルで、「**[!UICONTROL プロファイルを編集]**」を選択します。

![プロファイルを編集](assets/edit-profile.png)

デフォルトの組織およびランディングページでは、ログインエクスペリエンスをカスタマイズできます。

![デフォルトの組織およびランディングページ](assets/default-organization.png)

## アカウントのリンクに関する問題のトラブルシューティング {#concept_DFCB29A3B4834FC59AA29E0BBA301584}

アカウントのリンクに起因する問題に関するヘルプです。

一般的に、アカウントのリンクは、Adobe ID が以前のユーザーにリンクされていることが原因で失敗します。アカウントのリンクに失敗した場合は、

* [アドビサポートにお問い合わせ](https://experienceleague.adobe.com/?support-solution=General&amp;lang=ja#support)ください。
* 問題が解決するまでの間、標準のログインを使用してアプリケーションにアクセスします。
