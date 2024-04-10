---
title: “[!DNL Customer Attributes] EU 一般データ保護規則のサポート」
description: EU 一般データ保護規則に対する顧客属性のサポートについての説明
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 02417c0c-6780-4699-9470-f1685c3cd25d
source-git-commit: f229ec33ff721527e6a4c920ea63eabb4102935a
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 77%

---

# [!DNL Customer Attributes] eu 一般データ保護規則のサポート

このページでは、その方法について説明します [!DNL Customer Attributes] は、EU 一般データ保護規則（GDPR）をサポートしています。

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。GDPR に関するアドバイスについては、弁護士に相談してください。

2018 年 5 月 25 日（PT）施行の法律である [EU 一般データ保護規則](https://business.adobe.com/jp/privacy/general-data-protection-regulation.html)は、欧州連合（EU）圏内にあるすべての個人（データ主体）に対して、自身の個人データを制御する権利を付与します。また、国際ビジネスの規制環境も簡素化します。この法律は、データ管理者の事業拠点に関係なく、個人データが処理される時点において、EU 圏内のユーザーに製品やサービスを提供、それらのユーザーの代理で監視、またはそれらのユーザーの個人データを収集するすべての事業者（データ管理者）に適用されます。

Adobe Experience Cloud は、顧客に代わって受信および保存する個人データのデータ処理者としての役割を果たします。データ管理者であるお客様は、Adobe Experience Cloud に処理および保管を委任する個人データを決めます。

このドキュメントでは、その方法を説明します [!DNL Customer Attributes] は、Adobe Experience Platform Privacy Service API とPrivacy ServiceUI を使用して、データ主体の GDPR データアクセスおよび削除権をサポートします。

GDPR がお客様のビジネスに与える意味の詳細は、「[GDPR とお客様のビジネス](https://business.adobe.com/jp/privacy/general-data-protection-regulation.html)」を参照してください。

## リクエストを送信するために必要な設定 [!DNL Customer Attributes]

のデータへのアクセスおよび削除をリクエストするには [!DNL Customer Attributes]は、以下を行う必要があります。

1. 以下を特定します。

   * [組織 ID](#organizations.md)
   * 操作する CRS データソースのエイリアス ID
   * アクションを実行するプロファイルの CRM ID

   [組織 ID](#organizations.md) は、24 文字の英数字から成る文字列の後に @AdobeOrg が付いたものです。Privacy API にリクエストを送信するには、組織の ID が必要です。ID が見つからない場合は、アドビカスタマーケア（`gdprsupport@adobe.com`）にお問い合わせください。

1. 対象： [!UICONTROL Privacy Service]アクセス要求および削除要求をに送信できます。 [!DNL Customer Attributes]既存のリクエストのステータスを確認します。

## の必須フィールド値 [!DNL Customer Attributes] JSON リクエスト

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

* &quot;regulation&quot;：**gdpr**（リクエストに適用されるプライバシー規則）

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
"value":<*value*>,
"key":<*key*>,
"displayName":<*displayName*>
}
```
