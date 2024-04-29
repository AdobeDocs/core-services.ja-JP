---
title: Adobe Experience Platform Web SDK の cookie
description: Web SDK で実装に適用される Cookie を使用する方法を説明します。
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
source-git-commit: 66f78a04674a82335f5df20c4c15d983b6ebdc66
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# Adobe Experience Platform Web SDK の cookie

Adobe Experience Platform Web SDK は、cookie を使用して、実装に固有の値を保存します。

| 名前 | 最大経過年数 | 説明 |
|---|---|---|
| **knd_orgid_identity** | 34128000 （395 日） | ECID と、ECID に関連するその他の情報を保存します。 |
| **kndctr_orgid_consent_check** | 7200 （2 時間） | 同意環境設定サーバー側を検索するようにサーバーにシグナルします。 |
| **kndctr_orgid_consent** | 15552000 （180 日間） | Web サイトに対するユーザーの同意設定を格納します。 |
| **kndctr_orgid_cluster** | 1800 （30 分） | 現在のユーザーのリクエストに対応するEdge Networkリージョンを格納します。 Edge Networkがリクエストを正しいリージョンにルーティングできるように、リージョンは URL パスで使用されます。 ユーザーが別の IP アドレスで接続する場合や、別のセッションで接続する場合は、リクエストは再び最も近いリージョンにルーティングされます。 |
| **mbox** | 63072000 （2 年） | Target 移行設定が true に設定されている場合に存在します。 Target を許可します [mbox cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) Web SDK で設定されます。 |
| **mboxEdgeCluster** | 1800 （30 分） | Target 移行設定が true に設定されている場合に存在します。 これにより、Web SDK は正しいエッジクラスターをに通信できます `at.js` これにより、ユーザーがサイト全体を移動しても、Target プロファイルの同期が維持されます。 |
| **AMCV_###@AdobeOrg** | 34128000 （395 日） | 次の場合に存在 [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/idmigrationenabled) が有効になっています。 サイトの一部がまだを使用している状態で Web SDK に移行する場合に役立ちます `visitor.js`. |

Edge Networkは、すべての Cookie をに設定します。 `secure` および `sameSite="none"` 属性。 現在、web サイトにセキュリティで保護されたセクションと保護されていないセクションの両方がある場合、ユーザーの ID が不正確になる可能性があります。 ユーザーがサイトの保護されたセクションから保護されていないセクションに移動すると、Edge Networkは新しい `ECID` （リクエストを使用）。
