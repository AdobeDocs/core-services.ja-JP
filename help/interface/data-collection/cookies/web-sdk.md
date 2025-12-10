---
title: Adobe Experience Platform Web SDKの cookie
description: Web SDKで実装に適用される Cookie を使用する方法を説明します。
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
source-git-commit: 97b3db58a9bf25ec0a6dd18c7b62117063e58407
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 1%

---

# Adobe Experience Platform Web SDKの cookie

Adobe Experience Platform Web SDKでは、実装に固有の値を保存するために Cookie を使用します。

| 名前 | 最大経過年数 | サイズ | 説明 |
|---|---|---|---|
| **`AMCV_###@AdobeOrg`** | 34128000 （395 日） | 100～120 バイト（可変） | [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled) が有効な場合に表示されます。 これは、サイトの一部がまだ `visitor.js` を使用している場合に web SDKに移行するのに役立ちます。 Web SDKは、移行中にこの cookie の読み取りと書き込みを行います。 |
| **`demdex`** | 15552000 （180 日間） | 可変 | Audience Manager ID の同期が有効な場合に存在します。 Audience Managerは、一意の ID を割り当て、ID 同期、セグメント化、モデリング、レポートをサポートするために、この cookie を設定します。 `demdex`Audience Managerの Cookie[ の ](audience-manager.md) を参照してください。 |
| **`kndctr_<orgId>_identity`** | 34128000 （395 日） | 100～120 バイト（可変） | そのデバイスの ECID およびその他の関連情報を格納します。 |
| **`kndctr_<orgId>_cluster`** | 1800 （30 分） | 3 ～ 5 バイト | 現在のユーザーのリクエストを処理するEdge Network リージョン（場所のヒント）を格納します。 Edge Networkでリクエストを正しいリージョンにルーティングできるように、リージョンは URL パスで使用されます。 ユーザーが cookie の有効期間内に異なる IP アドレスで接続した場合、リクエストは再び最も近い地域にルーティングされます。 |
| **`kndctr_<orgId>_consent`** | 15552000 （180 日間） | 10 ～ 11 バイト | 訪問者の同意環境設定を格納します。 同意環境設定自体を保存するので、同意に関係なく常に設定します。 |
| **`kndctr_<orgId>_consent_check`** | 7200 （2 時間） | | TTL の有効期限が切れた後に、サーバーサイドで同意を再確認するようにEdge Networkにシグナルを送信する、セッションスコープのヘルパー。 キャッシュされた同意に対して TTL が適用されます。 |
| **`kndctr_<orgId>_personalization`** | 34128000 （395 日） | | Adobe Targetがコンテンツのパーソナライズに使用するセッション情報を格納します。 |
| **`mbox`** | 63072000 （2 年） | | [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled) が有効な場合に表示されます。 これにより、Web SDKで Target [mbox cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) を設定できます。 |
| **`mboxEdgeCluster`** | 1800 （30 分） | | [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled) が有効な場合に表示されます。 これにより、Web SDKは正しいエッジクラスターを `at.js` に通信できるため、ユーザーがサイト全体を移動しても、Target プロファイルの同期が維持されます。 |
| **`s_ecid`** | 63115200 （2 年） | ～ 45 バイト | Experience Cloud ID （ECID/MID）のコピーが `s_ecid=MCMID\|<ECID>` の形式で含まれます。 主に CNAME （ファーストパーティ）シナリオ用に、ECID のファーストパーティバックアップとして機能します。 |

Edge Networkは、`secure` 属性と `sameSite="none"` 属性を持つすべての cookie を設定します。 現在、web サイトにセキュリティで保護されたセクションと保護されていないセクションの両方がある場合、ユーザーの ID が不正確になる可能性があります。 ユーザーがサイトの保護されたセクションから保護されていないセクションに移動すると、Edge Networkはリクエストで新しい `ECID` を生成します。
