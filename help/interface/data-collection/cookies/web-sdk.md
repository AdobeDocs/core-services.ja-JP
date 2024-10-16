---
title: Adobe Experience Platform Web SDK の cookie
description: Web SDK で実装に適用される Cookie を使用する方法を説明します。
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
source-git-commit: d69af76f6deff4f2b73e67ee7b69b9fee1ee3a2e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Adobe Experience Platform Web SDK の cookie

Adobe Experience Platform Web SDK は、cookie を使用して、実装に固有の値を保存します。

| 名前 | 最大経過年数 | サイズ | 説明 |
|---|---|---|---|
| **kndctr_&lt;ORG_ID>_identity** | 34128000 （395 日） | 100～120 バイト（可変） | ECID と、ECID に関連するその他の情報を保存します。 |
| **kndctr_&lt;ORG_ID>_consent** | 15552000 （180 日間） | 10 ～ 11 バイト | Web サイトに対するユーザーの同意設定を格納します。 |
| **kndctr_&lt;ORG_ID>_cluster** | 1800 （30 分） | 3 ～ 5 バイト | 現在のユーザーのリクエストに対応するEdge Networkリージョンを格納します。 Edge Networkがリクエストを正しいリージョンにルーティングできるように、リージョンは URL パスで使用されます。 ユーザーが別の IP アドレスで接続する場合や、別のセッションで接続する場合は、リクエストは再び最も近いリージョンにルーティングされます。 |
| **mbox** | 63072000 （2 年） | | Target 移行設定が true に設定されている場合に存在します。 これにより、Web SDK で Target [mbox cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) を設定できます。 |
| **mboxEdgeCluster** | 1800 （30 分） | | Target 移行設定が true に設定されている場合に存在します。 これにより、Web SDK は正しいエッジクラスターを `at.js` に通信できるので、ユーザーがサイト全体を移動しても、Target プロファイルの同期が維持されます。 |
| **AMCV_###@AdobeOrg** | 34128000 （395 日） | | [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/idmigrationenabled) が有効な場合に表示されます。 サイトの一部がまだ `visitor.js` を使用している場合に Web SDK に移行すると役立ちます。 |

Edge Networkは、すべての cookie を `secure` 属性と `sameSite="none"` 属性に設定します。 現在、web サイトにセキュリティで保護されたセクションと保護されていないセクションの両方がある場合、ユーザーの ID が不正確になる可能性があります。 ユーザーがサイトの保護されたセクションから保護されていないセクションに移動すると、Edge Networkはリクエストで新しい `ECID` を生成します。
