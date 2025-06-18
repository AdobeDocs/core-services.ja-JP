---
title: カリフォルニア消費者プライバシー法に対する顧客属性のサポート
description: カリフォルニア消費者プライバシー法に対する顧客属性のサポートについて説明します
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
source-git-commit: 361175f290d73f1637673420700874a2415e3fca
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 57%

---

# カリフォルニア消費者プライバシー法に対する顧客属性のサポート

このページでは、カリフォルニア州消費者プライバシー法 ]CCPA）の [!UICONTROL  顧客属性）のサポートについて説明します。

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。（CCPA）に関するアドバイスについては、弁護士に相談してください。

CCPA は、2020 年 1 月 1 日に施行されるカリフォルニア州の新しいプライバシー法です。 CCPA は、カリフォルニア州の住民に対して個人情報に関する新しい権利を提供し、カリフォルニア州で事業をおこなう特定の法人に対してはデータ保護の責任を課します。CCPA は、消費者に対し、自身の個人情報にアクセスして削除する権利、および第三者への個人情報の「販売」に該当する特定の活動をオプトアウトする権利を提供します。

お客様は企業として、Adobe Experience Cloud に処理および保管を委任する個人データを決定します。

Adobe Experience Cloud はお客様のサービスプロバイダーとして、Experience Cloud の製品とサービスの使用に適用される、CCPA におけるお客様の義務をお客様が果たせるようサポートを提供します。このサポートには、個人情報へのアクセスおよび削除要求の管理が含まれます。

このドキュメントでは、[!UICONTROL  顧客属性 ] が、Adobe Experience Platform Privacy Service API とPrivacy Service UI を使用して、データ主体の CCPA データアクセスおよび削除権をどのようにサポートするかについて説明します。

CCPA のアドビプライバシーサービスについて詳しくは、[アドビプライバシーセンター](https://www.adobe.com/privacy/ccpa.html)を参照してください。

## [!UICONTROL  顧客属性 ] のリクエストを送信するために必要な設定

[!UICONTROL  顧客属性 ] のデータへのアクセスおよび削除をリクエストするには、次の操作が必要です。

1. 以下を特定します。

   * [組織 ID](../../administration/organizations.md)
   * 操作する CRS データソースのエイリアス ID
   * アクションを実行するプロファイルの CRM ID

   組織 ID は、24 文字の英数字から成る文字列の後に@AdobeOrg が付いたものです。 Privacy API にリクエストを送信するには、組織の ID が必要です。ID が見つからない場合は、アドビカスタマーケア（`gdprsupport@adobe.com`）にお問い合わせください。

1. [!UICONTROL Privacy Service] では、顧客属性に対してアクセスリクエストおよび削除リクエストを送信したり、既存のリクエストのステータスを確認したりできます。

## [!UICONTROL  顧客属性 ] JSON リクエストの必須フィールド値

&quot;company context&quot;：

* &quot;namespace&quot;：**imsOrgID**
* 「value」: &lt;*組織 ID の値*>

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

```json
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

```json
attributes:
{
"value": "<*value*>",
"key": "<*key*>",
"displayName": "<*displayName*>"
}
```
