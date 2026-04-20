---
title: Adobe Experience Platform Web SDK Cookie
description: Web SDKが、実装に適用されるCookieを使用する方法について説明します。
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
TQID: https://experienceleague.adobe.com/jysQ5m7o0cI3ECKz2RWZB4Kt3own7XAPm04pr4yLh-k
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a42153ba5a885509e7735e7407e38586fcabb0ad
workflow-type: tm+mt
source-wordcount: 484
ht-degree: 1%

---

# Adobe Experience Platform Web SDKのCookie

Adobe Experience Platform Web SDKでは、実装に固有の値を保存するためにCookieを使用します。

| 名前 | 最大年齢 | サイズ | 説明 |
| --- | --- | --- | --- |
| **`AMCV_###@AdobeOrg`** | 34128000 （395日） | 100 ～ 120 バイト（変数） | [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled)が有効になっている場合に表示されます。 サイトの一部がまだ`visitor.js`を使用している間に、Web SDKに移行する際に役立ちます。 Web SDKは、移行中にこのCookieに読み取りと書き込みを行います。 |
| **`com.adobe.alloy.getTld`** | なし（直ちに削除） | なし | Web SDKが現在のサイトのトップレベルドメインを判断するために内部で使用する一時的なヘルパーCookie。 トップレベルドメインが確立されると、Cookieは削除されます。 行動データやプロファイルデータは保存しません。 |
| **`demdex`** | 15552000 （180日間） | 可変 | Audience Manager IDの同期が有効になっている場合に表示されます。 Audience ManagerはこのCookieを設定して一意のIDを割り当て、IDの同期、セグメンテーション、モデリング、レポートをサポートします。 [Audience Manager Cookie](audience-manager.md)の`demdex`を参照してください。 |
| **`kndctr_<orgId>_identity`** | 34128000 （395日） | 100 ～ 120 バイト（変数） | そのデバイスのECIDおよびその他の関連情報を保存します。 |
| **`kndctr_<orgId>_cluster`** | 1800 （30分） | 3 ～ 5 バイト | 現在のユーザーのリクエストを処理するEdge Network リージョン（場所ヒント）を保存します。 このリージョンは、Edge Networkがリクエストを正しいリージョンにルーティングできるように、URL パスで使用されます。 ユーザーがCookieの有効期間の中で別のIP アドレスに接続した場合、リクエストは再び最も近い地域にルーティングされます。 |
| **`kndctr_<orgId>_consent`** | 15552000 （180日間） | 10 ～ 11 バイト | 訪問者の同意設定を保存します。 同意の環境設定そのものを保存するため、同意に関係なく常に設定されます。 |
| **`kndctr_<orgId>_consent_check`** | 7200 （2時間） | | TTLの有効期限が切れた後、Edge Networkにサーバーサイドで同意を再チェックするようにシグナルを送る、セッション範囲のヘルパー。 キャッシュされた同意に対してTTLを適用します。 |
| **`kndctr_<orgId>_personalization`** | 34128000 （395日） | | Adobe Targetがコンテンツのパーソナライズに使用するセッション情報を保存します。 |
| **`mbox`** | 63072000 （2年間） | | [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled)が有効になっている場合に表示されます。 Web SDKでTarget [mbox cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/)を設定できます。 |
| **`mboxEdgeCluster`** | 1800 （30分） | | [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled)が有効になっている場合に表示されます。 これにより、Web SDKは適切なエッジクラスターを`at.js`に通信できるので、ユーザーがサイトを移動してもTarget プロファイルを同期させることができます。 |
| **`s_ecid`** | 63115200 （2年間） | ～ 45 バイト | CX Enterprise ID （ECID/MID）のコピーを`s_ecid=MCMID\|<ECID>`形式で含みます。 ECIDのファーストパーティバックアップとして機能し、主にCNAME （ファーストパーティ）シナリオに対して機能します。 |

Edge Networkは、`secure`および`sameSite="none"`属性を持つすべてのCookieを設定します。 現在、web サイトに安全なセクションと安全でないセクションの両方がある場合、ユーザー識別が不正確になる可能性があります。 ユーザーがサイトの安全なセクションから安全でないセクションに移動すると、Edge Networkはリクエストとともに新しい`ECID`を生成します。
