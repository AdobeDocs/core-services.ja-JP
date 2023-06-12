---
description: Adobe Target で Cookie を使用して、どのオンラインコンテンツおよびオファーが訪問者に対してより関連性が高いかを web サイトオペレーターがテストできるようにする方法について説明します。
solution: Experience Cloud,Analytics,Target
title: Adobe Targetの Cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: a1d24f95b1ac567686d58af8adf0132e5beb8f2a
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 24%

---

# Adobe Targetの Cookie

[!DNL Adobe Target] では、オンラインコンテンツのテスト機能を実現する目的と、より関連性の高いコンテンツを訪問者に対して表示する目的で、Web サイト運用者向けに cookie を使用します。

>[!NOTE]
>
>この記事の情報は、 [[!DNL Target] at.js JavaScript ライブラリ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=ja){target=_blank} のみ。
>
>Cookie に関する情報 [!DNL Target] を使用した実装 [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ja){target=_blank}, see "Does the [!DNL Adobe Experience Platform Web SDK] use cookies? If so, what cookies does it use?" in [Frequently Asked questions in the DNL Platform Web SDK overview guide](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html){target=_blank}.
>
>cookie の期間を除き、必要に応じて、この記事で説明する設定を変更できます。 [cookie の設定を変更する場合は、アカウント担当者にお問い合わせください。](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html?lang=ja){target=_blank}
>
>[!DNL Target] ユーザーは、カスタマイズされたサードパーティ cookie を作成することもできます。

## ファーストパーティ cookie

次のファーストパーティ Cookie は、お客様のドメインに保存されます。

| Cookie | 詳細 |
| --- | --- |
| mbox | 訪問者に関する匿名の識別子を格納します。<P>**Cookie ドメイン**:mbox を扱うドメイン。 この cookie は会社のドメインで提供されているので、cookie はファーストパーティ cookie になります。 例：`mycompany.com`いずれかのドメイン名に国コード ( `mycompany.co.uk`では、クライアントサービスと連携して、このコードをサポートするように at.js を設定します。 cookie ドメインのカスタマイズについて詳しくは、必要に応じて、`cookieDomain`」の下に [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=ja){target=_blank} 内 *[!DNL Adobe Target]開発者ガイド*.<P>**サーバードメイン**: `clientcode.tt.omtrdc.net`、 [!DNL Target] アカウント<P>**cookie の期間**:cookie が訪問者のブラウザーに残る期間は、最後にログインしてから 2 年です。 cookie の期間は変更できません。<P>cookie には、訪問者のエクスペリエンスを管理するための値がいくつか保持されます [!DNL Target] アクティビティ：<P>**session ID**:特定のユーザーセッションの一意の識別子。 デフォルトでは、セッションは 30 分間無操作状態が続くと有効期限が切れます。生成する `sessionId` 自分自身 ( 例えば [サーバー側実装](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}) で、以下を確認します。<ul><li>セッション ID は、空白、疑問符 ( ? ）、またはスラッシュ（ / ）以外の印刷可能な文字列を使用できます。</li><li>セッション ID の長さは 1 ～ 128 文字にする必要があります。</li><li>特定のセッションの場合、Cookie の値は、複数のリクエストで同じ値を保持する必要があります。</li><li>並列セッション（個別）を使用しないでください `sessionIds`) に含まれます。</li></ul>エッジクラスター内の特定のノードへのルーティングは、セッション ID を使用しておこなわれます。<ul><li>セッションは、サーバサイドで 30 分間アクティブです。したがって、特定の `tntId/thirdPartyId` が `tntId/thirdPartyId`. そうしないと、プロファイルに対する変更に一貫性がなく、予測できないことがあります。</li><li>新しいセッション ID は、訪問者が 30 分間操作を行わなかった場合に使用する必要があります。</li><li>同じセッション ID を複数の `tntIds/thirdPartyIds` は、 `tntId/thirdPartyIDs`.</li></ul>注意：詳しくは、 [同時リクエスト数の制限](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=ja#content-delivery){target=_blank} （特定のセッション ID）に対して割り当てられます。<P>**pc ID**:訪問者のブラウザーの半永久的な ID です。 cookie が手動で削除されるまで存続します。<P>**check**:訪問者が cookie をサポートしているかどうかを判断するために使用される単純なテスト値。 訪問者がページをリクエストするたびに設定されます。<P>**無効**:訪問者の読み込み時間が at.js ファイルで設定されているタイムアウトを超えた場合に設定されます。 デフォルトでは、このタイムアウトは 1 時間存続します。 |
| at_check | 一時的な cookie。ブラウザーで cookie の読み取り/書き込み機能が有効になっているかどうかを確認します。 |
| mboxEdgeCluster | この cookie は、次の場合にのみ存在します。 [overrideMboxEdgeServer 設定](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=ja){target=_blank} が `true`. |

これらのファーストパーティ Cookie では HTTPOnly を使用できません。 at.js JavaScript ライブラリは、これらの Cookie に対して読み取り/書き込みをおこなう必要があります。 これらの cookie は at.js によって作成され、サーバーからは設定されません。

この `secure` 設定は、 `secureOnly: true` at.js 実装の設定

## サードパーティ Cookie

次のサードパーティ Cookie は、に保存されます。 `tt.omtrdc.net`:

| Cookie | 詳細 |
| --- | --- |
| customerclientcode!mboxPC | クロスドメインが有効な場合、この cookie が存在します。 |
| customerclientcode!mboxSession | クロスドメインが有効な場合、この cookie が存在します。 |

これらのサードパーティ Cookie は、初期設定の状態では HTTPOnly で、 [!DNL Target] エッジサーバー。

この `secure` 設定は、 `secureOnly: true` at.js 実装の設定