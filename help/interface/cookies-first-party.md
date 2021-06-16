---
description: Adobe Analytics では Cookie を使用して、イメージリクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供します。
keywords: cookie;プライバシー
solution: Experience Cloud,Analytics
title: '"ファーストパーティ cookie "'
index: y
snippet: y
feature: Cookie
topic: 管理
role: Administrator
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 145040facf70c6bde5c6c3fae9c7ed7f520c188d
workflow-type: tm+mt
source-wordcount: '1579'
ht-degree: 60%

---

# ファーストパーティ cookie について

Analytics は、イメージリクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供するために、cookie を使用します。アドビでは、可能な限りファーストパーティ cookie を使用してサイト上のアクティビティを記録します。所有している他のドメインなど、異なるサイトでのアクティビティを記録するには、サードパーティ cookieが必要です。

多くのブラウザーやスパイウェア駆除アプリケーションは、[!DNL Analytics]データ収集で使用されるcookieを含め、サードパーティcookieを拒否および削除するように設計されています。 訪問者が Web サイトとどのようにやり取りするかを追跡できるようにするには、データ収集でファーストパーティ cookie を使用するよう設定する必要があります。

ファーストパーティ cookie を実装する方法としては、次の 2 つの選択肢があります。

* Experience PlatformIDサービス（ECIDサービス）を使用している場合、JavaScriptを使用してファーストパーティコンテキストにCookieが自動的に設定されます。
* 従来の[!DNL Analytics]識別子（`s_vi` Cookieとも呼ばれます）を使用している場合は、データ収集サーバーの設定方法によって異なります。 データ収集サーバーがサイトのドメインと一致する場合、Cookieはファーストパーティとして設定されます。 収集サーバーが現在のドメインと一致しない場合、Cookieはサードパーティとして設定されます。 この場合、サードパーティCookieがブロックされると、[!DNL Analytics]は標準の「s_vi」Cookieではなくファーストパーティ[フォールバックID(s_fid)](cookies-analytics.md)を設定します。

収集サーバーがサイトのドメインと一致するように、CNAME実装を使用して、cookieをファーストパーティコンテキストで設定できます。 この際、会社の DNS 設定を変更し、アドビがホストするドメインを指すよう CNAME エイリアスを設定します。各種のアドビ製品では CNAME の使用をサポートしていますが、どの場合でも、CNAME は、特定の顧客用の信頼できるファーストパーティエンドポイントを作成するために使用され、その顧客に所有されることに注意してください。複数のドメインを制御する場合、1つのCNAMEエンドポイントを使用して複数のドメインでユーザーを追跡できますが、サイトドメインがCNAMEドメインcookieと一致しない場合は、どこでもサードパーティとして設定されます。

>[!NOTE]
>
>AppleのIntelligent Tracking Prevention(ITP)プログラムでは、どちらのオプションでも、ITPで管理されるブラウザー（macOSのSafariとiOSおよびiPadOSのすべてのブラウザーを含む）でファーストパーティCookieを短時間のみ有効にします。 2020 年 11 月現在、両方のタイプの Cookie は有効期限が 7 日間です。この有効期限は変更される可能性があります。

CNAME を使用する 2 番目の方法では、HTTPS プロトコルを使用したセキュリティで保護されているページがサイトにある場合は、アドビと協力して SSL 証明書を取得し、ファーストパーティ cookie を実装することができます。Adobeでは、Adobeが2020年後半にHTTP収集のサポートを終了するので、データ収集にはHTTPSのみを使用することを強くお勧めします。

SSL 証明書の発行プロセスは、多くの場合、わかりにくく、時間がかかる可能性があります。その結果、Adobeは業界をリードする認証局(CA)であるDigiCertとの提携を結び、これらの証明書の購入と管理を自動化する統合プロセスを開発しました。

お客様の許可を得て、アドビはCAと連携し、新しいSHA-2 SSL証明書の発行、デプロイ、および管理をおこないます。 Adobeはこの証明書を引き続き管理し、予期しない期限切れ、失効またはセキュリティ上の問題によって組織のセキュリティで保護された収集の可用性が脅かされないようにします。

## Adobe管理証明書プログラム

Adobe Managed Certificate Program は、ファーストパーティ cookie 用の新しいファーストパーティ SSL 証明書の実装にお勧めのプロセスです。

Adobe Managed Certificate Program を利用すると、ファーストパーティ cookie 用の新しいファーストパーティ SSL 証明書を追加費用なしで実装できます（最初の 100 個の CNAME）。現在、お客様が管理する独自のSSL証明書がある場合は、Adobeが管理する証明書プログラムへの移行について、Adobeカスタマーケアにお問い合わせください。

### 実装方法

次に、ファーストパーティ Cookie 用の新しいファーストパーティ SSL 証明書を実装する方法を示します。

1. [ファーストパーティcookieリクエストフォーム](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx)に入力し、Adobe管理プログラムでファーストパーティcookieの設定をカスタマーケアに依頼して、チケットを開きます。 例が記載されたフォーム内の各フィールドに記入します。

2. CNAME レコードを作成します（以下の手順を参照）。

   チケットを受け取ったら、カスタマーケアの担当者から CNAME レコードが提供されます。これらのレコードは、アドビが代理で証明書を購入する前に、会社の DNS サーバーで設定される必要があります。CNAMEは次のようになります。

   **セキュアの場合** - 例えば、ホスト名 `smetrics.example.com` が `example.com.adobedc.net` を指します。

>[!NOTE]
> 以前は、Adobeでは、HTTPS用とHTTP用に2つのCNAMEを設定することをお勧めします。 トラフィックの暗号化はベストプラクティスであり、ほとんどのブラウザーでは HTTP をできるだけ避けるべきとしているため、CNAME を HTTP 用に設定することはお勧めしません。必要に応じて、次のようになります。
>    **非セキュアの場合** - ホスト名 `metrics.example.com` は `example.com.adobedc.net` を指します。

1. CNAMEが設定されると、AdobeはDigiCertと連携して証明書を購入し、Adobeの実稼動サーバーにインストールします。

   既存の実装がある場合、既存の訪問者を維持するために、訪問者の移行を検討する必要があります。証明書がアドビの実稼動環境にプッシュされてライブになると、トラッキングサーバー変数を新しいホスト名に更新できます。つまり、サイトがセキュアでない場合（HTTP）、`s.trackingServer` を更新します。サイトがセキュアな場合（HTTPS）、`s.trackingServer` と `s.trackingServerSecure` の両方の変数を更新します。

2. [ホスト名転送の検証](#validate)をおこないます（以下を参照）。

3. [実装コードの更新](#update)をおこないます（以下を参照）。

### メンテナンスと更新

SSL 証明書は毎年期限が切れます。つまり、アドビは毎年、各実装用に新しい証明書を購入する必要があります。組織内のすべてのサポート対象ユーザーは、実装の有効期限が近づくたびに電子メール通知を受け取ります。 アドビがお客様のホスト名を更新するには、1 人のサポート対象ユーザーがアドビからの電子メールに返信して、引き続き期限が切れるホスト名をデータ収集に使用する計画であると示す必要があります。その時点で、アドビは自動的に新しい証明書を購入およびインストールします。

### よくある質問

| 質問 | 回答 |
|---|---|
| **このアイテムは保護されていますか？** | はい、Adobe管理プログラムは、Adobeや発行する証明機関の外部で証明書や秘密鍵が変更されないので、従来の方法よりも安全です。 |
| **ドメイン用の証明書をアドビはどのようにしたら購入できますか？** | 証明書は、特定のホスト名（例えば、`telemetry.example.com`）がアドビが所有するホスト名を指すようにお客様が指定する際にのみ、購入できます。これは、基本的に、このホスト名をアドビに委任し、アドビが代理で証明書を購入することを許可するということです。 |
| **証明書の失効を要求できますか？** | はい、ドメインの所有者として、お客様はアドビに証明書の失効を要求する資格があります。必要なのは、チケットを開いてカスタマーケアにこれの実行を依頼するだけです。 |
| **この証明書は SHA-2 暗号化を使用しますか？** | はい、アドビは DigiCert と連携して SHA-2 証明書を発行します。 |
| **追加費用が発生しますか？** | いいえ、アドビは、このサービスを Adobe Digital Experience の現在のすべてのお客様に追加費用なしで提供しています。 |

{style=&quot;table-layout:auto&quot;}

## CNAME レコードの作成

組織のネットワークオペレーションチームは、CNAMEレコードを作成してDNSサーバーを設定する必要があります。 各ホスト名は、アドビのデータ収集サーバーにデータを転送します。

FPC スペシャリストから、設定されたホスト名と、ホスト名で指定する必要のある CNAME が提供されます。以下に例を示します。

* **SSL ホスト名**： `smetrics.mysite.com`
* **SSL CNAME**：`mysite.com.adobedc.net`

>[!NOTE]
> まだセキュアでないを使用している場合、次のようになります。
> * **非 SSL ホスト名**： `metrics.mysite.com`
> * **非 SSL CNAME**： `mysite.com.adobedc.net`


実装コードが変更されない限り、この手順がデータ収集に影響を及ぼすことはなく、実装コードの更新後はいつでもおこなうことができます。

>[!NOTE]
>
>Experience Cloud 訪問者 ID サービスは、ファーストパーティ Cookie を有効にするために、CNAME を設定するための代替手段を提供します。

## ホスト名転送の検証 {#validate}

検証に使用できる方法は次のとおりです。

### ブラウザーを使用した検証

CNAME が設定され、証明書がインストールされている場合は、ブラウザーを使用して次のように検証することができます。

`https://smetrics.adobe.com/_check`

>[!NOTE]
>
>証明書がインストールされていない場合は、セキュリティ警告が表示されます。

### [!DNL curl] を使用した検証

コマンドラインから [[!DNL curl]](https://curl.se/) を使用することをお勧めします。（[!DNL Windows] ユーザーは <https://curl.se/windows/> から [!DNL curl] をインストールできます）。

CNAME が設定されていても、証明書がインストールされていない場合は、`curl -k https://smetrics.adobe.com/_check` を実行します。応答は `SUCCESS` となります。

（この `-k` 値を指定すると、セキュリティ警告が無効になります）

CNAME が設定されていて、証明書がインストールされている場合は、`curl https://smetrics.adobe.com/_check` を実行します。応答は `SUCCESS` となります。

### [!DNL nslookup] を使用した検証

`nslookup` を使用して検証できます。例えば、`smetrics.adobe.com` を使用する場合は、コマンドプロンプトを開き、`nslookup smetrics.adobe.com` と入力します。

すべてが正常に設定された場合は、次のような応答が表示されます。

```
nslookup smetrics.adobe.com
Server:             10.30.7.247
Address:     10.30.7.247#53

smetrics.adobe.com    canonical name = adobe.com.ssl.d1.sc.omtrdc.net.
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.218.180.161
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 52.39.8.230
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.187.216.46
```

## 実装コードの更新 {#update}

ファーストパーティcookieを使用するようにサイトのコードを編集する前に、次の前提条件を満たします。

* [Adobe管理証明書プログラム](#adobe-managed-certificate-program)の&#x200B;*実装*&#x200B;の節で説明した手順に従って、SSL証明書を要求します。
* CNAME レコードを作成します（上記を参照）。
* ホスト名を検証します（上記を参照）。

ホスト名がAdobeのデータ収集サーバーに応答し、転送することを確認したら、実装を変更して独自のデータ収集ホスト名を指定できます。

1. コア JavaScript ファイル（`s_code.js/AppMeasurement.js`）を開きます。
1. コードバージョンを更新する場合は、`s_code.js/AppMeasurement.js` ファイル全体を新しいバージョンに置き換え、すべてのプラグインやカスタマイズ（作成した場合）を置き換えます。**または**、ファーストパーティ cookie のみに関連するコードを更新するには、s.trackingServer および s.trackingServerSecure 変数（SSL 使用時）を探し、新しいデータ収集ホスト名を指定します。mysite.com を使用すると、`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"` のようになります。

1. 更新したコア JavaScript ファイルをサイトにアップロードします。

1. 長期にわたる実装からファーストパーティcookieに移行する場合、または別のファーストパーティ収集ホスト名に変更する場合は、以前のドメインから新しいドメインに訪問者を移行することをAdobeにお勧めします。

詳しくは、Analytics 導入ガイドの[訪問者の移行](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/visitor-migration.html?lang=en)を参照してください。

コア JavaScript ファイルをアップロードすると、ファーストパーティ cookie によるデータ収集用の設定がすべておこなわれます。Adobeでは、次の数時間、Analyticsレポートを監視して、データ収集が通常どおり続くことを確認することをお勧めします。 通常どおりおこなわれていない場合、上記のすべての手順が完了していることを確認し、組織のサポート対象ユーザーの中からカスタマーケアにお問い合わせください。
