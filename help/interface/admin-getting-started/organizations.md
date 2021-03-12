---
description: 組織の概要と、ソリューションアカウントの Experience Cloud へのリンクについて説明します。
keywords: Adobe Experience Cloud サービス
solution: Experience Cloud
title: '組織とアカウントのリンク '
uuid: ae47ad18-ac33-4efa-8b68-2bfaf77397aa
feature: Admin Console
topic: 管理
role: 管理者
level: 経験豊富
translation-type: ht
source-git-commit: 61d60273e933c637dfe4400da78257e1c80015b3
workflow-type: ht
source-wordcount: '394'
ht-degree: 100%

---


# 組織とアカウントのリンク

組織管理の概要と、ソリューションアカウントの Experience Cloud へのリンクについて説明します。

## 組織を特定する {#concept_384D169B0B724B799D573B8ECB5C39BF}

*組織は*、管理者がグループおよびユーザーの設定や、Experience Cloud でのシングルサインオンの制御をおこなえるエンティティです。組織は、すべての Experience Cloud 製品およびソリューションをまたいだログイン会社のように機能します。ほとんどの場合、組織は勤務先の会社名です。ただし、1 つの会社が多くの組織を持つことができます。

また、サポートを受けるために組織 ID を特定することが必要になる場合もあります。**[!UICONTROL 組織]**&#x200B;メニューを使用して、自分が正しい組織に属していることを確認したり、組織を切り替えたりできます。

![手順の結果](assets/organization-switch.png)

## 組織 ID を見つける {#concept_EA8AEE5B02CF46ACBDAD6A8508646255}

**組織 ID：**&#x200B;プロビジョニングされた Experience Cloud の会社に関連付けられた ID。この ID は 24 文字の英数字から成る文字列で、その後に @AdobeOrg（必須）が続きます。

組織 ID を表示するには、Experience Cloud ランディングページに移動するか、（![](assets/menu-icon.png)）をクリックしてから、「**[!UICONTROL 管理]**」をクリックします。組織 ID は、[!UICONTROL Experience Cloud 使用の手引き]ページまたは[!UICONTROL 管理]ページの下部にあります。

![](assets/administration-page.png)

## ソリューションアカウントを Adobe ID にリンクする {#task_FD389E78640848919E247AC5E95B8369}

通常は、Experience Cloud 管理者がソリューションやサービスへのアクセス権を付与します。まれに、ソリューションの資格情報を Adobe ID にリンクすることが必要になる場合があります。

1. Experience Cloud への招待メールに記載されている手順に従います。
1. Adobe ID または Enterprise ID を使用してログインします。
1. ソリューションセレクター（![](assets/menu-icon.png)）をクリックします。

   ![](assets/solutions-active.png)

   アクセスできるソリューションはカラー表示されます。
1. 目的のソリューションをクリックします。

   ![](assets/analytics-link-accounts.png)

   このタイプのメッセージは、ユーザーが適切なグループに属している（かつソリューションに対する権限を持っている）ものの、そのアカウントの資格情報をまだ Adobe ID にリンクしていない場合に表示されます。
1. 「**[!UICONTROL アカウントにリンク]**」をクリックし、資格情報を設定します。

## デフォルトの組織とランディングページを指定する {#concept_6A191B42A9874A9780882903BA18F071}

ログイン時に使用するデフォルトの組織およびランディングページを指定できます。

自分のプロファイルで、「**[!UICONTROL プロファイルを編集]**」をクリックします。

![](assets/edit-profile.png)

デフォルトの組織およびランディングページでは、ログインエクスペリエンスをカスタマイズできます。

![](assets/default-organization.png)

## アカウントのリンクに関する問題のトラブルシューティング {#concept_DFCB29A3B4834FC59AA29E0BBA301584}

アカウントのリンクに起因する問題に関するヘルプです。

一般的に、アカウントのリンクは、Adobe ID が以前のユーザーにリンクされていることが原因で失敗します。アカウントのリンクに失敗した場合は、

* [アドビサポートにお問い合わせ](https://helpx.adobe.com/jp/marketing-cloud/contact-support.html)ください。
* 問題の解決前でも、標準ログインを使用してソリューションにアクセスできます。
