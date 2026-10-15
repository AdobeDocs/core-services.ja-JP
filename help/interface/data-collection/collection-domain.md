---
title: データ収集ドメインの選択
description: Adobeにデータを送信するために使用できるドメインと、組織のテナント IDを検索する方法について説明します。
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: e1185eeafc809b036b10955880536db7a576ca0b
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 3%
---
# データ収集ドメインの選択

データ収集ドメインは、実装がデータを送信するホスト名です。 Adobe データ収集を使用するすべてのAdobe CX Enterprise製品（Adobe Analytics、Customer Journey Analytics、Adobe Experience Platform、Adobe Target、Adobe Journey Optimizerなど）は、このドメインに依存しています。

## データ収集ドメインのオプション

| オプション | 実装ドメイン | リージョンロック済み[RDC](rdc.md) | 証明書の保守 |
| --- | --- | --- | --- |
| [&#x200B; サードパーティのドメイン &#x200B;](#third-party) | `example.data.adobedc.net` | サポートなし | なし |
| [Adobeが管理する証明書](adobe-managed-cert.md)を持つファーストパーティドメイン | `data.example.com` | 対応 | なし（Adobeは証明書を自動更新します） |
| [顧客が管理する証明書](customer-managed-cert.md)を持つファーストパーティドメイン | `data.example.com` | 対応 | 証明書が更新され、Adobeに提供されます |
| サードパーティのオリジンを持つ[&#x200B; コンテンツ配信ネットワーク（CDN） &#x200B;](cdn.md#third-party-origin) | `data.example.com` | サポートなし | なし |
| [&#x200B; ファーストパーティオリジンを持つCDN](cdn.md#first-party-origin) | `data.example.com` | 対応 | 証明書が更新され、Adobeに提供されます |

## サードパーティデータの収集 {#third-party}

1st パーティドメインを使用しない場合は、`data.adobedc.net`のサブドメインにデータを送信します。 Adobeでは、組織の[&#x200B; テナント ID](#tenant-id)をサブドメインとして使用することをお勧めします。 例：`example.data.adobedc.net`。 このドメインは、[CDN](cdn.md)を介してデータ収集をルーティングする場合にも推奨されるオリジンです。

* サードパーティドメインでは、常にデフォルトの[RDC タイプ &#x200B;](rdc.md#third-party-data-collection)が使用されます。
* `example.data.adobedc.net`より深いサブドメインは使用しないでください。 例えば、`custom.example.data.adobedc.net`は有効なデータ収集ドメインではありません。
* 古い実装では、`sc.omtrdc.net`や`2o7.net`などのドメインを使用する場合があります。 これらのドメインは引き続き有効ですが、Adobeでは可能な限り`data.adobedc.net`を使用することをお勧めします。

### テナント IDの検索 {#tenant-id}

1. Adobe IDの資格情報を使用して[Adobe CX Enterprise](https://experience.adobe.com)にログインします。
1. CX Enterprise インターフェイスの任意の場所で、`[Cmd]` + `[I]` （macOS）または`[Ctrl]` + `[I]` （Windows）を押します。
1. **[!UICONTROL ユーザーデータデバッガー]**&#x200B;が表示されます。 「**[!UICONTROL 割り当てられた組織]**」タブを選択します。
1. 目的のIMS組織を展開します。
1. 「**[!UICONTROL テナント]**」フィールドを探します。 この値はテナント IDです。

テナント IDがIMS組織IDと異なり、`@AdobeOrg`で終わります。 各IMS組織には、1つのテナント IDがあります。 会社で複数のIMS組織を使用している場合は、各組織に独自のテナント IDがあります。

## 実装の更新 {#update-implementation}

データ収集ドメインを変更する場合は、Adobeにデータを送信するすべての実装を更新します。

* **Web SDK タグ拡張機能**：拡張機能の設定時に[[!UICONTROL Edge domain]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/general) フィールドを更新します。
* **Web SDK （alloy）**: `configure` コマンド内の[`edgeDomain`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/edgedomain) プロパティを更新します。
* **Adobe Analytics拡張機能**：拡張機能の設定時に[[!UICONTROL SSL Tracking Server]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/analytics/overview) フィールドを更新します。 [訪問者ID サービスタグ拡張機能](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/id-service/overview)もインストールされていることを確認してください。 詳しくは、[Analytics タグ拡張機能を使用した訪問者の識別](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/analytics-extension)を参照してください。
* **AppMeasurement**: [`trackingServerSecure`](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/config-vars/trackingserversecure)構成変数を更新します。 [訪問者ID サービス &#x200B;](https://experienceleague.adobe.com/ja/docs/id-service/using/home)が`VisitorAPI.js`を使用して実装されていることも確認してください。 詳しくは、[AppMeasurementを使用した訪問者特定](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/appmeasurement)を参照してください。
* **その他の実装**: モバイルアプリやサーバーサイド実装など、Adobeにデータを送信するその他の実装で、データ収集ドメインを更新します。

実装で訪問者ID サービスまたはWeb SDKを使用しない場合、データ収集ドメインを変更すると、訪問者Cookieのドメインが変更され、再訪問者は新規訪問者としてカウントされます。

サイトで複数の実装方法を使用しており、すべての実装方法を同時に更新できない場合は、猶予期間の設定を検討してください。 サイト全体で訪問者が新規訪問者としてカウントされないようにする方法について詳しくは、[訪問者ID サービスの移行に関する考慮事項](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/migration)を参照してください。
