---
description: Adobe Analytics では Cookie を使用して、イメージリクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供します。
solution: Experience Cloud,Analytics
title: "ファーストパーティ cookie "
index: y
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 0e4bf07a15c4601b3e6278a57880920710a69a79
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 79%

---

# ファーストパーティ cookie について

Analytics は、イメージリクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供するために、cookie を使用します。アドビでは、可能な限りファーストパーティ cookie を使用してサイト上のアクティビティを記録します。所有している他のドメインなど、異なるサイトでのアクティビティを記録するには、サードパーティ cookieが必要です。

多くのブラウザーやスパイウェア駆除アプリケーションは、サードパーティ Cookie を拒否し、削除するように設計されています。アドビは、サードパーティ Cookie がブロックされた場合でも Cookie を常に設定できるようにします。具体的な動作は、Experience PlatformID サービス（ECID サービス）を使用しているか、Analytics の従来の識別子（s_vi Cookie とも呼ばれます）を使用しているかによって異なります。

* [Experience Platform ID サービス（ECID サービス）](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=ja) は、収集ドメインがサイトドメインと一致するかどうかに関係なく、自動的にファーストパーティ Cookie を設定します。一致しない場合、ID サービスは JavaScript を使用してサイトのドメインに Cookie を設定します。
* [Analytics の従来の識別子](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html?lang=ja)（別名 `s_vi` cookie）を使用している場合、データ収集サーバーの設定方法によってどちらを使用するかは異なります。データ収集サーバーがサイトのドメインと一致する場合、Cookie はファーストパーティとして設定されます。収集サーバーが現在のドメインと一致しない場合、Cookie はサードパーティとして設定されます。この場合、サードパーティ Cookie がブロックされていると、Analytics は、標準の「s_vi」Cookie ではなく、ファーストパーティ [フォールバック ID（s_fid）](cookies-analytics.md) を設定します。

収集サーバーがサイトのドメインと一致するようにするには、CNAME 実装を使用して、CNAME 実装で指定されたカスタムドメインからAdobeの収集サーバーへの転送を有効にします。 この際、会社の DNS 設定を変更し、アドビがホストするドメインを指すよう CNAME エイリアスを設定します。各種のアドビ製品では CNAME の使用をサポートしていますが、どの場合でも、CNAME は、特定の顧客用の信頼できるファーストパーティエンドポイントを作成するために使用され、その顧客に所有されることに注意してください。複数のドメインを制御する場合、1 つの CNAME エンドポイントを使用して複数のドメインをまたいだユーザーを追跡できます。ただし、サイトドメインが CNAME と一致しない場合は、ドメイン Cookie はサードパーティとして設定されます。

>[!NOTE]
>
>Appleの Intelligent Tracking Prevention(ITP) プログラムでは、Adobeが設定したファーストパーティ Cookie が、macOSの Safari とiOSおよび iPadOS のすべてのブラウザーを含む ITP で管理されるブラウザーで短時間有効になります。 2020年11月以降、CNAME を使用して設定された Cookie も、JavaScript を使用して設定された Cookie と同じ有効期限を持ちます。この有効期限は変更される可能性があります。

データ収集用の CNAME を確立する場合で、サイトに HTTPS プロトコルを使用したセキュリティで保護されたページがある場合は、アドビと協力して SSL 証明書を取得できます。

SSL 証明書の発行プロセスは、多くの場合、わかりにくく、時間がかかる可能性があります。結果として、アドビは、業界最先端の証明機関（CA）である DigiCert とのパートナーシップを構築し、これらの証明書の購入や管理を自動化する統合プロセスを開発しました。

アドビではお客様の許可を得て、CA と連携し、お客様用に新しい SHA-2 SSL 証明書を発行、デプロイ、および管理します。アドビは証明書を継続的に管理し、予期しない期限切れ、失効またはセキュリティ上の問題によって、組織の安全な収集の可用性が脅かされないようにします。

## Adobe 管理証明書プログラム

Adobe 管理証明書プログラムは、Adobe 収集サーバーがサイトドメインと一致するように、CNAME 実装に必要なファーストパーティ SSL 証明書を設定するための推奨プロセスです。

Adobe 管理証明書プログラム を利用すると、新しいファーストパーティ SSL 証明書を追加費用なしで実装できます（最初の 100 個の CNAME）。現在、お客様が管理する独自の SSL 証明書がある場合、Adobe Managed Certificate Program への移行についてアドビカスタマーケアにお問い合わせください。

### 実装

次に、ファーストパーティデータ収集用の新しいファーストパーティ SSL 証明書を実装する方法を示します。

1. [ファーストパーティドメインリクエストフォーム](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx) に入力して、カスタマーケアでチケットを開き、Adobe Managed プログラムでファーストパーティデータ収集の設定をリクエストします。

   例が記載されたフォーム内の各フィールドに記入します。

1. CNAME レコードを作成します（以下の手順を参照）。

   チケットを受け取ったら、カスタマーケアの担当者から CNAME レコードが提供されます。これらのレコードは、アドビが代理で証明書を購入する前に、会社の DNS サーバーで設定される必要があります。CNAME は次のようになります。

   **セキュアの場合** - 例えば、ホスト名 `smetrics.example.com` が `[random-10-character-string].data.adobedc.net` を指します。

   >[!NOTE]
   > 以前は、Adobeでは、顧客が HTTPS と HTTP の 2 つの CNAME を設定することをお勧めしていました。 トラフィックの暗号化はベストプラクティスであり、ほとんどのブラウザーでは HTTP を強く推奨しないので、HTTP 用に CNAME を設定することはお勧めしません。 現在は、ベストプラクティスとして、 `trackingServer` および `trackingServerSecure` が同じ CNAME に設定されている。 例えば、 `trackingServer` および `trackingServerSecure` は次のように設定されます。 `smetrics.example.com`. HTTP は、サードパーティのホスト名に対してのみ使用できます。

1. CNAME が設定されると、アドビは DigiCert と連携して証明書を購入し、アドビの実稼動サーバーにインストールします。

   既存の実装がある場合、既存の訪問者を維持するために、訪問者の移行を検討する必要があります。証明書がAdobeの実稼動環境にプッシュされてライブになったら、トラッキングサーバー変数を新しいホスト名に更新できます。 つまり、サイトがセキュアでない場合（HTTP）、`s.trackingServer` を更新します。サイトがセキュアな場合（HTTPS）、`s.trackingServer` と `s.trackingServerSecure` の両方の変数を更新します。

1. [ホスト名転送の検証](#validate)をおこないます（以下を参照）。

1. [実装コードの更新](#update)をおこないます（以下を参照）。

### メンテナンスと更新

ファーストパーティ証明書の有効期限が切れる 30 日前に、Adobeは CNAME がまだ有効で使用中かどうかを検証します。 その場合、Adobeは、お客様が引き続きサービスを使用し、お客様に代わって証明書を自動的に更新すると想定しています。

>[!NOTE]
> CNAME が削除されたか、無効になった場合 ( または提供されたAdobeの SSL ホスト名にマッピングされない場合 )、Adobeは証明書を更新できず、システム内のエントリはそれ以上の通信がない限り削除用にマークされます。

### よくある質問

| 質問 | 回答 |
|---|---|
| **このアイテムは保護されていますか？** | はい、アドビおよび発行する証明機関の外部で証明書や秘密鍵が変更されることがないので、Adobe Managed プログラムは、従来の方法よりも安全です。 |
| **ドメイン用の証明書をアドビはどのようにしたら購入できますか？** | 証明書は、特定のホスト名（例えば、`telemetry.example.com`）がアドビが所有するホスト名を指すようにお客様が指定する際にのみ、購入できます。これは、基本的に、このホスト名をアドビに委任し、アドビが代理で証明書を購入することを許可するということです。 |
| **証明書の失効を要求できますか？** | はい、ドメインの所有者として、証明書の失効を要求する権限があります。 チケットを開き、カスタマーケアにこれを完了してもらう必要があります。 |
| **この証明書は SHA-2 暗号化を使用しますか？** | はい、Adobeは DigiCert と連携して SHA-2 証明書を発行します。 |
| **追加費用が発生しますか？** | いいえ、アドビは、このサービスを Adobe Digital Experience の現在のすべてのお客様に追加費用なしで提供しています。 |

{style=&quot;table-layout:auto&quot;}

## CNAME レコードの作成

組織のネットワークオペレーションチームは、CNAME レコードを作成することで、DNS サーバーを設定する必要があります。各ホスト名は、アドビのデータ収集サーバーにデータを転送します。

FPC スペシャリストから、設定されたホスト名と、ホスト名で指定する必要のある CNAME が提供されます。以下に例を示します。

* **SSL ホスト名**： `smetrics.mysite.com`
* **SSL CNAME**：`[random-10-character-string].data.adobedc.net`

>[!NOTE]
> それでも非セキュアを使用する場合は、次のようになります。 
> * **非 SSL ホスト名**： `metrics.mysite.com`
> * **非 SSL CNAME**： `[random-10-character-string].data.adobedc.net`


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

`nslookup` を使用して検証できます。例えば、`smetrics.adobe.com`を使用する場合は、コマンドプロンプトを開き、`nslookup smetrics.adobe.com` と入力します。

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

サイトのコードを編集してファーストパーティデータ収集を使用できるようにする前に、次の前提条件を満たします。

* [Adobe Managed Certificate Program](#adobe-managed-certificate-program) の&#x200B;*実装方法*&#x200B;の節で説明した手順に従って、SSL 証明書を要求します。
* CNAME レコードを作成します（上記を参照）。
* ホスト名を検証します（上記を参照）。

ホスト名がアドビのデータ収集サーバーに応答し、転送することを確認したら、実装を変更して独自のデータ収集ホスト名を指定できます。

1. コア JavaScript ファイル（`s_code.js/AppMeasurement.js`）を開きます。
1. コードバージョンを更新する場合は、`s_code.js/AppMeasurement.js` ファイル全体を新しいバージョンに置き換え、すべてのプラグインやカスタマイズ（作成した場合）を置き換えます。**または**、ファーストパーティデータ収集のみに関連するコードを更新するには、s.trackingServer および s.trackingServerSecure 変数（SSL 使用時）を探し、新しいデータ収集ホスト名を指定します。mysite.com を使用すると、`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"` のようになります。

1. 更新したコア JavaScript ファイルをサイトにアップロードします。

1. 長期にわたる実装からファーストパーティデータ収集に移動する場合、または異なるファーストパーティ収集ホスト名に変更する場合、アドビは以前のドメインから新しいドメインに訪問者を移行することをお勧めします。

詳しくは、Analytics 導入ガイドの [訪問者の移行](https://experienceleague.adobe.com/docs/analytics/technotes/visitor-migration.html?lang=ja) を参照してください。

コア JavaScript ファイルをアップロードすると、ファーストパーティ によるデータ収集用の設定がすべておこなわれます。アドビは、アップロード後の数時間は Analytics レポートを監視し、通常どおりデータ収集がおこなわれているかを確認することをお勧めします。通常どおりおこなわれていない場合、上記のすべての手順が完了していることを確認し、組織のサポート対象ユーザーの中からカスタマーケアにお問い合わせください。
