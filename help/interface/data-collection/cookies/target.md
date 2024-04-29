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
ht-degree: 18%

---

# Adobe Targetの cookie

Adobe Target では、オンラインコンテンツのテスト機能を実現する目的と、より関連性の高いコンテンツを訪問者に対して表示する目的で、Web サイト運用者向けに cookie を使用します。

>[!NOTE]
>
>この記事の情報は、次の場合にのみ適用されます [Adobe Target JavaScript ライブラリ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=ja){target=_blank} （`at.js`）に設定します。 参照： [Adobe Experience Platform Web SDK の cookie](web-sdk.md) web SDK を使用した Target 実装について説明します。
>
>cookie の期間を除き、必要に応じて、この記事で説明する設定を変更できます。 [アカウント担当者にお問い合わせください](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html?lang=ja){target=_blank} cookie の設定を変更する場合

## ファーストパーティ ｃookie

次のファーストパーティ cookie が顧客のドメインに保存されます。

| Cookie | 詳細 |
| --- | --- |
| `mbox` | 訪問者に関する匿名識別子を格納します。<P>**Cookie ドメイン**:mbox の提供元のドメイン。 この cookie は会社のドメインから提供されるため、この cookie はファーストパーティ cookie です。 いずれかのドメイン名に国コード（例：）が含まれる場合 `example.co.uk`、クライアントサービスと連携して設定 `at.js` このコードをサポートします。 Cookie ドメインのカスタマイズについて詳しくは、必要に応じて次を参照してください： `cookieDomain` 未満 [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=ja){target=_blank} （Adobe Target開発者ガイド）を参照してください。<P>**サーバードメイン**: `clientcode.tt.omtrdc.net`。Adobe Target アカウントのクライアントコードを使用します。<P>**Cookie の期間**:cookie が訪問者のブラウザーに残る期間は、最後にログインしてから 2 年間です。 cookie の期間は変更できません。<P>Cookie には、訪問者のエクスペリエンスを管理するためにいくつかの値が保持されています [!DNL Target] アクティビティ：<P>**セッション ID**：特定のユーザーセッションの一意の ID。 デフォルトでは、セッションは 30 分間無操作状態が続くと有効期限が切れます。を生成する場合 `sessionId` 自分自身（例： [サーバーサイドの実装](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html?lang=ja){target=_blank}）、次のことを確認します。<ul><li>セッション ID には、スペース、疑問符（? ）、またはスラッシュ（ / ）以外の印刷可能な文字列を使用できます。</li><li>セッション ID の長さは 1 ～ 128 文字にする必要があります。</li><li>特定のセッションでは、cookie の値は複数のリクエスト間で同じにする必要があります。</li><li>並列セッション（個別）は使用しないでください `sessionIds`）を選択します。</li></ul>エッジクラスター内の特定のノードへのルーティングは、セッション ID を使用して行われます。<ul><li>セッションは、サーバサイドで 30 分間アクティブです。したがって、特定のに異なるセッション ID を使用しないでください `tntId/thirdPartyId` で行われた最後のリクエストから 30 分以内 `tntId/thirdPartyId`. そうしないと、プロファイルに対する変更に一貫性がなく、予測できないことがあります。</li><li>訪問者からの非アクティブ状態が 30 分間続いた後は、新しいセッション ID を使用する必要があります。</li><li>同じセッション ID を複数で使用 `tntIds/thirdPartyIds` で識別されるプロファイルに、予期しない変更が加えられる可能性があります。 `tntId/thirdPartyIDs`.</li></ul>注意：「参照」 [同時要求数の制限](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html#content-delivery){target=_blank} （特定のセッション ID に対して）。<P>**pc ID**：訪問者のブラウザーの半永久的な ID。 cookie が手動で削除されるまで存続します。<P>**チェック**：訪問者が Cookie をサポートしているかどうかを判断するために使用される単純なテスト値。 訪問者がページをリクエストするたびに設定されます。<P>**disable**：訪問者の読み込み時間が at.js ファイルで設定されているタイムアウトを超えた場合に設定されます。 デフォルトでは、このタイムアウトは 1 時間続きます。 |
| `at_check` | 一時的な cookie：ブラウザーで cookie の読み取り/書き込み機能が有効かどうかを確認します。 |
| `mboxEdgeCluster` | この Cookie は、次の場合にのみ存在します [overrideMboxEdgeServer 設定](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=ja){target=_blank} はに設定されています。 `true`. |

を使用することはできません `HTTPOnly` これらのファーストパーティ cookie で。 この `at.js` JavaScript ライブラリは、これらの Cookie に対する読み取り/書き込みが必要です。 これらの cookie は次のユーザーによって作成されます。 `at.js` とはサーバーから設定されません。

この `secure` 設定は、を使用して、これらすべての Cookie で有効にすることができます `secureOnly: true` での設定 `at.js`.

## サードパーティ Cookie

Adobe Target ユーザーは、カスタマイズされたサードパーティ cookie を作成できます。 次のサードパーティ cookie が次の場所に保存されています `tt.omtrdc.net`:

| Cookie | 詳細 |
| --- | --- |
| `customerclientcode!mboxPC` | クロスドメインが有効な場合に存在します。 |
| `customerclientcode!mboxSession` | クロスドメインが有効な場合に存在します。 |

これらのサードパーティ cookie は HTTPOnly により初期設定されており、Adobe Target Data Collection Server によって設定されます。

この `secure` 設定は、を使用して、すべての cookie で有効にできます `secureOnly: true` での設定 `at.js`.
