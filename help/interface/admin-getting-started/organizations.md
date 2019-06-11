---
description: 組織の概要と、ソリューションアカウントの Experience Cloud へのリンクについて説明します。
keywords: コアサービス
seo-description: 組織の概要と、ソリューションアカウントの Experience Cloud へのリンクについて説明します。
seo-title: 組織とアカウントのリンク
solution: 'Marketing Cloud '
title: 組織とアカウントのリンク
uuid: ae47ad18- ac33-4efa-8b68-2bfaf77397aa
translation-type: tm+mt
source-git-commit: d9618a5e5a9b2cfbd1088acc8e970c0d6b477289

---


# 組織とアカウントのリンク

組織の管理およびソリューションアカウントのExperience Cloudへのリンクについて説明します。

<!-- accounts-experience-cloud.xml -->

## 組織を特定する {#concept_384D169B0B724B799D573B8ECB5C39BF}

*組織*とは、管理者がグループおよびユーザーを設定し、Experience Cloud でのシングルサインオンを制御するために使用するエンティティです。組織は、すべての Experience Cloud 製品およびソリューションをまたいだログイン会社のように機能します。ほとんどの場合、組織は、会社名です。ただし、会社は多数の組織を持つことができます。

また、サポートを受けるために組織 ID を特定することが必要になる場合もあります。**[!UICONTROL 組織]メニューを使用して、自分が正しい組織に属していることを確認したり、組織を切り替えたりできます。**

![Step Result](assets/organization-switch.png)

## 組織 ID を見つける {#concept_EA8AEE5B02CF46ACBDAD6A8508646255}

**組織ID** は、プロビジョニングされたExperience Cloud会社に関連付けられているIDです。この ID は 24 文字の英数字から成る文字列で、その後に @AdobeOrg（必須）が続きます。

組織IDを表示するには、Experience Cloudランディングページに移動するか（ ![](assets/menu-icon.png)）、または（）をクリックして、「管理」をクリック **[!UICONTROL ]** します。組織IDは、&quot;Experience [!UICONTROL Cloudの概要」] ページまたは [!UICONTROL 管理] ページの下部にあります。

![](assets/administration-page.png)

## ソリューションアカウントを Adobe ID にリンクする {#task_FD389E78640848919E247AC5E95B8369}

通常は、Experience Cloud 管理者がソリューションやサービスへのアクセス権を付与します。まれに、ソリューションの資格情報を Adobe ID にリンクすることが必要になる場合があります。

1. Experience Cloud への招待メールに記載されている手順に従います。
1. Adobe ID または Enterprise ID を使用してログインします。
1. ソリューションセレクターをクリックします。（ ![](assets/menu-icon.png)）.

   ![](assets/solutions-active.png)

   アクセスできるソリューションはカラー表示されます。
1. 目的のソリューションをクリックします。

   ![](assets/analytics-link-accounts.png)

   このタイプのメッセージは、ユーザーが適切なグループに属している（かつソリューションに対する権限を持っている）ものの、そのアカウントの資格情報をまだ Adobe ID にリンクしていない場合に表示されます。
1. 「アカウント **[!UICONTROL ]** にリンク」をクリックして、資格情報を入力します。

## デフォルトの組織とランディングページを指定する {#concept_6A191B42A9874A9780882903BA18F071}

ログイン時に使用するデフォルトの組織およびランディングページを指定できます。

プロファイルで、「プロファイル **[!UICONTROL を編集」をクリック]** します。

![](assets/edit-profile.png)

デフォルトの組織およびランディングページでは、ログインエクスペリエンスをカスタマイズできます。

![](assets/default-organization.png)

## アカウントのリンクに関する問題のトラブルシューティング {#concept_DFCB29A3B4834FC59AA29E0BBA301584}

アカウントのリンクに起因する問題に関するヘルプです。

一般的に、アカウントのリンクは、Adobe ID が以前のユーザーにリンクされていることが原因で失敗します。アカウントのリンクに失敗した場合、次のことができます。

* [アドビサポートに問い合わせる](https://helpx.adobe.com/marketing-cloud/contact-support.html)。
* 問題の解決前でも、標準ログインを使用してソリューションにアクセスする。
