---
title: EU 一般データ保護規則の [!DNL Customer attributes] サポート
description: EU 一般データ保護規則に対する顧客属性のサポートについて説明します
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 02417c0c-6780-4699-9470-f1685c3cd25d
source-git-commit: 21120abb5ab0fcc8d556012851548f39f3875038
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 95%

---

# [!DNL Customer Attributes] EU 一般データ保護規則のサポート

このページでは、[!DNL Customer Attributes]が EU 一般データ保護規則（GDPR）のサポートについて説明します。

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。GDPR に関するアドバイスについては、弁護士に相談してください。

2018 年 5 月 25 日（PT）施行の法律である [EU 一般データ保護規則](https://business.adobe.com/jp/privacy/general-data-protection-regulation.html)は、欧州連合（EU）圏内にあるすべての個人（データ主体）に対して、自身の個人データを制御する権利を付与します。また、国際ビジネスの規制環境も簡素化します。この法律は、データ管理者の事業拠点に関係なく、個人データが処理される時点において、EU 圏内のユーザーに製品やサービスを提供、それらのユーザーの代理で監視、またはそれらのユーザーの個人データを収集するすべての事業者（データ管理者）に適用されます。

Adobe Experience Cloud は、顧客に代わって受信および保存する個人データのデータ処理者としての役割を果たします。データ管理者であるお客様は、Adobe Experience Cloud に処理および保管を委任する個人データを決めます。

このドキュメントでは、[!DNL Customer Attributes] が Adobe Experience Platform Privacy Service API と Privacy Service UI を使用して、データ主体の GDPR データアクセスおよび削除権をどのようにサポートするかについて説明します。

GDPR がお客様のビジネスに与える影響について詳しくは、[GDPR とお客様のビジネス](https://business.adobe.com/jp/privacy/general-data-protection-regulation.html)を参照してください。

## [!DNL Customer Attributes] のリクエスト送信に必要な設定

[!DNL Customer Attributes] のデータへのアクセスおよび削除をリクエストするには、次の操作が必要です。

1. 以下を特定します。

   * [組織 ID](../../administration/organizations.md)
   * 操作する CRS データソースのエイリアス ID
   * アクションを実行するプロファイルの CRM ID

   [組織 ID](../../administration/organizations.md) は、24 文字の英数字から成る文字列の後に @AdobeOrg が付いたものです。Privacy API にリクエストを送信するには、組織の ID が必要です。ID が見つからない場合は、アドビカスタマーケア（`gdprsupport@adobe.com`）にお問い合わせください。

1. [!UICONTROL プライバシーサービス]で、[!DNL Customer Attributes] にアクセスおよび削除のリクエストを送信し、既存のリクエストのステータスを確認できます。

## [!DNL Customer Attributes] JSON リクエストの必須フィールド値

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
