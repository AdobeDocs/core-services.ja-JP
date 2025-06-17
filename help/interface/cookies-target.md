---
description: では Cookie を使用して  [!DNL Adobe Target]  訪問者により関連性の高いオンラインコンテンツやオファーを Web サイトオペレーターがテストできるようにする方法を説明します。
solution: Experience Cloud,Analytics,Target
title: Adobe Targetの cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: 95ca3a8e172166d7901873e0dc2e096e0bba7cd2
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 9%

---

# [!DNL Adobe Target] の cookie

[!DNL Adobe Target] では、オンラインコンテンツのテスト機能を実現する目的と、より関連性の高いコンテンツを訪問者に対して表示する目的で、Web サイト運用者向けに cookie を使用します。

>[!NOTE]
>
>この記事の内容は、[[!DNL Target] at.js JavaScript ライブラリ ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=ja){target=_blank} にのみ適用されます。
>
>[[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ja){target=_blank} を使用した [!DNL Target] 実装で使用される Cookie について詳しくは、「[!DNL Adobe Experience Platform Web SDK] で Cookie が使用されていますか？ その場合、どのような Cookie を使用しますか？」 [[!DNL Platform web SDKの概要ガイドのよくある質問 &#x200B;]](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=ja){target=_blank}。
>
>cookie の期間を除き、必要に応じて、この記事で説明する設定を変更できます。 cookie の設定を変更する場合は [ アカウント担当者にお問い合わせください ](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html?lang=ja){target=_blank}。
>
>カスタマイズ [!DNL Target] れたサードパーティ cookie を作成することもできます。

## ファーストパーティ cookie

次のファーストパーティ cookie が顧客のドメインに保存されます。

| Cookie | 詳細 |
| --- | --- |
| mbox | 訪問者に関する匿名識別子を格納します。<P>**Cookie ドメイン**:mbox の提供元のドメイン。 この cookie は会社のドメインから提供されるため、この cookie はファーストパーティ cookie です。 例：`mycompany.com`。ドメイン名に `mycompany.co.uk` などの国コードが含まれている場合は、クライアントサービスにお問い合わせの上、このコードをサポートするように at.js を設定してください。 Cookie ドメインのカスタマイズについて詳しくは、必要に応じて、『 *[!DNL Adobe Target]開発者ガイド [ の ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=ja){target=_blank}targetGlobalSettings* の「`cookieDomain`」を参照してください。<P>**サーバードメイン**:`clientcode.tt.omtrdc.net`。[!DNL Target] アカウントのクライアントコードを使用します。<P>**Cookie の期間**:Cookie は、最後にログインしてから 2 年間訪問者のブラウザーに残ります。 cookie の期間は変更できません。<P>Cookie には、訪問者のアクティビティのエクスペリエンスを管理するためにいくつかの値 [!DNL Target] 保持されています。<P>**セッション ID**：特定のユーザーセッションの一意の ID。 デフォルトでは、セッションは 30 分間無操作状態が続くと有効期限が切れます。`sessionId` を自分で生成する場合（例：[ サーバーサイド実装 ](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html?lang=ja){target=_blank}）は、次のことを確認します。<ul><li>セッション ID には、スペース、疑問符（? ）、中括弧（{ }）またはスラッシュ（/）。</li><li>セッション ID の長さは 1 ～ 128 文字にする必要があります。</li><li>特定のセッションでは、cookie の値は複数のリクエスト間で同じにする必要があります。</li><li>特定の訪問者に対して、どの時点でも並列セッション（個別の `sessionIds`）を使用しないでください。</li></ul>エッジクラスター内の特定のノードへのルーティングは、セッション ID を使用して行われます。<ul><li>セッションは、サーバサイドで 30 分間アクティブです。したがって、`tntId/thirdPartyId` で行われた最後のリクエストから 30 分以内に、特定の `tntId/thirdPartyId` ージに対して異なるセッション ID を使用しないでください。 そうしないと、プロファイルに対する変更に一貫性がなく、予測できないことがあります。</li><li>訪問者からの非アクティブ状態が 30 分間続いた後は、新しいセッション ID を使用する必要があります。</li><li>同じセッション ID を複数の `tntIds/thirdPartyIds` で使用すると、`tntId/thirdPartyIDs` で識別されるプロファイルに予期しない変更が加えられる可能性があります。</li></ul>注意：特定のセッション ID の [ 同時要求数の制限 ](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=ja#content-delivery){target=_blank} を参照してください。<P>**pc ID**：訪問者のブラウザーの半永久的な ID。 cookie が手動で削除されるまで存続します。<P>**チェック**：訪問者が Cookie をサポートしているかどうかを判断するために使用される単純なテスト値。 訪問者がページをリクエストするたびに設定されます。<P>**disable**：訪問者の読み込み時間が at.js ファイルで設定されているタイムアウトを超えた場合に設定されます。 デフォルトでは、このタイムアウトは 1 時間続きます。 |
| at_check | 一時的な cookie：ブラウザーで cookie の読み取り/書き込み機能が有効かどうかを確認します。 |
| mboxEdgeCluster | この Cookie は、[overrideMboxEdgeServer 設定 ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=ja){target=_blank} が `true` に設定されている場合にのみ存在します。 |

これらのファーストパーティ cookie で HTTPOnly を使用することはできません。 at.js JavaScript ライブラリは、これらの cookie に対する読み取り/書き込みが必要です。 これらの cookie は at.js で作成され、サーバーから設定されません。

`secure` 設定は、at.js 実装の `secureOnly: true` 設定を使用して、これらすべての cookie で有効にすることができます。

## サードパーティ Cookie

次のサードパーティ cookie が `tt.omtrdc.net` に保存されます。

| Cookie | 詳細 |
| --- | --- |
| customerclientcode!mboxPC | この cookie は、クロスドメインが有効な場合に存在します。 |
| customerclientcode!mboxSession | この cookie は、クロスドメインが有効な場合に存在します。 |

これらのサードパーティ cookie は HTTPOnly で標準で提供されており、[!DNL Target] エッジサーバーによって設定されます。

`secure` 設定は、at.js 実装の `secureOnly: true` 設定を使用して、すべての cookie で有効にすることができます。