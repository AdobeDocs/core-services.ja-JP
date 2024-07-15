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
source-git-commit: 9ee4d9b0e670dec35cda530892c49e36bf7cc107
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 17%

---

# Adobe Targetの cookie

Adobe Target では、オンラインコンテンツのテスト機能を実現する目的と、より関連性の高いコンテンツを訪問者に対して表示する目的で、Web サイト運用者向けに cookie を使用します。

>[!NOTE]
>
>この記事の情報は、[Adobe Target JavaScript ライブラリ ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} （`at.js`）にのみ適用されます。 Web SDK を使用した Target 実装について詳しくは、[Adobe Experience Platform Web SDK Cookie](web-sdk.md) を参照してください。
>
>cookie の期間を除き、必要に応じて、この記事で説明する設定を変更できます。 cookie の設定を変更する場合は [ アカウント担当者にお問い合わせください ](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank}。

## ファーストパーティ cookie

次のファーストパーティ cookie が顧客のドメインに保存されます。

| Cookie | 詳細 |
| --- | --- |
| `mbox` | 訪問者に関する匿名識別子を格納します。<P>**Cookie ドメイン**:mbox の提供元のドメイン。 この cookie は会社のドメインから提供されるため、この cookie はファーストパーティ cookie です。 ドメイン名に `example.co.uk` などの国コードが含まれている場合は、クライアントサービスにお問い合わせの上、このコードをサポートするように `at.js` を設定してください。 Cookie ドメインのカスタマイズについて詳しくは、必要に応じて、『Adobe Target開発者ガイド』の [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} の `cookieDomain` を参照してください。<P>**サーバードメイン**:`clientcode.tt.omtrdc.net`。Adobe Target アカウントのクライアントコードを使用します。<P>**Cookie の期間**:Cookie は、最後にログインしてから 2 年間訪問者のブラウザーに残ります。 cookie の期間は変更できません。<P>Cookie には、訪問者のアクティビティのエクスペリエンスを管理するためにいくつかの値 [!DNL Target] 保持されています。<P>**セッション ID**：特定のユーザーセッションの一意の ID。 デフォルトでは、セッションは 30 分間無操作状態が続くと有効期限が切れます。`sessionId` を自分で生成する場合（例：[ サーバーサイド実装 ](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}）は、次のことを確認します。<ul><li>セッション ID には、スペース、疑問符（? ）、またはスラッシュ（ / ）以外の印刷可能な文字列を使用できます。</li><li>セッション ID の長さは 1 ～ 128 文字にする必要があります。</li><li>特定のセッションでは、cookie の値は複数のリクエスト間で同じにする必要があります。</li><li>特定の訪問者に対して、どの時点でも並列セッション（個別の `sessionIds`）を使用しないでください。</li></ul>エッジクラスター内の特定のノードへのルーティングは、セッション ID を使用して行われます。<ul><li>セッションは、サーバサイドで 30 分間アクティブです。したがって、`tntId/thirdPartyId` で行われた最後のリクエストから 30 分以内に、特定の `tntId/thirdPartyId` ージに対して異なるセッション ID を使用しないでください。 そうしないと、プロファイルに対する変更に一貫性がなく、予測できないことがあります。</li><li>訪問者からの非アクティブ状態が 30 分間続いた後は、新しいセッション ID を使用する必要があります。</li><li>同じセッション ID を複数の `tntIds/thirdPartyIds` で使用すると、`tntId/thirdPartyIDs` で識別されるプロファイルに予期しない変更が加えられる可能性があります。</li></ul>注意：特定のセッション ID の [ 同時要求数の制限 ](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html#content-delivery){target=_blank} を参照してください。<P>**pc ID**：訪問者のブラウザーの半永久的な ID。 cookie が手動で削除されるまで存続します。<P>**チェック**：訪問者が Cookie をサポートしているかどうかを判断するために使用される単純なテスト値。 訪問者がページをリクエストするたびに設定されます。<P>**disable**：訪問者の読み込み時間が at.js ファイルで設定されているタイムアウトを超えた場合に設定されます。 デフォルトでは、このタイムアウトは 1 時間続きます。 |
| `at_check` | 一時的な cookie：ブラウザーで cookie の読み取り/書き込み機能が有効かどうかを確認します。 |
| `mboxEdgeCluster` | この Cookie は、[overrideMboxEdgeServer 設定 ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} が `true` に設定されている場合にのみ存在します。 |

これらのファーストパーティ cookie で `HTTPOnly` を使用することはできません。 `at.js` JavaScript ライブラリは、これらの cookie に対して読み取り/書き込みを行う必要があります。 これらの cookie は `at.js` によって作成され、サーバーから設定されるわけではありません。

`at.js` の `secureOnly: true` 設定を使用して、これらすべての Cookie で `secure` 設定を有効にすることができます。

## サードパーティ Cookie

Adobe Target ユーザーは、カスタマイズされたサードパーティ cookie を作成できます。 次のサードパーティ cookie が `tt.omtrdc.net` に保存されます。

| Cookie | 詳細 |
| --- | --- |
| `customerclientcode!mboxPC` | クロスドメインが有効な場合に存在します。 |
| `customerclientcode!mboxSession` | クロスドメインが有効な場合に存在します。 |

これらのサードパーティ cookie は HTTPOnly により初期設定されており、Adobe Target Data Collection Server によって設定されます。

`secure` 設定は、`at.js` の `secureOnly: true` 設定を使用して、すべての cookie で有効にすることができます。
