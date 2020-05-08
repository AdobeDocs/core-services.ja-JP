---
title: 一般的なデータ保護規制に対する顧客属性のサポート
description: 一般的なデータ保護規制に対する顧客属性のサポート
translation-type: tm+mt
source-git-commit: 3a86aed0794c3e35cc028e5bfde5dafcb2285fc8
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 6%

---


# 一般的なデータ保護規制に対する顧客属性のサポート


>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。一般的なデータ保護規則に関するアドバイスについては、法律顧問にお問い合わせください。

2018年5月25日発効の法律、 [GDPR(](https://www.adobe.com/privacy/general-data-protection-regulation/what-is-gdpr.html) General Data Protection Regulation)は、欧州和集合(EU)の国境にあるすべての個人（データ・テーマ）に個人データの制御を与え、国際事業に関する規制環境を簡素化する。 この法律は、オファー商品やサービスを、EUの国境内の個人から、データ管理者の事業所に関係なく個人データの処理を行う際に、その個人データの処理を行う個人データの収集、監視、収集を行う全ての事業者（データ管理者）に適用される。

Adobe Experience Cloudは、顧客に代わって個人データを受け取り、保存する場合のデータプロセッサーの役割を果たします。 データコントローラーは、Adobe Experience Cloudが処理し、お客様に代わって保存する個人データを決定します。

このドキュメントでは、顧客属性がAdobe Experience Platform Privacy Service APIとPrivacy Service UIを使用して、データサブジェクトのGDPRデータアクセスおよび削除権限をどのようにサポートするかを説明します。

GDPRがお客様のビジネスに与える意味の詳細は、「 [GDPRとお客様のビジネス](https://www.adobe.com/jp/privacy/general-data-protection-regulation.html)」を参照してください。

## 顧客属性に対する要求を送信するために必要な設定

顧客属性のデータにアクセスして削除するリクエストを作成するには、次の操作が必要です。

1. 以下を特定します。

* IMS Org ID
* 操作するCRSデータソースのエイリアスID
* アクションを実行するプロファイルのCRM ID

IMS組織IDは、24文字の英数字と共に使用される文字列で、その後に@AdobeOrgが付加されます。 マーケティングチームまたはアドビの内部システム管理者が組織のIMS組織IDを知らない場合は、アドビカスタマーケア(gdprsupport@adobe.com)にお問い合わせください。 プライバシーAPIにリクエストを送信するには、IMS組織IDが必要です。

2. アクセス要求や削除要求を顧客属性に送信したり、既存の要求のステータスを確認したりするには、プライバシーサービスUIを使用します。

## 顧客属性JSONリクエストの必須フィールド値

&quot;会社コンテキスト&quot;:

* &quot;名前空間&quot;: **imsOrgID**
* &quot;value”: &lt;*your IMS Org ID value*>

&quot;users&quot;:

* &quot;key&quot;: &lt;*通常はお客様の名前*>

* &quot;action&quot;: **アクセス** または **削除**

* &quot;user IDs&quot;:

   * &quot;名前空間&quot;: &lt;*Alias ID of CRS Data Source*>

   * &quot;type&quot;: **integrationCode**

   * &quot;value”: &lt;*CRM ID*>

* &quot;include&quot;: **CRS** （リクエストに適用されるAdobe製品）

* &quot;regulation&quot;: **gdpr** （リクエストに適用されるプライバシー規則）

## JSONリクエストの例

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

## Access要求に対して返されるデータフィールド

```
attributes:
{
"value”:<*value*>,
"key”:<*key*>,
"displayName”:<*displayName*>
}
```
