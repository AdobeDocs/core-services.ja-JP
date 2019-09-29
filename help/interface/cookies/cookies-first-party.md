---
description: Analytics は、イメージリクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供するために、cookie を使用します。
keywords: cookie;プライバシー
seo-description: Analytics は、イメージリクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供するために、cookie を使用します。
seo-title: ファーストパーティ cookie
solution: Experience Cloud,Analytics
title: ファーストパーティ cookie
index: y
snippet: y
translation-type: tm+mt
source-git-commit: 2bdc4b7287ccacfc4d968278b2c3ffdaeddfc105

---


# ファーストパーティ cookie について

Analytics は、イメージリクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供するために、cookie を使用します。これらの cookie は安全で、アドビがホストするドメインから作成されるもので、サードパーティ cookie と呼ばれます。

ブラウザーやスパイウェア駆除アプリケーションの多くは、サードパーティ cookie を拒否し、削除するよう設計されています。この cookie には、Analytics のデータ収集で使用される cookie も含まれます。ブラウザーおよびプログラムで設定される追跡の制限を回避するために、ファーストパーティ cookie を実装できます。

ファーストパーティ cookie を実装するには、2 つのオプションが利用できます。

* Experience Platform ID サービス。この ID サービスは、JavaScript を使用してファーストパーティコンテキストに cookie を設定できます。
* 会社の DNS サーバーの DNS エントリ。
* サイトに `https:` プロトコルを使用して保護されているページがあり、Experience Platform ID サービスを使用していない場合、ファーストパーティ cookie を実装するために、アドビと連携して SSL 証明書を取得できます。

SSL 証明書の発行プロセスは、多くの場合、わかりにくく、時間がかかる可能性があります。結果として、アドビは、業界最先端の証明機関（CA）である DigiCert とのパートナーシップを構築し、これらの証明書の購入および管理を自動化する統合プロセスを策定しました。

お客様の権限を使用して、アドビは CA と連携し、お客様用に新しい SHA-2 SSL 証明書を発行、デプロイおよび管理します。アドビは、引き続き証明書を管理し、予期しない期限切れ、失効またはセキュリティ上の問題によって組織のセキュリティで保護された収集の可用性が脅かされないようにします。

## Adobe Managed Certificate Program

Adobe Managed Certificate Program は、ファーストパーティ cookie 用の新しいファーストパーティ SSL 証明書の実装にお勧めのプロセスです。

Adobe Managed Certificate Program を利用すると、ファーストパーティ cookie 用の新しいファーストパーティ SSL 証明書を追加費用なしで実装できます。現在、お客様が管理する独自の SSL 証明書がある場合、Adobe Managed Certificate Program への移行についてアドビカスタマーケアにお問い合わせください。

### 実装方法

次に、ファーストパーティ Cookie 用の新しいファーストパーティ SSL 証明書を実装する方法を示します。

1. [ファーストパーティ cookie リクエストフォーム](/help/interface/cookies/assets/FPC_Request_Form.xlsx)に入力して、チケットを開き、Adobe Managed プログラムでファーストパーティ cookie の設定をカスタマーケアにリクエストします。例が記載されたフォーム内の各フィールドに記入します。

1. CNAME レコードを作成します（以下の手順を参照）。チケットを受け取ったら、FPSSL スペシャリストは CNAME レコードのペアをお客様に提供する必要があります。これらのレコードは、アドビが代理で証明書を購入する前に、会社の DNS サーバーで設定される必要があります。CNAME は次のようになります。**セキュア** - 例えば、ホスト名 `smetrics.example.com` が`example.com.ssl.d1.omtrdc.net` を指します。**非セキュア** - 例えば、ホスト名 `metrics.example.com` が `example.com.d1.omtrdc.net` を指します。

1. これらの CNAME が設定されると、アドビは DigiCert と連携して証明書を購入し、アドビの実稼動サーバーにインストールします。既存の実装がある場合、既存の訪問者を維持するために、訪問者の移行を検討する必要があります。証明書がアドビの実稼動環境にプッシュされてライブになると、トラッキングサーバー変数を新しいホスト名に更新できます。つまり、サイトが安全（https）でない場合、`s.trackingServer` を更新します。サイトが安全（https）な場合、`s.trackingServer` と `s.trackingServerSecure` の両方の変数を更新します。

1. ホスト名を ping します（以下を参照）。

1. 実装コードを更新します（以下を参照）。

### メンテナンスと更新

SSL 証明書は毎年期限が切れます。つまり、アドビは毎年、各実装用に新しい証明書を購入する必要があります。組織内のすべてのサポート対象ユーザーは、実装の有効期限が近づくたびに電子メール通知を受け取ります。アドビがお客様のホスト名を更新するには、1 人のサポート対象ユーザーがアドビからの電子メールに返信して、引き続き期限が切れるホスト名をデータ収集に使用する計画であると示す必要があります。その時点で、アドビは自動的に新しい証明書を購入およびインストールします。

### よくある質問

| 質問 | 回答 |
|---|---|
| **このアイテムは保護されていますか？** | はい、アドビおよび発行する証明機関の外部で証明書や秘密鍵が変更されることがないので、Adobe Managed プログラムは、従来の方法よりも安全です。 |
| **ドメイン用の証明書をアドビはどのようにしたら購入できますか？** | 証明書は、特定のホスト名（例えば、smetrics.example.com）がアドビが所有するホスト名を指すようにお客様が指定する際にのみ、購入できます。これは、基本的に、このホスト名をアドビに委任し、アドビが代理で証明書を購入することを許可するということです。 |
| **証明書の失効を要求できますか？** | はい、ドメインの所有者として、お客様はアドビに証明書の失効を要求する資格があります。必要なのは、チケットを開いてカスタマーケアにこれの実行を依頼するだけです。 |
| **この証明書は SHA-2 暗号化を使用しますか？** | はい、アドビは DigiCert と連携して SHA-2 証明書を発行します。 |
| **追加費用が発生しますか？** | いいえ、アドビは、このサービスを現在のすべての Analytics のお客様に追加費用なしで提供しています。 |

## CNAME レコードの作成

組織のネットワークオペレーションチームは、新しい CNAME レコードを作成することで、DNS サーバーを設定する必要があります。各ホスト名は、アドビのデータ収集サーバーにデータを転送します。

FPC スペシャリストから、設定されたホスト名とホスト名で指定する必要のある CNAME が提供されます。以下に例を示します。

* **SSL ホスト名**：`smetrics.mysite.com`
* **SSL CNAME**:`mysite.com.ssl.d1.sc.omtrdc.net`
* **非 SSL ホスト名**：`metrics.mysite.com`
* **非 SSL CNAME**：`mysite.com.d1.sc.omtrdc.net`

実装コードが変更されない限り、この手順がデータ収集に影響を及ぼすことはなく、実装コードの更新後はいつでもおこなうことができます。

>[!N注意：]Experience Cloud 訪問者 ID サービスは、ファーストパーティ cookie を有効にするために、CNAME を設定するための代替手段を提供します。

## ホスト名の ping

ホスト名を ping して、正しく転送していることを確認します。すべてのホスト名は、データ損失を避けるために ping に応答する必要があります。

CNAME レコードが適切に設定され、アドビが証明書のインストールを確認したら、コマンドプロンプトを開いてホスト名を ping します。`mysite.com` を使用すると、`ping metrics.mysite.com` のようになります。

すべてが正しく設定されていれば、次のような応答が返されます。

```Pinging mysite.com.112.2o7.net [66.235.132.232] with 32 bytes of data:
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246

Ping statistics for 66.235.132.232: Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds: Minimum = 19ms, Maximum = 19ms, Average = 19ms
```

CNAME レコードが正しく設定されていないか、有効でない場合は、次のような応答が返されます。

`Ping request could not find the host. Please check the name and try again.`

>[!N注意：]`https:// protocol` を使用している場合、FPC スペシャリストが指定したアップロード日の後でしか ping は応答しません。また、実装を更新する前に、必ず保護されたホスト名と保護されていないホスト名で ping を実行し、どちらも正しく機能していることを確認してください。

## 実装コードの更新

サイトのコードを編集してファーストパーティ cookie を使用できるようにする前に、次の前提条件を満たします。

* Adobe Managed Certificate Program の実装手順で説明したように、SSL 証明書を要求します。
* CNAME レコードを作成します（上記を参照）。
* ホスト名を ping します（上記を参照）。

ホスト名がアドビのデータ収集サーバーに応答し、転送することを確認したら、実装を変更して独自のデータ収集ホスト名を指定できます。

1. コア JavaScript ファイル（`s_code.js/AppMeasurement.js`）を開きます。
1. コードバージョンを更新する場合は、`s_code.js/AppMeasurement.js` ファイル全体を新しいバージョンに置き換え、すべてのプラグインやカスタマイズ（作成した場合）を置き換えます。**または**、ファーストパーティ cookie のみに関連するコードを更新するには、s.trackingServer および s.trackingServerSecure 変数（SSL 使用時）を探し、新しいデータ収集ホスト名を指定します。mysite.com を使用すると、`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"` のようになります。

1. 更新したコア JavaScript ファイルをサイトにアップロードします。

1. 長期にわたる実装からファーストパーティ cookie に移動する場合、または異なるファーストパーティ収集ホスト名に変更する場合、以前のドメインから新しいドメインに訪問者を移行することをお勧めします。

See [Visitor Migration](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html) in the Analytics Implementation Guide.

コア JavaScript ファイルをアップロードすると、ファーストパーティ cookie によるデータ収集用の設定がすべておこなわれます。アップロード後の数時間は、Analytics レポートを監視し、通常どおりデータ収集がおこなわれているかを確認することをお勧めします。通常どおりおこなわれていない場合、上記のすべての手順が完了していることを確認し、組織のサポート対象ユーザーの中からカスタマーケアにお問い合わせください。
