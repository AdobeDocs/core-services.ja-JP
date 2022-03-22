---
title: 'カリフォルニア州消費者プライバシー法に対する顧客属性のサポート '
description: カリフォルニア州消費者プライバシー法に対する顧客属性のサポートについて
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
source-git-commit: 1fb1abc7311573f976f7e6b6ae67f60ada10a3e7
workflow-type: ht
source-wordcount: '434'
ht-degree: 100%

---

# カリフォルニア州消費者プライバシー法に対する顧客属性のサポート

このページでは、カリフォルニア州消費者プライバシー法（CCPA）に対する[!UICONTROL 顧客属性]のサポートについて説明します。

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。（CCPA）に関するアドバイスについては、弁護士に相談してください。

CCPA は 2020 年 1 月 1 日（PT）に発効する、カリフォルニア州の新しいプライバシー法です。CCPA は、カリフォルニア州の住民に対して個人情報に関する新しい権利を提供し、カリフォルニア州で事業をおこなう特定の法人に対してはデータ保護の責任を課します。CCPA は消費者に対し、自身の個人情報にアクセスする権利やそれらを削除する権利、および第三者への個人の情報の「売却」にあたる特定の活動をオプトアウトする権利を提供します。

お客様は企業として、Adobe Experience Cloud に処理および保管を委任する個人データを決定します。

Adobe Experience Cloud はお客様のサービスプロバイダーとして、Experience Cloud の製品とサービスの使用に適用される、CCPA におけるお客様の義務をお客様が果たせるようサポートを提供します。このサポートには、個人情報へのアクセスおよび削除要求の管理が含まれます。

このドキュメントでは、[!UICONTROL 顧客属性]が、Adobe Experience Platform Privacy Service API と Privacy Service UI を使用して、データ主体の CCPA データアクセスおよび削除権をどのようにサポートするかについて説明します。

CCPA のアドビプライバシーサービスについて詳しくは、[アドビプライバシーセンター](https://www.adobe.com/privacy/ccpa.html)を参照してください。

## [!UICONTROL 顧客属性]のリクエストを送信するために必要な設定

[!UICONTROL 顧客属性]のデータへのアクセスおよび削除をリクエストするには、次の操作が必要です。

1. 以下を特定します。

   * IMS Org ID
   * 操作する CRS データソースのエイリアス ID
   * アクションを実行するプロファイルの CRM ID

   IMS Org ID は、24 文字の英数字と共に使用される文字列で、末尾に @AdobeOrg が付きます。マーケティングチームまたはアドビの内部システム管理者が組織の IMS Org ID を把握していない場合は、アドビカスタマーケア（gdprsupport@adobe.com）にお問い合わせください。プライバシー API にリクエストを送信するには、IMS 組織 ID が必要です。

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
