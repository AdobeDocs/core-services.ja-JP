---
description: Adobe Experience Cloud ファーストパーティ cookie で使用するセキュア証明書を設定する方法について説明します。
solution: Experience Cloud,Analytics
title: Adobe管理証明書プログラム
index: y
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 2691f0dc91e48a8f817467e334d9028f2e506e70
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 11%

---

# Adobe管理証明書プログラム

Adobe管理証明書プログラムは、CNAME 実装に必要なファーストパーティ証明書を設定するための推奨プロセスです。 設定が完了すると、プログラムは完全に自動化されます。 証明書をタイムリーに更新するので、証明書の有効期限が切れていることが原因でデータ収集に影響を与えません。 プログラムは、最初の 100 個の CNAME に対して無料です。

現在、独自の証明書を管理している場合、ファーストパーティ cookie で使用するための証明書を購入、管理およびAdobeに提供する責任があります。 Adobeが管理する証明書プログラムへの移行については、Adobeのカスタマーケアにお問い合わせください。

## 実装

次の手順に従って、ファーストパーティデータ収集用の新しい証明書を実装します。

1. をダウンロードして入力します [ファーストパーティドメインリクエストフォーム](cookies/assets/First_Party_Domain_Request_Form.xlsx)

1. Adobeカスタマーケアに対して、Adobe管理証明書プログラムでのファーストパーティデータ収集の設定をリクエストするチケットを開きます。

1. チケットを受け取ると、Adobe担当者から CNAME レコードが提供されます。 これらのレコードは、アドビが代理で証明書を購入する前に、会社の DNS サーバーで設定される必要があります。例：ホスト名 `data.example.com` 参照先 `hiodsibxvip01.data.adobedc.net`.

1. CNAME レコードが組織のサーバーに配置されている場合、Adobeは DigiCert と連携して証明書を購入し、Adobeのデータ収集サーバーにインストールします。

## ホスト名転送の検証 {#validate}

Adobeが証明書をインストールしたら、次のいずれかの方法を使用して証明書が機能していることを検証できます。

+++**ブラウザーの検証**

任意のブラウザーを使用して、証明書が正しくインストールされていることを検証できます。 CNAME をに入力します `_check` をアドレスバーへのパスとして使用します。 例：

`data.example.com/_check`

すべてが機能すると、ブラウザーが表示されます `SUCCESS`. 証明書が正しくインストールされていない場合は、セキュリティ警告が表示されます。

+++

+++**コマンドライン （`curl`）**

ほとんどの最新のオペレーティングシステムには、既にが含まれています [`curl`](https://curl.se) インストールされています。

コマンドラインに以下を入力します。

```sh
curl data.example.com/_check
```

すべてが正しく動作した場合、コンソールはを返します `SUCCESS`.

>[!TIP]
>
>を使用できます `-k` トラブルシューティングに役立つようにセキュリティ警告を無効にするフラグ。

+++

+++**コマンドライン （`nslookup`）**

コマンドラインに以下を入力します。

```sh
nslookup data.example.com
```

すべてが正しく動作した場合、Adobeのデータ収集サーバーが返されます。

```text
Server: hiodsibxvip01.corp.adobe.com
Address: 10.50.112.247

Name: example.com.ssl.d1.sc.omtrdc.net
Addresses: 63.140.37.126
    63.140.37.206
    63.140.36.51
    63.140.36.145
Aliases: smetrics.example.com
```

+++

## 実装コードの更新 {#update}

証明書が正しく動作することを検証したら、これらの値を使用するようにAdobe実装を更新できます。

* Adobe Analytics AppMeasurement実装の場合は、を更新します [`trackingServer`](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/config-vars/trackingserver) 設定変数。 既存の実装がある場合は、を参照してください。 [訪問者の移行](https://experienceleague.adobe.com/en/docs/analytics/technotes/visitor-migration) 既存の訪問者が新規訪問者としてカウントされないようにする方法に関する追加手順について説明します。
* Web SDK 実装の場合は、を更新します [`edgeDomain`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/edgedomain) 内のプロパティ [`configure`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) コマンド。

## 保守および更新

ファーストパーティ証明書の有効期限が切れる 30 日前に、Adobeは CNAME がまだ有効で使用中かどうかを検証します。 その場合、Adobeはサービスを引き続き使用するものと見なし、ユーザーに代わって自動的に証明書を更新します。

>[!IMPORTANT]
>
>組織の CNAME レコードが削除されているか、指定されたAdobeで保護されたホスト名にマッピングされなくなった場合、Adobeは証明書を更新できません。 Adobeのシステム内のエントリは、それ以上の通信を行わずに削除対象としてマークされます。

## よくある質問

+++このプロセスは安全ですか？

はい。Adobeが管理する証明書プログラムは、Adobeに証明書を提供する組織よりも安全です。 証明書または秘密キーは、Adobeおよび発行元の証明機関の外部で変更されません。

+++

+++ドメイン用の証明書をAdobeはどのようにしたら購入できますか？

証明書は、指定したホスト名がAdobeが所有するホスト名を指している場合にのみ購入できます。 このホスト名は基本的にAdobeにデリゲートされ、Adobeが代理で証明書を購入できるようになります。

+++

+++証明書の失効をリクエストできますか？

はい。ドメインの所有者は、証明書の失効をリクエストする権利があります。 このプロセスを開始するには、Adobeカスタマーケアにお問い合わせください。

+++

+++使用する暗号化タイプを教えてください。

Adobeは DigiCert と連携して SHA-2 証明書を発行します。

+++

+++このプログラムには追加費用がかかりますか？

いいえ。Adobeは、すべてのAdobe Experience Cloudのお客様に、このサービスを追加費用なしで提供します。

+++

+++Adobeでは、どのような暗号セキュリティレベルを提供していますか？

アドビでは、2 種類の暗号セキュリティレベルを提供し、ファーストパーティのデータ収集におけるセキュリティに関するお客様の様々なニーズに対応しています。これらのレベルにより、Adobeサーバーを使用した HTTPS 接続に対してサポートされる暗号化アルゴリズムが決まります。 Adobeは、現在のセキュリティ対策に基づいて、サポートされるアルゴリズムのセットを定期的にレビューおよび更新しています。 暗号セキュリティ設定を変更したい場合は、カスタマーケアへのお問い合わせ。

* **標準** tls 1.2 以降および少なくとも 128 ビットの暗号化が必要です。 安全な暗号化を維持しながら、最も広いデバイス互換性を提供するように設計されています。
* **高** 暗号セキュリティレベルには TLS 1.2 以降が必要で、より弱い暗号のサポートが削除されます。 最も強力な暗号化を求め、古いデバイスのサポートを気にしないお客様向けに設計されています。

次のクライアントは、に設定された暗号セキュリティで接続できないことがわかっています。 **高**:

* Windows 8.1 以前（最終更新は 2018年）
* Windows Phone 8.1 以前（最終更新は 2016年）
* OS X 10.10 以前（最終更新は 2017年）
* iOS 8.4 以前（最終更新は 2015年）

+++

+++サポートされている HTTPS 証明書の種類は何ですか？

Adobeは、RSA 証明書と ECC 証明書の両方をサポートし、お客様の多様なニーズに対応します。 RSA 証明書はクライアントに対してより広くサポートされていますが、ECC 証明書はサーバ側とクライアント側の両方で処理が少なくて済みます。 Adobeが管理する証明書の場合は、RSA と ECC の両方が提供されます。 お客様が管理する証明書の場合は、RSA と ECC の両方をお勧めします。 最新のクライアントは、RSA と ECC の両方をサポートしています。 次のクライアントは、通常、RSA 証明書のみをサポートします。

* Windows Vista 以前（最終更新は 2012 年）
* Windows Phone 8.0 以前（最終更新は 2014年）
* OS X 10.8 以前（最終更新は 2013年）
* iOS 5.1 以前（最終更新は 2012年）
* Android 4.3 以前（最終更新は 2013 年）

+++
