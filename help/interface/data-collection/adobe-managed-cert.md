---
description: Adobe CX Enterpriseのファーストパーティ Cookieで使用する安全な証明書を設定する方法について説明します。
solution: Experience Cloud,Analytics
title: Adobe 管理証明書プログラム
index: true
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
TQID: https://experienceleague.adobe.com/LWbjh-jXKmY6mcl047uzA1ZkhZlAmeNpt9JRg3Ynt9E
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: c8add8f2-4250-4fd9-9cde-9707036c567d
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
  - id: e992d880-33bc-4949-a648-aa7d410276cd
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 1243
ht-degree: 2%

---

# アドビの管理による証明書プログラム

Adobeで管理される証明書プログラムは、CNAMEの実装に必要なファーストパーティ証明書を設定する際にお勧めのプロセスです。 設定したらプログラムは完全に自動化されます。 有効期限が切れた証明書によるデータ収集への影響がないように、証明書をタイムリーに更新します。 このプログラムは、最初の100個のCNAMEに対して無料です。

現在、独自の証明書を管理している場合は、1st パーティ Cookieの使用のためにAdobeに証明書を購入、管理、提供する責任があります。 Adobeが管理する証明書プログラムへの移行については、Adobe カスタマーケアにお問い合わせください。

## 実装

ファーストパーティデータ収集用の新しい証明書を実装するには、次の手順に従います。

1. [&#x200B; ファーストパーティのドメイン要求フォームをダウンロードして入力します](cookies/assets/First_Party_Domain_Request_Form.xlsx)
1. Adobe カスタマーケアでチケットを開き、Adobeが管理する証明書プログラムでファーストパーティデータの収集を設定するようにリクエストします。 組織にデータレジデンシーまたはコンプライアンス要件がある場合は、リクエストに目的の[RDC タイプ &#x200B;](rdc.md)を指定します。
1. チケットを受け取ると、Adobeの担当者がCNAME レコードを提供します。 このレコードは、Adobeが証明書を購入する前に、会社のDNS サーバーで設定する必要があります。 例えば、ホスト名`data.example.com`は`hiodsibxvip01.data.adobedc.net`を指しています。
1. 組織のサーバーにCNAME レコードが配置されている場合、AdobeはDigiCertと連携して、Adobe データ収集サーバーに証明書を購入してインストールします。

## ホスト名転送の検証

Adobeが証明書をインストールしたら、次のいずれかの方法を使用して、証明書が機能していることを検証できます。

+++**ブラウザーの検証**

任意のブラウザーを使用して、証明書が正しくインストールされていることを検証できます。 アドレスバーへのパスとして`_check`を含むCNAMEを入力します。 例：

`data.example.com/_check`

すべてが機能する場合、ブラウザーに`SUCCESS`が表示されます。 証明書が正しくインストールされていない場合、セキュリティ警告が表示されます。

+++

+++**コマンドライン （`curl`）**

ほとんどの最新のオペレーティング システムには、既に[`curl`](https://curl.se)がインストールされています。

コマンドラインに次のコマンドを入力します。

```sh
curl data.example.com/_check
```

すべてが正しく動作すると、コンソールは`SUCCESS`を返します。

>[!TIP]
>
>トラブルシューティングに役立つセキュリティ警告を無効にするには、`-k` フラグを使用します。

+++

+++**コマンドライン （`nslookup`）**

コマンドラインに次のコマンドを入力します。

```sh
nslookup data.example.com
```

すべてが正しく機能すると、Adobeのデータ収集サーバーが返されます。

```text
Server: hiodsibxvip01.corp.adobe.com
Address: 10.50.112.247

Name: example.com.ssl.d1.sc.omtrdc.net
Addresses: 63.140.37.126
    63.140.37.206
    63.140.36.51
    63.140.36.145
Aliases: data.example.com
```

+++

## 実装コードの更新

証明書が正しく機能することを検証したら、新しいCNAME ホスト名を使用するようにAdobeの実装を更新できます。

* **Web SDK タグ拡張機能**：拡張機能の設定時に[[!UICONTROL Edge domain]](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/extensions/client/web-sdk/configure/general) フィールドを更新します。
* **Web SDK （alloy）**: `configure` コマンド内の[`edgeDomain`](https://experienceleague.adobe.com/ja/docs/experience-platform/collection/js/commands/configure/edgedomain) プロパティを更新します。
* **Adobe Analytics拡張機能**：拡張機能の設定時に[[!UICONTROL SSL Tracking Server]](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/extensions/client/analytics/overview) フィールドを更新します。 [訪問者ID サービスタグ拡張機能](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/extensions/client/id-service/overview)もインストールされていることを確認してください。 詳しくは、[Analytics タグ拡張機能を使用した訪問者の識別](https://experienceleague.adobe.com/ja/docs/analytics/implementation/id/analytics-extension)を参照してください。
* **AppMeasurement**: [`trackingServerSecure`](https://experienceleague.adobe.com/ja/docs/analytics/implementation/vars/config-vars/trackingserversecure)構成変数を更新します。 [訪問者ID サービス &#x200B;](https://experienceleague.adobe.com/ja/docs/id-service/using/home)が`VisitorAPI.js`を使用して実装されていることも確認してください。 詳しくは、[AppMeasurementを使用した訪問者特定](https://experienceleague.adobe.com/ja/docs/analytics/implementation/id/appmeasurement)を参照してください。

サイトで複数の実装方法を使用しており、すべての実装方法を同時に更新できない場合は、猶予期間の設定を検討してください。 サイト全体で訪問者が新規訪問者としてカウントされないようにする方法について詳しくは、[訪問者ID サービスの移行に関する考慮事項](https://experienceleague.adobe.com/ja/docs/analytics/implementation/id/migration)を参照してください。

## メンテナンスと更新

ファーストパーティ証明書の有効期限が切れる30日前に、AdobeはCNAMEがまだ有効で使用中かどうかを検証します。 その場合、Adobeは、サービスを引き続き使用することを想定し、代わりに証明書を自動的に更新します。

>[!IMPORTANT]
>
>組織のCNAME レコードが削除されたか、指定されたAdobe セキュアホスト名にマッピングされなくなった場合、Adobeは証明書を更新できません。 Adobeのシステム内のエントリは、それ以上の通信なしで削除するようにマークされています。

## よくある質問

+++このプロセスは安全ですか？

はい。 Adobeで管理される証明書プログラムは、Adobeに証明書を提供する組織よりも安全です。 Adobeおよび発行元の認証局の外部で証明書や秘密鍵が変更されることはありません。

+++

+++Adobeでドメインの証明書を購入するにはどうすればよいですか？

証明書は、指定したホスト名をAdobeが所有するホスト名に指定した場合にのみ購入できます。 このホスト名をAdobeにデリゲートし、Adobeが自分に代わって証明書を購入することを許可します。

+++

+++証明書の失効をリクエストできますか？

はい。 ドメインの所有者は、証明書の失効をリクエストできます。 このプロセスを開始するには、Adobe カスタマーケアにお問い合わせください。

+++

+++どの暗号化タイプが使用されますか？

AdobeはDigiCertと連携してSHA-2証明書を発行します。

+++

+++このプログラムには追加費用がかかりますか？

いいえ。 Adobeでは、Adobe CX Enterpriseをご利用のお客様に追加費用なしでサービスを提供しています。

+++

+++Adobeはどのような暗号セキュリティレベルを提供していますか？

Adobeは、1st パーティデータの収集に対するセキュリティに対するお客様のさまざまなニーズを満たすために、2つの暗号セキュリティレベルを提供します。 これらのレベルにより、Adobe サーバーとのHTTPS接続でサポートされる暗号化アルゴリズムが決まります。 Adobeでは、現在のセキュリティ対策にもとづいて、サポートされているアルゴリズムのセットを定期的に確認および更新しています。 暗号セキュリティの設定を変更する場合は、カスタマーケアにお問い合わせください。

* **Standard**&#x200B;では、TLS 1.2以降と少なくとも128 ビットの暗号化が必要です。 安全な暗号化を維持しながら、最も幅広いデバイス互換性を提供するように設計されています。
* **High**&#x200B;では、TLS 1.2以降が必要で、より弱い暗号のサポートが削除されます。 これは、最も強力な暗号化を望み、古いデバイスのサポートを心配しない顧客向けに設計されています。

次のクライアントは、**High**&#x200B;に設定された暗号セキュリティに接続できないことが判明しています。

* Windows 8.1以前（最終更新日：2018年）
* Windows Phone 8.1以前（最終更新日：2016年）
* OS X 10.10以前（最終更新日：2017年）
* iOS 8.4以前（最終更新は2015年）

+++

+++どのHTTPS証明書タイプがサポートされていますか？

Adobeでは、様々なお客様のニーズに対応するために、RSAとECCの両方の証明書タイプをサポートしています。 RSA証明書はクライアントにとってより広くサポートされていますが、ECC証明書はサーバーサイドとクライアントサイドの両方でより少ない処理を使用します。 Adobeで管理される証明書の場合は、RSAとECCの両方が提供されます。 顧客が管理する証明書の場合は、RSAが必要であり、ECCが推奨されます。 最新のクライアントは、RSAとECCの両方をサポートしています。 通常、次のクライアントはRSA証明書のみをサポートします。

* Windows Vista以前（最終更新日：2012年）
* Windows Phone 8.0以前（最終更新日：2014年）
* OS X 10.8以前（最終更新日：2013年）
* iOS 5.1以前（最終更新は2012年）
* Android 4.3以前（最終更新は2013年）

+++

+++代わりに自分の証明書を管理できますか？

はい。 ただし、独自の証明書を管理する場合は、証明書を更新し、更新するたびにAdobeに提供する責任があります。 このプロセスは安全性が低く、組織が証明書の更新を期限内に忘れた場合、データ収集にギャップが生じる可能性があります。 Adobeでは、特にTLS証明書の最大有効期間が短縮されたため、自分で証明書を管理する代わりにマネージド証明書プログラムを使用することをお勧めします。 詳しくは、「CA/Browser Forum Server Certificate Baseline Requirements」の「[6.3.2証明書の運用期間とキーペアの使用期間](https://cabforum.org/working-groups/server/baseline-requirements/requirements/#632-certificate-operational-periods-and-key-pair-usage-periods)」を参照してください。
+++

