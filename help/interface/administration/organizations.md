---
description: 組織（IMS組織ID）、アカウントの切り替え、ソリューション アカウントのリンクについて説明します。
solution: Experience Cloud
title: 組織とアカウント
uuid: ae47ad18-ac33-4efa-8b68-2bfaf77397aa
feature: Organizations
topic: Administration
role: Admin
level: Experienced
exl-id: 6eb58530-2a7a-48c7-9a5b-48a6e980a034
TQID: https://experienceleague.adobe.com/DCb0MQWwB0MOGALSDbLD-d4ik4B0C249xncB9eZbZMU
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: bdea9bc8-5600-45db-b85e-d74bb59dfcff
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 9c2010694b8bb32c3922dd65f846375e43b2caac
workflow-type: tm+mt
source-wordcount: 506
ht-degree: 17%

---

# 組織とアカウント

*組織* （組織ID）は、管理者がグループとユーザーを設定し、CX Enterpriseでのシングルサインオンを制御できるようにするエンティティです。

CXMは、あらゆるCX エンタープライズ製品とアプリケーションに対応するログイン企業のような役割を果たします。 ほとんどの場合、組織は勤務先の会社名です。 ただし、1 つの会社が多くの組織を持つことができます。

**組織メニュー**

![CX エンタープライズ組織](../assets/organizations-menu.png)

正しい組織にログインしていることを確認するには、**[!UICONTROL プロファイル]**&#x200B;をクリックして、デフォルトの組織名を表示します。 複数の組織にアクセスできる場合は、ヘッダーバーで別の組織を表示して切り替えることもできます。

>[!NOTE]
>
>組織を切り替えると、その組織のAdmin Consoleにアクセスできます。 目的の組織が表示されない場合は、その組織の管理者にアクセス権をリクエストする必要がある場合があります。 （複数のAdmin Consoleを統合する必要がある場合は、Adobe カスタマーサポートにお問い合わせください）。

## Federated ID

組織でFederated IDを使用している場合は、電子メールアドレスとパスワードを入力しなくても、組織のシングルサインオンでログインできます。 CX エンタープライズ URL （`https://experience.adobe.com`）に`#/sso:@domain`を追加して、このタスクを実行します。

例えば、Federated ID を持ち、ドメインが `example.com` の組織の場合、URL リンクを `https://experience.adobe.com/#/sso:@example.com` に設定します。 また、この URL にアプリケーションパスを付けてブックマークに追加することで、特定のアプリケーションに直接移動することもできます。 （例えば、Adobe Analytics の場合は `https://experience.adobe.com/#/sso:@example.com/analytics`。）

## フェデレーションゲストアカウント

[&#x200B; フェデレーションゲストアクセス &#x200B;](https://helpx.adobe.com/business/enterprise/using/federated-guest-access.html)を有効にして、自分のドメインでゲストユーザーを安全に認証できます。 有効にすると、組織メニューが変更され、これらのユーザーが任意のCX Enterprise ページの既存の組織内のアカウントを切り替えられるようになります。

フェデレーションゲストアカウントに切り替えるには、任意の[CX Enterprise](https://experience.adobe.com) ページの&#x200B;**[!UICONTROL 組織]** メニューで&#x200B;**[!UICONTROL その他のアカウント]**&#x200B;を見つけます。

**フェデレーションゲストアカウントの組織メニュー**

![&#x200B; フェデレーテッドアカウントスイッチャー](../assets/federated-account-switcher.png)

## 組織IDの表示

割り当てられた組織IDは、サポート目的で見つけることができます。 ヘッダーの&#x200B;**[!UICONTROL 組織]** セレクターを使用して、正しい組織に属していることを確認するか、組織間で切り替えることができます。

組織IDは、プロビジョニングされたCX Enterprise会社に関連付けられたIDです。 この ID は 24 文字の英数字から成る文字列の後に `@AdobeOrg`（必須）を付けたものです。

`https://experience.adobe.com`の任意のページのキーボードショートカット **Ctrl+i**&#x200B;を使用して、組織IDやその他のアカウント情報を表示できます。

**組織IDを表示するには**

1. [CX Enterprise](https://experience.adobe.com)で、キーボードの&#x200B;**Ctrl+i**&#x200B;を押します。

   ![割り当てられた組織 ID](../assets/assigned-organization.png)

1. **[!UICONTROL ユーザー情報]**&#x200B;で、**[!UICONTROL 現在の組織ID]**&#x200B;を探し、組織IDを見つけることができます。

   または、管理者はAdmin Consoleにログインし（[https://adminconsole.adobe.com](https://adminconsole.adobe.com)に移動）、URLで組織IDを確認できます。

   例として、次の URL を見てみましょう。

   `https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

   ID は次のとおりです。

   `C538193582390300A495CC9@AdobeOrg`

## 既定の組織を指定

ログイン時に使用するデフォルトの組織を指定できます。

1. ヘッダーで「**[!UICONTROL プロファイル]**」をクリックし、「環境設定」をクリックします。

1. [!UICONTROL General]で、既定の組織を選択します。


![プロファイルを編集](../assets/edit-profile.png)
