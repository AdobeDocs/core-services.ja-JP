---
description: Adobe Target で Cookie を使用して、どのオンラインコンテンツおよびオファーが訪問者に対してより関連性が高いかを web サイトオペレーターがテストできるようにする方法について説明します。
solution: Target
title: Adobe Target の cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
TQID: 'https://experienceleague.adobe.com/UgyFDDtrYEMsXUim90ygjkiR51e87hRLMDsP8F4O2-I'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
subfeature_v2: id:
role_v2: id:
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f01d85af42b8f2c27dbada8f73546bc6fe4bf710
workflow-type: tm+mt
source-wordcount: 706
ht-degree: 22%

---

# Adobe Target cookie

Adobe Target では、オンラインコンテンツのテスト機能を実現する目的と、より関連性の高いコンテンツを訪問者に対して表示する目的で、Web サイト運用者向けに cookie を使用します。

>[!NOTE]
>
>この記事に記載されている情報は、[Adobe Target JavaScript ライブラリ &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=ja){target=_blank} （`at.js`）にのみ適用されます。 Web SDKを使用したTargetの実装について詳しくは、[Adobe Experience Platform Web SDK Cookie](web-sdk.md)を参照してください。
>
>Cookieの期間を除き、必要に応じてこの記事で説明する設定を変更できます。 Cookie設定を変更する場合は、[&#x200B; アカウント担当者](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank}にご相談ください。

## ファーストパーティ Cookie

次の1st パーティ Cookieは、お客様のドメインに保存されます。

| Cookie | 詳細 |
| --- | --- |
| `mbox` | 訪問者に関する匿名IDを保存します。<P>**Cookie ドメイン**: mboxを提供するドメイン。 このCookieは企業のドメインから提供されるため、Cookieは1st パーティ Cookieです。 いずれかのドメイン名に`example.co.uk`などの国コードが含まれる場合は、クライアントサービスと協力して、このコードをサポートするように`at.js`を設定します。 Cookie ドメインのカスタマイズについて詳しくは、必要に応じて、Adobe Target開発者ガイドの[targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=ja){target=_blank}の`cookieDomain`を参照してください。<P>**サーバードメイン**: `clientcode.tt.omtrdc.net`。Adobe Target アカウントのクライアントコードを使用します。<P>**Cookie期間**: Cookieは、前回のログインから2年後も訪問者のブラウザーに残ります。 cookie の期間は変更できません。<P>Cookieは、訪問者が[!DNL Target]のアクティビティをどのように体験するかを管理するために、いくつかの値を保持します。<P>**セッション ID**：特定のユーザーセッションの一意のID。 デフォルトでは、セッションは 30 分間無操作状態が続くと有効期限が切れます。 `sessionId`を自分で生成する場合（例：[&#x200B; サーバーサイド実装](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html?lang=ja){target=_blank}の場合）、次の点を確認してください。<ul><li>セッション IDは、スペース、疑問符（?）以外の任意の印刷可能な文字列にできます ）、中括弧（{ }）、またはスラッシュ（/）。</li><li>セッション IDは、1文字から128文字の長さである必要があります。</li><li>特定のセッションの場合、Cookieの値は複数のリクエストで同じである必要があります。</li><li>任意の時点で、特定の訪問者に対して並列セッション（`sessionIds`）を設定しないでください。</li></ul>エッジクラスター内の特定のノードへのルーティングは、セッション IDを使用して実行されます。<ul><li>セッションは、サーバサイドで 30 分間アクティブです。 したがって、`tntId/thirdPartyId`で最後に行われたリクエストから30分以内に、特定の`tntId/thirdPartyId`に対して異なるセッション IDを使用しないでください。 そうしないと、プロファイルに対する変更に一貫性がなく、予測できないことがあります。</li><li>訪問者が非アクティブ状態になってから30分後に、新しいセッション IDを使用する必要があります。</li><li>複数の`tntIds/thirdPartyIds`で同じセッション IDを使用すると、`tntId/thirdPartyIDs`によって識別されるプロファイルに予測不可能な変更が生じる可能性があります。</li></ul>メモ：特定のセッション IDに対する同時要求の数の[制限](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html#content-delivery){target=_blank}を参照してください。<P>**pc ID**：訪問者のブラウザーの半永久的なID。 cookie が手動で削除されるまで存続します。<P>**check**：訪問者がCookieをサポートしているかどうかを判断するために使用される簡単なテスト値。 訪問者がページをリクエストするたびに設定されます。<P>**無効**：訪問者の読み込み時間がat.js ファイルで設定されたタイムアウトを超えるかどうかを設定します。 デフォルトでは、このタイムアウトは1時間続きます。 |
| `at_check` | ブラウザーでCookieの読み取り/書き込み機能が有効になっているかどうかを確認するための一時的なCookie。 |
| `mboxEdgeCluster` | このCookieは、[overrideMboxEdgeServer設定](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=ja){target=_blank}が`true`に設定されている場合にのみ存在します。 |

これらの1st パーティ Cookieで`HTTPOnly`を使用することはできません。 `at.js` JavaScript ライブラリは、これらのCookieに対する読み取り/書き込みが必要です。 これらのCookieは`at.js`によって作成されたもので、サーバーから設定されていません。

`secure`設定は、`at.js`の`secureOnly: true`設定を使用して、これらすべてのCookieで有効にできます。

## サードパーティ Cookie

Adobe Targetから取得したユーザーは、カスタマイズされたサードパーティ Cookieを作成できます。 次のサードパーティ Cookieは`tt.omtrdc.net`に保存されています：

| Cookie | 詳細 |
| --- | --- |
| `customerclientcode!mboxPC` | クロスドメインが有効な場合に表示されます。 |
| `customerclientcode!mboxSession` | クロスドメインが有効な場合に表示されます。 |

これらのサードパーティ Cookieは、標準装備のHTTPOnlyであり、Adobe Target Data Collection Serverによって設定されます。

`secure`設定は、`at.js`の`secureOnly: true`設定を使用してすべてのCookieで有効にできます。

