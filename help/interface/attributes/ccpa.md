---
title: カリフォルニア消費者プライバシー法の顧客属性サポート
description: カリフォルニア消費者プライバシー法の顧客属性サポート
translation-type: tm+mt
source-git-commit: 8709449909ce4fbd441d77fb4bbfb0b7758e805d
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 5%

---


# カリフォルニア州消費者プライバシー法の顧客属性サポート

このページでは、カリフォルニア州消費者プライバシー法(CCPA)に対する  顧客属性のサポートについて説明します。

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。(CCPA)に関するアドバイスについては、弁護士に相談してください。

CCPAはカリフォルニア州の新しいプライバシー法で、2020年1月1日から有効です。 CCPAは、カリフォルニア州の居住者に対して個人情報に関する新しい権利を提供し、カリフォルニア州でビジネスを行う特定の企業に対してデータ保護の責任を負います。 CCPAは、顧客に対して、個人情報にアクセスしたり削除したりする権利と、第三者に対して個人情報を「販売」すオプトアウトると認められる特定のアクティビティに対する権利を提供します。

ビジネスの場合、Adobe Experience Cloudが処理し、お客様に代わって保存する個人データを決定します。

Adobe Experience Cloudは、個人サービスプロバイダーへのアクセスと削除の要求の管理など、Experience Cloudの製品とサービスの使用に適用されるCCPAに基づく義務を満たすためのサポートをお客様のビジネスに提供します。

このドキュメントでは、 [!UICONTROL 顧客属性が] 、Adobe Experience Platform Privacy Service APIとPrivacy Service UIを使用して、データサブジェクトのCCPAデータアクセスおよび削除権限をどのようにサポートするかを説明します。

CCPAのアドビプライバシーサービスについて詳しくは、アドビプライバシーセンターを参照して [ください](https://www.adobe.com/privacy/ccpa.html)。

## 顧客属性の要求を送信するために必要な [!UICONTROL 設定]

顧客属性のデータにアクセスして削除するリクエストを作成するには 、次の操作が必要になります。

1. 以下を特定します。

   * IMS Org ID
   * 操作するCRSデータソースのエイリアスID
   * アクションを実行するプロファイルのCRM ID
   IMS組織IDは、24文字の英数字と共に使用される文字列で、その後に@AdobeOrgが付加されます。 マーケティングチームまたはアドビの内部システム管理者が組織のIMS組織IDを知らない場合は、アドビカスタマーケア(gdprsupport@adobe.com)にお問い合わせください。 プライバシーAPIにリクエストを送信するには、IMS組織IDが必要です。

1. プ [!UICONTROL ライバシーサービスでは]、顧客属性にアクセスおよび削除の要求を送信し、既存の要求のステータスを確認できます。

## [!UICONTROL 顧客属性] JSONリクエストの必須フィールド値

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

* &quot;regulation&quot;: **ccpa** （リクエストに適用されるプライバシー規則）

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

## アクセス要求に対して返されるデータフィールド

```
attributes:
{
"value”:<*value*>,
"key”:<*key*>,
"displayName”:<*displayName*>
}
```
