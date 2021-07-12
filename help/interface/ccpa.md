---
title: 'カリフォルニア州消費者プライバシー法に対する顧客属性のサポート '
description: カリフォルニア州消費者プライバシー法に対する顧客属性のサポートについて
feature: 顧客属性
topic: 管理
role: Admin
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
source-git-commit: 1fb1abc7311573f976f7e6b6ae67f60ada10a3e7
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 66%

---

# カリフォルニア州消費者プライバシー法に対する顧客属性のサポート

このページでは、カリフォルニア州消費者プライバシー法（CCPA）に対する[!UICONTROL 顧客属性]のサポートについて説明します。

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。（CCPA）に関するアドバイスについては、弁護士に相談してください。

CCPA は 2020 年 1 月 1 日（PT）に発効する、カリフォルニア州の新しいプライバシー法です。CCPA は、カリフォルニア州の住民に対して個人情報に関する新しい権利を提供し、カリフォルニア州で事業をおこなう特定の法人に対してはデータ保護の責任を課します。CCPAは、消費者に対し、自分の個人情報にアクセスし削除する権利と、第三者に対する個人情報の「販売」と見なされる特定の活動をオプトアウトする権利を提供します。

お客様は、ビジネスとして、Adobe Experience Cloudに処理および保管を委任する個人データを決めます。

Adobe Experience Cloudは、サービスプロバイダーとして、Experience Cloud製品やサービスの使用に適用されるCCPAに基づく義務を果たすためのサポートをお客様のビジネスに提供します。 このサポートには、個人情報へのアクセスと削除の要求の管理が含まれます。

このドキュメントでは、[!UICONTROL 顧客属性]が、Adobe Experience Platform Privacy Service APIとPrivacy ServiceUIを使用して、データ主体のCCPAデータアクセスおよび削除権をどのようにサポートするかについて説明します。

CCPA のアドビプライバシーサービスについて詳しくは、[アドビプライバシーセンター](https://www.adobe.com/privacy/ccpa.html)を参照してください。

## [!UICONTROL 顧客属性]のリクエストを送信するために必要な設定

[!UICONTROL 顧客属性]のデータに対するアクセスおよび削除をリクエストするには、次の操作を行う必要があります。

1. 以下を特定します。

   * IMS Org ID
   * 操作する CRS データソースのエイリアス ID
   * アクションを実行するプロファイルの CRM ID

   IMS Org ID は、24 文字の英数字と共に使用される文字列で、末尾に @AdobeOrg が付きます。マーケティングチームまたはアドビの内部システム管理者が組織の IMS Org ID を把握していない場合は、アドビカスタマーケア（gdprsupport@adobe.com）にお問い合わせください。プライバシーAPIにリクエストを送信するには、IMS Org IDが必要です。

1. [!UICONTROL プライバシーサービス]で、顧客属性にアクセスおよび削除のリクエストを送信し、既存のリクエストのステータスを確認できます。

## [!UICONTROL 顧客属性] JSON リクエストの必須フィールド値

&quot;company context&quot;：

* &quot;namespace&quot;：**imsOrgID**
* &quot;value&quot;：&lt;*お客様の IMS Org ID 値*>

&quot;users&quot;:

* &quot;key&quot;：&lt;*通常はお客様の名前*>

* &quot;action&quot;：**access** または **delete** のいずれか

* &quot;user IDs&quot;：

   * &quot;namespace&quot;：&lt;*CRS データソースのエイリアス ID*>

   * &quot;type&quot;：**integrationCode**

   * &quot;value&quot;：&lt;*CRM ID*>

* &quot;include&quot;：**CRS**（リクエストに適用されるアドビ製品）

* &quot;regulation&quot;：**ccpa**（リクエストに適用されるプライバシー規則）

## JSON リクエストの例

```
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "<IMS_ORG_ID>"
    }
  ],
  "users": [
    {
      "key": "<KEY>",
      "action": [
        "<access/delete>"
      ],
      "userIDs": [
        {
          "namespace": "<Alias ID of CRS Data Source>",
          "type": "integrationCode",
          "value": "<CRM ID>"
        }
      ]
    }
  ],
  "regulation": "<gdpr/ccpa/pdpa>",
  "include": [
    "CRS"
  ]
}
```

## アクセスリクエストに対して返されるデータフィールド

```
attributes:
{
"value”:<*value*>,
"key”:<*key*>,
"displayName”:<*displayName*>
}
```
