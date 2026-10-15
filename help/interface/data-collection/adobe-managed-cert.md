---
description: Adobe CX Enterpriseのファーストパーティ Cookieで使用する安全な証明書を設定する方法について説明します。
solution: Experience Cloud,Analytics
title: Adobe 管理証明書プログラム
index: true
snippet: 'y'
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
autotag-review: '2026-09-09T20:12:24.943Z'
TQID: 'https://experienceleague.adobe.com/8CSBLQaw3KOByyxxCYr1By4gyAQsDIhiofOdAzn38dg'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
    internal-label: Support
  - id: c8add8f2-4250-4fd9-9cde-9707036c567d
    internal-label: Methods
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
    internal-label: Appmeasurement implementation
  - id: e992d880-33bc-4949-a648-aa7d410276cd
    internal-label: Validation
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 18fd590d6f0fd1800e3d5c62851453aa91d9db5f
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 2%
---
# アドビの管理による証明書プログラム

Adobeで管理される証明書プログラムは、CNAMEの実装に必要なファーストパーティ証明書を設定する際にお勧めのプロセスです。 設定したらプログラムは完全に自動化されます。 有効期限が切れた証明書によるデータ収集への影響がないように、証明書をタイムリーに更新します。 このプログラムは、最初の100個のCNAMEに対して無料です。

Adobeで管理されている証明書プログラムでは、コンテンツ配信ネットワーク（CDN）を介したデータ収集のルーティングはサポートされていません。 CDNを使用する場合は、「[CDNを介してデータ収集をルーティングする](cdn.md)」を参照してください。 独自の証明書を管理する必要がある組織は、代わりに[顧客管理の証明書](customer-managed-cert.md)を使用できます。 現在、独自の証明書を管理しており、Adobeが管理する証明書プログラムに移行する場合は、Adobe カスタマーケアにお問い合わせください。

## 実装

ファーストパーティデータ収集用の新しい証明書を実装するには、次の手順に従います。

1. [ ファーストパーティのドメイン要求フォームをダウンロードして入力します](cookies/assets/First_Party_Domain_Request_Form.xlsx)
1. Adobe カスタマーケアでチケットを開き、Adobeが管理する証明書プログラムでファーストパーティデータの収集を設定するようにリクエストします。 組織にデータレジデンシーまたはコンプライアンス要件がある場合は、リクエストに目的の[RDC タイプ ](rdc.md)を指定します。
1. チケットを受け取ると、Adobeの担当者がCNAME レコードを提供します。 このレコードは、Adobeが証明書を購入する前に、会社のDNS サーバーで設定する必要があります。 例えば、ホスト名`data.example.com`は`hiodsibxvip01.data.adobedc.net`を指しています。 組織でDNS認証局認証（CAA） レコードを使用している場合は、CAA レコードでDigiCertが証明書を発行できることを確認してください。 [ メンテナンスと更新](#renewals)を参照してください。
1. 組織のサーバーにCNAME レコードが配置されている場合、AdobeはDigiCertと連携して、Adobe データ収集サーバーに証明書を購入してインストールします。
1. Adobe CNAMEがファーストパーティの目的でホストしているときに`robots.txt` ファイルの更新が必要な場合は、カスタマーケアにお問い合わせください。 このようなリクエストは、Googleがサブドメインをクロールできないように`robots.txt` ファイルを更新する場合に関連します。

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

新しいCNAME ホスト名を使用するには、証明書が正しく動作することを検証したら、Adobeの実装を更新します。 [実装の更新](collection-domain.md#update-implementation)を参照してください。

## メンテナンスと更新 {#renewals}

Adobeは、証明書を自動的に更新します。 証明書の有効期限が切れる30日前に、AdobeはCNAMEがまだ有効で使用中であることを検証し、代わりに証明書を更新します。 更新を維持するには、次のDNSの変更を避けます。

* **CNAME レコードの削除または再指定**: CNAME レコードが削除されたか、Adobeのセキュアホスト名を指さなくなった場合、Adobeは証明書を更新できません。 この条件には、CNAME レコードをコンテンツ配信ネットワーク（CDN）に指定することが含まれます。 CDNを使用する場合は、DNS レコードを変更する前に、[既存のファーストパーティ実装をCDN](cdn.md#migrate)に移動するを参照してください。
* **DigiCertを認証しないCAA レコードを追加しています**：認証局は、ホスト名とその親ドメインの認証局認証（CAA）レコードを確認します。 CAA レコードを使用する場合は、`digicert.com`を承認済み発行者として含めます。 例：`example.com. IN CAA 0 issue "digicert.com"`。
* **特定のアカウントへのDigiCert発行の制限**: DigiCertのドメインロック機能により、`example.com. IN CAA 0 issue "digicert.com; account=<token>"`などのCAA レコードに`account=` パラメーターが追加されます。 このパラメーターは、`digicert.com`が許可されている場合でも、組織のDigiCert アカウントへの発行を制限し、Adobeが証明書を取得できないようにします。 組織でDigiCert ドメインのロックが必要な場合は、代わりに[顧客管理の証明書](customer-managed-cert.md)を使用してください。 ドメインレジストラで設定されたドメインロック（転送ロックとも呼ばれます）は関連がなく、Adobeで管理される証明書には影響しません。

>[!IMPORTANT]
>
>CNAME レコードがAdobe セキュアホスト名を指さなくなった場合、Adobe システム内のエントリは、それ以上の通信を行わずに削除するようにマークされます。

## よくある質問

+++このプロセスは安全ですか？

はい。 Adobeで管理されている証明書プログラムは、[お客様が管理する証明書](customer-managed-cert.md)よりも安全です。 Adobeおよび発行証明機関の外部に証明書または秘密鍵が転送されることはありません。

+++

+++Adobeでドメインの証明書を購入するにはどうすればよいですか？

証明書は、指定したホスト名をAdobeが所有するホスト名に指定した場合にのみ購入できます。 このホスト名をAdobeにデリゲートし、Adobeが代わりに証明書を購入できるようにします。

+++

+++証明書の失効をリクエストできますか？

はい。 ドメインの所有者は、証明書の失効をリクエストできます。 このプロセスを開始するには、Adobe カスタマーケアにお問い合わせください。

+++

+++どの暗号化タイプが使用されますか？

AdobeはDigiCertと連携してSHA-2証明書を発行します。

+++

+++このプログラムには追加費用がかかりますか？

Adobeでは、最初の100 CNAMEの追加費用なしで、すべてのAdobe CX Enterpriseのお客様にこのプログラムを提供しています。

+++

+++Adobeはどのような暗号セキュリティレベルを提供していますか？

Adobeは、1st パーティデータの収集に対するセキュリティに対するお客様のさまざまなニーズを満たすために、2つの暗号セキュリティレベルを提供します。 これらのレベルにより、Adobe サーバーとのHTTPS接続でサポートされる暗号化アルゴリズムが決まります。 Adobeでは、現在のセキュリティ対策にもとづいて、サポートされているアルゴリズムのセットを定期的に確認および更新しています。 暗号のセキュリティ設定を変更するには、カスタマーケアにお問い合わせください。

* **Standard**&#x200B;では、TLS 1.2以降と少なくとも128 ビットの暗号化が必要です。 安全な暗号化を維持しながら、最も幅広いデバイス互換性を提供するように設計されています。
* **High**&#x200B;では、TLS 1.2以降が必要で、より弱い暗号のサポートが削除されます。 これは、最も強力な暗号化を必要とするお客様向けに設計されています。 2015年以前にリリースされたクライアントは、通常、暗号セキュリティが&#x200B;**High**&#x200B;に設定されている場合は接続できません。

+++

+++どのHTTPS証明書タイプがサポートされていますか？

AdobeはRSAとECCの両方の証明書をサポートし、最新のクライアントは両方の証明書タイプをサポートしています。 ECC証明書は、サーバーとクライアントの両方での処理が少なくて済みます。 Adobeで管理される証明書の場合、AdobeはRSA証明書とECC証明書の両方を提供します。 [顧客が管理する証明書](customer-managed-cert.md)の場合、RSAが必要であり、ECCが推奨されます。

+++

