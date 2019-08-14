---
description: Analytics は、画像リクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供するために、cookie を使用します。
keywords: cookie;プライバシー
seo-description: Analytics は、画像リクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供するために、cookie を使用します。
seo-title: ファーストパーティ cookie
solution: Experience Cloud、Analytics
title: ファーストパーティ cookie
index: y
snippet: y
translation-type: tm+mt
source-git-commit: 21bab04d9df4f75afbd1dc5940842b57c34ecb24

---


# ファーストパーティCookieについて

Analytics は、画像リクエストとブラウザーセッション間で保持されない変数およびコンポーネントの情報を提供するために、cookie を使用します。これらの cookie は安全で、アドビがホストするドメインから作成されるもので、サードパーティ cookie と呼ばれます。

多くのブラウザーおよびスパイウェア駆除アプリケーションは、Analyticsデータ収集で使用されているものを含め、サードパーティcookieを拒否および削除するように設計されています。ブラウザーやプログラムによって課せられるトラッキングの制限を回避するには、ファーストパーティcookieを実装できます。

ファーストパーティCookieを実装するには、2つのオプションがあります

* エクスペリエンスプラットフォームIDサービスIDサービスは、JavaScriptを使用して、ファーストパーティコンテキストにcookieを設定できます。
* DNSサーバー上のDNSエントリ。
* サイトに `https:` プロトコルを使用してセキュリティで保護されたページがあり、エクスペリエンスプラットフォームIDサービスを使用していない場合は、アドビと協力して、ファーストパーティcookieを実装するためにSSL証明書を取得できます

SSL証明書の発行プロセスでは、多くの場合、煩雑さと時間のかかる処理になります。その結果、アドビは業界最先端の認証局（CA）と提携し、これらの証明書の購入と管理が自動化された統合プロセスを開発しました。

権限を持って、アドビのCAと協力して、新しいSHA-2SSL証明書の発行、導入および管理を行います。アドビは、この証明書を引き続き管理し、予期しない有効期限、失効、セキュリティの問題があることを確認して、貴社のセキュアコレクションの可用性を脅威としません。

## Adobe Managed Certificate Program

ファーストパーティcookie用の新しいファーストパーティSSL証明書を実装するための推奨されるプロセスは、Adobe Managed Certificate Programです。

Adobe Managed Certificateプログラムを使用すると、ファーストパーティcookie用の新しいファーストパーティSSL証明書を追加費用なしで実装できます。現在お客様のお客様管理SSL証明書をお持ちの場合は、Adobe Managed Certificate Programへの移行についてアドビカスタマーケアにお問い合わせください。

### 実装方法

ファーストパーティcookie用の新しいファーストパーティSSL証明書を実装する方法を次に示します。

1. アドビ管理プログラムでファーストパーティcookieの設定を要求するリクエストフォームに入力し、カスタマーケアがチケットを開きます。例が記載されたフォーム内の各フィールドに記入します。

1. CNAMEレコードを作成します。チケットを受信すると、FPSSLスペシャリストはCNAMEレコードのペアを提供する必要があります。これらのレコードは、アドビが証明書を購入する前に、会社のDNSサーバー上で設定する必要があります。CNAMESは、次のようになります。

* **セキュリティ保護** 済み-例えば、ホスト名 `smetrics.example.com` は次を参照します。 `example.com.ssl.d1.omtrdc.net`を参照してください。
* **セキュリティで保護されていない** -例えば、ホスト名 `metrics.example.com` は次を参照します。 `example.com.d1.omtrdc.net`を参照してください。

詳しくは、CNAMEレコードの作成を参照してください。

1. これらのCNAMEを設定すると、アドビの実稼働サーバーに証明書を購入してインストールするDigicgerと連携します。既存の実装がある場合は、訪問者の移行を考慮して既存の訪問者を維持する必要があります。証明書がアドビの実稼働環境にプッシュされた後、トラッキングサーバー変数を新しいホスト名に更新できます。つまり、サイトがセキュリティで保護されていない（https）場合は、を更新 `s.trackingServer`します。サイトがセキュア（https）の場合、両方 `s.trackingServer` の変数と `s.trackingServerSecure` 変数を更新します。

1. ホスト名のping（下記を参照）。

1. 実装コードの更新（下記を参照）。

### メンテナンスと更新

SSL証明書は毎年期限切れになります。つまり、アドビでは毎年、各実装の新しい証明書を毎年購入する必要があります。導入が有効期限切れになるたびに、組織内のすべてのサポート対象ユーザーに電子メール通知が送信されます。ホスト名を更新するには、1人のサポート対象ユーザーがアドビから電子メールに返信し、データ収集の期限切れのホスト名を引き続き使用することをお勧めします。その時点で、アドビは自動的に新しい証明書を購入してインストールします。

### よくある質問

| 質問 | 回答 |
|---|---|
| **このプロセスはセキュリティ保護されていますか?** | はい、アドビ管理プログラムは、証明書や秘密鍵をアドビや発行者の外部で変更することなく、従来の方法よりも安全です。 |
| **アドビがドメインの証明書を購入する方法を教えてください。** | 証明書は、指定したホスト名（例えば、smetrics.example.com）をアドビが所有するホスト名に指定した場合にのみ購入できます。これは基本的に、このホスト名をアドビに委任し、アドビが証明書をアドビに購入できるようにしています。 |
| **証明書の失効を要求できますか。** | ドメインの所有者として、証明書が失効したことをリクエストする権利があります。カスタマーケアのチケットを開くだけで、これを完了することができます。 |
| **この証明書はSHA-2暗号化を使用しますか。** | はい、アドビは、SHA-2証明書を発行するためにDigiCalcを使用します。 |
| **これにより追加費用が発生しますか。** | いいえ。アドビは、追加費用なしですべてのAnalyticsユーザーにこのサービスを提供しています。 |

## CNAMEレコードの作成

組織のネットワークオペレーションチームは、新しいCNAMEレコードを作成してDNSサーバーを設定する必要があります。各ホスト名はデータをアドビのデータ収集サーバーに転送します。

FPCスペシャリストは、設定されているホスト名と、指定するCNAMEを提供します。以下に例を示します。

* **SSLホスト名**:`smetrics.mysite.com`
* **SSL CNAME**:`mysite.com.ssl.d1.sc.omtrdc.net`
* **非SSLホスト名**:`metrics.mysite.com`
* **非SSL CNAME**:`mysite.com.d1.sc.omtrdc.net`

実装コードが変更されない限り、この手順はデータ収集には影響しません。また、導入コードの更新後はいつでも行うことができます。

>[!Ntoo:] Experience Cloud訪問者IDサービスには、ファーストパーティcookieを有効にするためのCNAMEの設定方法があります。

## ホスト名のping

ホスト名をpingして、正しい転送を確認します。データの損失を防ぐために、すべてのホスト名がpingに応答する必要があります。

CNAMEレコードが正しく設定され、アドビが証明書のインストールを確認したら、コマンドプロンプトを開いてホスト名をpingします。Using `mysite.com` as an example: `ping metrics.mysite.com`

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

>[!Ntoo:] 使用し `https:// protocol`ている場合、FPCスペシャリストによって指定されたアップロード日の後にのみpingが応答します。さらに、安全なホスト名と保護されていないホスト名をpingして、実装を更新する前に、安全なホスト名とセキュリティで保護されていないホスト名をpingするようにしてください。

## 実装コードの更新

サイト上のコードを編集してファーストパーティcookieを利用する前に、以下の前提条件を満たしてください。

* "Adobe Managed Certificate Programの実装手順」の説明に従って、SSL証明書をリクエストします。
* CNAMEレコードを作成します。
* ホスト名のpingを参照してください。

ホスト名がAdobeデータ収集サーバーに応答して転送されることを確認したら、実装を変更して、独自のデータ収集ホスト名を指定できます。

1. Open your core JavaScript file (`s_code.js/AppMeasurement.js`).
1. コードバージョンを更新する場合は、`s_code.js/AppMeasurement.js` ファイル全体を新しいバージョンに置き換え、すべてのプラグインやカスタマイズ（作成した場合）を置き換えます。**または**、ファーストパーティcookieに関連するコードのみを更新する場合は、s. trackingServer変数とs. trackingServerSecure（SSLを使用する場合）変数を探し、新しいデータ収集ホスト名を指定します。Using mysite.com as an example:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. 更新したコアJavaScriptファイルをサイトにアップロードします。
1. 長期間の実装からファーストパーティcookieに移行する場合、または別のファーストパーティ収集ホスト名に変更する場合は、前のドメインから新しいドメインに訪問者を移行することをお勧めします。

"Analytics導入ガイド»の?«訪問者の移行?[](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html)

JavaScriptファイルをアップロードすると、すべてのファーストパーティcookieデータ収集用に設定されます。データ収集が通常どおり続行されるように、Analyticsレポートを次の数時間にわたって監視することをお勧めします。それ以外の場合は、上記のすべての手順が完了し、組織のサポート対象ユーザーがカスタマーケアに連絡していることを確認してください。
