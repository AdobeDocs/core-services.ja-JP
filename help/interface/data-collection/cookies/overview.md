---
description: Adobe Experience Cloud のソリューションとサービスで Cookie を使用する方法について説明します。
title: Experience Cloudでの Cookie の使用方法
uuid: 4255a13a-917b-4b5f-a7d4-4b2e7521d189
exl-id: 60f1a89e-d989-461b-a6a3-c1df022cd30b
TQID: https://experienceleague.adobe.com/GH5WHcI9440NKYpUzizHlhOMlBSf-Y0WQ5GDBaSvqNI
product_v2:
  - id: e1971122-7081-4556-9222-8a31bd71800c
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0d253888322194189fea6d492ae19cf248357960
workflow-type: tm+mt
source-wordcount: 600
ht-degree: 11%

---

# Experience Cloud での Cookie の使用方法

Adobe Experience Cloudでは cookie を使用します。 Cookie とは、Web サイトがブラウザーに送信する小さなデータであり、後で使用するために保存されます。 Cookie は、ユーザーが再訪問した際やページ間を移動した際に、Web サイトが情報を記憶するのに役立ちます。 Cookie は、訪問を追跡し、あるデバイスを別のデバイスと区別するのに役立ちます。

法律では、多くの場合、誰かのデバイスで cookie を保存または使用する前に許可を得る必要があります。 Adobeでは、法務チームに問い合わせて、適用されるルールを理解することをお勧めします。

## ファーストパーティ cookie について

Adobe Experience Cloudでは、ページビュー間やブラウザーセッション間で持続しない情報のトラッキングに cookie を使用します。 可能な場合、Adobeはファーストパーティ cookie （独自の web サイトに結び付けられます）を使用します。 所有する複数のサイトまたはドメインをまたいでアクティビティを追跡するには、サードパーティ cookie が必要です。

一部のブラウザーおよびスパイウェア駆除ツールでは、サードパーティ cookie がブロックされます。 Adobeには、Cookie がブロックされた場合でも Cookie が引き続き機能することを確認する方法があります。 これがどのように機能するかは、Experience Platform ID サービス（ECID）を使用するか、以前の Analytics Cookie （`s_vi` Cookie など）を使用するかによって異なります。

* [Experience Cloud ID サービス &#x200B;](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview): ECID サービスは、収集ドメインがサイトドメインと一致するかどうかに関係なく、常にファーストパーティ Cookie を設定します。 JavaScriptを使用して、サイトのドメインに cookie を配置します。

* [Analytics の従来の識別子 &#x200B;](analytics.md) （`s_vi` cookie など）:cookie がファーストパーティかサードパーティかは、設定によって異なります。

   * データ収集サーバーがサイトのドメインと一致する場合、cookie はファーストパーティです。
   * 一致しない場合、cookie はサードパーティです。 サードパーティ cookie がブロックされている場合、Adobeは通常の cookie ではなく、フォールバック cookie （`s_fid`）を設定します。

収集サーバーがサイトのドメインと一致するようにするには、**CNAME 設定** を使用します。 この際、DNS 設定を更新し、自分が所有するカスタムドメインがAdobeのサーバーを指すようにします。 これにより、トラッキング cookie がファーストパーティとして表示されます。 1 つの CNAME は複数のドメインで機能しますが、CNAME に一致しないドメインは引き続きサードパーティ Cookie を設定します。

>[!NOTE]
>
>Appleのインテリジェントトラッキング防止（ITP）は、収集ドメインがサイトドメインと一致する場合でも、Adobeのファーストパーティ cookie の持続時間を制限します。 ITP は、macOSの Safari と、iOSおよび iPadOS のすべてのブラウザーに影響します。 2020 年 11 月以降、CNAME を使用して設定された Cookie は、JavaScriptで設定された Cookie と同じくらい早く期限切れになります。 この制限時間は、今後変更される可能性があります。

次に、テキストの簡略化したバージョンを示します。

## Cookie とプライバシー

Adobeはプライバシーとデータセキュリティを重視しています。 プライバシー組織、規制当局、AdChoices などのプログラムと連携して、データの使用方法を制御できるようにします。

Adobe Experience Cloudのほとんどの Cookie は個人情報を保存しません。 これらは安全で、会社のみがレポート、コンテンツ、広告に使用します。 Adobeは、匿名の業界全体のレポート（デジタルマーケティングのInsight レポートなど）を除き、このデータを他の顧客やサードパーティと共有しません。

Adobeは、異なる会社間でブラウザーデータを組み合わせることはありません。 プライバシーを保護するために、一部のAdobe ツールでは、各 web サイトで独自の cookie を使用します。 また、Cookie に独自のドメインを使用することを許可し、ファーストパーティでより安全なものもあります。

Cookie は、以前に保存された情報のみを保存できます。 デバイス上でコードを実行したり、他のデータを読み取ったりすることはできません。 また、Web ブラウザーでは、Cookie を設定した Web サイトによる Cookie の読み取りのみが許可されます。 例えば、Adobe.comだけが、設定された Cookie を読み取ることができます。

次の図は、標準的なイメージリクエストにおける cookie の用途を示しています。

![標準的な画像リクエストの cookie 使用](assets/CookiesProcessGraphic-01.png)

次の図は、ストレートイメージリクエストの cookie の使用方法を示しています（JS ファイルが読み込まれていないシナリオで使用）。

![ストレートイメージリクエストの cookie 使用](assets/CookiesProcessGraphic2.png)

