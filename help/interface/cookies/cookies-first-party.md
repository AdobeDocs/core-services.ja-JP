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
translation-type: tm+mt
source-git-commit: 4e3d6e605df4d1861f1dffb4cde5311eea283ee3
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ファーストパーティ cookie について

Analytics は、イメージリクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供するために、cookie を使用します。これらの安全な cookie は、アドビがホストするドメインから作成されるもので、サードパーティ cookie と呼ばれます。

ブラウザーやスパイウェア駆除アプリケーションの多くは、サードパーティ cookie を拒否し、削除するよう設計されています。この cookie には、Analytics のデータ収集で使用される cookie も含まれます。訪問者による Web サイトとのやり取りを追跡できるように、ファーストパーティ cookie を実装できます。

ファーストパーティ cookie を実装する方法としては、次の 2 つの選択肢があります。

* Experience Platform ID サービス。この ID サービスは、JavaScript を使用してファーストパーティコンテキストに cookie を設定できます。
* アドビがホストするドメインへの CNAME エイリアスを設定するための、会社の DNS サーバー上にある DNS エントリ。各種のアドビ製品では CNAME の使用をサポートしていますが、どの場合でも、CNAME は、特定の顧客用の信頼できるファーストパーティエンドポイントを作成するために使用され、その顧客に所有されることに注意してください。その顧客が複数のドメインを管理している場合、1 つの CNAME エンドポイントを使用して複数のドメインにわたってユーザーを追跡できますが、それをおこなうには CNAME ドメイン以外のすべてのドメインにサードパーティ cookie が必要なので、サードパーティ cookie がブロックされる場合は機能せず、したがって推奨されません。Adobe CNAME を使用して、様々な顧客に所有されているドメインで個人やデバイスを追跡することはありません。

>[!NOTE]
>
>どちらのオプションでも、Apple の Intelligent Tracking Prevention (ITP) プログラムでは、ITP に準拠するブラウザー（macOS の Safari や iOS および iPadOS のすべてのブラウザーを含む）で、ファーストパーティ Cookie が短期間有効になります。2020 年 11 月現在、両方のタイプの Cookie は有効期限が 7 日間です。この有効期限は変更される可能性があります。

CNAME を使用する 2 番目の方法では、HTTPS プロトコルを使用したセキュリティで保護されているページがサイトにある場合は、アドビと協力して SSL 証明書を取得し、ファーストパーティ cookie を実装することができます。アドビでは HTTP によるデータ収集のサポートを 2020 年後半に終了する予定なので、データ収集には HTTPS のみを使用することを強くお勧めします。

SSL 証明書の発行プロセスは、多くの場合、わかりにくく、時間がかかる可能性があります。結果として、アドビは、業界最先端の証明機関（CA）である DigiCert とのパートナーシップを構築し、これらの証明書の購入および管理を自動化する統合プロセスを策定しました。

お客様の権限を使用して、アドビは CA と連携し、お客様用に新しい SHA-2 SSL 証明書を発行、デプロイおよび管理します。アドビは、引き続き証明書を管理し、予期しない期限切れ、失効またはセキュリティ上の問題によって組織のセキュリティで保護された収集の可用性が脅かされないようにします。

## Adobe Managed Certificate Program

Adobe Managed Certificate Program は、ファーストパーティ cookie 用の新しいファーストパーティ SSL 証明書の実装にお勧めのプロセスです。

Adobe Managed Certificate Program を利用すると、ファーストパーティ cookie 用の新しいファーストパーティ SSL 証明書を追加費用なしで実装できます（最初の 100 個の CNAME）。現在、お客様が管理する独自の SSL 証明書がある場合、Adobe Managed Certificate Program への移行についてアドビカスタマーケアにお問い合わせください。

### 実装方法

次に、ファーストパーティ Cookie 用の新しいファーストパーティ SSL 証明書を実装する方法を示します。

1. [ファーストパーティ cookie リクエストフォーム](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx)に入力して、チケットを開き、Adobe Managed プログラムでファーストパーティ cookie の設定をカスタマーケアにリクエストします。例が記載されたフォーム内の各フィールドに記入します。

2. CNAME レコードを作成します（以下の手順を参照）。

   チケットを受け取ったら、カスタマーケアの担当者からCNAMEレコードが提供されます。 これらのレコードは、アドビが代理で証明書を購入する前に、会社の DNS サーバーで設定される必要があります。CNAMEは次のようになります。

   **セキュアの場合** - 例えば、ホスト名 `smetrics.example.com` が `example.com.adobedc.net` を指します。

>[!NOTE]
> 以前は、HTTPS用とHTTP用の2つのCNAMEを設定することをお勧めしました。 トラフィックの暗号化はベストプラクティスであり、ほとんどのブラウザーではHTTPを使用しないので、CNAMEをHTTP用に設定することをお勧めしません。 必要に応じて、次のようになります。
>    **非セキュア** — ホスト名`metrics.example.com`は次を指します。`example.com.adobedc.net`。

1. CNAMEを設定すると、AdobeはDigiCertと連携して、Adobeの実稼働サーバーに証明書を購入してインストールします。

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

## CNAME レコードの作成

組織のネットワークオペレーションチームは、新しい CNAME レコードを作成することで、DNS サーバーを設定する必要があります。各ホスト名は、アドビのデータ収集サーバーにデータを転送します。

FPCスペシャリストは、設定済みのホスト名と、それらが指定するCNAMEを提供します。 以下に例を示します。

* **SSL ホスト名**： `smetrics.mysite.com`
* **SSL CNAME**: `mysite.com.adobedc.net`

>[!NOTE]
> セキュリティで保護されていないを使用する場合は、次のようになります。
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

コマンドラインから [[!DNL curl]](https://curl.haxx.se/) を使用することをお勧めします。（[!DNL Windows] ユーザーは <https://curl.haxx.se/windows/> から [!DNL curl] をインストールできます）。

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

サイトのコードを編集してファーストパーティ cookie を使用できるようにする前に、次の前提条件を満たします。

* [Adobe Managed Certificate Program](#adobe-managed-certificate-program) の&#x200B;*実装方法*&#x200B;の節で説明した手順に従って、SSL 証明書を要求します。
* CNAME レコードを作成します（上記を参照）。
* ホスト名を検証します（上記を参照）。

ホスト名がアドビのデータ収集サーバーに応答し、転送することを確認したら、実装を変更して独自のデータ収集ホスト名を指定できます。

1. コア JavaScript ファイル（`s_code.js/AppMeasurement.js`）を開きます。
1. コードバージョンを更新する場合は、`s_code.js/AppMeasurement.js` ファイル全体を新しいバージョンに置き換え、すべてのプラグインやカスタマイズ（作成した場合）を置き換えます。**または**、ファーストパーティ cookie のみに関連するコードを更新するには、s.trackingServer および s.trackingServerSecure 変数（SSL 使用時）を探し、新しいデータ収集ホスト名を指定します。mysite.com を使用すると、`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"` のようになります。

1. 更新したコア JavaScript ファイルをサイトにアップロードします。

1. 長期にわたる実装からファーストパーティ cookie に移動する場合、または異なるファーストパーティ収集ホスト名に変更する場合、以前のドメインから新しいドメインに訪問者を移行することをお勧めします。

詳しくは、Analytics 導入ガイドの[訪問者の移行](https://docs.adobe.com/content/help/ja-JP/analytics/components/metrics/unique-visitors.html)を参照してください。

コア JavaScript ファイルをアップロードすると、ファーストパーティ cookie によるデータ収集用の設定がすべておこなわれます。アップロード後の数時間は、Analytics レポートを監視し、通常どおりデータ収集がおこなわれているかを確認することをお勧めします。通常どおりおこなわれていない場合、上記のすべての手順が完了していることを確認し、組織のサポート対象ユーザーの中からカスタマーケアにお問い合わせください。
