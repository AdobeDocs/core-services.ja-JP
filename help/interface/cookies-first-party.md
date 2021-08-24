---
description: Adobe Analytics では Cookie を使用して、イメージリクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供します。
keywords: cookie;プライバシー
solution: Experience Cloud,Analytics
title: '"ファーストパーティ cookie "'
index: y
snippet: y
feature: Cookie
topic: 管理
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 9a232162008524d900e3655716a84961c287c773
workflow-type: tm+mt
source-wordcount: '1617'
ht-degree: 71%

---

# ファーストパーティ cookie について

Analytics は、イメージリクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供するために、cookie を使用します。アドビでは、可能な限りファーストパーティ cookie を使用してサイト上のアクティビティを記録します。所有している他のドメインなど、異なるサイトでのアクティビティを記録するには、サードパーティ cookieが必要です。

多くのブラウザーやスパイウェア駆除アプリケーションは、サードパーティcookieを拒否し、削除するように設計されています。 Adobeは、サードパーティCookieがブロックされた場合でもCookieを常に設定できるようにします。 具体的な動作は、Experience PlatformIDサービス（ECIDサービス）とAnalyticsの従来の識別子（s_vi Cookieとも呼ばれます）のどちらを使用しているかによって異なります。

* [Experience PlatformIDサービス（ECIDサービス）](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=ja)は、収集ドメインがサイトドメインと一致するかどうかに関係なく、自動的にファーストパーティCookieを設定します。 一致しない場合、IDサービスはJavaScriptを使用してサイトのドメインにCookieを設定します。
* [Analyticsの従来の識別子](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html?lang=en)（別名`s_vi` Cookie）を使用している場合は、データ収集サーバーの設定方法によって異なります。 データ収集サーバーがサイトのドメインと一致する場合、Cookie はファーストパーティとして設定されます。収集サーバーが現在のドメインと一致しない場合、Cookie はサードパーティとして設定されます。この場合、サードパーティCookieがブロックされると、Analyticsは、標準の「s_vi」Cookieの代わりにファーストパーティ[フォールバックID(s_fid)](cookies-analytics.md)を設定します。

収集サーバーがサイトのドメインと一致するようにする場合は、CNAME実装を使用して、CNAME実装で指定されたカスタムドメインからAdobeの収集サーバーへの転送を有効にできます。 これには、会社のDNS設定に対する変更が含まれ、ドメインがホストするドメインを指すようにCNAMEエイリアスをAdobeします。 各種のアドビ製品では CNAME の使用をサポートしていますが、どの場合でも、CNAME は、特定の顧客用の信頼できるファーストパーティエンドポイントを作成するために使用され、その顧客に所有されることに注意してください。複数のドメインを制御する場合、1 つの CNAME エンドポイントを使用して複数のドメインをまたいだユーザーを追跡できます。ただし、サイトドメインが CNAME と一致しない場合は、ドメイン Cookie はサードパーティとして設定されます。

>[!NOTE]
>
>収集ドメインがサイトドメインと一致するかどうかに関係なく、AppleのIntelligent Tracking Prevention(ITP)プログラムは、ITPで管理されるブラウザー（macOSのSafariとiOSおよびiPadOSのすべてのブラウザーを含む）でアドビが設定したファーストパーティCookieを短時間有効にします。 2020年11月以降、CNAMEを使用して設定されたcookieも、JavaScriptを使用して設定されたcookieと同じ有効期限を持ちます。 この有効期限は変更される可能性があります。

データ収集用のCNAMEを確立したい場合で、サイトにHTTPSプロトコルを使用したセキュリティで保護されたページがある場合は、Adobeと協力してSSL証明書を取得できます。

SSL 証明書の発行プロセスは、多くの場合、わかりにくく、時間がかかる可能性があります。結果として、アドビは、業界最先端の証明機関（CA）である DigiCert とのパートナーシップを構築し、これらの証明書の購入や管理を自動化する統合プロセスを開発しました。

アドビではお客様の許可を得て、CA と連携し、お客様用に新しい SHA-2 SSL 証明書を発行、デプロイ、および管理します。アドビは証明書を継続的に管理し、予期しない期限切れ、失効またはセキュリティ上の問題によって、組織の安全な収集の可用性が脅かされないようにします。

## Adobe 管理証明書プログラム

Adobe管理証明書プログラムは、Adobe収集サーバーがサイトドメインと一致するように、CNAME実装に必要なファーストパーティSSL証明書を設定するための推奨プロセスです。

Adobe管理証明書プログラムを使用すると、新しいファーストパーティSSL証明書を追加費用なしで実装できます（最初の100個のCNAME）。 現在、お客様が管理する独自の SSL 証明書がある場合、Adobe Managed Certificate Program への移行についてアドビカスタマーケアにお問い合わせください。

### 実装方法

次に、ファーストパーティデータ収集用の新しいファーストパーティSSL証明書の実装方法を示します。

1. [ファーストパーティAdobeリクエストフォーム](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx)に入力し、カスタマーケアに連絡して、ドメイン管理プログラムでファーストパーティデータ収集の設定をリクエストするチケットを開きます。 例が記載されたフォーム内の各フィールドに記入します。

2. CNAME レコードを作成します（以下の手順を参照）。

   チケットを受け取ったら、カスタマーケアの担当者から CNAME レコードが提供されます。これらのレコードは、アドビが代理で証明書を購入する前に、会社の DNS サーバーで設定される必要があります。CNAME は次のようになります。

   **セキュアの場合** - 例えば、ホスト名 `smetrics.example.com` が `example.com.adobedc.net` を指します。

>[!NOTE]
> 以前、アドビでは、HTTPS 用と HTTP 用の 2 つの CNAME を設定することをお勧めしていました。トラフィックの暗号化はベストプラクティスであり、ほとんどのブラウザーでは HTTP をできるだけ避けるべきとしているため、CNAME を HTTP 用に設定することはお勧めしません。必要に応じて、次のようになります。
>    **非セキュアの場合** - ホスト名 `metrics.example.com` は `example.com.adobedc.net` を指します。

1. CNAME が設定されると、アドビは DigiCert と連携して証明書を購入し、アドビの実稼動サーバーにインストールします。

   既存の実装がある場合、既存の訪問者を維持するために、訪問者の移行を検討する必要があります。証明書がアドビの実稼動環境にプッシュされてライブになると、トラッキングサーバー変数を新しいホスト名に更新できます。つまり、サイトがセキュアでない場合（HTTP）、`s.trackingServer` を更新します。サイトがセキュアな場合（HTTPS）、`s.trackingServer` と `s.trackingServerSecure` の両方の変数を更新します。

2. [ホスト名転送の検証](#validate)をおこないます（以下を参照）。

3. [実装コードの更新](#update)をおこないます（以下を参照）。

### メンテナンスと更新

SSL 証明書は毎年期限が切れます。つまり、アドビは毎年、各実装用に新しい証明書を購入する必要があります。組織内のすべてのサポート対象ユーザーは、実装の有効期限が近づくたびに電子メール通知を受け取ります。アドビがお客様のホスト名を更新するには、1 人のサポート対象ユーザーがアドビからの電子メールに返信して、引き続き期限が切れるホスト名をデータ収集に使用する計画であると示す必要があります。その時点で、アドビは自動的に新しい証明書を購入およびインストールします。

### よくある質問

| 質問 | 回答 |
|---|---|
| **このアイテムは保護されていますか？** | はい、アドビおよび発行する証明機関の外部で証明書や秘密鍵が変更されることがないので、Adobe Managed プログラムは、従来の方法よりも安全です。 |
| **ドメイン用の証明書をアドビはどのようにしたら購入できますか？** | 証明書は、特定のホスト名（例えば、`telemetry.example.com`）がアドビが所有するホスト名を指すようにお客様が指定する際にのみ、購入できます。これは、基本的に、このホスト名をアドビに委任し、アドビが代理で証明書を購入することを許可するということです。 |
| **証明書の失効を要求できますか？** | はい、ドメインの所有者として、お客様はアドビに証明書の失効を要求する資格があります。必要なのは、チケットを開いてカスタマーケアにこれの実行を依頼するだけです。 |
| **この証明書は SHA-2 暗号化を使用しますか？** | はい、アドビは DigiCert と連携して SHA-2 証明書を発行します。 |
| **追加費用が発生しますか？** | いいえ、アドビは、このサービスを Adobe Digital Experience の現在のすべてのお客様に追加費用なしで提供しています。 |

{style=&quot;table-layout:auto&quot;}

## CNAME レコードの作成

組織のネットワークオペレーションチームは、CNAME レコードを作成することで、DNS サーバーを設定する必要があります。各ホスト名は、アドビのデータ収集サーバーにデータを転送します。

FPC スペシャリストから、設定されたホスト名と、ホスト名で指定する必要のある CNAME が提供されます。以下に例を示します。

* **SSL ホスト名**： `smetrics.mysite.com`
* **SSL CNAME**：`mysite.com.adobedc.net`

>[!NOTE]
> それでも非セキュアを使用する場合は、次のようになります。 
> * **非 SSL ホスト名**： `metrics.mysite.com`
> * **非 SSL CNAME**： `mysite.com.adobedc.net`


実装コードが変更されない限り、この手順がデータ収集に影響を及ぼすことはなく、実装コードの更新後はいつでもおこなうことができます。

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

すべてが正常に設定されている場合は、次のような応答が表示されます。

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

ファーストパーティデータ収集を使用するようにサイトのコードを編集する前に、次の前提条件を満たします。

* [Adobe Managed Certificate Program](#adobe-managed-certificate-program) の&#x200B;*実装方法*&#x200B;の節で説明した手順に従って、SSL 証明書を要求します。
* CNAME レコードを作成します（上記を参照）。
* ホスト名を検証します（上記を参照）。

ホスト名がアドビのデータ収集サーバーに応答し、転送することを確認したら、実装を変更して独自のデータ収集ホスト名を指定できます。

1. コア JavaScript ファイル（`s_code.js/AppMeasurement.js`）を開きます。
1. コードバージョンを更新する場合は、`s_code.js/AppMeasurement.js` ファイル全体を新しいバージョンに置き換え、すべてのプラグインやカスタマイズ（作成した場合）を置き換えます。**または、ファーストパーティのデータ収集にのみ関連するコードを更新する場合は、s.trackingServer変数とs.trackingServerSecure変数（SSLを使用する場合）を探し、新しいデータ収集ホスト名を指定します。** mysite.com を使用すると、`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"` のようになります。

1. 更新したコア JavaScript ファイルをサイトにアップロードします。

1. 長期にわたる実装からファーストパーティデータ収集に移行する場合、または別のファーストパーティ収集ホスト名に変更する場合は、以前のドメインから新しいドメインに訪問者を移行することをAdobeにお勧めします。

詳しくは、Analytics 導入ガイドの[訪問者の移行](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/visitor-migration.html?lang=ja)を参照してください。

コア JavaScript ファイルをアップロードすると、ファーストパーティ によるデータ収集用の設定がすべておこなわれます。アドビは、アップロード後の数時間は Analytics レポートを監視し、通常どおりデータ収集がおこなわれているかを確認することをお勧めします。通常どおりおこなわれていない場合、上記のすべての手順が完了していることを確認し、組織のサポート対象ユーザーの中からカスタマーケアにお問い合わせください。
