---
description: Analytics は、イメージリクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供するために、cookie を使用します。
keywords: cookies;privacy
seo-description: Analytics は、イメージリクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供するために、cookie を使用します。
seo-title: ファーストパーティ cookie
solution: Experience Cloud,Analytics
title: ファーストパーティ cookie
index: y
snippet: y
translation-type: tm+mt
source-git-commit: d4ebe537c4a0da1f24c5cd48e73ec9567d13fb30

---


# ファーストパーティ cookie について

Analytics は、イメージリクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供するために、cookie を使用します。アドビがホストするドメインから発行されるこれらの無害なcookieは、サードパーティcookieと呼ばれます。

ブラウザーやスパイウェア駆除アプリケーションの多くは、サードパーティ cookie を拒否し、削除するよう設計されています。この cookie には、Analytics のデータ収集で使用される cookie も含まれます。訪問者のWebサイトとの関わり方の追跡をサポートするには、ファーストパーティcookieを実装します。

ファーストパーティcookieの実装には、次の2つのオプションを使用できます。

* Experience Platform ID サービス。この ID サービスは、JavaScript を使用してファーストパーティコンテキストに cookie を設定できます。
* アドビがホストするドメインにCNAMEエイリアスを設定するための、会社のDNSサーバー上のDNSエントリ。 様々なアドビ製品がCNAMEの使用をサポートしていますが、すべての場合、CNAMEは特定の顧客の信頼できるファーストパーティエンドポイントの作成に使用され、その顧客が所有します。 顧客が複数のドメインを管理する場合、1つのCNAMEエンドポイントを使用してドメイン間でユーザーを追跡できますが、CNAMEのドメイン外のすべてのドメインにサードパーティcookieが必要なので、サードパーティcookieがブロックされても機能しないのでお勧めしません。 Adobe CNAMEは、異なる顧客が所有するドメイン間で個々のCNAMEやデバイスを追跡するためには使用されません。

Experience Cloud IDサービスで最初のオプションを使用する場合でも、AppleのITPではファーストパーティcookieが短時間のみ有効となるので、2番目のオプションと組み合わせて使用すると最適です。

CNAMEを使用する2つ目のオプションでは、サイトにHTTPSプロトコルを使用したセキュリティで保護されたページがある場合、ファーストパーティcookieを実装するために、アドビと協力してSSL証明書を取得できます。 2020年後半にHTTP収集のサポートを終了する予定なので、データ収集にはHTTPSのみを使用することを強くお勧めします。

SSL 証明書の発行プロセスは、多くの場合、わかりにくく、時間がかかる可能性があります。結果として、アドビは、業界最先端の証明機関（CA）である DigiCert とのパートナーシップを構築し、これらの証明書の購入および管理を自動化する統合プロセスを策定しました。

お客様の権限を使用して、アドビは CA と連携し、お客様用に新しい SHA-2 SSL 証明書を発行、デプロイおよび管理します。アドビはこの証明書を引き続き管理し、予期しない有効期限切れ、失効、またはセキュリティ上の問題が発生した場合でも、組織のセキュアコレクションの可用性を脅かさないようにします。

## Adobe Managed Certificate Program

Adobe Managed Certificate Program は、ファーストパーティ cookie 用の新しいファーストパーティ SSL 証明書の実装にお勧めのプロセスです。

Adobe Managed Certificate Program を利用すると、ファーストパーティ cookie 用の新しいファーストパーティ SSL 証明書を追加費用なしで実装できます。現在、お客様が管理する独自の SSL 証明書がある場合、Adobe Managed Certificate Program への移行についてアドビカスタマーケアにお問い合わせください。

### 実装方法

次に、ファーストパーティ Cookie 用の新しいファーストパーティ SSL 証明書を実装する方法を示します。

1. [ファーストパーティ cookie リクエストフォーム](/help/interface/cookies/assets/FPC_Request_Form.xlsx)に入力して、チケットを開き、Adobe Managed プログラムでファーストパーティ cookie の設定をカスタマーケアにリクエストします。例が記載されたフォーム内の各フィールドに記入します。

1. CNAME レコードを作成します（以下の手順を参照）。

   チケットを受け取ったら、カスタマーケア担当者からCNAMEレコードのペアが提供されます。 これらのレコードは、アドビが代理で証明書を購入する前に、会社の DNS サーバーで設定される必要があります。CNAMESは次のようになります。

   **セキュア** — 例えば、ホスト名は次を指 `smetrics.example.com` し示します。 `example.com.ssl.d1.omtrdc.net`.

   **非セキュア** - 例えば、ホスト名 `metrics.example.com` が `example.com.d1.omtrdc.net` を指します。

1. これらの CNAME が設定されると、アドビは DigiCert と連携して証明書を購入し、アドビの実稼動サーバーにインストールします。

   既存の導入環境がある場合は、既存の訪問者を維持するために訪問者の移行を検討する必要があります。 証明書がアドビの実稼働環境にプッシュされた後、トラッキングサーバー変数を新しいホスト名に更新できます。 Meaning, if the site is not secure (HTTP), update the `s.trackingServer`. If the site is secure (HTTPS), update both `s.trackingServer` and `s.trackingServerSecure` variables.

1. [ホスト名転送の検証](#validate) （以下を参照）。

1. [導入コードの更新](#update) （以下を参照）。

### メンテナンスと更新

SSL 証明書は毎年期限が切れます。つまり、アドビは毎年、各実装用に新しい証明書を購入する必要があります。組織内のすべてのサポート対象ユーザーは、実装の有効期限が近づくたびに電子メール通知を受け取ります。アドビがホスト名を更新するには、サポート対象ユーザーの1人がアドビからの電子メールに返信し、データ収集用に有効期限切れのホスト名を引き続き使用する予定であることを示す必要があります。 その時点で、アドビは自動的に新しい証明書を購入およびインストールします。

### よくある質問

| 質問 | 回答 |
|---|---|
| **このアイテムは保護されていますか？** | はい、アドビおよび発行する証明機関の外部で証明書や秘密鍵が変更されることがないので、Adobe Managed プログラムは、従来の方法よりも安全です。 |
| **ドメイン用の証明書をアドビはどのようにしたら購入できますか？** | 証明書は、特定のホスト名（例えば、smetrics.example.com）がアドビが所有するホスト名を指すようにお客様が指定する際にのみ、購入できます。これは、基本的に、このホスト名をアドビに委任し、アドビが代理で証明書を購入することを許可するということです。 |
| **証明書の失効を要求できますか？** | はい、ドメインの所有者として、お客様はアドビに証明書の失効を要求する資格があります。必要なのは、チケットを開いてカスタマーケアにこれの実行を依頼するだけです。 |
| **この証明書は SHA-2 暗号化を使用しますか？** | はい、アドビは DigiCert と連携して SHA-2 証明書を発行します。 |
| **追加費用が発生しますか？** | いいえ。アドビは、現在のすべてのAdobe Digital Experienceのお客様に対し、追加費用なしで本サービスを提供しています。 |

## CNAME レコードの作成

組織のネットワークオペレーションチームは、新しい CNAME レコードを作成することで、DNS サーバーを設定する必要があります。各ホスト名は、アドビのデータ収集サーバーにデータを転送します。

FPC スペシャリストから、設定されたホスト名とホスト名で指定する必要のある CNAME が提供されます。以下に例を示します。

* **SSL ホスト名**：`smetrics.mysite.com`
* **SSL CNAME**:`mysite.com.ssl.sc.omtrdc.net`
* **非 SSL ホスト名**：`metrics.mysite.com`
* **非 SSL CNAME**：`mysite.com.sc.omtrdc.net`

実装コードが変更されない限り、この手順がデータ収集に影響を及ぼすことはなく、実装コードの更新後はいつでもおこなうことができます。

>[!N注意：]
>Experience Cloud訪問者IDサービスは、ファーストパーティcookieを有効にするCNAMEの設定の代わりに使用できますが、Apple ITPの最近の変更により、Experience Cloud IDサービスを使用している場合でも、CNAMEを割り当てることをお勧めします。

## ホスト名転送の検証 {#validate}

検証には、次の方法を使用できます。

### ブラウザーを使用した検証

CNAMEが設定され、証明書がインストールされている場合は、次の検証にブラウザーを使用できます。

`https://sstats.adobe.com/_check`

**注意：** 証明書がインストールされていない場合は、セキュリティ警告が表示されます。

### 次を使用して検証 [!DNL curl]

アドビでは、コマンドラインから[!DNL [curl](https://curl.haxx.se/)]を使用することをお勧めします。 (ユーザ[!DNL Windows] ーは次の場所からインス [!DNL curl] トールできます： <https://curl.haxx.se/windows/>)

CNAMEをお持ちで、証明書がインストールされていない場合は、次を実行します。`curl -k https://sstats.adobe.com/_check`回答： `SUCCESS`

(この値によ `-k` り、セキュリティ警告が無効になります)。

CNAMEが設定され、証明書がインストールされている場合は、次の手順を実行します。`curl https://sstats.adobe.com/_check`回答： `SUCCESS`

### 次を使用して検証 [!DNL nslookup]

検証に使用で `nslookup` きます。 例とし `mysite.com`てを使用し、コマンドプロンプトを開いて、 `nslookup metrics.mysite.com`

すべてが正常に設定された場合は、次のようなリターンが表示されます。

```
nslookup metrics.mysite.com
Server:  hiodsibxvip01.corp.adobe.com
Address:  10.50.112.247

Non-authoritative answer:
Name:    metrics.mysite.com
Address:  64.136.20.37
```

## 実装コードの更新 {#update}

サイトのコードを編集してファーストパーティ cookie を使用できるようにする前に、次の前提条件を満たします。

* SSL証明書を要求します。上記のAdobe Managed Certificate Programの ** Implement [（実装）の節で説明した手](#adobe-managed-certificate-program)順に従います。
* CNAME レコードを作成します（上記を参照）。
* ホスト名を検証します（上記を参照）。

ホスト名がアドビのデータ収集サーバーに応答し、転送することを確認したら、実装を変更して独自のデータ収集ホスト名を指定できます。

1. コア JavaScript ファイル（`s_code.js/AppMeasurement.js`）を開きます。
1. コードバージョンを更新する場合は、`s_code.js/AppMeasurement.js` ファイル全体を新しいバージョンに置き換え、すべてのプラグインやカスタマイズ（作成した場合）を置き換えます。**または**、ファーストパーティ cookie のみに関連するコードを更新するには、s.trackingServer および s.trackingServerSecure 変数（SSL 使用時）を探し、新しいデータ収集ホスト名を指定します。mysite.com を使用すると、`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"` のようになります。

1. 更新したコア JavaScript ファイルをサイトにアップロードします。

1. 長期にわたる実装からファーストパーティ cookie に移動する場合、または異なるファーストパーティ収集ホスト名に変更する場合、以前のドメインから新しいドメインに訪問者を移行することをお勧めします。

Analytics導入ガ [イドの訪問者の移行](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html) （英語のみ）を参照してください。

コア JavaScript ファイルをアップロードすると、ファーストパーティ cookie によるデータ収集用の設定がすべておこなわれます。アップロード後の数時間は、Analytics レポートを監視し、通常どおりデータ収集がおこなわれているかを確認することをお勧めします。通常どおりおこなわれていない場合、上記のすべての手順が完了していることを確認し、組織のサポート対象ユーザーの中からカスタマーケアにお問い合わせください。
