---
title: カリフォルニア州消費者プライバシー法の[!DNL Customer Attributes] サポート
description: カリフォルニア州消費者プライバシー法の [!DNL Customer Attributes]  サポートについて詳しく見る
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
TQID: 'https://experienceleague.adobe.com/YPl1rlZRciwN6GM7mtkqMKjPsW-H1ueMG4zqbH8auho'
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 9c2010694b8bb32c3922dd65f846375e43b2caac
workflow-type: tm+mt
source-wordcount: 404
ht-degree: 52%

---

# カリフォルニア州消費者プライバシー法の[!DNL Customer Attributes] サポート

このページでは、カリフォルニア州消費者プライバシー法（CCPA）の[!DNL Customer Attributes]のサポートについて説明します。

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。 （CCPA）に関するアドバイスについては、弁護士に相談してください。

CCPAは、2020年1月1日に施行されるカリフォルニア州の新しいプライバシー法です。 CCPA は、カリフォルニア州の住民に対して個人情報に関する新しい権利を提供し、カリフォルニア州で事業をおこなう特定の法人に対してはデータ保護の責任を課します。 CCPAは、消費者が自身の個人情報にアクセスして削除する権利と、個人情報を第三者に「販売」すると認定される特定の活動をオプトアウトする権利を提供します。

企業は、Adobe CX Enterpriseが代理で処理および保存する個人データを決定します。

お客様のサービスプロバイダーとして、Adobe CX Enterpriseは、CX Enterprise製品およびサービスの使用に適用されるCCPAに基づく義務を果たすため、お客様のビジネスをサポートします。 このサポートには、個人情報へのアクセスおよび削除要求の管理が含まれます。

このドキュメントでは、[!DNL Customer Attributes]がAdobe Experience Platform Privacy Service APIとPrivacy Service UIを使用して、データ主体のCCPA データへのアクセス権と削除権をどのようにサポートしているかを説明します。

CCPA のアドビプライバシーサービスについて詳しくは、[アドビプライバシーセンター](https://www.adobe.com/privacy/ccpa.html)を参照してください。

## [!DNL Customer Attributes] のリクエスト送信に必要な設定

[!DNL Customer Attributes] のデータへのアクセスおよび削除をリクエストするには、次の操作が必要です。

1. 以下を特定します。

   * [組織 ID](../../administration/organizations.md)
   * 操作する CRS データソースのエイリアス ID
   * アクションを実行するプロファイルの CRM ID

   組織IDは、24文字の英数字の文字列に@AdobeOrgが追加されています。 Privacy API にリクエストを送信するには、組織の ID が必要です。 ID が見つからない場合は、アドビカスタマーケア（`gdprsupport@adobe.com`）にお問い合わせください。

1. [!UICONTROL Privacy Service]では、顧客属性にアクセス要求と削除要求を送信し、既存の要求のステータスを確認できます。

## [!DNL Customer Attributes] JSON リクエストの必須フィールド値

&quot;company context&quot;：

* &quot;namespace&quot;：**imsOrgID**
* &quot;value&quot;: &lt;*組織ID値*>

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
